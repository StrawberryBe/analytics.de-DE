---
description: Anleitung zur Verwendung der Dashboards-Scorecards.
title: Handbuch zu Adobe Analytics Dashboards
translation-type: tm+mt
source-git-commit: 34c04a571a53c61970a97bc454df74b71bdbe10c

---


# Adobe Analytics-Dashboard: Handbuch zum Beginn für Führungskräfte

## Einführung

Adobe Analytics-Dashboard bieten jederzeit und überall Einblicke aus Adobe Analytics.  Die App ermöglicht Benutzern mobilen Zugriff auf intuitive Scorecards. Scorecards sind eine Sammlung von Schlüsselmetriken und anderen Komponenten, die in einem gekachelten Layout dargestellt werden. Sie können auf eine Scorecard tippen, um detailliertere Aufschlüsselungen und Trendberichte zu erhalten. Dashboard werden auf iOS- und Android-Betriebssystemen unterstützt.

## Informationen zu diesem Handbuch

Dieses Handbuch soll leitenden Benutzern helfen, Scorecards zu Analytics-Dashboards zu lesen und zu interpretieren. Die App ermöglicht es ausführenden Benutzern, eine umfassende Darstellung wichtiger Zusammenfassungsdaten schnell und einfach auf ihren eigenen Mobilgeräten anzuzeigen.

## Glossar

| Begriff | Definition |
|--- |--- |
| Verbraucher | Ausführende Person, die wichtige Metriken und Einblicke aus Analytics auf einem Mobilgerät anzeigt |
| Kurator | Person, die mit der Datenerfassung und -auswertung vertraut ist, Einblicke in Analytics erkennt und verteilt und die Scorecards konfiguriert, die von Verbrauchern angezeigt werden |
| Kuratierung | Der Vorgang der Erstellung oder Bearbeitung einer mobilen Scorecard mit relevanten Metriken, Dimensionen und anderen Komponenten für den Verbraucher |
| Scorecard | Eine Dashboard-Ansicht, die eine oder mehrere Kacheln enthält |
| Kachel | Wiedergabe einer Metrik in einer Scorecard-Ansicht |
| Aufschlüsselung | Eine sekundäre Ansicht, die durch Tippen auf eine Kachel in der Scorecard zugänglich ist. Diese Ansicht erweitert die auf der Kachel dargestellte Metrik und zeigt optional Informationen über zusätzliche Aufschlüsselungsdimensionen an. |
| Datumsbereich | Der primäre Datumsbereich für den Dashboard-Berichte |
| Vergleichsdatumsbereich | Der Datumsbereich, der mit dem primären Datumsbereich verglichen wird |

## Dashboard auf Ihrem Gerät einrichten

Um die Dashboard effektiv nutzen zu können, benötigen Sie einen Scorecard-Kurator, der Sie bei der Einrichtung unterstützt. Dieser Abschnitt enthält Informationen, die Ihnen helfen, die App zusammen mit Ihrem Kurator einzurichten.

### Zugriff erhalten

Für den Zugriff auf Scorecards zu Dashboards müssen Sie Folgendes sicherstellen:

* Sie haben gültige Anmeldeinformationen für Adobe Analytics.
* Ihr Kurator hat mobile Scorecards korrekt erstellt und für Sie freigegeben.

### Herunterladen und Installieren von Dashboards

Um die App herunterzuladen und zu installieren, führen Sie die Schritte entsprechend dem Betriebssystem auf Ihrem Gerät aus.

**Für iOS-Geräte:**

