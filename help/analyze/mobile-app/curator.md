---
description: Anleitung zum Einrichten der App-Scorecards.
title: Adobe Analytics Mobile App Curator Guide
translation-type: tm+mt
source-git-commit: 286ab1e043d8f54681a4df8171c244a98d0e0d2b

---



# BETA: Kuratorleitfaden für die mobile Analytics-App


## Einführung

Die mobile Adobe Analytics-App bietet jederzeit und überall Einblicke aus Adobe Analytics.   Die App ermöglicht Benutzern auf Mobilgeräten Zugriff auf intuitive Scorecards, die Sie über die Desktop-Benutzeroberfläche von Adobe Analytics erstellen und freigeben. Bei Scorecards handelt es sich um eine Sammlung von Schlüsselmetriken und anderen Komponenten, die in einem gekachelten Layout dargestellt sind und auf die Sie für detailliertere Aufschlüsselungen und Trendberichte tippen können. Sie können Scorecards entsprechend den für Sie wichtigsten Daten anpassen. Die mobile App wird auf iOS- und Android-Betriebssystemen unterstützt.

## Informationen zu diesem Handbuch

Dieses Handbuch soll Kuratoren von Adobe Analytics-Daten bei der Konfiguration von Scorecards für ihre leitenden Benutzer in der Analytics Mobile App unterstützen. Kuratoren können organisatorische Administratoren oder Personen in anderen Rollen sein, die für die Einrichtung von App-Scorecards zuständig sind. Diese ermöglichen es leitenden Benutzern, eine umfassende Darstellung wichtiger Zusammenfassungsdaten schnell und einfach auf ihren eigenen Mobilgeräten anzuzeigen. Obwohl geschäftsführende Benutzer Endbenutzer der mobilen Analytics-App sind, hilft dieses Handbuch Datenkuratoren bei der effektiven Einrichtung der App für diese Benutzer.


## Glossar der Begriffe

Die folgende Tabelle beschreibt die Begriffe zum Verständnis der Zielgruppe, Funktionen und Funktionsweise der mobilen Analytics-App.

|Begriff|Definition||—|—||Consumer| Executive persona sieht wichtige Metriken und Einblicke aus Analytics auf einem Mobilgerät an||Kurator|Datenliteratpersona, der Erkenntnisse aus Analytics findet und verteilt und die vom Verbraucher anzuzeigenden Scorecards konfiguriert||Kuratierung|Der Vorgang der Erstellung oder Bearbeitung einer mobilen Scorecard mit relevanten Metriken, Dimensionen und anderen Komponenten für den Verbraucher||Scorecard|Eine mobile App-Ansicht mit einer oder mehreren Kacheln||Kachel|Ein Rendering für eine Metrik in einer Scorecard-Ansicht||Aufschlüsselung|Eine sekundäre Ansicht, die durch Tippen auf eine Kachel in der Scorecard aufgerufen werden kann. Diese Ansicht wird bei der auf der Kachel angezeigten Metrik erweitert und optional bei weiteren Aufschlüsselungsdimensionen berichtet.||Datumsbereich|Der primäre Datumsbereich für Berichte zu mobilen Anwendungen||Vergleichsdatumsbereich|Der Datumsbereich, der mit dem primären Datumsbereich verglichen wird|

 
## Eine Wertungsliste für Führungskräfte erstellen

Eine mobile Scorecard zeigt wichtige Datenvisualisierungen für Benutzer in einem gekachelten Layout an, wie nachfolgend gezeigt:


Als Kurator für diese Scorecard können Sie mit dem Scorecard Builder konfigurieren, welche Kacheln auf der Scorecard für Ihren Kunden angezeigt werden. Sie können auch konfigurieren, wie die detaillierten Ansichten oder Aufschlüsselungen angepasst werden können, sobald auf die Kacheln getippt wird. Die Scorecard Builder-Oberfläche ist unten dargestellt:

Zur Erstellung des Scorecard müssen Sie folgende Schritte ausführen:

1. Greifen Sie auf die Vorlage "Leeres mobiles Scorecard"zu.
2. Konfigurieren Sie die Scorecard mit Daten und speichern Sie sie.

![Beispiel-Scorecard](/help/analyze/mobile-app/assets/intro_scorecard.png)



### Zugriff auf die Vorlage "Leeres mobiles Scorecard"

Sie haben folgende Möglichkeiten, auf die Vorlage Blank Mobile Scorecard zuzugreifen:

**Neues Projekt erstellen**

