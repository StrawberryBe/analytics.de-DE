---
description: Erfahren Sie, wie Sie mit dem Reporting Activity Manager Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: 7421b2eb2b8b00824de2910e37882c83d2d6f3e9
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 7%

---

# Reporting Activity Manager

>[!NOTE]
>
>Diese Funktion befindet sich derzeit im Beta-Test.

Die [!UICONTROL Reporting Activity Manager] zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an. Als Administrator erhalten Sie detaillierte Einblicke in den Berichtsverbrauch und können mühelos Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben.

Wenn Ihr Unternehmen die Berichtsanforderungskapazität erreicht und die Berichtsleistung verschlechtert wird, können Sie jetzt Reporting-Probleme selbstdiagnostizieren, ohne dass dies vom Kundendienst oder vom Techniker der Adobe vorgenommen wird. Sie können einfach Berichtwarteschlangen in einer einzigen Oberfläche verwalten und sofort &#x200B; handeln, um das Benutzererlebnis zu verbessern. Dieses Tool:

* Informiert Sie in Echtzeit über Ihre aktuelle Berichtskapazität in all Ihren Report Suites.
* Enthält detaillierte Berichtabfrageinformationen zu aktuellen Berichtsanforderungen, unabhängig davon, ob sie sich in der Warteschlange befinden oder in Bearbeitung sind.
* Ermöglicht Ihnen die Optimierung der Berichtswarteschlange durch Priorisierung einiger Anforderungen und Abbruch anderer Berichtsanforderungen, um die Kapazität freizugeben. Mit anderen Worten: Sie können in Echtzeit fragen: Ist dieser Bericht zu diesem Zeitpunkt notwendig oder kann ich ihn zugunsten dringender Berichte ablehnen?

## Zugriff auf den Reporting Activity Manager

In Adobe Analytics navigieren Administratoren zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

## Zugriffsberechtigungen

Sie benötigen die Berechtigung für Analytics-Produkt-Administrator (in Adobe Admin Console), um die Berichterstellungsaktivität zu verwalten.

Berechtigung ![](assets/rep-mgr-permission.png)

## Berichtwarteschlange anzeigen

Beim Öffnen der [!UICONTROL Berichtsaktivität] Manager-Übersichtsseite angezeigt, sehen Sie eine Liste Ihrer aktivierten Basis-Report Suites.

![Berichtwarteschlange](assets/reporting-activity1.png)

| UI-Element | Beschreibung |
| --- | --- |
| **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite, deren Berichtsaktivität Sie überwachen. |
| **[!UICONTROL Virtual Report Suite]** | Zeigt alle Virtual Report Suites an, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites bieten Berichtsanforderungen aufgrund zusätzlicher angewendeter Filter- und Segmentierungsebenen zusätzliche Komplexität. Alle Anforderungen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite.<p>Wenn Sie z. B. 10 Anforderungen von 5 VRSs haben, sind das 50 Anforderungen auf Basis-Report Suite. Auf diese Weise können Sie die Kapazität sehr schnell erreichen. |
| **[!UICONTROL Nutzungskapazität]** | Prozentualer Anteil, wie viel der Berichterstellungskapazität der Report Suite in Echtzeit verwendet wird. |
| **[!UICONTROL Status]** | Vier mögliche Statusindikatoren: <ul><li>**Rot - [!UICONTROL Kapazität]**: Die Report Suite wird in Bezug auf die Berichtskapazität festgelegt. (100%) </li><li>**Gelb - [!UICONTROL Anbaufähige Kapazität]**: Diese Report Suite läuft Gefahr, ihre maximale Kapazität zu erreichen. (90% - 99%)</li><li>**Green - [!UICONTROL Alles Gute]**: Die Berichtskapazität ist reichlich. (0% - 89%)</li><li>**Grau - [!UICONTROL Status ausstehend/Nicht aktiviert]**: Berichtskapazität nicht verfügbar.</li></ul> |

