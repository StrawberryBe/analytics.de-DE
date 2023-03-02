---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: 90914569256cf891cb3cf693843e7cf9ede2f4ce
workflow-type: ht
source-wordcount: '442'
ht-degree: 100%

---

# Tracking über verschiedene Implementierungstypen hinweg

Die Hauptarchitektur einer Adobe Analytics-Implementierung ist über alle Implementierungstypen hinweg konsistent. Der Prozess umfasst die Definition von Variablen und die Kompilierung in eine Bildanforderung, die an die Datenerfassungs-Server von Adobe gesendet wird. Mit diesem Konzept können Sie nahtlos zwischen AppMeasurement, dem Web SDK und den entsprechenden Erweiterungen in der Adobe Experience Platform-Datenerfassung über verschiedene Seiten derselben Site hinweg wechseln.

Adobe empfiehlt, die Konsistenz der Implementierung einer Site zu wahren, indem auf allen Seiten derselbe Implementierungstyp verwendet wird. Wenn jedoch Teile Ihrer Site unterschiedliche Anforderungen haben, können Sie diese Seite verwenden, um sicherzustellen, dass Besucherinnen und Besucher konsistent zwischen Seiten verfolgt werden.

Beim Einsatz mehrerer Typen von Implementierungen (wie JavaScript und fest codierte Bildanfragen) müssen Sie sicherstellen, dass die folgenden Variablen angegeben sind und miteinander übereinstimmen:

| Variable | AppMeasurement | Analytics-Erweiterung | Web SDK | Web SDK-Erweiterung | Fest programmierte Bildanforderung |
| --- | --- | --- | --- | --- | --- |
| Report Suite-ID | Zeichenfolgenargument in [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL Report Suites] im Abschnitt [!UICONTROL Bibliotheksverwaltung] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de) | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de) | Hinzufügen von Adobe Analytics als Dienst beim [Konfigurieren eines Datenstroms](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de) | Teil des `pathname` der URL (nach `/b/ss/`) |
| Tracking-Server | Die Variablen [`trackingServer`](../vars/config-vars/trackingserver.md) und [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) | [!UICONTROL Tracking-Server] und [!UICONTROL SSL-Tracking-Server] im Abschnitt [!UICONTROL Allgemein] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html?lang=de) | Die Eigenschaft `edgeDomain` beim [Konfigurieren des Web-SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) | Die [!UICONTROL Edge-Domain] beim [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=de) | Der `hostname` der Bildanfrage-URL |
| ID-Service von Experience Cloud | Implementierung von [`VisitorAPI.js`](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=de) | Verwenden der [Adobe Experience Cloud ID-Service-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=de) | Verwenden der [Adobe Experience Cloud ID-Service-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=de) | Verwenden der [Adobe Experience Cloud ID-Service-Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/id-service/overview.html?lang=de) | Erstellen Sie einen [separaten Aufruf an die ID-Service-Server](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html?lang=de), um die gewünschte ID zu erhalten |

{style=&quot;table-layout:auto&quot;}

Wenn eine dieser Variablen nicht für jeden Implementierungstyp konsistent ist, werden sie von Adobe als separate Besucherinnen und Besucher betrachtet. Wenn Besucherinnen und Besucher nicht nahtlos über Implementierungstypen auf Ihrer Site hinweg verfolgt werden, besteht der häufigste Grund darin, dass der ID-Service falsch konfiguriert ist. Siehe [Implementierungsmethoden](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-methods.html?lang=de) im Benutzerhandbuch für den ID-Service, um weitere Informationen zu erhalten.
