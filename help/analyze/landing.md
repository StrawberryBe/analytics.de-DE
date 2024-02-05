---
description: Erläutert die neue Landingpage, die Analysis Workspace und Reports & Analytics in einer Benutzeroberfläche zusammenfasst und so einen zentralen Zugriffspunkt (Workspace) bietet.
title: Neue Landingpage von Adobe Analytics
role: User, Admin
feature: Analytics Basics
exl-id: 0a2fb778-491a-4dc3-aae4-afadb3ab1a1e
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: ht
source-wordcount: '2168'
ht-degree: 100%

---

# Neue Landingpage von Adobe Analytics

Die Landingpage für Adobe Analytics vereint sowohl [!DNL Analysis Workspace] als auch [!DNL Reports & Analytics] (eingestellt) in einer einzigen Oberfläche und einem Zugangspunkt unter dem Dach von [!DNL Workspace]. Sie enthält eine neue Startseite für den Projekt-Manager, ein aktualisiertes Berichtsmenü und aktualisierte Berichte sowie einen Lernbereich, der Ihnen dabei hilft, die ersten Schritte effektiver zu bewältigen. Hier finden Sie eine Videoübersicht:

>[!VIDEO](https://video.tv.adobe.com/v/334278/?quality=12)

## Häufig gestellte Fragen zur neuen Landingpage {#new-features}

| Funktion | Beschreibung | Screenshot |
| --- | --- | --- |
| Erweitern der Tabelle [!UICONTROL Projekte] auf Vollbild | Um die Tabelle zu erweitern, klicken Sie einfach auf das Hamburger-Menüsymbol. Durch diese Aktion werden die Registerkarten in der linken Leiste reduziert. | ![Tabelle erweitern](assets/landing-collapse2.png) |
| Spaltenbreite anpassen | Zuvor war die Spaltenbreite fixiert. Jetzt können Sie sie anpassen, indem Sie das Spaltentrennzeichen ziehen. | ![Spaltenbreite](assets/column-width.png) |
| Fixierte Elemente neu anordnen | Um die fixierten Elemente nach oben und unten zu verschieben, klicken Sie auf das Auslassungszeichen neben dem fixierten Element und wählen Sie **[!UICONTROL Nach oben]** oder **[!UICONTROL Nach unten]**. | ![Verschieben von fixierten Elementen](assets/move-up-down.png) |
| Neue Tabellenspalten | Klicken Sie auf [!UICONTROL Tabelle anpassen] rechts oben in der Tabelle. Die neuen Tabellenspalten umfassen: <ul><li>**[!UICONTROL Geplant]**: Legen Sie dies auf [!UICONTROL Ein] fest, wenn ein Projekt geplant ist, oder auf [!UICONTROL Aus], wenn dies nicht der Fall ist. Ein Klick auf den Link [!UICONTROL Ein] zeigt Informationen über das geplante Projekt an. Sie können auch [den Projektplan bearbeiten](/help/analyze/analysis-workspace/curate-share/t-schedule-report.md), wenn Sie Projektinhaber sind.</li><li>**[!UICONTROL Projekt-ID]**: Die Projekt-ID kann zum Debugging von Projekten verwendet werden.</li><li>**[!UICONTROL Längster Datumsbereich]**: Längere Datumsbereiche erhöhen die Projektkomplexität und können die Verarbeitungs- und Ladezeiten erhöhen. </li><li>**[!UICONTROL Anzahl der Abfragen]**: Die Gesamtzahl der Anfragen, die beim Laden des Projekts an Analytics gesendet wurden. Eine höhere Anzahl von Projektabfragen erhöht die Projektkomplexität und kann die Verarbeitungs- und Ladezeiten erhöhen. Diese Daten sind erst verfügbar, nachdem ein Projekt geladen oder ein geplantes Projekt gesendet wurde. </li></ul> | ![Neue Spalten](assets/new-columns.png) |
| Einfacher Klick zum Öffnen eines Berichts | Zuvor musste ein Doppelklick durchgeführt werden. |  |
| Neue Links zu **[!UICONTROL Reports &amp; Analytics]**-Berichten | <ul><li>**[!UICONTROL Berichte]** > **[!UICONTROL Zielgruppe]** > **[!UICONTROL Bots]**</li><li>**[!UICONTROL Berichte]** > **[!UICONTROL Zielgruppe]** > **[!UICONTROL Bot-Seiten]**<li>**[!UICONTROL Berichte]** > **[!UICONTROL Interaktion]** > **[!UICONTROL Echtzeit]**</li></ul> | ![Neue Links](assets/report-links.png) |
| Neue native Berichte | <ul><li>**[!UICONTROL Berichte]** > **[!UICONTROL Am beliebtesten]** > **[!UICONTROL Nächste Seite]**</li><li>**[!UICONTROL Berichte]** > **[!UICONTROL Am beliebtesten]** > **[!UICONTROL Vorherige Seite]**</li><li>**[!UICONTROL Berichte]** > **[!UICONTROL Interaktion]** > **[!UICONTROL Seitenanalyse]** > **[!UICONTROL Seitenzusammenfassung]**</li></ul>Beachten Sie, dass diese Berichte im [!UICONTROL Arbeitsbereich]-Format vorliegen und eine Konfiguration und Erstellung erfordern. Die Ausgabe besteht aus einem Bereich mit allgemeinen Metriken, Trend-Daten, [!UICONTROL Flussvisualisierung] und mehr. Sie können diese Berichte anpassen und Dimensionen, Dimensionselemente usw. ändern. Diese Berichte sind auch als Bedienfelder unter Arbeitsbereich-Bedienfeldern verfügbar. | ![Nächste Seite](assets/next-page.png) |
| Das Modal **[!UICONTROL Projekt erstellen]** ist wieder verfügbar. | Wenn Sie in Analysis Workspace auf **[!UICONTROL Projekt erstellen]** klicken, haben Sie erneut die Wahl zwischen einem [!UICONTROL leeren Projekt] und einer [!UICONTROL leeren mobilen Scorecard]. Sie können auch aus beliebigen Vorlagen wählen, die Ihr Unternehmen erstellt hat. | ![Neu erstellen](assets/create-new.png) |
| Auch in Customer Journey Analytics verfügbar | Diese Landingpage ist in abgeänderter Form auch in Customer Journey Analytics verfügbar. |  |

{style="table-layout:auto"}

## Oberste Menüstruktur {#top-menu}

![Menü oben](assets/top-menus.png)

* Top-Analytics-Menü: Die meisten Berichte befinden sich nun im Menü [!UICONTROL Berichte] in der linken Leiste.
* Die linke Leiste verfügt über drei Registerkarten: [!UICONTROL Projekte], [!UICONTROL Berichte] und [!UICONTROL Lernen].

### Terminologie

* **[!UICONTROL Projekte]** sind benutzerdefinierte Entwürfe, die aus Datenkomponenten, Tabellen und Visualisierungen bestehen, die von Ihnen erstellt oder einer anderen Person für Sie erstellt und freigegeben wurden. [!UICONTROL Projekte] beziehen sich auch auf leere Projekte und leere mobile Scorecards.
* **[!UICONTROL Berichte]** beziehen sich auf alles, was von Adobe vorkonfiguriert wurde, z. B. Vorlagen in Workspace.
* **[!UICONTROL Vorlagen]** werden nicht mehr als Begriff für die vordefinierten Arbeitsbereich-Projekte von Adobe verwendet. Sie befinden sich nun unter [!UICONTROL Berichte]. Der Begriff [!UICONTROL Vorlagen] wird weiterhin für Vorlagen verwendet, die Ihr Unternehmen erstellt hat.

## Navigieren Sie zur Registerkarte [!UICONTROL Projekte] {#navigate-projects}

[!UICONTROL Projekte] fungieren als Startseite von [!UICONTROL Arbeitsbereich]. Auf der Registerkarte „Projekte“ werden der Unternehmensordner, alle von Ihnen erstellten persönlichen Ordner sowie Ihre Projekte und mobilen Scorecards angezeigt. Auf dieser Seite können Sie Ordner, Projekte und mobile Scorecards anzeigen, erstellen und ändern. Weitere Informationen finden Sie unter [Über Ordner in Analytics](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md).

![Landing (alle)](assets/landing-all2.png)

>[!NOTE]
>
>Einige der folgenden Einstellungen bleiben während der Sitzung und sitzungsübergreifend bestehen. Hierzu zählen die Registerkarte, die Filter und die Spalten, die ausgewählt wurden, sowie die Sortierrichtung der Spalte. Suchergebnisse sind nicht persistent.

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
| [!UICONTROL Typ] | Gibt an, ob es sich bei diesem Typ um ein Analysis Workspace-Projekt, eine mobile Scorecard oder einen Ordner handelt. |
| [!UICONTROL Tags] | Taggt Projekte, um sie in Gruppen einzuteilen. |
| [!UICONTROL Projektrolle] | Gibt die Projektrollen an: ob Sie Projekteigentümer sind und ob Sie berechtigt sind, das Projekt zu bearbeiten oder zu duplizieren. |
| [!UICONTROL Report Suite] | Gibt die Report Suites an, die mit dem Projekt verknüpft sind.<br>Tabellen und Visualisierungen innerhalb eines Bedienfelds erhalten Daten von der oben rechts im Bedienfeld ausgewählten Report Suite. Von der Report Suite hängt auch ab, welche Komponenten in der linken Leiste verfügbar sind. In einem Projekt können Sie je nach Anwendungsfällen Ihrer Analyse eine oder viele Report Suites verwenden. Die Liste der Report Suites ist nach Relevanz sortiert. Adobe definiert die Relevanz anhand der Häufigkeit der kürzlichen Verwendung der Suite durch die aktuelle Benutzerin bzw. den aktuellen Benutzer und der Häufigkeit der Verwendung der Suite innerhalb der Organisation. |
| [!UICONTROL Inhaber] | Die Person, die das Projekt erstellt hat. |
| [!UICONTROL Zuletzt geöffnet] | Gibt das Datum an, an dem Sie das Projekt zuletzt geöffnet haben. |
| Symbol „Tabelle anpassen“ | Ermöglicht die Auswahl der Spalten, die in der Tabelle angezeigt werden sollen. Um Spalten zur Projektliste hinzuzufügen oder daraus zu entfernen, klicken Sie oben rechts auf das Spaltensymbol (![Landing (alle)](/help/analyze/assets/select-column.png)) und wählen Sie dann Spaltentitel aus bzw. entfernen Sie die Auswahl. |
| ANZEIGEN: Ordner und Projekte oder alle Projekte | Ändert die Anzeigeeinstellung der Tabelle, sodass Ordner und Projekte entsprechend Ihrer Ordnerorganisation **oder** alle Projekte in einer ungeordneten Liste angezeigt werden. |
| &lt; (Schaltfläche „Zurück“) | Hiermit gelangen Sie in einem Analysis Workspace-Projekt oder einem Bericht zu Ihrer letzten Landingpage-Konfiguration zurück. Die Seitenkonfiguration, die Sie beim Verlassen der Landingpage hatten, bleibt bis zur Rückkehr erhalten. |

### Entfernen der Projekt-Manager-Seite {#deprecate-pm-page}

Mit der Veröffentlichung der neuen Landingpage haben wir die Seite „Projekt-Manager“ unter dem Komponenten-Manager entfernt. Die neue Landingpage verfügt über alle Funktionen der alten Seite „Projekt-Manager“ und bietet noch viel mehr.

Ein gängiger Anwendungsfall für die Seite „Projekt-Manager“ war die Ansicht aller Ihrer Projekte.

Um auf der neuen Landingpage mithilfe der Filterleiste alle Ihre Projekte anzuzeigen, wählen Sie **SONSTIGE FILTER** und danach **Alle anzeigen** aus.

![Alle Projekte anzeigen](assets/show-all-fIlter.png)

Wenn Sie sich in der Ansicht „Ordner &amp; Projekte“ befinden, wird ein modales Popup angezeigt, in dem Sie gefragt werden, ob Sie zur Ansicht „Alle Projekte“ wechseln möchten. Dies erleichtert die Anzeige aller Ihrer Projekte außerhalb der Ordner, in denen sie möglicherweise organisiert sind. Wählen Sie **Zur Ansicht „Alle Projekte“ wechseln** aus, um eine bessere Ansicht aller Projekte zu erhalten, auf die Sie Zugriff haben.

![Zu „Alle Projekte“ wechseln](assets/switch-all-projects-view.png)

Ein weiterer Anwendungsfall für Administrierende ist die Verwaltung von Unternehmensberichten, um sie zu löschen, umzubenennen, zu taggen oder zu genehmigen. Informationen zum Verwalten von Berichten finden Sie unter [Verwalten von Unternehmensberichten](#manage-company-reports).

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
