---
description: Anweisungen zum Einrichten von Scorecards für die Dashboards.
title: Kuratorleitfaden für Adobe Analytics-Dashboards
translation-type: ht
source-git-commit: 27a923ec3acb9a0343ba71e395e565a0f9ede251
workflow-type: ht
source-wordcount: '2380'
ht-degree: 100%

---


# Kuratorleitfaden für Adobe Analytics-Dashboards

Die folgenden Informationen liefern Kuratoren von Adobe Analytics-Daten Informationen dazu, wie Dashboards für ausführende Benutzer konfiguriert und dargestellt werden. Ein Video zur Verdeutlichung dieser Informationen finden Sie in den Adobe Analytics-Dashboards unter dem Namen Scorecard Builder-Video:

>[!VIDEO](https://video.tv.adobe.com/v/34544?captions=ger)

## Einführung

Adobe Analytics-Dashboards bieten jederzeit und überall Erkenntnisse aus Adobe Analytics. Die Mobile App bietet Benutzern auf Mobilgeräten Zugriff auf intuitive Scorecards, die Sie über die Desktop-Benutzeroberfläche von Adobe Analytics erstellen und freigeben. Scorecards sind eine Sammlung von Schlüsselmetriken und anderen Komponenten, die in einem gekachelten Layout dargestellt werden. Sie können auf eine Scorecard tippen, um detailliertere Aufschlüsselungen und Trendberichte zu erhalten. Sie können Scorecards entsprechend den für Sie wichtigsten Daten anpassen. Analytics-Dashboards werden sowohl unter iOS- als auch Android-Betriebssystemen unterstützt.

## Weitere Informationen zu diesem Handbuch

Dieses Handbuch soll Kuratoren von Adobe Analytics-Daten bei der Konfiguration von Scorecards für ausführende Benutzer in den Dashboards unterstützen. Kuratoren können organisatorische Administratoren oder Personen in anderen Rollen sein, die für die Einrichtung von App-Scorecards zuständig sind. Diese ermöglichen es ausführenden Benutzern, eine umfassende Darstellung wichtiger Zusammenfassungsdaten schnell und einfach auf ihren eigenen Mobilgeräten anzuzeigen. Obwohl ausführende Benutzer die Endbenutzer der Analytics-Dashboards sind, hilft dieses Handbuch Datenkuratoren bei der effektiven Einrichtung der App für diese Benutzer.

## Glossar

In der folgenden Tabelle werden Begriffe zum Verständnis von Zielgruppe, Funktionen und Verwendung der Analytics-Dashboards beschrieben.

| Begriff | Definition |
|--- |--- |
| Verbraucher | Ausführende Person, die wichtige Schlüsselmetriken und Einblicke aus Analytics auf einem Mobilgerät anzeigt |
| Kurator | Person, die mit der Datenerfassung und -auswertung vertraut ist, Einblicke in Analytics erkennt und verteilt und die Scorecards konfiguriert, die von Verbrauchern angezeigt werden |
| Kuratierung | Der Vorgang der Erstellung oder Bearbeitung einer mobilen Scorecard mit relevanten Metriken, Dimensionen und anderen Komponenten für den Verbraucher |
| Scorecard | Eine Ansicht der Dashboards mit einer oder mehreren Kacheln |
| Kachel | Wiedergabe einer Metrik in einer Scorecard-Ansicht |
| Aufschlüsselung | Eine sekundäre Ansicht, die durch Tippen auf eine Kachel in der Scorecard zugänglich ist. Diese Ansicht erweitert die auf der Kachel dargestellte Metrik und zeigt optional Informationen über zusätzliche Aufschlüsselungsdimensionen an |
| Datumsbereich | Der primäre Datumsbereich für die Berichterstellung über die Dashboards |
| Vergleichsdatumsbereich | Der Datumsbereich, der mit dem primären Datumsbereich verglichen wird |

## Scorecard für ausführende Benutzer erstellen

Eine Scorecard stellt wie nachfolgend gezeigt wichtige Datenvisualisierungen für ausführende Benutzer in einem gekachelten Layout bereit:

![Beispiel-Scorecard](assets/intro_scorecard.png)

Als Kurator dieser Scorecard können Sie mit dem Scorecard Builder konfigurieren, welche Kacheln auf der Scorecard für den Verbraucher angezeigt werden. Sie können auch konfigurieren, wie die detaillierten Ansichten oder Aufschlüsselungen angepasst werden können, sobald auf die Kacheln getippt wird. Hier sehen Sie die Scorecard Builder-Oberfläche:

![Scorecard Builder](assets/scorecard_builder.png)

Zur Erstellung der Scorecard führen Sie folgende Schritte aus:

1. Zugriff auf die Vorlage für [!UICONTROL leere mobile Scorecards].
2. Konfigurieren Sie die Scorecard mit Daten und speichern Sie sie.

### Zugriff auf die Vorlage für [!UICONTROL leere mobile Scorecards]

Sie haben folgende Möglichkeiten, auf die Vorlage für [!UICONTROL leere mobile Scorecards] zuzugreifen:

**Neues Projekt erstellen**

1. Öffnen Sie Adobe Analytics und klicken Sie auf die Registerkarte **[!UICONTROL Workspace]**.
2. Klicken Sie auf die Schaltfläche **[!UICONTROL Neues Projekt erstellen]** und wählen Sie die Projektvorlage **[!UICONTROL Leere mobile Scorecard]** aus.
3. Klicken Sie auf die Schaltfläche **[!UICONTROL Erstellen]**.

![Scorecard-Vorlage](assets/new_template.png)

**Projekt hinzufügen**

Klicken Sie im Bildschirm **[!UICONTROL Projekte]** auf der Registerkarte **[!UICONTROL Komponenten]** auf die Schaltfläche **[!UICONTROL Hinzufügen]** und wählen Sie **[!UICONTROL Mobile Scorecard]** aus.

![Projekte hinzufügen](assets/add_project.png)

**Verwenden von [!DNL Analytics]-Tools**

Klicken Sie in [!DNL Analytics] auf das Menü **[!UICONTROL Tools]** und wählen Sie **[!UICONTROL Analytics-Dashboards (Mobile App)]** aus. Klicken Sie im nachfolgenden Bildschirm auf den Button **[!UICONTROL Neue Scorecard erstellen]**.

### Scorecard mit Daten konfigurieren und speichern

So implementieren Sie die Scorecard-Vorlage:

1. Geben Sie unter **[!UICONTROL Eigenschaften]** (in der rechten Leiste) eine **[!UICONTROL Report Suite des Projekts]** an, aus der Sie Daten verwenden möchten.

   ![Report Suite-Auswahl](assets/properties_save.png)

2. Um Ihrer Scorecard eine neue Kachel hinzuzufügen, ziehen Sie eine Metrik aus dem linken Bereich und legen Sie sie im Bereich **[!UICONTROL Metriken hierher ziehen und ablegen]** ab. Sie können auch eine Metrik zwischen zwei Kacheln einfügen, indem Sie einen ähnlichen Workflow verwenden.

   ![Kacheln hinzufügen](assets/build_list.png)


   *Von jeder Kachel aus können Sie auf eine Detailansicht zugreifen, die zusätzliche Informationen über die Metrik anzeigt, wie z. B. die obersten Elemente in einer Liste verwandter Dimensionen.*


3. Um einer Metrik eine verwandte Dimension hinzuzufügen, ziehen Sie eine Dimension aus dem linken Bereich und legen Sie sie auf einer Kachel ab. Sie können beispielsweise geeignete Dimensionen (wie **[!DNL DMA Region]** in diesem Beispiel) zur Metrik **[!UICONTROL Unique Visitors]** hinzufügen, indem Sie sie auf die Kachel ziehen und dort ablegen. Dimensionen, die Sie hinzufügen, werden im Aufschlüsselungsabschnitt der kachelspezifischen **[!UICONTROL Eigenschaften]** angezeigt. Sie können jeder Kachel mehrere Dimensionen hinzufügen.

   ![Dimensionen hinzufügen](assets/layer_dimensions.png)

   Sie können auch allen Kacheln eine Dimension hinzufügen, indem Sie diese auf der Scorecard-Arbeitsfläche ablegen.

   Wenn Sie im Scorecard Builder auf eine Kachel klicken, zeigt die rechte Leiste die Eigenschaften und Merkmale an, die mit dieser Kachel verbunden sind. In dieser Leiste können Sie einen neuen **[!UICONTROL Titel]** für die Kachel angeben und alternativ die Kachel konfigurieren, indem Sie Komponenten angeben, anstatt sie aus der linken Leiste zu ziehen und abzulegen.

   Wenn Sie auf Kacheln klicken, wird in einem dynamischen Popup angezeigt, wie die Aufschlüsselungsansicht für ausführende Benutzer in der App dargestellt wird. Wenn keine Dimension auf die Kachel angewendet wurde, werden je nach Standarddatumsbereich entweder **Stunden** oder **Tage** als Aufschlüsselungsdimension verwendet.

   ![Aufschlüsselungsansicht](assets/break_view.png)

   Jede der Kachel hinzugefügte Dimension wird in einer Dropdown-Liste in der Detailansicht der App angezeigt. Der ausführende Benutzer kann dann aus den in der Dropdown-Liste aufgelisteten Optionen auswählen.

4. Um ein Segment auf einzelne Kacheln anzuwenden, ziehen Sie es aus dem linken Bereich und legen Sie es direkt auf der Kachel ab. Wenn Sie das Segment auf alle Kacheln in der Scorecard anwenden möchten, legen Sie die Kachel oben auf der Scorecard ab. Sie können auch Segmente anwenden, indem Sie im Filtermenü unterhalb der Datumsbereiche Segmente auswählen. Sie [konfigurieren und wenden Filter für Ihre Scorecards](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/using-panels/using-drop-down-filters.html?lang=de) genauso wie in Adobe Analytics Workspace an.

   ![Segmente für Filter erstellen](assets/segment_ui.png)

5. Um eine Komponente zu entfernen, die auf die gesamte Scorecard angewendet wird, klicken Sie auf eine beliebige Stelle außerhalb der Kacheln auf die Scorecard. Entfernen Sie die Komponente, indem Sie auf das **x** klicken, das angezeigt wird, wenn Sie den Mauszeiger über die Komponente bewegen, wie unten für das Segment **[!DNL Mobile Customers]** dargestellt:

   ![Komponenten entfernen](assets/new_remove.png)

6. In den **[!UICONTROL Eigenschaften]** der Scorecard können Sie optional auch Folgendes angeben:

   * Ein **[!UICONTROL Standarddatumsbereich]**. Die Bereiche, die Sie hier angeben, sind die gleichen, die beim ersten Zugriff des ausführenden Benutzers auf die Scorecard in der App angewendet werden.

   * Ein **[!UICONTROL Vergleichsdatumsbereich]**

   * Alle **[!UICONTROL Segmente]**, die auf die gesamte Scorecard angewendet werden sollen

7. Um die Scorecard zu benennen, klicken Sie auf den Namensbereich in der oberen linken Ecke des Bildschirms und geben Sie den neuen Namen ein.

   ![Scorecards benennen](assets/new_name.png)

## Scorecard freigeben

So geben Sie die Scorecard für einen ausführenden Benutzer frei:

1. Klicken Sie auf das Menü **[!UICONTROL Freigeben]** und wählen Sie **[!UICONTROL Scorecard freigeben]**.

2. Füllen Sie die Felder im Formular **[!UICONTROL Mobile Scorecard freigeben]** aus, indem Sie:

   * den Namen der Scorecard angeben
   * eine Beschreibung der Scorecard angeben
   * relevante Tags hinzufügen
   * die Empfänger der Scorecard angeben

3. Klicken Sie auf **[!UICONTROL Freigabe]**.

![Scorecards freigeben](assets/new_share.png)

Nachdem Sie eine Scorecard freigegeben haben, können die Empfänger in den Analytics-Dashboards darauf zugreifen. Wenn Sie in Scorecard Builder nachträgliche Änderungen an der Scorecard vornehmen, werden diese automatisch in der freigegebenen Scorecard aktualisiert. Ausführende Benutzer sehen die Änderungen, nachdem sie die Scorecard in ihrer App aktualisiert haben.

Wenn Sie die Scorecard durch Hinzufügen neuer Komponenten aktualisieren, sollten Sie die Scorecard erneut freigeben (und die Option zum **[!UICONTROL Freigeben eingebetteter Komponenten]** aktivieren), um sicherzustellen, dass die ausführenden Benutzer Zugriff auf diese Änderungen haben.

## Festlegen von ausführenden Benutzern mit der Applikation

In einigen Fällen benötigen die ausführenden Benutzer möglicherweise zusätzliche Hilfe, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.

### Ausführenden Benutzern beim Zugriff helfen

Um ausführenden Benutzern zu helfen, auf Ihre Scorecards in der App zuzugreifen, stellen Sie Folgendes sicher:

* Auf den Geräten Ihrer Benutzer muss mindestens iOS-Version 10 oder Android-Version 4.4 (KitKat) installiert sein.
* Die Adobe Analytics-Anmeldeinformationen Ihrer Benutzer müssen gültig sein.
* Sie müssen die mobilen Scorecards für Ihre Benutzer korrekt erstellt und freigegeben haben.
* Ihre Benutzer benötigen Zugriff auf Analysis Workspace und die Report Suite, auf der die Scorecard basiert.
* Ihre Benutzer müssen Zugriff auf die Komponenten haben, die die Scorecard enthält. Hinweis: Sie können bei der Freigabe Ihrer Scorecards eine Option auswählen, um **[!UICONTROL eingebettete Komponenten freizugeben]**.

### Ausführenden Benutzern mit der App helfen

So unterstützen Sie ausführende Benutzer:

1. Helfen Sie ihnen, die App herunterzuladen und zu installieren. Führen Sie zu diesem Zweck die folgenden Schritte aus, um den Zugriff auf Ihre ausführenden Benutzer zu erweitern, je nachdem, ob sie ein iOS- oder ein Android-Gerät verwenden.

   **Für ausführende Benutzer mit iOS-Geräten:**

   * Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

      [iOS-Link](https://apple.co/2zXq0aN)
   **Für ausführende Benutzer mit Android-Geräten:**

   * Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

      [Android-Link](https://bit.ly/2LM38Oo)
   Nach dem Herunterladen und der Installation können sich ausführende Benutzer mit ihren vorhandenen Adobe Analytics-Anmeldeinformationen bei der App anmelden. Adobe und Enterprise/Federated IDs werden unterstützt.

   ![Willkommensbildschirm der App](assets/welcome.png)

2. Helfen Sie Benutzern beim Zugriff auf Ihre Scorecard. Nach der Anmeldung bei der App wird ausführenden Benutzern der Bildschirm **[!UICONTROL Unternehmen auswählen]** angezeigt. Auf diesem Bildschirm werden die Unternehmensanmeldungen angezeigt, die der ausführende Benutzer verwenden kann. So helfen Sie Benutzern, eine Scorecard anzuzeigen:

   * Tippen Sie auf den Namen der Unternehmensanmeldung oder der Experience Cloud-Organisation, der für die von Ihnen freigegebene Scorecard gilt. Die Scorecard-Liste zeigt alle Scorecards an, die mit dem ausführenden Benutzer mit dieser Unternehmensanmeldung freigegeben wurden.
   * Helfen Sie Benutzern, diese Liste ggf. nach der **[!UICONTROL zuletzt geänderten Scorecard]** zu sortieren.
   * Tippen Sie auf den Namen der Scorecard, um sie anzuzeigen.

   ![Wählen Sie ein Unternehmen aus.](assets/accesscard.png)

   Wenn sich der ausführende Benutzer anmeldet und eine Meldung angezeigt wird, dass nichts freigegeben wurde, kann das folgende Gründe haben:

   * Der ausführende Benutzer hat möglicherweise die falsche Analytics-Instanz ausgewählt.

   * Eventuell wurde die Scorecard nicht für den ausführenden Benutzer freigegeben.

      ![Nichts freigegeben](assets/nothing.png)


   * Vergewissern Sie sich, dass sich der ausführende Benutzer bei der richtigen Analytics-Instanz anmelden kann und dass die Scorecard freigegeben wurde.


3. Erklären Sie dem ausführenden User, wie Kacheln in den von Ihnen freigegebenen Scorecards angezeigt werden (die erste Scorecard unten ist auf den Dunkelmodus festgelegt; weitere Informationen finden Sie unter **[!UICONTROL Voreinstellungen]** weiter unten, wenn Sie der Meinung sind, dass Ihr ausführender Benutzer diese Anzeigeoption bevorzugt):

   ![Kacheln erklären](assets/newexplain.png)

   ![Beispiel-Scorecard](assets/intro_scorecard.png)

   Zusätzliche Informationen zu Kacheln:

   * Die Granularität der Sparklines hängt von der Länge des Datumsbereichs ab:
      * Für einen Tag wird ein stündlicher Trend angezeigt.
      * Für mehr als einen Tag und weniger als ein Jahr wird ein täglicher Trend angezeigt.
      * Für ein Jahr oder mehr wird ein wöchentlicher Trend angezeigt.
   * Die Formel für die Änderung des Prozentwerts ist: Gesamtwert der Metrik (aktueller Datumsbereich) – Gesamtwert der Metrik (Vergleichsdatumsbereich) / Gesamtwert der Metrik (Vergleichsdatumsbereich).
   * Sie können den Anzeigebereich nach unten ziehen, um die Scorecard zu aktualisieren.


4. Tippen Sie auf eine Kachel, um zu zeigen, wie eine detaillierte Aufschlüsselung für die Kachel funktioniert.

   ![Aufschlüsselungsansicht](assets/sparkline.png)

   * Tippen Sie auf einen beliebigen Punkt auf einer Sparkline, um Daten anzuzeigen, die diesem Punkt auf der Linie zugeordnet sind.

   * In einer Tabelle werden Daten zu den der Kachel hinzugefügten Dimensionen angezeigt. Tippen Sie auf den Abwärtspfeil, um Dimensionen auszuwählen. Wenn der Kachel keine Dimension hinzugefügt wurde, werden in der Tabelle Diagrammdaten angezeigt.

5. So ändern Sie Datumsbereiche für Ihre Scorecard:

   ![Datum ändern](assets/changedate.png)

   * Sie können die Datumsbereiche auch in der oben gezeigten Aufschlüsselungsansicht auf dieselbe Weise ändern.

   * Je nachdem, auf welches Intervall Sie tippen (**Tag**, **Woche**, **Monat** oder **Jahr**), sehen Sie zwei Optionen für Datumsbereiche – entweder den aktuellen oder den unmittelbar vorhergehenden Zeitraum. Tippen Sie auf eine dieser beiden Optionen, um den ersten Bereich auszuwählen. Tippen Sie in der Liste unter **[!UICONTROL VERGLEICHEN MIT]** auf eine der angezeigten Optionen, um die Daten in diesem Zeitraum mit dem ersten von Ihnen ausgewählten Datumsbereich zu vergleichen. Tippen Sie oben rechts im Bildschirm auf **[!UICONTROL Fertig]**. Das Feld **[!UICONTROL Datumsbereiche]** und die Scorecard-Kacheln werden mit den neuen Vergleichsdaten aus den von Ihnen ausgewählten neuen Bereichen aktualisiert.

6. So hinterlassen Sie Feedback zu dieser App:

   1. Tippen Sie auf das Einstellungssymbol oben recht im App-Bildschirm.
   2. Tippen Sie auf dem Bildschirm **[!UICONTROL Einstellungen]** auf die Option **[!UICONTROL Feedback]**.
   3. Tippen Sie, um die Optionen zum Hinterlassen von Feedback anzuzeigen.

      ![Einstellungsbildschirm](assets/settings.png)

7. Um die Voreinstellungen zu ändern, tippen Sie auf die Option **[!UICONTROL Voreinstellungen]** oben. In den Voreinstellungen können Sie die biometrische Anmeldung aktivieren oder Sie können die App wie folgt für den Dunkelmodus einstellen:

   ![Dunkelmodus](assets/darkmode.png)

**So melden Sie einen Fehler:**

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Fehler aus. Geben Sie im Formular zur Meldung eines Fehlers im obersten Feld Ihre E-Mail-Adresse und im Feld darunter eine Beschreibung des Fehlers an. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um den Bericht zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.


![Fehler melden](assets/newbug.png)

**So schlagen Sie eine Verbesserung vor**:

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Vorschlag aus. Geben Sie im Vorschlagsformular im obersten Feld Ihre E-Mail-Adresse und im Feld darunter eine Beschreibung des Vorschlags an. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um den Vorschlag zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.

**So stellen Sie eine Frage:**

Tippen Sie auf die Option und geben Sie im obersten Feld Ihre E-Mail-Adresse und im Feld darunter Ihre Frage an. Ein Screenshot wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um die Frage zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.

>[!IMPORTANT]
>
>Seit Oktober 2020 führt Adobe schrittweise eine Reihe von Verbesserungen durch, um die Leistung der Applikation „Adobe Analytics-Dashboards“ zu optimieren. Diese Erweiterungen konzentrieren sich auf das Caching historischer Analytics-Daten, die zum Ausfüllen von Scorecards mit Datumsangaben (außer dem aktuellen Tag) verwendet werden. Diese Daten werden bis zu 24 Stunden lang in einem sicheren öffentlichen Microsoft Azure-Konto in der Cloud zwischengespeichert. Wenden Sie sich an Ihren CSM, wenn Sie diese Leistungsverbesserungsfunktionen nicht in Anspruch nehmen möchten.
