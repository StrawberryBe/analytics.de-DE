---
description: Anleitung zum Einrichten der App-Scorecards.
title: Adobe Analytics Mobile App Curator Guide
translation-type: tm+mt
source-git-commit: 9149e9ad5a74ef1de0ece5fb0056ee6fee5d50e9

---



# BETA: Kuratorleitfaden für die mobile Analytics-App


## Einführung

Die mobile Adobe Analytics-App bietet jederzeit und überall Einblicke aus Adobe Analytics.   Die App ermöglicht Benutzern auf Mobilgeräten Zugriff auf intuitive Scorecards, die Sie über die Desktop-Benutzeroberfläche von Adobe Analytics erstellen und freigeben. Bei Scorecards handelt es sich um eine Sammlung von Schlüsselmetriken und anderen Komponenten, die in einem gekachelten Layout dargestellt sind und auf die Sie für detailliertere Aufschlüsselungen und Trendberichte tippen können. Sie können Scorecards entsprechend den für Sie wichtigsten Daten anpassen. Die mobile App wird auf iOS- und Android-Betriebssystemen unterstützt.

## Informationen zu diesem Handbuch

Dieses Handbuch soll Kuratoren von Adobe Analytics-Daten bei der Konfiguration von Scorecards für ihre leitenden Benutzer in der Analytics Mobile App unterstützen. Kuratoren können organisatorische Administratoren oder Personen in anderen Rollen sein, die für die Einrichtung von App-Scorecards zuständig sind. Diese ermöglichen es leitenden Benutzern, eine umfassende Darstellung wichtiger Zusammenfassungsdaten schnell und einfach auf ihren eigenen Mobilgeräten anzuzeigen. Obwohl geschäftsführende Benutzer Endbenutzer der mobilen Analytics-App sind, hilft dieses Handbuch Datenkuratoren bei der effektiven Einrichtung der App für diese Benutzer.


## Glossar der Begriffe

Die folgende Tabelle beschreibt die Begriffe zum Verständnis der Zielgruppe, Funktionen und Funktionsweise der mobilen Analytics-App.

| Begriff | Definition |
|--- |--- |
| Verbraucher | Executive persona zeigt wichtige Metriken und Einblicke aus Analytics auf einem Mobilgerät an |
| Kurator | Datenwörterbuch-Persona, die Erkenntnisse aus Analytics findet und verteilt und die vom Verbraucher anzuzeigenden Barcodes konfiguriert |
| Kuratierung | Der Vorgang der Erstellung oder Bearbeitung einer mobilen Scorecard mit relevanten Metriken, Dimensionen und anderen Komponenten für den Verbraucher |
| Scorecard | Eine Ansicht für eine mobile App mit einer oder mehreren Kacheln |
| Kachel | Rendering einer Metrik in einer Scorecard-Ansicht |
| Aufschlüsselung | Eine sekundäre Ansicht, die durch Tippen auf eine Kachel in der Scorecard aufgerufen werden kann. Diese Ansicht wird bei der auf der Kachel angezeigten Metrik erweitert und optional bei weiteren Aufschlüsselungsdimensionen berichtet. |
| Datumsbereich | Der primäre Datumsbereich für Berichte über mobile Anwendungen |
| Vergleichsdatumsbereich | Der Datumsbereich, der mit dem primären Datumsbereich verglichen wird |

 
## Eine Wertungsliste für Führungskräfte erstellen

Eine mobile Scorecard zeigt wichtige Datenvisualisierungen für Benutzer in einem gekachelten Layout an, wie nachfolgend gezeigt:


![Beispiel-Scorecard](assets/intro_scorecard.png)


Als Kurator für diese Scorecard können Sie mit dem Scorecard Builder konfigurieren, welche Kacheln auf der Scorecard für Ihren Kunden angezeigt werden. Sie können auch konfigurieren, wie die detaillierten Ansichten oder Aufschlüsselungen angepasst werden können, sobald auf die Kacheln getippt wird. Die Scorecard Builder-Oberfläche ist unten dargestellt:

![Scorecard Builder](assets/scorecard_builder.png)


Zur Erstellung des Scorecard müssen Sie folgende Schritte ausführen:

1. Greifen Sie auf die Vorlage "Leeres mobiles Scorecard"zu.
2. Konfigurieren Sie die Scorecard mit Daten und speichern Sie sie.


