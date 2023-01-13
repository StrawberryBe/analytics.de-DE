---
description: Erläutert die neue Landingpage, die Analysis Workspace und Reports & Analytics in einer Benutzeroberfläche zusammenfasst und so einen zentralen Zugriffspunkt (Workspace) bietet.
title: Neue Landingpage von Adobe Analytics
role: User, Admin
feature: Analytics Basics
exl-id: 0a2fb778-491a-4dc3-aae4-afadb3ab1a1e
source-git-commit: 3be2db90220c7e54abf96e47a9ac8658bbd066cc
workflow-type: tm+mt
source-wordcount: '3727'
ht-degree: 79%

---

# Neue Landingpage von Adobe Analytics

Die Landingpage für Adobe Analytics vereint sowohl [!DNL Analysis Workspace] als auch [!DNL Reports & Analytics] in einer einzigen Oberfläche und einem Zugangspunkt unter dem Dach von [!DNL Workspace]. Sie enthält eine neue Startseite für den Projekt-Manager, ein aktualisiertes Berichtsmenü und aktualisierte Berichte sowie einen Lernbereich, der Ihnen dabei hilft, die ersten Schritte effektiver zu bewältigen. Im Folgenden finden Sie eine Videoübersicht:

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
| **[!UICONTROL Projekt erstellen]** modal is back | Wenn Sie auf **[!UICONTROL Projekt erstellen]** In Workspace haben Sie erneut die Wahl zwischen einem [!UICONTROL Leeres Projekt] und [!UICONTROL Leere mobile Scorecard]. Sie können auch aus beliebigen Vorlagen wählen, die Ihr Unternehmen erstellt hat. | ![Neu erstellen](assets/create-new.png) |
| Auch in Customer Journey Analytics verfügbar | Diese Landingpage in geänderter Form ist auch in CJA verfügbar. |  |

{style=&quot;table-layout:auto&quot;}

## Oberste Menüstruktur {#top-menu}

![Menü oben](assets/top-menus.png)

* Top-Analytics-Menü: Die meisten Berichte befinden sich nun im Menü [!UICONTROL Berichte] in der linken Leiste.
* Die linke Leiste verfügt über drei Registerkarten: [!UICONTROL Projekte], [!UICONTROL Berichte] und [!UICONTROL Lernen].

### Terminologie

* **[!UICONTROL Projekte]** sind angepasste Entwürfe, die von Ihnen erstellte Datenkomponenten, Tabellen und Visualisierungen oder die von einer anderen Person für Sie erstellt und freigegeben wurden. [!UICONTROL Projekte] beziehen sich auch auf leere Projekte und leere mobile Scorecards.
* **[!UICONTROL Berichte]** beziehen sich auf alles, was von Adobe vorkonfiguriert wurde, z. B. Berichte in Reports &amp; Analytics und Vorlagen im Arbeitsbereich.
* **[!UICONTROL Vorlagen]** werden nicht mehr als Begriff für die vordefinierten Arbeitsbereich-Projekte von Adobe verwendet. Sie befinden sich nun unter [!UICONTROL Berichte]. Der Begriff [!UICONTROL Vorlagen] wird weiterhin für Vorlagen verwendet, die Ihr Unternehmen erstellt hat.

## Navigieren Sie zur Registerkarte [!UICONTROL Projekte] {#navigate-projects}

[!UICONTROL Projekte] fungieren als Startseite von [!UICONTROL Arbeitsbereich]. Auf der Registerkarte Projekte werden der Ordner Firma, alle von Ihnen erstellten persönlichen Ordner, Ihre Projekte und Mobile Scorecards angezeigt. Auf dieser Seite können Sie Ordner, Projekte und mobile Scorecards anzeigen, erstellen und ändern. Weitere Informationen finden Sie unter [Über Ordner in Analytics](/help/analyze/analysis-workspace/build-workspace-project/workspace-folders/about-folders.md).

![Landing (alle)](assets/landing-all2.png)

>[!NOTE]
>
>Einige der folgenden Einstellungen bleiben während der Sitzung und sitzungsübergreifend bestehen. Beispielsweise die ausgewählte Registerkarte, die ausgewählten Filter, die ausgewählten Spalten und die Sortierrichtung der Spalte. Suchergebnisse sind nicht persistent.

