---
title: Regionale Datenerfassung für China
seo-title: Adobe Analytics China RDC
description: null
seo-description: null
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Regionale Datenerfassung für China

Die Regionale Datenerfassung (RDC) von Adobe auf dem chinesischen Festland ermöglicht es Kunden innerhalb Chinas, Daten direkt an ein Data Collection Center (DCC) in China zu senden statt an andere Standorte weltweit. Dies verbessert die Seitenladezeiten und die Datengenauigkeit gegenüber dem Versand der Daten an DCCs außerhalb Chinas.

> [!IMPORTANT] Mit der Verwendung des China RDC-Knotens sind zusätzliche Kosten verbunden. Bevor Sie die Datenerfassung in China mithilfe des RDC-Knotens implementieren, der in diesem Dokument beschrieben ist, wenden Sie sich an den Kundenbetreuer Ihrer Organisation, um sicherzustellen, dass Sie ordnungsgemäß zu dieser Funktion berechtigt sind.

## Einstellen des Tracking-Servers für China

Das Tracking im Rahmen von China RDC kann an einem beliebigen Ort durchgeführt werden, der für Ihren Service geeignet ist. Für jede digitale Eigenschaft (z. B. eine mobile App oder Webseite) möchten Sie China RDC weiterleiten und den Tracking-Server in

`<namespace>.sc.adobedc.cn`

Achten Sie darauf, den richtigen Namespace einzufügen. Dieser befindet sich typischerweise am Anfang Ihres bestehenden Tracking-Servers. For example: `<namespace>.sc.adobedc.cn` - although any namespace value will work. Sie können auch einen Nicht-SSL-First-Party [CNAME](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_cname.html)-Eintrag auf diesen neuen Ort verweisen.

Setzen Sie Ihren trackingserver-Wert nicht global für alle Eigenschaften und Regionen auf China RDC, wenn ein erheblicher Teil Ihrer Kundenbasis außerhalb von China liegt. Der trackingServer sollte nur für Kunden, die sich in China befinden, auf den China RDC-Wert eingestellt werden. Andernfalls wird sich dies negativ auf die Geschwindigkeit für Ihre Benutzer außerhalb Chinas auswirken, da die Datenerfassung gezwungen ist, nach China und zurück zu wechseln, um eine Antwort zu erhalten.

## Identifizieren von Benutzern in China

Unabhängig davon, wo Ihre digitale Eigenschaft gehostet wird oder welche Sprache sie verwendet, werden Ihre Benutzer in China Verbesserungen erfahren, wenn Sie den RDC-Knoten in China verwenden. Deshalb wird empfohlen, die Benutzer zu ermitteln, die sich in China befinden, und dann für diese Benutzer China RDC zu verwenden. Folgende Methoden können Ihnen bei der Identifizierung dieser Benutzer helfen:

* Verwenden einer zuverlässigen geoip-Lösung. Sie können eine serverseitige Lösung verwenden, um einfach mit dem Adobe Experience Platform Launch (oder dem Data Tag-Management) zu integrieren. In diesem Fall kann der Speicherort durch ein Standarddatenelement im Experience Platform Start- oder DTM-Objekt bestimmt werden. Oder Sie verwenden eine clientseitige GeoIP-Lösung. In diesem Fall kann der Experience Platform Launch in den clientseitigen Code aufgenommen werden. Beachten Sie, dass solche Lösungen dazu führen können, dass der Benutzer aufgefordert wird, zur lokalisierten Website zu navigieren. Dies birgt das Risiko, dass die erste Seite vom globalen Tracking-Server und der zweiten Seite in China gezählt wird, was zu einem doppelgezählten Besuch führen kann. Befolgen Sie die Best Practices für GeoIP-Lösungen. Adobe ist nicht für die Genauigkeit der von Ihnen verwendeten GeoIP-Lösung verantwortlich.

* Using site structure or the browser language (the `navigator.language / accept-language` header). Der Vorteil dieser Methode liegt in niedrigeren Kosten und einer möglicherweise besseren Leistung. Der Nachteil dieser Methode liegt darin, dass chinesischsprachige Besucher, wenn sie außerhalb Chinas unterwegs sind, einer negativ beeinflussten Geschwindigkeit ausgesetzt sind.
* Verwenden einer in China ansässigen Hosting-Lösung und Festlegen des trackingserver auf China RDC basierend auf Ihrem Host. Dadurch wird die Geschwindigkeit ebenfalls erheblich erhöht.

## Aktuelle Einschränkungen

Die aktuellen Einschränkungen von China RDC:

1. China RDC does not support first party SSL ([s.trackingServerSecure](https://helpx.adobe.com/analytics/kb/determining-data-center.html) in your JavaScript), or [Server-Side Forwarding](https://marketing.adobe.com/resources/help/en_US/reference/ssf.html) to Adobe Audience Manager.
2. Obwohl [A4T](https://marketing.adobe.com/resources/help/en_US/target/a4t/a4t.html) und [ECID](https://marketing.adobe.com/resources/help/en_US/mcvid/) unterstützt werden, befinden sich die Target- und Demdex-Domänen derzeit nicht auf dem chinesischen Festland und werden nicht die gleichen Geschwindigkeits- oder Zuverlässigkeitsvorteile haben wie die innerhalb von China RDC.

## Das Engagement von Adobe in China

Adobe plant, China RDC dauerhaft weiterzuentwickeln und wird schließlich Funktionen wie First-Party-SSL und serverseitige Weiterleitung unterstützen. Darüber hinaus plant Adobe, eine Demdex-Domäne (oder eine gleichwertige Domäne) in China bereitzustellen, um die Erfassung von ECID und Audience Manager aus China vollständig zu unterstützen. Kunden, die mit der Nutzung von Adobe China RDC beginnen, können diesen Endpunkt der Datenerfassung auf unbestimmte Zeit weiter nutzen.
