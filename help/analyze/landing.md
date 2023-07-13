---
description: Erläutert die neue Landingpage, die Analysis Workspace und Reports & Analytics in einer Benutzeroberfläche zusammenfasst und so einen zentralen Zugriffspunkt (Workspace) bietet.
title: Neue Landingpage von Adobe Analytics
role: User, Admin
feature: Analytics Basics
exl-id: 0a2fb778-491a-4dc3-aae4-afadb3ab1a1e
source-git-commit: f7bd5eaffd4502510451e3afb5929682ad967ecb
workflow-type: tm+mt
source-wordcount: '4071'
ht-degree: 85%

---

# Neue Landingpage von Adobe Analytics

Die Landingpage für Adobe Analytics vereint sowohl [!DNL Analysis Workspace] als auch [!DNL Reports & Analytics] in einer einzigen Oberfläche und einem Zugangspunkt unter dem Dach von [!DNL Workspace]. Sie enthält eine neue Startseite für den Projekt-Manager, ein aktualisiertes Berichtsmenü und aktualisierte Berichte sowie einen Lernbereich, der Ihnen dabei hilft, die ersten Schritte effektiver zu bewältigen. Hier finden Sie eine Videoübersicht:

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
| Auch in Customer Journey Analytics verfügbar | Diese Landingpage in geänderter Form ist auch in Customer Journey Analytics verfügbar. |  |

{style="table-layout:auto"}

## Oberste Menüstruktur {#top-menu}

![Menü oben](assets/top-menus.png)

* Top-Analytics-Menü: Die meisten Berichte befinden sich nun im Menü [!UICONTROL Berichte] in der linken Leiste.
* Die linke Leiste verfügt über drei Registerkarten: [!UICONTROL Projekte], [!UICONTROL Berichte] und [!UICONTROL Lernen].

### Terminologie

* **[!UICONTROL Projekte]** sind benutzerdefinierte Entwürfe, die aus Datenkomponenten, Tabellen und Visualisierungen bestehen, die von Ihnen erstellt oder einer anderen Person für Sie erstellt und freigegeben wurden. [!UICONTROL Projekte] beziehen sich auch auf leere Projekte und leere mobile Scorecards.
* **[!UICONTROL Berichte]** beziehen sich auf alles, was von Adobe vorkonfiguriert wurde, z. B. Berichte in Reports &amp; Analytics und Vorlagen im Arbeitsbereich.
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
| [!UICONTROL Report Suite] | Gibt die Report Suites an, die mit dem Projekt verknüpft sind.<br>Tabellen und Visualisierungen innerhalb eines Bedienfelds erhalten Daten von der oben rechts im Bedienfeld ausgewählten Report Suite. Von der Report Suite hängt auch ab, welche Komponenten in der linken Leiste verfügbar sind. In einem Projekt können Sie je nach Anwendungsfällen Ihrer Analyse eine oder viele Report Suites verwenden. Die Liste der Report Suites ist nach Relevanz sortiert. Adobe definiert die Relevanz anhand der Häufigkeit der kürzlichen Verwendung der Suite durch den aktuellen Benutzer und der Häufigkeit der Verwendung der Suite innerhalb des Unternehmens. |
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

Die [!UICONTROL Berichte] tab fasst die folgenden Berichtssätze zusammen:

* Die vordefinierten [!UICONTROL Arbeitsbereich]-Vorlagen, die sich zuvor unter [!UICONTROL Arbeitsbereich] > [!UICONTROL Projekt] > [!UICONTROL Neu] befanden. Adobe verwendet in diesem Zusammenhang nicht mehr das Wort „Vorlage“.
* Die meisten vordefinierten Berichte befanden sich zuvor in Adobe Analytics im oberen Menü [!UICONTROL Berichte]. Diese Berichte werden jetzt in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) angezeigt.

