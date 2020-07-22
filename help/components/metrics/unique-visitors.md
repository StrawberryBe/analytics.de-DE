---
title: Individuelle Besucher
description: Die Anzahl der Einzelpersonen (oder Geräte).
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 10%

---


# Individuelle Besucher

Die Metrik &quot;Individuelle Besucher&quot;zeigt die Anzahl der Besucher-IDs für das Dimensionselement an. Es handelt sich dabei um eine der am häufigsten verwendeten Metriken zur Bestimmung des Datenverkehrs, da es einen Überblick über die Popularität eines Dimensionselements auf hoher Ebene gibt. Ein Besucher kann beispielsweise jeden Tag einen Monat lang zu Ihrer Site gelangen, zählt jedoch immer noch als individueller Besucher.

Wenn Sie [geräteübergreifende Analysen](../cda/overview.md)verwenden, wird diese Metrik in &quot;Unique Devices&quot;umbenannt.

## Individuelle Besucher pro Tag, Woche, Monat, Quartal und Jahr

Reports &amp; Analytics bietet Optionen für individuelle Besucher pro Tag, Woche, Monat, Quartal und Jahr. Statt einen einzelnen eindeutigen Besucher für den gesamten Zeitraum zu zählen, werden individuelle Besucher auf der Grundlage der ausgewählten Metrik gezählt. Beispielsweise möchten Sie sich individuelle Besucher pro Tag für Ihre Site ansehen. Wenn ein Besucher morgens und nachts zu Ihrer Site kommt, zählt er als individueller Besucher pro Tag. Wenn ein Besucher am Montag und erneut am Dienstag Ihre Site aufsucht, zählen sie als zwei individuelle Besucher pro Tag.

Analysis Workspace behandelt individuelle Besucher auf Grundlage der Granularität des Berichts. Wenn Sie beispielsweise die Dimension [&quot;Tag](../dimensions/day.md) &quot;verwenden, sehen Sie für jedes Dimensionselement tägliche eindeutige Besucher. Für die Berichtssumme werden jedoch eindeutige Besucher für den Datumsbereich der Freiformtabelle dedupliziert.

## Berechnung dieser Metrik

Diese Metrik zählt die Anzahl der eindeutigen Besucher-IDs für ein bestimmtes Dimensionselement. Es verwendet mehrere erweiterte Mechanismen, um individuelle Besucher zu identifizieren, da es mehrere Möglichkeiten gibt, diese zu identifizieren. In der folgenden Tabelle werden die Identifizierungswege eines Besuchers und seine Priorität Liste. Einige Treffer können über mehrere Besucher-Identifizierungsmethoden verfügen. in diesen Fällen wird die Methode mit höherer Priorität verwendet.

| Verwendete Reihenfolge | Abfrageparameter (Erfassungsmethode) | Vorhanden, wenn |
| --- | --- | --- |
| 1 | `vid` | Die [`visitorID`](/help/implement/vars/config-vars/visitorid.md) Variable wird eingestellt. |
| 2 | `aid` | Besucher verfügt über ein vorhandenes [`s_vi`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html) Cookie. Wird bei Implementierungen ohne oder vor der Implementierung des Besucher-ID-Diensts eingestellt. |
| 3 | `mid` | Besucher verfügt über ein vorhandenes [`s_ecid`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html) Cookie. Wird bei Implementierungen mit dem [Adobe Experience Cloud-Identitätsdienst](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html)eingestellt. |
| 4 | `fid` | Besucher hat ein bestehendes [`s_fid`](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-analytics.html) Cookie, oder wenn `aid` und `mid` nicht eingestellt werden konnte. |
| 5 | IP-Adresse, Benutzeragent, Gateway-IP-Adresse | Letzter Ausweg zur Identifizierung eines eindeutigen Besuchers, wenn der Browser des Besuchers keine Cookies akzeptiert. |

>[!NOTE]
>
>Jede Analytics-Besucher-ID ist an ein Profil auf Adobe-Servern gebunden. Diese Besucher-Profil werden nach mindestens 13 Monaten Inaktivität gelöscht, unabhängig vom Ablauf eines Besucher-ID-Cookies.

## Verhalten, das sich auf die Anzahl der individuellen Besucher auswirkt

Eindeutige Besucher-IDs werden in der Regel in einem Browsercookie gespeichert. Ein neuer eindeutiger Besucher wird gezählt, wenn einer der folgenden Vorgänge ausgeführt wird:

* Löscht ihren Cache jederzeit
* Öffnet einen anderen Browser auf demselben Computer. Pro Browser wird ein eindeutiger Besucher gezählt.
* Derselbe Benutzer surft auf verschiedenen Geräten auf Ihrer Site. Ein separater eindeutiger Besucher wird pro Gerät gezählt. Sie können [geräteübergreifende Analysen](../cda/overview.md) verwenden, um Besucher mithilfe der Metrik &quot; [Personen](people.md) &quot;miteinander zu kombinieren.
* Öffnet eine private Browsersitzung (z. B. Chrome&#39;s Registerkarte &quot;Inkognito&quot;).

Ein neuer eindeutiger Besucher wird *nicht* gezählt, solange die Cookie-ID beibehalten wird:

* Schließt den Browser über einen längeren Zeitraum
* Aktualisieren des Browsers auf die neueste Version
