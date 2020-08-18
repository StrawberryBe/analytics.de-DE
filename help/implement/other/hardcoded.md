---
title: Implementieren mit fest programmierten Bildanforderungen
description: Adobe Analytics mithilfe eines HTML-Bild-Tags (einer fest programmierten Bildanforderung) implementieren
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 66%

---


# Implementieren mit fest programmierten Bildanforderungen

AppMeasurement-Bibliotheken, die von Adobe bereitgestellt werden, kompilieren Variablen auf der Seite und senden sie dann als Bildanforderung an Adobe. Sie können AppMeasurement-Bibliotheken ganz umgehen und eine Bildanforderung manuell an Adobe senden. Für diese Methode müssen Sie die Bildanforderung und die Abfragezeichenfolge manuell formulieren.

Diese Implementierungsmethode kann auf jeder Plattform verwendet werden, auf der Bilder aus externen Quellen angezeigt werden. JavaScript ist nicht erforderlich.

>[!NOTE]
>
>Während fest programmierte Bildanforderungen einfach einzurichten sind, sind sie bei größeren Projekten schwer zu debuggen, zu warten und zu skalieren. Stellen Sie sicher, dass fest programmierte Bildanforderungen die beste Option für Sie sind, bevor Sie fortfahren.

## Bildanforderungssyntax

Im Folgenden finden Sie ein Beispiel für eine fest programmierte Bildanforderung mit HTML:

```html
<img src="https://example.sc.omtrdc.net/b/ss/examplersid/1?AQB=1&g=http%3A%2F%2Fexample.com&pageName=Example%20hardcoded%20hit&v1=Example%20value&AQE=1"/>
```

* `https://` bezeichnet das Protokoll. Stimmen Sie das in der Bildanforderung verwendete Protokoll mit dem Protokoll ab, das der Rest Ihrer Website verwendet.
* `example.sc.omtrdc.net` ist der in der [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md)-Variablen enthaltene Wert.
* `/b/ss/` ist in allen Bildanforderungen enthalten. Dabei handelt es sich um einen Teil der Dateistruktur für Bilder, die auf Adobe-Datenerfassungs-Servern gespeichert werden.
* `examplersid` ist die Report Suite-ID, an die Sie Daten senden möchten.
* `/1/` ist die Trefferquelle. Siehe `hit_source` unter [Datenspaltenreferenz](../../export/analytics-data-feed/c-df-contents/datafeeds-reference.md) im Exportbenutzerhandbuch. Steuert die Reihenfolge, in der Cookies und andere Methoden Besucher identifizieren.
* Alles nach dem Trennzeichen der Abfragezeichenfolge (`?`) sind Daten, die Sie in Berichte aufnehmen möchten. Eine vollständige Liste der Parameter, die Sie in eine Bildanforderung einbeziehen können, finden Sie unter [Datenerfassungs-Abfrageparameter](../validate/query-parameters.md).

## Hartkodierte Bildanforderungen in Microsoft Outlook

Da die meisten E-Mails auf HTML basieren, ist es möglich, geöffnete E-Mails zu verfolgen und diese Daten an Adobe Analytics zu senden. Wenn sich Ihr Unternehmen für die Verwendung dieser Methode entscheidet, beachten Sie Folgendes:

* Jeder E-Mail-Rendering kann einen abrechnungsfähigen Server-Aufruf erhöhen.
* Es werden nur E-Mail-Clients verfolgt, die HTML unterstützen und Bilder zulassen. Einige E-Mail-Clients wie Microsoft Outlook blockieren standardmäßig externe Bilder. Diese E-Mails werden erst verfolgt, wenn der Empfänger sich dafür entscheidet, externe Bilder herunterzuladen.

So erstellen Sie eine Outlook-E-Mail mit einer Bildanforderung:

1. Öffnen Sie einen HTML-Editor. Wenn kein HTML-Editor verfügbar ist, funktioniert auch ein Texteditor.
2. Fügen Sie in eine neue HTML-Datei ein fest programmiertes Image Request- `<img>` Tag ein, das in ein `<body>` Tag eingeschlossen ist.
3. Speichern Sie die HTML-Datei.
4. Öffnen Sie Microsoft Outlook und erstellen Sie eine E-Mail.
5. Wechseln Sie zur Registerkarte &quot;Einfügen&quot;und klicken Sie auf &quot;Datei **anhängen&quot;**. Wählen Sie die HTML-Datei für die Bildanforderung aus.
6. Klicken Sie auf das Popupmenü neben &quot;Einfügen&quot;und wählen Sie &quot;Als Text **einfügen&quot;**. Wenn Sie ohne Popupmenü auf die Schaltfläche &quot;Einfügen&quot;klicken, wird die HTML-Datei zu einer Anlage, die nicht funktioniert.

Ihre E-Mail scheint sich nicht zu ändern, da die Bildanforderung ein transparentes 1x1-Pixel ist. Wenn Sie die Bildanforderung zu Testzwecken anzeigen möchten, ändern Sie die HTML-Datei, um einen Rand, zusätzlichen Text oder anderen Inhalt einzuschließen.

## Häufig gestellte Fragen

Erfahren Sie mehr über häufig gestellte Fragen bei der Verwendung von fest programmierten Bildanforderungen.

### Wird bei Abfragezeichenfolgenparametern zwischen Groß- und Kleinschreibung unterschieden?

Ja. Stellen Sie sicher, dass die Abfragezeichenfolgenparameter exakt übereinstimmen, andernfalls werden sie nicht aufgezeichnet. Beispiel: `pagename` ist kein gültiger Abfragezeichenfolgenparameter, während `pageName` einer ist.

### Darf die Abfragezeichenfolge Leerzeichen enthalten?

Die Werte aller Abfragezeichenfolgenparameter sind URL-codiert. Bei der URL-Codierung werden Zeichen, die in URLs normalerweise unzulässig sind, in zulässige Zeichen umgewandelt. So wird zum Beispiel ein Leerzeichen in `%20` umgewandelt. Achten Sie darauf, dass alle Zeichen, die nicht alphanumerisch sind, URL-codiert sind. Adobe URL-decodiert Werte automatisch, wenn die Bildanforderungen die Datenerfassungs-Server erreichen.

Weitere Informationen über die Funktionsweise der URL-Codierung finden Sie unter der [HTML-URL-Kodierungsreferenz](https://www.w3schools.com/tags/ref_urlencode.asp) auf W3Schools.

### Wie viele Zeichen darf ein einzelner Wert maximal enthalten?

Jede Variable hat eine andere maximale Länge. Die meisten Traffic-Variablen enthalten bis zu 100 Byte, während die meisten Konversionsvariablen bis zu 255 Byte enthalten. Wenn eine Bildanforderung die Datenerfassungs-Server erreicht, schneidet Adobe diese Werte automatisch auf ihre maximale Länge ab.