1. Öffnen Sie Adobe Analytics und klicken Sie auf die Registerkarte Arbeitsbereich.
2. Klicken Sie auf die Schaltfläche "Neues Projekt erstellen"und wählen Sie die Projektvorlage "Leeres mobiles Scorecard"aus.
3. Klicken Sie auf die Schaltfläche **erstellen**.

*Hinweis: Wenn Sie die Vorlage Blank Mobile Scorecard nicht sehen, wie unten gezeigt, wurde Ihr Unternehmen noch nicht für Beta aktiviert. Wenden Sie sich an Ihren Kundenbetreuer.*


**Projekt hinzufügen**

Klicken Sie im Bildschirm "Projekte"auf der Registerkarte "Komponenten"auf die Schaltfläche "Hinzufügen"und wählen Sie "Mobile Scorecard"aus.




**Analytics-Werkzeuge verwenden**

Klicken Sie in Analytics auf das Extras-Menü und wählen Sie "Mobile App". Klicken Sie im nachfolgenden Bildschirm auf die Schaltfläche "Scorecard erstellen".

### Konfigurieren des Scorecards mit Daten und Speichern

So implementieren Sie die Scorecard-Vorlage:

1. Geben Sie unter Eigenschaften (in der rechten Leiste) eine Projekt-Report Suite an, aus der Sie Daten verwenden möchten.



2. Um eine neue Kachel zu Ihrer Scorecard hinzuzufügen, ziehen Sie eine Metrik aus dem linken Bereich und legen Sie sie in der Zone Metriken hierher ziehen und ablegen ab. Sie können auch eine Metrik zwischen zwei Kacheln einfügen, indem Sie einen ähnlichen Arbeitsablauf verwenden.


   Von jeder Kachel aus können Sie auf eine detaillierte Ansicht zugreifen, die zusätzliche Informationen zur Metrik anzeigt, z. B. die obersten Elemente für eine Liste der zugehörigen Dimensionen.


3. Um einer Metrik eine zugehörige Dimension hinzuzufügen, ziehen Sie eine Dimension aus dem linken Bereich und legen Sie sie auf einer Kachel ab. Sie können z. B. der Metrik "Unique Visitors"geeignete Dimensionen (wie in diesem Beispiel DMA-Region) hinzufügen, indem Sie sie auf die Kachel ziehen und dort ablegen. Dimensionen, die Sie hinzufügen, werden im Unterteilungsabschnitt der kachelspezifischen Eigenschaften angezeigt. Sie können jeder Kachel mehrere Dimensionen hinzufügen.


   *Hinweis: Sie können allen Kacheln auch eine Dimension hinzufügen, indem Sie sie auf der Arbeitsfläche "Scorecard"ablegen. *

   Wenn Sie im Scorecard Builder auf eine Kachel klicken, zeigt die rechte Leiste die Eigenschaften und Eigenschaften an, die mit dieser Kachel verbunden sind. In dieser Leiste können Sie einen neuen Titel für die Kachel angeben und alternativ die Kachel konfigurieren, indem Sie Komponenten angeben, anstatt sie aus der linken Leiste zu ziehen und abzulegen.








   Wenn Sie auf Kacheln klicken, wird in einem dynamischen Popup angezeigt, wie die Aufschlüsselungsansicht dem Benutzer in der App angezeigt wird. Wenn keine Dimension auf die Kachel angewendet wurde, ist die Aufschlüsselungsdimension je nach Standarddatumsbereich Stunden oder Tage.




   Wenn Sie auf eine Kachel klicken, wird die Aufschlüsselungsansicht für diese Kachel neben der Scorecard angezeigt.
Beachten Sie, dass jede der Kachel hinzugefügte Dimension in einer Dropdown-Liste in der Detailansicht der App angezeigt wird. Der Exekutivbenutzer kann dann aus den in der Dropdownliste aufgelisteten Optionen auswählen.

4. Um Segmente auf einzelne Kacheln anzuwenden, ziehen Sie ein Segment aus dem linken Bereich und legen es direkt über die Kachel ab. Wenn Sie das Segment auf alle Kacheln in der Scorecard anwenden möchten, legen Sie die Kachel auf der Scorecard ab.

5. Um eine Komponente zu entfernen, die auf die gesamte Scorecard angewendet wird, klicken Sie auf eine beliebige Stelle außerhalb der Kacheln auf die Scorecard und entfernen Sie sie, indem Sie auf das X klicken, das angezeigt wird, wenn Sie den Mauszeiger über die Komponente bewegen, wie unten für das Segment Mobile Customers dargestellt:

