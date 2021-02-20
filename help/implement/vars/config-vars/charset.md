---
title: charSet
description: Die Variable „charSet“ bestimmt, mit welcher Codierung Adobe Ihre Bildanforderung analysiert.
translation-type: tm+mt
source-git-commit: 70410af433f540764b71bd29a81ff9d8210cb95c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 60%

---


# charSet

Die Variable „charSet“ wird von Adobe verwendet, um eingehende Daten für die Speicherung und Berichterstellung in UTF-8 zu konvertieren. Die meisten Sites müssen diese Variable nicht festlegen.

Legen Sie diese Variable nur fest, wenn in Berichten unleserliche Werte ([mojibake](https://en.wikipedia.org/wiki/Mojibake)) angezeigt werden. Sie können diese Variable seitenweise einstellen, wenn Ihre Site auf verschiedenen Seiten unterschiedliche Kodierungen verwendet.

## Zeichensatz in Adobe Experience Platform Launch

Zeichensatz ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfigurierung der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Zeichensatz] angezeigt wird.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Zeichensatz verwenden. Ändern Sie den Wert nicht von `UTF-8`, es sei denn, Sie sehen beschädigte Werte in Berichten.

## s.charSet in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `charSet`-Variable ist eine Zeichenfolge. Wenn Sie in Adobe Analytics über beschädigte Werte verfügen, setzen Sie diese Variable auf denselben Wert wie das HTML-Tag `<meta charset="">` auf Ihrer Site.

```js
s.charSet = "UTF-8";
```
