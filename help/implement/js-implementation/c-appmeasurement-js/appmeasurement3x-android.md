---
description: AppMeasurement 3.x für Android
seo-description: Alte Dokumentation für AppMeasurement 3.x für Android
seo-title: AppMeasurement 3.x für Android
solution: Analytics
subtopic: Lesezeichen
title: AppMeasurement 3.x für Android
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 595efd52fe3b8edae32d8b3c2216ea066ec642be

---


# AppMeasurement 3.x für Android

*Hinweis: Dieses Dokument enthält ältere Informationen zu früheren Versionen von AppMeasurement, insbesondere zu den Versionen 3.x für Android.
Informationen zur aktuellen AppMeasurement-Implementierung finden Sie unter[Info zu AppMeasurement für JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).*

*Zuletzt aktualisiert am 15.03.2018 AppMeasurement 3.x für Android*

Mit Adobe AppMeasurement für Android können Sie native Android-Anwendungen in der Adobe Experience Cloud messen.

Dieser Leitfaden ist in zwei Abschnitte unterteilt: einen Abschnitt für Analyst mit Adobe Analytics-Erfahrung und einen Abschnitt für Android-Entwickler mit Erfahrung bei der Entwicklung von Apps für Mobilgeräte.

**Unterstützte Versionen**: Android 2.0 oder höher.

**Laden Sie die Bibliotheksdownloadanweisungen und -links für alle AppMeasurement-Mobilplattformen** herunter. Sie finden sie auf der Seite Measuring and OptimizingMobile Applications unter Developer Connection. Zum Herunterladen der Bibliotheken müssen Sie über ein kostenloses Developer Connection-Konto oder eine SiteCatalyst-Anmeldung verfügen. Die Downloadlinks werden erst nach der Anmeldung angezeigt.

## Schnellstart für Analysten

Dieser Abschnitt erläutert Ihnen schrittweise, wie Sie die Android-Bibliothek implementieren und den für die Standardimplementierung benötigten Code hinzufügen können. Weiterhin sind Schritte enthalten, die Ihnen veranschaulichen, wie Sie benutzerspezifische Ereignisse und andere Daten senden können.

Analysten müssen die Mobilanwendungsberichte für die Report Suite aktivieren. Wenn Sie zusätzliche Metriken erfassen müssen, sollten Sie dem Entwickler eine Beschreibung der Kontextdatenvariablen zur Verfügung stellen, die durch die Anwendung gesendet werden sollen. So können Sie beispielsweise Ihren Entwickler damit beauftragen, den Benutzernamen in eine Kontextdatenvariable mit dem Namen `myco.username` einzusetzen, um den Benutzernamen nach der Anmeldung zu erfassen.

### Mobilanwendungsberichte in SiteCatalyst aktivieren

SiteCatalyst bietet eine Oberfläche, über welche die Lebenszyklusverfolgung für Mobilanwendungen aktiviert werden kann. Durch diese Zuordnung erstellt SiteCatalyst automatisch die Mobilanwendungsberichte.

1. Öffnen Sie Admin-Konsole &gt; Report Suites &gt; Einstellungen bearbeiten &gt; Mobile Management (Mobilmanagement) &gt; Mobilanwendungs-Berichterstellung.
1. Klicken Sie auf Lebenszyklusverfolgung für Mobilanwendungen aktivieren.

Die Lebenszyklusmetriken werden nun erfasst und im Menü Berichte in SiteCatalyst werden die Mobilanwendungsberichte angezeigt.

### Mithilfe von Verarbeitungsregeln weitere Metriken erfassen

Wenn Ihre Implementierung zusätzliche Ereignisse und Dimensionen mithilfe von Kontextdaten sendet, müssen Sie Verarbeitungsregeln konfigurieren, um diese Daten zu erfassen.

Vor dem Erstellen von Verarbeitungsregeln muss eine Person in Ihrer Organisation zertifiziert werden. Weitere Informationen finden Sie in der Hilfe zu Verarbeitungsregeln.

Nach der Aktivierung der Verarbeitungsregeln veranschaulicht das Beispiel Kontextdatenvariable kopieren den Prozess, mit dem Kontextdaten zugeordnet werden.

### (Optional) Offline-Verfolgung aktivieren

Wenn Sie Treffer speichern möchten, während das Gerät offline ist, muss Ihre Report Suite zeitstempelfähig sein.

Nach dem Aktivieren der Offline-Verfolgung müssen alle Treffer mit einem Zeitstempel versehen werden. Andernfalls werden sie entfernt. Wenn sie aktuell AppMeasurement-Daten in einer Report Suite erfassen, in der auch Daten von JavaScript gesammelt werden, müssen Sie eventuell eine separate Report Suite für mobile Daten einrichten, um Datenverlust zu vermeiden. Sie können aber auch einen benutzerdefinierten Zeitstempel auf JavaScript-Treffer über die Variable s.timestamp einfügen.

Wenn Sie sich nicht sicher sind, ob Ihre Report Suite zeitstempelfähig ist, wenden Sie sich an den Kundendienst.

## Schnellstart für Entwickler

Dieser Abschnitt erläutert Ihnen schrittweise die Auswahl und Konfiguration von Ereignissen, eVars und Props, die Sie zur Sammlung von Android-Daten verwenden werden. Weiterhin sind Schritte enthalten, mit denen Sie Verarbeitungsregeln erstellen können, um die von den Android-Bibliotheken gesendeten Kontextdaten in diese Variablen zu kopieren.

Die Schritte zur Implementierung der Android-Bibliothek und zum Senden von Messungsdaten sind wie folgt:

* Bibliothek herunterladen
* Bibliothek zu Ihrem Projekt hinzufügen
* App-Berechtigungen hinzufügen
* Kurze Hinweise zu TrackingHelper
* Implementierung

### Bibliothek herunterladen

Gehen Sie zu Messen und Optimieren von mobilen Anwendungen auf Developer Connection, um die Android-Bibliothek herunterzuladen. Nach dem Entpacken der heruntergeladenen Datei verfügen Sie über die folgenden Software-Komponenten:

* admsAppLibrary.jar: Bibliothek, die zur Verwendung mit Android-Geräten und Simulatoren entwickelt wurde. Dafür ist Android 2.0 oder höher erforderlich.
* Examples\TrackingHelper.java: Eine optionale Klasse, die dazu bestimmt ist, Rück-Trackingcode und Ihre Anwendungslogik voneinander getrennt zu halten.

### Bibliothek zu Ihrem Projekt hinzufügen

1. Klicken Sie in der Eclipse IDE mit der rechten Maustaste auf den Projektnamen.
1. Wählen Sie Pfad aufbauen &gt; Externe Archive hinzufügen aus.
1. Auswählen `admsAppLibrary.jar`.
1. Klicken Sie auf Öffnen.
1. Klicken Sie erneut mit der rechten Maustaste auf das Projekt, wählen Sie dann Build Path (Pfad aufbauen) &gt; Configure Build Path (Pfadaufbau konfigurieren).
1. Klicken Sie auf die Registerkarte Order and Export (Ordnen und Exportieren).
1. Vergewissern Sie sich, dass `admsAppLibrary.jar` ausgewählt ist.

Ihre Anwendung kann die Klassen/Schnittstellen aus der Bibliothek "admsAppLibrary.jar"importieren, indem Sie "import com.adobe.ADMS"verwenden.*;

### App-Berechtigungen hinzufügen

Die AppMeasurement-Bibliothek erfordert folgende Berechtigungen, um Daten zu senden und Offline-Verfolgungsaufrufe aufzuzeichnen:

* INTERNET
* ACCESS_NETWORK_STATE

To add these permissions, add the following lines to your AndroidManifest.xml file (in the application project directory):
`<uses-permission android:name="android.permission.INTERNET" />`
`<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />`

### Kurze Hinweise zu TrackingHelper

Das SDK enthält eine zusätzliche optionale Klasse namens TrackingHelper. TrackingHelper bietet eine Methode, um Messungscode von der Anwendungslogik getrennt zu halten.

Sehen Sie sich das folgende Beispiel an: In Ihrer Anwendung möchten Sie ein Ereignis senden, das jede Anmeldung verfolgt. Sie könnten folgenden Code direkt nach Ihrem Anmeldecode hinzufügen, um dieses Ereignis zu senden (die Einzelheiten zum Code werden später erläutert):

```
Hashtable<String, Object> contextData = new Hashtable<String, Object>();
contextData.put("username", "username_value");
measure.trackEvents("event1", contextData);
```

Dieser direkte Ansatz ist zwar brauchbar. Möglicherweise möchten Sie diesen Code jedoch an einer anderen Stelle unterbringen, sodass er bei der Entwicklung Ihrer Applikation nicht im Weg ist. Diese „andere Stelle“ ist der TrackingHelper. Innerhalb von TrackingHelper können Sie diesen Code in der Methode mit der Bezeichnung trackLogonEvent unterbringen:

```
public static void trackLogonEvent (String username_value) {
Hashtable<String, Object> contextData = new Hashtable<String, Object>();
contextData.put("username", username_value);
measure.trackEvents("event1", contextData);
}
```

Im Anwendungscode können Sie ein Anmeldeereignis durch einen einfachen Aufruf von trackLogonEvent verfolgen:

TrackingHelper.trackLogonEvent("username");

Der Messungsaufruf im Code Ihrer Anwendung ist auf eine einzelne Zeile reduziert. Ein weiterer Vorteil besteht darin, dass bei einer notwendigen Änderung der zugrunde liegenden Messungslogik lediglich der TrackingHelper aktualisiert werden muss. Wenn ein anderer Entwickler Ihren Code ergänzt, kann dieser die von Ihnen definierten vereinfachten Methoden verwenden, ohne sich in die AppMeasurement Library einarbeiten zu müssen.

Wir gehen davon aus, dass Sie den TrackingHelper für neue Implementierungen bevorzugen, auch wenn für die Einrichtung zunächst etwas mehr Zeit benötigt wird. Die verbleibenden Schritte in diesem Leitfaden erläutern Ihnen, wie Sie TrackingHelper einrichten und mit dem Senden von Messungsdaten beginnen können.

Stellen Sie sicher, dass Sie TrackingHelper.java in ein Verzeichnis kopieren, das Klassendateien für Ihre App enthält, und ersetzen Sie den Paketnamen oben in der Datei durch einen Namen, der Ihrer Paketstruktur (com.company.application). entspricht. Wenn Sie die Implementierung ohne TrackingHelper durchführen möchten, finden Sie in TrackingHelper eine Reihe von Beispielen, die Sie in Ihre Anwendung kopieren können.

### Implementierung

1. Öffnen Sie TrackingHelper.java und aktualisieren Sie TRACKING_RSID und TRACKING_SERVER mit der Report Suite-ID und dem Tracking-Server. Beispiel:

   ```
   private static final String TRACKING_RSID = "rsid";
   private static final String TRACKING_SERVER = "server";
   ```

   Diese Werte sind erforderlich und müssen korrekt sein. Andernfalls funktioniert die Messung nicht. Fragen Sie Ihren SiteCatalyst-Experten, wenn Sie sich bezüglich dieser Werte unsicher sind.

2. Suchen Sie die configureAppMeasurement-Methode. Dort können Sie SSL sowie Offline-Verfolgung aktivieren und andere globale Änderungen an Ihrer Konfiguration vornehmen. Belassen Sie die Zeile zunächst ohne Kommentar, um debugLogging zu aktivieren, bis alles Ihren Erwartungen entsprechend funktioniert.

3. Fügen Sie aus der Root-Aktivität in Ihrer Anwendung einen Aufruf an configureAppMeasurement hinzu.

```
@Override
public void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.main);
TrackingHelper.configureAppMeasurement(this);
}
```

Dies ist der gesamte Code, der zur Verfolgung benutzerspezifischer Metriken benötigt wird. Mit einigen zusätzlichen Codezeilen können Sie jedoch die Lebenszyklusverfolgung aktivieren, um Lebenszyklusmetriken automatisch zu senden, einschließlich Starts, Aktualisierungen, Abstürzen sowie täglichen und monatlichen Benutzern.

Die AppMeasurement Library erledigt dabei den größten Teil der Arbeit. Sie müssen lediglich den einzelnen Activity-Klassen Ihrer Anwendung zwei Methodenaufrufe hinzufügen.

### (Empfohlen) Lebenszyklusereignisse verfolgen

Wenn die Lebenszyklusverfolgung aktiviert ist, wird jedes Mal, wenn Ihre App gestartet wird, ein Einzeltreffer gesendet, um Installationen, Upgrades, belegte Tage und die anderen Lebenszyklusmetriken zu verfolgen.

Um Lebenszyklusereignisse zu verfolgen, fügen Sie Ihrer Anwendung entsprechend dem folgenden Beispiel in jeder Aktivität Aufrufe der Methoden onResume() und onPause() hinzu. Wir empfehlen weiterhin, die Aktivität bzw. den Dienst als das Kontextobjekt und nicht als globalen Applikationskontext weiterzugeben.

```
@Override
protected void onResume() {
super.onResume();
TrackingHelper.startActivity(this);
}
@Override
protected void onPause() {
super.onPause();
TrackingHelper.stopActivity();
}
```

Das ist alles! Sie haben nun die grundlegende Lebenszyklusverfolgung in Ihrer Android-App implementiert. Nachdem Ihr Webanalyst SiteCatalyst für die Verarbeitung der von Ihnen berichteten AppMeasurement-Metriken konfiguriert hat, enthält Ihre SiteCatalyst Report Suite die Standard-Lebenszyklusmetriken.

