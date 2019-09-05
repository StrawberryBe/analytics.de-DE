---
description: Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.
seo-description: Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.
seo-title: Namespaces
title: Namespaces
uuid: cab 61844-3209-4980-b 14 c -8859 de 777606
translation-type: tm+mt
source-git-commit: 9362a59afb6a51bd91d8a94ae5750c4d138fc2f7

---


# Namespaces

Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.

Mit der Namespace-Zeichenfolge identifizieren Sie die Felder, die bei der Bereitstellung einer ID im Rahmen einer DSGVO-Anfrage durchsucht werden sollen. Wenn eine DSGVO-Anfrage eingereicht wird, enthält die Anfrage einen JSON-Abschnitt, der die Datensubjekt-IDs angibt, die für die Anfrage verwendet werden sollen. Es können mehrere IDs in einer einzelnen Anfrage für eine betroffene Person enthalten sein. Dieser JSON-Abschnitt enthält Folgendes:

* ein Feld „namespace“ mit der Namespace-Zeichenfolge
* ein Feld „type“, das bei den meisten Adobe Analytics-Anfragen den Wert „analytics“ enthält
* ein Feld „value“, das die ID enthält, nach der Analytics in den zugehörigen Namespace-Variablen all Ihrer Report Suites suchen soll

Weitere Einzelheiten finden Sie in der [Dokumentation der Experience Cloud-DSGVO-API](https://www.adobe.io/apis/cloudplatform/gdpr/docs/alldocs.html#!api-specification/markdown/narrative/gdpr/use-cases/gdpr-api-overview.md).

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

Es ist auch möglich, anstelle `“namespaceId”: 10` oder zusätzlich zu den `“namespace”: “AAID”` anderen Adobe-Produkten ein anderes Formular zu verwenden.

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

## Cookie für Identitätsdienst

```
{
    namespace: "ECID",
    type: "standard",
    value: "00497781304058976192356650736267671594"
}
```

Der Wert muss in Form einer 38-stelligen Dezimalzahl angegeben werden. Wenn Sie diese Anzahl aus den Spalten "mcvisid\_ high/low" oder" post\_ msvisid\_ high/low" aus einem Datenfeed oder Data Warehouse-Bericht ziehen, müssen Sie jede der beiden Zahlen auf 19 Stellen aufteilen und sie dann mit dem ersten Wert verketten.

Sie können auch Folgendes verwenden: `“namespaceId”: 4` anstelle von oder zusätzlich zu `“namespace”: “ECID”` Ihnen können einige andere Adobe-Produkte dieses Formular verwenden.

>[!NOTE]
>
>Die Experience Cloud ID (ECID) wurde bisher als Marketing Cloud ID (MCID) bezeichnet und wird in einer vorhandenen Dokumentation weiterhin von diesem Namen bezeichnet.
>
>Diese IDs sind die einzigen IDs, die von Analytics unterstützt werden, die einen anderen Wert als "Analytics" verwenden.

Wenn das Format des Werteteils einer dieser Cookie-IDs nicht dem für diese ID beschriebenen Format entspricht, schlägt die DSGVO-Anfrage mit dem Fehler „Wert nicht korrekt formatiert“ fehl.

Sie werden diese Cookie-IDs in den meisten Fällen über das neue [Datenschutz-JavaScript](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm) erfassen, das automatisch alle relevanten Schlüssel-/Wertpaare für diese JSON-IDs bereitstellt.

Der JavaScript-Code füllt den JSON-Abschnitt mit anderen Schlüssel-/Wertpaaren als den oben aufgeführten (Namespace, Typ, Wert). Die oben genannten Felder sind jedoch die wichtigsten für die Analytics-DSGVO-Verarbeitung und die einzigen, die Sie bereitstellen müssen, wenn Sie IDs auf andere Weise erfassen.

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

Für IDs in benutzerdefinierten Traffic- oder Konversionsvariablen (Props oder evars) kennzeichnen Sie die Variable mit einem ID-Gerät oder ID-Personenpersonal und weisen Sie diesem ID-Typ Ihren eigenen Namespace-Namen zu. Siehe [Namespace-Bereitstellung beim Beschriften einer Variablen als ID-DEVICE oder ID-PERSON](gdpr-labels.md).

Sie können auch die Namespaces einsehen, die Sie zuvor für andere Variablen oder Report Suites definiert haben und diese wiederverwenden. So können Sie einfach einen Namespace für all Ihre Report Suites verwenden, die diesen ID-Typ enthalten. Darüber hinaus ist es möglich, denselben Namespace mehreren Variablen innerhalb einer Report Suite zuzuweisen. Manche Kunden speichern beispielsweise eine CRM-ID in einer Traffic- oder Konversionsvariablen (je nach Seite, manchmal auch beide). Sie können den Namespace „CRM-ID“ beiden Variablen zuweisen.

> [!TIP] Vermeiden Sie den Anzeigenamen einer Variablen (der in der Benutzeroberfläche der Berichterstellung angezeigte Name) oder die Nummer der Variablen (z. B. evar 12), wenn Sie den Namespace zur GDPR-API angeben, es sei denn, es handelt sich um den Namespace, der bei Anwendung des ID-Geräts oder der ID-Personenbeschreibung angegeben wurde. Wenn Sie anstelle eines Anzeigenamens einen Namespace verwenden, kann derselbe Benutzeridentitätsblock die richtige Variable für mehrere Report Suites angeben. Wenn sich die ID beispielsweise in verschiedenen evars in einigen der Report Suites befindet oder wenn die Anzeigenamen nicht übereinstimmen (z. B. wenn der Anzeigename für eine bestimmte Report Suite lokalisiert wurde).

> [!CAUTION] Die Namespaces "visitorid" und" customvisitorid" sind für die Identifizierung des Analytics-Legacy-Verfolgungscookies und der Analytics-Kunden-Besucher-ID reserviert. Verwenden Sie diese Namespaces nicht für benutzerdefinierte Traffic- oder Konversionsvariablen.

Weitere Informationen dazu finden Sie unter [Namespace-Bereitstellung beim Beschriften einer Variablen als ID-DEVICE oder ID-PERSON](../../admin/c-data-governance/gdpr-labels.md#section_F0A47AF8DA384A26BD56032D0ABFD2D7).