6. Unter Eigenschaften von Scorecard können Sie optional auch Folgendes angeben:

   * Ein Standarddatumsbereich. Die hier angegebenen Bereiche gelten für den ersten Zugriff des Benutzers auf die Scorecard in seiner App.

   * Ein Vergleichsdatumsbereich

   * Alle Segmente, die für die gesamte Wertungsliste gelten sollen

7. Um der Scorecard einen Namen zu geben, klicken Sie auf den Namespace oben links im Bildschirm und geben Sie den neuen Namen ein.

## Scorecard freigeben

So geben Sie die Scorecard für einen Executive-Benutzer frei:

1. Klicken Sie auf das Menü "Freigeben"und wählen Sie "Freigeben-Scorecard".

2. Füllen Sie im Freigabeformular die Felder aus, um:

   * Bezeichnung der Scorecard
   * Beschreibung des Scorecard
   * Hinzufügen relevanter Tags
   * Empfänger für die Scorecard angeben
   * Wählen Sie die Option "Eingebettete Komponenten mit Empfängern teilen", um sicherzustellen, dass der exekutive Benutzer Zugriff auf alle Komponenten in der Scorecard hat.

3. Klicken Sie auf Freigabe.

Nachdem Sie eine Scorecard freigegeben haben, können Ihre Empfänger auf diese in ihrer mobilen Analytics-App zugreifen. Wenn Sie nachfolgende Änderungen am Scorecard im Scorecard Builder vornehmen, werden diese automatisch in der freigegebenen Scorecard aktualisiert. Die Änderungen werden dann angezeigt, nachdem die Scorecard in der App aktualisiert wurde.

*Hinweis: Wenn Sie die Scorecard durch Hinzufügen neuer Komponenten aktualisieren, sollten Sie die Scorecard erneut freigeben (und die Option "Embedded-Komponenten automatisch mit Empfängern teilen"aktivieren), um sicherzustellen, dass Ihre Manager-Benutzer Zugriff auf diese Änderungen haben.*


## Einrichten von Executive-Benutzern mit der App

In einigen Fällen benötigen Benutzer, die sie ausführen, möglicherweise zusätzliche Unterstützung, um auf die App zuzugreifen und sie zu verwenden. Dieser Abschnitt enthält Informationen, die Sie bei der Bereitstellung dieser Hilfe unterstützen.

### Zugriff für Führungskräfte

Um leitende Benutzer beim Zugriff auf Ihre Scorecards in der App zu unterstützen, stellen Sie Folgendes sicher:

    * Die Mindestanforderungen an das mobile Betriebssystem auf ihren Geräten sind iOS Version 10 oder höher oder Android Version 4.4 (KitKat) oder höher
    * Sie haben eine gültige Anmeldung bei Adobe Analytics
    * Sie haben für sie korrekte mobile Scorecards erstellt und teilen diese mit ihnen.
    * Sie haben Zugriff auf den Arbeitsbereich für Analysen und die Report Suite, auf
    der die Scorecard basiert* Sie haben Zugriff auf die Komponenten, die die Scorecard enthält. Hinweis: Sie können eine Option auswählen, wenn Sie Ihre Scorecards freigeben, um eingebettete Komponenten automatisch für Empfänger freizugeben.


### Hilfe für Benutzer, die die App verwenden

1. Um leitenden Benutzern zu helfen, stellen Sie sicher, dass sie die App gemäß ihrem Betriebssystem für Mobilgeräte herunterladen und installieren können.

   **iOS**



   **Android**






2. Helfen Sie ihnen beim Zugriff auf Ihre Scorecard. Nachdem sich Benutzer mit leitenden Funktionen bei der App angemeldet haben, wird der Bildschirm "Unternehmen auswählen"angezeigt. Dieser Bildschirm listet die Anmeldeunternehmen auf, zu denen der geschäftsführende Benutzer gehört. Um ihnen beim Aufrufen des Scorecard zu helfen:

* Tippen Sie auf den Namen des angemeldeten Unternehmens oder der Experience Cloud-Organisation, der für die freigegebene Scorecard gilt. In der Scorecard-Liste werden dann alle Scorecards angezeigt, die mit der Geschäftsführung unter dieser Firmenanmeldung geteilt wurden.
* Hilft ihnen, diese Liste nach der neuesten Änderung zu sortieren, falls zutreffend.
* Tippen Sie auf den Namen der Scorecard, um sie anzuzeigen.


1. Wählen Sie ein Unternehmen aus, indem Sie darauf tippen.
2. Tippen Sie auf eine Scorecard aus der Scorecard-Liste.

   Hinweis: Wenn sich der geschäftsführende Benutzer anmeldet und eine Meldung angezeigt wird, dass nichts freigegeben wurde:

   * Der geschäftsführende Benutzer hat möglicherweise die falsche Analytics-Instanz ausgewählt
   * Die Scorecard wurde nicht für den Exekutivbenutzer freigegeben

