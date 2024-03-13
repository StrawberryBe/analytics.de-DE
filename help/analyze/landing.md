---
description: Erläutert die neue Landingpage, die Analysis Workspace und Reports & Analytics in einer Benutzeroberfläche zusammenfasst und so einen zentralen Zugriffspunkt (Workspace) bietet.
title: Neue Landingpage von Adobe Analytics
role: User, Admin
feature: Analytics Basics
exl-id: 0a2fb778-491a-4dc3-aae4-afadb3ab1a1e
source-git-commit: a75c807c1f54676e359cf502781ba1de5fd6c51c
workflow-type: tm+mt
source-wordcount: '1803'
ht-degree: 90%

---

# Neue Landingpage von Adobe Analytics

Die Landingpage für Adobe Analytics vereint sowohl [!DNL Analysis Workspace] als auch [!DNL Reports & Analytics] (eingestellt) in einer einzigen Oberfläche und einem Zugangspunkt unter dem Dach von [!DNL Workspace]. Sie enthält eine neue Startseite für den Projekt-Manager, ein aktualisiertes Berichtsmenü und aktualisierte Berichte sowie einen Lernbereich, der Ihnen dabei hilft, die ersten Schritte effektiver zu bewältigen. Hier finden Sie eine Videoübersicht:

>[!VIDEO](https://video.tv.adobe.com/v/334278/?quality=12)

Die Adobe Analytics-Landingpage besteht aus den folgenden Unterregisterkarten: Projekte, Berichte und Lernen.

**[!UICONTROL Projekte]** sind benutzerdefinierte Entwürfe, die aus Datenkomponenten, Tabellen und Visualisierungen bestehen, die von Ihnen erstellt oder einer anderen Person für Sie erstellt und freigegeben wurden. [!UICONTROL Projekte] beziehen sich auch auf leere Projekte und leere mobile Scorecards.

**[!UICONTROL Berichte]** beziehen sich auf alles, was von Adobe vorkonfiguriert wurde, z. B. Vorlagen in Workspace.

Die **[!UICONTROL Lernen]** enthält praktische Videoführungen, Tutorials und Links zur Dokumentation.

## Navigieren Sie zur Registerkarte [!UICONTROL Projekte] {#navigate-projects}

Die [!UICONTROL Projekte] Registerkarte dient als [!UICONTROL Arbeitsbereich] Homepage. Es zeigt den Ordner Unternehmen, alle von Ihnen erstellten persönlichen Ordner, Ihre Projekte und mobile Scorecards an. Auf dieser Seite können Sie Ordner, Projekte und mobile Scorecards anzeigen, erstellen und ändern. Weitere Informationen finden Sie unter [Über Ordner in Analytics](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md).

![Landing (alle)](assets/landing-all2.png)

>[!NOTE]
>
>Einige der folgenden Einstellungen bleiben während der Sitzung und sitzungsübergreifend bestehen. Hierzu zählen die Registerkarte, die Filter und die Spalten, die ausgewählt wurden, sowie die Sortierrichtung der Spalte. Suchergebnisse sind nicht persistent.

### Anpassen von Tabellenspalten

Um die Spaltenbreiten anzupassen, ziehen Sie den vertikalen Balken, der die einzelnen Spalten trennt.

Um Spalten zur Projektliste hinzuzufügen oder daraus zu entfernen, klicken Sie oben rechts auf das Spaltensymbol (![Landing (alle)](/help/analyze/assets/select-column.png)) und wählen Sie dann Spaltentitel aus bzw. entfernen Sie die Auswahl.

Die verfügbaren Spalten sind:

| Spaltenname | Beschreibung |
|---------|----------|
| [!UICONTROL **Name**] | Der Name des Projekts. |
| [!UICONTROL **Typ**] | Gibt an, ob es sich bei diesem Typ um ein Analysis Workspace-Projekt, eine mobile Scorecard oder einen Ordner handelt. |
| [!UICONTROL **Tags**] | Taggt Projekte, um sie in Gruppen einzuteilen. |
| [!UICONTROL **Geplant**] | Wählen Sie [!UICONTROL Ein], wenn ein Projekt geplant ist, oder [!UICONTROL Aus], wenn dies nicht der Fall ist. Wenn Sie auf den [!UICONTROL Ein]-Link klicken, können Sie Informationen zum geplanten Projekt anzeigen. Sie können auch [den Projektplan bearbeiten](/help/analyze/analysis-workspace/curate-share/t-schedule-report.md), wenn Sie Projektinhaber sind. |
| [!UICONTROL **Projektrolle**] | Gibt die Projektrollen an: ob Sie Projekteigentümer sind und ob Sie berechtigt sind, das Projekt zu bearbeiten oder zu duplizieren. |
| [!UICONTROL **Report Suite**] | Gibt die Report Suites an, die mit dem Projekt verknüpft sind.<br>Tabellen und Visualisierungen innerhalb eines Bedienfelds erhalten Daten von der oben rechts im Bedienfeld ausgewählten Report Suite. Von der Report Suite hängt auch ab, welche Komponenten in der linken Leiste verfügbar sind. In einem Projekt können Sie je nach Anwendungsfällen Ihrer Analyse eine oder viele Report Suites verwenden. Die Liste der Report Suites ist nach Relevanz sortiert. Adobe definiert die Relevanz anhand der Häufigkeit der kürzlichen Verwendung der Suite durch die aktuelle Benutzerin bzw. den aktuellen Benutzer und der Häufigkeit der Verwendung der Suite innerhalb der Organisation. |
| [!UICONTROL **Inhaber**] | Die Person, die das Projekt erstellt hat. |
| [!UICONTROL **Freigegeben für**] | Zeigt an, für wen das Projekt derzeit freigegeben ist. |
| [!UICONTROL **Zuletzt geändert**] | Datum und Uhrzeit der letzten Änderung des Projekts. |
| [!UICONTROL **Zuletzt geöffnet**] | Identifiziert das Datum, an dem ein Projekt zuletzt von dem Benutzer geöffnet wurde, der sich gerade die Seite &quot;Projekte&quot;ansieht. |
| [!UICONTROL **Zuletzt verwendet**] | Hilft festzustellen, ob ein Projekt für Benutzer in Ihrer Organisation nützlich ist, indem das Datum und die Uhrzeit der letzten Öffnung des Projekts durch einen Benutzer innerhalb der Organisation angezeigt werden.<p>Diese Spalte steht nur Systemadministratoren zur Verfügung.</p> |
| [!UICONTROL **Projekt-ID**] | Kann zum Debugging von Projekten verwendet werden. |
| [!UICONTROL **Längster Datumsbereich**] | Längere Datumsbereiche erhöhen die Komplexität von Projekten und können die Verarbeitungs- und Ladezeiten erhöhen. |
| [!UICONTROL **Anzahl der Abfragen**] | Die Gesamtzahl der Anfragen, die an Analytics beim Laden des Projekts gesendet wurden. Eine höhere Anzahl von Projektabfragen erhöht die Komplexität eines Projekts und somit auch die Verarbeitungs- und Ladezeiten. Diese Daten sind erst verfügbar, nachdem ein Projekt geladen oder ein geplantes Projekt gesendet wurde. |
| [!UICONTROL **Ort**] | Zeigt den Ordner an, in dem sich das Projekt befindet. |

### Andere UI-Elemente auf der Seite &quot;Projekte&quot;

| UI-Element | Definition |
| --- | --- |
| Voreinstellungen bearbeiten | Ermöglicht es Ihnen, [!UICONTROL Tutorials anzuzeigen] und [Benutzereinstellungen zu bearbeiten](/help/analyze/analysis-workspace/user-preferences.md). |
| [!UICONTROL Neu erstellen] | Öffnet das Projekt-Modal, in dem Sie ein Analysis Workspace-Projekt oder eine mobile Scorecard erstellen oder eine Unternehmensvorlage öffnen können. |
| [!UICONTROL Weniger anzeigen<br> Mehr anzeigen] | Blendet das Banner ein oder aus: ![Oberes Banner](assets/top-banner.png) |
| [!UICONTROL Analysis Workspace-Projekt] | Erstellt ein leeres [Analysis Workspace-Projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de), das Sie anpassen und weiterverwenden können. |
| [!UICONTROL Mobile Scorecard] | Erstellt eine leere [mobile Scorecard](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/curator.html?lang=de), die Sie anpassen und weiterverwenden können. |
| [!UICONTROL Schulungs-Tutorial öffnen] | Öffnet das Analysis Workspace-Tutorial, das Sie Schritt für Schritt durch die Erstellung eines neuen Projekts führt. |
| [!UICONTROL Versionshinweise öffnen] | Öffnet den Abschnitt „Adobe Analytics“ der neuesten Versionshinweise zu Adobe Experience Cloud. |
| Filtersymbol | Ermöglicht das Filtern nach Tags, Report Suites, Eigentümern, Typen und anderen Kriterien („Meine“, „Für mich freigegeben“, „Favoriten“ und „Genehmigt“) |
| Suchleiste | Durchsucht alle Spalten in der Tabelle. |
| Auswahlfeld | Wählt ein oder mehrere Projekte aus, um die Projektverwaltungsaktionen anzuzeigen, die Sie ausführen können: **Löschen**, **Freigeben**, **Umbenennen**, **Kopieren**, **Loslösen**, **Nach oben**, **Nach unten**, **Taggen**, **Genehmigen**, **CSV exportieren** und **Verschieben nach**. Sie sind möglicherweise nicht berechtigt, alle aufgeführten Aktionen durchzuführen. |
| [!UICONTROL Favoriten] | Fügt neben einem Projekt oder Ordner einen Stern hinzu, der als Filter verwendet werden kann. |
| [!UICONTROL Name] | Der Name des Projekts. |
| Anheften-Symbol | Fixiert Elemente so, dass sie immer oben in der Liste angezeigt werden. Sie können die Reihenfolge aber anpassen, indem Sie Elemente nach oben oder unten verschieben. Verwenden Sie das Optionsmenü mit den Auslassungspunkten und wählen Sie in der Liste **Nach oben** oder **Nach unten** aus. |
| Infosymbol (i) | Zeigt die folgenden Informationen zu einem Projekt an: Typ, Projektrolle, Eigentümer, Beschreibung und für wen es freigegeben ist. Es zeigt auch an, wer dieses Projekt [bearbeiten oder duplizieren](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/share-projects.html?lang=de) kann. |
| Auslassungspunkte (...) | Zeigt die Projektverwaltungsaktionen an, die Sie ausführen können: **Löschen**, **Freigeben**, **Umbenennen**, **Kopieren**, **Loslösen**, **Nach oben**, **Nach unten**, **Taggen**, **Genehmigen**, **CSV exportieren** und **Verschieben nach**. Sie sind möglicherweise nicht berechtigt, alle aufgeführten Aktionen durchzuführen. |
| ANZEIGEN: Ordner und Projekte oder alle Projekte | Ändert die Anzeigeeinstellung der Tabelle, sodass Ordner und Projekte entsprechend Ihrer Ordnerorganisation **oder** alle Projekte in einer ungeordneten Liste angezeigt werden. |
| &lt; (Schaltfläche „Zurück“) | Hiermit gelangen Sie in einem Analysis Workspace-Projekt oder einem Bericht zu Ihrer letzten Landingpage-Konfiguration zurück. Die Seitenkonfiguration, die Sie beim Verlassen der Landingpage hatten, bleibt bis zur Rückkehr erhalten. |

## Navigieren durch die Registerkarte [!UICONTROL Berichte] {#navigate-reports}

Die Registerkarte [!UICONTROL Berichte] fasst die folgenden drei Berichtssätze zusammen:

* Die vordefinierten [!UICONTROL Arbeitsbereich]-Vorlagen, die sich zuvor unter [!UICONTROL Arbeitsbereich] > [!UICONTROL Projekt] > [!UICONTROL Neu] befanden. Adobe verwendet in diesem Zusammenhang nicht mehr das Wort „Vorlage“.
* Die meisten vordefinierten Berichte befanden sich zuvor in Adobe Analytics im oberen Menü [!UICONTROL Berichte]. Diese Berichte werden jetzt in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) angezeigt.