Was Sie jetzt tun können:

* (Optional) Benutzerspezifische Ereignisse verfolgen. Fügen Sie benutzerspezifische Methoden zu TrackingHelper hinzu, um alle Ereignisse zu verfolgen, die Sie in Ihrer Anwendung messen möchten. Sie können diese Methoden hinzufügen, um zum Beispiel Anmeldevorgänge oder Einkäufe innerhalb der App usw. zu verfolgen.
* (Optional) App-Zustände verfolgen. Ein Anwendungszustand ähnelt einem Seitenabruf. Dieser Abschnitt veranschaulicht Ihnen, wie Sie eine benutzerspezifische Methode zu TrackingHelper hinzufügen können, um einen Anwendungszustand zu verfolgen.
* Schnellstart Videomessung. Fügen Sie Code hinzu, um Videometriken wie Videoabrufe, Gesamtabspielzeit und beliebte Videos zu verfolgen.

### (Optional) Benutzerspezifische Ereignisse verfolgen

Bei benutzerspezifischen Metriken handelt es sich um individuelle Erfolgsmetriken für Ihre Applikation. Sie können ein benutzerspezifisches Ereignis senden, wenn sich ein Benutzer anmeldet, einen Kauf innerhalb der App auslöst oder einen Link auf Ihre Facebook-Seite anklickt. Die Tracking Helper-Klasse enthält ein Beispiel für die Verfolgung eines benutzerspezifischen Ereignisses. Sie können diese Methode als Vorlage verwenden, um zusätzliche Verfolgungsmethoden für Ereignisse hinzuzufügen.

Legen Sie in TrackingHelper.java eine Verfolgungsmethode für benutzerspezifische Ereignisse fest:

```
public static void trackCustomEvents () {
Hashtable<String, Object> contextData = new Hashtable<String, Object>();
contextData.put("contextKey", "value");
measure.trackEvents("event1, event2", contextData);
}
```

Sie können diese Methode überall in Ihrem Code aufrufen, um ein benutzerspezifisches Ereignis zu verfolgen:

`TrackingHelper.trackCustomEvents();`

Mit diesem Vorgang können Sie so viele Ereignisverfolgungsmethoden hinzufügen, wie Sie benötigen. Im Abschnitt Kurzübersicht zu TrackingHelper finden Sie eine Beispielmethode zur Verfolgung eines Anmeldeereignisses.

### (Optional) App-Zustände verfolgen

Die Tracking Helper-Klasse enthält auch ein Beispiel für die Verfolgung eines Applikationszustandes. Die Verfolgung eines benutzerspezifischen Zustandes ähnelt der Verfolgung eines Ereignisses. Der einzige Unterschied besteht darin, dass Sie die trackAppState-Methode anstelle der trackEvents-Methode verwenden.

```
measure.trackAppState("name", contextData);
```

Bei der Berichterstellung schaltet trackAppState den Stand für die Seitenabrufe weiter, trackEvents dagegen nicht.

## Schnellstart Videomessung

Die Videomessung wird im Handbuch Videomessung mit SiteCatalyst beschrieben. Der allgemeine Prozess zur Videomessung ist für sämtliche AppMeasurement-Plattformen sehr ähnlich. Dieser Schnellstart-Abschnitt bietet eine grundlegende Übersicht über die Aufgaben für Entwickler sowie einige Codebeispiele.

Für Anwendung und Videoverfolgung wird mit admsAppLibrary die gleiche Bibliothek verwendet. Die Dokumentation bezieht sich auf diese Methoden als Medienmodul für plattformübergreifende Konsistenz.

Sie müssen eine Messungsinstanz konfigurieren, bevor Sie das Medienmodul benutzen können.

Führen Sie folgende Aufgaben aus, um die Videoverfolgung auf Android zu implementieren:

* Player-Ereignisse SiteCatalyst-Variablen zuordnen
* Meilensteine, Segmente und Aufrufhäufigkeit konfigurieren
* Player-Ereignisse verfolgen

### Player-Ereignisse SiteCatalyst-Variablen zuordnen

Zum Konfigurieren der Videomessung müssen Sie die SiteCatalyst-Ereignisse und eVars, die Sie für die Videoverfolgung ausgewählt haben, Kontextdatenvariablen zuordnen. Weitere Information erhalten Sie unter Videokonfiguration mit SiteCatalyst.

Ihr Webanalyst sollte Ihnen ein Arbeitsblatt zur Videoimplementierung zur Verfügung stellen, welches eine Liste der SiteCatalyst-Variablen enthält, die für den Empfang von Videodaten konfiguriert wurden:

* Videoname (eVar): eVar2
* Videoname (prop): prop2
* Segmente (eVar): eVar3
* Inhaltstyp (eVar): eVar1
* Videozeit (Ereignis): event3
* Videowiedergaben (Ereignis): event1
* Videobeendigungen (Ereignis): event7
* Videosegmentansichten (Ereignis): event2

1. Fügen Sie nach dem Code, den Sie in Implementierung hinzugefügt haben, den folgenden Code hinzu, sodass die von Ihnen ausgewählte SiteCatalyst-Variable mit dem Beispiel im Code ersetzt wird:

   ```
   ADMS_MediaMeasurement mediaMeasure = ADMS_MediaMeasurement.sharedInstance();
   Hashtable<String, Object> contextDataMapping = new Hashtable<String, Object>();
   contextDataMapping.put("a.media.name", "eVar2,prop2");
   contextDataMapping.put("a.media.segment", "eVar3");
   contextDataMapping.put("a.contentType", "eVar1"); //note that this is not in the .media
   namespace
   contextDataMapping.put("a.media.timePlayed", "event3");
   contextDataMapping.put("a.media.view", "event1");
   contextDataMapping.put("a.media.segmentView", "event2");
   contextDataMapping.put("a.media.complete", "event7");
   mediaMeasure.ContextDataMapping = contextDataMapping;
   ```

2. Meilensteine, Segmente und Aufrufhäufigkeit konfigurieren.

3. Player-Ereignisse verfolgen.


### Meilensteine, Segmente und Aufrufhäufigkeit konfigurieren

Mithilfe von Meilensteinen können Sie Ereignisse nach Erreichen eines bestimmten Punktes im Video senden. Mithilfe von Segmenten können Sie Ihr Video in Abschnitte unterteilen, wodurch eine genauere Verfolgung möglich ist. Mithilfe der Aufrufhäufigkeit können Sie in bestimmten Abständen Messungsaufrufe mit der Ansichtszeit senden. Weitere Informationen finden Sie unter Videometrik.

### Meilensteine zuordnen

Sie können Meilensteine auf Basis von Anteilen an der Gesamtlänge oder auf Basis der vergangenen Sekunden definieren. In diesem Beispiel werden Meilensteine als Anteil der Gesamtlänge definiert. Bei einem Video mit einer Länge von zwei Minuten sendet der folgende Code Meilensteinereignisse nach 30, 60 und 90 Sekunden.

```
Hashtable<String, Object> milestoneMapping = new Hashtable<String, Object>();
milestoneMapping.put("25", "event4");
milestoneMapping.put("50", "event5");
milestoneMapping.put("75", "event6");
contextDataMapping.put("a.media.milestones", milestoneMapping);
```


### Offset-Meilensteine zuordnen

In diesem Beispiel werden Meilensteine nach Anzahl der Sekunden definiert, die seit Beginn des Videos abgelaufen sind. Bei einem Video mit einer Länge von zwei Minuten sendet der folgende Code Meilensteinereignisse nach 20, 40 und 60 Sekunden, unabhängig von der Gesamtlänge des Videos.

```
Hashtable<String, Object> offsetMilestoneMapping = new Hashtable<String, Object>();
offsetMilestoneMapping.put("20", "event8");
offsetMilestoneMapping.put("40", "event9");
offsetMilestoneMapping.put("60", "event10");

contextDataMapping.put("a.media.offsetMilestones", offsetMilestoneMapping);
```

### Beispiele

```
//get sharedInstance
ADMS_MediaMeasurement mediaMeasure = ADMS_MediaMeasurement.sharedInstance();

//Track By Milestones:
mediaMeasure.trackMilestones = "25,50,75";

// track Milestones & segmentByMilestones:
mediaMeasure.trackMilestones = "25,50,75";
mediaMeasure.segmentByMilestones = true;

// track by seconds:
mediaMeasure.trackSeconds = 15;

// track Milestones & segmentByMilestones & seconds:
mediaMeasure.trackMilestones = "25,50,75";
mediaMeasure.segmentByMilestones = true;
mediaMeasure.trackSeconds = 15;

// track offsetMilestones & segmentByOffsetMilestones:
mediaMeasure.trackOffsetMilestones = "15,30,45,60,75,90";
mediaMeasure.segmentByOffsetMilestones = true;

// track offsetMilestones:
mediaMeasure.trackOffsetMilestones = "5,15,45";
```

### Player-Ereignisse verfolgen

Zur Videomessung müssen Sie Code hinzufügen, der dem Medienmodul mitteilt, wann Ereignisse in Ihrem Player auftreten (mithilfe der Methoden open, play, stop und close). Wenn ein Benutzer mit dem Abspielen eines Videos beginnt, müssen Sie die Methode play aufrufen, damit das Medienmodul beginnt, die abgelaufenen Sekunden zu zählen.

Wenn der Benutzer des Videos die Wiedergabe unterbricht, müssen Sie stop aufrufen, damit die Zählung unterbrochen wird. Dies wird üblicherweise mithilfe von Ereignishandlern erreicht, die durch Ihren Player freigelegt werden.

Beispiel:

Laden: open und play wird aufgerufen

Unterbrechen: stop wird aufgerufen. Wenn ein Benutzer z. B. die Wiedergabe eines Videos nach 15 Sekunden unterbricht, wird stop(„Video1“,15) aufgerufen

Zwischenspeichern: stop wird aufgerufen, während das Video zwischengespeichert wird. play wird aufgerufen, wenn die Wiedergabe fortgesetzt wird.

Fortsetzen: play wird aufgerufen. Wenn ein Benutzer z. B. das Video nach dem anfänglichen Abspielen von 15 Sekunden und der Pause fortsetzt, wird s.play(„Video1“,15) aufgerufen.

Scrubbing (Regler): Wenn der Benutzer den Videoregler zieht, wird stop aufgerufen. Bei Freigabe des Videoreglers wird play aufgerufen.

Beenden: stop wird aufgerufen und anschließend close. Beispielsweise wird am Ende eines 100-Sekunden-Videos stop(„Video1“,100) aufgerufen und anschließend close(„Video1“).

Um dies zu erreichen, können Sie vier anwenderspezifische Funktionen definieren, die Sie über die Media Player-Ereignishandler aufrufen können. Die verschiedenen Parameter, die an open, play, stop und close weitergegeben werden, stammen aus dem Player. Das folgende Pseudocode-Beispiel zeigt, wie dies erreicht wird:

```
function startMovie(){
mediaMeasure.open(mediaName,mediaLength,mediaPlayerName);
playMovie();
}
/*Call on video resume from pause and slider release*/
function playMovie(){
mediaMeasure.play(mediaName,mediaOffset);
}
/*Call on video pause and slider grab*/
function stopMovie(){
mediaMeasure.stop(mediaName,mediaOffset);
}
/*Call on video end*/
function endMovie(){
stopMovie();
mediaMeasure.close(mediaName);
Video Measurement Quick Start 12
```

## Lebenszyklusmetriken

Dieses Arbeitsblatt listet die Metriken und Dimensionen auf, die bei aktivierter automatischer Lebenszyklusverfolgung gemessen werden.

### Lebenszyklusmetriken und -dimensionen

Wenn Lebenszyklusmetriken konfiguriert sind, werden sie in Kontextdatenparametern an Analytics, in Parametern an Target bei jedem mbox-Aufruf und als Signal an das Zielgruppen-Management gesendet. Analytics und Target verwenden dasselbe Format, während das Zielgruppen-Management ein anderes Präfix für jede Metrik verwendet.

Bei Analytics werden die mit jedem Lebenszyklus-Tracking-Aufruf gesendeten Kontextdaten automatisch in der in der ersten Spalte aufgeführten Metrik oder Dimension erfasst und damit gemeldet (eventuelle Ausnahmen werden in der Spalte „Beschreibung“ genannt).

| Metrik | Analytics-Kontext | Analytics Context Audience Manager - Signalbeschreibung | Daten-/Target-Parameter |
|--- |--- |--- |--- |
| Erste Starts | a.InstallEvent | c_a_InstallEvent | Wird beim ersten Ausführen nach einer Installation (oder Neuinstallation) ausgelöst. |
| Aktualisierungen | a.UpgradeEvent | c_a_UpgradeEvent | Wird bei der ersten Ausführung nach der Aktualisierung ausgelöst (bei jeder Änderung der Versionsnummer). |
| Täglich beteiligte Benutzer | a.DailyEngUserEvent | c_a_DailyEngUserEvent | Wird ausgelöst, wenn die Anwendung an einem bestimmten Tag verwendet wird. |
| Monatlich beteiligte Benutzer | Monatlich beteiligte Benutzer | a.MonthlyEngUserEvent | Wird ausgelöst, wenn die Anwendung während eines bestimmten Monats verwendet wird. |
| Starts | a.LaunchEvent | c_a_LaunchEvent | Wird bei jeder Ausführung ausgelöst, einschließlich Abstürzen und Installationen. | Starts werden auch bei einer Wiederaufnahme aus dem Hintergrund ausgelöst, wenn der Timeout der Lebenszyklussitzung überschritten wurde. |
| Abstürze | a.CrashEvent | c_a_CrashEvent | Wird ausgelöst, wenn die Applikation nicht kontrolliert herunterfährt. Das Ereignis wird beim Start der Applikation nach einem Absturz gesendet (die Applikation gilt als abgestürzt, wenn der Befehl zum Beenden nicht aufgerufen wurde). |
| Länge der vorherigen Sitzung | a.PreviousSessionLength | Cc_a_PreviousSessionLength | Aggregierte Gesamtdauer der vorherigen Sitzung in Sekunden. |

