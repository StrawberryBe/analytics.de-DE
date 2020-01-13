---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.currencyCode

Die Variable bestimmt, welche Konversionsrate auf den Umsatz angewendet werden soll.

Alle Geldbeträge werden in einer Währung Ihrer Wahl gespeichert. Wenn dies die gleiche Währung ist, wie in Wenn *`currencyCode`* oder *`currencyCode`* leer ist, wird keine Konversion vorgenommen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| nicht angegeben | cc | Konversion &gt; Einkäufe &gt; Umsatz Alle Konversionsberichte, die Umsätze oder Geldbeträge anzeigen | „USD“ |

Wenn Besucher auf Ihrer Website Einkäufe in verschiedenen Währungen tätigen können, müssen Sie mithilfe der Variable *`currencyCode`* sicherstellen, dass Umsätze in der entsprechenden Währung gespeichert werden. Wenn die Basiswährung für Ihre Report Suite beispielsweise USD ist und Sie einen Artikel für 40 Euro verkaufen, müssen Sie die *`currencyCode`* mit „EUR“ auf der HTML-Seite ausfüllen. Nach Eingang der Daten bei der Datenerfassung werden diese 40 Euro dann unter Verwendung des aktuellen Konversionskurses in USD umgerechnet.

Wenn Sie Verkäufe in mehreren Währungen tätigen, empfiehlt es sich, die Variable *`currencyCode`* auf der HTML-Seite anstatt in der JavaScript-Datei aufzufüllen. Wenn Sie anstelle der von Adobe verwendeten Konversionsraten Ihre eigenen Konversionsraten verwenden möchten, stellen Sie *`currencyCode`* auf die Basiswährung Ihrer Report Suite ein. Dann rechnen Sie alle Umsätze um, bevor diese nach [!DNL Analytics] gesendet werden.

Wechselkurskonversionen werden sowohl bei Umsatz- als auch bei Währungs-Ereignissen vorgenommen. Das sind Ereignisse, mit denen Werte zu Umsätzen summiert werden, wie Steuern und Versandkosten. Die Umsatz- und Währungs-Ereignisse werden in den Produktzeichenfolgen angegeben. Weitere Informationen zu Produkten finden Sie unter [events](https://docs.adobe.com/content/help/de-DE/analytics/implementation/analytics-basics/ref-events.html).

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

* Wenn Sie überraschend hohe Umsätze in Berichten feststellen, stellen Sie sicher, dass die Variable *`currencyCode`* und die Basiswährung der Report Suite korrekt eingestellt sind.
* Die Variable *`currencyCode`* ist nicht persistent, d. h., die Variable muss in derselben Bildanforderung wie andere Umsatz- oder sonstige Metriken, die mit Währungen in Verbindung stehen, übergeben werden.
* Währungs-Ereignisse dürfen nicht für Zwecke eingesetzt werden, bei denen es nicht um Währungen geht. Wenn Sie beliebige oder dynamische Werte zählen möchten, die keine Währungen sind, verwenden Sie den Ereignistyp [!UICONTROL numeric].
* Wenn die Variable *`currencyCode`* leer ist, wird keine Konversion vorgenommen.

Weitere Informationen finden Sie unter [Währungscodes](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/currency.html).