3. Zeigt, wie Kacheln in der freigegebenen Scorecard angezeigt werden.



   Zusätzliche Informationen zu Kacheln:

       
 * Die Granularität der Wortgrafiken hängt von der Länge des Datumsbereichs ab:       * Ein Tag zeigt einen stündlichen Trend
     * Mehr als ein Tag und weniger als ein Jahr zeigt einen täglichen Trend
 .     * Ein Jahr oder mehr zeigt einen wöchentlichen Trend
 .     * Die Formel zur prozentualen Wertänderung ist Metriksumme (aktueller Datumsbereich) - Metriksumme (Vergleichsdatumsbereich) / Metriksumme (Vergleichsdatumsbereich).
       * Sie können den Bildschirm nach unten ziehen, um die Scorecard zu aktualisieren.
   

4. Tippen Sie auf eine Kachel, um anzuzeigen, wie eine detaillierte Aufschlüsselung oder ein Trendbericht für die Kachel funktioniert.


5. So ändern Sie Datumsbereiche für Ihre Wertungsliste:



   *1. Tippen Sie auf die Kopfzeile Datum. 2. Tippen Sie im Bildschirm "Datumsbereich"auf den Zeitraum, mit dem Sie arbeiten möchten.*

   Je nach dem Zeitraum, auf den Sie tippen (Tag, Woche, Monat oder Jahr), sehen Sie zwei Optionen für Datumsbereiche: entweder den aktuellen Zeitraum oder den unmittelbar davor liegenden Zeitraum. Tippen Sie auf eine dieser beiden Optionen, um den ersten Bereich auszuwählen. Tippen Sie in der Liste "COMPARE TO"auf eine der angezeigten Optionen, um die Daten dieses Zeitraums mit dem ersten ausgewählten Datumsbereich zu vergleichen. Tippen Sie oben rechts im Bildschirm auf Fertig. Das Feld Datumsbereiche und die Kacheln der Scorecard werden mit den neuen Vergleichsdaten aus den ausgewählten Bereichen aktualisiert.


6. So hinterlassen Sie Feedback zu dieser App:


   1. Tippen Sie auf das Benutzersymbol oben rechts im App-Bildschirm.
   2. Tippen Sie im Bildschirm "Mein Konto"auf die Option Feedback.
   3. Tippen Sie auf , um die Optionen zum Verlassen des Feedbacks anzuzeigen.



*Tippen Sie oben rechts auf das Symbol Benutzer. 2. Tippen Sie auf den Feedback-Typ. 3. Tippen Sie auf die entsprechende Feedback-Option.*








So melden Sie einen Fehler:

Tippen Sie auf die Option und wählen Sie eine Unterkategorie des Fehlers. Geben Sie im Formular zur Meldung eines Fehlers im oberen Feld Ihre E-Mail-Adresse und Ihre Beschreibung des Fehlers im Feld darunter ein. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können dies jedoch löschen, indem Sie auf das X im Anlagenbild tippen. Sie haben auch Optionen zum Aufnehmen von Screenshots, Hinzufügen von Screenshots oder Anhängen von Dateien. Um den Bericht zu senden, tippen Sie oben rechts im Formular auf das Papierebenensymbol.














Verbesserungsvorschläge:

Tippen Sie auf die Option und wählen Sie eine Unterkategorie für den Vorschlag aus. Geben Sie im Empfehlungsformular Ihre E-Mail-Adresse im oberen Feld und Ihre Beschreibung des Fehlers im Feld darunter ein. Ein Screenshot Ihrer Kontoinformationen wird automatisch an die Nachricht angehängt. Sie können dies jedoch löschen, indem Sie auf das X im Anlagenbild tippen. Sie haben auch Optionen zum Aufnehmen von Screenshots, Hinzufügen von Screenshots oder Anhängen von Dateien. Um den Vorschlag zu senden, tippen Sie oben rechts im Formular auf das Papierebenensymbol.

So stellen Sie eine Frage:

Tippen Sie auf die Option und geben Sie Ihre E-Mail-Adresse im oberen Feld und Ihre Frage im Feld darunter ein. Ein Screenshot wird automatisch an die Nachricht angehängt. Sie können dies jedoch löschen, indem Sie auf das X im Anlagenbild tippen. Sie haben auch Optionen zum Aufnehmen von Screenshots, Hinzufügen von Screenshots oder Anhängen von Dateien. Um die Frage zu senden, tippen Sie oben rechts im Formular auf das Papierebenensymbol.
