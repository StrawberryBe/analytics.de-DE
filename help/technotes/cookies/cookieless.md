---
title: Optionen zur Abschwächung der Auswirkungen von Browser-Cookie-Einschränkungen
description: Erfahren Sie, wie Sie die Auswirkungen von Browser-Cookie-Einschränkungen mildern und die Datenerfassung für Adobe Analytics verbessern können.
translation-type: tm+mt
source-git-commit: 07c76cea1f6fd64957fd4fd20bc5187976f3c14c
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# Optionen zur Abschwächung der Auswirkungen von Browser-Cookie-Einschränkungen

In diesem Dokument wird erläutert, wie die permanente Identifizierung von Besuchern über Eigenschaften und Lösungen hinweg erhalten werden kann, da wichtige Browser Verfolgungspräventionsmaßnahmen für Cookies implementieren.

Adobe Analytics verwendet Erstanbieter-Cookies, um die Aktivität eines Besuchers vor Ort aufzuzeichnen. Analytics nutzt auch Drittanbieter-Cookies, um die Offsite-Aktivität eines Besuchers zu verstehen, z. B. die Aktivität auf anderen Domänen, deren Inhaber Sie sind. Drittanbieter-Cookies werden auf vielen Browsern blockiert und stehen mit dem bevorstehenden Wegfall der Unterstützung durch Chrome (derzeit für 2022 geplant) weitgehend nicht zur Verfügung. Erstanbieter-Cookies sind in allen Browsern zulässig, haben aber unter den [ITP-Verfolgungsvorbeugungsmaßnahmen](https://webkit.org/tracking-prevention) von Apple einen begrenzten Ablaufzeitpunkt in Safari und anderen Browsern. Weitere Informationen zu aktuellen Einschränkungen bei Browser-Cookies finden Sie unter &quot;[Adobe Analytics- und Browser-Cookies](cookies.md).

Diese Browser-Beschränkungen spiegeln einen umfassenderen Übergang von der Verfolgung durch anonyme Drittanbieter hin zum expliziten Austausch von Informationen zwischen Benutzern und Marken, denen sie vertrauen, wider. Zur Unterstützung dieses Vorgangs bietet Adobe Kunden Möglichkeiten, herkömmliche Cookies zu ergänzen, indem sie dauerhafte IDs einbeziehen, die über ihre Erstanbieter-Beziehungen gesammelt werden.

## Customer Journey Analytics- und geräteübergreifende Analyse

[Adobe von Kunden-Journey-](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) Analytics und  [geräteübergreifenden ](/help/components/cda/overview.md) Analytics-Benutzern, um neben Cookies auch dauerhafte IDs wie Hash-Anmeldungen einzuschließen:

* **Customer Journey** Analytics ermöglicht die Kanal-übergreifende Analyse in Analysis Workspace durch eine Integration mit Adobe Experience Platform. Es konsolidiert Online- und Offline-Kundendaten, die Ihnen zur Abfrage in Experience Platform zur Verfügung stehen, mit einer beliebigen ID.

* **Bei der geräteübergreifenden** Analyse wird anhand des Adobe Experience Platform-Identitätsdienstes identifiziert, wie digitale Geräte Personen zugeordnet sind, und die Journey wird dem Benutzer über eine beliebige ID zugeordnet. Es wird entweder das Adobe Experience Cloud Device Co-op-Diagramm, ein Diagramm für ein Privatgerät oder eine feldbasierte Kontur verwendet.

## Serverseitige Datenerfassung

Die serverseitige Erfassung bietet die Flexibilität, Ihre eigenen IDs bereitzustellen, anstatt sich beim Setzen von Cookies auf Browsermechanismen zu verlassen.

Sie können serverseitige Daten mit der [Dateneinfüge-API](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) oder der [Masseneinfüge-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) in Analytics importieren. Einen Vergleich der beiden APIs finden Sie unter &quot;[Welches Adobe Analytics-Tool sollte ich verwenden](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html)&quot;.

## Weitere Informationen

Praktische Schritte, die Ihr Unternehmen zur Transition von Drittanbieter-Cookies unternehmen kann, finden Sie unter &quot;[Erwerben und halten Sie Ihre Kunden mit Adobe](https://business.adobe.com/solutions/cookieless.html) in einer Cookie-Welt,&quot;und in der Tiefe &quot;[Denken Sie über das Drittanbieter-Cookie hinaus: Ihr vollständiger Leitfaden für eine Welt ohne Drittanbieter-Cookies](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).&quot;

>[!MORELIKETHIS]
>
>[Adobe Analytics und Browsercookies](cookies.md)