>[!NOTE]
>
>Beachten Sie bei der Verwendung von Berichten Folgendes:
>* Unter „Berichte“ wird der Ordner „Favoriten“ nur angezeigt, wenn Sie einen neuen Bericht als Favoriten markieren. Es werden keine bereits vorhandenen Reports &amp; Analytics-Favoriten übernommen.
>* Es sind nur die am häufigsten verwendeten Berichte verfügbar, die zuvor in Reports &amp; Analytics gruppiert wurden. Eine Handvoll selten verwendeter oder nicht mehr relevanter Berichte ist nicht mehr verfügbar. Siehe [Häufig gestellte Fragen zu Landingpages](#landing-page-faq) unten finden Sie weitere Details.

![Registerkarte „Berichte“](assets/reports-tab2.png)


### Berichte anzeigen {#menus}

1. Navigieren Sie zur Registerkarte [!UICONTROL **Berichte**]
1. Verwenden Sie das Suchfeld, um nach einem bestimmten Bericht zu suchen.

   Oder

   Navigieren Sie zum Bericht, den Sie anzeigen möchten.

   Die folgenden Berichte sind verfügbar:

   | Menüelement | Berichte unter diesem Menüelement |
   | --- | --- |
   | **[!UICONTROL Beliebteste]** | <ul><li>Schulungs-Tutorial (Vorhandene Vorlage für Arbeitsbereich)</li><li>Seiten (Was sind meine Top-Seiten?)</li><li>Seitenansichten (Wie viele Seitenaufrufe erzeuge ich?)</li><li>Besuche (Wie viele Besuche erhalte ich?)</li><li>Besucher (Wie viele Besucher bekomme ich?)</li><li>Schlüsselmetriken (Wie sehen meine wichtigsten Kennzahlen aus?)</li><li>Site-Bereiche (Welche Bereiche meiner Site generierten die meisten Seitenansichten?</li><li>Nächste Seite (Auf welche Seiten gehen meine Besucher als Nächstes?)</li><li>Vorherige Seite (Welche vorherigen Seiten haben meine Besucher aufgerufen?)</li><li>Kampagnen (Welche Kampagnen liegen meinen Schlüsselmetriken zugrunde?)</li><li>Produkte (Welche Produkte liegen meinen Schlüsselmetriken zugrunde?)</li><li>Letztkontakt-Kanal (Welcher Letztkontakt-Kanal erzielt die beste Leistung?)</li><li>Letztkontakt-Kanaldetail (Welcher spezifische Letztkontakt-Kanal ist leistungsstärker als andere?)</li><li>Umsatz (Wie entwickelt sich mein Umsatz?)</li><li>Bestellungen (Wie entwickeln sich meine Bestellungen?)</li><li>Einheiten (Wie viele Einheiten verkaufe ich?)</li></ul> |
   | **[!UICONTROL Interaktion]** | <ul><li>Schlüsselmetriken (Wie sehen meine wichtigsten Kennzahlen aus?)</li><li>Seitenansichten (Wie viele Seitenaufrufe erzeuge ich?)</li><li>Seiten (Was sind meine Top-Seiten?)</li><li>Besuche (Wie viele Besuche erhalte ich?)</li><li>Besucher (Wie viele Besucher bekomme ich?)</li><li>Zeit pro Besuch (Wie viel Zeit verbringen meine Benutzer pro Besuch?)</li><li>Zeit vor Ereignis (Wie viel Zeit verbringen meine Benutzer vor einem Erfolgsereignis?)</li><li>Site-Bereiche (Welche Bereiche meiner Site generierten die meisten Seitenansichten?</li><li>Nutzung von Web-Inhalten (Welche Inhalte werden am häufigsten genutzt und sind für Benutzer interessant?)</li><li>Nutzung von Medieninhalten (Welche Inhalte werden am häufigsten genutzt und sind für Benutzer interessant?)</li><li>Fluss zur nächsten/vorherigen Seite (Was sind/waren die nächsten/vorherigen Pfade, die meine Besucher nutzen/genutzt haben?)</li><li>Fallout (Wo sehe ich Fallout für meine digitalen Eigenschaften?)</li><li>Geräteübergreifende Analyse (Verwendung geräteübergreifender Analysen in Analysis Workspace)</li><li>Web-Bindungsgrad (Wer sind meine treuen Benutzer und was tun sie?)</li><li>Medien-Audiokonsum (Was sind Trends und Top-Metriken beim Audiokonsum?)</li><li>Medien-Neuigkeit, -Häufigkeit, -Treue (Wer sind meine treuen Leser?)</li><li>Seitenanalyse > Neuladungen (Welche Seiten werden am häufigsten neu geladen?)</li><li>Seitenanalyse > Besuchszeit pro Seite (Wie viel Zeit verbringen meine Benutzer auf meinen Seiten?)</li><li>Einstiege und Ausstiege > Einstiegsseiten (Was sind meine Top-Einstiegsseiten?)</li><li>Einstiege und Ausstiege > Ursprüngliche Einstiegsseiten (Auf welcher Seite ist mein Besucher ursprünglich eingetreten?)</li><li>Einstiege und Ausstiege > Einzelseitenbesuche (Welche Seiten haben die meisten Einzelseitenbesuche generiert?)</li><li>Einstiege und Ausstiege > Ausstiegseiten (Was sind meine Top-Ausstiegsseiten?)</li></ul> |
   | **[!UICONTROL Konversion]** | <ul><li>Produkte > Produkte (Welche Produkte liegen meinen Schlüsselmetriken zugrunde?)</li><li>Produkte > Produktleistung (Welche Produkte schneiden am besten ab?)</li><li>Produkte > Kategorien (Was sind meine leistungsstärksten Produktkategorien?)</li><li>Warenkorb > Warenkörbe (Wie viele Benutzer haben ein Produkt zum Warenkorb hinzugefügt?)</li><li>Warenkorb > Warenkorbansichten (Wie oft haben meine Besucher ihren Warenkorb angesehen?)</li><li>Warenkorb > Zusatz zum Warenkorb (Wie oft fügen Benutzer ihrem Warenkorb ein Produkt hinzu?)</li><li>Warenkorb > Entnahme aus Warenkorb (Wie oft entfernen Benutzer ein Produkt aus ihrem Warenkorb?)</li><li>Einkäufe > Umsatz (Wie sieht mein Umsatz aus?)</li><li>Einkäufe > Bestellungen (Wie sehen meine Bestellungen aus?)</li><li>Käufe > Einheiten (Wie viele Einheiten verkaufe ich?)</li><li>[Magento: Marketing und Commerce](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#commerce)</li></ul> |
   | **[!UICONTROL Zielgruppe]** | <ul><li>Personenmetrik (Wie viele Personen interagieren mit meiner Marke?)</li><li>Besucherprofil > Standortübersicht (Welche Standorte werden von Benutzern am meisten genutzt?)</li><li>Besucherprofil > GeoSegmentation > Geo-Länder, Geo-US-Bundesstaaten, Geo-Regionen, Geo-Städte, Geo-US-DMA (Aus welchen Regionen besuchen mich meine Benutzer?)</li><li>Besucherprofil > Sprachen (Welche Sprache bevorzugen meine Benutzer?)</li><li>Besucherprofil > Zeitzonen (Aus welchen Zeitzonen kommen meine Benutzer?)</li><li>Besucherprofil > Domains (Welche ISPs werden von meinen Besuchern verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Domains auf oberster Ebene (Welche Domains leiten den Traffic zu meiner Site?)</li><li>Besucherprofil > Technologie > Technologieübersicht (Welche Technologien werden verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Technologie > Browser, Browser-Typ, Browser-Breite, Browser-Höhe (welcher Browser, welche Browser-Version des Unternehmens und welche Breite und Höhe werden von Benutzern verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Technologie > Betriebssystem, Betriebssystemtypen (Welches Betriebssystem und welche Version davon verwenden meine Besucher?)</li><li>Besucherprofil > Technologie > Mobilnetzbetreiber (Welche Mobilnetzbetreiber verwenden meine Besucher, um auf meine Site zuzugreifen?)</li><li>Besuchertreue > Rückkehrhäufigkeit (Wie viel Zeit vergeht zwischen dem aktuellen Besuch meines Benutzers und vorherigen Besuchen?)</li><li>Besuchertreue > Erneute Besuche (Wie viele meiner Besucher kehren zurück?)</li><li>Besuchertreue > Besuchsnummer (Welcher Besuchsnummernbehälter liegt den meisten meiner Schlüsselmetriken zugrunde?)</li><li>Besucherbindung > Verkaufszyklus > Kundentreue (Zu welchem Treuesegment gehören meine Benutzer?)</li><li>Besucherbindung > Verkaufszyklus > Tage bis Erstkauf (Wie viele Tage sind zwischen dem ersten Besuch meiner Benutzer und dem ersten Kauf vergangen?)</li><li>Besucherbindung > Verkaufszyklus > Tage seit letztem Kauf (Wie viele Tage sind zwischen dem aktuellen Besuch meiner Benutzer und ihrem letzten Kauf vergangen? )</li><li>Besuchertreue > Mobile > Geräte und Gerätetypen (Welche Geräte und Gerätetypen verwenden meine Besucher?)</li><li>Besucherbindung > Mobile > Hersteller (Welchen Mobilgerätehersteller verwenden meine Besucher?)</li><li>Besuchertreue > Mobile > Bildschirmgröße, Bildschirmhöhe, Bildschirmbreite (Welche Bildschirmgröße/-höhe/-breite für Mobilgeräte verwenden meine Besucher?)</li><li>Besucherbindung > Mobile > [Mobile-App-Nutzung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Journey](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Metriken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Nachrichten](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besuchertreue > Mobile > [Leistung von Mobile Apps](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Bindung durch Mobile Apps](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li></ul> |
   | **[!UICONTROL Akquise]** | <ul><li>Marketing-Kanäle > Erstkontakt-Kanal, Details zum Erstkontakt-Kanal (Welcher Erstkontakt-Kanal und welcher spezifische Erstkontakt-Kanal schneidet am besten ab?)</li><li>Marketing-Kanäle > Erster letzter Kanal, Details des ersten letzten Kanals (Welcher Letztkontakt-Kanal und welcher spezifische Letztkontakt-Kanal schneidet am besten ab?)</li><li>Kampagnen > Kampagnen (Welche Kampagnen liegen meinen Schlüsselmetriken zugrunde?)</li><li>Kampagnen > Kampagnenleistung (Welche Kampagnen erzielen den höchsten Umsatz?)</li><li>Kampagnen > Trackingcode (Welche Kampagnen-Trackingcodes erzielen die besten Ergebnisse?)</li><li>[Web-Akquise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#web)</li><li>[Mobile-Akquise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>[Advertising Analytics: Paid Search](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#advertising)</li><li>Suchbegriffe – alle, gebührenpflichtig, kostenlos (Welche Suchbegriffe und gebührenpflichtigen/kostenlosen Suchbegriffe bringen meine Schlüsselmetriken am besten voran?)</li><li>Suchmaschinen – alle, gebührenpflichtig, kostenlos (Welche Suchmaschinen und gebührenpflichtigen/kostenlosen Suchmaschinen bringen meine Schlüsselmetriken am besten voran?)</li><li>Ranking aller Suchseiten (Von welcher Suchseite aus besuchen mich meine Benutzer?)</li><li>Verweisende Domains (Von welchen Domains kommt der Traffic auf meine Seite?)</li><li>Ursprüngliche verweisende Domain (Was waren die ersten Domains, auf denen sich Benutzer vor dem Besuch meiner Site befanden?)</li><li>Referrer (Auf welchen URLs waren meine Benutzer, bevor sie sich zu meiner Website durchgeklickt haben?)</li><li>Referrer-Typen (Zu welcher Kategorie gehören die auf mich verweisenden URLs?)</li></ul> |

### Bericht anzeigen und speichern {#use-reports}

Wenn Sie nach den Änderungen von einem Bericht weg navigieren, werden Sie aufgefordert, Ihre Änderungen zu speichern oder zu verwerfen. Durch Speichern von Änderungen an einem Bericht wird der Bericht als neues Projekt gespeichert.

1. Navigieren Sie zur Registerkarte [!UICONTROL **Berichte**]
1. Wählen Sie den Bericht aus, den Sie anzeigen möchten. Beispiel: unter [!UICONTROL **Am häufigsten**], wählen Sie die [!UICONTROL **Seiten**] Bericht.

   ![Bericht zu Seiten](assets/pages-report.png)

1. Der Seitenbericht, wie in Analysis Workspace angezeigt, zeigt zwei [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) ([Balkendiagramm](/help/analyze/analysis-workspace/visualizations/bar.md) und [Zusammenfassungsnummer](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)) und eine [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) an. Die verwendete Metrik ist „Vorkommen“.
1. Führen Sie einen der folgenden Schritte aus:

   * Zeigen Sie den Bericht an.
   * Ziehen Sie ein oder mehrere Segmente in die Dropzone Segment oben. Ziehen Sie beispielsweise das Segment [!UICONTROL **Mobile Kunden**] und die Ergebnisse anzeigen.
   * Ändern Sie den Datumsbereich, indem Sie in den Kalender oben rechts wechseln.
   * Fügen Sie Dimensionsaufschlüsselungen hinzu, ziehen Sie andere Metriken hinzu und passen Sie den Bericht im Allgemeinen an Ihre Anforderungen an.

1. (Optional) Speichern Sie den Bericht als Projekt, indem Sie [!UICONTROL **Projekt**] > [!UICONTROL **Speichern**].

   Dadurch wird der Bericht als neues Projekt gespeichert. Der vorhandene Bericht wird dadurch nicht geändert. Weitere Informationen zum Speichern eines Berichts als Projekt finden Sie unter &quot;Erstellen eines Projekts aus einem leeren Projekt oder Bericht&quot;in [Erstellen von Projekten](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md).

### Erstellen eines benutzerdefinierten Unternehmensberichts {#company-report}

Benutzerdefinierte Berichte, die zur Verwendung durch andere Benutzende in Ihrem angemeldeten Unternehmen erstellt und gespeichert werden, werden als Unternehmensberichte bezeichnet. Zuvor und neu erstellte Unternehmensberichte werden wie unten dargestellt im Modal „Projekt erstellen“ aufgeführt.

So erstellen Sie einen neuen Unternehmensbericht:

1. Erstellen Sie ein Projekt in Analysis Workspace in Ihrem gewünschten Zustand.
1. Auswählen [!UICONTROL **Projekt**] > **[!UICONTROL Als Unternehmensbericht speichern...]**.

   ![Unternehmensbericht](assets/company-report.png)

1. Aktualisieren Sie den Namen des Berichts, fügen Sie eine Beschreibung hinzu, fügen Sie Tags hinzu und wählen Sie [!UICONTROL **Als Unternehmensbericht speichern**].

   Der Bericht wird zur Liste Unternehmensberichte im Modal Projekt erstellen hinzugefügt und steht Benutzern in Ihrem Anmeldeunternehmen zur Verfügung.

   Weitere Informationen dazu, wie Benutzer ein Projekt basierend auf einem Unternehmensbericht erstellen können, finden Sie unter &quot;Erstellen eines Projekts aus einem leeren Projekt oder Bericht&quot;in [Erstellen von Projekten](/help/analyze/analysis-workspace/build-workspace-project/create-projects.md).

Weitere Lernoptionen:

* Beachten Sie, dass Sie oben links in jedem Bericht, den Sie öffnen, eine 20-minütige Videoübersicht über Analysis Workspace sehen können
* Für neue Benutzer wird das Video [Trainings-Tutorial](https://www.youtube.com/watch?v=lCH1Kl1q9Wk) empfohlen, das Sie durch den Aufbau eines neuen Projekts führt.
* Hier finden Sie einen Link zur [vollständigen Dokumentation zu Analysis Workspace](/help/analyze/analysis-workspace/home.md).
* Hier finden Sie die vollständige [YouTube-Playlist für Analysis Workspace](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS).

### Verwalten von Unternehmensberichten {#manage-company-reports}

Administratoren können die Projektliste filtern, um Unternehmensberichte anzuzeigen und zu verwalten. Angeheftete Elemente bleiben angeheftet und werden von der Liste der Unternehmensberichte gefolgt, die durch das Berichtssymbol ![Berichtssymbol](https://spectrum.adobe.com/static/icons/workflow_18/Smock_FileTemplate_18_N.svg) gekennzeichnet sind. In dieser Ansicht können Sie einen oder mehrere Berichte löschen, umbenennen, taggen oder genehmigen.

Anzeigen und Verwalten von Unternehmensberichten

1. Wählen Sie in der Filterleiste **SONSTIGE FILTER** und danach **Unternehmensberichte** aus.
Eine Liste der Unternehmensberichte wird angezeigt. Alle regulären Projekte werden nicht angezeigt, es sei denn, sie sind fixiert.

   ![Anzeigen von Filtern für Unternehmensberichte](assets/company-reports-filter.png)

   Wenn Unternehmensberichte angezeigt werden, können Administrierende diese löschen, umbenennen, taggen oder genehmigen.

1. Wählen Sie in der Berichtsliste einen einzelnen Bericht oder mehrere Berichte aus.

1. Klicken Sie auf das Auslassungssymbol **...** neben einem Bericht, um die verfügbaren Optionen anzuzeigen (Löschen, Umbenennen, Taggen und Genehmigen).

   ![Aktionen für Unternehmensberichte](assets/company-reports-actions.png)

1. Wählen Sie eine Option aus (Löschen, Umbenennen, Taggen und Genehmigen).

1. Um nach Abschluss des Vorgangs zur regulären Ansicht zurückzukehren, deaktivieren Sie in der Filterleiste wieder die Option „Unternehmensberichte“.

### Löschen eines Unternehmensberichts

Administrierende können einen Bericht mithilfe der (oben beschriebenen) Option „Liste der Unternehmensberichte“ löschen oder einen Bericht aus dem Modal „Projekt erstellen“ löschen.

![Sonstige Filter](assets/delete-fr-create-project-modal.png)

### Speicherort der Vorlagen (jetzt als Berichte bezeichnet) {#templates}

| Name des Berichts (Vorlage) | Berichtsort |
| --- | --- |
| Anleitungsvideo | Beliebteste > Schulungs-Tutorial |
| Nutzung von Web-Inhalten | Interaktion > Nutzung von Web-Inhalten |
| Nutzung von Medieninhalten | Interaktion > Nutzung von Medieninhalten |
| Geräteübergreifende Analyse | Interaktion > Geräteübergreifende Analyse |
| Web-Kundenbindungsgrad | Interaktion > Web-Kundenbindungsgrad |
| Medien-Audiokonsum | Interaktion > Medien-Audiokonsum |
| Medien-Neuigkeit, -Häufigkeit, -Kundentreue | Interaktion > Medien-Neuigkeit, -Häufigkeit, -Kundentreue |
| Auswirkungen von ITP | Interaktion > ITP-Auswirkungen |
| Produktleistung | Konversion > Produkte > Produktleistung |
| Magento: Marketing und Handel | Konversion > Magento: Marketing und Handel |
| Metrik für Personen | Zielgruppe > Metrik für Personen |
| Standort-Übersicht | Zielgruppe > Besucherprofil > Standortübersicht |
| Technologieübersicht | Zielgruppe > Besucherprofil > Technologie > Technologieübersicht |
| Mobile App Usage | Zielgruppe > Mobil > Nutzung von Mobile Apps |
| Journeys für Mobile Apps | Zielgruppe > Mobil > Mobile App-Journeys |
| Mobile App-Metriken | Zielgruppe > Mobil > Mobile App-Nachrichten |
| Leistung von Mobile Apps | Zielgruppe > Mobil > Leistung von Mobile Apps |
| Beibehaltung von Mobile Apps | Zielgruppe > Mobil > Mobile App-Kundenbindung |
| Kampagnenleistung | Akquise > Kampagnen > Kampagnenleistung |
| Mobile App-Akquise | Akquise > Akquise für Mobile Apps |
| Web-Akquise | Akquise > Web-Akquise |
| Advertising Analytics: Gebührenpflichtige Suche | Akquise > Advertising Analytics: Gebührenpflichtige Suche |


## Registerkarte &quot;Lernen&quot;verwenden {#navigate-learning}

Die Lernseite enthält praktische Videoführungen, Tutorials und Links zur Dokumentation.

Auf der Lernseite in Adobe Analytics erfahren Sie mehr über Anfänger, Zwischenschritte oder erweiterte Funktionen und Anwendungsfälle in Adobe Analytics.

### Auf die Lernseite zugreifen

1. Wählen Sie in Adobe Analytics [!UICONTROL **Arbeitsbereich**] > [!UICONTROL **Lernen**].

### Funktionen von Lernseiten

* **Inhalt filtern:** Mit dem Filtersymbol in der linken Leiste können Sie Lerninhalte nach Erlebnisebene (Starter, Intermediate oder Erweitert) und nach Inhaltstyp (Dokument, Video oder Tours &amp; Tutorials) filtern.
* **Fortschritt verfolgen:** Nachdem Sie ein Inhaltselement ausgewählt haben, wird ein **[!UICONTROL Angezeigt]** -Tag angezeigt. Mit diesem Tag können Sie Ihren Fortschritt durch den Lerninhalt verfolgen. Sie können die **[!UICONTROL Angezeigt]** -Tag, um es aus einem Inhaltselement zu entfernen.
* **Zusätzliche Inhalte anzeigen:** Wählen Sie beim Anzeigen eines Videos die **[!UICONTROL Weitere Infos]** -Schaltfläche, um zugehörige Dokumentationsinhalte auf der Experience League anzuzeigen. Wählen Sie auf der Seite Lernen eine der folgenden Optionen aus, um weitere Inhalte anzuzeigen:
   * **[!UICONTROL Besuchen Sie YouTube]:** Zeigen Sie die vollständige Analysis Workspace YouTube-Playlist an.
   * [!UICONTROL **Experience League des Besuchs**]: Zeigen Sie die vollständige Adobe Analytics-Dokumentation zur Experience League an.
* **Grundlagen für neue Benutzer:** Die [!UICONTROL Workspace-Grundlagen] Diese Tour wird für neue Benutzer empfohlen. Diese Tour führt Sie direkt zu Workspace und führt Sie durch die gängigsten Aktionen. Diese Tour kann auch jederzeit in Workspace über das QuickInfo-Pop-over in der Bedienfeldkopfzeile neu gestartet werden.

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
| Werden meine aktuellen [!DNL Reports & Analytics]-Favoriten übernommen? | Nein, sie werden NICHT übernommen. Alle [!UICONTROL Arbeitsbereich]-Projekt-Favoriten werden jedoch übernommen. |
| Gibt es eine maximale Anzahl von Projekten, die ich anheften kann? | Nein, es gibt keine Begrenzung für die Anzahl der Projekte, die Sie anheften können. |
| Können Administratoren diese neue Landingpage für ihre Benutzer festlegen? | Nein, Administratoren können die neue Landingpage nicht im Namen von Benutzern festlegen. Die einzelnen Benutzer müssen den Umschalter selbst aktivieren. |
| Sind alle Berichte, die derzeit in [!DNL Reports & Analytics] vorhanden sind, weiterhin verfügbar? | Nein, die folgenden Berichte wurden auf der Grundlage der allgemeinen Nutzungsdaten schrittweise eingestellt: <ul><li>Alle benutzerdefinierten eVars/Eigenschaften/Ereignisse/Klassifizierungen<li>Meine empfohlenen Berichte</li><li>Unique Visitors pro Tag, Woche, Monat, Quartal und Jahr</li><li>Unique Customers pro Woche/Monat/Quartal/Jahr</li><li>Tiefe des Aktionsnamens</li><li>Zusammenfassung des Aktionsnamens</li><li>Dashboard hinzufügen</li><li>Alter</li><li>Audio-Unterstützung</li><li>Rechnungsinformationen</li><li>Klicks pro Seite</li><li>Farbtiefe</li><li>Cookie-Unterstützung</li><li>Cookies</li><li>Verbindungstypen</li><li>Kreative Elemente</li><li>Kreditkartenart</li><li>Crossselling</li><li>Benutzerdefinierte Ereignistrichter</li><li>Benutzerspezifische Links</li><li>Kunden-ID</li><li>Wochentag</li><li>Name der Einstiegsaktion</li><li>Name der Ausstiegsaktion</li><li>Ausstiegs-Links</li><li>Fallout</li><li>Datei-Downloads</li><li>Suche im Geschäft</li><li>Vollständige Pfade</li><li>Geschlecht</li><li>VISTA-Regel für Treffertyp</li><li>Bildunterstützung</li><li>Java</li><li>JavaScript</li><li>JavaScript-Version </li><li>Lesezeichen verwalten</li><li>Dashboards verwalten</li><li>Farbtiefe des Bildschirms</li><li>Auflösung des Bildschirms</li><li>Newsletter-Anmeldungen</li><li>Name der nächsten Aktion</li><li>Fluss für Name der nächsten Aktion</li><li>Null-Suchen</li><li>Betriebssystem</li><li>Bestellübersicht</li><li>Seite des Tages</li><li>Nicht gefundene Seiten</li><li>PathFinder</li><li>Pfadlänge</li><li>Name der vorherigen Aktion</li><li>Fluss für Name der vorherigen Aktion</li><li>Produktaktivität</li><li>Produktkosten</li><li>Produktabteilung</li><li>Produktinventarkategorie</li><li>Produktname</li><li>Produktbewertungen</li><li>Produktsaison</li><li>Produktfreigaben</li><li>Produktvergrößerungen</li><li>Neu laden</li><li>Suchvorgänge</li><li>Server</li><li>Einzelseitenbesuche</li><li>Versandinformationen</li><li>Site-Hierarchie</li><li>Erwähnungen in Social Media</li><li>Tageszeit</li><li>Verbrachte Zeit für Aktionsname</li><li>Video-Unterstützung</li><li>Besucherstatus</li></ul> |