*Hinweis: Die **täglich eingebundenen Benutzer**und **monatlich eingebundenen Benutzer**werden nicht automatisch in einer Analytics-Metrik gespeichert. Sie müssen eine Verarbeitungsregel erstellen, die ein benutzerdefiniertes Ereignis zum Erfassen dieser Metriken festlegt.*

### Dimensionen

| Metrik | Analytics-Kontextdaten/Target-Parameter | Analytics Context Audience Manager-Signal | Beschreibung |
|--- |--- |--- |--- |
| Installationsdatum | a.InstallDate | c_a_InstallDate | Datum des ersten Starts nach der Installation. MM/TT/JJJJ |
| Aktualisierungen | a.UpgradeEvent | c_a_UpgradeEvent | Wird bei der ersten Ausführung nach der Aktualisierung ausgelöst (bei jeder Änderung der Versionsnummer). |
| App-ID | a.AppID | c_a_AppID | Speichert den Applikationsnamen und die Version im folgenden Format:`[AppName] [BundleVersion]`. Beispiel: myapp 1.1. |
| Tage seit der ersten Benutzung | a.DaysSinceFirstUse | c_a_DaysSinceFirstUse | Anzahl der Tage seit dem ersten Ausführen. |
| Monatlich beteiligte Benutzer | Monatlich beteiligte Benutzer | a.MonthlyEngUserEvent | Wird ausgelöst, wenn die Anwendung während eines bestimmten Monats verwendet wird. |
| Starts | a.LaunchEvent | c_a_LaunchEvent | Wird bei jeder Ausführung ausgelöst, einschließlich Abstürzen und Installationen. | Starts werden auch bei einer Wiederaufnahme aus dem Hintergrund ausgelöst, wenn der Timeout der Lebenszyklussitzung überschritten wurde. |
| Abstürze | a.CrashEvent | c_a_CrashEvent | Wird ausgelöst, wenn die Applikation nicht kontrolliert herunterfährt. Das Ereignis wird beim Start der Applikation nach einem Absturz gesendet (die Applikation gilt als abgestürzt, wenn der Befehl zum Beenden nicht aufgerufen wurde). |
| Länge der vorherigen Sitzung | a.PreviousSessionLength | Cc_a_PreviousSessionLength | Aggregierte Gesamtdauer der vorherigen Sitzung in Sekunden. |
| Tage seit der letzten Benutzung | a.DaysSinceLastUse | c_a_DaysSinceLastUse | Anzahl der Tage seit der letzten Verwendung. |
| Wochentag | a.DayOfWeek | c_a_DayOfWeek | Nummer des Wochentags, an dem die Applikation gestartet wurde. |
| Stunde des Tages | a.HourOfDay | c_a_HourOfDay | Misst die Stunde, in der die App gestartet wurde. Numerisches 24-Stunden-Format. Wird für die Zeitaufteilung verwendet, um Spitzennutzungszeiten zu ermitteln. |
| Betriebssystemversion | a.OSVersion | c_a_OSVersion | Betriebssystemversion. |
| Tage seit der letzten Aktualisierung | a.DaysSinceLastUpgrade | c_a_DaysSinceLastUpgrade | Anzahl der Tage seit der Änderung der Versionsnummer der Applikation. |
| Starts seit der letzten Aktualisierung | a.LaunchesSinceUpgrade | c_a_LaunchesSinceUpgrade | Anzahl der Starts seit der Änderung der Versionsnummer der Applikation. |
| Gerätename | a.DeviceName | c_a_DeviceName | Speichert den Gerätenamen. | iOS: Zweistellige, kommagetrennte Zeichenfolge, die das iOS-Gerät bezeichnet. Die erste Ziffer steht üblicherweise für die Gerätegeneration, die zweite weist die Version der verschiedenen Mitglieder der Gerätefamilie aus. Eine Liste der häufig verwendeten Gerätenamen finden Sie im Abschntt iOS-Geräteversionen. |
| Betreibername | a.CarrierName | c_a_CarrierName | Speichert den vom Gerät angegebenen Namen des Mobilfunkanbieters. |
| Auflösung | a.Resolution | c_a_Resolution | Breite x Höhe in Pixel |

*Hinweis: Die **Tage seit der letzten Aktualisierung**, die **Starts seit der letzten Aktualisierung**und der **Betreibername**werden nicht automatisch in einer Analytics-Variablen gespeichert. You must create a processing rule to copy these values to an Analytics variable for reporting.*

## Kontextdaten

Kontextdaten sind die bevorzugte Methode zum Senden von Applikationsdaten an Erfassungsserver.

Anstelle der expliziten Zuweisung von Werten an Props und eVars können Sie Kontextdatenvariablen verwenden, um Paare von Namenswerten zu senden, die in SiteCatalyst zugeordnet werden. Auf der Grundlage dieser Schlüsselwertpaare können Sie Ereignisse einstellen, Werte in eVars und Props kopieren und zusätzliche bedingte Anweisungen ausführen. Damit wird vermieden, dass Sie Codeaktualisierungen durchführen, um verschiedene Report Suite-Konfigurationen zu unterstützen.

Es gibt zwei Möglichkeiten, Kontextdaten mit den Verfolgungsmethoden zu senden. Alle Kontextdaten, die direkt auf dem PersistentContextData-Objekt festgelegt wurden, werden mit jedem Aufruf gesendet. Sie können Kontextdaten auch als Parameter an einen einzigen Verfolgungsaufruf weitergeben, der nur mit diesem Aufruf gesendet wird.

### Beständige Kontextdaten

Werte, die in den beständigen Kontextdaten platziert sind, werden mit jedem Server-Aufruf gesendet. Im folgenden Beispiel werden „Schlüssel“ und „Wert“ mit allen trackAppState-Aufrufen gesendet:

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.setPersistentContextData(contextData);
measure.trackAppState("state1");
measure.trackAppState("state2");
measure.trackAppState("state3");
```

### Kontextdaten mit einzelnem Aufruf 

Um Kontextdaten mit einem einzelnen Aufruf zu senden, senden Sie Kontextdaten als Parameter an den Verfolgungsaufruf (trackAppState, trackEvents usw.).

Im folgenden Beispiel werden „Schlüssel“ und „Wert“ mit allen trackAppState-Aufrufen gesendet: „key2“ und „value2“ werden jedoch nur mit dem zweiten trackAppState-Aufruf gesendet:

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.setPersistentContextData = contextData;
Hashtable<String, Object> contextDataState = new HashTable<String,Object>();
contextDataState.put("key2", "value2");
measure.trackAppState("state1");
measure.trackAppState("state2", contextDataState);
measure.trackAppState("state3");
```

## Konfigurationsvariablen

Die folgenden Variablen werden beim Start der Applikation eingestellt:

*Hinweis: Mit Ausnahme von ReportSuiteID und trackingServer sind alle Konfigurationsvariablen optional.*

**Freigegebene Instanz**

Bevor Sie Messungsaufrufe durchführen, müssen Sie eine Instanz der Bibliothek für jede Methode abrufen, die Sie in der Measurement Library aufrufen:

```
ADMS_Measurement measure = ADMS_Measurement.sharedInstance(((Activity)
context).getApplication());
```

*Hinweis: Konfigurationsvariablen sind privat. Verwenden Sie die Methoden zum Abrufen und Einstellen, um diese Werte zu ändern.*

### Konfigurationsvariablen

**reportSuiteIDs**: (Erforderlich) Die Report Suite oder Report Suites (Multi-Suite-Tagging), die verfolgt werden sollen. Übergeben Sie eine kommagetrennte Liste mit den Namen der einzelnen Report Suites, um mehrere Report Suites zu verfolgen.

Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:

```
String getReportSuiteIDs()
void setReportSuiteIDs(String reportSuiteIDs)
```

Beispiele:

`measure.setReportSuiteIDs("rsid");`

Multi-Suite-Tagging:
`measure.setReportSuiteIDs("rsid1, rsid2");`

**trackingServer**: (Erforderlich) Identifiziert den Erfassungsserver.

