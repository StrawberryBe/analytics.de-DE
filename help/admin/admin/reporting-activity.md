---
description: Erfahren Sie, wie Sie mit dem Reporting Activity Manager Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
mini-toc-levels: 3
hide: true
hidefromtoc: true
source-git-commit: 123a2131be1a3cb23246e2ba591be645c7025b26
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 7%

---


# Reporting Activity Manager

>[!NOTE]
>
>Diese Funktion befindet sich derzeit im Beta-Test.

Mit dem Reporting Activity Manager können Sie die Berichtskapazität für jede Report Suite in Ihrer Organisation anzeigen. Als Administrator erhalten Sie detaillierte Einblicke in den Berichtsverbrauch und können mühelos Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben. Wenn Ihr Unternehmen die Berichtsanforderungskapazität erreicht und die Berichtsleistung verschlechtert wird, können Sie jetzt Reporting-Probleme selbstdiagnostizieren, ohne dass dies vom Kundendienst oder vom Techniker der Adobe vorgenommen wird. Sie können einfach Berichtwarteschlangen in einer einzigen Oberfläche verwalten und sofort &#x200B; handeln, um das Benutzererlebnis zu verbessern. Dieses Tool:

* Informiert Sie über Ihre aktuelle Berichtskapazität in all Ihren Report Suites.
* Enthält detaillierte Berichtabfrageinformationen zu aktuellen Berichtsanforderungen, unabhängig davon, ob sie sich in der Warteschlange befinden oder in Bearbeitung sind.
* Ermöglicht Ihnen die Optimierung der Berichtswarteschlange durch Priorisierung einiger Anforderungen und Abbruch anderer Berichtsanforderungen, um die Kapazität freizugeben. Mit anderen Worten: Sie können in Echtzeit fragen: Ist dieser Bericht zu diesem Zeitpunkt notwendig oder kann ich ihn zugunsten dringender Berichte ablehnen?

## Zugriff auf den Reporting Activity Manager

In Adobe Analytics navigieren Administratoren zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

## Berichtwarteschlange anzeigen

Beim Öffnen der Übersichtsseite &quot;Reporting Activity Manager&quot;wird eine Liste Ihrer aktivierten Basis-Report Suites angezeigt.

![Berichtwarteschlange](assets/reporting-activity1.png)

| UI-Element | Beschreibung |
| --- | --- |
| **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite, deren Berichtsaktivität Sie überwachen. |
| **[!UICONTROL Virtual Report Suite]** | Zeigt alle Virtual Report Suites an, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites bieten Berichtsanforderungen aufgrund zusätzlicher angewendeter Filter- und Segmentierungsebenen zusätzliche Komplexität. Alle Anforderungen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite.<p>Wenn Sie z. B. 10 Anforderungen von 5 VRSs haben, sind das 50 Anforderungen auf Basis-Report Suite. Auf diese Weise können Sie die Kapazität sehr schnell erreichen. |
| **[!UICONTROL Nutzungskapazität]** | Prozentualer Anteil, wie viel der Berichterstellungskapazität der Report Suite in Echtzeit verwendet wird. |
| **[!UICONTROL Status]** | Vier mögliche Statusindikatoren: <ul><li>**Rot - [!UICONTROL Kapazität]**: Die Report Suite wird in Bezug auf die Berichtskapazität festgelegt.</li><li>**Gelb - [!UICONTROL Anbaufähige Kapazität]**: Diese Report Suite läuft Gefahr, ihre maximale Kapazität zu erreichen.</li><li>**Green - [!UICONTROL Alles Gute]**: Die Berichtskapazität ist reichlich.</li><li>**[!UICONTROL Status ausstehend]**: ?</li><li>**Grau - nicht verfügbar**: Die Report Suite ist nicht für die Berichtskapazität konfiguriert.</li></ul> |

### Andere Aktionen der Berichtsaktivität

* Klicken **[!UICONTROL Aktualisieren]** oben rechts, um die Ergebnisse zu aktualisieren.
* Klicken Sie auf den Stern links neben dem Report Suite-Namen, um diese Report Suite als Favoriten zu kennzeichnen.
* Überprüfen **[!UICONTROL Favoriten]** oben links, um Ihre Favoriten anzuzeigen.
* Suchen Sie in der Suchleiste nach Report Suites nach Name oder Kennung.
* Filtern von Report Suites nach ihrem Status.

## Berichtsaktivität für einzelne Report Suites anzeigen

Klicken Sie auf den Titel-Link einer Report Suite, für die Sie Details anzeigen möchten.

![Report Suite](assets/indiv-report-ste.png)

### Kantengraph

Das Liniendiagramm zeigt die Berichtsaktivität für die ausgewählte Report Suite in den letzten 2 Stunden an.

* Die X-Achse zeigt die Daten zur Berichtskapazität über die letzten 2 Stunden an.
* Die Y-Achse zeigt die durchschnittliche Wartezeit für eine Abfrage in Sekunden an.
* Sie können den Mauszeiger über das Liniendiagramm bewegen, um die Zeitpunkte und die durchschnittliche Wartezeit für diesen Zeitpunkt anzuzeigen.

   ![detail](assets/detail.png)

### Filter

Sie können die Tabelle nach Anwendung (siehe Liste in der Tabelle unten), nach Benutzer und nach Projekt filtern.

![Filter](assets/filter.png)

### Zusammenfassungsnummern

![Filter](assets/summary_numbers.png)

Die Zusammenfassungsnummern zeigen die folgenden Informationen an:

| Zusammenfassungszahl | Beschreibung |
| --- | --- |
| Benutzer | Wie viele Benutzer derzeit Reporting-Anforderungen an diese Report Suite senden. |
| Projekte |  |
| Abfragen |  |
| Durchschnittliche Wartezeit |  |
| Nutzungskapazität | Die aktuelle Nutzungskapazität für diese Report Suite. |

{style=&quot;table-layout:auto&quot;}

### Tabelle

Die nachstehende detaillierte Tabelle zeigt

| Spalte | Beschreibung |
| --- | --- |
| Abfrage-ID |  |
| Ausführungszeit |  |
| Wartezeit |  |
| Startzeit |  |
| Anwendung | Die vom Reporting Activity Manager unterstützten Anwendungen sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Arbeitsbereich</li><li>Report Builder</li><li>Builder-Benutzeroberfläche: Segment, berechnete Metriken, Anmerkungen, Zielgruppen usw.</li></ul> |
| Benutzer |  |
| Projekt |  |
| Monatsgrenzen |
| Spalten |  |
| Segmente |  |
| Status |  |

{style=&quot;table-layout:auto&quot;}


