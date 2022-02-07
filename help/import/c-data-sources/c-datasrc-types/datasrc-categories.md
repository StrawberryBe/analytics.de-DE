---
description: Mithilfe von Datenquellen-Kategorien werden die unterschiedlichen Datenquellen-Typen identifiziert, die ähnliche Funktionen bieten.
subtopic: Data sources
title: Übersicht über Datentypen und Kategorien
topic-fix: Developer and implementation
uuid: b5004cdc-b68a-4a82-a159-a7cd7b8bfe21
exl-id: d459fd06-a0fe-49e6-8624-b42f0c60ee6e
source-git-commit: 0b31585f5a928d68083764b80f3a08927b407387
workflow-type: ht
source-wordcount: '903'
ht-degree: 100%

---

# Übersicht über Datentypen und Kategorien

Mithilfe von Datenquellen-Kategorien werden die unterschiedlichen Datenquellen-Typen identifiziert, die ähnliche Funktionen bieten.

Kategorien bieten eine Möglichkeit, Datenquellen aus Sicht eines Benutzers zu gruppieren. Wählen Sie beim Erstellen einer Datenquelle über die [!DNL Data Sources]-Benutzeroberfläche zuerst eine Datenquellenkategorie und dann einen bestimmten Datenquellentyp aus. Jede Kategorie enthält Datenquellen-Typen, die ähnliche Datentypen unterstützen. [!DNL Data Sources] bietet die folgenden Datenquellenkategorien:

## Website-Gebrauch {#web-usage}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Webserver-Protokolldateien] | [Webprotokoll](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md) | Die meisten Webserver generieren Protokolldateien, die jede Seite in ihrem Versorgungsnetz aufzeichnen. Mithilfe dieser Datenquelle können Sie die Protokolldateien der meisten Webserver-Daten verarbeiten und diese Daten zu Ihren Berichten hinzufügen. |
| [!UICONTROL Massen-Upload in Advertising Cloud] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht den manuellen und von Excel automatisierten Massen-Upload in [!DNL Advertising Cloud]. |
| [!UICONTROL Traffic-Datenquelle auf Site-Ebene] | [Traffic](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) | Importiert Traffic-Daten für Ihre gesamte Website. Zum Beispiel [!UICONTROL Seitenansichten]. |
| [!UICONTROL Unterteilte Traffic-Datenquelle] | [Traffic](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md) | Importiert Traffic-Daten, die durch eine andere Website-Variable unterteilt werden. Beispiel: [!UICONTROL Seitenaufrufe] aufgeschlüsselt nach [!UICONTROL Produkt]. |

## Werbekampagnen   {#ad-campaigns}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Allgemeiner Werbeserver] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht es Ihnen, Impressionen und andere erstrangige Metriken zu den Werbebereitstellungsaktivitäten Ihres Werbeservers in Marketingberichte zu integrieren. Dies ist die generische Werbeserver-Datenquelle, die verwendet werden sollte, wenn Ihr spezifischer Werbeserver nicht unterstützt wird. |
| [!UICONTROL Allgemeiner E-Mail-Kampagnen-Server] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht es Ihnen, Metriken aus Ihrem E-Mail-Kampagnen-Server in Marketingberichte zu integrieren.  Üblicherweise integrierte Metriken umfassen die Anzahl der gesendeten, zugestellten und gelesenen Nachrichten. Dies ist die generische E-Mail-Kampagnen-Datenquelle, die verwendet werden sollte, wenn Ihr spezifischer E-Mail-Kampagnen-Server nicht unterstützt wird. |
| [!UICONTROL Allgemeiner Pay-Per-Click-Service] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen den Import von Daten zu Ihrer Pay-per-Click-Leistung einschließlich Impressionen, Klicks und Kosten.  Dies ist die generische Pay-per-Click-Datenquelle, die verwendet werden sollte, wenn Ihr spezifischer Pay-per-Click-Service nicht unterstützt wird. |

## CRM (Customer Relationship Management)   {#crm}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Allgemeines Callcenter] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen die Integration von Informationen zu Ihrer Telefonzentrale (Call Center) in Marketingberichte. Zu den häufiger importierten Metriken zählen die Anzahl der Anrufe, die Gesprächszeit, der Agent und der Gesamtumsatz.  Dies ist die generische Anrufzentrale-Datenquelle, die verwendet werden sollte, wenn Ihre spezifische Call-Center-Software nicht unterstützt wird. |
| [!UICONTROL Allgemeine Kundensupportanwendung] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen die Integration von Informationen aus Ihrer Kundensupport-Software in Marketingberichte. Diese enthält Metriken wie die Anzahl der neuen Fälle, die Anzahl der gelösten Fälle und den Zeitaufwand zur Lösung der Fälle.  Dies ist die generische Kundensupport-Datenquelle, die verwendet werden sollte, wenn Ihre spezifische Kundenservice-Anwendung nicht unterstützt wird. |

