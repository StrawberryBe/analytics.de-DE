---
title: Analytics-Variablenzuordnung in Adobe Experience Edge
description: Anzeigen der XDM-Felder, die Edge automatisch Analytics-Variablen zuordnet
exl-id: fbff5c38-0f04-4780-b976-023e207023c6
source-git-commit: 8ff414efff302adfee42f192e781a8dec5c42902
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 0%

---

# Analytics-Variablenzuordnung in Adobe Experience Edge

Die folgende Tabelle zeigt die Variablen, die das Adobe Experience Platform Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese XDM-Feldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden.

| XDM-Feldpfad | Analytics-Dimension und -Beschreibung |
| --- | --- |
| `application.id` | Mobile Dimension [App-ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.isClose` | Hilft bei der Definition der Mobilmetrik [Abstürze](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.closeType` | Bestimmt, ob ein Schließen-Ereignis ein Absturz ist oder nicht. Gültige Werte sind `close` (Eine Lebenszyklussitzung endet und ein Pausenereignis für die vorherige Sitzung empfangen wurde) und `unknown` (Eine Lebenszyklussitzung endet ohne Pausenereignis). |
| `application.isInstall` | Die mobile Metrik [Installationen](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isLaunch` | Die mobile Metrik [Starts](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.name` | Hilft beim Festlegen der Mobile-Dimension [App-ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.launches.value` | Die mobile Metrik [Starts](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.isUpgrade` | Die mobile Metrik [Upgrades](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `application.version` | Hilft beim Festlegen der Mobile-Dimension [App-ID](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `application.sessionLength` | Die mobile Metrik [Gesamtsitzungslänge](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#metrics). |
| `commerce.checkouts.id` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) der [Checkouts](../../components/metrics/checkouts.md) Metrik. |
| `commerce.checkouts.value` | Erhöht die [Checkouts](../../components/metrics/checkouts.md) um den gewünschten Betrag. |
| `commerce.order.currencyCode` | Legt die [currencyCode](../vars/config-vars/currencycode.md) Konfigurationsvariable. |
| `commerce.order.purchaseID` | Legt die [purchaseID](../vars/page-vars/purchaseid.md) Seitenvariable. |
| `commerce.productListAdds.id` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) der [Zusatz zum Warenkorb](../../components/metrics/cart-additions.md) Metrik. |
| `commerce.productListAdds.value` | Erhöht die [Zusatz zum Warenkorb](../../components/metrics/cart-additions.md) um den gewünschten Betrag. |
| `commerce.productListOpens.id` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) der [Warenkorb](../../components/metrics/carts.md) Metrik. |
| `commerce.productListOpens.value` | Erhöht die [Warenkorb](../../components/metrics/carts.md) um den gewünschten Betrag. |
| `commerce.productListRemovals.id` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) der [Entnahme aus Warenkorb](../../components/metrics/cart-removals.md) Metrik. |
| `commerce.productListRemovals.value` | Erhöht die [Entnahme aus Warenkorb](../../components/metrics/cart-removals.md) um den gewünschten Betrag. |
| `commerce.productListViews.id` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) der [Warenkorbansichten](../../components/metrics/cart-views.md) Metrik. |
| `commerce.productListViews.value` | Erhöht die [Warenkorbansichten](../../components/metrics/cart-views.md) um den gewünschten Betrag. |
| `commerce.productViews.id` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) der [Produktansichten](../../components/metrics/product-views.md) Metrik. |
| `commerce.productViews.value` | Erhöht die [Produktansichten](../../components/metrics/product-views.md) um den gewünschten Betrag. |
| `commerce.purchases.value` | Erhöht die [Bestellungen](../../components/metrics/orders.md) um den gewünschten Betrag. |
| `device.manufacturer` | Der Mobilgerätehersteller. |
| `device.model` | Mobile Dimension [Gerätename](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `device.modelNumber` | Die Modellnummer des Mobilgeräts. |
| `device.colorDepth` | Hilft beim Festlegen der [Farbtiefe](../../components/dimensions/color-depth.md) Dimension. |
| `device.screenHeight` | Hilft beim Festlegen der [Bildschirmauflösung](../../components/dimensions/monitor-resolution.md) Dimension. Stellen Sie sicher, dass Sie auch das XDM-Feld festlegen `device.screenWidth`. |
| `device.screenWidth` | Hilft beim Festlegen der [Bildschirmauflösung](../../components/dimensions/monitor-resolution.md) Dimension. Stellen Sie sicher, dass Sie auch das XDM-Feld festlegen `device.screenHeight`. |
| `device.type` | Der Mobilgerätetyp. |
| `environment.browserDetails.acceptLanguage` | Hilft beim Festlegen der [Sprache](../../components/dimensions/language.md) Dimension. |
| `environment.browserDetails.cookiesEnabled` | Legt die [Cookie-Unterstützung](../../components/dimensions/cookie-support.md) Dimension. Gültige Werte sind `Y` (der Browser akzeptiert Cookies) und `N` (der Browser lehnt Cookies ab). |
| `environment.browserDetails.javaEnabled` | Legt die [Java aktiviert](../../components/dimensions/java-enabled.md) Dimension. Gültige Werte sind `Y` (Java ist aktiviert) und `N` (Java ist deaktiviert). |
| `environment.browserDetails.userAgent` | Wird als Fallback verwendet [Unique Visitor](../../components/metrics/unique-visitors.md) Identifizierungsmethode. In der Regel mit dem `User-Agent` HTTP-Anforderungsheader. Sie können dieses Feld einer eVar zuordnen, wenn Sie es in Berichten verwenden möchten. |
| `environment.browserDetails.viewportHeight` | Legt die [Browserhöhe](../../components/dimensions/browser-height.md) Dimension. |
| `environment.browserDetails.viewportWidth` | Legt die [Browserbreite](../../components/dimensions/browser-width.md) Dimension. |
| `environment.carrier` | Mobile Dimension [Betreibername](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.connectionType` | Hilft beim Festlegen der [Verbindungstyp](../../components/dimensions/connection-type.md) Dimension. |
| `environment.ipV4` | Wird als Fallback verwendet [Unique Visitor](../../components/metrics/unique-visitors.md) Identifizierungsmethode. In der Regel mit dem `X-Forwarded-For` HTTP-Header. |
| `environment.language` | Die mobile Dimension Gebietsschema. |
| `environment.operatingSystem` | Mobile Dimension [Betriebssystem](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.operatingSystemVersion` | Mobile Dimension [Betriebssystemversion](https://experienceleague.adobe.com/docs/mobile-services/using/get-started-ug/mobile-metrics/metrics-reference.html#dimensions). |
| `environment.type` | Gibt an, ob das Ereignis von einer [Wearable](https://experienceleague.adobe.com/docs/mobile-services/android/wearables-android/c-android-wearables--additional-notes.html) Gerät. Gültige Werte sind `Application` (Das Ereignis stammt aus der App), `Extension` (das Ereignis stammt von der Wearable App) oder `Widget` (Das Ereignis stammt von einem mobilen Widget). |
| `_experience.analytics.customDimensions.eVars.eVar1` -<br/>`_experience.analytics.customDimensions.eVars.eVar250` | Legt die entsprechenden fest [eVar](../../components/dimensions/evar.md) Dimension. |
| `_experience.analytics.customDimensions.listProps.prop1.delimiter` -<br/>`_experience.analytics.customDimensions.listProps.prop75.delimiter` | Das für eine bestimmte [Listen-Prop](../vars/page-vars/prop.md#list-props). |
| `_experience.analytics.customDimensions.listProps.prop1.values` -<br/>`_experience.analytics.customDimensions.listProps.prop75.values` | Ein Zeichenfolgen-Array, das die entsprechenden [Listen-Prop](../vars/page-vars/prop.md#list-props) -Werte. |
| `_experience.analytics.customDimensions.lists.list1.list` -<br/>`_experience.analytics.customDimensions.lists.list3.list` | Legt die entsprechenden fest [Listenvariable](../vars/page-vars/list.md). |
| `_experience.analytics.customDimensions.props.prop1` -<br/>`_experience.analytics.customDimensions.props.prop75` | Legt die entsprechenden fest [Prop](../../components/dimensions/prop.md) Dimension. |
| `_experience.analytics.event1to100.event1.id` -<br/>`_experience.analytics.event901to1000.event1000.value` | Gilt [Ereignis-Serialisierung](../vars/page-vars/events/event-serialization.md) an die jeweiligen [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md) Metrik. |
| `_experience.analytics.event1to100.event1.value` -<br/>`_experience.analytics.event901to1000.event1000.value` | Erhöht die jeweilige [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md) um den gewünschten Betrag. |
| `identityMap.ECID[0].id` | Die [Adobe Experience Cloud Identity-Dienst-ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de). |
| `marketing.trackingCode` | Legt die [Trackingcode](../../components/dimensions/tracking-code.md) Dimension. |
| `media.mediaTimed.completes.value` | Die Media Analytics-Metrik [Inhaltsbeendigung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-complete). |
| `media.mediaTimed.dropBeforeStart.value` | `c.a.media.view`, `c.a.media.timePlayed`, `c.a.media.play` |
| `media.mediaTimed.federated.value` | Die Media Analytics-Metrik [Federated Data](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#federated-data). |
| `media.mediaTimed.firstQuartiles.value` | Die Media Analytics-Metrik [25 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#twenty-five-progress-marker). |
| `media.mediaTimed.mediaSegmentView.value` | Die Media Analytics-Metrik [Ansichten des Inhaltssegments](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment-views). |
| `media.mediaTimed.midpoints.value` | Die Media Analytics-Metrik [50 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#fifty-progress-marker). |
| `media.mediaTimed.pauseTime.value` | Die Media Analytics-Metrik [Pausierung - Gesamtdauer](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#total-pause-duration). |
| `media.mediaTimed.pauses.value` | Die Media Analytics-Metrik [Pausierung - Ereignisse](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#pause-events). |
| `media.mediaTimed.primaryAssetReference.`<br/>`@id` | Die Dimension &quot;Media Analytics&quot; [Asset-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#asset-id). |
| `media.mediaTimed.primaryAssetReference.`<br/>`dc:title` | Die Dimension &quot;Media Analytics&quot; [Videoname](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-name). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Creator[N].iptc4xmpExt:Name` | Die Dimension &quot;Media Analytics&quot; [Urheber](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#originator). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Episode.iptc4xmpExt:Number` | Die Dimension &quot;Media Analytics&quot; [Folge](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#episode). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Genre` | Die Dimension &quot;Media Analytics&quot; [Genre](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#genre). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Rating[N].iptc4xmpExt:RatingValue` | Die Dimension &quot;Media Analytics&quot; [Inhaltsbewertung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-rating). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Season.iptc4xmpExt:Number` | Die Dimension &quot;Media Analytics&quot; [Staffel](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#season). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Identifier` | Die Dimension &quot;Media Analytics&quot; [Inhalts-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-id). |
| `media.mediaTimed.primaryAssetReference.`<br/>`iptc4xmpExt:Series.iptc4xmpExt:Name` | Die Dimension &quot;Media Analytics&quot; [Anzeigen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show). |
| `media.mediaTimed.primaryAssetReference.`<br/>`showType` | Die Dimension &quot;Media Analytics&quot; [Sendungstyp](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#show-type). |
| `media.mediaTimed.primaryAssetReference.`<br/>`xmpDM:duration` | Die Dimension &quot;Media Analytics&quot; [Videolänge](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#video-length). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`@id` | Die Dimension &quot;Media Analytics&quot; [Mediensitzungs-ID](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-session-id). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastChannel` | Die Dimension &quot;Media Analytics&quot; [Inhaltskanal](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-channel). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastContentType` | Die Dimension &quot;Media Analytics&quot; [Content-Typ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-type). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`broadcastNetwork` | Die Dimension &quot;Media Analytics&quot; [Netzwerk](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#network). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`mediaSegmentView.value` | Die Dimension &quot;Media Analytics&quot; [Inhaltssegment](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-segment). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`playerName` | Die Dimension &quot;Media Analytics&quot; [Inhalts-Player-Name](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-player-name). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`playerSDKVersion.version` | Die Dimension &quot;Media Analytics&quot; [SDK-Version](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#sdk-version). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`sourceFeed` | Die Dimension &quot;Media Analytics&quot; [Medien-Feed-Typ](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-feed-type). |
| `media.mediaTimed.primaryAssetViewDetails.`<br/>`streamFormat` | Die Dimension &quot;Media Analytics&quot; [Stream-Format](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#stream-format). |
| `media.mediaTimed.progress10.value` | Die Media Analytics-Metrik [10 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ten-progress-marker). |
| `media.mediaTimed.progress95.value` | Die Media Analytics-Metrik [95 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#ninety-five-progress-marker). |
| `media.mediaTimed.resumes.value` | Die Media Analytics-Metrik [Inhaltswiederaufnahmen](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-resumes). |
| `media.mediaTimed.starts.value` | Die Media Analytics-Metrik [Medienstarts](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-starts). |
| `media.mediaTimed.thirdQuartiles.value` | Die Media Analytics-Metrik [75 % Fortschrittsmarkierung](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#seventy-five-progress-marker). |
| `media.mediaTimed.timePlayed.value` | Die Media Analytics-Metrik [Besuchszeit für Inhalt](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#content-time-spent). |
| `media.mediaTimed.totalTimePlayed.value` | Die Media Analytics-Metrik [Besuchszeit für Medien](https://experienceleague.adobe.com/docs/media-analytics/using/metrics-and-metadata/audio-video-parameters.html#media-time-spent). |
| `placeContext.geo.latitude` | Die Mobilgerätedimension Latitude. |
| `placeContext.geo.longitude` | Die Länge der Mobile-Dimension. |
| `placeContext.geo.postalCode` | Die [Postleitzahl](../../components/dimensions/zip-code.md) Dimension. |
| `placeContext.geo.stateProvince` | Die [US-Staaten](../../components/dimensions/us-states.md) Dimension. |
| `productListItems[].lineItemId` | Die [Kategorie](../../components/dimensions/category.md) Dimension. |
| `productListItems[].name` | Die [Produkt](../../components/dimensions/product.md) Dimension. |
| `productListItems[].priceTotal` | Hilft bei der Bestimmung der [Umsatz](../../components/metrics/revenue.md) Metrik. |
| `productListItems[].quantity` | Hilft bei der Bestimmung der [Einheiten](../../components/metrics/units.md) Metrik. |
| `web.webInteraction.URL` | Die [linkURL](../vars/config-vars/linkurl.md) Implementierungsvariable. |
| `web.webInteraction.name` | Die [Benutzerspezifischer Link](../../components/dimensions/custom-link.md), [Downloadlink](../../components/dimensions/download-link.md)oder [Exitlink](../../components/dimensions/exit-link.md) Dimension, abhängig vom Wert in `web.webInteraction.type` |
| `web.webInteraction.type` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `other` (Benutzerspezifische Links), `download` (Downloadlinks) und `exit` (Exitlinks). |
| `web.webPageDetails.URL` | Die [Seiten-URL](../../components/dimensions/page-url.md) Dimension. |
| `web.webPageDetails.errorPage` | Flag, das bei der Bestimmung von &quot;Seiten nicht gefunden&quot;hilft [Dimension](../../components/dimensions/pages-not-found.md) und [Metrik](../../components/metrics/pages-not-found.md). |
| `web.webPageDetails.name` | Die [Seite](../../components/dimensions/page.md) Dimension. |
| `web.webPageDetails.server` | Die [Server](../../components/dimensions/server.md) Dimension. |
| `web.webPageDetails.siteSection` | Die [Sitebereich](../../components/dimensions/site-section.md) Dimension. |
| `web.webReferrer.URL` | Die [Referrer](../../components/dimensions/referrer.md) Dimension. |

{style=&quot;table-layout:auto&quot;}

<!-- `environment.browserDetails.javaScriptVersion` and `web.webPageDetails.homePage` were included in the original table, but they no longer exist in Analytics. | -->

## Zuordnen anderer XDM-Felder zu Analytics-Variablen

Wenn es Dimensionen oder Metriken gibt, die Sie zu Adobe Analytics hinzufügen möchten, können Sie dies über [Kontextdatenvariablen](../vars/page-vars/contextdata.md). Alle XDM-Feldelemente werden als Kontextdaten mit dem Präfix an Adobe Analytics gesendet `a.x`. Sie können diese Kontextdatenvariable dann der gewünschten Analytics-Variablen zuordnen, indem Sie [Verarbeitungsregeln](../../admin/admin/c-processing-rules/processing-rules.md). Wenn Sie beispielsweise das folgende Ereignis senden:

```js
alloy("event",{
    "xdm":{
        "_atag":{
            "search":{
                "term":"Example search term"
            }
        }
    }
})
```

Das Web SDK sendet diese Daten als Kontextdatenvariable an Adobe Analytics `a.x._atag.search.term`. Anschließend können Sie eine Verarbeitungsregel verwenden, um diesen Wert der Kontextdatenvariablen der gewünschten Analytics-Variablen zuzuweisen, z. B. einer eVar:

![Suchbegriff-Verarbeitungsregel](assets/examplerule.png)
