---
title: Data Feed-Benutzeroberfläche
description: Erfahren Sie, wie Sie in der Data Feed-Oberfläche navigieren.
translation-type: tm+mt
source-git-commit: c9b3471b138c2e056a5abadb4ace6bb4eccd1d72

---


# Verwalten von Datenfeeds

Mit dem Data Feed Manager können Sie Datenfeeds für Ihr Unternehmen erstellen, bearbeiten und löschen. Wenn Sie berechtigt sind, auf den Data Feed Manager zuzugreifen, können Sie Datenfeeds für alle Report Suites verwalten, die für Sie sichtbar sind.

Gehen Sie wie folgt vor, um auf die Datenfeed-Verwaltung zuzugreifen:

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
2. Klicken Sie oben rechts auf das 9-Raster-Menü und dann auf [!UICONTROL Analytics].
3. Klicken Sie im oberen Menü auf [!UICONTROL Admin] &gt; [!UICONTROL Datenfeeds].

![Datenfeed-Menü](assets/AdminMenu.png)

## Navigieren in der Oberfläche

Wenn Sie zur Seite "Data Feed Manager"gelangen, sieht die Oberfläche wie folgt aus:

![Datenfeeds](assets/feeds.png)

Wenn keine Feeds eingerichtet wurden, wird auf der Seite die Schaltfläche [!UICONTROL Neuen Daten-Feed erstellen] angezeigt.

### Filter und Suche

Verwenden Sie Filter und suchen Sie nach dem gewünschten Feed.

Klicken Sie ganz links auf das Filtersymbol, um die Filteroptionen ein- oder auszublenden. Filter sind nach Kategorie geordnet. Klicken Sie auf das Chevron, um die Filterkategorien zu reduzieren oder zu erweitern. Markieren Sie das Kontrollkästchen, um diesen Filter anzuwenden.

![Filter](assets/filters.jpg)

Suchen Sie nach einem Feed anhand des Namens.

![Durchsuchen](assets/search.jpg)

### Feeds und Aufträge

Klicken Sie auf die Registerkarte "Aufträge", um einzelne Aufträge anzuzeigen, die von den einzelnen Feeds erstellt werden. Siehe Datenfeed-Aufträge [verwalten](df-manage-jobs.md).

### Fügen Sie

Klicken Sie in der Nähe der Registerkarten Feeds und Aufträge auf die Schaltfläche + [!UICONTROL Hinzufügen] , um einen neuen Feed zu erstellen. Weitere Informationen finden Sie unter Feed [hinzufügen](create-feed.md) .

### Spalten

Jeder erstellte Feed zeigt mehrere Spalten mit Informationen dazu an. Klicken Sie auf eine Spaltenüberschrift, um sie in aufsteigender Reihenfolge zu sortieren. Klicken Sie erneut auf eine Spaltenüberschrift, um sie in absteigender Reihenfolge zu sortieren. Wenn eine bestimmte Spalte nicht angezeigt wird, klicken Sie auf das Spaltensymbol oben rechts.

![Spaltensymbol](assets/cols.jpg)

* **Feed-Name**: Erforderliche Spalte. Zeigt den Feed-Namen an.
* **Feed-ID**: Zeigt die Feed-ID an, eine eindeutige ID.
* **Report Suite**: Die Report Suite, aus der der Feed Daten referenziert.
* **Report Suite-ID**: Die eindeutige Kennung der Report Suite.
* **Datenspalten**: Welche Datenspalten sind für den Feed aktiv? In den meisten Fällen gibt es zu viele Spalten, die in diesem Format angezeigt werden können.
* **Intervall**: Geben Sie an, ob der Feed stündlich oder täglich gesendet wird.
* **Zieltyp**: Der Zieltyp für den Feed. Zum Beispiel FTP, Amazon S3 oder Azurblau.
* **Zielhost**: Der Speicherort der Datei. Beispiel, `ftp.example.com`.
* **Inhaber**: Das Benutzerkonto, das den Feed erstellt hat.
* **Status**: Der Status des Feeds.
   * Aktiv: Der Feed ist betriebsbereit.
   * Genehmigung ausstehend: Unter bestimmten Umständen muss ein Feed von Adobe genehmigt werden, bevor er Aufträge generieren kann.
   * Gelöscht: Der Feed wird gelöscht.
   * Abgeschlossen: Die Verarbeitung des Feeds wurde abgeschlossen. Ein abgeschlossener Feed kann bearbeitet, ausgesetzt oder abgebrochen werden.
   * Ausstehend: Der Feed wird erstellt, aber noch nicht aktiv. Feeds bleiben für eine kurze Übergangszeit in diesem Zustand.
   * Inaktiv: Entspricht einem Status "angehalten"oder "im Halten". Wenn der Feed reaktiviert wird, wird die Bereitstellung von Aufträgen beim Beenden fortgesetzt.
* **Zuletzt geändert**: Das Datum, an dem der Feed zuletzt geändert wurde. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Versatz angezeigt.
* **Startdatum**: Das Datum des ersten Auftrags für diesen Feed. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Versatz angezeigt.
* **Enddatum**: Das Datum des letzten Auftrags für diesen Feed. Laufende Datenfeeds haben kein Enddatum.

## Datenfeed-Aktionen

Aktivieren Sie das Kontrollkästchen neben einem Datenfeed, um verfügbare Aktionen anzuzeigen.

* **Auftragsverlauf**: Zeigen Sie alle Aufträge an, die mit diesen Datenfeeds verknüpft sind. Leitet Sie automatisch zur [Oberfläche](df-manage-jobs.md)für Aufträge verwalten.
* **Löschen**: Löscht den Datenfeed und stellt dessen Status auf " [!UICONTROL Gelöscht]"ein.
* **Kopieren**: Ermöglicht die [Erstellung eines neuen Feeds](create-feed.md) mit allen Einstellungen des aktuellen Feeds. Ein Datenfeed kann nicht kopiert werden, wenn mehrere ausgewählt sind.
* **Anhalten**: Beendet die Verarbeitung für den Feed und legt dessen Status auf [!UICONTROL Inaktiv]fest.
* **Aktivieren**: Nur für inaktive Feeds verfügbar. Ruft die Verarbeitungsdaten an der Stelle ab, an der sie aufgehört wurden, und füllt ggf. alle Daten auf.
