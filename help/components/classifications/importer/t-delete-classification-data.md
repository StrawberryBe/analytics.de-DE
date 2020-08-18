---
description: In diesen Schritten wird beschrieben, wie Sie Klassifizierungsdaten löschen oder entfernen.
subtopic: Classifications
title: Löschen von Klassifizierungsdaten
topic: Admin tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 100%

---


# Löschen von Klassifizierungsdaten

In einigen Fällen müssen Klassifizierungsdaten nach dem Hochladen entfernt werden. Verwenden Sie entweder `~empty~` oder `~deletekey~`, je nachdem, was Sie entfernen möchten.

## Schritte zum Entfernen von Klassifizierungsdaten

Das Entfernen von Klassifizierungsdaten umfasst das Hochladen einer Klassifizierungsdatei, mit `~empty~` oder `~deletekey~` in den entsprechenden Zellen.

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Browser-Export]**.
1. Wählen Sie die Report Suite und den Datensatz aus, aus denen Classification-Daten entfernt werden sollen.
1. Passen Sie die optionalen Einstellungen zum Filtern der gesuchten Daten an und klicken Sie auf **[!UICONTROL Datei exportieren]**.
1. Nachdem die Datei heruntergeladen wurde, öffnen Sie die Datei und ersetzen Sie alle Klassifizierungswerte durch `~empty~` oder `~deletekey~`.
1. Speichern Sie die Datei als tabulatorgetrennte Textdatei.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und laden Sie die gespeicherte Klassifizierungsdatei erneut in Adobe Analytics hoch.

## Löschen eines einzelnen Klassifizierungswerts

Mehrere Klassifizierungen können zur gleichen Variable gehören. Sie können beispielsweise zwei verschiedene Klassifizierungen von eVar1 haben. Wenn Sie nur einen einzelnen klassifizierten Wert entfernen möchten, ersetzen Sie den Klassifizierungswert durch `~empty~`. Beispiel:

| Inventar-SKU (eVar8) | Inventarname | Inventarkategorie |
| --- | --- | --- |
| 857467 | Pullover mit V-Ausschnitt | Damenbekleidung |
| 948203 | Fußkettchen | Schmuck |
| 174391 | Weiße Kordhose | `~empty~` |

Die Verwendung von `~empty~` unter der Klassifizierung „Inventarkategorie“ behält weiterhin Daten für die Klassifizierung „Inventarname“ bei. Der `~empty~`-Wert löscht nur die Klassifizierungsdaten für diese Zelle.

## Löschen einer gesamten Klassifizierungszeile

Verwenden Sie `~deletekey~` in einer beliebigen Spalte, um die gesamte Klassifizierungszeile zu löschen. Beispiel:

| Inventar-SKU (eVar8) | Inventarname | Inventarkategorie |
| --- | --- | --- |
| 857467 | Pullover mit V-Ausschnitt | Damenbekleidung |
| 948203 | Fußkettchen | Schmuck |
| 174391 | Weiße Kordhose | `~deletekey~` |

Durch Verwendung von `~deletekey~` unter der Klassifizierung „Inventarkategorie“ werden alle Klassifizierungsdaten für den Schlüsselwert `174391` gelöscht. Es wirkt dann so, als ob die Zeile nie klassifiziert wurde.

## Fallstricke und Tipps

* Bei der Verwendung von `~deletekey~` benötigen Sie nur eine Zeile in einer Klassifizierungsdatei.
* `~empty~` und `~deletekey~` müssen *exakt* übereinstimmen. Leerzeichen oder Groß-/Kleinschreibung sind nicht zulässig.
* Werte in der Schlüsselspalte können nicht gelöscht werden. Diese Werte werden direkt in die Variable übergeben und sind dauerhaft.
* Wenn Sie einen Klassifizierungswert entfernen, der Unterklassifizierungen enthält, werden diese ebenfalls entfernt. Classifications können nicht ohne Schlüsselwert bestehen, und die übergeordnete Classification ist der Schlüsselwert für eine Unter-Classification.
* Sie können die Unter-Classificationsdaten entfernen, wobei die übergeordnete Classification intakt bleibt.
