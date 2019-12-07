---
description: Bei einer Implementierung von Analytics ohne JavaScript sind noch weitere Anforderungen und Konfigurationsschritte erforderlich.
keywords: Analytics Implementation;case sensitive;encode query parameters;invalid characters;secure image requests;maximum variable length;referring;url;caching;namespace
title: Ohne JavaScript-Richtlinien implementieren
topic: Developer and implementation
uuid: c672dd63-1c74-4f66-8992-9257c5a75e36
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Ohne JavaScript-Richtlinien implementieren

Bei einer Implementierung von Analytics ohne JavaScript sind noch weitere Anforderungen und Konfigurationsschritte erforderlich.

Zum besseren Verständnis der Implementierung können Sie sich Codebeispiele ansehen. In den folgenden Informationen sind die zusätzlichen Anforderungen und Konfigurationsschritte aufgeführt:

<!--Meike, I converted this from a table. Table within a table was a mess, and I'm not sure I captured everything. Please check this content against the orginal. -Bob -->

**Groß-/Kleinschreibung**

Bei den Parameternamen (`pageName`, `purchaseID` usw.) muss auf die richtige Groß-/Kleinschreibung geachtet werden. Andernfalls werden Daten nur dann korrekt erfasst, wenn der Parameter in der Tabelle im Abschnitt [Abfrageparameter](/help/implement/js-implementation/data-collection/query-parameters.md) zugewiesen ist.

**Kodierung von Abfrageparametern**

Die Werte aller Abfragezeichenfolgen-Parameter müssen URL-kodiert werden. Bei der URL-Codierung werden Zeichen, die in einer Abfragezeichenfolge normalerweise unzulässig sind (wie z. B. Leerzeichen) in codierte Zeichen umgewandelt, die mit `%` beginnen. So wird zum Beispiel ein Leerzeichen in `%20` umgewandelt.

Die JavaScript-Version dieser Funktion heißt „escape“ (bzw. „unescape“ zum Dekodieren). Auch Microsoft IIS Version 5.0 verfügt über Escape- und Unescape-Funktionalität für die Kodierung von Abfragezeichenfolgen. Des Weiteren enthalten auch andere Webserver-Skriptsprachen Kodierung-/Dekodierungs-Hilfsprogramme.

**Maximale Länge von Variablen**

Zu jeder Variablen gibt es eine maximal erlaubte Länge. Nähere Angaben zu den Höchstlängen der einzelnen Variablen finden Sie unter [Analytics-Variablen](/help/implement/js-implementation/c-variables/sc-variables.md). Wenn die maximal zulässige Länge bei einer Variablen überschritten wird, führt dies dazu, dass der Wert abgeschnitten gespeichert und in Analytics nur verkürzt angezeigt wird.

**Ungültige Zeichen**

Unzulässig sind nicht druckfähige Zeichen mit einer ASCII-Nummer kleiner als 128 sowie alle Zeichen oberhalb der 128. Ebenfalls unzulässig sind HTML-Formatierungen („&lt;h1&gt;“) sowie Markenzeichen, eingetragene Markenzeichen und Copyright-Symbole.

**Bildanforderungen über sichere (&lt;https:&gt;) oder nicht sichere (&lt;http:&gt;) Verbindungen**

Bei Seiten, auf die über HTTPS (sichere Verbindung) zugegriffen wird, wird der URL-Teil der Bildanforderungen so geändert, dass eine andere Gruppe von Datenerfassungsservern angesprochen wird.

Welche Unterschiede es bei URLs für sichere und nicht sichere Bildanforderungen gibt, sehen Sie in den folgenden Informationen.

