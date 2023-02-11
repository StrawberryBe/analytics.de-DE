---
title: Tracking über verschiedene Implementierungstypen hinweg
description: Verwenden Sie unterschiedliche Implementierungstypen und verfolgen Sie Besucher nahtlos zwischen ihnen.
exl-id: 18aa5595-d2a7-4df2-a4ef-a5040c097483
source-git-commit: 90914569256cf891cb3cf693843e7cf9ede2f4ce
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 18%

---

# Tracking über verschiedene Implementierungstypen hinweg

Die Hauptarchitektur einer Adobe Analytics-Implementierung ist über alle Implementierungstypen hinweg konsistent. Der Prozess umfasst die Definition von Variablen und die Kompilierung in eine Bildanforderung, die an die Datenerfassungsserver der Adobe gesendet wird. Mit diesem Konzept können Sie nahtlos zwischen AppMeasurement, dem Web SDK und den entsprechenden Erweiterungen in der Adobe Experience Platform-Datenerfassung über verschiedene Seiten derselben Site hinweg wechseln.

Adobe empfiehlt, die Konsistenz der Implementierung einer Site zu wahren, indem auf allen Seiten derselbe Implementierungstyp verwendet wird. Wenn jedoch Teile Ihrer Site unterschiedliche Anforderungen haben, können Sie diese Seite verwenden, um sicherzustellen, dass Besucher konsistent zwischen Seiten verfolgt werden.

Wenn Sie mehr als einen Implementierungstyp verwenden (z. B. AppMeasurement und fest programmierte Bildanforderungen), stellen Sie sicher, dass die folgenden Variablen richtig eingestellt sind und übereinstimmen:

| Variable | AppMeasurement | Analytics-Erweiterung | Web SDK | Web SDK-Erweiterung | Fest programmierte Bildanforderung |
| --- | --- | --- | --- | --- | --- |
| Report Suite-ID | Zeichenfolgenargument in [`s_gi`](../vars/functions/s-gi.md) | [!UICONTROL Report Suites] unter [!UICONTROL Bibliotheksverwaltung] Abschnitt, wenn [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | Hinzufügen von Adobe Analytics als Dienst, wenn [Konfigurieren eines Datastreams](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de) | Hinzufügen von Adobe Analytics als Dienst, wenn [Konfigurieren eines Datastreams](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=de) | Teil der URL `pathname` (nach `/b/ss/`) |
| Tracking-Server | Die [`trackingServer`](../vars/config-vars/trackingserver.md) und [`trackingServerSecure`](../vars/config-vars/trackingserversecure.md) variables | [!UICONTROL Tracking-Server] und [!UICONTROL SSL-Tracking-Server] unter [!UICONTROL Allgemein] Abschnitt, wenn [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html) | Die `edgeDomain` Eigenschaft, wenn [Web SDK konfigurieren](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=de) | Die [!UICONTROL Edge-Domäne] when [Konfigurieren der Erweiterung](https://experienceleague.adobe.com/docs/experience-platform/edge/extension/web-sdk-extension-configuration.html?lang=de) | Die `hostname` der Bildanforderungs-URL |
| Experience Cloud ID-Dienst | Implementierung [`VisitorAPI.js`](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=de) | Verwenden Sie die [Adobe Experience Cloud ID-Diensterweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | Verwenden Sie die [Adobe Experience Cloud ID-Diensterweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | Verwenden Sie die [Adobe Experience Cloud ID-Diensterweiterung](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/id-service/overview.html) | Erstellen Sie eine [separater Aufruf an die ID-Dienst-Server](https://experienceleague.adobe.com/docs/id-service/using/implementation/direct-integration.html) zum Abrufen der gewünschten ID |

{style=&quot;table-layout:auto&quot;}

Wenn eine dieser Variablen nicht für jeden Implementierungstyp konsistent ist, werden sie von Adobe als separate Besucher betrachtet. Wenn Besucher nicht nahtlos über Implementierungstypen auf Ihrer Site hinweg verfolgt werden, besteht der häufigste Grund darin, dass der ID-Dienst falsch konfiguriert ist. Siehe [Implementierungsmethoden](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-methods.html) im Benutzerhandbuch für den ID-Dienst für weitere Informationen.
