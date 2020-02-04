---
title: Implementierung mit fest programmierten Bildanforderungen
description: Adobe Analytics mithilfe eines HTML-Image-Tags implementieren (fest codierte Bildanforderung)
translation-type: tm+mt
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651

---


# Implementierung mit fest programmierten Bildanforderungen

AppMeasurement-Bibliotheken, die von Adobe bereitgestellt werden, kompilieren Variablen auf der Seite und senden sie dann als Bildanforderung an Adobe. Sie können AppMeasurement-Bibliotheken ganz umgehen und eine Bildanforderung manuell an Adobe senden. Für diese Methode müssen Sie die Bildanforderung und die Abfragezeichenfolge manuell formulieren.

Diese Implementierungsmethode kann auf jeder Plattform verwendet werden, auf der Bilder aus externen Quellen angezeigt werden. JavaScript ist nicht erforderlich.

> [!NOTE] Hartkodierte Bildanforderungen lassen sich zwar leicht einrichten, sind aber beim Debuggen, Verwalten und Skalieren in größeren Projekten schwierig. Stellen Sie sicher, dass fest programmierte Bildanforderungen die beste Option für Sie sind, bevor Sie fortfahren.

## Bildanforderungssyntax

Im Folgenden finden Sie eine komprimierte Bildanforderung mit HTML:

```html
<img src="https://example.sc.omtrdc.net/b/ss/examplersid/1?AQB=1&g=http%3A%2F%2Fexample.com&pageName=Example%20hardcoded%20hit&v1=Example%20value&AQE=1"/>
```

* `https://` bezeichnet das Protokoll. Entspricht dem Protokoll, das in der Bildanforderung verwendet wird, dem Protokoll, das der Rest Ihrer Site verwendet.
* `example.sc.omtrdc.net` ist der in der `trackingServer` Variablen enthaltene Wert.
* `/b/ss/` ist in allen Bildanforderungen enthalten. Es ist Teil der Dateistruktur für Bilder, die auf Adobe-Datenerfassungsservern gespeichert werden.
* `examplersid` ist die Report Suite-ID, an die Sie Daten senden möchten.
* `/1/` ist die Trefferquelle. Siehe auch `hit_source` unter [Datenspaltenverweis](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) im Handbuch Exportieren. Steuert die Reihenfolge, in der Cookies und andere Methoden Besucher identifizieren.
* Alles nach dem Trennzeichen der Abfragezeichenfolge (`?`) sind Daten, die Sie in Berichte aufnehmen möchten. Eine vollständige Liste der Parameter, die Sie in eine Bildanforderung einbeziehen können, finden Sie unter Abfrageparameter[ für die ](../validate/query-parameters.md)Datenerfassung.

## FAQs

Erfahren Sie mehr über häufig gestellte Fragen mit fest programmierten Bildanforderungen.

**Achten Abfragezeichenfolgenparameter auf die Groß-/Kleinschreibung?**

Ja. Stellen Sie sicher, dass die Abfragezeichenfolgenparameter exakt übereinstimmen, andernfalls werden sie nicht aufgezeichnet. Beispiel: `pagename` ist kein gültiger Abfragezeichenfolgenparameter, solange `pageName` dies der Fall ist.

**Kann ich Leerzeichen in die Abfragezeichenfolge aufnehmen?**

Die Werte für die einzelnen Abfragezeichenfolgenparameter werden URL-kodiert. Bei der URL-Kodierung werden Zeichen, die in URLs normalerweise unzulässig sind, in zulässige Zeichen umgewandelt. So wird zum Beispiel ein Leerzeichen in `%20` umgewandelt. Achten Sie darauf, dass alle Zeichen, die nicht alphanumerisch sind, URL-kodiert sind. Adobe-URL dekodiert Werte automatisch, wenn Bildanforderungen Datenerfassungsserver erreichen.

Weitere Informationen zur Funktionsweise der URL-Kodierung finden Sie in der [HTML-URL-Kodierung](https://www.w3schools.com/tags/ref_urlencode.asp) auf W3Schools.

**Wie viele Zeichen darf ein einzelner Wert maximal enthalten?**

Jede Variable hat eine andere Maximallänge. Die meisten Traffic-Variablen halten bis zu 100 Byte, während die meisten Konversionsvariablen bis zu 255 Byte lang sind. Wenn eine Bildanforderung die Datenerfassungsserver erreicht, schneidet Adobe diese Werte automatisch auf ihre maximale Länge ab.
