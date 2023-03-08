---
description: Adobe bietet verschiedene berechnete Metriken, die Sie verwenden können. Auf dieser Seite werden diese Metriken und ihre Verwendungszwecke aufgelistet.
title: Standardberechnete Metriken
feature: calculated metrics
exl-id: 1a49435c-96d1-4617-bd1a-a5d3b74e3ebd
source-git-commit: 43bb7102e2caff93c3beea6e8c23500347679327
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 4%

---

# Standardberechnete Metriken

Adobe Analytics bietet verschiedene berechnete Metriken, die die häufigsten Anwendungsfälle abdecken. Diese berechneten Metriken sind in Analysis Workspace standardmäßig verfügbar.

Im Folgenden finden Sie eine Liste aller berechneten Metriken, die von Adobe bereitgestellt werden, mit der beabsichtigten Funktion und der zugrunde liegenden Formel, die zur Berechnung verwendet wird:

>[!NOTE]
>
>Zusätzlich zu den auf dieser Seite beschriebenen standardmäßigen berechneten Metriken können Sie auch zusätzliche berechnete Metriken zu einer Report Suite hinzufügen.
>
>Sie können:
> * Fügen Sie standardmäßige berechnete Metriken für Streaming-Medien hinzu, wie unter [Berechnete Metriken](/https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * Erstellen Sie benutzerdefinierte berechnete Metriken aus vorhandenen Metriken, wie unter [Berechnete und erweiterte berechnete (abgeleitete) Metriken](/help/components/c-calcmetrics/cm-overview.md).



| Name der berechneten Metrik | Funktion | Formel |
|---------|----------|---------|
| Absprungrate | Das Verhältnis der Besuche, die genau einen Treffer enthielten, zur Anzahl der Besuche auf dieser Seite. Auf diese Weise können Sie erkennen, welche Dimensionselemente die höchste Absprungrate aufweisen, oder eine aggregierte Gesamtabsprungrate Ihrer Site im Zeitverlauf anzeigen. | `[Bounces] / [Entries]` |
| Umsatz/Besucher | Der durchschnittliche Umsatz, der von jedem einzelnen Besucher der Site generiert wurde. | `[Revenue] / [Unique Visitors]` |
| Bestellungen/Besucher | Die durchschnittliche Anzahl von Bestellungen oder Transaktionen, die von jedem einzelnen Besucher der Site generiert wurden. | `[Orders] / [Unique Visitors]` |
| Umsatz/Besuche | Der durchschnittliche Umsatzbetrag, der durch einen einzelnen Besuch der Site generiert wurde. | `[Revenue] / [Visits]` |
| Umsatz/Bestellung | Der durchschnittliche Umsatzbetrag, der durch jede abgeschlossene Transaktion oder Bestellung auf der Site generiert wurde. | `[Revenue] / [Orders]` |
| Bestellungen/Besuche | Der Prozentsatz der Besuche auf der Site, die zu einer abgeschlossenen Transaktion führen. | `[Orders] / [Visits]` |
| Seitenansichten/Besuche | Die durchschnittliche Anzahl der Seiten, die ein Benutzer während eines einzelnen Besuchs der Site anzeigt. | `[Page Views] / [Visits]` |
| Besuche/Besucher | Die durchschnittliche Anzahl der Besuche eines Unique Visitors auf der Site. | `[Visits] / [Unique Visitors]` |
| Neuladungen/Seitenansichten | Der Prozentsatz der Seitenansichten, die zu einem Neuladen oder Aktualisieren der Seite führten. | `[Reloads] / [Page Views]` |
| Gewichtete Rücksendungsrate | Funktion | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |
| Bestellhilfen | Die Häufigkeit, mit der ein Kanal oder eine Quelle zur Journey eines Kunden beigetragen hat, aber nicht zum endgültigen Kauf führte. | `[Orders (Visit Participation)] - [Orders]` |
| Ausstiegsrate | Der Prozentsatz der Besucher, die die Site nach Ansicht einer bestimmten Seite verlassen. | `[Exits] / [Visits]` |
| Einstiegsrate | Der Prozentsatz der Besucher, die die Site auf einer bestimmten Seite aufgerufen haben, in Bezug auf die Gesamtzahl der Sitzungen auf der Site. | `[Entries] / [Visits]` |
| Durchschnittliche Besuchszeit pro Site | Die durchschnittliche Zeit, die ein Besucher auf der Site verbringt, bevor er die Site verlässt oder wegnavigiert. | `[Average Time Spent on Site (Seconds)]` |
| Besuchszeit/Benutzer (Status) | Die Zeitdauer, die der durchschnittliche Besucher in einem bestimmten Bundesstaat auf der Site verbringt. | `[Mobile App Users] (segment)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| Benutzer (Mobil) | Gesamtanzahl der Benutzer einer mobilen App | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| App-Benutzer | Gesamtanzahl der Benutzer einer mobilen App | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| Statusansichten | Die Anzahl der Ansichten für die verschiedenen Status oder Bildschirme der App | `[Mobile App Users] (segment)`<br>`[Page Views] (metric)` |
| Aktionen | Die Gesamtzahl der in der App durchgeführten Aktionen | `[Has an Action] (segment)`<br>`[Custom Link Instances] (metric)` |
| Akquise-Link-Klicks | Die Häufigkeit, mit der Benutzer auf einen Link klicken, mit dem der Traffic zur Site geleitet werden soll. | `[Campaign Click-throughs]` |
| Seitengeschwindigkeit | Die Anzahl der zusätzlichen Seitenansichten, die ein Inhaltselement generiert. Auf diese Weise können Sie feststellen, welche Inhalte zusätzliche Interaktionen erfordern. | `[Page Views] / [Visits]` |
| Konversionsrate | Der Prozentsatz der Besucher, die eine gewünschte Aktion durchgeführt haben, z. B. einen Kauf getätigt haben. | `[Orders] / [Visits]` |
| Durchschnittliche Sitzungslänge (Mobil) | Die durchschnittliche Zeit, die Besucher während einer einzelnen Sitzung auf der Site verbringen. | Leer |
| Experience Cloud-ID-Abdeckung | Der Prozentsatz der Besucher, die über eine Experience Cloud-ID verfügen. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| Content-Geschwindigkeit | Die Geschwindigkeit, mit der neue Inhalte auf der Site erstellt und veröffentlicht werden und wie schnell sie Benutzerinteraktionen generieren. | `[Page Views] / [Visits]` |
| Unique Visitors (ITP 2.1) / Unique Visitors | Der Prozentsatz der Unique Visitors, die einen Browser verwenden, der von ITP 2.1-Cookie-Beschränkungen betroffen ist. Mit anderen Worten, Kunden, die keine CNAME-Implementierung verwenden. (Dies gilt für Kunden, die Cookies über clientseitiges JavaScript setzen.) | `[Unique Visitors metric with ITP Visitors segment] / [Unique Visitors]` |
| Unique Visitors/Unique Visitors, die nach 7 Tagen zurückkehren | Der Prozentsatz der Unique Visitors, die nach einem Zeitraum von 7 oder mehr Tagen zurückkehren. | `[Unique Visitors metric with Users returning after 7 days segment] / [Unique Visitors]` |
| Seitenansichten/Unique Visitor | Die durchschnittliche Anzahl der angezeigten Seiten für jeden Unique Visitor der Site. | `[Page Views] / [Unique Visitors]` |
| Besuche/Besucher | Die durchschnittliche Anzahl der Besuche eines Unique Visitors auf der Site . | `[Visits] / [Unique Visitors]` |
| Geschätzte Unique Visitors (ITP 2.1) | Teilen Sie für ITP-Besucher (Benutzer in Safari-Browsern) Unique Visitors durch 2 oder weniger. Diese berechnete Metrik setzt voraus, dass Sie Cookies mit clientseitigem JavaScript setzen (ohne eine CNAME-Implementierung zu verwenden). Implementierungen, die Cookies mit clientseitigem JavaScript setzen, wurden ab ITP 2.1 beeinträchtigt. Siehe [Intelligente Tracking-Prävention](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) für Details. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Seitenansichten/Geschätzte Unique Visitors (ITP 2.1) | Die durchschnittliche Anzahl der angezeigten Seiten für geschätzte Unique Visitors (ITP 2.1). | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |

{style="table-layout:auto"}
