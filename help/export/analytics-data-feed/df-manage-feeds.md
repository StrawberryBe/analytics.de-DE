---
title: Daten-Feed-Benutzeroberfläche
description: Erfahren Sie, wie Sie in der Daten-Feed-Oberfläche navigieren.
feature: Data Feeds
exl-id: 4d4f0062-e079-48ff-9464-940c6425ad54
source-git-commit: 84bdeb5d502e46c922fc5123fcdd5b6819426c0e
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 77%

---

# Verwalten von Daten-Feeds

Mit dem Daten-Feed-Manager können Sie Daten-Feeds für Ihre Organisation erstellen, bearbeiten und löschen. Wenn Sie berechtigt sind, auf den Daten-Feed-Manager zuzugreifen, können Sie Daten-Feeds für alle Report Suites verwalten, die für Sie sichtbar sind.

Im Folgenden finden Sie ein Video zur Benutzeroberfläche für die Verwaltung von Daten-Feeds:

>[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

Gehen Sie wie folgt vor, um auf das Daten-Feed-Management zuzugreifen:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Wählen Sie das 9-Quadrat-Symbol oben rechts aus und wählen Sie dann [!UICONTROL **Analytics**].
1. Navigieren Sie in der oberen Navigationsleiste zu [!UICONTROL **Admin**] > [!UICONTROL **Datenfeeds**].

## Navigieren in der Benutzeroberfläche

Wenn Sie zur Seite „Daten-Feed-Manager“ gelangen, sieht die Oberfläche wie folgt aus:

![Datenfeeds](assets/feeds.png)

Wenn keine Feeds eingerichtet wurden, wird auf der Seite die Schaltfläche [!UICONTROL Neuen Daten-Feed erstellen] angezeigt.

### Filter und Suche

Suchen Sie mithilfe von Suchvorgängen oder Filtern nach einem bestimmten Feed.

* Geben Sie im Suchfeld den Namen eines Feeds ein. In der Liste der verfügbaren Feeds werden nur die Feeds angezeigt, die übereinstimmen.

* Klicken Sie ganz links auf das Filtersymbol, um die Filteroptionen ein- oder auszublenden. Filter sind nach Kategorie geordnet. Sie können Filterkategorien reduzieren oder erweitern. Aktivieren Sie das Kontrollkästchen neben den Filtern, die Sie anwenden möchten.

  ![Filter](assets/filters.png)

### Feeds und Aufträge

Wählen Sie die [!UICONTROL **Aufträge**] um einzelne Aufträge anzuzeigen, die von jedem Ihrer Feeds erstellt werden. Siehe [Verwalten von Daten-Feed-Aufträgen](df-manage-jobs.md).

### Fügen Sie

Die [!UICONTROL Hinzufügen] -Schaltfläche können Sie einen neuen Feed erstellen. Siehe [Erstellen eines Daten-Feeds](create-feed.md) für weitere Informationen.

### Spalten

Jeder erstellte Feed zeigt mehrere Spalten mit Informationen an. Wählen Sie eine Spaltenüberschrift aus, um sie in aufsteigender Reihenfolge zu sortieren. Wählen Sie eine Spaltenüberschrift erneut aus, um sie in absteigender Reihenfolge zu sortieren. Wenn eine bestimmte Spalte nicht angezeigt wird, klicken Sie oben rechts auf das Spaltensymbol.

![Spaltensymbol](assets/cols.jpg)

* **Feed-Name**: Erforderliche Spalte. Zeigt den Feed-Namen an.
* **Feed-ID**: Zeigt die Feed-ID an, eine eindeutige Kennung.
* **Report Suite**: Die Report Suite, aus der der Feed Daten referenziert.
* **Report Suite-ID**: Die eindeutige Kennung der Report Suite.
* **Datenspalten**: Gibt an, welche Datenspalten für den Feed aktiv sind. In den meisten Fällen gibt es so viele Spalten, dass sie in diesem Format nicht alle angezeigt werden können.
* **Intervall**: Gibt an, ob der Feed stündlich oder täglich ist.
* **Zieltyp**: Der Zieltyp für den Feed. Zum Beispiel Amazon S3, GCP oder Azure.
* **Zielhost**: Der Speicherort der Datei.
* **Inhaber**: Das Benutzerkonto, über das der Feed erstellt wurde.
* **Status:** Der Status des Feeds.
   * Aktiv: Der Feed ist betriebsfähig.
   * Genehmigung ausstehend: Unter bestimmten Umständen muss ein Feed von Adobe genehmigt werden, bevor er Aufträge generieren kann.
   * Gelöscht: Der Feed wurde gelöscht.
   * Abgeschlossen: Die Verarbeitung des Feeds wurde abgeschlossen. Ein abgeschlossener Feed kann bearbeitet, angehalten und abgebrochen werden.
   * Ausstehend: Der Feed wurde erstellt, ist aber noch nicht aktiv. Feeds bleiben für eine kurze Übergangszeit in diesem Zustand.
   * Inaktiv: Entspricht einem Status „angehalten“. Wenn der Feed reaktiviert wird, wird die Bereitstellung von Aufträgen an derselben Stelle fortgesetzt.
* **Zuletzt geändert**: Das Datum, an dem der Feed zuletzt geändert wurde. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Verschiebung angezeigt.
* **Startdatum**: Das Datum des ersten Auftrags für diesen Feed. Datum und Uhrzeit werden in der Zeitzone der Report Suite mit GMT-Verschiebung angezeigt.
* **Enddatum**: Das Datum des letzten Auftrags für diesen Feed. Laufende Daten-Feeds haben kein Enddatum.

## Daten-Feed-Aktionen

Aktivieren Sie das Kontrollkästchen neben einem Daten-Feed, um verfügbare Aktionen anzuzeigen.

* **Auftragsverlauf**: Zeigen Sie alle Aufträge an, die mit diesem Daten-Feed verknüpft sind. Leitet Sie automatisch zur [Oberfläche für die Verwaltung von Aufträgen](df-manage-jobs.md) weiter.
* **Löschen**: Löscht den Daten-Feed und ändert dessen Status zu [!UICONTROL Gelöscht].
* **Kopieren**: Ermöglicht die [Erstellung eines neuen Feeds](create-feed.md) mit allen Einstellungen des aktuellen Feeds. Ein Daten-Feed kann nicht kopiert werden, wenn mehrere Feeds ausgewählt sind.
* **Anhalten**: Beendet die Verarbeitung für den Feed und setzt dessen Status auf [!UICONTROL Inaktiv].
* **Aktivieren**: Nur für inaktive Feeds verfügbar. Ruft die Verarbeitungsdaten an der Stelle ab, an der aufgehört wurde, und füllt ggf. alle Daten rückwirkend auf.