---
title: Erste Schritte mit Datenquellen
description: Laden Sie Beispieldaten in eine Entwicklungs-Report Suite hoch.
exl-id: d9f74f55-abbb-4ceb-b4db-8d3c32aacd4a
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Erste Schritte mit Datenquellen

Sie können diese Schritte ausführen, um einfach Beispieldaten in eine Entwicklungs-Report Suite hochzuladen und den Workflow in Aktion zu sehen. Sobald Sie den Prozess verstanden haben, können Sie ihn erweitern und speziell auf die Implementierung Ihres Unternehmens anpassen.

>[!IMPORTANT]
>
>Führen Sie diese Schritte mit einer Entwicklungs- oder Test-Report Suite aus. Daten, die über Datenquellen hochgeladen wurden, werden **dauerhaft**. Dies wirkt sich auf die Produktions-Report Suite-Daten aus, wenn sie dorthin hochgeladen werden.

1. Bei Adobe Analytics über anmelden [https://experience.adobe.com](https://experience.adobe.com).
1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Datenquellen]**.
1. Wählen Sie mithilfe der Dropdownliste oben rechts eine Entwicklungs-Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Erstellen]** Schaltfläche oben links.
1. under [!UICONTROL Kategorie auswählen], wählen Sie &quot;[!UICONTROL Generisch]&quot;und unter [!UICONTROL Typ auswählen], wählen Sie &quot;[!UICONTROL Generische Datenquelle (nur Zusammenfassungsdaten)]&quot;.
1. Klicks **[!UICONTROL Aktivieren]**. Ein Popup-Fenster wird geöffnet, in dem die [!UICONTROL Datenquellen-Aktivierungsassistent].
   1. Schritt 1: Geben Sie der Datenquelle einen Namen und klicken Sie auf das Kontrollkästchen Haftungsausschluss .
   1. Schritt 2: Dieser Schritt wurde in früheren Versionen von Adobe Analytics häufiger verwendet. Aktivieren Sie ein Kontrollkästchen und geben Sie einen beliebigen Wert in das Textfeld neben dem Feld ein.
   1. Schritt 3: Wählen Sie die Metrik aus, die in Ihre Datenquellenvorlagendatei aufgenommen werden soll. Wählen Sie &quot;Ereignis 1&quot;aus der Dropdown-Liste aus.
   1. Schritt 4: Dieser Schritt wurde in früheren Versionen von Adobe Analytics besser genutzt. Aktivieren Sie ein Kontrollkästchen und geben Sie einen beliebigen Wert in das Textfeld neben dem Feld ein.
   1. Schritt 5: Wählen Sie die Dimension aus, die in Ihre Datenquellenvorlagendatei aufgenommen werden soll. Wählen Sie &quot;eVar1&quot;aus der Dropdown-Liste aus.
   1. Schritt 6: Überprüfen Sie die Zusammenfassung mit den Dimensionen und Metriken, die in der Vorlagendatei enthalten sind.
   1. Schritt 7: Klicken Sie auf die **[!UICONTROL Herunterladen]** zum Herunterladen der Vorlagendatei für Datenquellen. Beachten Sie auch die Anmeldedaten für die FTP-Site, da sie in Kürze verwendet werden.
1. Die Datenquelle wird jetzt erstellt. Der nächste Schritt besteht darin, ihr Daten zur Verarbeitung zu geben. Öffnen Sie die heruntergeladene Datei in Ihrem gewünschten Texteditor.
1. Die Vorlagendatei enthält drei Zeilen, zwei Kommentarzeilen (beginnend mit &quot;`#`&quot;) und einer Kopfzeile:

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 2)
   #    eVar1    event1
   Date    Evar 1    Event 1
   ```

1. Geben Sie in mehrere Datenzeilen ein und trennen Sie jeden Eintrag durch einen Tab. Verwenden Sie keine Leerzeichen oder Kommas, um Werte zu trennen.
   * Die erste Spalte ist das Datum im folgenden Format: `MM/DD/YYYY/HH/mm/SS`.
   * Die zweite Spalte ist der Textwert, den Sie in eVar1 einbeziehen möchten.
   * Die dritte Spalte ist der Betrag, um den Sie Ereignis 1 erhöhen möchten.

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 5)
   #    eVar1    event1
   Date    Evar 1    Event 1
   09/07/YYYY/11/23/00    Data source example value    3
   09/07/YYYY/15/59/00    Another data source value    18
   ```

1. Speichern Sie die Datei. Sie können ihr optional einen anderen Dateinamen geben, falls gewünscht. Nach dem Speichern der Datei können Sie den Texteditor schließen.
1. Navigieren Sie in Windows Explorer, Finder oder Ihrem FTP-Client Ihrer Wahl zu [ftp://ftp.omniture.com](ftp://ftp.omniture.com).
1. Wenn Sie zur Eingabe der Anmeldedaten aufgefordert werden, verwenden Sie den Benutzernamen und das Kennwort, die im letzten Schritt des Datenquellen-Erstellungsassistenten angegeben wurden. Sie können erneut darauf verweisen, indem Sie zu [!UICONTROL Datenquellen] und klicken **[!UICONTROL FTP-Info]** neben der Datenquelle, die Sie erstellt haben.
1. Nachdem Sie sich authentifiziert haben, ziehen Sie die bearbeitete Datei in das authentifizierte FTP-Fenster.
1. Erstellen Sie eine leere Textdatei an einem beliebigen Speicherort außerhalb des FTP-Fensters. Geben Sie denselben Dateinamen wie die Datenquellendatei ein, die Sie auf die FTP-Site hochgeladen haben (mit einer Ausnahme). Anstelle einer `.txt` Dateityp, `.fin` Dateityp. Stellen Sie sicher, dass Ihre Betriebssystemeinstellungen es Ihnen ermöglichen, Dateitypen anzuzeigen und zu ändern.
1. Leer ziehen `.fin` an denselben FTP-Speicherort wie die Datenquellendatei. Das Vorhandensein der `.fin` weist Adobe an, dass die Datenquellendatei vollständig hochgeladen wurde und aufgenommen werden kann.
1. Nach einigen Minuten verschwindet die Datei vom FTP-Speicherort und ist in der Berichterstellung sichtbar.
1. Aktualisieren Sie die Data Sources-Seite und überprüfen Sie, ob die Datei erfolgreich erfasst wurde.
1. Navigieren Sie zu Analysis Workspace und erstellen Sie ein Projekt.
1. Ziehen Sie eVar 1 als Dimension in die Arbeitsfläche und Ereignis 1 als Metrik. Stellen Sie sicher, dass der Datumsbereich von Workspace die Daten enthält, die Sie in der Datenquelle angegeben haben.

   ![Beispielbericht](assets/success-report.png)

## Nächste Schritte

[Dateiformat](file-format.md): Erfahren Sie mehr über die Erstellung einer Datenquellendatei, die auf Ihr Unternehmen zugeschnitten ist.