| UI-Element | Definition |
| --- | --- |
| Voreinstellungen bearbeiten | Ermöglicht es Ihnen, [!UICONTROL Tutorials anzuzeigen] und [Benutzereinstellungen zu bearbeiten](/help/analyze/analysis-workspace/user-preferences.md). |
| [!UICONTROL Neu erstellen] | Öffnet das Projekt-Modal, in dem Sie ein Workspace-Projekt oder eine mobile Scorecard erstellen oder eine Unternehmensvorlage öffnen können. |
| [!UICONTROL Weniger anzeigen<br> Mehr anzeigen] | Blendet das Banner ein oder aus: ![Oberes Banner](assets/top-banner.png) |
| [!UICONTROL Arbeitsbereich-Projekt] | Erstellt eine leere [Workspace-Projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) für Sie zu entwerfen und zu erstellen. |
| [!UICONTROL Mobile Scorecard] | Erstellt eine leere [mobile Scorecard](https://experienceleague.adobe.com/docs/analytics/analyze/mobapp/curator.html?lang=de) für Sie zu entwerfen und zu erstellen. |
| [!UICONTROL Schulungs-Tutorial öffnen] | Öffnet das Workspace-Tutorial, das Sie durch den Prozess der Erstellung eines neuen Einstiegsprojekts in einem Schritt-für-Schritt-Tutorial führt. |
| [!UICONTROL Versionshinweise öffnen] | Öffnet den Abschnitt „Adobe Analytics“ der neuesten Versionshinweise zu Adobe Experience Cloud. |
| Filtersymbol | Filter nach Tags, Report Suites, Inhabern, Typen und anderen Filtern (Meine, Für mich freigegeben, Favoriten und Genehmigt) |
| Suchleiste | Durchsucht alle Spalten in der Tabelle. |
| Auswahlfeld | Wählt ein oder mehrere Projekte aus, um die Projektverwaltungsaktionen anzuzeigen, die Sie ausführen können: **Löschen**, **Freigeben**, **Umbenennen**, **Kopieren**, **Aufheben**, **Nach oben**, **Nach unten**, **Tag**, **Genehmigen**, **CSV exportieren** und **Verschieben nach**. Sie sind möglicherweise nicht berechtigt, alle aufgelisteten Aktionen durchzuführen. |
| [!UICONTROL Favoriten] | Fügt einen Stern neben einem Lieblingsprojekt oder -ordner hinzu, der als Filter verwendet werden kann. |
| [!UICONTROL Name] | Identifiziert den Namen des Projekts. |
| Anheften-Symbol | Löst Elemente so ein, dass sie immer oben in der Liste angezeigt werden. Sie können die Reihenfolge jedoch neu anpassen, indem Sie sie in der Reihenfolge nach oben oder unten verschieben. Verwenden Sie das Optionsmenü mit Auslassungspunkten und wählen Sie **Nach oben** oder **Nach unten** in der Liste. |
| Infosymbol (i) | Zeigt die folgenden Informationen zu einem Projekt an: Typ, Projektrolle, Eigentümer, Beschreibung und für wen sie freigegeben ist. Es zeigt auch an, wer dieses Projekt [bearbeiten oder duplizieren](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/share-projects.html?lang=de) kann. |
| Auslassungspunkte (...) | Zeigt die Projektverwaltungsaktionen an, die Sie ausführen können: **Löschen**, **Freigeben**, **Umbenennen**, **Kopieren**, **Aufheben**, **Nach oben**, **Nach unten**, **Tag**, **Genehmigen**, **CSV exportieren** und **Verschieben nach**. Sie sind möglicherweise nicht berechtigt, alle aufgelisteten Aktionen durchzuführen. |
| [!UICONTROL Typ] | Gibt an, ob es sich bei diesem Typ um ein Workspace-Projekt, eine mobile Scorecard oder einen Ordner handelt. |
| [!UICONTROL Tags] | Taggt Projekte, um sie in Gruppen zu organisieren. |
| [!UICONTROL Projektrolle] | Identifiziert die Projektrollen: ob Sie Projekteigentümer sind und über Berechtigungen zum Bearbeiten oder Duplizieren des Projekts verfügen. |
| [!UICONTROL Report Suite] | Identifiziert die Report Suites, die mit dem Projekt verknüpft sind.<br>Tabellen und Visualisierungen innerhalb eines Bedienfelds leiten Daten von der Report Suite ab, die oben rechts im Bedienfeld ausgewählt wurde. Von der Report Suite hängt auch ab, welche Komponenten in der linken Leiste verfügbar sind. In einem Projekt können Sie je nach Anwendungsfällen Ihrer Analyse eine oder viele Report Suites verwenden. Die Liste der Report Suites ist nach Relevanz sortiert. Adobe definiert die Relevanz anhand der Häufigkeit der kürzlichen Verwendung der Suite durch den aktuellen Benutzer und der Häufigkeit der Verwendung der Suite innerhalb des Unternehmens. |
| [!UICONTROL Inhaber] | Identifiziert die Person, die das Projekt erstellt hat. |
| [!UICONTROL Zuletzt geöffnet] | Identifiziert das Datum, an dem Sie das Projekt zuletzt geöffnet haben. |
| Symbol „Tabelle anpassen“ | Auswahl der Spalten, die in der Tabelle angezeigt werden sollen. Um Spalten aus der Projektliste hinzuzufügen oder daraus zu entfernen, klicken Sie auf das Spaltensymbol (![Landing all](/help/analyze/assets/select-column.png) ) oben rechts klicken und dann Spaltentitel auswählen oder deaktivieren. |
| SHOW: Ordner und Projekte oder Alle Projekte | Ändert die Anzeigeeinstellung auf der Tabelle, sodass Ordner und Projekte entsprechend Ihrer Ordnerorganisation angezeigt werden **oder** alle Projekte in einer unorganisierten Liste anzeigen. |
| &lt; (Schaltfläche „Zurück“) | Gibt Sie zur neuesten Landingpage-Konfiguration in einem Workspace-Projekt oder einem Bericht zurück. Die Seitenkonfiguration, die Sie beim Verlassen der Landingpage vorgenommen haben, bleibt bestehen, wenn Sie zurückkehren. |

### Veraltete Seite des Projekt-Managers {#deprecate-pm-page}

Mit der Veröffentlichung der neuen Landingpage haben wir den Projekt-Manager eingestellt, der unter dem Komponenten-Manager aufgeführt ist. Die neue Landingpage verarbeitet alle Funktionen der alten Seite &quot;Projektmanager&quot;und mehr.

Ein gängiger Anwendungsfall für die Seite &quot;Projektmanager&quot;war die Ansicht aller Ihrer Projekte. Um mithilfe der Filterleiste alle Ihre Projekte auf der neuen Landingpage anzuzeigen, wählen Sie **SONSTIGE FILTER** und wählen Sie **Alle anzeigen**.

![Sonstige Filter](assets/other-filters.png)

Wenn Sie sich in der Ansicht &quot;Ordner &amp; Projekte&quot;befinden, wird ein modales Popup angezeigt, in dem Sie gefragt werden, ob Sie zur Ansicht &quot;Alle Projekte&quot;wechseln möchten. Dies erleichtert die Anzeige aller Ihrer Projekte außerhalb der Ordner, in denen sie möglicherweise organisiert sind.   Auswählen **Zur Ansicht &quot;Alle Projekte&quot;wechseln** , um alle Projekte, auf die Sie Zugriff haben, besser anzuzeigen.

![Alle Projekte wechseln](assets/switch-all-projects-view.png)

## Navigieren durch die Registerkarte [!UICONTROL Berichte] {#navigate-reports}

Die Registerkarte [!UICONTROL Berichte] fasst drei Berichtssätze zusammen:

* Die vordefinierten [!UICONTROL Arbeitsbereich]-Vorlagen, die sich zuvor unter [!UICONTROL Arbeitsbereich] > [!UICONTROL Projekt] > [!UICONTROL Neu] befanden. Adobe verwendet in diesem Zusammenhang nicht mehr das Wort „Vorlage“.
* Die meisten vordefinierten Berichte befanden sich zuvor in Adobe Analytics im oberen Menü [!UICONTROL Berichte]. Diese Berichte werden jetzt in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) angezeigt.

