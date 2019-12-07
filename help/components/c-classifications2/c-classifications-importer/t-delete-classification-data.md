---
description: In diesen Schritten wird beschrieben, wie Sie Klassifizierungsdaten löschen oder entfernen.
subtopic: Classifications
title: Löschen von Classification-Daten
topic: Admin tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Löschen von Classification-Daten

In einigen Fällen müssen Klassifizierungsdaten nach dem Hochladen entfernt werden. Verwenden Sie entweder `~empty~` oder `~deletekey~`, je nachdem, was Sie entfernen möchten.

## Schritte zum Entfernen von Classification-Daten

Das Entfernen von Classification-Daten umfasst das Hochladen einer Classification-Datei, die die entsprechenden Zellen enthält `~empty~` oder `~deletekey~` in ihnen liegt.

1. Klicken Sie auf **[!UICONTROL Admin]** &gt; **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Browser-Export]**.
1. Wählen Sie die Report Suite und den Datensatz aus, aus denen Classification-Daten entfernt werden sollen.
1. Passen Sie die optionalen Einstellungen zum Filtern der gesuchten Daten an und klicken Sie auf **[!UICONTROL Datei exportieren]**.
1. Nachdem die Datei heruntergeladen wurde, öffnen Sie die Datei und ersetzen Sie alle Classification-Werte durch `~empty~` oder `~deletekey~`.
1. Speichern Sie die Datei als tabulatorgetrennte Textdatei.
1. Klicken Sie auf Datei **[!UICONTROL importieren]** und laden Sie die gespeicherte Classification-Datei erneut in Adobe Analytics hoch.

## Löschen eines einzelnen Classification-Werts

Mehrere Classifications können zur gleichen Variablen gehören. Sie können beispielsweise zwei verschiedene Klassifizierungen von eVar1 haben. Wenn Sie nur einen einzelnen klassifizierten Wert entfernen möchten, ersetzen Sie den Klassifizierungswert durch `~empty~`. Beispiel:

| Bestands-SKU (eVar8) | Lagerbestandsname | Bestandskategorie |
| --- | --- | --- |
| 857467 | V-Nacken-Pullover | Damenbekleidung |
| 948203 | Armband | Schmuck |
| 174391 | Weiße korduroide Hose | `~empty~` |

Die Verwendung `~empty~` unter der Classification der Lagerbestandskategorie behält weiterhin Daten für die Classification der Lagerbestandsnamen bei. Der `~empty~` Wert löscht nur die Classification-Daten für diese Zelle.

## Löschen einer gesamten Classification-Zeile

Verwenden Sie `~deletekey~` in einer beliebigen Spalte, um die gesamte Classification-Zeile zu löschen. Beispiel:

| Bestands-SKU (eVar8) | Lagerbestandsname | Bestandskategorie |
| --- | --- | --- |
| 857467 | V-Nacken-Pullover | Damenbekleidung |
| 948203 | Armband | Schmuck |
| 174391 | Weiße korduroide Hose | `~deletekey~` |

Durch Verwendung `~deletekey~` unter der Classification der Lagerbestandskategorie werden alle Classification-Daten für den Schlüsselwert gelöscht `174391`. Es wird so, als ob die Zeile nie klassifiziert wurde.

## Fallstricke und Tipps

* Bei Verwendung `~deletekey~`benötigen Sie nur eine Zeile in einer Classification-Datei.
* `~empty~` und `~deletekey~` muss *exakt* übereinstimmen. Leerzeichen oder Groß-/Kleinschreibung sind nicht zulässig.
* Werte in der Schlüsselspalte können nicht gelöscht werden. Diese Werte werden direkt in die Variable übergeben und sind dauerhaft.
* Wenn Sie einen Classification-Wert mit Unterklassifizierungen entfernen, werden diese Unterklassifizierungen ebenfalls entfernt. Classifications können nicht ohne Schlüsselwert bestehen, und die übergeordnete Classification ist der Schlüsselwert für eine Unter-Classification.
* Sie können die Unter-Classificationsdaten entfernen, wobei die übergeordnete Classification intakt bleibt.
