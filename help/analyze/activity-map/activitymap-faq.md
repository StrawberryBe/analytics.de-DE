---
description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Einsatz von Funktionen in [!DNL Activity Map].
seo-description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Einsatz von Funktionen in [!DNL Activity Map].
seo-title: '[!DNL Activity Map] FAQ'
solution: Analytics
title: '[!DNL Activity Map] FAQ'
topic: Activity Map
uuid: e4f6d4e2-55d1-4e32-bf70-a334178af370
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# [!DNL Activity Map] FAQs

Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in [!DNL Activity Map].

## Implementierung und AppMeasurement {#section_FB46DD652E854C07AD339D7DD5CBCEC6}

**Q: Welche Implementierungsschritte sind für die Aktivierung der neuen Funktion erforderlich[!DNL Activity Map]?**

A: Bitte lesen Sie [Aktivieren Sie [!DNL Activity Map]](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**F: Haben alle Analytics-Kunden Zugriff auf die Seite „Activity Map – Aktivierung“ in den Admin Tools?**

A: Adobe SiteCatalyst customers do not have access to the Admin Console's [!DNL Activity Map] Enablement page. Nur Unternehmen mit Adobe Analytics Standard- und Adobe Analytics Premium-Verträgen haben Zugriff auf diese Konfigurationsseite.

**F: Kann der neue AppMeasurement-Code über Dynamic Tag Management (DTM) konfiguriert werden?**

A: Ja, Sie können den neuen AppMeasurement-Code [manuell implementieren](https://marketing.adobe.com/resources/help/en_US/dtm/analytics_dtm.html).

**F: Welche großen Änderungen wurden an der AppMeasurement v1.6-Bibliothek vorgenommen?**

A: The only change in AppMeasurement v1.6 is in the [!DNL Activity Map] link tracking process methodology that requires the collection of Page name, Link ID and RegionID.

**F: Wird das Rollout von AppMeasurement auf Domänenebene oder nur auf bestimmten Seiten ausgeführt?**

A: Das Rollout von AppMeasurement wird auf Report Suite-Ebene ausgeführt. Die Report Suite-Ebene ist typischerweise mit einer Domänenebene verbunden. Dies ist jedoch bei jeder Implementierung anders.

**[!DNL Activity Map]F: DTM lädt automatisch eine ältere Version (1.3.4) der Besucher-API als die von verlangte Version (1.5.1). Ist das ein Problem?**

A: Nein. [!DNL Activity Map] ist nicht von der VisitorAPI abhängig.

## [!DNL Activity Map] application {#section_E4F2DAC09EBA4E3BA7BACB49A0A89F8D}

**[!DNL Activity Map]F: Kann ich verwenden, wenn ich zuvor Besucher-ClickMap auf meiner Website nicht verwendet habe?**

A: Die Installation der älteren Version (wird jetzt auch einfach als ClickMap bezeichnet) ist keine Voraussetzung für die Implementierung der neuen Version. Für einen beschränkten Zeitraum wird die ältere Version weiterhin von Adobe unterstützt.

**Q: Welche Browser und Versionen werden unterstützt[!DNL Activity Map]?**

A: Es wird nur die jeweils neueste Version der vier gängigsten Browser (Chrome, Firefox, Safari und IE) unterstützt.

**F: Was sind die Standardeinstellungen für Überlagerungen?**

A: By default, [!DNL Activity Map] shows ALL links that have collected data.

Wenn Popupfenster über den Webseiten von Kunden angezeigt werden, können Überlagerungen für Links unter dem Popupfenster auch über dem Popupfenster angezeigt werden.

**F: Warum fehlen für einige Elemente, denen ein Rang zugewiesen wurde, die Überlagerungen?**

A: Einige Links mit einem Rang können auf der Seite verborgen sein (beispielsweise Links in Untermenüs). Daher werden die entsprechenden Linküberlagerungen nicht angezeigt. Sie können also damit rechnen, dass in einigen Überlagerungen bestimmte Rangwerte fehlen, da der Rang anhand aller Links auf der Seite (vorhandene und verborgene) berechnet wird.

**F: Wie wird die Rangzuweisung für Links im Bericht „Alle Links“ bestimmt?**

* In den Modi **Verlauf** und **Blase**: Die Rangzuweisung wird anhand der Metrikspalte bestimmt. Für Links mit dem gleichen Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* Im Modus **Gewinner und Verlierer** wird der Rang hauptsächlich anhand der Spalte „% Gewinn“ bestimmt. Für Links mit dem gleichen Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

**[!DNL Activity Map]F: Warum werden keine Link-Klickdaten erfasst, wenn ausgeführt wird?**

A: While [!DNL Activity Map] is in use, link click data is not collected by the Analytics tag. Dieses Verhalten folgt dem Verhalten des ClickMap-Plugins.

**F: Warum wird in der Metrik-Dropdownliste die gleiche Metrik mehrmals aufgeführt?**

A: [!DNL Activity Map] lists metrics for all report suites. [Daher können Sie mit Duplikaten rechnen, wenn das Unternehmen noch keine Metrikkonsolidierung vorgenommen hat](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/cm_transition.html).

Mit dem Metrikmenü können Sie die Liste berechneter Metriken auf diejenigen begrenzen, die der Report Suite der besuchten Seite zugewiesen sind.

**Q: Wie unterscheidet sich der Bericht "[!DNL Activity Map]Alle Links"von der[!DNL Activity Map]Berichterstellung in Reports &amp; Analysen?**

A: Um den Bericht "Alle Links"einzubeziehen, [!DNL Activity Map]erstellen wir eine Aufschlüsselungsanforderung wie folgt: Seite [!DNL Activity Map] = "visitedpage", aufgeschlüsselt nach [!DNL Activity Map] Link&amp;Region in `<list of link&regions present in the page at rendering time>`.

To get an equivalent report in Reports &amp; Analytics, you would need to first navigate to the [!DNL Activity Map] Page report. Dort filtern Sie nach dem Namen der besuchten Seite in [!DNL Activity Map]. The visited Pagename is shown in the left column in the [!DNL Activity Map] Page Details Bottom Panel. Once the page has been found, you can break down from that page and choose [!DNL Activity Map] Links &amp; Regions as a secondary dimension.

Beachten Sie jedoch, dass der in „Reports &amp; Analysen“ generierte Bericht alle Links und Regionen enthält, die für diese Seite erfasst wurden. But [!DNL Activity Map] only reports on Links&amp;Regions that are currently present in the webpage. Auf einer Nachrichtensite werden daher nur die Daten für den aktuell vorhandenen Artikel angezeigt, nicht für Artikel, die zu einem früheren Zeitpunkt am selben Tag zu sehen waren.

**[!DNL Activity Map]F: Wie funktioniert bei Seiten, die mehrere Tags für verschiedene Report Suites aufweisen?**

A: By default, [!DNL Activity Map] uses the report suite that is associated with the first tag that is sent by the page.

Sie können eine andere getaggte Report Suite auf der Registerkarte unter [!DNL Activity Map]Einstellungen für  &gt;  &gt; Andere auswählen.

**[!DNL Activity Map]F: Wie lange sucht das Analytics-Tag?**

A: Das Analytics-Tag wird bis zu 20 Sekunden nach einem Page Complete-Ereignis gesucht.

**Q: Wie werden dynamische Inhalte[!DNL Activity Map]behandelt?**

A: [!DNL Activity Map] checks every 2 seconds to see if it has found changes in the state of the web page such as:

* HTML-Inhalt wurde angezeigt
* HTML-Inhalt wurde verborgen
* Neuer HTML-Inhalt wurde eingefügt

Wird Inhalt verborgen oder angezeigt, so ändert die Anwendung automatisch den Status der betroffenen Links (und somit der Überlagerungen) von „verborgen“ in „angezeigt“ oder umgekehrt.

Wird neuer Inhalt eingefügt, ruft die Anwendung die zugehörigen Links ab, generiert Analysedaten für sie und fügt Überlagerungen für diese Links hinzu.

**F: Auf welcher Metrik basiert der Seitenflussbericht?**

A: Alle angezeigten Daten basieren auf Seitenansichten.

**Q: Können Sie das[!DNL Activity Map]Verhalten bei verschiedenen Seitentypen erklären?**

*Webseite ohne Analytics-Tag*

Unter der Symbolleiste wird eine Warnmeldung angezeigt, die angibt, dass kein Tag vorhanden ist.

*Webseite mit inkompatiblem Analytics-Tag (AppMeasurement v1.5 oder früher)*

Eine Warnmeldung weist darauf hin, dass Sie (/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md) den Seiten-Code auf Version 1.6 aktualisieren müssen.

*Webseite mit kompatiblem Analytics-Tag (AppMeasurement v1.6 oder höher), aber die[!DNL Activity Map]Berichterstellung wurde in den Admin Tools nicht aktiviert*

Es wird eine Warnmeldung angezeigt, die darauf hinweist, dass Sie Ihren Administrator bitten müssen, \[Bericht aktivieren\] [!DNL Activity Map] (/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md") zu aktivieren.

**Q: Kann ich[!DNL Activity Map]Daten (contextData) über den[Analytics-Datenfeed](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html)exportieren?**

A.: Nein.

## Segmentierung in [!DNL Activity Map]{#section_44D6C5F59B8542DC8A3AF38BD8078DCA}

**F: Sind Segmente auf bestimmte Benutzersegmente beschränkt? Or are shared Admin-level segments available in[!DNL Activity Map]?**

A: [!DNL Activity Map] inherits your Admin-level segments (reporting segments) from Analytics.

**F: Funktionieren Segmente im Livemodus?**

A: Nein, Segmente funktionieren nicht im Livemodus. Die Funktionalität entspricht der Echtzeit-Berichterstellung in „Reports &amp; Analytics“.

## Virtual Report Suites {#section_BDB0CA9E732F478EAC349A79753A78DB}

**Q: Ist[!DNL Activity Map]mit Virtual Report Suites kompatibel?**

A: Ja. However, due to virtual report suite limitations, [!DNL Activity Map]'s Live Mode is not compatible with virtual report suites.
