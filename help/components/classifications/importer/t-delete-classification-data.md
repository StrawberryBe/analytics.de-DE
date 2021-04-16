---
description: In diesen Schritten wird beschrieben, wie Sie Classification-Daten löschen oder entfernen.
subtopic: Classifications
title: Löschen von Classification-Daten
feature: Admin Tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
exl-id: 2b156e66-3090-4048-8192-a412320e3be3
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 100%

---

# Löschen von Classification-Daten

In einigen Fällen müssen Classification-Daten nach dem Hochladen entfernt werden. Verwenden Sie entweder `~empty~` oder `~deletekey~`, je nachdem, was Sie entfernen möchten.

## Schritte zum Entfernen von Classification-Daten

Das Entfernen von Classification-Daten umfasst das Hochladen einer Classification-Datei, mit `~empty~` oder `~deletekey~` in den entsprechenden Zellen.

1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klicken Sie auf **[!UICONTROL Browser-Export]**.
1. Wählen Sie die Report Suite und den Datensatz aus, aus denen Classification-Daten entfernt werden sollen.
1. Passen Sie die optionalen Einstellungen zum Filtern der gesuchten Daten an und klicken Sie auf **[!UICONTROL Datei exportieren]**.
1. Nachdem die Datei heruntergeladen wurde, öffnen Sie die Datei und ersetzen Sie alle Classification-Werte durch `~empty~` oder `~deletekey~`.
1. Speichern Sie die Datei als tabulatorgetrennte Textdatei.
1. Klicken Sie auf **[!UICONTROL Datei importieren]** und laden Sie die gespeicherte Classification-Datei erneut in Adobe Analytics hoch.

## Löschen eines einzelnen Classification-Werts

Mehrere Klassifizierungen können zur gleichen Variable gehören. Sie können beispielsweise zwei verschiedene Klassifizierungen von eVar1 haben. Wenn Sie nur einen einzelnen klassifizierten Wert entfernen möchten, ersetzen Sie den Classification-Wert durch `~empty~`. Beispiel:

| Inventar-SKU (eVar8) | Inventarname | Inventarkategorie |
| --- | --- | --- |
| 857467 | Pullover mit V-Ausschnitt | Damenbekleidung |
| 948203 | Fußkettchen | Schmuck |
| 174391 | Weiße Kordhose | `~empty~` |

Die Verwendung von `~empty~` unter der Classification „Inventarkategorie“ behält weiterhin Daten für die Classification „Inventarname“ bei. Der `~empty~`-Wert löscht nur die Classification-Daten für diese Zelle.

## Löschen einer gesamten Classification-Zeile

Verwenden Sie `~deletekey~` in einer beliebigen Spalte, um die gesamte Classification-Zeile zu löschen. Beispiel:

| Inventar-SKU (eVar8) | Inventarname | Inventarkategorie |
| --- | --- | --- |
| 857467 | Pullover mit V-Ausschnitt | Damenbekleidung |
| 948203 | Fußkettchen | Schmuck |
| 174391 | Weiße Kordhose | `~deletekey~` |

Durch Verwendung von `~deletekey~` unter der Classification „Inventarkategorie“ werden alle Classification-Daten für den Schlüsselwert `174391` gelöscht. Es wirkt dann so, als ob die Zeile nie klassifiziert wurde.

## Fallstricke und Tipps

* Bei der Verwendung von `~deletekey~` benötigen Sie nur eine Zeile in einer Classification-Datei.
* `~empty~` und `~deletekey~` müssen *exakt* übereinstimmen. Leerzeichen oder Groß-/Kleinschreibung sind nicht zulässig.
* Werte in der Schlüsselspalte können nicht gelöscht werden. Diese Werte werden direkt in die Variable übergeben und sind dauerhaft.
* Wenn Sie einen Classification-Wert entfernen, der Unter-Classifications enthält, werden diese ebenfalls entfernt. Classifications können nicht ohne Schlüsselwert bestehen, und die übergeordnete Classification ist der Schlüsselwert für eine Unter-Classification.
* Sie können die Unter-Classificationsdaten entfernen, wobei die übergeordnete Classification intakt bleibt.
