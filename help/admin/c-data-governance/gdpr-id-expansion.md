---
description: Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern
title: ID-Erweiterung
feature: Data Governance
exl-id: 312a249f-e0e7-44da-bb3d-b19f1bb4c706
source-git-commit: e9fffe62d3e53ae075610b1feec9a9071d925433
workflow-type: tm+mt
source-wordcount: '1327'
ht-degree: 47%

---

# ID-Erweiterung

Die IDs, die Sie einsenden, decken nicht immer alle Hit-Daten ab, die Analytics dem Datensubjekt zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern:

```
"expandIds": true
```

Weitere Informationen finden Sie in der [Dokumentation der Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de).


| Typ | Zu beachten |
| --- | --- |
| Cookie-ID-Erweiterung | Viele Analytics-Kunden haben ursprünglich die (ältere) [Analytics-Cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-privacy.html?lang=en), aber jetzt verwenden Sie die [Experience Cloud Identity Service (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). Für Benutzer, die die Website erst nach der Umstellung zum ersten Mal besucht haben, ist nur eine ECID vorhanden. Für diejenigen, die zum ersten Mal besucht haben, wenn nur das Legacy-Cookie verfügbar war, aber seitdem Folgendes besucht haben: Einige ihrer Daten enthalten beide Cookies. Die älteren Daten haben jedoch nur das Analytics-Cookie, und in seltenen Fällen verfügen die neuesten Daten möglicherweise nur über eine ECID.<p>Stellen Sie sicher, dass Sie alle Daten für einen Besucher finden, der über ein Analytics-Cookie (Besucher-ID) oder eine ECID identifiziert wurde. Wenn Sie derzeit die ECID verwenden und zuvor das Analytics-Cookie verwendet haben, sollten Sie beim Senden einer Anforderung mit einem der beiden ID-Typen beide IDs in die Anfrage einschließen oder die `expandIds` -Option. Wann `expandIds`sucht Adobe nach anderen ECIDs oder Analytics-Cookies, die den von Ihnen angegebenen Cookie-IDs entsprechen. Die Anfrage wird automatisch erweitert und umfasst diese neu identifizierten Cookie-IDs. |
| Cookie-ID-Erweiterung über benutzerspezifische ID | Auf E-Commerce-Sites ist es nicht ungewöhnlich, dass ein Besucher die Seite durchsucht, Produkte in den Warenkorb legt und den Checkout-Prozess beginnt, noch bevor er sich angemeldet hat. Wenn die ID, die zur Identifizierung von Benutzern für eine Datenschutzanfrage verwendet wird, nur dann in einer benutzerdefinierten Variablen gespeichert wird, wenn der Benutzer angemeldet ist, wird diese Aktivität vor der Anmeldung nicht mit der ID verknüpft. Mithilfe der Analytics-Cookie-ID können Kunden die Aktivität vor der Anmeldung dem Kauf nach der Anmeldung zuordnen, da die Cookie-ID über den Login hinweg bestehen bleibt.<p>Angenommen, Ihre Implementierung speichert eine Anmelde-ID (CRM-ID, Benutzername, Kundennummer, E-Mail-Adresse usw. oder einen Hash eines dieser Werte) in einer benutzerdefinierten Variable („prop“ oder „eVar“) oder einer benutzerdefinierten Besucher-ID und verwendet diese ID dann für eine Datenschutz-Zugriffsanforderung: Das Datensubjekt kann überrascht sein, dass im Rahmen einer Zugriffsanfrage keine Informationen über all sein Surfen zurückgegeben werden, insbesondere wenn Sie Artikel beworben haben, die zwar angesehen, aber noch nicht gekauft wurden. Die Analytics-Datenschutzverarbeitung unterstützt deshalb die ID-Erweiterung, bei der Analytics alle Cookie-IDs sucht, die im selben Hit auftreten wie eine beliebige benutzerspezifische ID, und erweitert die Anfrage daraufhin, damit auch diese IDs enthalten sind.<p>Wann `expandIDs` zusammen mit einem anderen Namespace als einem Cookie-Namespace angegeben ist, wird die Anfrage erweitert und enthält alle Cookie-IDs (ECID oder Analytics-Cookie), die in Treffern mit einer der angegebenen IDs enthalten sind. Die Cookie-ID-Erweiterung, wie oben beschrieben, wird dann für alle neu gefundenen Cookie-IDs durchgeführt.<p>Wenn die `expandIDs` -Option für eine Zugriffsanfrage verwendet wird und die angegebene ID den Titel ID-PERSON aufweist, werden zwei Dateisätze zurückgegeben. Die erste Gruppe (die Personengruppe) enthält nur Daten aus Hits, in denen die angegebene ID gefunden wurde. Die zweite Gruppe (die Gerätegruppe) enthält nur Daten aus erweiterten IDs, in denen die angegebene ID nicht enthalten ist. |

{style=&quot;table-layout:auto&quot;}

## Verwendung der ID-Erweiterung

In den ersten Monaten nach dem Inkrafttreten des Datenschutzes beantragte die überwiegende Mehrheit der Analytics-Datenschutzanfragen keine ID-Erweiterung. Die Bestimmung des geeigneten Werts für Ihre Organisation liegt jedoch bei Ihnen. Wenden Sie sich an Ihr Rechtsabteilung, um zu erfahren, ob eine ID-Erweiterung für Ihre Daten mit den von Ihnen verwendeten IDs und den von Ihnen in Adobe Analytics erfassten Daten erforderlich ist.

Ein vorrangiges Thema sollte sein: Auf einem gemeinsam genutzten Gerät, von dem aus mehrere Benutzer Ihre Site besucht haben, enthält die ID-Erweiterung Daten aus den Treffern anderer Benutzer des Geräts in Daten, die von Zugriffsanfragen zurückgegeben werden (in der Gerätedatei). Selbst wenn Sie bei der Beschriftung Best Practices befolgt haben (z. B. sind keine privaten Daten in der Gerätedatei enthalten, wie z. B. besuchte Seiten), enthält die Gerätedatei die Anzahl der besuchten Seiten und die Zeit jedes Besuchs. Fragen Sie sich: Ist es in Ordnung, wenn Sie diese Informationen an jemanden weitergeben, der möglicherweise nicht der Besucher war?

Wenn die ID-Erweiterung *not* wird für eine Löschanfrage verwendet: Wenn Sie eine Nicht-Cookie-ID (eine andere ID als ECID oder Analytics-Cookie) verwenden, um Treffer zu identifizieren, die gelöscht werden sollen, und diese ID über eine ID-DEVICE-Beschriftung verfügt, ändern sich die Unique Visitor-Zahlen in Berichten. Dies liegt daran, dass nur einige Instanzen der Cookie-IDs anonymisiert werden, während andere unverändert bleiben. Wenn Sie keine ID-Erweiterung angeben, empfehlen wir, entweder eine Cookie-ID für Anfragen zu verwenden oder IDs mit einer ID-PERSON-Beschriftung zu verwenden.

Wenn Adobe eine ID-Erweiterung durchführt, kann eine zusätzliche vollständige Datenüberprüfung erforderlich sein. Dadurch wird die Adobe zum Abschließen der Anforderung verlängert, was oft eine Woche zur Verarbeitungszeit hinzufügt.

## Markierungen von anderen Datenschutzanfragen

Zusätzlich zur Markierung „expandIDs“ unterstützt Analytics zwei weitere Markierungen, die als Teil einer Datenschutzanfrage übergeben werden können. Diese Markierungen und ihre Standardwerte sind:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In Zukunft wird die `analyticsDeleteMethod` kann zusätzlich zum Standardwert &quot;anonymize&quot;den Wert &quot;purge&quot;unterstützen. Wenn dies unterstützt wird, wird der gesamte Treffer gelöscht, anstatt einfach die Werte von Trefferfeldern mit DEL-Beschriftungen zu aktualisieren.

Zusätzlich zum Standardwert wird die `priority` -Feld unterstützt auch den Wert &quot;low&quot;. Diesen Wert sollten Sie für Anfragen angeben, die nicht auf eine Anfrage der betroffenen Person zurückzuführen sind und für die somit keine gesetzliche Verpflichtung besteht, dass diese innerhalb von 30 Tagen abgeschlossen sein müssen.

## Verwendung der Privacy Service-API

>[!IMPORTANT]
>
>Adobe rät von der Anwendung der [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de) aus anderen Gründen als vom Datensubjekt initiierten Anfragen. Die Datenschutz-API ist kein geeignetes Werkzeug für Datenbereinigungen oder -reparaturen und kann unbeabsichtigte Folgen haben. Die Privacy Service-API soll Ihnen dabei helfen, zeitkritische Datenschutzanfragen zu erfüllen. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, für andere Adobe-Kunden eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität bereitzustellen. Wir möchten Sie bitten, die Privacy Service API nicht für andere Zwecke zu verwenden, wie z. B. das Löschen von Daten, die versehentlich durch große Besuchergruppen übermittelt wurden.

Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Dieser Nebeneffekt ist in Situationen unerwünscht, in denen Sie Datenfelder löschen möchten, und zeigt, warum die Privacy Service API für diese Verwendung ungeeignet ist.

Bitte wenden Sie sich an Ihren Account Manager (CSM), um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und die Anstrengungen zur Beseitigung von PII- oder Datenproblemen zu verstärken.
