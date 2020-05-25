---
description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.
title: Activity Map – Häufig gestellte Fragen
topic: Activity map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
translation-type: ht
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Activity Map – Häufig gestellte Fragen

Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map.

## Implementierung und AppMeasurement

**F: Welche Implementierungsschritte sind zur Aktivierung der neuen Activity Map erforderlich?**

A: Lesen Sie [Activity Map aktivieren](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**F: Haben alle Analytics-Kunden Zugriff auf die Seite „Activity Map – Aktivierung“ in den Admin Tools?**

A: Adobe SiteCatalyst-Kunden haben keinen Zugriff auf die Seite „Activity Map – Aktivierung“ in der Admin Console. Nur Unternehmen mit Adobe Analytics Standard- und Adobe Analytics Premium-Verträgen haben Zugriff auf diese Konfigurationsseite.

**F: Kann der neue AppMeasurement-Code über Dynamic Tag Management (DTM) konfiguriert werden?**

A: Ja, Sie können den neuen AppMeasurement-Code [manuell implementieren](https://docs.adobe.com/content/help/de-DE/dtm/using/tools/analytics-dtm.translate.html).

**F: Welche großen Änderungen wurden an der AppMeasurement v1.6-Bibliothek vorgenommen?**

A: Die einzige Änderung in AppMeasurement v1.6 ist die Linktracking-Methode in Activity Map, für die Seitenname, Link-ID und Regions-ID erfasst werden müssen.

**F: Wird das Rollout von AppMeasurement auf Domänenebene oder nur auf bestimmten Seiten ausgeführt?**

A: Das Rollout von AppMeasurement wird auf Report Suite-Ebene ausgeführt. Die Report Suite-Ebene ist typischerweise mit einer Domänenebene verbunden. Dies ist jedoch bei jeder Implementierung anders.

**F: DTM lädt automatisch eine ältere Version (1.3.4) der Besucher-API als die von Activity Map verlangte Version (1.5.1). Ist das ein Problem?**

A.: Nein. Die Activity Map-Funktion hängt nicht von der Besucher-API ab.

## Activity Map-Anwendung

<!--**Q: How does Activity Map support Single-Page Applications (SPA)?**

A: 

* Every few seconds, Activity Map scans the web page, looking for changes to the page. ActivityMap finds new content on the page without needing a new page load, but this new content is always attributed to the first pageName found when the page loaded.

* Activity Map checks to see if the visibility of links that it knows about has changed. If a change in visibility is found, then the [Links On Page](/help/analyze/activity-map/activitymap-links-report.md) table's Present column for that link updates with **[!UICONTROL Displayed]** or **[!UICONTROL Hidden]**.

* When user interaction creates new content, any new elements that are found by AppMeasurement to be a link will be added to the **[!UICONTROL Links On Page]** table. Activity Map sends a new data request that includes these new links. The new links should appear in the **[!UICONTROL Links On Page]** table when the data request is handled by the UI.-->

**F: Bietet Activity Map Daten zu „Ansichten“?**

A: Nein, Adobe verfolgt keine Links, die angezeigt wurden.

**F: Kann ich Activity Map verwenden, wenn ich zuvor Besucher-ClickMap auf meiner Website nicht verwendet habe?**

A: Die Installation der älteren Version (wird jetzt auch einfach als ClickMap bezeichnet) ist keine Voraussetzung für die Implementierung der neuen Version. Für einen beschränkten Zeitraum wird die ältere Version weiterhin von Adobe unterstützt.

**F: Welche Browser und Versionen werden von Activity Map unterstützt?**

A: Es wird die jeweils neueste Version der vier gängigsten Browser (Chrome, Firefox, Safari und IE) unterstützt.

**F: Was sind die Standardeinstellungen für Überlagerungen?**

A: Standardmäßig zeigt Activity Map Überlagerungen für ALLE Links mit erfassten Daten an.

Wenn Popupfenster über den Webseiten von Kunden angezeigt werden, können Überlagerungen für Links unter dem Popupfenster auch über dem Popupfenster angezeigt werden.

**F: Warum fehlen für einige Elemente, denen ein Rang zugewiesen wurde, die Überlagerungen?**

A: Einige Links mit einem Rang können auf der Seite verborgen sein (beispielsweise Links in Untermenüs). Daher werden die entsprechenden Linküberlagerungen nicht angezeigt. Sie können also damit rechnen, dass in einigen Überlagerungen bestimmte Rangwerte fehlen, da der Rang anhand aller Links auf der Seite (vorhandene und verborgene) berechnet wird.

**F: Wie wird die Rangzuweisung für Links im Bericht „Alle Links“ bestimmt?**

* In den Modi **Verlauf** und **Blase**: Die Rangzuweisung wird anhand der Metrikspalte bestimmt. Für Links mit dem gleichen Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* Im Modus **Gewinner und Verlierer** wird der Rang hauptsächlich anhand der Spalte „% Gewinn“ bestimmt. Für Links mit dem gleichen Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

**F: Warum werden keine Link-Klickdaten erfasst, wenn Activity Map ausgeführt wird?**

A: Während Activity Map in Verwendung ist, werden keine Link-Klickdaten vom Analytics-Tag erfasst. Dieses Verhalten folgt dem Verhalten des ClickMap-Plug-ins.

**F: Wo liegt der Unterschied zwischen dem Activity Map-Bericht „Alle Links“ und der Activity Map-Berichterstellung in „Reports &amp; Analytics“?**

A: Um den Bericht „Alle Links“ in Activity Map abzurufen, erstellen wir wie folgt eine Aufschlüsselungsanforderung: Activity Map-Seite = &quot;visitedpage&quot;, aufgeschlüsselt nach Activity Map-Link und -Region in `<list of link&regions present in the page at rendering time>`.

Um einen entsprechenden Bericht in „Reports &amp; Analytics“ zu erhalten, müssen Sie zunächst zum Activity Map-Seitenbericht navigieren. Dort filtern Sie nach dem Namen der besuchten Seite in Activity Map. Der Name der besuchten Seite wird in der linken Spalte der Activity Map-Seitendetails im unteren Bereich angezeigt. Sobald die Seite gefunden wurde, können Sie die Aufschlüsselung vornehmen und Activity Map-Links und -Regionen als sekundäre Dimension auswählen.

Beachten Sie jedoch, dass der in „Reports &amp; Analysen“ generierte Bericht alle Links und Regionen enthält, die für diese Seite erfasst wurden. Activity Map erstellt jedoch nur Berichte für Links und Regionen, die aktuell auf der Webseite vorhanden sind. Auf einer Nachrichtensite werden daher nur die Daten für den aktuell vorhandenen Artikel angezeigt, nicht für Artikel, die zu einem früheren Zeitpunkt am selben Tag zu sehen waren.

**F: Wie funktioniert Activity Map bei Seiten, die mehrere Tags für verschiedene Report Suites aufweisen?**

A: Standardmäßig verwendet Activity Map die Report Suite, die mit dem ersten Tag verbunden ist, das von der Seite gesendet wird. Sie können eine andere getaggte Report Suite auf der Registerkarte unter Einstellungen für Activity Map > Andere auswählen.

**F: Wie lange sucht Activity Map das Analytics-Tag?**

A: Das Analytics-Tag wird bis zu 20 Sekunden nach einem Page Complete-Ereignis gesucht.

**F: Wie behandelt Activity Map dynamischen Inhalt?**

A: Activity Map sucht alle zwei Sekunden nach Statusänderungen der Webseite wie:

* HTML-Inhalt wurde angezeigt
* HTML-Inhalt wurde verborgen
* Neuer HTML-Inhalt wurde eingefügt

Wird Inhalt verborgen oder angezeigt, so ändert die Anwendung automatisch den Status der betroffenen Links (und somit der Überlagerungen) von „verborgen“ in „angezeigt“ oder umgekehrt.

Wird neuer Inhalt eingefügt, ruft die Anwendung die zugehörigen Links ab, generiert Analysedaten für sie und fügt Überlagerungen für diese Links hinzu.

**F: Auf welcher Metrik basiert der Seitenflussbericht?**

A: Alle angezeigten Daten basieren auf Seitenansichten.

**F: Können Sie das Activity Map-Verhalten für verschiedene Seitentypen erklären?**

*Webseite ohne Analytics-Tag*

Unter der Symbolleiste wird eine Warnmeldung angezeigt, die angibt, dass kein Tag vorhanden ist.

*Webseite mit inkompatiblem Analytics-Tag (AppMeasurement v1.5 oder früher)*

Eine Warnmeldung weist Sie darauf hin, dass Sie ein Upgrade des Seiten-Codes auf v1.6 oder höher durchführen müssen.

*Webseite mit kompatiblem Analytics-Tag (AppMeasurement v1.6 oder höher), für die jedoch die Activity Map-Berichterstattung in den Admin Tools nicht aktiviert wurde*

Eine Warnmeldung weist Sie darauf hin, dass Sie Ihren Administrator bitten müssen, den \[Activity Map-Bericht zu aktivieren\](/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md&quot;).

**F: Kann ich Activity Map-Daten (contextData) über [Analytics Data Feed](https://docs.adobe.com/content/help/de-DE/analytics/export/analytics-data-feed/data-feed-overview.translate.html) exportieren?**

A: Nein.

## Segmentierung in Activity Map

**F: Sind Segmente auf bestimmte Benutzersegmente beschränkt? Gibt es freigegebene Segmente in Activity Map?**

A: Activity Map übernimmt Ihre Berichterstellungssegmente aus Analytics.

**F: Funktionieren Segmente im Livemodus?**

A: Nein, Segmente funktionieren nicht im Livemodus. Die Funktionalität entspricht der Echtzeit-Berichterstellung in „Reports &amp; Analytics“.

## Virtual Report Suites

**F: Ist Activity Map mit Virtual Report Suites kompatibel?**

A: Ja. Aufgrund der Einschränkungen der Virtual Report Suites ist jedoch der Livemodus von Activity Map nicht mit Virtual Report Suites kompatibel.
