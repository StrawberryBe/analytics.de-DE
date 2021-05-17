---
title: Optionen zur Abschwächung der Auswirkungen von Browser-Cookie-Einschränkungen
description: Erfahren Sie, wie Sie die Auswirkungen von Browser-Cookie-Einschränkungen mildern und die Datenerfassung für Adobe Analytics verbessern können.
source-git-commit: 6c354a343648162ce2951c52a70a688970e1304d
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 5%

---


# Optionen zur Abschwächung der Auswirkungen von Browser-Cookie-Einschränkungen

In diesem Dokument werden Optionen zur Beibehaltung der Identifikation beständiger Besucher über Eigenschaften und Lösungen hinweg diskutiert, da wichtige Browser Verfolgungspräventionsmaßnahmen für Cookies implementieren.

Adobe Analytics verwendet Erstanbieter-Cookies, um die Aktivität eines Besuchers vor Ort aufzuzeichnen. Analytics nutzt auch Drittanbieter-Cookies, um die Offsite-Aktivität eines Besuchers zu verstehen, z. B. die Aktivität auf anderen Domänen, deren Inhaber Sie sind. Drittanbieter-Cookies werden auf vielen Browsern blockiert und stehen mit dem bevorstehenden Wegfall der Unterstützung durch Chrome (derzeit für 2022 geplant) weitgehend nicht zur Verfügung. Erstanbieter-Cookies sind in allen Browsern zulässig, haben aber unter den [ITP-Verfolgungsvorbeugungsmaßnahmen](https://webkit.org/tracking-prevention) von Apple einen begrenzten Ablaufzeitpunkt in Safari und anderen Browsern. Weitere Informationen zu aktuellen Einschränkungen bei Browser-Cookies finden Sie unter [Adobe Analytics- und Browser-Cookies](cookies.md).

Diese Browser-Beschränkungen spiegeln einen umfassenderen Übergang von der Verfolgung durch anonyme Drittanbieter hin zum expliziten Austausch von Informationen zwischen Benutzern und Marken, denen sie vertrauen, wider. Zur Unterstützung dieses Vorgangs bietet Adobe Kunden Möglichkeiten, herkömmliche Cookies zu ergänzen, indem sie dauerhafte IDs einbeziehen, die über ihre Erstanbieter-Beziehungen gesammelt werden.

## Customer Journey Analytics- und geräteübergreifende Analyse

[Adobe von Kunden-Journey ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) Analytics und  [geräteübergreifenden ](/help/components/cda/overview.md) Analytics-Benutzern, um neben Cookies auch dauerhafte IDs wie Hash-Anmeldungen einzuschließen. Auf diese Weise können Sie die Journey der Kunden geräteübergreifend und im Customer Journey Analytics auch über Online- und Offline-Kanal hinweg nachvollziehen:

* **Kundenanalysen** basieren auf Adobe Experience Platform und bieten die Flexibilität, Online- und Offlinedaten in Analysis Workspace auf der Grundlage beliebiger Kunden-IDs zu kombinieren. Sie können angeben, welche ID Sie für eine beliebige Analyse verwenden möchten, und die Daten in Analysis Workspace untersuchen. Analytics Select-, Prime- und Ultimate-Kunden können dieses Produkt als Zusatzprodukt erwerben.

* **Geräteübergreifende** Analyse ist eine Erweiterung des herkömmlichen Adobe Analytics, mit der Kunden alternative IDs für Besucher verwenden können. Mit dieser Funktion können Sie von einer geräteorientierten Ansicht zu einer personenzentrierten Ansicht wechseln. Geräteübergreifende Analysen sind für Analytics Ultimate-Kunden verfügbar.

## Serverseitige Datenerfassung

Die serverseitige Erfassung bietet die Flexibilität, Ihre eigenen IDs bereitzustellen, anstatt sich beim Setzen von Cookies auf Browsermechanismen zu verlassen.

Sie können Daten entweder mit der [Dateneinfüge-API](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) oder mit der [Masseneinfüge-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md) an die Analytics-Serverseite senden. Die Bulk Data Insertion API wird für neue serverseitige Implementierungen empfohlen. Einen Vergleich der beiden APIs finden Sie unter &quot;[Welches Adobe Analytics-Tool sollte ich verwenden](https://experienceleague.adobe.com/docs/analytics/admin/admin-overview/which-analytics-tool.html)&quot;.

## Weitere Informationen

Praktische Schritte, die Ihr Unternehmen zur Transition von Drittanbieter-Cookies unternehmen kann, finden Sie unter [Erwerben und halten Sie Kunden mit Adobe](https://business.adobe.com/solutions/cookieless.html) und der Tiefe [Denken Sie über das Drittanbieter-Cookie hinaus in einer Cookie-Welt: Ihr vollständiger Leitfaden für eine Welt ohne Drittanbieter-Cookies](https://business.adobe.com/content/dam/www/us/en/pdfs/Adobe_Thinking_Beyond_the_Third_Party_Cookie.pdf).&quot;

>[!MORELIKETHIS]
[Adobe Analytics und Browsercookies](cookies.md)>
>