1. Click the following public link (It is also available in Analytics under **Tools** > **dashboards**):

   [iOS-Link](https://testflight.apple.com/join/WtXMQxlI): `https://testflight.apple.com/join/WtXMQxlI`

   Nachdem Sie auf den Link geklickt haben, wird der folgende Testflight-Bildschirm angezeigt:

   ![Testflight-Bildschirm](assets/testflight1.png)

2. Tippen Sie auf den Link **Im App Store anzeigen** auf dem Bildschirm, um die Testflight-App herunterzuladen.

3. Suchen und installieren Sie nach der Installation der Testflight-App Adobe Analytics-Dashboard aus Testflight:

   ![Testflight-Bildschirm](assets/testflight2.png)

**Für Android-Geräte:**

1. Tap the following Play Store link on the user&#39;s device (It is also available in Analytics under **Tools** > **dashboards**):


   [Android](https://play.google.com/apps/testing/com.adobe.analyticsmobileapp): `https://play.google.com/apps/testing/com.adobe.analyticsmobileapp`

   Nachdem Sie auf den Link getippt haben, tippen Sie auf dem folgenden Bildschirm auf den Link „Tester werden“:

   ![Play Store-Bildschirm](assets/play.png)

2. Tippen Sie im folgenden Bildschirm auf den Link, damit Sie die App **bei Google Play herunterladen** können:

   ![Download-Link](assets/playnext.png)

## Dashboard verwenden

So verwenden Sie Dashboard:

1. Melden Sie sich bei der App an. Der Anmeldebildschirm wird beim Starten von Dashboards angezeigt. Folgen Sie den Anweisungen und melden Sie sich mit Ihren bestehenden Adobe Analytics-Anmeldeinformationen an. Adobe und Enterprise/Federated IDs werden unterstützt.

   ![Anmeldesequenz](assets/signseq.png)

2. Wählen Sie ein Unternehmen aus. After you sign into dashboards, the **Choose a company** screen appears. Auf diesem Bildschirm werden die Unternehmensanmeldungen angezeigt, die Sie verwenden können. Tippen Sie auf den Unternehmensnamen, der mit der für Sie freigegebenen Scorecard verknüpft ist.

3. Anschließend wird die Scorecard-Liste mit allen für Sie freigegebenen Scorecards angezeigt. Tippen Sie auf die Scorecard, die Sie anzeigen möchten.

   ![Wählen Sie ein Unternehmen aus.](assets/accesscard.png)

   *Hinweis: Wenn Sie sich anmelden und eine Meldung darüber erhalten, dass nichts freigegeben wurde, überprüfen Sie Folgendes zusammen mit Ihrem Kurator:*

   * *Sie können sich bei der richtigen Analytics-Instanz anmelden.*
   * *Die Scorecard wurde für Sie freigegeben.*

      ![Nichts freigegeben](assets/nothing.png)

4. Sehen Sie sich die Kacheln an, die in der Scorecard angezeigt werden.

   ![Erklärte Kacheln](assets/newexplain.png)

   Zusätzliche Informationen zu Kacheln:

   * Die Granularität der Sparklines hängt von der Länge des Datumsbereichs ab:
   * Für einen Tag wird ein stündlicher Trend angezeigt.
   * Für mehr als einen Tag und weniger als ein Jahr wird ein täglicher Trend angezeigt.
   * Für ein Jahr oder mehr wird ein wöchentlicher Trend angezeigt.
   * Die Formel für die Änderung des Prozentwerts ist: Gesamtwert der Metrik (aktueller Datumsbereich) – Gesamtwert der Metrik (Vergleichsdatumsbereich) / Gesamtwert der Metrik (Vergleichsdatumsbereich).
   * Sie können den Anzeigebereich nach unten ziehen, um die Scorecard zu aktualisieren.

5. Tippen Sie auf eine Kachel, um zu zeigen, wie eine detaillierte Aufschlüsselung für die Kachel funktioniert.

   ![Aufschlüsselungsansicht](assets/sparkline.png)


6. So ändern Sie Datumsbereiche für Ihre Scorecard:

   ![Datum ändern](assets/changedate.png)

   *Hinweis: Sie können die Datumsbereiche auch in der oben gezeigten Aufschlüsselungsansicht auf dieselbe Weise ändern.*

   Je nachdem, auf welches Intervall Sie tippen (**Tag**, **Woche**, **Monat** oder **Jahr**), sehen Sie zwei Optionen für Datumsbereiche – entweder den aktuellen oder den unmittelbar vorhergehenden Zeitraum. Tippen Sie auf eine dieser beiden Optionen, um den ersten Bereich auszuwählen. Tippen Sie in der Liste unter **VERGLEICHEN MIT** auf eine der angezeigten Optionen, um die Daten in diesem Zeitraum mit dem ersten von Ihnen ausgewählten Datumsbereich zu vergleichen. Tippen Sie oben rechts im Bildschirm auf **Fertig**. Das Feld **Datumsbereiche** und die Scorecard-Kacheln werden mit den neuen Vergleichsdaten aus den von Ihnen ausgewählten neuen Bereichen aktualisiert.

7. Fordern Sie eine Scorecard-Aktualisierung an. Wenn eine Scorecard nicht alle Metriken oder Aufschlüsselungen enthält, die für Sie von Interesse sein könnten, wenden Sie sich an Ihr Analytics-Team, um die Scorecard zu aktualisieren. Nach der Aktualisierung können Sie die Karte auf dem Bildschirm nach unten ziehen, um sie zu aktualisieren und die kürzlich hinzugefügten Daten zu laden.



8. Feedback hinterlassen. So hinterlassen Sie Feedback:

   1. Tippen Sie auf das Benutzersymbol oben rechts im Bildschirm &quot;Dashboards&quot;.
   2. Tippen Sie auf dem Bildschirm **Mein Konto** auf die Option **Feedback**.
   3. Tippen Sie, um die Optionen zum Hinterlassen von Feedback anzuzeigen.
   ![Feedback hinterlassen](assets/feedback.png)
   ![Feedback-Optionen](assets/feedback_option.png)


**So melden Sie einen Fehler:**

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Fehler aus. Geben Sie im Formular zur Meldung eines Fehlers im obersten Feld Ihre E-Mail-Adresse und im Feld darunter eine Beschreibung des Fehlers an. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um den Bericht zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.


![Fehler melden](assets/newbug.png)

**So schlagen Sie eine Verbesserung vor**:

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Vorschlag aus. Geben Sie im Vorschlagsformular im obersten Feld Ihre E-Mail-Adresse und im Feld darunter eine Beschreibung des Vorschlags an. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um den Vorschlag zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.

**So stellen Sie eine Frage:**

Tippen Sie auf die Option und geben Sie im obersten Feld Ihre E-Mail-Adresse und im Feld darunter Ihre Frage an. Ein Screenshot wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um die Frage zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.
