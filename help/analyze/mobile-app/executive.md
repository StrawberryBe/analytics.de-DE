---
description: Anleitung zum Einrichten der App-Scorecards.
title: Adobe Analytics Mobile App Curator Guide
translation-type: tm+mt
source-git-commit: 9149e9ad5a74ef1de0ece5fb0056ee6fee5d50e9

---


# Analytics Mobile App: Schnellstartanleitung für leitende Benutzer

## Einführung

Die mobile Adobe Analytics-App bietet jederzeit und überall Einblicke aus Adobe Analytics.  Die App ermöglicht Benutzern mobilen Zugriff auf intuitive Scorecards. Bei Scorecards handelt es sich um eine Sammlung von Schlüsselmetriken und anderen Komponenten, die in einem gekachelten Layout dargestellt sind und auf die Sie für detailliertere Aufschlüsselungen und Trendberichte tippen können. Die mobile App wird auf iOS- und Android-Betriebssystemen unterstützt.

## Informationen zu diesem Handbuch

 Dieses Handbuch soll leitenden Benutzern helfen, Scorecards in der mobilen Analytics-App zu lesen und zu interpretieren. Die App ermöglicht es leitenden Benutzern, eine umfassende Darstellung wichtiger Zusammenfassungsdaten schnell und einfach auf ihren eigenen Mobilgeräten anzuzeigen.

## Glossar der Begriffe

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

## App auf Ihrem Gerät einrichten

Um die App effektiv zu nutzen, müssen Sie den Scorecard-Kurator zur Einrichtung der App verwenden. Dieser Abschnitt enthält Informationen, die Ihnen bei der Einrichtung mithilfe Ihres Kurators helfen.

### Zugriff

Um auf Scorecards in der App zuzugreifen, stellen Sie Folgendes sicher:

* Sie haben eine gültige Anmeldung bei Adobe Analytics
* Ihr Kurator hat Mobilgeräte-Scorecards korrekt erstellt und für Sie freigegeben

### Herunterladen und Installieren der App

Um die App herunterzuladen und zu installieren, führen Sie die Schritte entsprechend dem Betriebssystem auf Ihrem Gerät aus.

**Für iOS-Geräte:**

