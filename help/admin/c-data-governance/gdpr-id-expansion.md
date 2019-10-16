---
description: 'Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann einen erweiterten Satz von IDs erstellen, um diese verknüpften Daten in die Datenschutzanforderungen einzubeziehen. Sie können diese Option mit einem optionalen Parameter für jede gesendete Datendatenschutzanforderung anfordern, die der JSON-Anforderung hinzugefügt wird '
seo-description: 'Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann einen erweiterten Satz von IDs erstellen, um diese verknüpften Daten in die Datenschutzanforderungen einzubeziehen. Sie können diese Option mit einem optionalen Parameter für jede gesendete Datendatenschutzanforderung anfordern, die der JSON-Anforderung hinzugefügt wird '
seo-title: ID-Erweiterung
title: ID-Erweiterung
uuid: 2672d17d-c957-4e08-8dd9-16d54bf2be18
translation-type: tm+mt
source-git-commit: 3be4e96df12d5e53bf77b1960afc229a1ac6c046

---


# ID-Erweiterung

Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann einen erweiterten Satz von IDs erstellen, um diese verknüpften Daten in die Datenschutzanforderungen einzubeziehen. Sie können diese Option mit einem optionalen Parameter für jede gesendete Datenschutzanforderung anfordern, die der JSON-Anforderung hinzugefügt wird:

```
"expandIds": true
```

