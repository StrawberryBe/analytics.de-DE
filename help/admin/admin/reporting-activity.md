---
description: Erfahren Sie, wie Sie Kapazitätsprobleme bei Spitzen während der Berichterstellung mit Reporting Activity Manager diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
mini-toc-levels: 3
exl-id: f638c6a9-1c2c-4936-a787-281269f95afc
source-git-commit: e7346b11a7d3eb4c18ec02df6c8a07574e02a2b4
workflow-type: ht
source-wordcount: '962'
ht-degree: 100%

---

# Reporting Activity Manager

>[!NOTE]
>
>Diese Funktion wird derzeit in Beta-Tests überprüft.

[!UICONTROL Reporting Activity Manager] zeigt die Berichtskapazität für jede Report Suite in Ihrer Organisation an. Admins erhalten detaillierte Einblicke in die Berichtsnutzung und können mühelos Kapazitätsprobleme bei Spitzen während der Berichterstellung diagnostizieren und beheben.

Wenn Ihre Organisation die Berichtsanforderungskapazität erreicht und sich die Berichtsleistung verschlechtert, können Sie jetzt Reporting-Probleme selber einer Diagnose unterziehen, ohne dass hierzu die Kundenunterstützung oder das Technik-Team von Adobe eingereifen muss. Sie können Berichtswarteschlangen einfach in einer einzigen Oberfläche verwalten und sofort handeln, um das Benutzererlebnis zu verbessern. Dieses Tool:

* Informiert Sie in Echtzeit über Ihre aktuelle Berichtskapazitäten in all Ihren Report Suites.
* Enthält detaillierte Berichtsabfrageinformationen zu aktuellen Berichtsanfragen, unabhängig davon, ob diese sich in der Warteschlange befinden oder in Bearbeitung sind.
* Ermöglicht Ihnen die Optimierung der Berichtswarteschlange durch Priorisierung einiger Berichtsanfragen und Abbruch von anderen, um Kapazitäten freizugeben. Anders ausgedrückt: Sie können in Echtzeit fragen, ob dieser Bericht zu diesem Zeitpunkt notwendig ist oder zugunsten dringenderer Berichte abgebrochen werden kann.

## Zugriff auf Reporting Activity Manager

In Adobe Analytics navigieren Admins zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

## Zugriffsberechtigung

Sie benötigen die Berechtigung eines Analytics-Produktadministrators bzw. einer Analytics-Produktadministratorin (in der Adobe Admin Console), um die Berichterstellungsaktivität zu verwalten.

Berechtigung ![](/help/admin/admin/assets/rep-mgr-permission.png)

## Anzeigen der Berichtswarteschlange

Beim Öffnen der [!UICONTROL Reporting Activity Manager]-Übersichtsseite wird eine Liste Ihrer aktivierten zugrunde liegenden Report Suites angezeigt.

![Berichtswarteschlange](/help/admin/admin/assets/reporting-activity1.png)

| UI-Element | Beschreibung |
| --- | --- |
| **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite, deren Berichtsaktivität von Ihnen überwacht wird. |
| **[!UICONTROL Virtual Report Suite]** | Zeigt alle Virtual Report Suites an, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites ermöglichen eine höhere Komplexität von Berichtsanfragen aufgrund zusätzlich anwendbarer Filter- und Segmentierungsebenen. Alle Anfragen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite.<p>Beispielsweise ergeben 10 Anfragen, die von 5 Virtual Report Suites kommen, 50 Anfragen auf Seiten der zugrunde liegenden Report Suite. Auf diese Weise können Sie sehr schnell die Kapazitätsgrenzen erreichen. |
| **[!UICONTROL Nutzungskapazität]** | Prozentualer Anteil, wie viel der Berichterstellungskapazität der Report Suite in Echtzeit verwendet wird. |
| **[!UICONTROL Status]** | Vier mögliche Statusindikatoren: <ul><li>**Rot – [!UICONTROL Kapazitätsgrenze erreicht]**: Die Report Suite wird in Bezug auf die Berichtskapazität maximal genutzt. (100 %) </li><li>**Gelb – [!UICONTROL Nah an der Kapazitätsgrenze]**: Diese Report Suite läuft Gefahr, ihre maximale Kapazität zu erreichen. (90 % - 99 %)</li><li>**Grün – [!UICONTROL Alles in Ordnung]**: Es ist genügend Berichtskapazität vorhanden. (0 % - 89 %)</li><li>**Grau – [!UICONTROL Status ausstehend/Nicht aktiviert]**: Es ist keine Berichtskapazität verfügbar.</li></ul> |

{style=&quot;table-layout:auto&quot;}

### Andere Berichtsaktivitätsaktionen

* Klicken Sie oben rechts auf **[!UICONTROL Aktualisieren]**, um die Ergebnisse zu aktualisieren.
* Klicken Sie auf den Stern links neben dem Namen der Report Suite, um diese Report Suite als Favoriten zu kennzeichnen.
* Aktivieren Sie oben links **[!UICONTROL Favoriten]**, um Ihre Favoriten anzuzeigen.
* Suchen Sie in der Suchleiste nach Report Suites nach Name oder ID.
* Filtern Sie Report Suites nach ihrem Status.

## Anzeigen der Berichtsaktivität für einzelne Report Suites

Klicken Sie auf den Titel-Link einer Report Suite, für die Sie Details anzeigen möchten.

![Report Suite](/help/admin/admin/assets/indiv-report-ste.png)

### Liniendiagramm

