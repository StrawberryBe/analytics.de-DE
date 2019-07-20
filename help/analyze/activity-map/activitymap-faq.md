---
description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map
seo-description: Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map
seo-title: Activity Map – Häufig gestellte Fragen
solution: Analytics
title: Activity Map – Häufig gestellte Fragen
topic: Activity Map
uuid: e 4 f 6 d 4 e 2-55 d 1-4 e 32-bf 70-a 334178 af 370
translation-type: tm+mt
source-git-commit: 8f72f8cf086be0eade5616b074123a9f22e33347

---


# Activity Map – Häufig gestellte Fragen

Häufig gestellte Fragen zum Einrichten, Konfigurieren und Anwenden der Funktionen in Activity Map

## Implementierung und AppMeasurement {#section_FB46DD652E854C07AD339D7DD5CBCEC6}

**F: Welche Implementierungsschritte sind zur Aktivierung der neuen Activity Map erforderlich?**

A: Lesen Sie [Activity Map aktivieren](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md)

**F: Haben alle Analytics-Kunden Zugriff auf die Seite „Activity Map – Aktivierung“ in den Admin Tools?**

A: Adobe SiteCatalyst-Kunden haben keinen Zugriff auf die Seite „Activity Map – Aktivierung“ in der Admin Console. Nur Unternehmen mit Adobe Analytics Standard- und Adobe Analytics Premium-Verträgen haben Zugriff auf diese Konfigurationsseite.

**F: Kann der neue AppMeasurement-Code über Dynamic Tag Management (DTM) konfiguriert werden?**

