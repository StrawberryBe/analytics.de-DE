---
description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.
title: Activity Map – Häufig gestellte Fragen
topic: Activity map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
translation-type: tm+mt
source-git-commit: 0e125be6e1710c65effa0adc8097e8916c8a3290

---


# Activity Map – Häufig gestellte Fragen

Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.

## Implementierung und AppMeasurement

**F: Welche Implementierungsschritte sind zur Aktivierung der neuen Activity Map erforderlich?**

A: Lesen Sie [Activity Map aktivieren](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**F: Haben alle Analytics-Kunden Zugriff auf die Seite „Activity Map – Aktivierung“ in den Admin Tools?**

A: Adobe SiteCatalyst-Kunden haben keinen Zugriff auf die Seite „Activity Map – Aktivierung“ in der Admin Console. Auf diese Konfigurationsseite haben nur Firmen mit Adobe Analytics Standard- und Adobe Analytics Premium-Verträgen Zugriff.

**Q: Kann der neue AppMeasurement-Code über das dynamische Tag-Management (DTM) konfiguriert werden?**

A: Ja, Sie können den neuen AppMeasurement-Code [manuell implementieren](https://marketing.adobe.com/resources/help/en_US/dtm/analytics_dtm.html) .

**Q: Was sind die großen Änderungen in der AppMeasurement v1.6-Bibliothek?**

A: Die einzige Änderung in AppMeasurement v1.6 betrifft die Linktracking-Methode für Aktivitäten-Map, die die Erfassung von Seitennamen, Link-ID und Regions-ID erfordert.

**Q: Wird das Rollout von AppMeasurement eher auf Domänenebene als auf bestimmten Seiten erfolgen?**

A: Das Rollout von AppMeasurement wird auf Report Suite-Ebene ausgeführt. Die Report Suite-Ebene ist in der Regel mit einer Domänenebene verknüpft, dies unterscheidet sich jedoch je nach Implementierung.

**Q: DTM lädt automatisch eine ältere Version (1.3.4) der Besucher-API, als die Aktivität Map es wünscht (1.5.1). Ist das ein Problem?**

A.: Nein. Die Funktion für die Zuordnung von Aktivitäten ist nicht von der VisitorAPI abhängig.

## Activity Map-Anwendung

<!--**Q: How does Activity Map support Single-Page Applications (SPA)?**

A: 

* Every few seconds, Activity Map scans the web page, looking for changes to the page. ActivityMap finds new content on the page without needing a new page load, but this new content is always attributed to the first pageName found when the page loaded.

* Activity Map checks to see if the visibility of links that it knows about has changed. If a change in visibility is found, then the [Links On Page](/help/analyze/activity-map/activitymap-links-report.md) table's Present column for that link updates with **[!UICONTROL Displayed]** or **[!UICONTROL Hidden]**.

* When user interaction creates new content, any new elements that are found by AppMeasurement to be a link will be added to the **[!UICONTROL Links On Page]** table. Activity Map sends a new data request that includes these new links. The new links should appear in the **[!UICONTROL Links On Page]** table when the data request is handled by the UI.-->

**Q: Bietet Aktivität Map Daten zu &quot;Ansichten&quot;?**

A: Nein, Adobe verfolgt keine Links, die angezeigt wurden.

**Q: Kann ich die Aktivität Map verwenden, wenn ich Besucher ClickMap auf meiner Website noch nicht verwendet habe?**

A: Die Installation der älteren Version - jetzt einfach als ClickMap bezeichnet - ist keine Voraussetzung für die Implementierung der neuen Version. Adobe wird die ältere Version für einen begrenzten Zeitraum weiterhin unterstützen.

**Q: Welche Browser und Versionen werden von Aktivität Map unterstützt?**

A: Wir unterstützen die neueste Version der vier wichtigsten Browser (Chrome, Firefox, Safari und IE).

**Q: Was sind die Standardeinstellungen für Überlagerungen?**

A: Standardmäßig zeigt Aktivität Map ALLE Links an, die Daten erfasst haben.

Wenn Popup-Bedienfelder über den Webseiten von Kunden angezeigt werden, können Überlagerungen, die zu Links gehören, die sich unterhalb des Popup-Bedienfelds befinden, über dem Popup-Bedienfeld angezeigt werden.

**Q: Warum fehlen Überlagerungen für Elemente mit Rangansicht?**

A: Einige Links mit Rangansicht können auf der Seite ausgeblendet werden (z. B. Links im Untermenü). Daher werden die entsprechenden Linküberlagerungen nicht angezeigt. Sie können also erwarten, dass Überlagerungsrankings angezeigt werden, bei denen bestimmte Rangwerte fehlen, da der Rang für alle Links auf der Seite berechnet wird (der aktuelle und der verborgene).

**Q: Wie wird die Rangfolge von Links im Bericht &quot;Alle Links&quot;bestimmt?**

* Im **Verlauf** - und **Blasenmodus** : Die Rangfolge wird durch die Metrikspalte bestimmt. Bei Links mit demselben Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* Im **Modus Gewinner und Verlierer** wird der Rang primär durch die Spalte &quot;% Gewinn&quot;bestimmt. Bei Links mit demselben Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

**Q: Warum werden keine Link-Klickdaten erfasst, wenn Aktivität Map ausgeführt wird?**

A: Während die Aktivität Map verwendet wird, werden die Link-Klickdaten nicht vom Analytics-Tag erfasst. Dieses Verhalten entspricht dem Verhalten des ClickMap-Plugins.

**Q: Wie sieht der Bericht &quot;Aktivität alle Links&quot;im Vergleich zum Berichte &quot;Aktivität für Reports &amp; Analysen&quot;aus?**

A: Um den Bericht „Alle Links“ in Activity Map abzurufen, erstellen wir wie folgt eine Aufschlüsselungsanforderung: Activity Map-Seite = &quot;visitedpage&quot;, aufgeschlüsselt nach Activity Map-Link und -Region in `<list of link&regions present in the page at rendering time>`.

Um einen entsprechenden Bericht in „Reports &amp; Analytics“ zu erhalten, müssen Sie zunächst zum Activity Map-Seitenbericht navigieren. Dort filtern Sie nach dem Namen der besuchten Seite in der Aktivität Map. Der besuchte Seitenname wird in der linken Spalte im unteren Bedienfeld &quot;Seitendetails der Aktivität zuordnen&quot;angezeigt. Sobald die Aktivität gefunden wurde, können Sie von dieser Seite nach unten unterteilen und die Seitenzuordnungslinks und -bereiche als sekundäre Dimension auswählen.

Es ist jedoch wichtig zu beachten, dass der in der FuA abgerufene Bericht alle Links und Regionen, die für diese Seite erfasst wurden, Liste. Aktivität Map erstellt jedoch nur Berichte zu Links und Regionen, die aktuell auf der Webseite vorhanden sind. Wenn Sie also eine News-Site haben, werden nur Daten zu der aktuellen Meldung angezeigt, nicht zu den Nachrichten, die zu einem früheren Zeitpunkt am Tag zu sehen waren.

**Q: Wie funktioniert Aktivität Map mit Seiten, die mehrere Tags enthalten, die mehrere Report Suites auflisten?**

A: Standardmäßig verwendet Aktivität Map die Report Suite, die mit dem ersten Tag verknüpft ist, das von der Seite gesendet wird. Sie können eine andere getaggte Report Suite auf der Registerkarte unter Einstellungen für Activity Map > Andere auswählen.

**Q: Wie lange sucht Aktivität Map nach dem Analytics-Tag?**

A: Wir suchen nach dem Analytics-Tag bis zu 20 Sekunden nach einem Ereignis zum Abschluss der Seite.

**Q: Wie behandelt Aktivität Map dynamischen Inhalt?**

A: Aktivität Map überprüft alle 2 Sekunden, ob sich der Status der Webseite verändert hat, z. B.:

* HTML-Inhalt, der sichtbar geworden ist
* HTML-Inhalt, der ausgeblendet wird
* Neuer HTML-Inhalt, der eingefügt wurde

Wenn Inhalte ausgeblendet oder angezeigt werden, ändert die Anwendung automatisch den Status der betroffenen Links (und damit der Überlagerungen) von ausgeblendet zu eingeblendet oder eingeblendet zu.

Wenn neue Inhalte eingefügt werden, ruft die Anwendung die zugehörigen Links ab, ruft Analysedaten für sie ab und fügt Überlagerungen für diese Links hinzu.

**Q: Auf welcher Metrik basiert der Seitenflussbericht?**

A: Alle angezeigten Daten basieren auf den Ansichten der Seite.

**Q: Können Sie das Seitenbildverhalten mit verschiedenen Seitentypen erklären?**

*Webseite ohne Analytics-Tag*

Unter der Symbolleiste wird eine Warnmeldung angezeigt, die darauf hinweist, dass kein Tag vorhanden ist.

*Webseite mit inkompatiblem Analytics-Tag (AppMeasurement v1.5 oder früher)*

Es wird eine Warnmeldung angezeigt, die darauf hinweist, dass Sie den Seiten-Code auf Version 1.6 oder höher aktualisieren müssen.

*Webseite mit kompatiblem Analytics-Tag (AppMeasurement v1.6 oder höher), für die jedoch die Activity Map-Berichterstattung in den Admin Tools nicht aktiviert wurde*

Eine Warnmeldung weist Sie darauf hin, dass Sie Ihren Administrator bitten müssen, den \[Activity Map-Bericht zu aktivieren\](/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md&quot;).

**F: Kann ich Activity Map-Daten (contextData) über [Analytics Data Feed](https://docs.adobe.com/content/help/en/analytics/export/analytics-data-feed/data-feed-overview.html) exportieren?**

A: Nein.

## Segmentierung in Activity Map

**Q: Sind Segmente an die einzelnen Benutzersegmente gebunden? Sind freigegebene Segmente in der Aktivität verfügbar?**

A: Aktivität Map übernimmt Ihre Berichte-Segmente aus Analytics.

**Q: Funktionieren Segmente im Livemodus?**

A: Nein, Segmente funktionieren nicht im Livemodus. Die Funktionalität entspricht der des Echtzeit-Berichte in Reports &amp; Analysen.

## Virtual Report Suites

**Q: Ist Aktivität Map mit Virtual Report Suites kompatibel?**

A: Ja. Aufgrund der Einschränkungen der Virtual Report Suite ist der Livemodus von Aktivität Map jedoch nicht mit Virtual Report Suites kompatibel.