* Das `*` in der oben aufgeführten URL bedeutet, dass dies eine Data-Center-spezifische URL ist, die Sie von Ihrem Adobe-Berater erhalten. Da Adobe verschiedene Data Center einsetzt, ist es erforderlich, dass Sie die richtige URL implementieren, die Ihrem Unternehmen zugewiesen wurde. In jedem Code, den Sie von Ihrem Unternehmen aus über die Admin Console herunterladen, ist das richtige Data Center automatisch schon angegeben. An Code, den Sie aus externen Quellen beziehen, müssen Sie möglicherweise noch Korrekturen vornehmen, damit er auf das richtige Data Center verweist.
* Bei Kunden, die mehrere Report Suites verwenden, sollten diese nur im Verzeichnisteil (nicht im Domänenteil) der URL aufgeführt sein:
* Das `*` in der oben aufgeführten URL bedeutet, dass dies eine Data-Center-spezifische URL ist, die Sie von Ihrem Adobe-Berater erhalten. Da Adobe verschiedene Data Center einsetzt, ist es erforderlich, dass Sie die richtige URL implementieren, die Ihrem Unternehmen zugewiesen wurde.

**URL und Verweis-URL**

Die URL und die Verweis-URL können vom Server aus in den Variablen `g=` und `r=` angegeben werden. Verwenden Sie die Request ServerVariables (`HTTP\_REFERRER`) oder Request ServerVariables `(URL) (IIS/ASP)` oder die entsprechende Variable Ihrer Server/Skripttechnologie. Die Verweis-URL `( r=)` ist äußerst wichtig, um Verweis-URLs, Domänen, Suchmaschinen und Suchbegriffe verfolgen zu können.

Wenn pageName nicht verwendet wird, ist es wichtig, dass das Feld „Aktuelle URL“ eindeutig ausgefüllt ist. Wenn weder pageName noch „Aktuelle URL“ `(g=)` Werte enthalten, ist der Datensatz ungültig und wird nicht verarbeitet. Damit der Datensatz verarbeitet werden kann, muss mindestens das URL-Feld angegeben sein.

**Auswirkungen von Zwischenspeicherung**

HTML- und andere Webseiten können im Browser oder auf Servern, die sich zwischen dem Besucher und der Website mit den Inhalten befinden, zwischengespeichert werden. Wenn keine Technik eingesetzt wird, die diese Zwischenspeicherung unterdrückt, kann dadurch eine exakte Zählung von Seitenansichten und anderer Ereignisse verhindert werden.

Das standardmäßige JavaScript von Adobe enthält eine dynamische Methode, die Änderungen an den Bildanforderungen vornimmt und so deren Zwischenspeicherung unterbindet. So kann eine exakte Zählung der Seitenansichten sichergestellt werden.

Diese zufallsbasierten Änderungen funktionieren jedoch nicht bei Bildanforderungen, die serverseitig erstellt werden. Erneut geladene Seiten und zwischengespeicherte Seiten (entweder im Cache des Browsers oder auf einem Proxyserver) werden beim Einsatz serverseitiger Bildanforderungen in manchen Fällen nicht mitgezählt.

SSL-Seiten (`https:`) werden definitionsgemäß nie zwischengespeichert und diese Warnung gilt nur für nicht sichere Seiten (`http:`). Des Weiteren werden auch Seiten mit Parametern (`https://www.samplesite.com/page.asp?parameter=1`) oder bestimmten Dateierweiterungen (`.jsp`, `.asp`, usw.) nicht zwischengespeichert.

Das Beispiel unten zeigt eine JavaScript-Minimallösung, bei der im Wesentlichen die serverseitige Bildanforderung zusammengestellt und eine Zufallszahl im Browser angehängt wird. Dadurch wird die Zwischenspeicherung umgangen, die sonst bei Zugriffen auf statische HTML-Seiten über das HTTPS-Protokoll erfolgen würde.

**nameSpace (Variable)**

Der Abfragezeichenfolgen-Parameter nameSpace ist bei Implementierungen ohne JavaScript erforderlich.

Beispiel: ns=nameSpace

Den nameSpace-Wert für Ihr Unternehmen erhalten Sie von Ihrem Adobe-Berater oder -Kundenbetreuer.