1. Klicken Sie auf den folgenden öffentlichen Link (er ist auch in Analytics unter **Tools** &gt; **Mobile App** verfügbar):

   [iOS-Link](https://testflight.apple.com/join/WtXMQxlI): `https://testflight.apple.com/join/WtXMQxlI`

   Nachdem Sie auf den Link geklickt haben, wird der folgende Testflight-Bildschirm angezeigt:

   ![Testflight-Bildschirm](assets/testflight1.png)

2. Tippen Sie auf den Link **Im App Store** anzeigen, um die Testflight-App herunterzuladen.

3. Suchen und installieren Sie nach der Installation der Testflight-App die Adobe Analytics Mobile-App aus Testflight:

   ![Testflight-Bildschirm](assets/testflight2.png)

**Für Android-Geräte:**

1. Tippen Sie auf dem Gerät des Benutzers auf den folgenden Link zum Play Store (er ist auch in Analytics unter **Tools** &gt; **Mobile App** verfügbar):


   [Android](https://play.google.com/apps/testing/com.adobe.analyticsmobileapp): `https://play.google.com/apps/testing/com.adobe.analyticsmobileapp`

   Nachdem Sie auf den Link getippt haben, tippen Sie auf dem folgenden Bildschirm auf den Link Als Tester werden:

   ![Play Store-Bildschirm](assets/play.png)

2. Tippen Sie auf den Link zum **Herunterladen auf Google Play** im folgenden Bildschirm:

   ![Download-Link](assets/playnext.png)

## App verwenden

So verwenden Sie die App:

1. Melden Sie sich bei der App an. Der Anmeldebildschirm wird beim Starten der App angezeigt. Folgen Sie den Eingabeaufforderungen mit Ihren vorhandenen Adobe Analytics-Anmeldeinformationen. Adobe und Enterprise/Federated IDs werden unterstützt.

   ![Sequenz anmelden](assets/signseq.png)

2. Wählen Sie ein Unternehmen. Nach der Anmeldung bei der App wird der Bildschirm "Unternehmen **auswählen** "angezeigt. In diesem Bildschirm werden die Anmeldeunternehmen aufgelistet, zu denen Sie gehören. Tippen Sie auf den Firmennamen, der mit der für Sie freigegebenen Scorecard verknüpft ist.

3. Die Scorecard-Liste zeigt dann alle Scorecards an, die für Sie freigegeben wurden. Tippen Sie auf die Scorecard, die Sie anzeigen möchten.

   ![Wählen Sie ein Unternehmen aus.](assets/accesscard.png)

   *Hinweis: Wenn Sie sich anmelden und eine Meldung darüber erhalten, dass nichts freigegeben wurde, überprüfen Sie Folgendes mit Ihrem Kurator:*

   * *Sie können sich bei der richtigen Analytics-Instanz anmelden*
   * *Die Scorecard wurde für Sie freigegeben*

      ![Nichts freigegeben](assets/nothing.png)

4. Untersuchen Sie, wie die Kacheln in der Scorecard angezeigt werden.

   ![Erklärte Kacheln](assets/newexplain.png)

   Zusätzliche Informationen zu Kacheln:

   * Die Granularität der Wortgrafiken hängt von der Länge des Datumsbereichs ab:
   * Ein Tag zeigt einen stündlichen Trend
   * Mehr als ein Tag und weniger als ein Jahr zeigen einen täglichen Trend
   * Ein Jahr oder mehr zeigt einen wöchentlichen Trend an
   * Formel zur Änderung des Prozentwerts ist Metriksumme (aktueller Datumsbereich) - Metriksumme (Vergleichsdatumsbereich) / Metriksumme (Vergleichsdatumsbereich).
   * Sie können den Anzeigebereich nach unten ziehen, um die Scorecard zu aktualisieren.

5. Tippen Sie auf eine Kachel, um anzuzeigen, wie eine detaillierte Aufschlüsselung für die Kachel funktioniert.

   ![Aufschlüsselungsansicht](assets/sparkline.png)


6. So ändern Sie Datumsbereiche für Ihre Wertungsliste:

   ![Datum ändern](assets/changedate.png)

   *Hinweis: Sie können die Datumsbereiche auch in der oben gezeigten Aufschlüsselungsansicht auf dieselbe Weise ändern.*

   Je nachdem, auf welchen Zeitraum Sie tippen (**Tag**, **Woche**, **Monat** oder **Jahr**), sehen Sie zwei Optionen für Datumsbereiche: entweder den aktuellen Zeitraum oder den unmittelbar davor liegenden Zeitraum. Tippen Sie auf eine dieser beiden Optionen, um den ersten Bereich auszuwählen. Tippen Sie in der Liste " **VERGLEICHEN MIT** "auf eine der angezeigten Optionen, um die Daten dieses Zeitraums mit dem ersten ausgewählten Datumsbereich zu vergleichen. Tippen Sie oben rechts im Bildschirm auf **Fertig** . Die Kacheln **Datumsbereiche** und Scorecard werden mit den neuen Vergleichsdaten aus den ausgewählten Bereichen aktualisiert.

7. Hier finden Sie Aktualisierungen zu Scorecard. Wenn eine Scorecard nicht alle Metriken oder Aufschlüsselungen enthält, die für Sie von Interesse sein könnten, wenden Sie sich an Ihr Analytics-Team, um die Scorecard zu aktualisieren. Nach der Aktualisierung können Sie die Karte auf dem Bildschirm nach unten ziehen, um sie zu aktualisieren und die kürzlich hinzugefügten Daten zu laden.



8. Lassen Sie Feedback. So hinterlassen Sie Feedback:

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