>[!NOTE]
>
>Beachten Sie bei der Verwendung von Berichten Folgendes:
>* Unter „Berichte“ wird der Ordner „Favoriten“ nur angezeigt, wenn Sie einen neuen Bericht als Favoriten markieren. Es werden keine bereits vorhandenen Reports &amp; Analytics-Favoriten übernommen.
>* Es sind nur die am häufigsten verwendeten Berichte verfügbar, die zuvor in Reports &amp; Analytics gruppiert waren. Eine Handvoll selten verwendeter oder nicht mehr relevanter Berichte ist nicht mehr verfügbar. Sehen Sie sich im Folgenden die [häufig gestellten Fragen zu Landingpages](#landing-page-faq) an, um weitere Details zu erhalten.

![Registerkarte „Berichte“](assets/reports-tab2.png)

Weitere Informationen zur Registerkarte „Berichte“ in Analysis Workspace, einschließlich Anzeigen und Speichern von Berichten, finden Sie unter [Verwenden von vordefinierten Berichten](/help/analyze/analysis-workspace/reports/use-reports.md).

Informationen zum Erstellen und Verwalten benutzerdefinierter Unternehmensberichte finden Sie unter [Erstellen und Verwalten von Unternehmensberichten](/help/analyze/analysis-workspace/reports/create-company-reports.md).

## Verwenden der Registerkarte „Lernen“ {#navigate-learning}

Die Seite „Lernen“ enthält praktische Videoführungen und Tutorials sowie Links zur Dokumentation.

Verwenden Sie die Seite „Lernen“ in Adobe Analytics, um Funktionen für Anfängerinnen bzw. Anfänger, ein mittleres Niveau oder für Fortgeschrittene sowie Anwendungsfälle in Adobe Analytics zu erfahren.

### Zugreifen auf die Seite „Lernen“

1. Wählen Sie in Adobe Analytics [!UICONTROL **Arbeitsbereich**] > [!UICONTROL **Lernen**] aus.

### Funktionen von Lernseiten

* **Inhalt filtern:** Mit dem Filtersymbol in der linken Leiste können Sie Lerninhalte nach Erlebnisebene („Anfängerinnen und Anfänger“, „Mittleres Niveau“ oder „Fortgeschrittene“) und nach Inhaltstyp („Dokument“, „Video“ oder „Touren und Tutorials“) filtern.
* **Fortschritt verfolgen:** Nachdem Sie ein Inhaltselement ausgewählt haben, wird das Tag **[!UICONTROL Angesehen]** angezeigt. Mit diesem Tag können Sie Ihren Fortschritt durch den Lerninhalt verfolgen. Sie können das Tag **[!UICONTROL Angesehen]** auswählen, um es aus einem Inhaltselement zu entfernen.
* **Zusätzliche Inhalte anzeigen:** Wählen Sie beim Anzeigen eines Videos die Schaltfläche **[!UICONTROL Weitere Informationen]** aus, um zugehörige Dokumentationsinhalte zu Experience League anzuzeigen. Wählen Sie auf der Seite „Lernen“ eine der folgenden Optionen aus, um weitere Inhalte anzuzeigen:
   * **[!UICONTROL YouTube besuchen]:** Sehen Sie die vollständige YouTube-Playlist von Analysis Workspace.
   * [!UICONTROL **Experience League besuchen**]: Sehen Sie die vollständige Adobe Analytics-Dokumentation in Experience League.
* **Grundlagen für neue Benutzer:** Die Tour [!UICONTROL Workspace-Grundlagen] wird für neue Benutzerinnen und Benutzer empfohlen. Diese Tour führt Sie direkt zu Workspace und durch die gängigsten Aktionen. Diese Tour kann auch jederzeit in Workspace über das QuickInfo-Popup in der Kopfzeile des Bedienfelds neu gestartet werden.

## Einrichten einer Landingpage {#set-landing}

Benutzer können ihre bevorzugte Landingpage festlegen.

1. Gehen Sie zu Analytics > [!UICONTROL Komponenten] > [!UICONTROL Voreinstellungen] > [!UICONTROL Allgemein].
1. Überprüfen Sie, welche Landingpage Sie bevorzugen:

   ![Landingpage festlegen](assets/landing-pref.png)

## Ausblenden der Registerkarte „Berichte“ {#hide-reports}

Administratoren können die Registerkarte „Berichte“ für alle Benutzer in ihrer Organisation ausblenden.

1. Navigieren Sie zu [!UICONTROL Analytics] > [!UICONTROL Komponenten] > [!UICONTROL Voreinstellungen] > [!UICONTROL Firma].
1. Aktivieren Sie **[!UICONTROL Registerkarte „Berichte“ ausblenden]**.

## Häufig gestellte Fragen zu Landingpages {#landing-faq}

| Frage | Antwort |
| --- | --- |
| Wo sind die Vorlagen, die ich aus dem [!UICONTROL Arbeitsbereich] gewohnt bin? | Diese Vorlagen sind auf der Registerkarte [!UICONTROL Berichte] gruppiert. |
| Wird die Arbeit, die ich in der Benutzeroberfläche des Beta-Programms verrichte, in die Produktionsumgebung des [!UICONTROL Arbeitsbereichs] übertragen? | Ja, alle in der Beta-Version durchgeführten Arbeiten werden in das alte/aktuelle [!UICONTROL Arbeitsbereich]-Erlebnis übernommen. |
| Werden meine aktuellen Reports &amp; Analytics-Favoriten übernommen? | Nein, sie werden NICHT übernommen. Alle [!UICONTROL Arbeitsbereich]-Projekt-Favoriten werden jedoch übernommen. |
| Gibt es eine maximale Anzahl von Projekten, die ich anheften kann? | Nein, es gibt keine Begrenzung für die Anzahl der Projekte, die Sie anheften können. |
| Können Administratoren diese neue Landingpage für ihre Benutzer festlegen? | Nein, Administratoren können die neue Landingpage nicht im Namen von Benutzern festlegen. Die einzelnen Benutzer müssen den Umschalter selbst aktivieren. |
| Sind alle Berichte, die in [!DNL Reports & Analytics] vorhanden waren, weiterhin verfügbar? | Nein, die folgenden Berichte wurden auf der Grundlage der allgemeinen Nutzungsdaten schrittweise eingestellt: <ul><li>Alle benutzerdefinierten eVars/Eigenschaften/Ereignisse/Klassifizierungen<li>Meine empfohlenen Berichte</li><li>Unique Visitors pro Tag, Woche, Monat, Quartal und Jahr</li><li>Unique Customers pro Woche/Monat/Quartal/Jahr</li><li>Tiefe des Aktionsnamens</li><li>Zusammenfassung des Aktionsnamens</li><li>Dashboard hinzufügen</li><li>Alter</li><li>Audio-Unterstützung</li><li>Rechnungsinformationen</li><li>Klicks pro Seite</li><li>Farbtiefe</li><li>Cookie-Unterstützung</li><li>Cookies</li><li>Verbindungstypen</li><li>Kreative Elemente</li><li>Kreditkartenart</li><li>Crossselling</li><li>Benutzerdefinierte Ereignistrichter</li><li>Benutzerspezifische Links</li><li>Kunden-ID</li><li>Wochentag</li><li>Name der Einstiegsaktion</li><li>Name der Ausstiegsaktion</li><li>Ausstiegs-Links</li><li>Fallout</li><li>Datei-Downloads</li><li>Suche im Geschäft</li><li>Vollständige Pfade</li><li>Geschlecht</li><li>VISTA-Regel für Treffertyp</li><li>Bildunterstützung</li><li>Java</li><li>JavaScript</li><li>JavaScript-Version </li><li>Lesezeichen verwalten</li><li>Dashboards verwalten</li><li>Farbtiefe des Bildschirms</li><li>Auflösung des Bildschirms</li><li>Newsletter-Anmeldungen</li><li>Name der nächsten Aktion</li><li>Fluss für Name der nächsten Aktion</li><li>Null-Suchen</li><li>Betriebssystem</li><li>Bestellübersicht</li><li>Seite des Tages</li><li>Nicht gefundene Seiten</li><li>PathFinder</li><li>Pfadlänge</li><li>Name der vorherigen Aktion</li><li>Fluss für Name der vorherigen Aktion</li><li>Produktaktivität</li><li>Produktkosten</li><li>Produktabteilung</li><li>Produktinventarkategorie</li><li>Produktname</li><li>Produktbewertungen</li><li>Produktsaison</li><li>Produktfreigaben</li><li>Produktvergrößerungen</li><li>Neu laden</li><li>Suchvorgänge</li><li>Server</li><li>Einzelseitenbesuche</li><li>Versandinformationen</li><li>Site-Hierarchie</li><li>Erwähnungen in Social Media</li><li>Tageszeit</li><li>Verbrachte Zeit für Aktionsname</li><li>Video-Unterstützung</li><li>Besucherstatus</li></ul> |
