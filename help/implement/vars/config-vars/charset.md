---
title: charSet
description: Die Variable „charSet“ bestimmt, mit welcher Codierung Adobe Ihre Bildanforderung analysiert.
translation-type: ht
source-git-commit: f769da139d9890fd736a9b277934b11aa131e166

---


# charSet

Die Variable „charSet“ wird von Adobe verwendet, um eingehende Daten für die Speicherung und Berichterstellung in UTF-8 zu konvertieren. Wenn Ihre Website einen anderen charSet als UTF-8 verwendet, ermöglicht diese Variable die korrekte Codierung Ihrer Daten durch Adobe. Diese Variable kann seitenweise eingestellt werden, wenn Ihre Website auf verschiedenen Seiten unterschiedliche Codierungen verwendet.

## Zeichensatz in Adobe Experience Platform Launch

Zeichensatz ist ein Feld unter dem Akkordeon [!UICONTROL Allgemein] bei der Konfigurierung der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Allgemein], wodurch das Feld [!UICONTROL Zeichensatz] angezeigt wird.

Sie können entweder einen vorab festgelegten oder einen benutzerdefinierten Zeichensatz verwenden. Dieser Wert sollte mit der Zeichencodierung auf Ihrer Website übereinstimmen. Die meisten Websites verwenden `UTF-8`.

## s.charSet in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `charSet`-Variable ist eine Zeichenfolge. Legen Sie diese Variable auf denselben Wert wie das HTML-Tag `<meta charset="">` auf Ihrer Website fest.

```js
s.charSet = "UTF-8";
```
