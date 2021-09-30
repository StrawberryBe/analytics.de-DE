---
description: So erstellen Sie eine Analytics-Dashboards-Scorecard
title: Scorecard erstellen
feature: Analytics Dashboards
role: User, Admin
source-git-commit: 38bb36db0e7f2fc032f0531fa40cfec29b7e926e
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 74%

---


# Festlegen von ausführenden Benutzern mit der Applikation

In einigen Fällen benötigen die ausführenden Benutzer möglicherweise zusätzliche Hilfe, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.

## Sicherstellen, dass Mobile-App-Benutzer Zugriff auf Adobe Analytics haben

1. Richten Sie neue Benutzer in der [Experience Cloud-Admin Console](/help/admin/admin-console/permissions/product-profile.md) ein.

1. Um Scorecards freigeben zu können, müssen Sie App-Benutzern Berechtigungen für den Zugriff auf Scorecard-Komponenten wie Analysis Workspace, die Report Suites, auf denen Scorecards basieren, sowie Segmente, Metriken und Dimensionen gewähren.

## Systemanforderungen von App-Benutzern

Um sicherzustellen, dass ausführende Benutzer Zugriff auf Ihre Scorecards in der App haben, stellen Sie Folgendes sicher:

* Auf den Geräten Ihrer Benutzer muss mindestens iOS-Version 10 oder Android-Version 4.4 (KitKat) installiert sein.
* Die Adobe Analytics-Anmeldeinformationen Ihrer Benutzer müssen gültig sein..
* Sie haben mobile Scorecards für sie korrekt erstellt und für diese freigegeben.
* Sie haben Zugriff auf die Komponenten, die die Scorecard enthält. Beachten Sie, dass Sie beim Freigeben Ihrer Scorecards für **[!UICONTROL Freigeben eingebetteter Komponenten]** eine Option auswählen können.

## Hilfe für Führungskräfte beim Herunterladen und Installieren der App

**Für ausführende Benutzer mit iOS-Geräten:**

Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

`[iOS link](https://apple.co/2zXq0aN)`

**Für ausführende Benutzer mit Android-Geräten:**

Klicken Sie auf den folgenden Link (auch in Analytics unter **[!UICONTROL Tools]** > **[!UICONTROL Analytics-Dashboards (mobile App)]** verfügbar) und befolgen Sie die Anweisungen zum Herunterladen, Installieren und Öffnen der Applikation:

`[Android link](https://bit.ly/2LM38Oo)`

Nach dem Herunterladen und der Installation können sich ausführende Benutzer mit ihren vorhandenen Adobe Analytics-Anmeldeinformationen bei der App anmelden. Adobe und Enterprise/Federated IDs werden unterstützt.

![Willkommensbildschirm der App](assets/welcome.png)

## Helfen Sie Führungskräften beim Zugriff auf Ihre Scorecard

1. Lassen Sie ausführende Benutzer sich bei der App anmelden.

   Der Bildschirm **[!UICONTROL Unternehmen]** auswählen wird angezeigt. Auf diesem Bildschirm werden die Unternehmensanmeldungen angezeigt, die der ausführende Benutzer verwenden kann.

1. Bitten Sie sie, auf den Namen des angemeldeten Unternehmens oder der Experience Cloud-Organisation zu tippen, der für die von Ihnen freigegebene Scorecard gilt.

   In der Scorecard-Liste werden dann alle Scorecards angezeigt, die für den ausführenden Benutzer unter diesem Anmeldeunternehmen freigegeben wurden.

1. Lassen Sie sie diese Liste gegebenenfalls nach **[!UICONTROL Zuletzt geändert]** sortieren.

1. Lassen Sie sie auf den Namen der Scorecard tippen, um sie anzuzeigen.

   ![Wählen Sie ein Unternehmen aus.](assets/accesscard.png)


### Scorecard-Benutzeroberfläche erläutern

Erklären Sie dem ausführenden Benutzer, wie Kacheln in den von Ihnen freigegebenen Scorecards angezeigt werden.

![Kacheln erklären](assets/newexplain.png)

![Beispiel-Scorecard](assets/intro_scorecard.png)

Zusätzliche Informationen zu Kacheln:

* Die Granularität der Sparklines hängt von der Länge des Datumsbereichs ab:
* Für einen Tag wird ein stündlicher Trend angezeigt.
   * Für mehr als einen Tag und weniger als ein Jahr wird ein täglicher Trend angezeigt.
   * Für ein Jahr oder mehr wird ein wöchentlicher Trend angezeigt.
   * Die Formel für die Änderung des Prozentwerts ist: Gesamtwert der Metrik (aktueller Datumsbereich) – Gesamtwert der Metrik (Vergleichsdatumsbereich) / Gesamtwert der Metrik (Vergleichsdatumsbereich).
   * Sie können den Anzeigebereich nach unten ziehen, um die Scorecard zu aktualisieren.


