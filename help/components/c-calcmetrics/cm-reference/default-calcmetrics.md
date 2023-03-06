---
description: Adobe bietet verschiedene berechnete Metriken, die Sie verwenden können. Auf dieser Seite werden diese Metriken und ihre Verwendungszwecke aufgelistet.
title: 'Referenz: Grundfunktionen'
feature: Calculated Metrics
exl-id: 1a49435c-96d1-4617-bd1a-a5d3b74e3ebd
source-git-commit: 2874ea66765e650a92bc39537d6a9eb8cebcd6a4
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 10%

---

# Berechnete Standardmetriken

Adobe Analytics bietet verschiedene berechnete Metriken, die die häufigsten Anwendungsfälle abdecken. Diese berechneten Metriken sind standardmäßig in Analysis Workspace verfügbar.

Im Folgenden finden Sie eine Liste der einzelnen berechneten Metriken, die von Adobe bereitgestellt werden, mit der beabsichtigten Funktion und der zugrunde liegenden Formel, die zur Berechnung verwendet wird:

>[!NOTE]
>
>Zusätzlich zu den auf dieser Seite beschriebenen standardmäßigen berechneten Metriken können Sie auch zusätzliche berechnete Metriken zu einer Report Suite hinzufügen.
>
>Sie können:
> * Fügen Sie standardmäßige berechnete Metriken für Streaming-Medien hinzu, wie unter [Berechnete Metriken](/https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * Erstellen Sie benutzerdefinierte berechnete Metriken aus vorhandenen Metriken, wie unter [Berechnete und erweiterte berechnete (abgeleitete) Metriken](/help/components/c-calcmetrics/cm-overview.md).



| Name der berechneten Metrik | Funktion | Formel |
|---------|----------|---------|
| Absprungrate | Das Verhältnis der Besuche, die genau einen Treffer enthielten, zur Anzahl der Besuche auf dieser Seite. Auf diese Weise können Sie erkennen, welche Dimensionselemente die höchste Absprungrate aufweisen, oder eine aggregierte Gesamtabsprungrate Ihrer Site im Zeitverlauf anzeigen. | Absprungrate |
| Umsatz/Besucher | Der durchschnittliche Umsatz, der von jedem einzelnen Besucher der Site generiert wurde. | <p>Umsatz</p><p>/</p><p>Unique Visitors</p> |
| Bestellungen/Besucher | Die durchschnittliche Anzahl von Bestellungen oder Transaktionen, die von jedem einzelnen Besucher der Site generiert wurden. | <p>Standardbestellungen</p><p>/</p><p>Besucher</p> |
| Umsatz/Besuche | Der durchschnittliche Umsatzbetrag, der durch einen einzelnen Besuch der Site generiert wurde. | <p>Umsatz</p><p>/</p><p>Unique Visits</p> |
| Umsatz/Bestellung | Der durchschnittliche Umsatzbetrag, der durch jede abgeschlossene Transaktion oder Bestellung auf der Site generiert wurde. | <p>Umsatz</p><p>/</p><p>Bestellung</p> |
| Bestellungen/Besuche | Der Prozentsatz der Besuche auf der Site, die zu einer abgeschlossenen Transaktion führen. | <p>Bestellung</p><p>/</p><p>Besuche</p> |
| Seitenansichten/Besuche | Die durchschnittliche Anzahl der Seiten, die ein Benutzer während eines einzelnen Besuchs der Site anzeigt. | <p>Seitenansichten</p><p>/</p><p>Besuche</p> |
| Besuche/Besucher | Die durchschnittliche Anzahl der Besuche eines Unique Visitors auf der Site. | <p>Besuche</p><p>/</p><p>Unique Visitors</p> |
| Neuladungen/Seitenansichten | Der Prozentsatz der Seitenansichten, die zu einem Neuladen oder Aktualisieren der Seite führten. | <p>Neuladungen</p><p>/</p><p>Seitenansichten</p> |
| Gewichtete Rücksendungsrate | Funktion | if(visit>percentile(visit),bouncerate,0) |
| Bestellhilfen | Die Häufigkeit, mit der ein Kanal oder eine Quelle zur Journey eines Kunden beigetragen hat, aber nicht zum endgültigen Kauf führte. | <p>Bestellungen (Beitrag\|Besuch)</p><p>–</p><p>Bestellungen</p> |
| Ausstiegsrate | Der Prozentsatz der Besucher, die die Site nach Ansicht einer bestimmten Seite verlassen. | <p>Ausstiege</p><p>/</p><p>Besuche</p> |
| Einstiegsrate | Der Prozentsatz der Besucher, die die Site auf einer bestimmten Seite aufgerufen haben, in Bezug auf die Gesamtzahl der Sitzungen auf der Site. | <p>Einstiege</p><p>/</p><p>Besuche</p> |
| Durchschnittliche Besuchszeit pro Site | Die durchschnittliche Zeit, die ein Besucher auf der Site verbringt, bevor er die Site verlässt oder wegnavigiert. | Durchschnittliche Besuchszeit pro Site (Sekunden) |
| Besuchszeit/Benutzer (Status) | Die Zeitdauer, die der durchschnittliche Besucher in einem bestimmten Bundesstaat auf der Site verbringt. | Metrik &quot;Zeit pro Besucher (Sekunden)&quot;und Segment &quot;Mobile App&quot; |
| Benutzer (Mobil) | Gesamtanzahl der Benutzer einer mobilen App | Metrik &quot;Unique Visitors&quot;und Segment &quot;Mobile App-Benutzer&quot; |
| App-Benutzer | Gesamtanzahl der Benutzer einer mobilen App | Unique Visitors-Metrik + Mobile-App-Segment |
| Statusansichten | Die Anzahl der Ansichten für die verschiedenen Status oder Bildschirme der App | Metrik &quot;Seitenansichten&quot;+ Segment &quot;Mobile App&quot; |
| Aktionen | Die Gesamtzahl der in der App durchgeführten Aktionen | Metrik Benutzerspezifische Link-Instanzen + Aktionssegment |
| Akquise-Link-Klicks | Die Häufigkeit, mit der Benutzer auf einen Link klicken, mit dem der Traffic zur Site geleitet werden soll. | Kampagnen-Clickthrough-Metrik |
| Seitengeschwindigkeit | Die Anzahl der zusätzlichen Seitenansichten, die ein Inhaltselement generiert. Auf diese Weise können Sie feststellen, welche Inhalte zusätzliche Interaktionen erfordern. | <p>Seitenansichten</p><p>/</p><p>Besuche</p> |
| Konversionsrate | Der Prozentsatz der Besucher, die eine gewünschte Aktion durchgeführt haben, z. B. einen Kauf getätigt haben. | <p>Bestellungen</p><p>/</p><p>Besuche</p> |
| Durchschnittliche Sitzungslänge (Mobil) | Die durchschnittliche Zeit, die Besucher während einer einzelnen Sitzung auf der Site verbringen. | Leer |
| Experience Cloud-ID-Abdeckung | Der Prozentsatz der Besucher, die über eine Experience Cloud-ID verfügen. | <p>Besucher mit Experience Cloud ID</p><p>/</p><p>Unique Visitors</p> |
| Content-Geschwindigkeit | Die Geschwindigkeit, mit der neue Inhalte auf der Site erstellt und veröffentlicht werden und wie schnell sie Benutzerinteraktionen generieren. | <p>Seitenansichten</p><p>/</p><p>Besuche</p> |
| Unique Visitors (ITP 2.1) / Unique Visitors | Der Prozentsatz der Unique Visitors, die einen Browser verwenden, der von ITP 2.1-Cookie-Beschränkungen betroffen ist. Mit anderen Worten, Kunden, die keine CNAME-Implementierung verwenden. (Dies gilt für Kunden, die Cookies über clientseitiges JavaScript setzen.) | <p>Unique Visitors-Metrik + ITP-Besucher-Segment</p><p>/</p><p>Unique Visitors</p> |
| Unique Visitors/Unique Visitors, die nach 7 Tagen zurückkehren | Der Prozentsatz der Unique Visitors, die nach einem Zeitraum von 7 oder mehr Tagen zurückkehren. | <p>Metrik &quot;Unique Visitors&quot;+ Benutzer, die nach dem 7-Tage-Segment zurückkehren</p><p>/</p><p>Unique Visitors</p> |
| Seitenansichten/Unique Visitor | Die durchschnittliche Anzahl der angezeigten Seiten für jeden Unique Visitor der Site. | <p>Seitenansichten</p><p>/</p><p>Unique Visitors</p> |
| Besuche / Besucher | Die durchschnittliche Anzahl der Besuche eines Unique Visitors auf der Site . | <p>Besuche</p><p>/</p><p>Unique Visitors</p> |
| Geschätzte Unique Visitors (ITP 2.1) | <p>Für ITP-Besucher (Benutzer in Safari-Browsern) teilen Sie Unique Visitors durch 2 oder weniger.</p><p>Dabei wird davon ausgegangen, dass Sie Cookies mit clientseitigem JavaScript setzen (ohne eine CNAME-Implementierung zu verwenden). Implementierungen, die Cookies mit clientseitigem JavaScript setzen, wurden ab ITP 2.1 beeinträchtigt. Siehe: [https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/)</p> | <p>Unique Visitors-Metrik + ITP-Besucher (ITP 2.1, Implementierungen ohne CNAME)</p><p>/</p><p>Unique Visitors-Metrik + Segment &quot;Nicht-ITP-Besucher&quot;(ITP 2.1, Nicht-CNAME-Implementierungen)</p> |
| Seitenansichten/Geschätzte Unique Visitors (ITP 2.1) | Die durchschnittliche Anzahl der angezeigten Seiten für geschätzte Unique Visitors (ITP 2.1). | <p>Unique Visitors-Metrik + ITP-Besucher (ITP 2.1, Implementierungen ohne CNAME)</p><p>/</p><p>Unique Visitors-Metrik + Segment &quot;Nicht-ITP-Besucher&quot;(ITP 2.1, Nicht-CNAME-Implementierungen)</p> |

{style="table-layout:auto"}