Das Liniendiagramm zeigt die Berichtsaktivität für die ausgewählte Report Suite in den letzten zwei Stunden an.

* Die X-Achse zeigt die Berichtskapazitätsdaten der letzten zwei Stunden an.
* Die Y-Achse zeigt die durchschnittliche Wartezeit für eine Abfrage in Sekunden an.
* Sie können den Mauszeiger über das Liniendiagramm bewegen, um Zeitpunkte und die durchschnittliche Wartezeit für einen bestimmten Zeitpunkt anzuzeigen.

   ![Detail](/help/admin/admin/assets/detail.png)

### Filter

Sie können die Tabelle nach Programm (siehe Liste in der Tabelle unten), nach Benutzer und nach Projekt filtern.

![Filter](/help/admin/admin/assets/filter.png)

### Zusammenfassungszahlen

![Filter](/help/admin/admin/assets/summary_numbers.png)

Die Zusammenfassungszahlen geben die folgenden Informationen an:

| Zusammenfassungszahl | Beschreibung |
| --- | --- |
| [!UICONTROL Benutzer] | Die Anzahl der Benutzenden, die zurzeit Reporting-Anfragen an diese Report Suite senden. |
| [!UICONTROL Projekte] | Workspace-Projekte, Report Builder-Arbeitsmappen usw. |
| [!UICONTROL Abfragen] | Die Anzahl der derzeit laufenden Abfragen. |
| [!UICONTROL Durchschnittliche Wartezeit] | Die durchschnittliche Wartezeit für alle laufenden Abfragen. |
| [!UICONTROL Nutzungskapazität] | Die aktuelle Nutzungskapazität für diese Report Suite. |

{style=&quot;table-layout:auto&quot;}

### Tabelle

Die nachstehende detaillierte Tabelle zeigt Details zur Report Suite.

| Spalte | Beschreibung |
| --- | --- |
| [!UICONTROL Abfrage-ID] | Kann zur Fehlerbehebung verwendet werden. |
| [!UICONTROL Ausführungszeit] | Die Dauer der Abfrage. |
| [!UICONTROL Wartezeit] | Die Wartezeit für die Abfrage vor ihrer Verarbeitung. im Allgemeinen bei „0“, wenn genügend Kapazität vorhanden ist. |
| [!UICONTROL Startzeit] | Der Zeitpunkt, zu dem die Verarbeitung der Abfrage begonnen hat (Ortszeit des Admins). |
| [!UICONTROL Programm] | Die von [!UICONTROL Reporting Activity Manager] unterstützten Programme sind: <ul><li>Analysis Workspace-Benutzeroberfläche</li><li>Geplante Projekte im Workspace</li><li>Report Builder</li><li>Builder-Benutzeroberflächen: Segment, berechnete Metriken, Anmerkungen, Audiences usw.</li><li>API-Aufrufe aus der API 1.4 oder 2.0</li><li>Intelligente Warnhinweise</li></ul> |
| [!UICONTROL Benutzer] | Der Benutzer, der die Abfrage initiiert hat. |
| [!UICONTROL Projekt] | Gespeicherte Workspace-Projektnamen, API-Berichts-IDs usw. (Metadaten können von Programm zu Programm variieren.) |
| [!UICONTROL Monatsgrenzen] | Wie viele Monatsgrenzen eine Anfrage überschreitet. Dies erhöht die Komplexität der Anfrage. |
| [!UICONTROL Spalten] | Die Anzahl der Metriken und Aufschlüsselungen in Workspace, um die Komplexität der Anfrage abzuschätzen. |
| [!UICONTROL Segmente] | Wie viele Segmente auf diese Anfrage angewendet werden. Dies erhöht die Komplexität der Anfrage. |
| [!UICONTROL Status] | Statusindikatoren: <ul><li>**Läuft**: Die Anfrage wird derzeit verarbeitet.</li><li>**Ausstehend**: Die Anfrage wartet auf die Verarbeitung.</li></ul> |

{style=&quot;table-layout:auto&quot;}

## Abbrechen von Berichtsanfragen

So brechen Sie eine Anfrage ab:

1. Aktivieren Sie das Kontrollkästchen links neben einer oder mehreren **[!UICONTROL Abfrage-IDs]** in der Tabelle und klicken Sie unten auf **[!UICONTROL Anfragen abbrechen]**.

   Sie können Anfragen auch stapelweise abbrechen, indem Sie Details nach [!UICONTROL Benutzer], [!UICONTROL Projekt] oder [!UICONTROL Anwendung] anzeigen. Nachfolgende Anfragen für ein Projekt, einen Benutzer oder eine Anwendung, die sich zum Zeitpunkt des Abbruchs nicht in der Warteschlange befanden oder nicht ausgeführt wurden, könnten weiterhin angezeigt werden, wenn die Aktivität aktualisiert wird.

1. Im Fenster **[!UICONTROL X-Abfrage abbrechen]** können Sie bei Bedarf die Abbruchsmeldung ändern.
1. Klicken Sie auf **[!UICONTROL Weiter]**.

   ![cancel-query](/help/admin/admin/assets/cancel-query.png)

Programmbenutzern in Workspace wird beispielsweise in ihren Projekten der folgende Hinweis angezeigt:

![cancel-user-notice](/help/admin/admin/assets/cancel-user-facing.png)

## Häufig gestellte Fragen

| Frage | Antwort |
| --- | --- |
| Kann ich zusätzliche Berichtskapazitäten erwerben? | Diese Funktion wird demnächst verfügbar sein. |

{style=&quot;table-layout:auto&quot;}
