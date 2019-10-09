---
description: Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.
seo-description: Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.
seo-title: Namespaces
title: Namespaces
uuid: cab61844-3209-4980-b14c-6859de77606
translation-type: tm+mt
source-git-commit: 21fe6a0ee434e430d77a24d060acd2ffce08e219

---


# Namespaces

Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.

Die Namespace-Zeichenfolge dient zur Identifizierung der Felder, die bei der Bereitstellung einer ID im Rahmen einer Datendatenschutzanforderung durchsucht werden sollen. Wenn eine Datendatenschutzanforderung gesendet wird, enthält die Anforderung einen JSON-Abschnitt, in dem die für die Anforderung zu verwendenden Datensubjekt-IDs angegeben sind. Es können mehrere IDs in einer einzelnen Anfrage für eine betroffene Person enthalten sein. Dieser JSON-Abschnitt enthält Folgendes:

* ein Feld „namespace“ mit der Namespace-Zeichenfolge
* ein Feld „type“, das bei den meisten Adobe Analytics-Anfragen den Wert „analytics“ enthält
* ein Feld „value“, das die ID enthält, nach der Analytics in den zugehörigen Namespace-Variablen all Ihrer Report Suites suchen soll

Refer to the [Experience Cloud Data Privacy API documentation](https://www.adobe.io/apis/cloudplatform/gdpr/docs/alldocs.html#!api-specification/markdown/narrative/gdpr/use-cases/gdpr-api-overview.md) for more details.

<!-- Meike, I converted this table to headings and text to fix a validation error. -Bob -->

## Cookie-ID

Legacy-Analytics-Tracking-Cookie, auch bekannt als Adobe Analytics-ID (AAID):

```
{
   namespace: "AAID",
   type: "standard",
   value: "2CCEEAE88503384F-1188000089CA"
}
```

Der Wert muss in Form von zwei Hexadezimalzahlen, getrennt durch einen Bindestrich, angegeben werden. Alle Hexadezimalzahlen, die alphabetische Zeichen sind, müssen in Großbuchstaben angegeben werden. Die Hexadezimalwerte sollte keine vorangestellten Nullen enthalten. (Beachten Sie die Differenz zum gleichen Wert, der in der veralteten Form angegeben ist, bei der vorangestellte Nullen erforderlich sind.)

Es ist auch akzeptabel, dieses Formular `“namespaceId”: 10` anstelle von oder zusätzlich zu verwenden `“namespace”: “AAID”` und einige andere Adobe-Produkte verwenden es möglicherweise.

## Legacy-Analytics-Tracking-Cookie: Veraltete Form

```
{
   "namespace": "visitorId",
   "type": "analytics",
   "value": "2cceeae88503384f-00001188000089ca"
}
```

Veraltete Form:

Der Wert sollte in Form von zwei 16-stelligen Hexadezimalzahlen oder zwei 19-stelligen Dezimalzahlen angegeben werden. Die Zahlen sollten durch einen Bindestrich, Unterstrich oder Doppelpunkt getrennt sein. Vorangestellte Nullen sollten hinzugefügt werden, wenn beide Zahlen nicht genügend Ziffern haben.

## Identitätsdienst-Cookie

```
{
    namespace: "ECID",
    type: "standard",
    value: "00497781304058976192356650736267671594"
}
```

Der Wert muss in Form einer 38-stelligen Dezimalzahl angegeben werden. Wenn Sie diese Zahl aus den beiden Spalten "mcvisid\_high/low"oder "post\_msvisid\_high/low"aus einem Data Feed oder Data Warehouse-Bericht ziehen, müssen Sie die beiden Zahlen mit null auf 19 Stellen füllen und dann mit dem hohen Wert verketten.

Es ist auch zulässig, Dieses Formular wird `“namespaceId”: 4` anstelle von oder zusätzlich zu `“namespace”: “ECID”` anderen Adobe-Produkten verwendet.

>[!NOTE]
>
>Die Experience Cloud ID (ECID) wurde früher als Marketing Cloud ID (MCID) bezeichnet und wird in einer vorhandenen Dokumentation weiterhin durch diesen Namen referenziert.
>
>Diese IDs sind die einzigen von Analytics unterstützten IDs, die einen anderen "type"-Wert als "analytics"verwenden.

Wenn das Format des Wertanteils einer dieser Cookie-IDs nicht dem für diese ID beschriebenen Format entspricht, schlägt die Datendatenschutzanforderung fehl, mit der Fehlermeldung "Wert nicht korrekt formatiert".

Sie werden diese Cookie-IDs in den meisten Fällen über das neue [Datenschutz-JavaScript](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm) erfassen, das automatisch alle relevanten Schlüssel-/Wertpaare für diese JSON-IDs bereitstellt.

Dieser JavaScript-Code füllt die JSON mit anderen Schlüssel/Wert-Paaren (Namespace, Typ, Wert), aber die oben aufgeführten Felder sind die wichtigsten für die Verarbeitung der Daten in Analytics und die einzigen, die Sie angeben müssen, wenn Sie die IDs auf andere Weise erfassen.

## Benutzerspezifische Besucher-ID

```
{
     namespace: "customVisitorID",
     type: "analytics",
     value: "<ID>"
}
```

Auch für die benutzerspezifische Besucher-ID wird der Namespace vordefiniert.

## IDs in benutzerspezifischen Variablen

```
{
    namespace: "Email Address",
    type: "analytics", 
    value: "john@xyz.com" }, 
{
    namespace: "CRM ID", 
    type: "analytics", 
    value: "123456-ABCD" 
}
```

Bei IDs in Custom Traffic- oder Konversionsvariablen (Props oder eVars) beschriften Sie die Variable mit einer ID-GERÄT- oder ID-PERSON-Beschriftung und weisen Sie dann diesem ID-Typ Ihren eigenen Namespace-Namen zu. Siehe [Namespace-Bereitstellung beim Beschriften einer Variablen als ID-DEVICE oder ID-PERSON.](gdpr-labels.md)

Sie können auch die Namespaces einsehen, die Sie zuvor für andere Variablen oder Report Suites definiert haben und diese wiederverwenden. So können Sie einfach einen Namespace für all Ihre Report Suites verwenden, die diesen ID-Typ enthalten. Darüber hinaus ist es möglich, denselben Namespace mehreren Variablen innerhalb einer Report Suite zuzuweisen. Manche Kunden speichern beispielsweise eine CRM-ID in einer Traffic- oder Konversionsvariablen (je nach Seite, manchmal auch beide). Sie können den Namespace „CRM-ID“ beiden Variablen zuweisen.

> [!TIP] Vermeiden Sie den benutzerfreundlichen Namen einer Variablen (der in der Berichterstellungs-Benutzeroberfläche angezeigte Name) oder die Variablennummer (z. B. eVar12), wenn Sie den Namespace für die Data Privacy API angeben, es sei denn, es handelt sich um den Namespace, der beim Anwenden der ID-GERÄT- oder ID-PERSON-Bezeichnung angegeben wurde. Wenn ein Namespace anstelle eines benutzerfreundlichen Namens verwendet wird, kann derselbe Benutzeridentitätsblock die richtige Variable für mehrere Report Suites angeben. Wenn sich die ID beispielsweise in einigen Report Suites in verschiedenen eVars befindet oder wenn die Anzeigenamen nicht übereinstimmen (z. B. wenn der Anzeigename für eine bestimmte Report Suite lokalisiert wurde).

> [!CAUTION] Die Namespaces "visitorId"und "customVisitorId"sind zur Identifizierung des Legacy-Tracking-Cookies in Analytics und der Analytics-Kunden-Besucher-ID reserviert. Verwenden Sie diese Namespaces nicht für benutzerdefinierten Traffic oder Konversionsvariablen.

Weitere Informationen dazu finden Sie unter [Namespace-Bereitstellung beim Beschriften einer Variablen als ID-DEVICE oder ID-PERSON.](/help/admin/c-data-governance/gdpr-labels.md#section_F0A47AF8DA384A26BD56032D0ABFD2D7)