A: Ja, Sie können den neuen AppMeasurement-Code [manuell implementieren](https://marketing.adobe.com/resources/help/en_US/dtm/analytics_dtm.html).

**F: Welche großen Änderungen wurden an der AppMeasurement v1.6-Bibliothek vorgenommen?**

A: Die einzige Änderung in AppMeasurement v1.6 ist die Linktracking-Methode in Activity Map, für die Seitenname, Link-ID und Regions-ID erfasst werden müssen.

**F: Wird das Rollout von AppMeasurement auf Domänenebene oder nur auf bestimmten Seiten ausgeführt?**

A: Das Rollout von AppMeasurement wird auf Report Suite-Ebene ausgeführt. Die Report Suite-Ebene ist typischerweise mit einer Domänenebene verbunden. Dies ist jedoch bei jeder Implementierung anders.

**F: DTM lädt automatisch eine ältere Version (1.3.4) der Besucher-API als die von Activity Map verlangte Version (1.5.1). Ist das ein Problem?**

A: Nein. Die Activity Map-Funktion hängt nicht von der Besucher-API ab.

## Activity Map application {#section_E4F2DAC09EBA4E3BA7BACB49A0A89F8D}

**F: Kann ich Activity Map verwenden, wenn ich zuvor Besucher-ClickMap auf meiner Website nicht verwendet habe?**

A: Die Installation der älteren Version (wird jetzt auch einfach als ClickMap bezeichnet) ist keine Voraussetzung für die Implementierung der neuen Version. Für einen beschränkten Zeitraum wird die ältere Version weiterhin von Adobe unterstützt.

**F: Welche Browser und Versionen werden von Activity Map unterstützt?**

A: Es wird nur die jeweils neueste Version der vier gängigsten Browser (Chrome, Firefox, Safari und IE) unterstützt.

**F: Was sind die Standardeinstellungen für Überlagerungen?**

A: Standardmäßig zeigt Activity Map Überlagerungen für ALLE Links mit erfassten Daten an.

Wenn Popupfenster über den Webseiten von Kunden angezeigt werden, können Überlagerungen für Links unter dem Popupfenster auch über dem Popupfenster angezeigt werden.

**F: Warum fehlen für einige Elemente, denen ein Rang zugewiesen wurde, die Überlagerungen?**

A: Einige Links mit einem Rang können auf der Seite verborgen sein (beispielsweise Links in Untermenüs). Daher werden die entsprechenden Linküberlagerungen nicht angezeigt. Sie können also damit rechnen, dass in einigen Überlagerungen bestimmte Rangwerte fehlen, da der Rang anhand aller Links auf der Seite (vorhandene und verborgene) berechnet wird.

**F: Wie wird die Rangzuweisung für Links im Bericht „Alle Links“ bestimmt?**

* In den Modi **Verlauf** und **Blase**: Die Rangzuweisung wird anhand der Metrikspalte bestimmt. Für Links mit dem gleichen Metrikwert basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.
* Im Modus **Gewinner und Verlierer** wird der Rang hauptsächlich anhand der Spalte „% Gewinn“ bestimmt. Für Links mit dem gleichen Gewinn basiert der Rang außerdem auf der alphabetischen Reihenfolge der Link-IDs.

**F: Warum werden keine Link-Klickdaten erfasst, wenn Activity Map ausgeführt wird?**

A: Während Activity Map in Verwendung ist, werden keine Link-Klickdaten vom Analytics-Tag erfasst. Dieses Verhalten folgt dem Verhalten des ClickMap-Plugins.

**F: Warum wird in der Metrik-Dropdownliste die gleiche Metrik mehrmals aufgeführt?**

A: Activity Map listet Metriken für alle Report Suites auf. [Daher können Sie mit Duplikaten rechnen, wenn das Unternehmen noch keine Metrikkonsolidierung vorgenommen hat](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/cm_transition.html).

Mit dem Metrikmenü können Sie die Liste berechneter Metriken auf diejenigen begrenzen, die der Report Suite der besuchten Seite zugewiesen sind.

**F: Wo liegt der Unterschied zwischen dem Activity Map-Bericht „Alle Links“ und der Activity Map-Berichterstattung in „Reports &amp; Analytics“?**

A: To pull the All Links Report in Activity Map, we create a breakdown request as follows: Activity Map Page = “visitedpage”, broken down by Activity Map Link&amp;Region in `<list of link&regions present in the page at rendering time>`.

Um einen entsprechenden Bericht in „Reports &amp; Analytics“ zu erhalten, müssen Sie zunächst zum Activity Map-Seitenbericht navigieren. Dort filtern Sie nach dem Namen der besuchten Seite in Activity Map. Der Name der besuchten Seite wird in der linken Spalte der Activity Map-Seitendetails im unteren Bereich angezeigt. Sobald die Seite gefunden wurde, können Sie die Aufschlüsselung vornehmen und Activity Map-Links und -Regionen als sekundäre Dimension auswählen.

Beachten Sie jedoch, dass der in „Reports &amp; Analysen“ generierte Bericht alle Links und Regionen enthält, die für diese Seite erfasst wurden. Activity Map erstellt jedoch nur Berichte für Links und Regionen, die aktuell auf der Webseite vorhanden sind. Auf einer Nachrichtensite werden daher nur die Daten für den aktuell vorhandenen Artikel angezeigt, nicht für Artikel, die zu einem früheren Zeitpunkt am selben Tag zu sehen waren.

**F: Wie funktioniert Activity Map bei Seiten, die mehrere Tags für verschiedene Report Suites aufweisen?**

A: Standardmäßig verwendet Activity Map die Report Suite, die mit dem ersten Tag verbunden ist, das von der Seite gesendet wird.

Sie können eine andere getaggte Report Suite auf der Registerkarte unter Einstellungen für Activity Map &gt; Andere auswählen.

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

Eine Warnmeldung weist darauf hin, dass Sie den Seiten-Code auf v 1.6 aktualisieren müssen (/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable. md).

*Webseite mit kompatiblem Analytics-Tag (AppMeasurement v1.6 oder höher), für die jedoch die Activity Map-Berichterstattung in den Admin Tools nicht aktiviert wurde*

Es wird eine Warnmeldung angezeigt, die angibt, dass Sie Ihren Administrator nach\ [Activity Map-Bericht\] (/home/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable. md "fragen müssen.)

**F: Kann ich Activity Map-Daten (contextData) über[Analytics Data Feed](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html)exportieren?**

A.: Nein.

## Segmentierung in Activity Map {#section_44D6C5F59B8542DC8A3AF38BD8078DCA}

**F: Sind Segmente auf bestimmte Benutzersegmente beschränkt? Oder gibt es freigegebene Segmente auf Admin-Ebene in Activity Map?**

A: Activity Map übernimmt Ihre Segmente auf Administratorebene (Berichtssegmente) aus Analytics.

**F: Funktionieren Segmente im Livemodus?**

A: Nein, Segmente funktionieren nicht im Livemodus. Die Funktionalität entspricht der Echtzeit-Berichterstellung in „Reports &amp; Analytics“.

## Virtual report suites {#section_BDB0CA9E732F478EAC349A79753A78DB}

**F: Ist Activity Map mit Virtual Report Suites kompatibel?**

A: Ja. Aufgrund der Einschränkungen der Virtual Report Suites ist jedoch der Livemodus von Activity Map nicht mit Virtual Report Suites kompatibel.
