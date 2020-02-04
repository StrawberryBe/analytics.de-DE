---
title: charSet
description: Die Variable "charSet"bestimmt, mit welcher Kodierung Adobe Ihre Bildanforderung analysiert.
translation-type: tm+mt
source-git-commit: f769da139d9890fd736a9b277934b11aa131e166

---


# charSet

Die Variable &quot;charSet&quot;wird von Adobe verwendet, um eingehende Daten für die Speicherung und Berichterstellung in UTF-8 zu konvertieren. Wenn Ihre Site einen anderen charSet als UTF-8 verwendet, ermöglicht diese Variable die korrekte Kodierung Ihrer Daten durch Adobe. Diese Variable kann seitenweise eingestellt werden, wenn Ihre Site auf verschiedenen Seiten unterschiedliche Kodierungen verwendet.

## Zeichensatz beim Start der Adobe Experience Platform

Der Zeichensatz ist ein Feld unter dem Akkordeon &quot; [!UICONTROL Allgemein] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Allgemein] &quot;, mit dem das Feld &quot; [!UICONTROL Zeichensatz] &quot;angezeigt wird.

Sie können entweder einen voreingestellten Zeichensatz oder einen benutzerdefinierten Zeichensatz verwenden. Dieser Wert sollte mit der Zeichenkodierung auf Ihrer Site übereinstimmen. Die meisten Sites verwenden `UTF-8`.

## s.charSet in AppMeasurement und benutzerdefinierten Codeeditor starten

Die `charSet` Variable ist eine Zeichenfolge. Legen Sie diese Variable auf denselben Wert wie das `<meta charset="">` HTML-Tag auf Ihrer Site fest.

```js
s.charSet = "UTF-8";
```
