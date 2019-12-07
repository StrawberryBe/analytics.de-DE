---
description: 'null'
title: Verwenden der Integration
uuid: c902a868-20a7-42df-8a79-8e154608f299
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Verwenden der Integration{#using-the-integration}

Nach der Bereitstellung können Sie die zusätzlichen Funktionen dieser Integration nutzen.

**Hinweis**: Es kann 24-48 Stunden dauern, bis einige der dynamischen Signaldaten in Ihren Adobe Analytics-Berichten angezeigt werden.

Die folgenden Aktionen führen zu einem Mehrwert aus dieser Integration in Adobe Analytics.

## Anzeigen von Traffic- und Konversionsmetriken nach dynamischen Signaldimensionen{#viewing-traffic-and-conversion-metrics-by-dynamic-signal-dimensions}

Beispiel eines Berichts in Adobe Analytics.

Diese Integration bietet neue Dimensionen, die als Adobe Analytics-Berichte verfügbar werden. Der unten stehende Bericht ist ein Beispiel für die Analyse von Besuchen und einer Konversionsmetrik (Registrierungen), die nach Artikeltitel aufgeschlüsselt wurden.

![](assets/examplereport.png)

## Segmentierung nach dynamischen Signaldimensionen{#segmenting-by-dynamic-signal-dimensions}

Beispiele für Segmente, die auf dynamischen Signaldimensionen basieren.

Eine wichtige Funktion dieser Integration ist die Möglichkeit, Adobe Analytics-Segmente basierend auf den integrierten Berichterstellungsdimensionen zu erstellen. Sie können beispielsweise ein Segment erstellen, das nur Besuche aus einer bestimmten VoiceStorm-Community enthält. Sie könnten dies als "Besuche, die von SuperFans gesteuert werden"bezeichnen. Diese Segmentdefinition könnte wie folgt aussehen.

![](assets/segment1.png)

![](assets/segment2.png)

## Integrierte Berichtsdimensionen{#integrated-reporting-dimensions}

Listet die Dimensionen der dynamischen Signalberichterstellung auf, die in dieser Integration enthalten sind.

| Dimension | Beschreibung |
|---|---|
| Kanaltyp | Das soziale Netzwerk (oder die Blogging-Plattform), in dem der Benutzer einen Community-Beitrag freigegeben hat. Benutzer können einen Beitrag auf mehreren Kanälen freigeben. Klicks und andere Aktivitäten werden pro Kanal segmentiert. In diesem Feld werden Facebook, Twitter usw. angezeigt. damit Sie sehen können, welcher Kanaltyp die Aktivität antreibt. |
| Artikel-ID | Die Artikel-ID identifiziert jedes Inhaltselement in der Dynamic Signal-Community eindeutig. |
| Typ der Quelle | Dieses Feld gibt an, ob der Beitrag von einem "Mitglied"oder einer "Marke"erstellt wurde. Beachten Sie, dass in beiden Fällen Inhalte manuell in der Anwendung erstellt oder aus einem externen Feed importiert werden können. |
| Benutzername | Der Benutzer, der einen Beitrag in seinem/seinen sozialen Netzwerk(en) geteilt hat und Clickthroughs zu Ihrer Site generiert hat. |
| Quell-ID | Die Quell-ID identifiziert eindeutig den Ersteller (oder Autor) des freigegebenen Beitrags. Meistens handelt es sich dabei um ein bestimmtes Mitglied oder einen externen Feed. |
| Benutzer-ID | Die Benutzer-ID identifiziert eindeutig einen Benutzer (d. h. einen Mitglied) in der Dynamic Signal-Community. In diesem Fall ist der Benutzer der freigebende Benutzer, der den Beitrag in seinem/seinen sozialen Netzwerk(n) geteilt hat. |
| Name der Quelle | Die Quelle ist der Ersteller (oder Autor) des freigegebenen Beitrags. In den meisten Fällen ist dies ein Mitglied der Community oder ein externer Feed. |
| Artikeltitel | Der Titel des freigegebenen Beitrags, der Klicks zu Ihrer Site generiert hat. |
| Community-Name | Der Name Ihrer Dynamic Signal-Community. |