### Zugriff auf die Vorlage "Leeres mobiles Scorecard"

Sie haben folgende Möglichkeiten, auf die Vorlage Blank Mobile Scorecard zuzugreifen:

**Neues Projekt erstellen**

1. Öffnen Sie Adobe Analytics und klicken Sie auf die Registerkarte **Arbeitsbereich** .
2. Klicken Sie auf die Schaltfläche "Neues Projekt **** erstellen"und wählen Sie die Projektvorlage für die **leere mobile Scorecard** aus.
3. Klicken Sie auf die Schaltfläche **erstellen**.

![Scorecard-Vorlage](assets/new_template.png)


*Hinweis: Wenn Sie die Vorlage Blank Mobile Scorecard nicht sehen, wie unten gezeigt, wurde Ihr Unternehmen noch nicht für Beta aktiviert. Wenden Sie sich an Ihren Kundenbetreuer.*


**Projekt hinzufügen**

Klicken Sie im Bildschirm " **Projekte** "auf der Registerkarte " **Komponenten** "auf die Schaltfläche " **Hinzufügen** "und wählen Sie " **Mobilgerät-Scorecard"**.

![Projekte hinzufügen](assets/add_project.png)

**Analytics-Werkzeuge verwenden**

Klicken Sie in Analytics auf das **Extras** -Menü und wählen Sie " **Mobile App**"aus. Klicken Sie im nachfolgenden Bildschirm auf die Schaltfläche " **Scorecard** erstellen".

### Konfigurieren des Scorecards mit Daten und Speichern

So implementieren Sie die Scorecard-Vorlage:

1. Geben Sie unter **Eigenschaften** (in der rechten Leiste) eine **Projekt-Report Suite** an, aus der Sie Daten verwenden möchten.

   ![Report Suite-Auswahl](assets/properties_save.png)

2. Um eine neue Kachel zu Ihrer Scorecard hinzuzufügen, ziehen Sie eine Metrik aus dem linken Bereich und legen Sie sie in die **Drag &amp; Drop-Metriken hier** -Zone. Sie können auch eine Metrik zwischen zwei Kacheln einfügen, indem Sie einen ähnlichen Arbeitsablauf verwenden.

   ![Hinzufügen von Kacheln](assets/build_list.png)


   *Von jeder Kachel aus können Sie auf eine detaillierte Ansicht zugreifen, die zusätzliche Informationen zur Metrik anzeigt, z. B. die obersten Elemente für eine Liste der zugehörigen Dimensionen.*


3. Um einer Metrik eine zugehörige Dimension hinzuzufügen, ziehen Sie eine Dimension aus dem linken Bereich und legen Sie sie auf einer Kachel ab. Sie können beispielsweise geeignete Dimensionen (wie **DMA-Region** in diesem Beispiel) zur Metrik " **Unique Visitors** "hinzufügen, indem Sie sie auf die Kachel ziehen und dort ablegen. Dimensionen, die Sie hinzufügen, werden im Unterteilungsabschnitt der kachelspezifischen **Eigenschaften** angezeigt. Sie können jeder Kachel mehrere Dimensionen hinzufügen.

   ![Dimensionen hinzufügen](assets/layer_dimensions.png)

   *Hinweis: Sie können allen Kacheln auch eine Dimension hinzufügen, indem Sie sie auf der Arbeitsfläche "Scorecard"ablegen.*

   Wenn Sie im Scorecard Builder auf eine Kachel klicken, zeigt die rechte Leiste die Eigenschaften und Eigenschaften an, die mit dieser Kachel verbunden sind. In dieser Leiste können Sie einen neuen **Titel** für die Kachel angeben und alternativ die Kachel konfigurieren, indem Sie Komponenten angeben, anstatt sie aus der linken Leiste zu ziehen und abzulegen.


   Wenn Sie auf Kacheln klicken, wird in einem dynamischen Popup angezeigt, wie die Aufschlüsselungsansicht dem Benutzer in der App angezeigt wird. Wenn keine Dimension auf die Kachel angewendet wurde, beträgt die Aufschlüsselungsdimension je nach Standarddatumsbereich **Stunde** oder **Tage**.

   ![Breakdown_view](assets/break_view.png)

   *Beachten Sie, dass jede der Kachel hinzugefügte Dimension in einer Dropdown-Liste in der Detailansicht der App angezeigt wird. Der Exekutivbenutzer kann dann aus den in der Dropdownliste aufgelisteten Optionen auswählen.*

