---
title: Implementieren mit fest programmierten Bildanforderungen
description: Adobe Analytics mithilfe eines HTML-Bild-Tags (einer fest programmierten Bildanforderung) implementieren
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Implementieren mit fest programmierten Bildanforderungen

AppMeasurement-Bibliotheken, die von Adobe bereitgestellt werden, kompilieren Variablen auf der Seite und senden sie dann als Bildanforderung an Adobe. Sie können AppMeasurement-Bibliotheken ganz umgehen und eine Bildanforderung manuell an Adobe senden. Für diese Methode müssen Sie die Bildanforderung und die Abfragezeichenfolge manuell formulieren.

Diese Implementierungsmethode kann auf jeder Plattform verwendet werden, auf der Bilder aus externen Quellen angezeigt werden. JavaScript ist nicht erforderlich.

>[!NOTE] Während fest programmierte Bildanforderungen einfach einzurichten sind, sind sie bei größeren Projekten schwer zu debuggen, zu warten und zu skalieren. Stellen Sie sicher, dass fest programmierte Bildanforderungen die beste Option für Sie sind, bevor Sie fortfahren.

## Bildanforderungssyntax

Im Folgenden finden Sie ein Beispiel für eine fest programmierte Bildanforderung mit HTML:

```html
<img src="https://example.sc.omtrdc.net/b/ss/examplersid/1?AQB=1&g=http%3A%2F%2Fexample.com&pageName=Example%20hardcoded%20hit&v1=Example%20value&AQE=1"/>
```

* `https://` bezeichnet das Protokoll. Stimmen Sie das in der Bildanforderung verwendete Protokoll mit dem Protokoll ab, das der Rest Ihrer Website verwendet.
* `example.sc.omtrdc.net` ist der in der `trackingServer`-Variablen enthaltene Wert.
* `/b/ss/` ist in allen Bildanforderungen enthalten. Dabei handelt es sich um einen Teil der Dateistruktur für Bilder, die auf Adobe-Datenerfassungs-Servern gespeichert werden.
* `examplersid` ist die Report Suite-ID, an die Sie Daten senden möchten.
* `/1/` ist die Trefferquelle. Siehe `hit_source` unter [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) im Exportbenutzerhandbuch. Steuert die Reihenfolge, in der Cookies und andere Methoden Besucher identifizieren.
* Alles nach dem Trennzeichen der Abfragezeichenfolge (`?`) sind Daten, die Sie in Berichte aufnehmen möchten. Eine vollständige Liste der Parameter, die Sie in eine Bildanforderung einbeziehen können, finden Sie unter [Datenerfassungs-Abfrageparameter](../validate/query-parameters.md).

## Häufig gestellte Fragen

Erfahren Sie mehr über häufig gestellte Fragen bei der Verwendung von fest programmierten Bildanforderungen.

**Wird bei Abfragezeichenfolgenparametern zwischen Groß- und Kleinschreibung unterschieden?**

Ja. Stellen Sie sicher, dass die Abfragezeichenfolgenparameter exakt übereinstimmen, andernfalls werden sie nicht aufgezeichnet. Beispiel: `pagename` ist kein gültiger Abfragezeichenfolgenparameter, während `pageName` einer ist.

**Darf die Abfragezeichenfolge Leerzeichen enthalten?**

Die Werte aller Abfragezeichenfolgenparameter sind URL-codiert. Bei der URL-Codierung werden Zeichen, die in URLs normalerweise unzulässig sind, in zulässige Zeichen umgewandelt. So wird zum Beispiel ein Leerzeichen in `%20` umgewandelt. Achten Sie darauf, dass alle Zeichen, die nicht alphanumerisch sind, URL-codiert sind. Adobe URL-decodiert Werte automatisch, wenn die Bildanforderungen die Datenerfassungs-Server erreichen.

Weitere Informationen über die Funktionsweise der URL-Codierung finden Sie unter der [HTML-URL-Kodierungsreferenz](https://www.w3schools.com/tags/ref_urlencode.asp) auf W3Schools.

**Wie viele Zeichen darf ein einzelner Wert maximal enthalten?**

Jede Variable hat eine andere maximale Länge. Die meisten Traffic-Variablen enthalten bis zu 100 Byte, während die meisten Konversionsvariablen bis zu 255 Byte enthalten. Wenn eine Bildanforderung die Datenerfassungs-Server erreicht, schneidet Adobe diese Werte automatisch auf ihre maximale Länge ab.