>[!IMPORTANT]
>
>Unter „Berichte“ wird der Ordner „Favoriten“ nur angezeigt, wenn Sie einen neuen Bericht als Favoriten markieren. Es werden keine bereits vorhandenen Reports &amp; Analytics-Favoriten übernommen.

![Registerkarte „Berichte“](assets/reports-tab2.png)

Wie bereits erwähnt, sind hier nur die am häufigsten verwendeten Berichte verfügbar, die zuvor in Reports &amp; Analytics gruppiert waren. Einige wenige selten verwendete oder nicht mehr relevante Berichte wurden nicht migriert. Weitere Informationen finden Sie in den FAQ unten.

### Menüs und Untermenüs {#menus}

Dies sind die Menüs und ihre Untermenüs. Wenn Sie einen bestimmten Bericht nicht finden können, führen Sie eine „Suche auf Seite“ durch, um ihn zu finden.

| Menüelement | Berichte unter diesem Menüelement |
| --- | --- |
| **[!UICONTROL Beliebteste]** | <ul><li>Schulungs-Tutorial (Vorhandene Vorlage für Arbeitsbereich)</li><li>Seiten (Was sind meine Top-Seiten?)</li><li>Seitenansichten (Wie viele Seitenaufrufe erzeuge ich?)</li><li>Besuche (Wie viele Besuche erhalte ich?)</li><li>Besucher (Wie viele Besucher bekomme ich?)</li><li>Schlüsselmetriken (Wie sehen meine wichtigsten Kennzahlen aus?)</li><li>Site-Bereiche (Welche Bereiche meiner Site generierten die meisten Seitenansichten?</li><li>Nächste Seite (Auf welche Seiten gehen meine Besucher als Nächstes?)</li><li>Vorherige Seite (Welche vorherigen Seiten haben meine Besucher aufgerufen?)</li><li>Kampagnen (Welche Kampagnen liegen meinen Schlüsselmetriken zugrunde?)</li><li>Produkte (Welche Produkte liegen meinen Schlüsselmetriken zugrunde?)</li><li>Letztkontakt-Kanal (Welcher Letztkontakt-Kanal erzielt die beste Leistung?)</li><li>Letztkontakt-Kanaldetail (Welcher spezifische Letztkontakt-Kanal ist leistungsstärker als andere?)</li><li>Umsatz (Wie entwickelt sich mein Umsatz?)</li><li>Bestellungen (Wie entwickeln sich meine Bestellungen?)</li><li>Einheiten (Wie viele Einheiten verkaufe ich?)</li></ul> |
| **[!UICONTROL Interaktion]** | <ul><li>Schlüsselmetriken (Wie sehen meine wichtigsten Kennzahlen aus?)</li><li>Seitenansichten (Wie viele Seitenaufrufe erzeuge ich?)</li><li>Seiten (Was sind meine Top-Seiten?)</li><li>Besuche (Wie viele Besuche erhalte ich?)</li><li>Besucher (Wie viele Besucher bekomme ich?)</li><li>Zeit pro Besuch (Wie viel Zeit verbringen meine Benutzer pro Besuch?)</li><li>Zeit vor Ereignis (Wie viel Zeit verbringen meine Benutzer vor einem Erfolgsereignis?)</li><li>Site-Bereiche (Welche Bereiche meiner Site generierten die meisten Seitenansichten?</li><li>Nutzung von Web-Inhalten (Welche Inhalte werden am häufigsten genutzt und sind für Benutzer interessant?)</li><li>Nutzung von Medieninhalten (Welche Inhalte werden am häufigsten genutzt und sind für Benutzer interessant?)</li><li>Fluss zur nächsten/vorherigen Seite (Was sind/waren die nächsten/vorherigen Pfade, die meine Besucher nutzen/genutzt haben?)</li><li>Fallout (Wo sehe ich Fallout für meine digitalen Eigenschaften?)</li><li>Geräteübergreifende Analyse (Verwendung geräteübergreifender Analysen in Analysis Workspace)</li><li>Web-Bindungsgrad (Wer sind meine treuen Benutzer und was tun sie?)</li><li>Medien-Audiokonsum (Was sind Trends und Top-Metriken beim Audiokonsum?)</li><li>Medien-Neuigkeit, -Häufigkeit, -Treue (Wer sind meine treuen Leser?)</li><li>Seitenanalyse > Neuladungen (Welche Seiten werden am häufigsten neu geladen?)</li><li>Seitenanalyse > Besuchszeit pro Seite (Wie viel Zeit verbringen meine Benutzer auf meinen Seiten?)</li><li>Einstiege und Ausstiege > Einstiegsseiten (Was sind meine Top-Einstiegsseiten?)</li><li>Einstiege und Ausstiege > Ursprüngliche Einstiegsseiten (Auf welcher Seite ist mein Besucher ursprünglich eingetreten?)</li><li>Einstiege und Ausstiege > Einzelseitenbesuche (Welche Seiten haben die meisten Einzelseitenbesuche generiert?)</li><li>Einstiege und Ausstiege > Ausstiegseiten (Was sind meine Top-Ausstiegsseiten?)</li></ul> |
| **[!UICONTROL Konversion]** | <ul><li>Produkte > Produkte (Welche Produkte liegen meinen Schlüsselmetriken zugrunde?)</li><li>Produkte > Produktleistung (Welche Produkte schneiden am besten ab?)</li><li>Produkte > Kategorien (Was sind meine leistungsstärksten Produktkategorien?)</li><li>Warenkorb > Warenkörbe (Wie viele Benutzer haben ein Produkt zum Warenkorb hinzugefügt?)</li><li>Warenkorb > Warenkorbansichten (Wie oft haben meine Besucher ihren Warenkorb angesehen?)</li><li>Warenkorb > Zusatz zum Warenkorb (Wie oft fügen Benutzer ihrem Warenkorb ein Produkt hinzu?)</li><li>Warenkorb > Entnahme aus Warenkorb (Wie oft entfernen Benutzer ein Produkt aus ihrem Warenkorb?)</li><li>Einkäufe > Umsatz (Wie sieht mein Umsatz aus?)</li><li>Einkäufe > Bestellungen (Wie sehen meine Bestellungen aus?)</li><li>Käufe > Einheiten (Wie viele Einheiten verkaufe ich?)</li><li>[Magento: Marketing und Commerce](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#commerce)</li></ul> |
| **[!UICONTROL Zielgruppe]** | <ul><li>Personenmetrik (Wie viele Personen interagieren mit meiner Marke?)</li><li>Besucherprofil > Standortübersicht (Welche Standorte werden von Benutzern am meisten genutzt?)</li><li>Besucherprofil > GeoSegmentation > Geo-Länder, Geo-US-Bundesstaaten, Geo-Regionen, Geo-Städte, Geo-US-DMA (Aus welchen Regionen besuchen mich meine Benutzer?)</li><li>Besucherprofil > Sprachen (Welche Sprache bevorzugen meine Benutzer?)</li><li>Besucherprofil > Zeitzonen (Aus welchen Zeitzonen kommen meine Benutzer?)</li><li>Besucherprofil > Domains (Welche ISPs werden von meinen Besuchern verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Domains auf oberster Ebene (Welche Domains leiten den Traffic zu meiner Site?)</li><li>Besucherprofil > Technologie > Technologieübersicht (Welche Technologien werden verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Technologie > Browser, Browser-Typ, Browser-Breite, Browser-Höhe (welcher Browser, welche Browser-Version des Unternehmens und welche Breite und Höhe werden von Benutzern verwendet, um auf meine Site zuzugreifen?)</li><li>Besucherprofil > Technologie > Betriebssystem, Betriebssystemtypen (Welches Betriebssystem und welche Version davon verwenden meine Besucher?)</li><li>Besucherprofil > Technologie > Mobilnetzbetreiber (Welche Mobilnetzbetreiber verwenden meine Besucher, um auf meine Site zuzugreifen?)</li><li>Besuchertreue > Rückkehrhäufigkeit (Wie viel Zeit vergeht zwischen dem aktuellen Besuch meines Benutzers und vorherigen Besuchen?)</li><li>Besuchertreue > Erneute Besuche (Wie viele meiner Besucher kehren zurück?)</li><li>Besuchertreue > Besuchsnummer (Welcher Besuchsnummernbehälter liegt den meisten meiner Schlüsselmetriken zugrunde?)</li><li>Besucherbindung > Verkaufszyklus > Kundentreue (Zu welchem Treuesegment gehören meine Benutzer?)</li><li>Besucherbindung > Verkaufszyklus > Tage bis Erstkauf (Wie viele Tage sind zwischen dem ersten Besuch meiner Benutzer und dem ersten Kauf vergangen?)</li><li>Besucherbindung > Verkaufszyklus > Tage seit letztem Kauf (Wie viele Tage sind zwischen dem aktuellen Besuch meiner Benutzer und ihrem letzten Kauf vergangen? )</li><li>Besuchertreue > Mobile > Geräte und Gerätetypen (Welche Geräte und Gerätetypen verwenden meine Besucher?)</li><li>Besucherbindung > Mobile > Hersteller (Welchen Mobilgerätehersteller verwenden meine Besucher?)</li><li>Besuchertreue > Mobile > Bildschirmgröße, Bildschirmhöhe, Bildschirmbreite (Welche Bildschirmgröße/-höhe/-breite für Mobilgeräte verwenden meine Besucher?)</li><li>Besucherbindung > Mobile > [Mobile-App-Nutzung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Journey](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Metriken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Mobile-App-Nachrichten](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besuchertreue > Mobile > [Leistung von Mobile Apps](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>Besucherbindung > Mobile > [Bindung durch Mobile Apps](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li></ul> |
| **[!UICONTROL Akquise]** | <ul><li>Marketing-Kanäle > Erstkontakt-Kanal, Details zum Erstkontakt-Kanal (Welcher Erstkontakt-Kanal und welcher spezifische Erstkontakt-Kanal schneidet am besten ab?)</li><li>Marketing-Kanäle > Erster letzter Kanal, Details des ersten letzten Kanals (Welcher Letztkontakt-Kanal und welcher spezifische Letztkontakt-Kanal schneidet am besten ab?)</li><li>Kampagnen > Kampagnen (Welche Kampagnen liegen meinen Schlüsselmetriken zugrunde?)</li><li>Kampagnen > Kampagnenleistung (Welche Kampagnen erzielen den höchsten Umsatz?)</li><li>Kampagnen > Trackingcode (Welche Kampagnen-Trackingcodes erzielen die besten Ergebnisse?)</li><li>[Web-Akquise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#web)</li><li>[Mobile-Akquise](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#mobile)</li><li>[Advertising Analytics: Paid Search](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/starter-projects.html?lang=de#advertising)</li><li>Suchbegriffe – alle, gebührenpflichtig, kostenlos (Welche Suchbegriffe und gebührenpflichtigen/kostenlosen Suchbegriffe bringen meine Schlüsselmetriken am besten voran?)</li><li>Suchmaschinen – alle, gebührenpflichtig, kostenlos (Welche Suchmaschinen und gebührenpflichtigen/kostenlosen Suchmaschinen bringen meine Schlüsselmetriken am besten voran?)</li><li>Ranking aller Suchseiten (Von welcher Suchseite aus besuchen mich meine Benutzer?)</li><li>Verweisende Domains (Von welchen Domains kommt der Traffic auf meine Seite?)</li><li>Ursprüngliche verweisende Domain (Was waren die ersten Domains, auf denen sich Benutzer vor dem Besuch meiner Site befanden?)</li><li>Referrer (Auf welchen URLs waren meine Benutzer, bevor sie sich zu meiner Website durchgeklickt haben?)</li><li>Referrer-Typen (Zu welcher Kategorie gehören die auf mich verweisenden URLs?)</li></ul> |

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

### Verwenden der Registerkarte „Berichte“ {#use-reports}

Aktuelle Benutzer von Reports &amp; Analytics finden hier einen kurzen Einstieg in die Verwendung der Berichte, die sie kennen und die jetzt in Arbeitsbereich angezeigt werden. Berichte verhalten sich wie vorhandene Vorlagen: Wenn Sie Änderungen daran vornehmen, werden Sie aufgefordert, Ihre Änderungen zu speichern/zu verwerfen, wenn Sie weg navigieren oder zu einem anderen Bericht gehen. Wenn Sie Änderungen speichern möchten, wird der Bericht als neues Projekt gespeichert.

1. Navigieren Sie zur Registerkarte [!UICONTROL Berichte]
1. Wählen Sie den Bericht, den Sie anzeigen möchten, beispielsweise wählen Sie unter [!UICONTROL Am beliebtesten] den Bericht [!UICONTROL Seiten] aus.
1. Klicken Sie rechts auf **[!UICONTROL Bericht öffnen]**.

   ![Bericht zu Seiten](assets/pages-report.png)

1. Der Seitenbericht, wie in Analysis Workspace angezeigt, zeigt zwei [Visualisierungen](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md) ([Balkendiagramm](/help/analyze/analysis-workspace/visualizations/bar.md) und [Zusammenfassungsnummer](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)) und eine [Freiformtabelle](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) an. Die verwendete Metrik ist „Vorkommen“.
1. Von hier aus haben Sie mehrere Optionen. Im Folgenden finden Sie einige dieser Optionen:

   * Sie können den Bericht unverändert verwenden.
   * Sie können ein oder mehrere Segmente in die Dropzone „Segment“ oben ziehen. Ziehen Sie beispielsweise das Segment [!UICONTROL Mobile Kunden] und sehen Sie sich die Ergebnisse an.
   * Sie können den Datumsbereich ändern, indem Sie oben rechts in den Kalender wechseln.
   * Sie können Dimensionsaufschlüsselungen hinzufügen, andere Metriken einfügen und den Bericht allgemein beliebig anpassen.

### Benutzerdefinierten Unternehmensbericht erstellen {#company-report}

Benutzerdefinierte Berichte, die zur Verwendung durch andere Benutzer in Ihrem Anmeldeunternehmen erstellt und gespeichert werden, werden als Unternehmensberichte bezeichnet. Zuvor erstellte Unternehmensberichte und neu erstellte Unternehmensberichte werden im Modal Projekt erstellen aufgeführt, wie unten dargestellt.

So erstellen Sie einen neuen Unternehmensbericht:

1. Erstellen Sie den Arbeitsbereich für Ihren gewünschten Status.
1. Öffnen Sie das Menü [!UICONTROL Projekt] und klicken Sie auf **[!UICONTROL Als Unternehmensbericht speichern...]**.

   ![Unternehmensbericht](assets/company-report.png)

1. Fügen Sie alle gewünschten Felder zum Modal hinzu und speichern Sie es.

   Der Bericht wird zur Liste Unternehmensberichte im Modal Projekt erstellen hinzugefügt und steht denjenigen in Ihrem Anmeldeunternehmen zur Verfügung.

Weitere Lernoptionen:

* Beachten Sie, dass Sie oben links in jedem Bericht, den Sie öffnen, eine 20-minütige Videoübersicht über Analysis Workspace sehen können
* Für neue Benutzer wird das Video [Trainings-Tutorial](https://www.youtube.com/watch?v=lCH1Kl1q9Wk) empfohlen, das Sie durch den Aufbau eines neuen Projekts führt.
* Hier finden Sie einen Link zur [vollständigen Dokumentation zu Analysis Workspace](/help/analyze/analysis-workspace/home.md).
* Hier finden Sie die vollständige [YouTube-Playlist für Analysis Workspace](https://www.youtube.com/playlist?list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS).

## Navigieren Sie zur Registerkarte „Lernen“. {#navigate-learning}

Die Seite „Lernen“ enthält praktische Videoführungen und -Tutorials sowie Links zur Dokumentation.

* Die Tour [!UICONTROL Arbeitsbereich-Grundlagen] führt Sie direkt zu Arbeitsbereich und zeigt Ihnen das Arbeitsbereich-Layout und wo Sie die häufigsten Aktionen finden/durchführen können. Diese Tour kann auch jederzeit direkt in Arbeitsbereich über das QuickInfo-Pop-over in der Kopfzeile des Bedienfelds neu gestartet werden.
* Durch Klicken auf ein Video/eine Tour wird ein Tag **[!UICONTROL Angezeigt]** hinzugefügt. Mit diesem Tag können Sie Ihren Fortschritt durch den Lerninhalt verfolgen. Sie können auf das Tag klicken und es wird ausgeblendet, falls Sie den Inhalt noch nicht abgeschlossen haben.
* Die Schaltfläche **[!UICONTROL Weitere Informationen]** im Video-Modal bietet Zugriff auf eine Adobe Experience League-Dokumentationsseite mit weiteren Hilfeinhalten zu dem Video, das Sie gerade angesehen haben.  **[!UICONTROL Weitere Videos anzeigen]** führt Sie zur vollständigen YouTube-Playlist für Analysis Workspace.

## Landingpage festlegen {#set-landing}

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
