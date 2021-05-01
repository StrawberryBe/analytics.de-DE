---
description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.
title: Activity Map – Häufig gestellte Fragen
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
feature: Activity Map
role: Business Practitioner, Administrator
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
translation-type: tm+mt
source-git-commit: a283ba5d5678498cde9d0065a4f9f6b8a98558dd
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 29%

---

# Activity Map – Häufig gestellte Fragen

Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.

## Haben alle Analytics-Kunden Zugriff auf die Seite &quot;Activity Map-Aktivierung&quot;der Admin Tools?

Organisationen mit Adobe Analytics Standard, Premium und Ultimate haben Zugang zu Activity Map.

## Wie unterstützt Activity Map Einzelseitenanwendungen (SPA)?

Alle paar Sekunden scannt Activity Map die Webseite und sucht nach Änderungen an der Seite. ActivityMap findet neue Inhalte auf der Seite, ohne dass eine neue Seite geladen werden muss, aber dieser neue Inhalt wird immer dem ersten pageName zugeordnet, der beim Laden der Seite gefunden wurde.

* Activity Map überprüft, ob sich die Sichtbarkeit der Links, von denen es Kenntnis hat, geändert hat. Wenn eine Änderung der Sichtbarkeit gefunden wird, wird die Spalte &quot;Präsenz&quot;der Tabelle &quot;Links auf Seite&quot;für diesen Link mit [!UICONTROL Angezeigt] oder [!UICONTROL Ausgeblendet] aktualisiert.

* Wenn durch Benutzerinteraktion neue Inhalte erstellt werden, werden alle neuen Elemente, die von AppMeasurement als Link erkannt werden, der Tabelle [!UICONTROL Links auf Seite] hinzugefügt. Activity Map sendet eine neue Datenanforderung, die diese neuen Links enthält. Die neuen Links sollten in der Tabelle [!UICONTROL Links auf Seite] angezeigt werden, wenn die Datenanforderung von der Benutzeroberfläche verarbeitet wird.


## Stellt Activity Map Daten zu &quot;Ansichten&quot;bereit?

Nein, Adobe verfolgt keine Links, die angezeigt wurden.

## Welche Browser und Versionen werden von Activity Map unterstützt?

Activity Map unterstützt die neueste Version der meisten modernen Browser.

## Steigern Activity Map Serveraufrufe?

Activity Map sendet keine Server-Aufrufe allein. Stattdessen werden die Kontextdatenvariablen der Activity Map in die Seitenaufrufe der Analytics-Ansicht auf der nachfolgenden Seite einbezogen.

## Warum fehlen Überlagerungen für Elemente in der Rangansicht?**

Einige Links mit Rangansicht, wie z. B. Links in Untermenüs, werden von der Seite ausgeblendet. Daher werden die entsprechenden Linküberlagerungen nicht angezeigt. Rang wird für alle Links auf der Seite berechnet, einschließlich ausgeblendeter Links.

## Wie wird die Rangfolge von Links im Bericht &quot;Alle Links&quot;bestimmt?**

* **Im Verlauf und Blasenmodus**: Rang wird durch die Metrikspalte bestimmt. Für Links mit dem gleichen Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* **Im Modus** Gewinner und Verlierer: Rang wird hauptsächlich durch die Spalte &quot;% Gewinn&quot;bestimmt. Bei Links mit demselben Gewinn basiert der Rang weiter auf der alphabetischen Reihenfolge der Link-IDs.

## Wie funktioniert Activity Map mit Seiten, die mehrere Report Suites verwenden?

Standardmäßig verwendet Activity Map die Report Suite, die mit dem ersten Tag verbunden ist, das von der Seite gesendet wird. Sie können eine andere getaggte Report Suite auf der Registerkarte unter **[!UICONTROL Einstellungen für Activity Map]** > **[!UICONTROL Andere]** auswählen.

## Wie lange sucht Activity Map nach Adobe Analytics auf der Seite?

Aktivität Map überprüft bis zu 20 Sekunden nach dem Ereignis &quot;Seitenbeendigung&quot;auf das Vorhandensein von Adobe Analytics.

## Wie behandelt Activity Map dynamische Inhalte?

Activity Map sucht alle zwei Sekunden nach Statusänderungen der Webseite wie:

* HTML-Inhalt wurde angezeigt
* HTML-Inhalt wurde verborgen
* Neuer HTML-Inhalt wurde eingefügt

Wird Inhalt verborgen oder angezeigt, so ändert die Anwendung automatisch den Status der betroffenen Links (und somit der Überlagerungen) von „verborgen“ in „angezeigt“ oder umgekehrt. Wenn neue Inhalte eingefügt werden, ruft die Anwendung die zugehörigen Links ab, ruft Analysedaten für sie ab und fügt Überlagerungen für diese Links hinzu.

## Auf welcher Metrik basiert der Seitenflussbericht?

Alle angezeigten Daten basieren auf Seitenansichten.

## Kann ich Kontextdatenvariablen aus Activity Map über Data Feeds exportieren?

Kontextdatenvariablen für die Aktivität sind in Datenfeeds nicht verfügbar.

## Funktionieren Segmente im Livemodus?

Nein, Segmente funktionieren nicht im Livemodus. Die Funktionalität entspricht der des Echtzeit-Berichte in Reports &amp; Analysen, die keine Segmentierung unterstützen.

## Ist Activity Map mit Virtual Report Suites kompatibel?

Ja. Aufgrund der Einschränkungen der Virtual Report Suites ist jedoch der Livemodus von Activity Map nicht mit Virtual Report Suites kompatibel.