1. Tippen Sie auf eine Kachel, um zu zeigen, wie eine detaillierte Aufschlüsselung für die Kachel funktioniert.

   ![Aufschlüsselungsansicht](assets/sparkline.png)

   * Tippen Sie auf einen beliebigen Punkt auf einer Sparkline, um Daten anzuzeigen, die diesem Punkt auf der Linie zugeordnet sind.

   * In einer Tabelle werden Daten zu den der Kachel hinzugefügten Dimensionen angezeigt. Tippen Sie auf den Abwärtspfeil, um Dimensionen auszuwählen. Wenn der Kachel keine Dimension hinzugefügt wurde, werden in der Tabelle Diagrammdaten angezeigt.

1. Um die Datumsbereiche für die Scorecard zu ändern, tippen Sie auf die Kopfzeile „Datum“ und wählen Sie die gewünschte Kombination aus Primär- und Vergleichsdatumsbereich aus.

   ![Datum ändern](assets/changedate.png)

## App-Voreinstellungen ändern

Um die Voreinstellungen zu ändern, tippen Sie auf die Option **[!UICONTROL Voreinstellungen]** oben. In den Voreinstellungen können Sie die biometrische Anmeldung aktivieren oder Sie können die App wie folgt für den Dunkelmodus einstellen:

![Dunkelmodus](assets/darkmode.png)

## Fehlerbehebung

Wenn sich der ausführende Benutzer anmeldet und eine Meldung angezeigt wird, dass nichts freigegeben wurde, kann das folgende Gründe haben:

![Nichts freigegeben](assets/nothing.png)

* Der ausführende Benutzer hat möglicherweise die falsche Analytics-Instanz ausgewählt oder
* Die Scorecard wurde möglicherweise nicht für den ausführenden Benutzer freigegeben.

Stellen Sie sicher, dass sich der ausführende Benutzer bei der richtigen Adobe Analytics-Instanz anmelden kann und dass die Scorecard freigegeben wurde.

### Fehler melden

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Fehler aus. Geben Sie im Formular zur Meldung eines Fehlers im obersten Feld Ihre E-Mail-Adresse und im Feld darunter eine Beschreibung des Fehlers an. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um den Bericht zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.

![Fehler melden](assets/newbug.png)

### Feedback hinterlassen

1. Tippen Sie auf das Einstellungssymbol oben recht im App-Bildschirm.
1. Tippen Sie auf dem Bildschirm **[!UICONTROL Einstellungen]** auf die Option **[!UICONTROL Feedback]**.
1. Tippen Sie, um die Optionen zum Hinterlassen von Feedback anzuzeigen.

   ![Einstellungsbildschirm](assets/settings.png)

### Verbesserungsvorschläge

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Vorschlag aus. Geben Sie im Vorschlagsformular im obersten Feld Ihre E-Mail-Adresse und im Feld darunter eine Beschreibung des Vorschlags an. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um den Vorschlag zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.

### Frage stellen

Tippen Sie auf die Option und geben Sie im obersten Feld Ihre E-Mail-Adresse und im Feld darunter Ihre Frage an. Ein Screenshot wird automatisch an die Nachricht angehängt. Sie können den Screenshot jedoch löschen, indem Sie auf das **X** im Bild des Anhangs tippen. Außerdem können Sie eine Bildschirmaufzeichnung erstellen, weitere Screenshots hinzufügen oder Dateien anhängen. Um die Frage zu senden, tippen Sie auf das Papierfliegersymbol oben rechts im Formular.

>[!IMPORTANT]
>
>Seit Oktober 2020 führt Adobe schrittweise eine Reihe von Verbesserungen durch, um die Leistung der Applikation „Adobe Analytics-Dashboards“ zu optimieren. Diese Erweiterungen konzentrieren sich auf das Caching historischer Analytics-Daten, die zum Ausfüllen von Scorecards mit Datumsangaben (außer dem aktuellen Tag) verwendet werden. Diese Daten werden bis zu 24 Stunden lang in einem sicheren öffentlichen Microsoft Azure-Konto in der Cloud zwischengespeichert. Wenden Sie sich an Ihren CSM, wenn Sie diese Leistungsverbesserungsfunktionen nicht in Anspruch nehmen möchten.