4. Um Segmente auf einzelne Kacheln anzuwenden, ziehen Sie ein Segment aus dem linken Bereich und legen es direkt über die Kachel ab. Wenn Sie das Segment auf alle Kacheln in der Scorecard anwenden möchten, legen Sie die Kachel auf der Scorecard ab.

5. Um eine Komponente zu entfernen, die auf die gesamte Scorecard angewendet wird, klicken Sie auf eine beliebige Stelle außerhalb der Kacheln auf die Scorecard und entfernen Sie sie, indem Sie auf das **x** klicken, das angezeigt wird, wenn Sie den Mauszeiger über die Komponente bewegen, wie unten für das Segment **Mobile Customers** dargestellt:

   ![Remove_components](assets/new_remove.png)

6. Unter **Eigenschaften** von Scorecard können Sie optional auch Folgendes angeben:

   * Ein **Standarddatumsbereich**. Die hier angegebenen Bereiche gelten für den ersten Zugriff des Benutzers auf die Scorecard in seiner App.

   * Ein **Vergleichsdatumsbereich**

   * Alle **Segmente** , die für die gesamte Wertungsliste gelten sollen

7. Um der Scorecard einen Namen zu geben, klicken Sie auf den Namespace oben links im Bildschirm und geben Sie den neuen Namen ein.

   ![Naming_Scorecards](assets/new_name.png)

## Scorecard freigeben

So geben Sie die Scorecard für einen Executive-Benutzer frei:

1. Klicken Sie auf das Menü " **Freigeben** "und wählen Sie " **Freigeben**".

2. Füllen Sie die Felder im **Freigabeformular** aus, indem Sie:

   * Bezeichnung der Scorecard
   * Beschreibung des Scorecard
   * Hinzufügen relevanter Tags
   * Empfänger für die Scorecard angeben
   * Wählen Sie die Option zum **Freigeben eingebetteter Komponenten mit Empfängern** aus, um sicherzustellen, dass der exekutive Benutzer Zugriff auf alle Komponenten in der Scorecard hat.

3. Klicken Sie auf **Freigabe**.

![Share_Scorecards](assets/new_share.png)


Nachdem Sie eine Scorecard freigegeben haben, können Ihre Empfänger auf diese in ihrer mobilen Analytics-App zugreifen. Wenn Sie nachfolgende Änderungen am Scorecard im Scorecard Builder vornehmen, werden diese automatisch in der freigegebenen Scorecard aktualisiert. Die Änderungen werden dann angezeigt, nachdem die Scorecard in der App aktualisiert wurde.

*Hinweis: Wenn Sie die Scorecard durch Hinzufügen neuer Komponenten aktualisieren, sollten Sie die Scorecard erneut freigeben (und die Option "Eingebettete Komponenten **automatisch mit Empfängern**teilen"aktivieren), um sicherzustellen, dass Ihre Manager-Benutzer Zugriff auf diese Änderungen haben.*

## Einrichten von Executive-Benutzern mit der App

In einigen Fällen benötigen Benutzer, die sie ausführen, möglicherweise zusätzliche Unterstützung, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.

### Zugriff für Führungskräfte

Um leitende Benutzer beim Zugriff auf Ihre Scorecards in der App zu unterstützen, stellen Sie Folgendes sicher:

* Die Mindestanforderungen an das mobile Betriebssystem auf ihren Geräten sind iOS Version 10 oder höher oder Android Version 4.4 (KitKat) oder höher
* Sie haben eine gültige Anmeldung bei Adobe Analytics
* Sie haben für diese Karten korrekt mobile Scorecards erstellt und diese mit ihnen geteilt.
* Sie haben Zugriff auf den Arbeitsbereich für Analysen und die Report Suite, auf der die Wertangabe basiert
* Sie haben Zugriff auf die Komponenten, die der Binnenmarktanzeiger enthält. Hinweis: Sie können eine Option auswählen, wenn Sie Ihre Scorecards freigeben, um eingebettete Komponenten **automatisch für Empfänger** freizugeben.

