---
description: Beschreibungen von Berichtstypen, die in Experience Cloud verwendet werden.
title: Berichtstypen
topic: Ad hoc analysis
uuid: 357102eb-a172-40ec-a302-01c87abaacb5
translation-type: tm+mt
source-git-commit: 5d96a2868bee48e2294ec2fb27e0340a3bcc50ae
workflow-type: tm+mt
source-wordcount: '1731'
ht-degree: 99%

---


# Berichtstypen

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 zum Lebensende. [Weitere Infos](https://adobe.ly/discoverworkspace)

Beschreibungen von Berichtstypen, die in Experience Cloud verwendet werden.

## Rangberichte {#concept_E1710FFFBB334F3D9DB63A1626DBCB01}

Zeigen eine Tabelle mit Elementen in einer Rangfolge an, wobei in den Metriken Zahlen und Prozentsätze genutzt werden. So ordnet beispielsweise der [!UICONTROL Seitenbericht] die Seiten Ihrer Website auf Grundlage des Datenverkehrs an, und in der Detailtabelle werden Prozentsätze und Zahlen für Metriken wie Seitenansichten und Umsatz angezeigt. Standardmäßig erfolgt die Darstellung in Form eines horizontalen Balkendiagramms. Jede Metrik ist im Diagramm mit einer eigenen Farbe gekennzeichnet. Bei Rangberichten können mehrere Metriken in einem Bericht angezeigt werden.

<!-- 

c_reports_ranked.xml

 -->

Ranggraphen umfassen standardmäßig fünf Elemente, Sie haben in den Diagrammoptionen aber die Möglichkeit, bis zu 30 Elemente aufzunehmen.

## Trendberichte {#concept_65FEA92704024232BB21A5952939711F}

Hiermit können Sie Trends zu Konversionen und Ereignissen während des Berichtzeitraums für eine ausgewählte Zeit-Granularität (Stunde, Tag, Woche, Monat, Quartal oder Jahr) untersuchen.

<!-- 

c_reports_trended.xml

 -->

Im Diagramm werden die nachverfolgten Elemente auf der vertikalen Achse angezeigt. Die horizontale Achse zeigt die Zeit-Granularität. In der Tabelle können Sie einen Trend auf Grundlage einer bestimmten Zelle erstellen und einen vollständigen Bericht aus dieser Zelle generieren. Datum und Uhrzeit basieren dabei auf dem Zellenwert.

Sie können auch mehrere Zellen auswählen und einen Trendbericht mit der ausgewählten Granularität starten. Wenn Sie einen Trend auf Grundlage mehrerer Zellen analysieren, werden in den Berichtspalten Daten für den gesamten Berichtzeitraum angezeigt.

Ein Beispiel für einen Trendbericht ist der [!UICONTROL Produktbericht]. Hier können Sie sehen, wie viel Umsatz ein Produkt während des ausgewählten Zeitraums generiert hat. Wenn der Berichtzeitraum eine Woche ist, können Sie sehen, wie viel Umsatz das Produkt für jeden Tag des Zeitraums generiert hat. Sie können ein Trenddiagramm zu einen spezifischen Produkt an einem bestimmten Tag anzeigen oder einen separaten Trendbericht für die Auswahl öffnen.

## Trendbericht aus Zellen {#task_AD9275BED5CE4D61AC25778D144406A4}

Schritte, die beschreiben, wie Sie aus einer oder mehreren Zellen einer Tabelle einen Trendbericht starten.

<!-- 

t_trend_row.xml

 -->

**So erstellen Sie Trendberichte aus Zellen**

1. Öffnen Sie einen Rangbericht.
1. Suchen Sie nach der Zelle in der Tabelle und klicken Sie auf **[!UICONTROL Trend]**.

   ![](assets/TrendInspector_Buttcon.png)

1. Um einen vollständigen Bericht zu der Zelle anzuzeigen, klicken Sie auf **[!UICONTROL Trendbericht starten]**.

   Alternativ können Sie mit der rechten Maustaste auf die Zelle und dann auf **[!UICONTROL Zelle als Trend verfolgen]** klicken. Sie können diese Aufgabe aus ausführen, nachdem Sie mehrere Zellen ausgewählt haben.

## Summenbericht {#concept_48E23FB3BCCD43DFB486A048960800A8}

<!-- 

c_reports_totals.xml

 -->

Ein Bericht für Führungskräfte, der Ergebniszahlen anzeigt. Er enthält Daten zu Gesamtumsatz, Seitenansichten und Bestellungen. Sie können den Bericht segmentieren und ihm weitere Metriken hinzufügen, um weitere Daten anzuzeigen.

## Flussberichte {#concept_3E417D018F1B4566973F694B01E6439F}

Flussberichte zeigen die gängigsten Pfade, die Benutzer auf Seiten, Site-Abschnitten und Servern nehmen.

<!-- 

c_reports_flow.xml

 -->

**Nächster Fluss**

Die Berichtsgruppe [!UICONTROL Nächster Fluss] besteht aus drei Berichten: [!UICONTROL Nächster Seitenfluss], [!UICONTROL Nächster Abschnittsfluss] und [!UICONTROL Nächster Serverfluss]. Die Berichte in dieser Gruppe zeigen Ihnen die häufigsten Seiten, Sitebereiche und Server, die ein Besucher nach dem Aufrufen der von Ihnen angegebenen Seite, des Sitebereichs oder des Servers besucht. Diese Berichte zeigen Ihnen die häufigsten Pfade, die durch Ihre Website genommen werden.

**Vorheriger Fluss**

Die Berichte „Vorheriger Fluss“ sind den Berichten „Nächster Fluss“ ähnlich; allerdings zeigen sie in diesem Fall nicht an, wohin der Besucher nach der jeweiligen Seite navigierte, sondern woher der Besucher kam. Die Steuerelemente für die Verwendung des Berichts sind identisch mit den Steuerelementen für die Berichte „Nächster Fluss“.

## Nächster Seitenfluss {#concept_F7565234927942BEAF75D5D94A7AB47D}

Zeigt Pfadanzeigen oder die Anzahl der Male sowie Prozentzahlen an, die eine Seite innerhalb der Pfad-Einschränkungen angezeigt wurde. So kann die Seite der Datenschutzregeln z. B. insgesamt 10.000 Mal angezeigt worden sein, aber nur 500 dieser Seitenansichten erfolgten unmittelbar vor der Homepage. In diesem Fall würden Sie 500 Pfadanzeigen sehen. Sie können diesen Bericht auf Besuchs- oder Besucherebene anzeigen. Prozentwerte zur jeweiligen Seite stehen neben dem Seitennamen. Die Breite einer mit einer Seite verbundenen Zeile bildet den relativen Besuchsprozentsatz ab.

<!-- 

c_reports_next_page_flow.xml

 -->

Der Bericht zeigt in der Standardeinstellung die 10 am häufigsten aufgerufenen Seiten nach der von Ihnen gewählten Seite. Sie können jede unterstrichene Seite anklicken, um das Diagramm zu erweitern. Die Zahl der Seiten, die Sie einbeziehen können, ist nicht beschränkt. Zudem können Sie auf einer Seite verweilen, um Besuchs- und Umsatzdaten der Seite anzusehen.

Verwenden Sie diesen Bericht, um:

* zu erkennen, welche Schritte am häufigsten nach Ansicht der gewählten Seite ausgeführt werden.
* Ihren Site-Pfadentwurf zu optimieren, um mehr Traffic auf die gewünschte Zielseite zu lenken.
* zu identifizieren, welche Seiten statt der gewünschten Zielseiten die Besucher aufrufen.

## Nächster Serverfluss {#concept_DB8C20E18AEA4051903C47A16C0E9C4E}

Zeigt die Navigationsdaten zwischen Servern auf Ihrer Site an. Wenn Sie einen Servernamen aus Ihrer Site auswählen, zeigt der Bericht die Anzahl der Besucher an, die während eines Besuchs oder über mehrere Besuche über diesen Server zu den jeweiligen anderen Servern navigiert sind.

<!-- 

c_reports_next_server_flow.xml

 -->

Falls Sie beispielsweise über bestimmte Daten auf verschiedenen Servern verfügen oder Daten auf separaten Servern gespiegelt haben, zeigt der Bericht den Pfad zwischen den Servern an, dem die Benutzer gefolgt sind. Dies gilt auch für Domänen auf Ihrer Website. Sie können beispielsweise sehen, wie viele Benutzer von `https://www.mysite.com` zu `https://info.mysite.com` oder `https://sales.mysite.com` gelangt sind.

## Nächster Abschnittsfluss {#concept_7C9C8567E7DF477DA186E47DD3FD47A4}

Der Bericht [!UICONTROL Nächster Abschnittsfluss] ähnelt dem Bericht [!UICONTROL Nächster Seitenfluss]. Er zeigt Daten für Sitebereiche (Gruppen miteinander in Beziehung stehender Webseiten) an. Falls eine Seite in mehr als einem Sitebereich enthalten ist, zeigt der Bericht Daten für alle Sitebereiche an.

<!-- 

c_reports_next_section_flow.xml

 -->

Ein Online-Händler hat beispielsweise Sitebereiche für seine Produkte und für Produktmarken eingerichtet. In diesem Fall kann eine Produkt-Webseite unter mehrere Sitebereiche fallen. Obwohl eine Produktseite nur einmal angezeigt wurde, zeigt der Bericht [!UICONTROL Nächster Abschnittsfluss] eine Seitenansicht für jeden Sitebereich, der mit der Seite verbunden ist.

## Vorheriger Seitenfluss {#concept_ADEAEBAE3F37401B977A27E03B5A523B}

Ähnlich dem Bericht [!UICONTROL Nächster Seitenfluss]. Der Bericht [!UICONTROL Vorheriger Seitenfluss] zeigt mehrere Stufen der bevorzugten Seiten an, die Besucher vor der gewählten Seite aufrufen. Der Bericht hebt auch die Seiten hervor, von denen die Besucher zu Ihrer Site kamen.

<!-- 

c_reports_previous_page_flow.xml

 -->

Verwenden Sie diesen Bericht, um:

* Einblick in die Schritte zu erhalten, die am häufigsten vor Ansicht der gewählten Seite ausgeführt werden.
* Ihren Site-Pfadentwurf zu optimieren, um mehr Traffic auf die gewünschte Zielseite zu lenken.

## Vorheriger Abschnittsfluss {#concept_30688D97B48449E1958866BAF376FA8C}

Der Bericht [!UICONTROL Vorheriger Abschnittsfluss] ähnelt dem Bericht [!UICONTROL Vorheriger Seitenfluss]. Er zeigt Daten für Sitebereiche (Gruppen miteinander in Beziehung stehender Webseiten) an. Falls eine Seite in mehr als einem Sitebereich enthalten ist, zeigt der Bericht Daten für alle Sitebereiche an.

<!-- 

c_reports_previous_section_flow.xml

 -->

Ein Online-Händler hat beispielsweise Sitebereiche für seine Produkte und für Produktmarken eingerichtet. In diesem Fall kann eine Produkt-Webseite unter mehrere Sitebereiche fallen. Obwohl eine Produktseite nur einmal angezeigt wurde, zeigt der Bericht [!UICONTROL Vorheriger Abschnittsfluss] eine Seitenansicht für jeden Website-Abschnitt, der mit der Seite verbunden ist.

## Vorheriger Serverfluss {#concept_8E43208CAF2C4C358F19D4669B73822F}

Dieser Bericht zeigt die Navigationsdaten zwischen Servern auf Ihrer Site an. Wenn Sie einen Servernamen aus Ihrer Site auswählen, zeigt der Bericht die Anzahl der Besucher an, die während eines Besuchs oder über mehrere Besuche von den anderen zu diesem Server navigiert sind.

<!-- 

c_reports_previous_server_flow.xml

 -->

Falls Sie beispielsweise über bestimmte Daten auf verschiedenen Servern verfügen oder Daten auf separaten Servern gespiegelt haben, zeigt der Bericht den Pfad zwischen den Servern an, dem die Benutzer gefolgt sind. Dies gilt auch für Domänen auf Ihrer Website. Sie können beispielsweise sehen, wie viele Benutzer von `www.mysite.com` zu `info.mysite.com` oder `sales.mysite.com` gelangt sind.

## Konversionstrichterberichte {#concept_35A2EB61E84441CBB670C2E02CA26F81}

Konversionstrichterberichte zeigen Konversionsprozentsätze zwischen spezifischen Metrikereignissen an. Sie können diesen Bericht nutzen, um sich einen Überblick über die Clickthroughs, die zu Verkäufen geführt haben, sowie über die Anzahl verkaufter Einheiten zu verschaffen. Ein [!UICONTROL Produktkonversionsbericht] beispielsweise zeigt den Prozentsatz von Einkaufswagen-Ereignissen im Verhältnis zu Besuchsereignissen und dann die Gesamtzahlen zu Bestellungen, Umsatz und Einheiten auf Grundlage dieser Ereignisse.

<!-- 

c_reports_conversion_funnel.xml

 -->

Die folgenden Trichterberichte stehen zur Verfügung:

* [!UICONTROL Einkaufskonversionstrichter]: Zeigt Besuche (berichtspezifisch), Warenkorb, Bestellungen, Einheiten und Umsatz an.
* [!UICONTROL Warenkorbkonversionstrichter]: Zeigt Besuche (berichtspezifisch), Warenkorb, Checkouts, Bestellungen und Umsatz an.
* [!UICONTROL Benutzerspezifischer Ereignistrichter]: Zeigt benutzerspezifische Ereignisse auf Ihrer Site an. Standardmäßig werden die benutzerspezifischen Ereignisse 1-5 angezeigt.
* [!UICONTROL Kampagnen-Konversionstrichter]: Zeigt Clickthroughs, Kassengänge, Bestellungen und Umsatz an.

Die Berichtstabelle zeigt Statistiken zu durchschnittlichen Verkäufen pro Clickthrough-Rate und durchschnittlich verkauften Einheiten pro Clickthrough-Rate an. Sie können zu diesen Berichten Metriken und benutzerspezifische Ereignisse aus anderen Berichtgruppen hinzufügen. Diese Trichter haben viele Ähnlichkeiten, basieren aber auf verschiedenen Variablen und Ereignissen. Sie können diese Berichte nutzen, um zu prüfen, welche Prozentsätze und allgemeine Besuchertrends von Ihnen spezifizierte Ereignisse auslösen. Sie können sehen, wo Benutzer nicht bis zu bestimmen Ereignissen folgen und erhalten so umfassende Informationen zu diesem spezifischen Punkt im Konversionsprozess.

## Bericht „Site-Analyse“ {#concept_65694C6BDE424714B7975764F95497A4}

In der [!UICONTROL Site-Analyse] können Sie sehen, wie Besucher festgelegte Seiten und Ereignisse durchlaufen. Sie können beispielsweise den Traffic-Fluss zwischen Seiten, die Affinität zwischen Produkten und Marketingkanälen und den Fluss zwischen Kampagnen/Kanälen und Produktbestellungen beobachten. Sie können Seiten, Dimensionselemente (und Listen) sowie Metrikereignisse hineinziehen. Jede Säule steht für eines oder mehrere Dimensionselemente (Seiten) oder ein Ereignis. Pfeile stehen für den Fluss zwischen den Säulenwerten. Metriken sind den Säulenpositionen (X und Y), der Säulenbreite, Säulenhöhe und -farbe zugeordnet. Die Position, Größe und Farben ändern sich abhängig von den Metrikwerten.

<!-- 

c_reports_site_analysis.xml

 -->

Ziehen Sie Elemente aus Tool-Bereichen, um sie zum Diagramm- oder Dimensionsfeld hinzuzufügen.

Klicken Sie mit der rechten Maustaste auf Säulen, um sie zu bearbeiten oder zu entfernen.

<!-- Meike, UICONTROL and DNL stripped from tables. Re-add. -->

| Option | Beschreibung |
|--- |--- |
| Site-Analyse anzeigen bei (Besuch oder Besucher) | Hiermit können Sie bei der Analyse der Besucherpfade zwischen Besuch und Besucher wechseln. Diese Einstellungen helfen Ihnen, die Besucher-Interaktion auf Besucherebene und besuchsübergreifend zu verstehen. Site-Analyse-, Fluss- und Fallout-Berichte sind für die Besucherpfadermittlung aktiviert. Durch Änderung dieser Einstellung wird der Bericht erneut ausgeführt, wobei die Daten auf die Auswahl beschränkt sind. |
| Checkpoint hinzufügen | Ruft den Checkpoint-Editor auf, über den Sie Dimensionen oder Ereignisse auswählen und zur Anzeige hinzufügen können. |
| Diagramm ersetzen | Ersetzt das Site-Analyse-Diagramm durch die Checkpoints, die Sie zum Editor hinzugefügt haben. |
| Bildschirmgröße | Stellt die Ursprungsansicht eines Diagramms wieder her. |
| Von oben gesehen | Bietet einen Top-Down-Überblick auf das Diagramm. |
| Raster wechseln | Schaltet das Raster ein oder aus. |
| Dimension | Das Element, zu dem Sie einen Bericht erstellen. Das Element aus Dimensionen ziehen. |

| Option | Beschreibung |
|--- |--- |
| Vorlage | Hiermit können Sie Seiten zu einer Säule hinzufügen oder daraus entfernen. |
| Entfernen | Hiermit können Sie eine Säule entfernen. |
| Berichte | Hiermit können Sie einen anderen Bericht über die Säule starten. |
| Diagramm speichern unter | Hiermit können Sie das Diagramm als .png- oder .jpg-Datei speichern. Wenn Sie die Diagrammsteuerungen (Diagrammwinkel, Größe) vor dem Speichern ändern, bleiben die Änderungen in der Ausgabe erhalten. |
| Diagramm in Zwischenablage kopieren | Kopiert das Diagramm, um es in anderen Anwendungen einfügen zu können. Wenn Sie die Diagrammsteuerungen (Diagrammwinkel, Größe) vor dem Speichern ändern, bleiben die Änderungen in der Ausgabe erhalten. |