## Kundenzufriedenheit   {#csat}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Allgemeine Umfragedaten] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen die Integration der Umfrageergebnisse vom Tool eines Drittanbieters in Marketingberichte, sodass Sie einen Überblick darüber erhalten, wie zufrieden Kunden mit der Interaktion mit Ihrer Seite sind.  Dies ist die generische Umfragen-Datenquelle, die verwendet werden sollte, wenn Ihr spezifischer Umfragedatenservice nicht unterstützt wird. |

## Site-Leistung   {#performance}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Allgemeine Site-Ladegeschwindigkeit] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen die Integration von Daten einer Anwendung oder eines Service, mit dem die Geschwindigkeit Ihrer Downloads mit Ihren Daten verfolgt wird. Dies ist die generische Download-Geschwindigkeits-Datenquelle, die verwendet werden sollte, wenn Ihre spezifische Software oder Ihr spezifischer Service für die Download-Geschwindigkeit nicht unterstützt wird. |

## Generisch   {#generic}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Generische Datenquelle (nur Zusammenfassungsdaten)] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Verwenden Sie diese Datenquelle, wenn es keine bessere Entsprechung für den Datentyp gibt, den Sie in Marketing Reports &amp; Analysen importieren möchten. |
| [!UICONTROL Generische Datenquelle (volle Verarbeitung)] | Vollständige Verarbeitung | Adobe hat Datenquellen mit vollständiger Verarbeitung am 31. Januar 2022 als veraltet markiert. [Weitere Infos](/help/import/c-data-sources/c-datasrc-types/datasrc-fullproc-eol.md). Adobe empfiehlt, stattdessen die [Bulk Data Insertion API (BDIA](https://www.adobe.io/apis/experiencecloud/analytics/docs.html?lang=de) zu verwenden. |
| [!UICONTROL Generische Datenquelle (Transaktions-ID)] | <ul><li>Transaktions-ID</li><li>Besucher-ID</li></ul> | Ermöglicht es Ihnen, ein Offline-Ereignis mit einem Online-Ereignis zu verbinden. Die [!UICONTROL Transaktions-ID] dient als Schlüssel zwischen Offline- und Online-Ereignissen. |

## Online-Käufe {#purchases}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Produktrückgaben] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen den Import von Produktrückgabe-Daten, um sie einer Kauf-ID zuzuordnen, damit Sie Suchmaschinen, Keywords, Kampagnen und andere Attribute identifizieren können, die eher zu Rückgaben führen. |
| [!UICONTROL Produktkosten] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen die Angabe der tatsächlichen Kosten für über Ihre Website gekaufte und versandte Produkte, indem die Kosten oder die Gewinne einzelnen Produkten zugeordnet werden, um präzise Berichte zu den gewinnträchtigsten Kampagnen, Keywords und internen Aktionen für Ihre Website zu erstellen. |
| [!UICONTROL Bestellstatus] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht Ihnen die Verwendung von Metriken zur Ermittlung des Status aller eingegangenen Bestellungen, einschließlich stornierter, versendeter, abgeschlossener oder als betrügerisch gekennzeichneter Bestellungen. Die Berichte zum Bestellstatus ermöglichen es Ihnen, zu ermitteln, welche Akquisemethoden die höchste Bestellabschlussrate erzielen. |

## Interessenten und Preisangebote   {#leads}

| Datenquelle | Verarbeitungstyp | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Lead-Generierung] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht es Ihnen, Ergebnisinformationen zu den Interessenten für Ihre Site hochzuladen, darunter auch der tatsächlich generierte Umsatz.  Nachdem der Umsatz den Interessenten-IDs genau zugeordnet wurde, können Sie Ihre rentabelsten Kampagnen und Promotionen bestimmen. |
| [!UICONTROL Online-Preisangebot] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht es Ihnen, Ergebnisinformationen zu den Interessenten für Ihre Site hochzuladen, darunter auch der tatsächlich generierte Umsatz.  Nachdem der Umsatz den Interessenten-IDs genau zugeordnet wurde, können Sie Ihre rentabelsten Kampagnen und Promotionen bestimmen. |
| [!UICONTROL Telefonzentralendaten] | [Konversion](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md) | Ermöglicht es Ihnen, Call-Center-Transaktionen hochzuladen, damit Sie die Taktiken identifizieren können (Kampagnen, Aktionen usw.). die dazu führen, dass Kunden zum Hörer greifen. |
