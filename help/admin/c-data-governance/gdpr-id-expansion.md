---
description: 'Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern '
title: ID-Erweiterung
uuid: 2672d17d-c957-4e08-8dd9-16d54bf2be18
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 100%

---


# ID-Erweiterung

Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern:

```
"expandIds": true
```

Unter [JSON-Beispielanfrage](/help/admin/c-data-governance/gdpr-submit-access-delete.md#sample-json-request) finden Sie ein Beispiel dazu, wie Sie diese Option zur Anfrage hinzufügen. Weitere Informationen finden Sie in der [Dokumentation der Privacy Service API](https://www.adobe.io/apis/experienceplatform/gdpr.html).

<table id="table_A10CA8DC8C1643CF84A4DF30A6740D51"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Typ </th> 
   <th colname="col2" class="entry"> Zu beachten </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-ID-Erweiterung </p> </td> 
   <td colname="col2"> <p>Viele Analytics-Kunden haben ursprünglich das (Legacy) <a href="https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-privacy.html">Analytics-Cookie</a> verwendet, verwenden nun jedoch die <a href="https://docs.adobe.com/content/help/de-DE/id-service/using/home.html">Identity Service (ECID)</a>, die früher als Marketing Cloud ID (MCID) bezeichnet wurde. Für Benutzer, die die Website erst nach der Umstellung zum ersten Mal besucht haben, ist nur eine ECID vorhanden. Bei Benutzern, die die Site schon zu Zeiten des Legacy-Cookies und auch nach der Umstellung besucht haben, werden zwar einige ihrer Daten in beiden Cookies gespeichert, ältere Daten verfügen jedoch nur über ein Analytics-Cookie und die neuesten in seltenen Fällen nur über eine ECID. </p> <p>Sie sollten sicherstellen, dass Sie sämtliche Daten von Besuchern finden, die über ein Analytics-Cookie (Besucher-ID) oder eine ECID identifiziert werden. Wenn Sie also derzeit die ECID verwenden und zuvor das Analytics-Cookie verwendet haben, sollten Sie, wenn Sie eine Anfrage mit einer der beiden Arten von IDs senden, beide IDs in die Anfrage aufnehmen oder die Option „expandIDs“ angeben. Wenn Sie „expandIDs“ angeben, sucht Adobe nach anderen ECIDs oder Analytics-Cookies, die mit den von Ihnen angegebenen Cookie-IDs übereinstimmen. Die Anfrage wird automatisch erweitert, um diese neu gefundenen Cookie-IDs hinzuzufügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie-ID-Erweiterung über benutzerspezifische ID </p> </td> 
   <td colname="col2"> <p>Auf E-Commerce-Sites ist es nicht ungewöhnlich, dass ein Besucher die Seite durchsucht, Produkte in den Warenkorb legt und den Checkout-Prozess beginnt, noch bevor er sich angemeldet hat. Wenn die ID, mit der Benutzer für eine Datenschutzanfrage identifiziert werden, nur dann in einer benutzerdefinierten Variablen gespeichert wird, wenn der Benutzer angemeldet ist, wird diese Voranmeldeaktivität nicht mit der ID verknüpft. Mithilfe der Analytics-Cookie-ID können Kunden die Aktivität vor der Anmeldung dem Kauf nach der Anmeldung zuordnen, da die Cookie-ID über den Login hinweg bestehen bleibt. </p> <p>Angenommen, Ihre Implementierung speichert eine Anmelde-ID (CRM-ID, Benutzername, Kundennummer, E-Mail-Adresse usw. oder einen Hash eines dieser Werte) in einer benutzerdefinierten Variable („prop“ oder „eVar“) oder einer benutzerdefinierten Besucher-ID und verwendet diese ID dann für eine Datenschutz-Zugriffsanforderung: Das Datensubjekt wäre vielleicht überrascht, dass im Rahmen der Zugriffsanfrage nicht alle Informationen über seinen Seitenbesuch zurückgegeben werden, insbesondere wenn Sie Produkte beworben haben, die zwar aufgerufen, aber noch nicht gekauft wurden. </p> <p>Die Analytics-Datenschutzverarbeitung unterstützt deshalb die ID-Erweiterung, bei der Analytics alle Cookie-IDs sucht, die im selben Hit auftreten wie eine beliebige benutzerspezifische ID, und erweitert die Anfrage daraufhin, damit auch diese IDs enthalten sind. </p> <p>Wenn „expandIDs“ gemeinsam mit einem anderen Namespace als dem Cookie-Namespace angegeben wird, wird die Anfrage erweitert, um sämtliche Cookie-IDs (ECID oder Analytics-Cookie) hinzuzufügen, die in Hits mit den angegebenen IDs gefunden wurden. Die Cookie-ID-Erweiterung wird dann wie oben beschrieben für sämtliche neu gefundene Cookie-IDs durchgeführt. </p> <p>Wenn die Option „expandIDs“ für eine Zugriffsanfrage verwendet wird und die angegebene ID über eine ID-PERSON-Beschriftung verfügt, werden zwei Dateiengruppen zurückgegeben. Die erste Gruppe (die Personengruppe) enthält nur Daten aus Hits, in denen die angegebene ID gefunden wurde. Die zweite Gruppe (die Gerätegruppe) enthält nur Daten aus erweiterten IDs, in denen die angegebene ID nicht enthalten ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

In den ersten Monaten nach dem Inkrafttreten des Datenschutzes hat die überwiegende Mehrheit der Analytics-Datenschutzanfragen keine ID-Erweiterung beantragt, doch die Bestimmung des geeigneten Werts für Ihr Unternehmen liegt bei Ihnen. Sie sollten sich mit Ihrer Rechtsabteilung darüber beraten, ob eine Erweiterung der ID für Ihre Daten mit den von Ihnen verwendeten IDs und die von Ihnen in Adobe Analytics erfassten Daten erforderlich ist. Eine wichtige Überlegung sollte sein, dass auf einem gemeinsam genutzten Gerät, von dem aus mehrere Benutzer Ihre Website besucht haben, die Verwendung der ID-Erweiterung Daten von Treffern anderer Benutzer des Geräts in Daten beinhaltet, die von Zugriffsanfragen (in der Gerätedatei) zurückgegeben werden. Selbst wenn Sie bei der Beschriftung Best Practices befolgt haben, sodass keine privaten Daten (z. B. zu besuchten Seiten) in der Gerätedatei enthalten sind, enthält die Gerätedatei die Anzahl der besuchten Seiten und die Zeitpunkte der einzelnen Besuche. Ist es in Ordnung, wenn Sie diese Informationen an jemanden weitergeben, der möglicherweise nicht der Besucher war?

Wenn Sie für eine Löschanfrage, bei der keine ID-Erweiterung verwendet wird, eine Nicht-Cookie-ID (eine andere ID als die ECID oder das Analytics-Cookie) verwenden, um zu löschende Treffer zu identifizieren, und diese ID eine „ID-DEVICE“-Beschriftung hat, ändern sich die Werte für Unique Visitors in Berichten, da nur einige Instanzen der Cookie-IDs anonymisiert werden, während andere unverändert bleiben. Wenn Sie keine ID-Erweiterung angeben, sollten Sie entweder eine Cookie-ID für Anfragen verwenden oder IDs mit einer „ID-PERSON“-Beschriftung verwenden.

Wenn Adobe eine ID-Erweiterung durchführt, kann ein zusätzlicher vollständiger Datenscan erforderlich sein, was die Zeit, die Adobe benötigt, um die Anfrage abzuschließen, erhöht, wodurch die Verarbeitungszeit oft um eine Woche verlängert wird.

## Markierungen von anderen Datenschutzanfragen

Zusätzlich zur Markierung „expandIDs“ unterstützt Analytics zwei weitere Markierungen, die als Teil einer Datenschutzanfrage übergeben werden können. Diese Markierungen und ihre Standardwerte sind:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In Zukunft kann die „analyticsDeleteMethod“ zusätzlich zum Standardwert „anonymize“ den Wert „purge“ unterstützen. Bei der Unterstützung wird der gesamte Treffer gelöscht, anstatt nur die Werte von Trefferfeldern mit DEL-Labels zu aktualisieren.

Zusätzlich zu seinem standardmäßigen Wert unterstützt das Prioritätsfeld auch den Wert „low“. Diesen Wert sollten Sie für Anfragen angeben, die nicht auf eine Anfrage der betroffenen Person zurückzuführen sind und für die somit keine gesetzliche Verpflichtung besteht, dass diese innerhalb von 30 Tagen abgeschlossen sein müssen. Beachten Sie, dass Adobe von der Verwendung der Datenschutz-API aus anderen Gründen als den vom Betroffenen initiierten Anfragen abrät. Die Datenschutz-API ist kein geeignetes Werkzeug für Datenbereinigungen oder -reparaturen und kann unbeabsichtigte Folgen haben.

>[!NOTE]
>
>Die [Privacy Service API](https://www.adobe.io/apis/experienceplatform/gdpr.html) soll Ihnen dabei helfen, zeitkritische Datenschutzanfragen zu erfüllen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, für andere Adobe-Kunden eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität bereitzustellen. Wir möchten Sie bitten, die Privacy Service API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden.

Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Privacy Service API für diese Verwendung ungeeignet ist.

Bitte wenden Sie sich an Ihren Kundenbetreuer (CSM), um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Informationen oder Datenproblemen zu unternehmen.