Unter [JSON-Beispielanfrage](/help/admin/c-data-governance/gdpr-submit-access-delete.md#sample-json-request) finden Sie ein Beispiel dazu, wie Sie diese Option zur Anfrage hinzufügen. For more details, refer to the [Privacy Service API documentation.](https://www.adobe.io/apis/experienceplatform/gdpr.html)

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
   <td colname="col2"> <p>Viele Analytics-Kunden haben ursprünglich das <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_analytics.html" format="html" scope="external">(Legacy-)Analytics-Cookie</a> verwendet, verwenden nun jedoch die <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/" format="https" scope="external">Identity Service (ECID)</a>, die früher als Experience Cloud ID (MCID) bezeichnet wurde. Für Benutzer, die die Website erst nach der Umstellung zum ersten Mal besucht haben, ist nur eine ECID vorhanden. Bei Benutzern, die die Site schon zu Zeiten des Legacy-Cookies und auch nach der Umstellung besucht haben, werden zwar einige ihrer Daten in beiden Cookies gespeichert, ältere Daten verfügen jedoch nur über ein Analytics-Cookie und die neuesten in seltenen Fällen nur über eine ECID. </p> <p>Sie sollten sicherstellen, dass Sie sämtliche Daten von Besuchern finden, die über ein Analytics-Cookie (Besucher-ID) oder eine ECID identifiziert werden. Wenn Sie also derzeit die ECID verwenden und zuvor das Analytics-Cookie verwendet haben, sollten Sie, wenn Sie eine Anfrage mit einer der beiden Arten von IDs senden, beide IDs in die Anfrage aufnehmen oder die Option „expandIDs“ angeben. Wenn Sie „expandIDs“ angeben, sucht Adobe nach anderen ECIDs oder Analytics-Cookies, die mit den von Ihnen angegebenen Cookie-IDs übereinstimmen. Die Anfrage wird automatisch erweitert, um diese neu gefundenen Cookie-IDs hinzuzufügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie-ID-Erweiterung über benutzerspezifische ID </p> </td> 
   <td colname="col2"> <p>Auf E-Commerce-Sites ist es nicht ungewöhnlich, dass ein Besucher die Seite durchsucht, Produkte in den Warenkorb legt und zur Kasse geht, noch bevor er sich angemeldet hat. Wenn die ID, mit der Benutzer für eine Datendatenschutzanforderung identifiziert werden, nur bei der Anmeldung des Benutzers in einer benutzerdefinierten Variablen gespeichert wird, wird diese Aktivität vor der Anmeldung nicht mit der ID verknüpft. Mithilfe der Analytics-Cookie-ID können Kunden die Aktivität vor der Anmeldung dem Kauf nach der Anmeldung zuordnen, da die Cookie-ID über den Login hinweg bestehen bleibt. </p> <p>Nehmen wir an, Ihre Implementierung speichert eine Anmelde-ID (CRM-ID, Benutzername, Treuhandnummer, E-Mail-Adresse usw. oder einen Hash dieser Werte) in einer benutzerspezifischen Variablen (prop oder eVar) oder einer benutzerdefinierten Besucher-ID und verwendet diese ID dann für eine Datendatenschutzanforderung. Das Datensubjekt wäre vielleicht überrascht, dass im Rahmen der Zugriffsanfrage nicht alle Informationen über seinen Seitenbesuch zurückgegeben werden, insbesondere wenn Sie Produkte beworben haben, die zwar aufgerufen, aber noch nicht gekauft wurden. </p> <p>Die Verarbeitung zum Datenschutz in Analytics unterstützt daher die ID-Erweiterung, bei der Analytics alle Cookie-IDs findet, die im selben Treffer wie eine benutzerdefinierte ID auftreten, und dann die Anforderung erweitert, um auch diese IDs einzuschließen. </p> <p>Wenn „expandIDs“ gemeinsam mit einem anderen Namespace als dem Cookie-Namespace angegeben wird, wird die Anfrage erweitert, um sämtliche Cookie-IDs (ECID oder Analytics-Cookie) hinzuzufügen, die in Hits mit den angegebenen IDs gefunden wurden. Die Cookie-ID-Erweiterung wird dann wie oben beschrieben für sämtliche neu gefundene Cookie-IDs durchgeführt. </p> <p>Wenn die Option „expandIDs“ für eine Zugriffsanfrage verwendet wird und die angegebene ID über eine ID-PERSON-Beschriftung verfügt, werden zwei Dateiengruppen zurückgegeben. Die erste Gruppe (die Personengruppe) enthält nur Daten aus Hits, in denen die angegebene ID gefunden wurde. Die zweite Gruppe (die Gerätegruppe) enthält nur Daten aus erweiterten IDs, in denen die angegebene ID nicht enthalten ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

In den ersten Monaten nach der Live-Schaltung des Datenschutzes wurde bei der überwiegenden Mehrheit der Analytics-Datendatenschutzanforderungen keine ID-Erweiterung angefordert, aber die Ermittlung des entsprechenden Werts für Ihr Unternehmen liegt bei Ihnen. Sie sollten sich mit Ihrer Rechtsabteilung darüber beraten, ob eine Erweiterung der ID für Ihre Daten mit den von Ihnen verwendeten IDs und die von Ihnen in Adobe Analytics erfassten Daten erforderlich ist. Eine wichtige Überlegung sollte sein, dass auf einem gemeinsam genutzten Gerät, von dem aus mehrere Benutzer Ihre Website besucht haben, die Verwendung der ID-Erweiterung Daten von Treffern anderer Benutzer des Geräts in Daten beinhaltet, die von Zugriffsanfragen (in der Gerätedatei) zurückgegeben werden. Selbst wenn Sie bei der Beschriftung bewährte Verfahren befolgt haben, sodass keine privaten Daten (z. B. zu besuchten Seiten) in der Gerätedatei enthalten sind, enthält die Gerätedatei die Anzahl der besuchten Seiten und die Zeitpunkte der einzelnen Besuche. Ist es in Ordnung, wenn Sie diese Informationen an jemanden weitergeben, der möglicherweise nicht der Besucher war?

Wenn Sie für eine Löschanfrage, bei der keine ID-Erweiterung verwendet wird, eine Nicht-Cookie-ID (eine andere ID als die ECID oder das Analytics-Cookie) verwenden, um zu löschende Treffer zu identifizieren, und diese ID eine „ID-DEVICE“-Beschriftung hat, ändern sich die Werte für Unique Visitors in Berichten, da nur einige Instanzen der Cookie-IDs anonymisiert werden, während andere unverändert bleiben. Wenn Sie keine ID-Erweiterung angeben, sollten Sie entweder eine Cookie-ID für Anfragen verwenden oder IDs mit einer „ID-PERSON“-Beschriftung verwenden.

Wenn Adobe eine ID-Erweiterung durchführt, kann ein zusätzlicher vollständiger Datenscan erforderlich sein, was die Zeit, die Adobe benötigt, um die Anfrage abzuschließen, erhöht, wodurch die Verarbeitungszeit oft um eine Woche verlängert wird.

## Flags von anderen Datenschutzanfragen

Zusätzlich zum Flag "developIDs"unterstützt Analytics zwei weitere Flags, die als Teil einer Datenschutzanforderung weitergeleitet werden können. Diese Markierungen und ihre Standardwerte sind:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In Zukunft wird der Wert "analyticsDeleteMethod"möglicherweise zusätzlich zum Standardwert "anonymisieren"den Wert "bereinigen"unterstützen. Bei der Unterstützung wird der gesamte Treffer gelöscht, anstatt nur die Werte von Trefferfeldern mit DEL-Labels zu aktualisieren.

Neben dem Standardwert unterstützt das Prioritätsfeld auch den Wert "low". Diesen Wert sollten Sie für Anfragen angeben, die nicht auf eine Anfrage der betroffenen Person zurückzuführen sind und für die somit keine gesetzliche Verpflichtung besteht, dass diese innerhalb von 30 Tagen abgeschlossen sein müssen. Beachten Sie, dass Adobe die Verwendung der Datenschutzdienst-API aus anderen Gründen als den von den betroffenen Personen initiierten Anforderungen ablehnt. Die Datenschutzdienst-API ist kein geeignetes Werkzeug zur Datenbereinigung oder -reparatur und hat unbeabsichtigte Folgen.

[!NOTE]
Die [Datenschutzdienst-API](https://www.adobe.io/apis/experienceplatform/gdpr.html) wurde bereitgestellt, um Ihnen bei der Erfüllung von Datenschutzanfragen behilflich zu sein, die zeitempfindlich sind. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann sich auf die Fähigkeit von Adobe auswirken, für andere Adobe-Kunden eine zeitnahe Umstellung auf vom Benutzer initiierte Datenschutzanforderungen mit hoher Priorität bereitzustellen. Wir bitten Sie, die Datenschutzdienst-API nicht für andere Zwecke zu verwenden, z. B. zum Löschen von Daten, die versehentlich über große Besuchergruppen gesendet wurden.

Sie sollten außerdem wissen, dass bei jedem Besucher, der infolge einer Löschungsanfrage zum Datenschutz einen Treffer gelöscht (aktualisiert oder anonymisiert) hat, die Statusinformationen zurückgesetzt werden. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen, in denen Sie Datenfelder löschen möchten, nicht wünschenswert und zeigt einen Grund an, warum die Datenschutzdienst-API für diese Verwendung nicht geeignet ist.

Bitte wenden Sie sich an Ihren Kundenbetreuer (CSM), um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Informationen oder Datenproblemen zu unternehmen.

