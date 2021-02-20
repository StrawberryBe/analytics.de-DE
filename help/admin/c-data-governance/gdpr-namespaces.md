---
description: Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.
title: Namespaces
uuid: cab61844-3209-4980-b14c-6859de777606
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 100%

---


# Namensraum

Jeder ID, nach der Sie suchen können möchten, wird ein Namespace zugewiesen. Hierbei handelt es sich um eine benutzerspezifische Zeichenfolge, die die entsprechende ID über alle Report Suites hinweg in jeder Variablen, in der sie verwendet wird, identifiziert.

Mit der Namespace-Zeichenfolge identifizieren Sie die Felder, die bei der Bereitstellung einer ID im Rahmen einer Datenschutzanfrage durchsucht werden sollen. Wenn eine Datenschutzanfrage eingereicht wird, enthält die Anfrage einen JSON-Abschnitt, der die Datensubjekt-IDs angibt, die für die Anfrage verwendet werden sollen. Es können mehrere IDs in einer einzelnen Anfrage für eine betroffene Person enthalten sein. Dieser JSON-Abschnitt enthält Folgendes:

* ein Feld „namespace“ mit der Namespace-Zeichenfolge
* ein Feld „type“, das bei den meisten Adobe Analytics-Anfragen den Wert „analytics“ enthält
* ein Feld „value“, das die ID enthält, nach der Analytics in den zugehörigen Namespace-Variablen all Ihrer Report Suites suchen soll

Weitere Einzelheiten finden Sie in der [Dokumentation der Experience Cloud-Datenschutz-API](https://docs.adobe.com/content/help/de-DE/experience-platform/privacy/home.html#!api-specification/markdown/narrative/technical_overview/privacy_service_overview/privacy_service_overview.md).

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

Es ist auch möglich, `"namespaceId": 10` anstelle von oder zusätzlich zu `"namespace": "AAID"` zu verwenden. Auch andere Adobe-Produkte können diese Form verwenden.

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

## Identity Service Cookie

```
{
    namespace: "ECID",
    type: "standard",
    value: "00497781304058976192356650736267671594"
}
```

Der Wert muss in Form einer 38-stelligen Dezimalzahl angegeben werden. Wenn Sie diese Zahl aus den beiden Spalten „mcvisid\_high/low“ oder „post\_msvisid\_high/low“ aus einem Daten-Feed- oder Data Warehouse-Bericht beziehen, müssen Sie jede der beiden Zahlen mit Nullen auf 19 Stellen auffüllen und sie dann mit dem hohen Wert voran verknüpfen.

Es ist auch möglich, `"namespaceId": 4` anstelle von oder zusätzlich zu `"namespace": "ECID"` zu verwenden. Auch andere Adobe-Produkte können diese Form verwenden.

>[!NOTE]
>
>Die Experience Cloud ID (ECID) wurde früher als Marketing Cloud ID (MCID) bezeichnet. Dementsprechend findet sich dieser Name noch in älteren Dokumentationen.
>
>Diese IDs sind die einzigen von Analytics unterstützten IDs, die für „type“ einen anderen Wert verwenden als „analytics“.

Wenn das Format des Werteteils einer dieser Cookie-IDs nicht dem für diese ID beschriebenen Format entspricht, schlägt die Datenschutzanfrage mit dem Fehler „Wert nicht korrekt formatiert“ fehl.

Sie werden diese Cookie-IDs in den meisten Fällen über das neue [Datenschutz-JavaScript](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm) erfassen, das automatisch alle relevanten Schlüssel-/Wertpaare für diese JSON-IDs bereitstellt.

Der JavaScript-Code füllt den JSON-Abschnitt mit anderen Schlüssel-Wert-Paaren als den oben aufgeführten (Namespace, Typ, Wert). Die oben genannten Felder sind jedoch die wichtigsten für die Analytics-Datenschutzverarbeitung und die einzigen, die Sie bereitstellen müssen, wenn Sie IDs auf andere Weise erfassen.

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

Bei IDs in benutzerspezifischen Traffic- oder Konversionsvariablen (Props oder eVars) müssen Sie die Variable mit einer ID-DEVICE- oder ID-PERSON-Beschriftung versehen und diesem ID-Typ daraufhin einen eigenen Namespace-Namen zuweisen. Siehe [Namespace-Bereitstellung beim Beschriften einer Variablen als ID-DEVICE oder ID-PERSON.](gdpr-labels.md)

Sie können auch die Namespaces einsehen, die Sie zuvor für andere Variablen oder Report Suites definiert haben und diese wiederverwenden. So können Sie einfach einen Namespace für all Ihre Report Suites verwenden, die diesen ID-Typ enthalten. Darüber hinaus ist es möglich, denselben Namespace mehreren Variablen innerhalb einer Report Suite zuzuweisen. Manche Kunden speichern beispielsweise eine CRM-ID in einer Traffic- oder Konversionsvariablen (je nach Seite, manchmal auch beide). Sie können den Namespace „CRM-ID“ beiden Variablen zuweisen.

>[!TIP]
>
>Vermeiden Sie bei der Namespace-Angabe für die Data Privacy-API die Verwendung des Anzeigenamens einer Variablen (der auf der Benutzeroberfläche für das Reporting angezeigte Name) oder die Nummer der Variablen (z. B. eVar12), es sei denn, es handelt sich um den Namespace, den Sie beim Anwenden der Beschriftung ID-DEVICE oder ID-PERSON angegeben haben. Durch die Verwendung eines Namespace anstelle eines Anzeigenamens kann mithilfe desselben Benutzeridentitätsblocks die korrekte Variable für mehrere Report Suites angegeben werden. Dies ist beispielsweise der Fall, wenn die ID in manchen Report Suites in unterschiedlichen eVars ist oder die Anzeigenamen nicht übereinstimmen (z. B. wenn der Anzeigename für eine bestimmte Report Suite lokalisiert wurde).

>[!CAUTION]
>
>Die Namespaces „visitorId“ und „customVisitorId“ sind zur Identifikation des früheren Tracking-Cookies von Analytics und der benutzerdefinierten Besucher-ID von Analytics reserviert. Verwenden Sie diese Namespaces nicht für benutzerdefinierte Traffic-Variablen oder Konversionsvariablen.

Weitere Informationen dazu finden Sie unter [Namespace-Bereitstellung beim Beschriften einer Variablen als ID-DEVICE oder ID-PERSON.](/help/admin/c-data-governance/gdpr-labels.md)
