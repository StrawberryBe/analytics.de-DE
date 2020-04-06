---
description: 'Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern '
title: ID-Erweiterung
uuid: 2672d17d-c957-4e08-8dd9-16d54bf2be18
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

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
   <td colname="col2"> <p>Viele Analytics-Kunden haben ursprünglich das (Legacy) <a href="https://marketing.adobe.com/resources/help/de_DE/whitepapers/cookies/cookies_analytics.html">Analytics-Cookie</a> verwendet, verwenden nun jedoch die <a href="https://marketing.adobe.com/resources/help/de_DE/mcvid/">Identity Service (ECID)</a>, die früher als Marketing Cloud ID (MCID) bezeichnet wurde. Für Besucher ihrer Website, die die Website zum ersten Mal nach der Transition besucht haben, gibt es nur die ECID. Für diejenigen, die zum ersten Mal besucht haben, wenn nur das Legacy-Cookie verfügbar war, die jedoch seitdem Folgendes besucht haben: Einige ihrer Daten enthalten beide Cookies, aber die älteren Daten enthalten nur das Analytics-Cookie, und in seltenen Fällen haben die neuesten Daten möglicherweise nur eine ECID. </p> <p>Sie möchten sicherstellen, dass Sie alle Daten zu einem Besucher finden, der über ein Analytics-Cookie (Besucher-ID) oder eine ECID identifiziert wurde. Wenn Sie die ECID derzeit verwenden und zuvor das Analytics-Cookie verwendet haben, sollten Sie bei jeder Anforderung mit einem der ID-Typen beide IDs in die Anforderung einschließen oder die Option "developIds"angeben. Wenn Sie die Option "expandierenIDs"angeben, sucht Adobe nach anderen ECIDs oder Analytics-Cookies, die den von Ihnen angegebenen Cookie-IDs entsprechen. Die Anforderung wird automatisch erweitert, um diese neu identifizierten Cookie-IDs einzuschließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerdefinierte ID zu Cookie-ID-Erweiterung </p> </td> 
   <td colname="col2"> <p>Auf E-Commerce-Sites ist es nicht ungewöhnlich, dass ein Besucher die Seite durchsucht, Produkte in den Warenkorb legt und den Checkout-Prozess beginnt, noch bevor er sich angemeldet hat. Wenn die ID, mit der Benutzer für eine Datenschutzanfrage identifiziert werden, nur dann in einer benutzerdefinierten Variablen gespeichert wird, wenn der Benutzer angemeldet ist, wird diese Voranmeldeaktivität nicht mit der ID verknüpft. Mithilfe der Analytics-Cookie-ID können Kunden die Aktivität vor der Anmeldung dem Kauf nach der Anmeldung zuordnen, da die Cookie-ID über den Login hinweg bestehen bleibt. </p> <p>Angenommen, Ihre Implementierung speichert eine Anmelde-ID (CRM-ID, Benutzername, Kundennummer, E-Mail-Adresse usw. oder einen Hash eines dieser Werte) in einer benutzerdefinierten Variable („prop“ oder „eVar“) oder einer benutzerdefinierten Besucher-ID und verwendet diese ID dann für eine Datenschutz-Zugriffsanforderung: Das Datensubjekt wäre vielleicht überrascht, dass im Rahmen der Zugriffsanfrage nicht alle Informationen über seinen Seitenbesuch zurückgegeben werden, insbesondere wenn Sie Produkte beworben haben, die zwar aufgerufen, aber noch nicht gekauft wurden. </p> <p>Die Analytics-Datenschutzverarbeitung unterstützt deshalb die ID-Erweiterung, bei der Analytics alle Cookie-IDs sucht, die im selben Hit auftreten wie eine beliebige benutzerspezifische ID, und erweitert die Anfrage daraufhin, damit auch diese IDs enthalten sind. </p> <p>Wenn Sie die Option "extendedIDs"zusammen mit einem anderen Namensraum als einem Cookie-Namensraum angeben, wird die Anforderung erweitert und enthält nun alle Cookie-IDs (ECID oder Analytics-Cookies), die in Treffern mit einer der angegebenen IDs enthalten sind. Die Erweiterung der Cookie-ID, wie oben beschrieben, wird dann mit allen neu gefundenen Cookie-IDs durchgeführt. </p> <p>Wenn die Option "expandeIDs"für eine Zugriffsanforderung verwendet wird und die angegebene ID eine ID-PERSON-Bezeichnung hat, werden zwei Dateien zurückgegeben. Der erste Satz (der Personensatz) enthält nur Daten aus Treffern, bei denen die angegebene ID gefunden wurde. Der zweite Satz (der Gerätesatz) enthält nur Daten aus Treffern der erweiterten IDs, bei denen die angegebene ID nicht vorhanden war. </p> </td> 
  </tr> 
 </tbody> 