{style=&quot;table-layout:auto&quot;}

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
| [!UICONTROL Benutzer] | Wie viele Benutzer derzeit Reporting-Anforderungen an diese Report Suite senden. |
| [!UICONTROL Projekte] | Workspace-Projekte, Report Builder-Arbeitsmappen usw. |
| [!UICONTROL Abfragen] | Die Anzahl der derzeit ausgeführten Abfragen. |
| [!UICONTROL Durchschnittliche Wartezeit] | Die durchschnittliche Wartezeit für alle ausgeführten Abfragen. |
| [!UICONTROL Nutzungskapazität] | Die aktuelle Nutzungskapazität für diese Report Suite. |

{style=&quot;table-layout:auto&quot;}

### Tabelle

Die nachstehende detaillierte Tabelle zeigt Details zur Report Suite.

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL Abfrage-ID] | Kann zur Fehlerbehebung verwendet werden. |
| [!UICONTROL Ausführungszeit] | Dauer der Abfrage. |
| [!UICONTROL Wartezeit] | Dauer der Verarbeitung der Abfrage. Im Allgemeinen bei &quot;0&quot;, wenn genügend Kapazität vorhanden ist. |
| [!UICONTROL Startzeit] | Der Zeitpunkt, zu dem die Verarbeitung der Abfrage begonnen hat (Ortszeit des Administrators). |
| [!UICONTROL Anwendung] | Die von der [!UICONTROL Reporting Activity Manager] sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Arbeitsbereich</li><li>Report Builder</li><li>Builder-Benutzeroberfläche: Segment, berechnete Metriken, Anmerkungen, Zielgruppen usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Intelligente Warnhinweise</li></ul> |
| [!UICONTROL Benutzer] | Der Benutzer, der die Abfrage initiiert hat. |
| [!UICONTROL Projekt ] | Workspace-Projektnamen, API-Bericht-IDs usw. gespeichert. (Metadaten können von Anwendung zu Anwendung variieren.) |
| [!UICONTROL Monatsgrenzen] | Wie viele Monatsgrenzen eine Anforderung überschreitet. Dies erhöht die Komplexität der Anfrage. |
| [!UICONTROL Spalten] | Die Anzahl der Metriken und Aufschlüsselungen in Workspace, um die Komplexität der Anforderung abzuschätzen. |
| [!UICONTROL Segmente] | Wie viele Segmente auf diese Anforderung angewendet werden. Dies erhöht die Komplexität der Anfrage. |
| [!UICONTROL Status] | Statusindikatoren: <ul><li>**Läuft**: Die Anfrage wird derzeit verarbeitet.</li><li>**Ausstehend**: Die Anfrage wartet auf die Verarbeitung.</li></ul> |

{style=&quot;table-layout:auto&quot;}

## Berichtsanforderungen abbrechen

So brechen Sie eine Anforderung ab

1. Aktivieren Sie das Kontrollkästchen links neben einem oder mehreren **[!UICONTROL Abfrage-ID]** in der Tabelle und klicken Sie auf **[!UICONTROL Anforderungen abbrechen]** unten. (Sie können Anforderungen auch stapelweise abbrechen, indem Sie Details anzeigen durch [!UICONTROL Benutzer], [!UICONTROL Projekt]oder [!UICONTROL Anwendung].
1. Im **[!UICONTROL Abbrechen der X-Abfrage]** angezeigt wird, können Sie bei Bedarf die Abbruchsnachricht ändern.
1. Klicken Sie auf **[!UICONTROL Weiter]**.

   ![cancel-query](assets/cancel-query.png)

Anwendungsbenutzer in Workspace sehen beispielsweise in ihren Projekten den folgenden Hinweis:

![cancel-user-notification](assets/cancel-user-facing.png)

## Häufig gestellte Fragen

| Frage | Antwort |
| --- | --- |
| Kann ich zusätzliche Berichtskapazitäten erwerben? | Diese Funktion wird demnächst verfügbar sein. |

{style=&quot;table-layout:auto&quot;}