### Hilfe für Benutzer, die die App verwenden

Während der Betaphase und bevor die App für die Öffentlichkeit freigegeben wird, können Sie steuern, wer Zugriff auf die App hat.

1. Helfen Sie leitenden Benutzern, die App herunterzuladen und zu installieren. Führen Sie zu diesem Zweck die folgenden Schritte aus, um den Zugriff auf Ihre leitenden Benutzer zu erweitern, je nachdem, ob sie ein iOS- oder ein Android-Gerät verwenden.

   **Für leitende Benutzer unter iOS:**

   1. Klicken Sie auf den folgenden öffentlichen Link (er ist auch in Analytics unter **Tools** &gt; **Mobile App** verfügbar):

      [iOS-Link](https://testflight.apple.com/join/WtXMQxlI): `https://testflight.apple.com/join/WtXMQxlI`

      Nachdem Sie auf den Link geklickt haben, wird der folgende Testflight-Bildschirm angezeigt:

      ![Testflight-Bildschirm](assets/testflight1.png)

   2. Tippen Sie auf den Link **Im App Store** anzeigen, um die Testflight-App herunterzuladen.

   3. Suchen und installieren Sie nach der Installation der Testflight-App die Adobe Analytics Mobile-App aus Testflight:

      ![Testflight-Bildschirm](assets/testflight2.png)
   **Für Führungskräfte unter Android:**

   1. Tippen Sie auf dem Gerät des Benutzers auf den folgenden Link zum Play Store (er ist auch in Analytics unter **Tools** &gt; **Mobile App** verfügbar):


      [Android](https://play.google.com/apps/testing/com.adobe.analyticsmobileapp): `https://play.google.com/apps/testing/com.adobe.analyticsmobileapp`

      Nachdem Sie auf den Link getippt haben, tippen Sie auf dem folgenden Bildschirm auf den Link Als Tester werden:

      ![Play Store-Bildschirm](assets/play.png)

   2. Tippen Sie auf den Link zum **Herunterladen auf Google Play** im folgenden Bildschirm:

      ![Download-Link](assets/playnext.png)

   3. Laden Sie die App herunter und installieren Sie sie.
   Nach dem Herunterladen und der Installation können sich Benutzer mit ihren vorhandenen Adobe Analytics-Anmeldeinformationen bei der App anmelden. Adobe und Enterprise/Federated IDs werden unterstützt.

   ![App-Startbildschirm](assets/welcome.png)

2. Helfen Sie ihnen beim Zugriff auf Ihre Scorecard. Nachdem sich Benutzer mit leitenden Funktionen bei der App angemeldet haben, wird der Bildschirm "Unternehmen **auswählen** "angezeigt. Dieser Bildschirm listet die Anmeldeunternehmen auf, zu denen der geschäftsführende Benutzer gehört. Um ihnen beim Aufrufen des Scorecard zu helfen:

   * Tippen Sie auf den Namen des angemeldeten Unternehmens oder der Experience Cloud-Organisation, der für die freigegebene Scorecard gilt. In der Scorecard-Liste werden dann alle Scorecards angezeigt, die mit der Geschäftsführung unter dieser Firmenanmeldung geteilt wurden.
   * hilft ihnen, diese Liste gegebenenfalls nach der **zuletzt geänderten** Liste zu sortieren.
   * Tippen Sie auf den Namen der Scorecard, um sie anzuzeigen.
   ![Wählen Sie ein Unternehmen aus.](assets/accesscard.png)

   Hinweis: Wenn sich der geschäftsführende Benutzer anmeldet und eine Meldung angezeigt wird, dass nichts freigegeben wurde:

   * Der geschäftsführende Benutzer hat möglicherweise die falsche Analytics-Instanz ausgewählt
   * Möglicherweise wurde die Scorecard nicht für den Exekutivbenutzer freigegeben

      ![Nichts freigegeben](assets/nothing.png)
   Vergewissern Sie sich, dass sich der geschäftsführende Benutzer bei der richtigen Analytics-Instanz anmelden kann und dass die Scorecard freigegeben wurde.

3. Erklären Sie dem geschäftsführenden Benutzer, wie Kacheln in den freigegebenen Scorecards angezeigt werden.

   ![Kacheln erklären](assets/newexplain.png)


   Zusätzliche Informationen zu Kacheln:

   * Die Granularität der Wortgrafiken hängt von der Länge des Datumsbereichs ab:
      * Ein Tag zeigt einen stündlichen Trend
      * Mehr als ein Tag und weniger als ein Jahr zeigen einen täglichen Trend
      * Ein Jahr oder mehr zeigt einen wöchentlichen Trend an
   * Formel zur Änderung des Prozentwerts ist Metriksumme (aktueller Datumsbereich) - Metriksumme (Vergleichsdatumsbereich) / Metriksumme (Vergleichsdatumsbereich).
   * Sie können den Anzeigebereich nach unten ziehen, um die Scorecard zu aktualisieren.


4. Tippen Sie auf eine Kachel, um anzuzeigen, wie eine detaillierte Aufschlüsselung für die Kachel funktioniert.

   ![Aufschlüsselungsansicht](assets/sparkline.png)


5. So ändern Sie Datumsbereiche für Ihre Wertungsliste:

   ![Datum ändern](assets/changedate.png)

   *Hinweis: Sie können die Datumsbereiche auch in der oben gezeigten Aufschlüsselungsansicht auf dieselbe Weise ändern.*

   Je nachdem, auf welchen Zeitraum Sie tippen (**Tag**, **Woche**, **Monat** oder **Jahr**), sehen Sie zwei Optionen für Datumsbereiche: entweder den aktuellen Zeitraum oder den unmittelbar davor liegenden Zeitraum. Tippen Sie auf eine dieser beiden Optionen, um den ersten Bereich auszuwählen. Tippen Sie in der Liste " **VERGLEICHEN MIT** "auf eine der angezeigten Optionen, um die Daten dieses Zeitraums mit dem ersten ausgewählten Datumsbereich zu vergleichen. Tippen Sie oben rechts im Bildschirm auf **Fertig** . Die Kacheln **Datumsbereiche** und Scorecard werden mit den neuen Vergleichsdaten aus den ausgewählten Bereichen aktualisiert.

6. So hinterlassen Sie Feedback zu dieser App:

   1. Tippen Sie auf das Benutzersymbol oben rechts im App-Bildschirm.
   2. Tippen Sie im Bildschirm " **Mein Konto** "auf die Option **Feedback** .
   3. Tippen Sie auf , um die Optionen zum Verlassen des Feedbacks anzuzeigen.
   ![Feedback hinterlassen](assets/feedback.png)
   ![Feedback-Optionen](assets/feedback_option.png)


**So melden Sie einen Fehler**:

Tippen Sie auf die Option und wählen Sie eine Unterkategorie des Fehlers. Geben Sie im Formular zur Meldung eines Fehlers im oberen Feld Ihre E-Mail-Adresse und Ihre Beschreibung des Fehlers im Feld darunter ein. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können dies jedoch löschen, indem Sie auf das **X** im Anlagenbild tippen. Sie haben auch Optionen zum Aufnehmen von Screenshots, Hinzufügen von Screenshots oder Anhängen von Dateien. Um den Bericht zu senden, tippen Sie oben rechts im Formular auf das Papierebenensymbol.


![Berichtsfehler](assets/newbug.png)

**Verbesserungsvorschläge**:

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Vorschlag aus. Geben Sie im Empfehlungsformular Ihre E-Mail-Adresse im oberen Feld und Ihre Beschreibung des Fehlers im Feld darunter ein. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können dies jedoch löschen, indem Sie auf das **X** im Anlagenbild tippen. Sie haben auch Optionen zum Aufnehmen von Screenshots, Hinzufügen von Screenshots oder Anhängen von Dateien. Um den Vorschlag zu senden, tippen Sie oben rechts im Formular auf das Papierebenensymbol.

**So stellen Sie eine Frage**:

Tippen Sie auf die Option und geben Sie Ihre E-Mail-Adresse im oberen Feld und Ihre Frage im Feld darunter ein. Ein Screenshot wird automatisch an die Nachricht angehängt. Sie können dies jedoch löschen, indem Sie im Anlagenbild auf das **X** tippen. Sie haben auch Optionen zum Aufnehmen von Screenshots, Hinzufügen von Screenshots oder Anhängen von Dateien. Um die Frage zu senden, tippen Sie oben rechts im Formular auf das Papierebenensymbol.
