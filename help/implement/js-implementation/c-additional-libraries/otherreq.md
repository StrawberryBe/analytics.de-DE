---
description: Bei einer Implementierung von Analytics ohne JavaScript sind noch weitere Anforderungen und Konfigurationsschritte erforderlich.
keywords: Analytics-Implementierung; Groß-/Kleinschreibung beachten; Kodieren von Abfrageparametern; ungültige Zeichen; sichere Bildanforderungen; maximale Variablenlänge; verweist; url; caching; namespace
seo-description: Bei einer Implementierung von Analytics ohne JavaScript sind noch weitere Anforderungen und Konfigurationsschritte erforderlich.
seo-title: Implementierung ohne javascript-Richtlinien
solution: Analytics
title: Implementierung ohne javascript-Richtlinien
topic: Entwickler und Implementierung
uuid: c 672 dd 63-1 c 74-4 f 66-8992-9257 c 5 a 75 e 36
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Implementierung ohne javascript-Richtlinien

Bei einer Implementierung von Analytics ohne JavaScript sind noch weitere Anforderungen und Konfigurationsschritte erforderlich.

Zum besseren Verständnis der Implementierung können Sie sich Codebeispiele ansehen. Die folgenden Informationen beschreiben die zusätzlichen Anforderungen und Konfigurationen:

<!--Meike, I converted this from a table. Table within a table was a mess, and I'm not sure I captured everything. Please check this content against the orginal. -Bob -->

**Groß-/Kleinschreibung**

The parameter names (`pageName`, `purchaseID`, and so forth) are case-sensitive and will not properly record data unless they appear as designated in the table displayed in [Query Parameters](../../../implement/js-implementation/data-collection/query-parameters.md).

**Kodierung von Abfrageparametern**

Die Werte aller Abfragezeichenfolgen-Parameter müssen URL-kodiert werden. URL encoding converts characters that are normally illegal when appearing in a query string, such as a space character, into an encoded character beginning with `%`. For example, a space character is converted into `%20`.

Die JavaScript-Version dieser Funktion heißt „escape“ (bzw. „unescape“ zum Dekodieren). Auch Microsoft IIS Version 5.0 verfügt über Escape- und Unescape-Funktionalität für die Kodierung von Abfragezeichenfolgen. Des Weiteren enthalten auch andere Webserver-Skriptsprachen Kodierung-/Dekodierungs-Hilfsprogramme.

**Maximale Länge von Variablen**

Zu jeder Variablen gibt es eine maximal erlaubte Länge. Nähere Angaben zu den Höchstlängen der einzelnen Variablen finden Sie unter [Analytics-Variablen](../../../implement/js-implementation/c-variables/sc-variables.md). Wenn die maximal zulässige Länge bei einer Variablen überschritten wird, führt dies dazu, dass der Wert abgeschnitten gespeichert und in Analytics nur verkürzt angezeigt wird.

**Ungültige Zeichen**

Unzulässig sind nicht druckfähige Zeichen mit einer ASCII-Nummer kleiner als 128 sowie alle Zeichen oberhalb der 128. Ebenfalls unzulässig sind HTML-Formatierungen („&lt;h1&gt;“) sowie Markenzeichen, eingetragene Markenzeichen und Copyright-Symbole.

**Sicher (&lt; HTTPS: &gt; im Vergleich zu nicht sicher (&lt; http: &gt;) Bildanforderungen**

Bei Seiten, auf die über HTTPS (sichere Verbindung) zugegriffen wird, wird der URL-Teil der Bildanforderungen so geändert, dass eine andere Gruppe von Datenerfassungsservern angesprochen wird.

Die folgenden Informationen zeigen die verschiedenen urls, die für sichere und nicht sichere Bildanforderungen verwendet werden.

* The `*` in the URL above denotes a data-center specific URL that is provided to you by your Adobe Consultant. Da Adobe verschiedene Data Center einsetzt, ist es erforderlich, dass Sie die richtige URL implementieren, die Ihrem Unternehmen zugewiesen wurde. In jedem Code, den Sie von Ihrem Unternehmen aus über die Admin Console herunterladen, ist das richtige Data Center automatisch schon angegeben. An Code, den Sie aus externen Quellen beziehen, müssen Sie möglicherweise noch Korrekturen vornehmen, damit er auf das richtige Data Center verweist.
* Bei Kunden, die mehrere Report Suites verwenden, sollten diese nur im Verzeichnisteil (nicht im Domänenteil) der URL aufgeführt sein:
* The `*` in the URL above denotes a data-center specific URL that is provided to you by your Adobe Consultant. Da Adobe verschiedene Data Center einsetzt, ist es erforderlich, dass Sie die richtige URL implementieren, die Ihrem Unternehmen zugewiesen wurde.

**URL und Verweis-URL**

The URL and Referring URL may be populated from the server in the `g=` and `r=` variables. Use the Request ServerVariables (`HTTP\_REFERRER`) or Request ServerVariables `(URL) (IIS/ASP)`, or the appropriate variable for your server/scripting technology. The referring URL `( r=)` is extremely important for tracking referring URLs, domains, search engines, and search terms.

Wenn pagename nicht verwendet wird, ist es zwingend erforderlich, dass das Feld Aktuelle URL eindeutig ausgefüllt ist. If neither pageName nor Current URL `(g=)` is populated, the record is invalid and is not processed. Damit der Datensatz verarbeitet werden kann, muss mindestens das URL-Feld angegeben sein.

**Auswirkungen von Zwischenspeicherung**

HTML- und andere Webseiten können im Browser oder auf Servern, die sich zwischen dem Besucher und der Website mit den Inhalten befinden, zwischengespeichert werden. Die Zwischenspeicherung verhindert eine genaue Zählung von Seitenansichten und anderen Ereignissen, es sei denn, eine "Cache-Busting" -Technik wird verwendet.

Das standardmäßige JavaScript von Adobe enthält eine dynamische Methode, die Änderungen an den Bildanforderungen vornimmt und so deren Zwischenspeicherung unterbindet. So kann eine exakte Zählung der Seitenansichten sichergestellt werden.

Diese zufallsbasierten Änderungen funktionieren jedoch nicht bei Bildanforderungen, die serverseitig erstellt werden. Erneut geladene Seiten und zwischengespeicherte Seiten (entweder im Cache des Browsers oder auf einem Proxyserver) werden beim Einsatz serverseitiger Bildanforderungen in manchen Fällen nicht mitgezählt.

SSL (`https:`) pages are not, by definition, ever cached so this warning applies only to non-secure (`http:`) pages. Additionally, pages with parameters (`https://www.samplesite.com/page.asp?parameter=1`) or certain file extensions (`.asp`, `.jsp`, etc.) nicht zwischengespeichert.

Das Beispiel unten zeigt eine JavaScript-Minimallösung, bei der im Wesentlichen die serverseitige Bildanforderung zusammengestellt und eine Zufallszahl im Browser angehängt wird. Diese Methode überwindet die Zwischenspeicherung, die sonst auf statischen HTML-Seiten erfolgen würde, die über HTTPS aufgerufen werden: Protokoll.

**nameSpace (Variable)**

Der Abfragezeichenfolgen-Parameter nameSpace ist bei Implementierungen ohne JavaScript erforderlich.

Beispiel: ns=nameSpace

Den nameSpace-Wert für Ihr Unternehmen erhalten Sie von Ihrem Adobe-Berater oder -Kundenbetreuer.
