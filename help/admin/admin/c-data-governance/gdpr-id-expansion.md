---
description: Die von Ihnen übermittelten IDs decken nicht immer alle Trefferdaten ab, die Analytics der betroffenen Person zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern
title: ID-Erweiterung
feature: Data Governance
exl-id: 312a249f-e0e7-44da-bb3d-b19f1bb4c706
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '1348'
ht-degree: 97%

---

# ID-Erweiterung

Die von Ihnen übermittelten IDs decken nicht immer alle Trefferdaten ab, die Analytics der betroffenen Person zuordnen kann. Analytics kann eine erweiterte ID-Gruppe erstellen, um diese zugehörigen Daten zu den Datenschutzanfragen hinzuzufügen. Mit einem optionalen Parameter, der zur JSON-Anfrage hinzugefügt wird, können Sie diese Option für jede eingereichte Datenschutzanfrage anfordern:

```
"expandIds": true
```

Weitere Informationen finden Sie in der [Dokumentation der Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de).


| Typ | Zu beachten |
| --- | --- |
| Cookie-ID-Erweiterung | Viele Analytics-Kundinnen und -Kunden haben ursprünglich den (älteren) [Analytics-Cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-privacy.html?lang=de) verwendet, nutzen jedoch mittlerweile den [Experience Cloud Identity Service (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). Für Benutzende, die die Website erst nach der Umstellung zum ersten Mal besucht haben, ist nur eine ECID vorhanden. Für diejenigen, die die Website zum ersten Mal besucht haben, als nur das Legacy-Cookie verfügbar war, und die uns seither nochmals besucht haben, sind einige ihrer Daten in beiden Cookies enthalten. Die älteren Daten haben jedoch nur das Analytics-Cookie, und in seltenen Fällen verfügen die neuesten Daten möglicherweise nur über eine ECID.<p>Sie sollten sicherstellen, dass Sie sämtliche Daten von Personen finden, die über ein Analytics-Cookie (eine Besucher-ID) oder eine ECID identifiziert werden. Wenn Sie also derzeit die ECID verwenden und zuvor das Analytics-Cookie verwendet haben, sollten Sie, wenn Sie eine Anfrage mit einer der beiden Arten von IDs senden, beide IDs in die Anfrage aufnehmen oder die Option `expandIds` angeben. Wenn Sie `expandIds` angeben, sucht Adobe nach anderen ECIDs oder Analytics-Cookies, die den von Ihnen angegebenen Cookie-IDs entsprechen. Die Anfrage wird automatisch erweitert, um diese neu gefundenen Cookie-IDs hinzuzufügen. |
| Cookie-ID-Erweiterung über benutzerspezifische ID | Auf E-Commerce-Sites ist es nicht ungewöhnlich, dass ein Besucher die Seite durchsucht, Produkte in den Warenkorb legt und den Checkout-Prozess beginnt, noch bevor er sich angemeldet hat. Wenn die ID, mit der Benutzende für eine Datenschutzanfrage identifiziert werden, nur für angemeldete Benutzende in einer benutzerdefinierten Variablen gespeichert wird, wird diese Aktivität, die vor der Anmeldung stattgefunden hat, nicht mit der ID verknüpft. Mithilfe der Analytics-Cookie-ID können Kunden die Aktivität vor der Anmeldung dem Kauf nach der Anmeldung zuordnen, da die Cookie-ID über den Login hinweg bestehen bleibt.<p>Angenommen, Ihre Implementierung speichert eine Anmelde-ID (CRM-ID, Benutzername, Kundennummer, E-Mail-Adresse usw. oder einen Hash eines dieser Werte) in einer benutzerdefinierten Variable („prop“ oder „eVar“) oder einer benutzerdefinierten Besucher-ID und verwendet diese ID dann für eine Datenschutz-Zugriffsanforderung: Die betroffene Person wäre vielleicht überrascht, dass im Rahmen der Zugriffsanfrage nicht alle Informationen über ihren Seitenbesuch zurückgegeben werden, insbesondere wenn Sie Produkte beworben haben, die zwar aufgerufen, aber noch nicht gekauft wurden. Die Analytics-Datenschutzverarbeitung unterstützt deshalb die ID-Erweiterung, bei der Analytics alle Cookie-IDs sucht, die im selben Treffer auftreten wie eine beliebige benutzerspezifische ID, und erweitert die Anfrage daraufhin so, dass auch diese IDs enthalten sind.<p>Wenn `expandIDs` gemeinsam mit einem anderen Namespace als dem Cookie-Namespace angegeben wird, wird die Anfrage erweitert, um sämtliche Cookie-IDs (ECID- oder Analytics-Cookie) hinzuzufügen, die in Treffern mit irgendeiner der angegebenen IDs gefunden wurden. Die Cookie-ID-Erweiterung wird dann wie oben beschrieben für sämtliche neu gefundenen Cookie-IDs durchgeführt.<p>Wenn die Option `expandIDs` für eine Zugriffsanfrage verwendet wird und die angegebene ID über eine ID-PERSON-Kennzeichnung verfügt, werden zwei Dateiengruppen zurückgegeben. Die erste Gruppe (die Personengruppe) enthält nur Daten aus Hits, in denen die angegebene ID gefunden wurde. Die zweite Gruppe (die Gerätegruppe) enthält nur Daten aus erweiterten IDs, in denen die angegebene ID nicht enthalten ist. |

{style="table-layout:auto"}

## Verwendungszeitpunkt der ID-Erweiterung

In den ersten Monaten nach der Einführung des Datenschutzes beantragte die überwiegende Mehrheit der Analytics-Datenschutzanfragen keine ID-Erweiterung. Die Bestimmung des geeigneten Werts für Ihre Organisation liegt jedoch bei Ihnen. Sie sollten sich von Ihrer Rechtsabteilung beraten lassen, ob eine Erweiterung der ID für Ihre Daten mit den von Ihnen verwendeten IDs und den von Ihnen in Adobe Analytics erfassten Daten erforderlich ist.

Zu berücksichtigen ist dabei: Auf einem gemeinsam genutzten Gerät, von dem aus mehrere Benutzende Ihre Website besucht haben, beinhaltet die Verwendung der ID-Erweiterung Daten von Treffern anderer Benutzender des Geräts in Daten, die von Zugriffsanfragen (in der Gerätedatei) zurückgegeben werden. Selbst wenn Sie bei der Kennzeichnung Best Practices befolgt haben (sodass z. B. keine privaten Daten in der Gerätedatei enthalten sind), enthält die Gerätedatei die Anzahl der besuchten Seiten und die Zeitpunkte der einzelnen Besuche. Sie können sich daher fragen: Ist es in Ordnung, wenn Sie diese Informationen an eine Person weitergeben, die die Seite möglicherweise nicht besucht hat?

Wenn die ID-Erweiterung *nicht* für eine Löschanfrage verwendet wird: Falls Sie eine Nicht-Cookie-ID (kein ECID- oder Analytics-Cookie) verwenden, um Treffer zu identifizieren, die gelöscht werden sollen, und diese ID über eine ID-DEVICE-Kennzeichnung verfügt, ändern sich die Unique Visitor-Zahlen in Berichten. Dies liegt daran, dass nur einige Instanzen der Cookie-IDs anonymisiert werden, während andere unverändert bleiben. Wenn Sie keine ID-Erweiterung angeben, sollten Sie entweder eine Cookie-ID n oder IDs mit einer ID-PERSON-Kennzeichnung für Anfragen verwenden.

Wenn Adobe eine ID-Erweiterung durchführt, kann eine zusätzliche vollständige Datenüberprüfung erforderlich sein. Dadurch wird die Zeit verlängert, die Adobe zum Bearbeiten der Anfrage benötigt, was oft eine Woche zur Verarbeitungszeit hinzufügt.

## Markierungen von anderen Datenschutzanfragen

Zusätzlich zur Markierung „expandIDs“ unterstützt Analytics zwei weitere Markierungen, die als Teil einer Datenschutzanfrage übergeben werden können. Diese Markierungen und ihre Standardwerte sind:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In Zukunft könnte die `analyticsDeleteMethod` zusätzlich zum Standardwert „anonymize“ den Wert „purge“ unterstützen. Im Fall einer Unterstützung wird der gesamte Treffer gelöscht, anstatt nur die Werte von Trefferfeldern mit DEL-Kennzeichnungen zu aktualisieren.

Zusätzlich zu seinem standardmäßigen Wert unterstützt das Feld `priority` auch den Wert „niedrig“. Diesen Wert sollten Sie für Anfragen angeben, die nicht auf eine Anfrage der betroffenen Person zurückzuführen sind und für die somit keine gesetzliche Verpflichtung besteht, dass diese innerhalb eines bestimmten Zeitrahmens abgeschlossen sein müssen.

## Verwendung der Privacy Service-API

>[!IMPORTANT]
>
>Adobe gestattet die Verwendung der [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=de) nur für gültige, vom Datensubjekt initiierte Anfragen. Die Privacy Service-API ist kein geeignetes Tool zur Datenbereinigung oder -reparatur. Jede missbräuchliche Verwendung der Privacy Service-API für Anfragen, die nicht von der betroffenen Person initiiert wurden, hat unbeabsichtigte Folgen. Die Privacy Service-API wird Kundinnen und Kunden von Adobe zur Verfügung gestellt, damit Sie zeitkritische Datenschutzanfragen erfüllen können. Die Verwendung dieser API für andere Zwecke wird von Adobe nicht unterstützt und kann die Fähigkeit von Adobe beeinträchtigen, anderen Kundinnen und Kunden von Adobe eine rechtzeitige Bearbeitung von benutzerinitiierten Datenschutzanfragen mit hoher Priorität zu bieten. Wir bitten Sie, die Privacy Service-API nicht für andere Zwecke zu verwenden, wie z. B. für die Datenhygiene oder das Löschen von Daten, die versehentlich über große Besuchergruppen übermittelt wurden.

Beachten Sie auch, dass jeder Besucher, der einen Treffer aufgrund einer Datenschutz-Löschanforderung gelöscht (aktualisiert oder anonymisiert) hat, seine Statusinformationen zurücksetzen lässt. Wenn der Besucher das nächste Mal auf Ihre Website zurückkehrt, wird er ein neuer Besucher sein. Jede eVar-Attribution fängt von vorn an, ebenso wie Informationen wie Besuchszahlen, Verweise, die erste besuchte Seite usw. Das Ergebnis ist in Situationen, in denen Sie Datenfelder löschen möchten, unerwünscht und verdeutlicht einen Grund, warum die Privacy Service-API für diese Verwendung ungeeignet ist.

Wenden Sie sich an Ihr Kundenbetreuungsteam, um sich mit unserem Engineering Architect-Beratungsteam abzustimmen, um weitere Überprüfungen durchzuführen und Anstrengungen zur Beseitigung von personenbezogenen Daten oder zur Lösung von Datenproblemen zu unternehmen.