</table>

In den ersten Monaten nach dem Inkrafttreten des Datenschutzes hat die überwiegende Mehrheit der Analytics-Datenschutzanfragen keine ID-Erweiterung beantragt, doch die Bestimmung des geeigneten Werts für Ihr Unternehmen liegt bei Ihnen. Sie sollten sich mit Ihrem Juristischen Team darüber beraten, ob die ID-Erweiterung für Ihre Daten mit den von Ihnen verwendeten IDs und den in Adobe Analytics erfassten Daten erforderlich ist. Bei einem freigegebenen Gerät, von dem mehrere Benutzer Ihre Site besucht haben, sollte in erster Linie berücksichtigt werden, dass die ID-Erweiterung Daten von Treffern anderer Benutzer des Geräts in Daten enthält, die von Zugriffsanfragen zurückgegeben werden (in der Gerätedatei). Auch wenn Sie bei der Kennzeichnung die Best Practices befolgt haben, sodass keine privaten Daten in die Gerätedatei aufgenommen werden, wie z. B. besuchte Seiten, enthält die Gerätedatei die Anzahl der besuchten Seiten und die Zeiten jedes einzelnen Besuchs. Ist es in Ordnung, wenn Sie diese Informationen mit jemandem teilen, der nicht der Besucher war?

Bei einer Löschanforderung, bei der keine ID-Erweiterung verwendet wird, wenn Sie eine Nicht-Cookie-ID (eine andere ID als die ECID oder das Analytics-Cookie) verwenden, um Treffer zu identifizieren, die gelöscht werden sollen, und diese ID eine ID-GERÄT-Bezeichnung aufweist, ändert sich die Anzahl der individuellen Besucher in Berichten, da nur einige Instanzen der Cookie-IDs anonymisiert werden, während andere unverändert bleiben. Wenn Sie keine ID-Erweiterung angeben, sollten Sie entweder eine Cookie-ID für Anforderungen verwenden oder IDs mit einer ID-PERSON-Bezeichnung verwenden.

Wenn Adobe ID-Erweiterungen durchführt, kann eine zusätzliche vollständige Datenprüfung erforderlich sein. Dies verlängert die Verarbeitungszeit, die Adobe zum Abschließen der Anforderung benötigt, und fügt der Verarbeitungszeit oft eine Woche hinzu.

## Markierungen von anderen Datenschutzanfragen

Zusätzlich zur Markierung „expandIDs“ unterstützt Analytics zwei weitere Markierungen, die als Teil einer Datenschutzanfrage übergeben werden können. Diese Markierungen und ihre Standardwerte sind:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In Zukunft kann die „analyticsDeleteMethod“ zusätzlich zum Standardwert „anonymize“ den Wert „purge“ unterstützen. Bei der Unterstützung wird der gesamte Treffer gelöscht, anstatt nur die Werte von Trefferfeldern mit DEL-Labels zu aktualisieren.

Zusätzlich zu seinem standardmäßigen Wert unterstützt das Prioritätsfeld auch den Wert „low“. Diesen Wert sollten Sie für Anfragen angeben, die nicht auf eine Anfrage der betroffenen Person zurückzuführen sind und für die somit keine gesetzliche Verpflichtung besteht, dass diese innerhalb von 30 Tagen abgeschlossen sein müssen. Beachten Sie, dass Adobe von der Verwendung der Datenschutz-API aus anderen Gründen als den vom Betroffenen initiierten Anfragen abrät. Die Datenschutz-API ist kein geeignetes Werkzeug für Datenbereinigungen oder -reparaturen und kann unbeabsichtigte Folgen haben.

>[!NOTE] Die [Privacy Service API](https://www.adobe.io/apis/experienceplatform/gdpr.html) soll Ihnen dabei helfen, zeitkritische Datenschutzanfragen zu erfüllen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, für andere Adobe-Kunden eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität bereitzustellen. Wir möchten Sie bitten, die Privacy Service API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden.

Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Privacy Service API für diese Verwendung ungeeignet ist.

Bitte wenden Sie sich an Ihren Kundenbetreuer (CSM), um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Informationen oder Datenproblemen zu unternehmen.

