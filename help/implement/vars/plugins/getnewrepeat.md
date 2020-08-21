---
title: getNewRepeat
description: Verfolgen Sie die Aktivitäten neuer oder wiederkehrender Besucher.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '819'
ht-degree: 100%

---


# Adobe-Plug-in: getNewRepeat

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `getNewRepeat`-Plug-in können Sie innerhalb einer gewünschten Anzahl von Tagen feststellen, ob es sich bei einem Besucher um einen neuen Besucher oder einen wiederkehrenden Besucher handelt. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie Besucher anhand einer benutzerdefinierten Anzahl von Tagen als „neu“ identifizieren möchten. Dieses Plug-in ist nicht erforderlich, wenn die Besucherdimensionen „Neu“/„Wiederkehrend“ in Analysis Workspace den Anforderungen Ihres Unternehmens entsprechen.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: getNewRepeat initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: getNewRepeat v2.1 */
s.getNewRepeat=function(d){d=d?d:30;var s=this,p="s_nr"+d,b=new Date,e=s.c_r(p),f=e.split("-"),c=b.getTime();b.setTime(c+864E5*d); if(""===e||18E4>c-f[0]&&"New"===f[1])return s.c_w(p,c+"-New",b),"New";s.c_w(p,c+"-Repeat",b);return"Repeat"};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `getNewRepeat`-Methode verwendet die folgenden Argumente:

* **`d`** (Ganzzahl, optional): Die erforderliche Mindestanzahl von Tagen zwischen Besuchen, die Besucher auf `"New"` zurücksetzt. Wenn dieses Argument nicht festgelegt ist, wird der Standardwert 30 Tage verwendet.

Diese Methode gibt den Wert von `"New"` zurück, wenn das vom Plug-in eingestellte Cookie nicht vorhanden oder abgelaufen ist. Gibt den Wert von `"Repeat"` zurück, wenn das vom Plug-in eingestellte Cookie vorhanden ist und die Zeit seit dem aktuellen Treffer und die im Cookie festgelegte Zeit länger als 30 Minuten sind. Diese Methode gibt denselben Wert für den gesamten Besuch zurück.

Dieses Plug-in verwendet ein Cookie mit dem Namen `"s_nr[LENGTH]"`, bei dem `[LENGTH]` mit dem `d`-Argument übereinstimmt. Das Cookie enthält einen Unix-Zeitstempel, der die aktuelle Zeit und den aktuellen Status des Besuchers (`"New"` oder `"Repeat"`) darstellt.

## Beispielaufrufe

### Beispiel 1

Der folgende Code setzt s.eVar1 für neue Besucher auf den Wert „Neu“ und setzt s.eVar1 während des restlichen Besuchs des Besuchers auf der Website weiterhin auf den Wert „Neu“ (bei jedem neuen Aufruf).

```js
s.eVar1=s.getNewRepeat();
```

### Beispiel 2

Wenn der Besucher zu irgendeinem Zeitpunkt zwischen 31 Minuten und 30 Tagen seit dem letzten Aufruf von s.getNewRepeat() auf die Website zurückkommt, setzt der folgende Code s.eVar1 auf den Wert „Wiederkehrend“ und setzt s.eVar1 während des restlichen Besuchs des Besuchers auf der Website weiterhin auf den Wert „Wiederkehrend“ (bei jedem neuen Aufruf).

```js
s.eVar1=s.getNewRepeat();
```

### Beispiel 3

Wenn der Besucher seit dem letzten Aufruf von s.getNewRepeat () mindestens 30 Tage nicht auf der Website war, setzt der folgende Code s.eVar1 auf den Wert „Neu“ und setzt s.eVar1 während des restlichen Besuchs des Besuchers auf der Website weiterhin auf den Wert „Neu“ (bei jedem neuen Aufruf).

```js
s.eVar1=s.getNewRepeat();
```

### Beispiel 4

Wenn der Besucher zu irgendeinem Zeitpunkt zwischen 31 Minuten und 365 Tagen (d. h. 1 Jahr) seit dem letzten Aufruf von s.getNewRepeat() auf die Website zurückkommt, setzt der folgende Code s.eVar1 auf den Wert von „Wiederkehrend“ und setzt s.eVar1 während des restlichen Besuchs des Besuchers auf der Website weiterhin auf den Wert „Wiederkehrend“ (bei jedem neuen Aufruf).

```js
s.eVar1=s.getNewRepeat(365);
```

### Beispiel 5

Wenn der Besucher seit mindestens 365 Tagen (d. h. 1 Jahr) seit dem letzten Aufruf von s.getNewRepeat() nicht auf der Website war, setzt der folgende Code s.eVar1 auf den Wert „Neu“ und setzt s.eVar1 während des restlichen Besuchs des Besuchers auf der Website weiterhin auf den Wert „Neu“ (bei jedem neuen Aufruf).

```js
s.eVar1=s.getNewRepeat(365);
```

## Versionsverlauf

### 2.1 (30. September 2019)

* Neuanordnung der JavaScript-Logik zur Reduzierung der Plug-in-Größe

### 2.0 (16. April 2018)

* Neu kompiliert mit kleinerer Code-Größe
* Die Möglichkeit, das Cookie zum Speichern der Besuchsinformationen zu benennen, wurde entfernt. Das Plug-in benennt das Cookie nun dynamisch basierend auf dem Wert, der an das `d`-Argument übergeben wird.
