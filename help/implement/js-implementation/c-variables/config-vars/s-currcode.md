---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.currencyCode

Die Variable bestimmt die Konversionsrate, die auf den Umsatz angewendet werden soll.

Alle Geldbeträge werden in einer Währung Ihrer Wahl gespeichert. Wenn dies die gleiche Währung ist, wie in *`currencyCode`*, or *`currencyCode`* is empty, no conversion is applied.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | cc | Konversion &gt; Einkäufe &gt; Umsatz Alle Konversionsberichte, die Umsätze oder Geldbeträge anzeigen | „USD“ |

Wenn Besucher auf Ihrer Website Einkäufe in verschiedenen Währungen tätigen können, sollten Sie mithilfe der Variablen *`currencyCode`* sicherstellen, dass Umsätze in der entsprechenden Währung gespeichert werden. For example, if the base currency for your report suite is USD, and you sell an item for 40 Euros, you should populate the *`currencyCode`* with "EUR" on the HTML page. Nach Eingang der Daten bei der Datenerfassung werden diese 40 Euro dann unter Verwendung des aktuellen Konversionskurses in USD umgerechnet.

Wenn Sie Verkäufe in mehreren Währungen tätigen, empfiehlt es sich, die Variable *`currencyCode`* auf der HTML-Seite anstatt in der JavaScript-Datei aufzufüllen. Wenn Sie anstelle der von Adobe verwendeten Konversionsraten Ihre eigenen Konversionsraten verwenden möchten, stellen Sie die *`currencyCode`* auf die Basiswährung Ihrer Report Suite ein. Dann rechnen Sie alle Umsätze um, bevor diese nach [!DNL Analytics] gesendet werden.

Wechselkurskonversionen werden sowohl bei Umsatz- als auch bei Währungs-Ereignissen vorgenommen. Das sind Ereignisse, mit denen Werte zu Umsätzen summiert werden, wie Steuern und Versandkosten. Die Umsatz- und Währungs-Ereignisse werden in den Produktzeichenfolgen angegeben. Weitere Informationen zu Produkten finden Sie unter [events](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-events.html).

## Syntax und mögliche Werte

```js
s.currencyCode="currency_code"
```

## Beispiele

```js
s.currencyCode="GBP"
```

```js
s.currencyCode="EUR"
```

## Konfigurationseinstellungen

Adobe [!DNL Customer Care] kann die für Ihre Report Suite standardmäßig eingestellte Währung ändern. Wenn die Basiswährung für eine Report Suite geändert wird, werden die im System vorhandenen Umsätze nicht umgerechnet. Alle neuen Umsatzwerte werden entsprechend umgerechnet.

## Probleme, Fragen und Tipps

* Wenn in Berichten unerwartet größere Umsätze auftauchen, müssen Sie überprüfen, ob die Variable *`currencyCode`* und die Basiswährung der Report Suite korrekt festgelegt sind.
* The *`currencyCode`* variable is not persistent, meaning that the variable must be passed in the same image request as any revenue or other currency-related metrics.
* Währungs-Ereignisse dürfen nicht für Zwecke eingesetzt werden, bei denen es nicht um Währungen geht. Wenn Sie beliebige oder dynamische Werte zählen möchten, die keine Währungen sind, verwenden Sie den Ereignistyp [!UICONTROL numeric].
* Wenn die Variable *`currencyCode`* leer ist, wird keine Konversion vorgenommen.

Weitere Informationen finden Sie unter [Währungscodes](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/currency.html).
