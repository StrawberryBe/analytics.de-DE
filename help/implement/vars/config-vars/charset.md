---
title: charSet
description: Die Variable „charSet“ bestimmt, mit welcher Codierung Adobe Ihre Bildanforderung analysiert.
exl-id: 2a2660c6-809d-4b33-a846-01e49dd99c7f
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 90%

---

# charSet

Die Variable „charSet“ wird von Adobe verwendet, um eingehende Daten für die Speicherung und Berichterstellung in UTF-8 zu konvertieren. Die meisten Sites müssen diese Variable nicht festlegen.

Legen Sie diese Variable nur fest, wenn in Berichten unleserliche Werte ([Zeichensalat](https://de.wikipedia.org/wiki/Zeichensalat)) angezeigt werden. Diese Variable kann seitenweise eingestellt werden, wenn Ihre Website auf verschiedenen Seiten unterschiedliche Codierungen verwendet.

## Zeichensatz in Adobe Experience Platform 

Zeichensatz ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfigurierung der Adobe Analytics-Erweiterung.

1. Gehen Sie zu `experience.adobe.com` und melden Sie sich bei entsprechender Aufforderung an.
1. Wählen Sie [!UICONTROL Launch/Data Collection] aus.
1. Klicken Sie auf [!UICONTROL Gehen Sie zu Launch/Data Collection] und wählen Sie [!UICONTROL Tags] aus.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Zeichensatz] angezeigt wird.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Zeichensatz verwenden. Ändern Sie den Wert nicht von `UTF-8`, es sei denn, Sie sehen beschädigte Werte in Berichten.

## s.charSet in AppMeasurement und im benutzerdefinierten Code-Editor in 

Die `charSet`-Variable ist eine Zeichenfolge. Wenn Sie in Adobe Analytics über beschädigte Werte verfügen, setzen Sie diese Variable auf denselben Wert wie das HTML-Tag `<meta charset="">` auf Ihrer Site.

```js
s.charSet = "UTF-8";
```