Diese Variable sollte mit der Domäne Ihres Tracking-Servers gefüllt werden (ohne das Protokollpräfix „http://“ oder „https://“). Das Protokollpräfix wird anhand der Variable ssl automatisch von der Bibliothek verarbeitet.

Wenn ssl auf true gesetzt ist, wird eine sichere Verbindung zu diesem Server hergestellt. Wenn ssl auf false gesetzt ist, wird eine nicht sichere Verbindung zu diesem Server hergestellt.

Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:

```
String getTrackingServer()
void setTrackingServer(String trackingServer)
```

Beispiele:

`measure.setTrackingServer("metrics.corp1.com");`

**visitorID**: Standard: uuidUnique identifier für jeden Besucher. Wenn Sie keine benutzerspezifische visitorID einstellen, wird eine individuelle visitorID generiert.

Wir empfehlen die Verwendung der Standard-ID, wenn kein besonderes Verwendungsszenario für eine visitorID vorliegt. Das Festlegen einer benutzerspezifischen visitorID kann bei Verwendung der Lebenszyklusverfolgung zu Besuchsdoppelungen führen. Legen Sie die visitorID fest, bevor Sie App Measurement konfigurieren, um diese Situation auszuschließen.

**characterSet**: Standard ist UTF-8

Syntax:

```
String getCharSet()
void setCharSet(String charSet)
```

Beispiele:
`[measure.setCharacterSet("UTF-8");`

**currencyCode**: Der Standardwert ist none (für die Report Suite definierter Wert wird verwendet)

Der Währungscode, der für Kauf- oder Währungsereignisse verwendet wird, die in der Android-Anwendung verfolgt werden.

Syntax:

```
String getCurrencyCode()
void setCurrencyCode(String currencyCode)
```

Beispiele:
`measure.setCurrencyCode("USD");`

**lifecycleSessionTimeout**: Standardwert ist 5 Minuten

Legt die Dauer in Sekunden fest, die zwischen verschiedenen Startvorgängen einer App verstreichen muss, damit ein Startvorgang als neue Sitzung gilt. Dieses Zeitlimit wird auch angewendet, wenn eine Anwendung in den Hintergrund verschoben und später reaktiviert wird. Die Dauer, für welche die App im Hintergrund ausgeführt wird, wird nicht in die Sitzungsdauer eingerechnet.

Syntax:

```
int getLifecycleSessionTimeout()
void setLifecycleSessionTimeout(int sessionLength)
```

Beispiele:

`measure.setLifecycleSessionTimeout(600); //10 minute session`

**ssl**: Standard ist false

Aktiviert (true) oder deaktiviert (false) das Senden der Messdaten über SSL (HTTPS). Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:

`void setSSL(boolean ssl)`

Beispiele:

`measure.setSSL(true);`

**debugLogging** Der Standardwert ist false

Aktiviert (true) oder deaktiviert (false) die Anzeige-Debug-Informationen und die Bibliotheksversion in der Ausgabekonsole. Für die Variable ist standardmäßig „false“ festgelegt. Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:

`void setDebugLogging(boolean debugLogging)`

Beispiele:

`measure.setDebugLogging(true);`

## Verfolgungsvariablen

**Freigegebene Instanz**

Bevor Sie Messungsaufrufe durchführen, müssen Sie eine Instanz der Bibliothek für jede Methode abrufen, die Sie in der Measurement Library aufrufen:

```
ADMS_Measurement measure = ADMS_Measurement.sharedInstance(((Activity)
context).getApplication());
```

*Hinweis: Konfigurationsvariablen sind privat. Verwenden Sie die Methoden zum Abrufen und Einstellen, um diese Werte zu ändern.*

### Beständige Verfolgungsvariablen

**eVar**: Legt für die angegebene eVar den bereitgestellten Wert fest. Die eVar wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wird oder bis „clear vars“ aufgerufen wird.

Syntax:

`void setEvar(int evarNum, String evarValue)`

Beispiel:
`measure.setEvar(1, "value");`

**Eigenschaft**: Legt für die angegebene Eigenschaftsvariable den bereitgestellten Wert fest. Die prop wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wir oder bis der Aufruf clearVars erfolgt.

Syntax:

`void setProp(int propNum, String propValue)`

Beispiel:

`measure.setProp(1, "value");`

**Hier**: Legt für die angegebene Nachfolgevariable den bereitgestellten Wert fest. Die hier-Variable wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wird oder bis der Aufruf clearVars erfolgt.

Syntax:

`void setHier(int hierNum, String hierValue)`

Beispiel:

`measure.setHier(1, "value");`


**ListVar**: Legt für die angegebene listVar den bereitgestellten Wert fest. Die listVar wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wird oder bis der Aufruf clearVars erfolgt.

Syntax:

`void setListVar(int listNum, String listValue)`

Beispiel:

`measure.setListVar(1, "value");`

**purchaseID**: Die purchaseID verhindert, dass eine Bestellung von SiteCatalyst mehrmals gezählt wird.

Immer wenn das Kaufereignis auf Ihrer Site verwendet wird, sollten Sie diesem Kauf über die purchaseID-Variable eine eindeutige ID zuweisen.

`measure.setPurchaseID("unique_id");`

**transactionID**: Integration-Data Sources verwenden eine Transaktions-ID, um Offlinedaten mit einer Online-Transaktion zu verknüpfen (z. B. ein online generierter Lead oder Einkauf).

Jede eindeutige an Adobe gesendete transactionID wird aufgezeichnet, um den Datenquellenupload von Offlineinformationen zu dieser Transaktion vorzubereiten.

`measure.setTransactionID("unique_id");`

**appState**: (Seitenname) Der für den App-Status angegebene Wert wird in der Variablen "pageName"gespeichert.

`measure.setAppState("state");`

**channel**: measure.setChannel("mobile");

**appSection**: Der für den App-Abschnitt bereitgestellte Wert wird in der Servervariablen gespeichert.

Syntax:

`void setAppSection(String Section)`

Beispiel:
`measure.setAppSection("news");`

**Kampagne**

Syntax:

`void setCampaign(String Campaign)`

Beispiel:

`measure.setCampaign("112233");`

**„products“**

Syntax:

```
void setProducts(String Products)
// example Products string: Category;Product[,Category;Product]
```

Beispiel:

`measure.setProducts("Running;Shoe");`

**events**

Syntax:

`void setEvents(String Event) //comma-delimited list`

Beispiel:

`measure.setEvents("event1, event2");`

**geoState**

Syntax:

`void setGeoState(String GeoState)`

Beispiel:

`measure.setGeoState("UT");`

**geoZip**

Syntax:

`void setGeoZip(String GeoZip)`

Beispiel:

`measure.setGeoZip("12345");`

**Beständige Kontextdaten**: Werte, die in "Persistente Kontextdaten"platziert werden, werden mit jedem Serveraufruf gesendet. Um Kontextdaten mit einem einzelnen Aufruf zu senden, senden Sie eine contextData-Hash-Tabelle als Parameter an den Verfolgungsaufruf (trackAppState, trackEvents usw.).

Beispiel:

```
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
measure.setPersistentContextData(contextData);
```

Siehe Kontextdaten.

**linkTrackVars**: Eine kommagetrennte Liste mit Variablennamen, die den aktuellen Variablensatz zur Linktracking eingrenzt. Wenn linkTrackVars nicht definiert ist, sendet AppMeasurement für Android alle definierten Variablen mit einem trackLink-Aufruf.

Syntax:

`void setLinkTrackVars(String Vars) //comma-delimited list`

Beispiel:

`measure.setLinkTrackVars("eVar1, prop1");`

**linkTrackEvents**: Eine kommagetrennte Liste von Ereignissen, die den aktuellen Ereignissatz zur Linktracking eingrenzt. Wenn linkTrackEvents nicht definiert ist, sendet AppMeasurement für Android alle Ereignisse mit einem trackLink-Aufruf.

Syntax:

`void setLinkTrackEvents(String Events) //comma-delimited list`

Beispiel:

`measure.setLinkTrackEvents("event1, event2");`

## Methoden

Dieser Abschnitt enthält eine Liste der Methoden, die durch die Android-Bibliothek zur Verfügung gestellt werden.

**Freigegebene Instanz**

Bevor Sie Messungsaufrufe durchführen, müssen Sie eine Instanz der Bibliothek für jede Methode abrufen, die Sie in der Measurement Library aufrufen:

```
ADMS_Measurement measure = ADMS_Measurement.sharedInstance(((Activity)
context).getApplication());
```

### Ausgangskonfiguration

Diese Methode konfiguriert die erforderlichen Variablen und muss daher vor anderen Methoden aufgerufen werden.

**configureMeasurement**: Diese Methode wird verwendet, um die beiden Parameter zu konfigurieren, die zum Starten der Anwendungsmessung erforderlich sind. Vor dem Senden von Server-Aufrufen müssen Sie die Werte reportSuiteIDs und trackingServer für das Messungsobjekt festlegen, das diese Methode verwendet.

Syntax:

`void configureMeasurement(String reportSuiteIDs, String trackingServer)`

Beispiele:

`measure.configureMeasurement("my_rsid", "my_tracking_server");`

### Ereignis- und Zustandsverfolgung

Dies sind die vorrangig verwendeten Methoden zur Verfolgung von benutzerspezifischen Ereignissen und App-Zuständen.

**trackAppState**: Dies ist die empfohlene Methode zur Verfolgung von Anwendungszuständen in Ihrer Anwendung. Der in appState bereitgestellte Wert wird als Seitennamenvariable des Server-Aufrufs angezeigt. Die Zeichenfolge appState muss für jeden Aufruf angegeben werden, da sie nicht in den nächsten Aufruf übernommen wird.

Kontextdaten, die mit diesem Aufruf gesendet werden, werden an beliebige Werte in persistentContextData angehängt und mit dem Aufruf gesendet. Lediglich die in persistentContextData festgelegten Werte verbleiben für den nächsten Aufruf.

Syntax:

`void trackAppState(string AppStateName)`

Beispiele:

`measure.trackAppState("state");`

```
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
measure.trackAppState("state", contextData);
```

**trackEvents**: Dies ist die empfohlene Methode zur Verfolgung von Ereignissen in Ihrer Anwendung. trackEvents ähnelt trackAppState, sendet jedoch Ereignisse anstelle von Seitennamen. Ereignisse werden als kommagetrennte Zeichenfolgen bereitgestellt. Die Zeichenfolge events muss für jeden Aufruf angegeben werden, da sie nicht in den nächsten Aufruf übernommen wird.

Diese Methode führt einen zugrunde liegenden Aufruf an trackLinkURL aus, wobei linkURL auf null, linkType auf "o"festgelegt ist und linkName mit der Anwendungs-ID ausgefüllt wird.

Das bedeutet, dass Ihre linkTrackVars und linkTrackEvents für Aufrufe von trackEvents gelten.

Kontextdaten, die mit diesem Aufruf gesendet werden, werden an beliebige Werte in persistentContextData angehängt und mit dem Aufruf gesendet. Lediglich die in persistentContextData festgelegten Werte verbleiben für den nächsten Aufruf.

Syntax:

`void trackEvents(string Events)`

Beispiele:

`measure.trackEvents("event1");`

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.trackEvents("event1", contextData);
```

**Importhinweis für die Verwendung der trackLink-Methode**

trackEvents unternimmt einen zugrundeliegenden Aufruf an trackLink, wobei linkURL auf null und linkType auf „o“ festgelegt ist und der linkName mit der Anwendungs-ID ausgefüllt wird. Dies erfolgt, um zu verhindern, dass bei jedem Senden eines Ereignisses die Anzahl der Seitenansichten (Zustandsansicht) erhöht wird.

Wenn Sie trackLink direkt aufrufen und Werte für linkTrackVars und linkTrackEvents einstellen, werden diese Beschränkungen für Variablen und Ereignisse für TrackEvents angewendet. Das bedeutet, dass lediglich die auf diesen Listen festgelegten Variablen und Ereignisse mit TrackEvents gesendet werden. Sie sollten linkTrackVars und linkTrackEvents auf null setzen, wenn Sie nicht wünschen, dass diese Beschränkungen auf trackEvents angewendet werden.

### Erweiterte Verfolgung (Track und TrackLink)

Diese Methoden bieten zusätzliche Optionen für die Verfolgung, mit denen Sie Props, eVars und andere SiteCatalyst-Variablen direkt ausfüllen können. Diese sollten von Kunden mit einer vorhandenen Implementierung verwendet werden oder von Kunden, die mit anderen SiteCatalyst-Implementierungen sehr vertraut sind.

`track` und `trackLink` sind die wichtigsten Messungsmethoden, die in allen Versionen der Adobe Measurement Libraries auf mehreren Plattformen implementiert sind. Bei der Verfolgung von Mobilanwendungen ist es in den meisten Fällen leichter, trackAppState oder trackEvents-Methoden zu verwenden, anstatt „track“ und trackLink direkt aufzurufen.

Seitenabrufverfolgung (track) und Linktracking (trackLink) senden alle beständigen Variablen mit Werten (nicht null, nicht leer, nicht 0). Sie sollten bei Bedarf alle Variablen zurücksetzen oder leeren, bevor Sie track oder trackLink aufrufen.

*Hinweis: Aufgrund der Multi-Thread-Charakteristik moderner Anwendungen ist es nicht empfehlenswert, beständige Variablenwerte festzulegen, die mit einem zukünftigen Verfolgungsaufruf gesendet werden (mit setEvar, setProp, setHier, SetListVar und setPersistentContextData). Wenn beispielsweise ein Variablenwert in mehreren Threads festgelegt ist, befindet sich der Wert möglicherweise in einem inkonsistenten Zustand, wenn die Verfolgung durchgeführt wird. Um diese Situation auszuschließen, empfehlen wir, Kontextdaten mit jedem Verfolgungsaufruf zu übergeben und den Variablenwert in den Verarbeitungsregeln festzulegen.

**Methodenbeschreibungen**

**track**: Sendet eine Standardseitenansicht zusammen mit weiteren Variablen, die für das Messungsobjekt festgelegt sind, an den Erfassungsserver.

Jeder Aufruf von „track“ sendet sämtliche für das Messungsobjekt definierten Daten (diese werden in der Beschreibung zu clearVars aufgelistet) sowie weitere contextData bzw. Variablen, die Sie lediglich für diesen Aufruf angeben. Wenn Sie eine definierte Variable senden, werden Werte in der entsprechenden beständigen Variable überschrieben.

Syntax:

```
void track()
void track(Hashtable<String, Object> contextData)
void track(Hashtable<String, Object> contextData, Hashtable<String, Object>
variables)
```

Beispiele:

`measure.track();`

```
measure.setEvar(1, "evar1value");
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
measure.track(contextData);
```

```
//set an eVar
measure.setEvar(1, "evar1value");
//contextData
Hashtable contextData = new Hashtable<String, Object>();
contextData.put("key", "value");
//variable overrides
Hashtable variableOverrides = new Hashtable<String, Object>();
variableOverrides.put("evar2", "evar2value");
//sends eVar1, eVar2 (set in overrides), and context data
measure.track(contextData, variableOverrides);
```

**trackLink**: Sendet benutzerspezifische, Download- oder Ausstiegslink-Daten zusammen mit beliebigen trackconfig-Variablen mit Werten an Adobe-Datenerfassungsserver.

Verwenden Sie trackLink, um alle Aktivitäten zu verfolgen, die keinen Seitenabruf erfassen sollen.

Syntax:

```
void trackLink(String linkURL, String linkType, String linkName,
Hashtable<String, Object> contextData, Hashtable<String, Object> variables)
```

**linkURL**: Bestimmt die angeklickte URL. Wenn keine URL angegeben ist, wird der Name verwendet. Verwenden Sie diese Option nur, wenn Sie von der Android-Anwendung aus per Link eine Webseite aufrufen. Geben Sie andernfalls null für diesen Parameter an.

**linkType**: Bestimmt den Link-Bericht, der diese URL oder den Namen anzeigt. Folgende Werte werden unterstützt:
* „o“ (Benutzerdefinierte Links)
* „d“ (Datei-Downloads)
* „e“ (Exitlinks)

**linkName**: Der Name, der im Link-Bericht steht. Wenn kein Name angegeben ist, verwendet der Bericht die URL.

Zur Datenerfassung müssen Sie entweder den linkURL- oder den linkName-Parameter angeben. Geben Sie null als Wert an, wenn Sie keinen dieser Parameter, Kontextdaten oder zusätzliche Variablen verwenden.

Beispiele:

`measure.trackLink("url", "o", "name", contextData, null);`

**setEvar**: Legt für die angegebene eVar den bereitgestellten Wert fest. Die eVar wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wird oder bis „clear vars“ aufgerufen wird.

Syntax:

`void setEvar(int evarNum, String evarValue)`

**setProp**: Legt für die angegebene Eigenschaftsvariable den bereitgestellten Wert fest. Der prop wird solange mit allen Verfolgungsaufrufen gesendet, bis er durch Festlegen einer leeren Zeichenfolge geleert wird oder bis der Aufruf „clear vars“ erfolgt.

Syntax:

`void setProp(int propNum, String propValue)`

**setHier**: Legt für die angegebene Nachfolgevariable den bereitgestellten Wert fest. Die Nachfolgevariable wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wird oder bis der Aufruf „clear vars“ erfolgt.

Syntax:

`void setHier(int hierNum, String hierValue)`

**setListVar**: Legt für die angegebene listVar den bereitgestellten Wert fest. Die listVar wird solange mit allen Verfolgungsaufrufen gesendet, bis sie durch Festlegen einer leeren Zeichenfolge geleert wird oder bis „clear vars“ aufgerufen wird.

Syntax:

`void setListVar(int listNum, String listValue)`

**setPersistentContextData**: Werte, die in "Persistente Kontextdaten"platziert werden, werden mit jedem Serveraufruf gesendet. Um Kontextdaten mit einem einzelnen Aufruf zu senden, senden Sie eine contextData-Hash-Tabelle als Parameter an den Verfolgungsaufruf (trackAppState, trackEvents usw.).

```
Hashtable<String, Object> contextData = new HashTable<String,Object>();
contextData.put("key", "value");
measure.setPersistentContextData(contextData);
```

Siehe Kontextdaten.

**clearVars**: Entfernt Werte aus den folgenden Variablen im Objekt:

```
props
eVars
heirs
listVars
events
PersistentContextData
purchaseID
transactionID
appState
channel
appSection
campaign
products
geoZip
geoState
linkTrackVars
linkTrackEvents
```

Syntax:

`void clearVars()`

Beispiele:
`measure.clearVars();`

**Offline-Verfolgung**

*Hinweis: Um Offline-AppMeasurement zu aktivieren, muss Ihre Report Suite zeitstempelfähig sein.*

Mithilfe der folgenden Variablen können Sie Messungsaufrufe speichern, wenn die Anwendung offline ist. Um Offline-AppMeasurement zu aktivieren, muss Ihre Report Suite zeitstempelfähig sein. Nach dieser Änderung müssen alle Treffer mit einem Zeitstempel versehen werden oder sie werden entfernt. Wenn Sie momentan AppMeasurement-Daten an eine Report Suite berichten, die auch Daten aus JavaScript erfasst, müssen Sie möglicherweise eine separate Report Suite für Offline-AppMeasurement einrichten, um Datenverlust zu vermeiden.

Sofern Offline-AppMeasurement aktiviert ist, verhält es sich folgendermaßen:
* Die Anwendung sendet einen Server-Aufruf, aber es kommt zu einem Fehler bei der Datenübertragung.
* AppMeasurement generiert einen Zeitstempel für den aktuellen Treffer.
* AppMeasurement puffert die Trefferdaten und sichert die gepufferten Trefferdaten im beständigen Speicher, um Datenverlust zu vermeiden.

Bei jedem folgenden Treffer bzw. nach einem durch offlineThrottleDelay definierten Intervall versucht AppMeasurement, die gepufferten Trefferdaten zu senden, und bewahrt dabei die ursprüngliche Trefferfolge. Wenn die Datenübertragung fehlschlägt, werden die Trefferdaten weiterhin gepuffert (auch dann, wenn das Gerät offline ist).

### Konfigurationsmethoden

**setOfflineTrackingEnabled**: Der Standardwert ist "false". Aktiviert bzw. deaktiviert Offline-Verfolgung für die Measurement Library.

Syntax:

`void setOfflineTrackingEnabled(boolean Enabled);`

Beispiele:
"measure.setOfflineTrackingEnabled(true);

**setOfflineHitLimit**: Der Standardwert ist 1000. Maximale Anzahl der in der Warteschlange gespeicherten Treffer. Wenn die Trefferbeschränkung auf über 5000 festgelegt wird, kann dies Leistungseinbußen zur Folge haben. 

Syntax:

`void setOfflineHitLimit(int offlineHitLimit)`

Beispiele:

`measure.setOfflineHitLimit(2000);`

**getTrackingQueueSize**: Gibt die Anzahl der gespeicherten Verfolgungsaufrufe in der Offline-Warteschlange zurück.

Syntax:

`int getTrackingQueueSize()`

Beispiele:

`int size = measure.getTrackingQueueSize();`

**clearTrackingQueue**: Entfernt alle gespeicherten Verfolgungsaufrufe aus der Offline-Warteschlange.

Syntax:

`void clearTrackingQueue()`

Beispiele:

`measure.clearTrackingQueue();`

**Warnung: Gehen Sie beim manuellen Leeren der Warteschlange vorsichtig vor. Dieser Vorgang kann nicht rückgängig gemacht werden.**


**setOnline und setOffline**: Stellen Sie manuell den Online- oder Offlinestatus des Messungsobjekts ein. Die Bibliothek erkennt automatisch, wann das Gerät offline oder online ist, sodass diese Methoden nur dann benötigt werden, wenn Sie die Offline-Messung erzwingen möchten. SetOnline wird nur verwendet, um zum Onlinezustand zurückzukehren, nachdem der Offlinezustand manuell hergestellt wurde.

Wenn die Messung offline ist:

* Wenn offlineTrackingEnabled true ist: Treffer werden gespeichert, bis die Messung online ist.
* Wenn offlineTrackingEnabled false ist: Treffer werden verworfen.

Syntax:

```
void setOnline()
void setOffline()
```

Beispiele:

```
measure.setOffline();
measure.setOnline();
```

## Offline-Verfolgung

Mit AppMeasurement können Sie die App-Verwendung messen, selbst wenn das Android-Gerät offline ist.

*Hinweis: Um Offline-AppMeasurement zu aktivieren, muss Ihre Report Suite zeitstempelfähig sein.*

Weitere Informationen finden Sie im Abschnitt Offline-Verfolgung.

## Target

Mit Adobe können Sie zielgericheten Inhalt innerhalb von Android-Anwendungen bereitstellen.

Test&amp;Target kann sämtliche textbasierten Inhalte wie HTML, XML oder Nur-Text zurückgeben. Sobald der Inhalt geladen wurde, liegt es am Entwickler der Android-Applikation zu entscheiden, wie er in der Applikation genutzt wird. Der Inhalt kann als HTML angezeigt werden oder genutzt werden, um das Verhalten der Applikation zu verändern. Dieses Handbuch bietet ein einfaches Anwendungsbeispiel für Test&amp;Target-Klassen.

Voraussetzungen

* JDK 5/6/7
* Android SDK for Platform 1.5 oder neuer.

Das in diesem Abschnitt verwendete Beispiel basiert auf Eclipse.

**Bibliothek herunterladen**

Gehen Sie zu Messen und Optimieren von mobilen Anwendungen auf Developer Connection, um die Android-Bibliothek herunterzuladen.

Nach dem Entpacken der heruntergeladenen Datei verfügen Sie über die folgenden Software-Komponenten:

* admsAppLibrary.jar: Bibliothek, die zur Verwendung mit Android-Geräten und Simulatoren entwickelt wurde. Dafür ist Android 2.0 oder höher erforderlich.
* Examples\TrackingHelper.java: Eine optionale Klasse, die dazu bestimmt ist, Rück-Trackingcode und Ihre Anwendungslogik voneinander getrennt zu halten.

**Bibliothek zu Ihrem Projekt hinzufügen**

1. Klicken Sie in der Eclipse IDE mit der rechten Maustaste auf den Projektnamen.
1. Wählen Sie Pfad aufbauen &gt; Externe Archive hinzufügen aus.
1. Wählen Sie admsAppLibrary.jar aus.
1. Klicken Sie auf Öffnen.
1. Klicken Sie erneut mit der rechten Maustaste auf das Projekt, wählen Sie dann Build Path (Pfad aufbauen) &gt; Configure Build Path (Pfadaufbau konfigurieren).
1. Klicken Sie auf die Registerkarte Order and Export (Ordnen und Exportieren).
1. Vergewissern Sie sich, dass admsAppLibrary.jar ausgewählt ist.

Ihre Anwendung kann die Klassen/Schnittstellen aus der admsAppLibrary.jar-Bibliothek mithilfe von `importcom.adobe.ADMS.*;` .*; importieren.

**App-Berechtigungen hinzufügen**

Die AppMeasurement Library erfordert folgende Berechtigungen, um Daten zu senden und Offline-Verfolgungsaufrufe aufzuzeichnen:

* INTERNET
* ACCESS_NETWORK_STATE

Ergänzen Sie Ihre AndroidManifest.xml-Datei (im Projektverzeichnis der Anwendung) um die folgenden Zeilen, um diese Berechtigungen hinzuzufügen:

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Beispiel

Nachdem Sie die Bibliothek zum Projekt hinzugefügt und App-Berechtigungen erteilt haben, können Sie zwei Test&amp;Target-Klassen verwenden: MboxFactory und Mbox.

Das folgende Beispiel veranschaulicht, wie HTML-Inhalte aus Test&amp;Target innerhalb einer einfachen Android-Anwendung in eine WebView geladen werden können. Für das Beispiel wird angenommen, dass die zugehörige Kampagne und HTML-Angebote bereits im Admin-Tool von Test&amp;Target erstellt wurden und dass die Kampagne freigegeben wurde.

1. Führen Sie die Schritte im Abschnitt Implementierung aus und importieren Sie anschließend das testandtarget-Paket oben in der Subklasse Ihrer Anwendung oder Aktivität:

   `com.adobe.adms.testandtarget.*;`

2. Folgen Sie dem untenstehenden nummerierten Code zur Erstellung einer mbox (siehe die Kommentare zur Erläuterung jeder einzelnen Codezeile). Um diesen Schritt abzuschließen, müssen Sie den Code Ihres Klienten und den Namen der für die Einrichtung der Kampagne im Admin-Tool von Test&amp;Target verwendeten mbox kennen.

   ```
   public class AndroidDemoApplication extends Activity {
   private WebView _webView;
   public void onCreate(Bundle savedInstanceState) {
   super.onCreate(savedInstanceState);
   _webView = new WebView(this);
   setContentView(_webView);
   // 1. Create an instance of the MboxFactory class with your client code.
   MboxFactory factory = new MboxFactory("androiddemo16");
   // 2. Use the MboxFactory instance to create an Mbox.
   Mbox mbox = factory.create("DemoApp");
   // 3. Set the default content for the Mbox.
   mbox.setDefaultContent("<h1>DEFAULT CONTENT</h1>");
   /**
   * 4. Create a custom MboxContentConsumer to consume the content returned. The
   * CustomMboxContentConsumer class defined below simply displays the content
   * returned in a BrowserField as HTML.
   */
   CustomConsumer consumer = new CustomConsumer(_webView);
   mbox.addOnLoadConsumer(consumer);
   // 5. Load the Mbox.
   mbox.load();
   ...
   ```

3. Definieren Sie die benutzerspezifische Klasse zur Implementierung der MboxContentConsumer-Schnittstelle. Diese abstrakte Schnittstelle erfordert lediglich, dass Sie eine Methode mit dem Namen „consume“ definieren, in die Inhalte eingespeist werden können. Die unten definierte CustomConsumer-Klasse zeigt lediglich den Inhalt in einer WebView an.

   ```
   class CustomConsumer implements MboxContentConsumer {
   private WebView _view;
   public CustomConsumer(WebView webview) {
   _view = webview;
   }
   public void consume(String content) {
   _view.loadData(content, "text/html", "utf-8");
   }
   }
   ```

4. Klicken Sie mit der rechten Maustaste auf Ihr Projekt und wählen Sie anschließend Run As (Ausführen als) &gt; Android Application (Android-Applikation), um Ihre Applikation zu bauen und zu testen. Wenn Sie Ihre Test&amp;Target-Kampagne ordnungsgemäß eingerichtet und freigegeben haben, sollte Ihr Angebot im Android-Geräteemulator angezeigt werden.

**Lebenszyklusmetriken**

Wenn Lebenszyklusmetriken aktiviert sind, werden diese als Parameter an jede mbox-Last gesendet.

* (Empfohlen) Lebenszyklusereignisse verfolgen
* Lebenszyklusmetriken

## Zielgruppen-Management

Adobe ermöglicht das Senden von Signalen und das Abrufen von Besuchersegmenten über das Zielgruppen-Management.

### Voraussetzungen

* JDK 5/6/7
* Android SDK for Platform 1.5 oder neuer.

Das in diesem Abschnitt verwendete Beispiel basiert auf Eclipse.

### Bibliothek herunterladen

Gehen Sie zu Messen und Optimieren von mobilen Anwendungen auf Developer Connection, um die Android-Bibliothek herunterzuladen.

Nach dem Entpacken der heruntergeladenen Datei verfügen Sie über die folgenden Software-Komponenten:

* admsAppLibrary.jar: Bibliothek, die zur Verwendung mit Android-Geräten und Simulatoren entwickelt wurde. Dafür ist Android 2.0 oder höher erforderlich.
* Examples\TrackingHelper.java: Eine optionale Klasse, die dazu bestimmt ist, Rück-Trackingcode und Ihre Anwendungslogik voneinander getrennt zu halten.

### Bibliothek zu Ihrem Projekt hinzufügen

1. Klicken Sie in der Eclipse IDE mit der rechten Maustaste auf den Projektnamen.
1. Wählen Sie Pfad aufbauen &gt; Externe Archive hinzufügen aus.
1. Wählen Sie admsAppLibrary.jar aus.
1. Klicken Sie auf Öffnen.
1. Klicken Sie erneut mit der rechten Maustaste auf das Projekt, wählen Sie dann Build Path (Pfad aufbauen) &gt; Configure Build Path (Pfadaufbau konfigurieren).
1. Klicken Sie auf die Registerkarte Order and Export (Ordnen und Exportieren).
1. Vergewissern Sie sich, dass admsAppLibrary.jar ausgewählt ist.

Ihre Anwendung kann die Klassen/Schnittstellen aus der admsAppLibrary.jar-Bibliothek mithilfe von `importcom.adobe.ADMS.*;` .*; importieren.

### App-Berechtigungen hinzufügen

Die AppMeasurement-Bibliothek erfordert folgende Berechtigungen, um Daten zu senden und Offline-Verfolgungsaufrufe aufzuzeichnen:
* INTERNET
* ACCESS_NETWORK_STATE

Ergänzen Sie Ihre AndroidManifest.xml-Datei (im Projektverzeichnis der Anwendung) um die folgenden Zeilen, um diese Berechtigungen hinzuzufügen:

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

### Codebeispiel

Nachdem Sie die Bibliothek zum Projekt hinzugefügt haben, können Sie die ADMS_AudienceManager-Klasse verwenden. To import the audience manager package add: `import com.adobe.adms.audiencemanager;`

1. Konfigurieren des Zielgruppen-Managements:

   `ADMS_AudienceManager.ConfigureAudienceManager("mycompany.demdex.net", this);`

   Ersetzen Sie mycompany.demdex.net durch Ihren Endpunkt. Sie können das Zielgruppen-Management an jedem Punkt in der Anwendung konfigurieren.


2. Legen Sie optional dpid und dpuuid fest.

   `ADMS_AudienceManager.SetDpidAndDpuuid("284", "abc123");`

3. Erstellen Sie ein Eigenschaften-Wörterbuch und senden Sie das Wörterbuch in einem Signal ab.

```
HashMap<String, Object> data = new HashMap<String, Object>();
data.put("trait", "b");
ADMS_AudienceManager.SubmitSignal(data, new
ADMS_AudienceManager.AudienceManagerCallback<HashMap>() {
@Override
public void call(HashMap visitorProfile) {
// do things with visitorProfile
}
});
```

Das Besucherprofil-Wörterbuch wird als content-Parameter im Rückruf zurückgegeben.

### Lebenszyklusmetriken

Wenn Lebenszyklusmetriken aktiviert und das Zielgruppen-Management in application:didFinishLaunchingWithOptions: konfiguriert ist, wird nach Abschluss der Konfiguration ein Signal mit Lebenszyklusmetriken gesendet.

* (Empfohlen) Lebenszyklusereignisse verfolgen
* Lebenszyklusmetriken

### ADMS_AudienceManager-Referenz

**Methoden**

**ConfigureAudienceManager**: Legt den Endpunkt für das Zielgruppen-Management fest.

Syntax:

`public static void ConfigureAudienceManager(String server, Context context);`

Beispiel:

`ADMS_AudienceManager.ConfigureAudienceManager("mycompany.demdex.net", this);`

**GetDebugLogging**: Gibt einen booleschen Wert zurück, der angibt, ob Audience Manager-Methoden die Debug-Protokollierung in Ihrer Konsole bereitstellen.

Syntax:

`public static boolean GetDebugLogging();`

**GetDpid**: Gibt die dpid zurück.

Syntax:

`public static String GetDpid();`

**GetDpuuid**: Gibt die dpuuid zurück.

Syntax:

`public static String GetDpuuid();`

**GetVisitorProfile**: Diese Methode kann jederzeit aufgerufen werden, nachdem Sie ein Signal zum Abrufen des neuesten Besucherprofils gesendet haben.

Das Besucherprofil enthält alle Schlüssel/Wert-Paare, die im stuff-Objekt zurückgegeben wurden.

Syntax:

`public static HashMap GetVisitorProfile();`

**SetDebugLogging**: Aktiviert oder deaktiviert die Debug-Protokollierung in Ihrer Konsole.

Syntax:

`public static void SetDebugLogging(boolean logging);`

**SetDpidAndDpuuid**: Wenn newDpid und newDpuuid festgelegt sind, werden sie mit jedem Signal gesendet.

Syntax:

`public static void SetDpidAndDpuuid(String newDpid, String newDpuuid);`

**SubmitSignal**: Sendet ein Wörterbuch mit Eigenschaften und empfängt das aktualisierte Besucherprofil im Rückruf.

Die uuid aus der JSON-Antwort wird intern gespeichert und mit allen nachfolgenden Signalen verwendet. Außerdem wird eine Pixelanforderung an jede URL im dests-Objekt gesendet.

Syntax:

```
public static void SubmitSignal(HashMap<String, Object> data,
AudienceManagerCallback<HashMap> callback);
```

### Schnittstellen

**Methoden**


**AudienceManagerCallback**

Syntax:

```
public interface AudienceManagerCallback<T> {
AudienceManagerCallback
public void call(T item);
}
```

Schnittstelle für Objekt, das im Rückruf des SubmitSignal-Aufrufs verwendet wird.


## PhoneGap-Plug-in

Mit diesem Plug-in können Sie Android-AppMeasurement-Aufrufe von Ihrem PhoneGap-Projekt ausführen.

Eine Anleitung zum Erstellen eines PhoneGap-Projekts finden Sie unter PhoneGap – Einstieg mit Android.

Das Plug-in können Sie über PhoneGap iOS and Android Plug-ins for SiteCatalyst (PhoneGap iOS- und Android-Plug-ins für SiteCatalyst) herunterladen.

### Plug-in einschließen

1. Kopieren Sie ADMS_plugin.java in das Paket im Ordner src.
2. Kopieren Sie ADMS_Helper.js in den Ordner assets/www/js im PhoneGap-Projekt.
3. Öffnen Sie im Ordner res/xml die Datei config.xml und registrieren Sie ein neues Plug-in, indem Sie einen neuen untergeordneten Knoten unter Plug-ins`<plugin name="ADMS_Plugin" value="[YOUR_PACKAGE_NAME].ADMS_plugin" />` erstellen: 

Wenn beispielsweise Ihr Paket die Bezeichnung com.example.phonegaptest trägt, dann würde der Plug-in-Knoten wie folgt lauten: `<plugin name="ADMS_Plugin" value="com.example.phonegaptest.ADMS_plugin" />`

### AppMeasurement Library einschließen

Informationen zum Herunterladen der AppMeasurement Library finden Sie im Abschnitt Bibliothek abrufen.

1. Kopieren Sie admsAppLibrary.jar in den Ordner libs in Ihrem PhoneGap-Projekt.
2. Vergewissern Sie sich, dass sich admsAppLibrary.jar im Build-Pfad befindet, indem Sie mit der rechten Maustaste auf libs &gt; Build-Pfad &gt; Build-Pfad konfigurieren klicken.
3. Klicken Sie auf der Registerkarte "Bibliotheken"auf JAR-Dateien hinzufügen, falls diese noch nicht in Ihrer Liste enthalten sind, und wählen Sie im Ordner "libs"die Option "admsAppLibrary.jar"aus.


### Automatische Verfolgung der Lebenszyklusmetriken

Die Verfolgung der Lebenszyklusmetriken erfordert eine Konfiguration außerhalb von PhoneGap. Führen Sie zur Aktivierung der automatischen Lebenszyklusverfolgung die Implementierungsschritte in der Developer-Kurzanleitung aus.

### Plug-in verwenden

Schließen Sie Folgendes in HTML-Dateien ein, in denen Sie die Verfolgung verwenden möchten:

`<script type="text/javascript" src="js/ADMS_Helper.js"></script>`

Das war alles. Sie können nun Messungsaufrufe ausführen. Weitere Informationen finden Sie im Abschnitt PhoneGap-Plug-in-Methoden.

### Fehlerbehebung

**Meine Syntax stimmt. Warum wird der Code im Plug-in nicht erreicht?**

Überprüfen Sie die Ausgangskonsole auf den folgenden Fehler: `java.lang.ClassNotFoundException: ADMS_plugin`

Tritt dieser Fehler auf, stellen Sie sicher, dass Sie Schritt 3 im Abschnitt Plug-in einschließen ausgeführt haben.

## PhoneGap-Plug-in-Methoden

Schließen Sie Folgendes in HTML-Dateien ein, in denen Sie diese Methoden verwenden möchten:

`<script type="text/javascript" src="js/ADMS_Helper.js"></script>`

**Konfigurationsmethoden**


**configureMeasurementWithReportSuiteIDsTrackingServer**: Diese Methode wird verwendet, um die beiden Parameter zu konfigurieren, die zum Starten der Anwendungsmessung erforderlich sind. Vor dem Senden von Server-Aufrufen müssen Sie die Werte reportSuiteIDs und trackingServer für das Messungsobjekt festlegen, das diese Methode verwendet.

Syntax:

`void configureMeasurementWithReportSuiteIDsTrackingServer(stringreportSuiteIDs, string trackingServer);`

Beispiel:

`ADMS.configureMeasurementWithReportSuiteIDsTrackingServer("testRSID","10.20.40.199:5050");`

**setOnline und setOffline**: Stellen Sie manuell den Online- oder Offlinestatus des Messungsobjekts ein. Die Bibliothek erkennt automatisch, wann das Gerät offline oder online ist, sodass diese Methoden nur dann benötigt werden, wenn Sie die Offline-Messung erzwingen möchten. SetOnline wird nur verwendet, um zum Onlinezustand zurückzukehren, nachdem der Offlinezustand manuell hergestellt wurde.

Wenn die Messung offline ist:

* Wenn offlineTrackingEnabled true ist: Treffer werden gespeichert, bis die Messung online ist.
* Wenn offlineTrackingEnabled false ist: Treffer werden verworfen.

Syntax:

```
void setOnline();
void setOffline();
```

Beispiel:

```
ADMS.setOnline();
ADMS.setOffline();
```

**setDebugLogging**: Aktiviert (true) oder deaktiviert (false) das Anzeigen von Debugging-Informationen. Für die Variable ist standardmäßig „false“ festgelegt.

Diese Variable lässt sich nicht außer Kraft setzen.

Syntax:

`void setDebugLogging(bool debugLogging);`

Beispiel:

`ADMS.setDebugLogging(true);`

### Ereignis- und Zustandsverfolgungsmethoden


**trackAppState**: Dies ist die empfohlene Methode zur Verfolgung von Anwendungszuständen (z. B. Seiten) in Ihrer Anwendung. Der in appState bereitgestellte Wert wird als Seitennamenvariable des Server-Aufrufs angezeigt. Die Zeichenfolge appState muss für jeden Aufruf angegeben werden, da sie nicht in den nächsten Aufruf übernommen wird.

Syntax:

`void trackAppState(string stateName);`

Beispiel:

`ADMS.trackAppState("login page");`

**trackAppStateWithContextData**: Dies ist die empfohlene Methode zur Verfolgung von Anwendungszuständen (z. B. Seiten) in Ihrer Anwendung. Der in appState bereitgestellte Wert wird als Seitennamenvariable des Server-Aufrufs angezeigt. Die Zeichenfolge appState muss für jeden Aufruf angegeben werden, da sie nicht in den nächsten Aufruf übernommen wird.

Kontextdaten, die mit diesem Aufruf gesendet werden, werden an beliebige Werte in persistentContextData angehängt und mit dem Aufruf gesendet. Lediglich die in persistentContextData festgelegten Werte verbleiben für den nächsten Aufruf.

Syntax:

`void trackAppStateWithContextData(string stateName, JSON cData);`

cData: JSON-Objekt mit Schlüsselwertpaaren, die in den Kontextdaten gesendet werden.

Beispiel:

```
trackAppStateWithContextData("login page",
{"user":"john","remember":"true"});
```

**trackEvents**: Dies ist die empfohlene Methode zur Verfolgung von Ereignissen in Ihrer Anwendung. trackEvents ähnelt trackAppState, sendet jedoch Ereignisse anstelle von Seitennamen. Ereignisse werden als durch Kommas getrennte Zeichenfolge mit trackEvents bereitgestellt. Die Zeichenfolge events muss für jeden Aufruf angegeben werden, da sie nicht in den nächsten Aufruf übernommen wird.

Diese Methode führt einen zugrunde liegenden Aufruf an trackLinkURL aus, wobei linkURL auf null, linkType auf "o"festgelegt ist und linkName mit der Anwendungs-ID ausgefüllt wird.

Das bedeutet, dass Ihre linkTrackVars und linkTrackEvents für Aufrufe von `trackEvents` gelten.

Syntax:

`void trackEvents(string eventNames);`

Beispiel:

`ADMS.trackEvents("login,event2");`

**Importhinweis für die Verwendung der trackLink-Methode**

`trackEvents` führt einen zugrundeliegenden Aufruf an trackLinkURL aus, wobei linkURL auf null, linkType auf „o“ festgelegt ist und der linkName mit der Anwendungs-ID ausgefüllt wird. Dadurch soll verhindert werden, dass bei jedem Verfolgen eines Ereignisses die Anzahl der Seitenansichten (Zustandsansicht) erhöht wird.

Wenn Sie trackLinkURL direkt aufrufen und Werte für linkTrackVars und linkTrackEvents einstellen, werden diese Beschränkungen für Variablen und Ereignisse für TrackEvents angewendet. Das bedeutet, dass lediglich die auf diesen Listen festgelegten Variablen und Ereignisse mit TrackEvents gesendet werden. Sie sollten linkTrackVars und linkTrackEvents auf null setzen, wenn Sie nicht wünschen, dass diese Beschränkungen auf trackEvents angewendet werden.

**trackEventsWithContextData**: Dies ist die empfohlene Methode zur Verfolgung von Ereignissen in Ihrer Anwendung. trackEvents ähnelt trackAppState, sendet jedoch Ereignisse anstelle von Seitennamen. Ereignisse werden als kommagetrennte Zeichenfolgen bereitgestellt. Die Zeichenfolge events muss für jeden Aufruf angegeben werden, da sie nicht in den nächsten Aufruf übernommen wird.

Diese Methode führt einen zugrundeliegenden Aufruf an trackLinkURL aus, wobei linkURL auf null und linkType auf „o“ festgelegt ist und linkName mit der Anwendungs-ID ausgefüllt wird.

Das bedeutet, dass Ihre linkTrackVars und linkTrackEvents für Aufrufe von trackEvents gelten.

Kontextdaten, die mit diesem Aufruf gesendet werden, werden an beliebige Werte in persistentContextData angehängt und mit dem Aufruf gesendet. Lediglich die in persistentContextData festgelegten Werte verbleiben für den nächsten Aufruf.

Syntax:

`void trackEventsWithContextData(string eventNames, JSON cData);`

cData: JSON-Objekt mit Schlüsselwertpaaren, die in den Kontextdaten gesendet werden.

Beispiel:

`ADMS.trackEventsWithContextData("login,event2",
{"user":"john","remember":"true"});`

**Importhinweis für die Verwendung der trackLink-Methode**

trackEvents führt einen zugrundeliegenden Aufruf an trackLinkURL aus, wobei linkURL auf null, linkType auf „o“ festgelegt ist und der linkName mit der Anwendungs-ID ausgefüllt wird. Dadurch soll verhindert werden, dass bei jedem Verfolgen eines Ereignisses die Anzahl der Seitenansichten (Zustandsansicht) erhöht wird.

Wenn Sie trackLinkURL direkt aufrufen und Werte für linkTrackVars und linkTrackEvents einstellen, werden diese Beschränkungen für Variablen und Ereignisse für TrackEvents angewendet. Das bedeutet, dass lediglich die auf diesen Listen festgelegten Variablen und Ereignisse mit TrackEvents gesendet werden. Sie sollten linkTrackVars und linkTrackEvents auf null setzen, wenn Sie nicht wünschen, dass diese Beschränkungen auf trackEvents angewendet werden.

**Erweiterte Verfolgungsmethoden (track und trackLink)**

Diese Methoden bieten zusätzliche Optionen für die Verfolgung, mit denen Sie Props, eVars und andere SiteCatalyst-Variablen direkt ausfüllen können. Diese sollten von Kunden mit einer vorhandenen Implementierung verwendet werden oder von Kunden, die mit anderen SiteCatalyst-Implementierungen sehr vertraut sind.

`track` und `trackLink` sind die wichtigsten Messungsmethoden, die in allen Versionen der Adobe Measurement Libraries auf mehreren Plattformen implementiert sind. Bei der Verfolgung von Mobilanwendungen ist es in den meisten Fällen leichter, trackAppState oder trackEvents-Methoden zu verwenden, anstatt „track“ und trackLink direkt aufzurufen.

Seitenabrufverfolgung (track) und Linktracking (trackLink) senden alle beständigen Variablen mit Werten (nicht null, nicht leer, nicht 0). Sie sollten bei Bedarf alle Variablen zurücksetzen oder leeren, bevor Sie track oder trackLink aufrufen.

**Methoden**

**track**: Sendet eine Standardseitenansicht zusammen mit weiteren Variablen, die für das Messungsobjekt festgelegt sind, an den Erfassungsserver.

Syntax:

`void track();`

Beispiel:

`ADMS.track();`

**trackWithContextData**: Sendet eine Standardseitenansicht zusammen mit weiteren Variablen, die für das Messungsobjekt festgelegt sind, an den Erfassungsserver.

Jeder Aufruf von trackWithContextData sendet alle für das Messungsobjekt definierten Daten (diese werden in der Beschreibung für clearVars aufgelistet) sowie weitere contextData, die Sie nur für diesen Aufruf angeben.

Syntax:

`void trackWithContextData(JSON cData);`

cData: JSON-Objekt mit Schlüsselwertpaaren, die in den Kontextdaten gesendet werden.

Beispiel:

`ADMS.trackWithContextData({"key1":"value1","key2":"value2"});`


**trackWith ContextDataAndVariables**: Sendet eine Standardseitenansicht zusammen mit weiteren Variablen, die für das Messungsobjekt festgelegt sind, an den Erfassungsserver.

Jeder Aufruf von trackWithContextDataAndVariables sendet alle für das Messungsobjekt definierten Daten (diese werden in der Beschreibung für clearVars aufgeführt) sowie weitere contextData und Variablen, die Sie nur für diesen Aufruf angeben. Wenn Sie eine definierte Variable senden, werden Werte in der entsprechenden beständigen Variable überschrieben.

Syntax:

`void trackWithContextDataAndVariables(JSON cData, JSON vars);`

cData: JSON-Objekt mit Schlüsselwertpaaren, die in den Kontextdaten gesendet werden.

Beispiel:

```
ADMS.trackWithContextDataAndVariables({"key1":"value1","key2":"value2"},
{"eVar1":"newValue","prop3":"newValue"});
```

**trackLinkURLWithLinkTypeName**: Sendet benutzerspezifische, Download- oder Ausstiegslink-Daten zusammen mit beliebigen track config-Variablen mit Werten an Adobe-Datenerfassungsserver.

Verwenden Sie trackLink, um alle Aktivitäten zu verfolgen, die keinen Seitenabruf erfassen sollen.

Jeder Aufruf von trackLinkURLWithLinkTypeNameContextDataVariables sendet alle für das Messungsobjekt definierten Daten (diese werden in der Beschreibung zu clearVars aufgelistet) sowie weitere contextData, die Sie nur für diesen Aufruf angeben.

Syntax:

```
void trackLinkURLWithLinkTypeNameContextDataVariables(string`
linkUrl, string linkType, string linkName, JSON cData, JSON vars);
```

cData: JSON-Objekt mit Schlüsselwertpaaren, die in den Kontextdaten gesendet werden.

Beispiel:

```
ADMS.trackLinkURLWithLinkTypeNameContextDataVariables("theLink",
"o", "logout", {"key1":"value1"}, {"eVar1":"newValue"});
```

### AppMeasurement-Variablen festlegen und abrufen

**Methoden**

**setEvarToValue**: Legt für die angegebene eVar den bereitgestellten Wert fest. Die eVar wird mit dem nächsten Verfolgungsaufruf gesendet.

Syntax:

`void setEvarToValue(int evar, string value);`

Beispiel:

`ADMS.setEvarToValue(1, "newValue");`

**setPropToValue**: Legt für die angegebene Eigenschaftsvariable den bereitgestellten Wert fest. Die Prop wird mit dem nächsten Verfolgungsaufruf gesendet.

Syntax:

void setPropToValue(int prop, string value);

Beispiel:

`ADMS.setPropToValue(1, "newValue");`

**setHierToValue**: Legt für die angegebene Variable hier den bereitgestellten Wert fest. Die Variable wird mit dem nächsten Verfolgungsaufruf gesendet.

Syntax:

`void setHierToValue(int hier, string value);`

Beispiel:

`ADMS.setHierToValue(1, "newValue");`

**setListVarToValue**: Legt für die angegebene listVar den bereitgestellten Wert fest. Die listVar wird mit dem nächsten Verfolgungsaufruf gesendet.

Syntax:

`void setListVarToValue(int list, string value);`

Beispiel:

`ADMS.setListVarToValue(1, "newValue");`

**getEvar**: Ruft die angegebene Variable ab.

Syntax:

`void getEvar(int evar, function success, function fail);`

Beispiel:

```
ADMS.getEvar(1, function (value) { myTempEvar1 = value; }, function ()
{ myTempEvar1 = null; });
```

**getProp**: Ruft die angegebene Variable ab.

Syntax:

`void getProp(int prop, function success, function fail);`

Beispiel:

```
ADMS.getProp(1, function (value) { myTempProp1 = value; }, function ()
{ myTempProp1 = null; });
```

**getHier**: Ruft die angegebene Variable ab.

Syntax:

`void getHier(int hier, function success, function fail);`

Beispiel:

```
ADMS.getHier(1, function (value) { myTempHier1 = value; }, function ()
{ myTempHier1 = null; });
```

**getListVar**: Ruft die angegebene Variable ab.

Syntax:

`void getListVar(int list, function success, function fail);`

Beispiel:

```
ADMS.getListVar(1, function (value) { myTempListVar1 = value; }, function
() { myTempListVar1 = null; });
```

**clearVars**: Entfernt Werte aus den folgenden Variablen im Objekt:

```
props
eVars
heirs
listVars
events
PersistentContextData
purchaseID
transactionID
appState
channel
appSection
campaign
products
geoZip
geoState
linkTrackVars
linkTrackEvents
```

Syntax:

`void clearVars();`

Beispiel:

`ADMS.clearVars();`

**trackingQueueSize**: Ruft die Anzahl der gespeicherten Verfolgungsaufrufe in der Offline-Warteschlange ab oder legt diese fest.

Syntax:

`void trackingQueueSize(function success, function fail);`

Beispiel:

`ADMS.trackingQueueSize(function (value) { myQueueSize = value; }, function () { myQueueSize = 0; });`

**clearTrackingQueue**: Entfernt alle gespeicherten Verfolgungsaufrufe aus der Offline-Warteschlange. Warnung: Gehen Sie beim manuellen Leeren der Warteschlange vorsichtig vor. Dieser Vorgang kann nicht rückgängig gemacht werden.

Syntax:

`void clearTrackingQueue();`

Beispiel:

`ADMS.clearTrackingQueue();`

### Konfigurationsvariablen festlegen und abrufen

**Methoden**

**getVersion**: Ruft die Bibliotheksversion ab.

Syntax:

`void getVersion(function success, function fail);`

Beispiel:

```
ADMS.getVersion(function (value) { versionNum = value; }, function ()
{ versionNum = 1.0; });
```

**setReportSuiteIDs**: (Erforderlich) Die Report Suite oder Report Suites (Multi-Suite-Tagging), die verfolgt werden sollen. Übergeben Sie eine kommagetrennte Liste mit den Namen der einzelnen Report Suites, um mehrere Report Suites zu verfolgen.

Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:
`void setReportSuiteIDs(string reportSuiteIDs);`

Beispiel:

`ADMS.setReportSuiteIDs("rsid1, rsid2");`

**setTrackingServer**: (Erforderlich) Identifiziert den Erfassungsserver.

Diese Variable muss mit dem für Sie in Code-Manager generierten Wert gefüllt werden.

Derselbe Wert wird bei aktiviertem SSL für die sichere Verfolgung verwendet.

Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:

`void setTrackingServer(string trackingServer);`

Beispiel:

`ADMS.setTrackingServer("10.23.52.191:5923");`

**setDataCenter**:

Syntax:

`void setDataCenter(string dataCenter);`

Beispiel:

`ADMS.setDataCenter("myDataCenter");`

**setVisitorID**: Der Standardwert ist CFUUID.

Eindeutige Kennung eines Besuchers. Wenn Sie keine benutzerspezifische visitorID festlegen, wird (mithilfe der CFUUID von Apple) beim ersten Start eine individuelle visitorID erzeugt, die anschließend im Standardschlüssel eines Benutzers gespeichert wird. Dieser Schlüssel wird ab diesem Zeitpunkt von AppMeasurement und PhoneGap verwendet. Dieser Schlüssel wird auch während des Standardprozesses zur Anwendungssicherung gespeichert und wiederhergestellt.

Syntax:

`void setVisitorID(string visitorId);`

Beispiel:

`ADMS.setVisitorID("myVisitorId");`

**setCharSet**: Der Standardwert ist UTF-8.

Syntax:

`void setCharSet(string charSet);`

Beispiel:

`ADMS.setCharSet("UTF-8");`

**setCurrencyCode**: Der Standardwert ist "none"(für die Report Suite definierter Wert wird verwendet).

Der Währungscode, der für Kauf- oder Währungsereignisse verwendet wird, die in der iOS-Anwendung verfolgt werden.

Syntax:

`void setCurrencyCode(string currencyCode);`

Beispiel:

`ADMS.setCurrencyCode("USD");`


**setSSLEnabled**: Der Standardwert ist "false".

Aktiviert (true) oder deaktiviert (false) das Senden der Messdaten über SSL (HTTPS). Sie können diese Variable nicht für einen einzelnen Aufruf überschreiben. Sie müssen den beständigen Wert ändern.

Syntax:

`void setSSLEnabled(bool sslEnabled);`

Beispiel:

`ADMS.setSSLEnabled(false);`

### Beständige Verfolgungsvariablen festlegen und abrufen

**Methoden**

**setPurchaseID**:

Syntax:

`void setPurchaseID(string purchaseId);`

Beispiel:

`ADMS.setPurchaseID("purchase1");`

**setTransactionID**:

Syntax:

`void setTransactionID(string transactionId);`

Beispiel:

`ADMS.setTransactionID("transaction1");`

**setAppState**:

Syntax:

`void setAppState(string stateName);`

Beispiel:

`ADMS.setAppState("myAppState");`

**setChannel**:

Syntax:

`void setChannel(string channel);`

Beispiel:

`ADMS.setChannel("myChannel");`

**setAppSection**:

Syntax:

`void setAppSection(string appSection);`

Beispiel:

`DMS.setAppSection("myAppSection");`

**setCampaign**:

Syntax:

`void setCampaign(string campaign);`

Beispiel:

`ADMS.setCampaign("myCampaign");`

**setProducts**:

Syntax:

`void setProducts(string products);`

Beispiel:

`ADMS.setProducts("myProduct1,myProduct2");`

**setEvents**:

Syntax:

`void setEvents(string events);`

Beispiel:

`ADMS.setEvents("event1, event2");`

**setGeoState**

Syntax:

`void setGeoState(string state);`

Beispiel:

`ADMS.setGeoState("FL");`

**setGeoZip**:

Syntax:

`void setGeoZip(string zip);`

Beispiel:

`ADMS.setGeoZip("39984");`

**setPersistentContextData**: Kontextdaten sind die empfohlene Methode zur Datenerfassung. Erstellen Sie zum Senden von Kontextdaten ein JSON-Objekt und weisen Sie Schlüsselwertpaare für die Werte zu, die Sie senden möchten.

Syntax:

`void setPersistentContextData(JSON cData);`

Beispiel:

`ADMS.setPersistentContextData({"key1":"value1"});`

**persistentContextData**:

Syntax:

`void persistentContextData(function success, function fail);`

Beispiel:

```
ADMS.persistentContextData(function(value) { alert(value); },
function(error) { alert(error); });
```

**setLinkTrackVars**: Eine kommagetrennte Liste mit Variablennamen, die den aktuellen Variablensatz zur Linktracking eingrenzt.

Wenn linkTrackVars nicht definiert ist, sendet das PhoneGap-Plug-in alle definierten Variablen mit einem trackLink-Aufruf.

Syntax:

`void setLinkTrackVars(string linkTrackVars);`

Beispiel:

`ADMS.setLinkTrackVars("eVar1,eVar2");`


**setLinkTrackEvents**: Eine kommagetrennte Liste von Ereignissen, die den aktuellen Ereignissatz zur Linktracking eingrenzt. Wenn linkTrackEvents nicht definiert ist, sendet das PhoneGap-Plug-in alle Ereignisse mit einem trackLink-Aufruf.

Syntax:

`void setLinkTrackEvents(string linkTrackEvents);`

Beispiel:

`ADMS.setLinkTrackEvents("event1,loginEvent");`


**setLightTrackVars**: Eine kommagetrennte Liste von Variablen, die den aktuellen Variablensatz für leichte Verfolgungsaufrufe eingrenzt. Diese Variablen, die Sie mit einem leichten Server-Aufruf senden, werden durch ClientCare konfiguriert.

Syntax:

`void setLightTrackVars(string lightTrackVars);`

Beispiel:

`ADMS.setLightTrackVars("prop1,hier3");`

### Offline-Verfolgung

**Methoden**

**setOfflineTrackingEnabled**:

Syntax:

`void setOfflineTrackingEnabled(bool offlineTrackingEnabled);`

Beispiel:

`ADMS.setOfflineTrackingEnabled(true);`

**setOfflineHitLimit**:

Syntax:

`void setOfflineHitLimit(int offlineHitLimit);`

Beispiel:

`ADMS.setOfflineHitLimit(3000);`

## Handbuch zur Migration von Android-Version 2.x auf 3.x

* AppMeasurement ist nun ADMS_Measurement. Suchen Sie Positionen, an denen Sie diese Klasse referenzieren, und aktualisieren Sie den Namen auf ADMS_Measurement.
* getInstance ist jetzt sharedInstance. Suchen Sie Positionen, an denen Sie getInstance aufrufen, und ersetzen Sie dieses durch sharedInstance.
* Entfernen Sie alle Aufrufe für massenhafte Messung (getChurnInstance). Diese Aufrufe werden durch die automatische Verfolgung verarbeitet und die Variablen werden jetzt mithilfe von Kontextdaten eingesetzt.
* Timestamp wurde entfernt. Die Bibliothek erfasst Zeitstempel automatisch.

Die Syntax für die folgenden Methoden wurde geändert. Aktualisierte Beispiele für sämtliche Eigenschaften und Methoden stehen zur Verfügung in Konfigurationsvariablen und -methoden.


### Report Suite

**Frühere Version (2.1.x)**

`account`

**Neue Version (3.x)**

`reportSuiteIDs`

### Track

**Frühere Version (2.1.x)**


`String track()`

`String track(Hashtable variableOverrides)`

**Neue Version (3.x)**

Für nicht verwendete Werte wird null übermittelt.

```
void track()
void track(Hashtable<String, Object>
contextData)
void track(Hashtable<String, Object>
contextData, Hashtable<String, Object>
variables)
```

### Link verfolgen

**Frühere Version (2.1.x)**

```
String trackLink(String linkURL, String
linkType, String linkName)
```

```
String trackLink(String linkURL, String
linkType, String linkName,
Hashtable variableOverrides)
```

**Neue Version (3.x)**

Diese beiden Aufrufe wurden durch einen einheitlichen Aufruf ersetzt. Für nicht verwendete Werte wird null übermittelt.

```
void trackLink(String linkURL, String linkType,
String linkName,
Hashtable<String, Object> contextData,
Hashtable<String, Object> variables)
```

### Offline-Verfolgungsmethoden

**Frühere Version (2.1.x)**

`void forceOffline();`


`void forceOnline();`

**Neue Version (3.x)**

`void setOnline();`

`void setOffline();`


### Umbenannte Variablen

In der folgenden Liste sind die Eigenschaften in Version 2.x sowie deren entsprechende Werte in Version 3.x aufgeführt. In Version 3.x wurden einige Eigenschaften entfernt, um die Bibliothek mehr auf mobile Anwendungen auszulegen und um die Implementierung zu vereinfachen.


*Hinweis: Version 3.x verwendet Getter und Setter anstelle von öffentlichen Variablen. Sie müssen die Stellen im Code aktualisieren, in denen die Variablen direkt zur Verwendung der Abruf- und Festlegungsmethoden festgelegt werden.*

```
timestamp; //Removed
trackOffline; //void setOfflineTrackingEnabled(boolean Enabled)
offlineLimit; //void setOfflineHitLimit(int offlineHitLimit)
account; //reportSuiteIDs
linkURL; //Removed (sent with linkTrackURL)
linkName; //Removed (sent with linkTrackURL)
linkType; //Removed (sent with linkTrackURL)
linkTrackVars; //void setLinkTrackVars(String Vars) //comma-delimited list
linkTrackEvents; //void setLinkTrackEvents(String Events) //comma-delimited list
dc; //Removed
trackingServer; //void setTrackingServer(String trackingServer)
trackingServerSecure; //Removed, trackingServer value is used for secure server if ssl=YES
userAgent; //Removed
dynamicVariablePrefix; //Removed
visitorID; //void setVisitorID(String ID)
charSet; //void setCharSet(String charSet)
visitorNamespace; //Removed
pageName; //void setAppState(String State)
pageURL; //Removed
referrer; //Removed
currencyCode; //void setCurrencyCode(String currencyCode)
purchaseID; //void setPurchaseID(String ID)
channel; //void setChannel(String Channel)
server; //void setAppSection(String Section)
pageType; //Removed
transactionID; //void setTransactionID(String ID)
campaign; //void setCampaign(String Campaign)
state; //void setGeoState(String GeoState)
zip; //void setGeoZip(String GeoZip)
events; //void setEvents(String Event) //comma-delimited list
products; //void setProducts(String Products)
list1-list3; //setListVar(int listNum, String listValue);
hier1-heir5; //setHier(int hierNum, String hierValue);
prop1-prop75; //setProp(int propNum, String propValue);
eVar1-eVar75; //setEvar(int evarNum, String evarValue);
ssl; //void setSSL(boolean ssl)
linkLeaveQueryString; //Removed
debugTracking; //debugLogging
usePlugins; //Removed
useBestPractices; //Removed - handled by Lifecycle AutoTracking
contextData; //persistentContextData
```

## Bloodhound für Mobilanwendungstests verwenden

Mit dem Tool Bloodhound können Sie Server-Aufrufe an einen lokalen Computer senden und auf diese Weise Mobilanwendungen testen.

*Wichtig: Am 30. April 2017 wurde die Entwicklung von Adobe Bloodhound eingestellt. Seit dem 1. Mai 2017 wurde keine Verbesserung mehr vorgenommen und es wird kein zusätzlicher Engineering- oder Adobe Expert Care-Support mehr angeboten.*

Bei der Anwendungsentwicklung können Sie in Bloodhound die Server-Aufrufe lokal anzeigen und die Daten optional an Adobe-Erfassungsserver weiterleiten.

Bloodhound ist für Mac und Windows verfügbar.

### Voraussetzungen

* Ein Intel-basierter Mac-Computer, auf dem Snow Leopard (10.6) oder höher ausgeführt wird, oder ein Windows-PC.
* Netzwerkverbindung zu den Mobilgeräten oder Simulatoren.

### Download

Gehen Sie zu Bloodhound – App Measurement QA Tool auf Developer Connection.

### Installation

* Mac: Öffnen Sie die heruntergeladene DMG-Datei und ziehen Sie Bloodhound in den Ordner „Anwendungen“.
* Windows: Führen Sie die heruntergeladene Installationsdatei aus.

### Bloodhound verwenden

Der Server ist nach dem Toolstart deaktiviert, bis Sie auf die Schaltfläche Start klicken. Klicken Sie auf die Schaltfläche Start, wenn Sie für die Erfassung von Server-Aufrufen über Ihre Anwendung bereit sind.

Optional können Sie vor dem Starten des Servers eine benutzerspezifische Portnummer (größer als 1024) angeben. Wenn Sie keine Portnummer eingeben, wählt der Server automatisch einen geöffneten Port aus.

Nach Aktivierung des Servers müssen Sie Ihre Anwendungen oder Geräte zum Senden von Daten an das Tool konfigurieren. Eine Beschreibung hierzu finden Sie im nächsten Abschnitt.

### Geräte für das Senden von Treffern an Bloodhound konfigurieren

Sie können die Proxy-Einstellungen des Geräts so ändern, dass HTTP-Anforderungen an das Tool gesendet werden. An das Tool gesendete Anforderungen können optional an Adobe-Datenerfassungsserver weitergeleitet werden.

Wenn Ihr Gerät Proxys nicht unterstützt, können Sie die Treffer direkt an Bloodhound senden, wo sie geprüft werden.

*Hinweis: Bloodhound unterstützt nicht die SSL-Verfolgung. Sie müssen SSL beim Testen mit Bloodhound in der AppMeasurement Library deaktivieren.*

#### iOS-Geräte

Das iOS-Gerät muss sich in demselben Netzwerk befinden wie der Computer mit Bloodhound.

1. Navigieren Sie zu Einstellungen &gt; Wi-Fi.
1. Klicken Sie auf den blauen Pfeil rechts neben dem aktuellen Wi-Fi-Netzwerk.
1. Gehen Sie mithilfe der Bildlaufleiste zu den HTTP-Proxy-Einstellungen.
1. Wählen Sie Automatisch aus.
1. Geben Sie die Proxy-URL und den Port (der Bloodhound-Oberfläche) im Feld URL ein.

#### Andere Geräte

Wenn das Gerät die automatische Proxy-Konfiguration unterstützt, verwenden Sie einfach die Proxy-URL (aus der Bloodhound-Oberfläche) als Proxy Auto Config (PAC)-URL. Die Proxy-Unterstützung unterscheidet sich je nach Android-Version. Für Android sind zur Vereinfachung des Vorgangs verschiedene Proxykonfigurationstools verfügbar.

### Treffer direkt senden

Für Geräte ohne Proxy-Unterstützung (iOS-Simulator, ältere Android-Versionen usw.) kann Bloodhound als Verfolgungsserver verwendet werden, um die erzeugten Treffer zu erfassen. Legen Sie zu diesem Zweck Folgendes für den Verfolgungsserver fest "<Bloodhound IP>:<BloodhoundPort>".

Beispiel:

```
//iOS
[measure configureMeasurementWithReportSuiteIDs:@"my_rsid" trackingServer:@"10.10.2.2:5000"];
measure.ssl = NO;
```

```
//Android
measure.configureMeasurement("my_rsid", "10.10.2.2:5000");
measure.ssl = false;
```

```
//WinRT for Windows 8, Windows Phone 8
measure.ConfigureMeasurement("my_rsid", "10.10.2.2:5000");
measure.ssl = false;
```

### Fehlerbehebung/Häufige Probleme

* Bloodhound funktioniert nur mit Nicht-SSL-Verfolgung. Über SSL gesendete Verfolgungstreffer werden bei keinem der oben aufgeführten Verfahren erfasst.

## Android-Widgets

Android-Widgets können über dieselben Methoden wie Apps verfolgt werden. Widgets haben denselben Anwendungskontext wie die App. Daher werden die Hit-Reihenfolge und die Besucheridentifizierung beibehalten.

Sie können Android-Widgets anhand der folgenden Richtlinien verfolgen:

* Implementieren Sie keine Lebenszyklusmetriken (startActivity-/stopActivity-Aufrufe) im Widget selbst.
* Fügen Sie einen trackState- oder trackEvent-Aufruf zur onEnabled-Methode eines Widgets hinzu, um aufzuzeichnen, wenn das Widget zum Startbildschirm hinzugefügt wird.
* Um aufzuzeichnen, wenn die App über ein Widget gestartet wird, fügen Sie einen trackState- oder trackEvent-Aufruf hinzu, bevor Sie den Intent für den Start der Anwendung erstellen.
* Wenn Sie den Kontext einer Aktion verfolgen möchten, können Sie eine ContextData-Variable definieren, mit der es möglich ist, jede Aktion separat zu segmentieren (z. B. AppExperienceType="widget" oder "app").
