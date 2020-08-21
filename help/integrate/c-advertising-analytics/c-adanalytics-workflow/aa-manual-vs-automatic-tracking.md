---
description: Tracking bestimmt, wie Suchmaschinendaten von Ihrer Adobe Analytics-Implementierung verfolgt werden. Dieser Schritt ist erforderlich, um die Adobe Analytics-Daten ordnungsgemäß mit den Suchmaschinendaten zu ergänzen.
title: 'Tracking: Manueller Modus und Auto-Modus'
translation-type: tm+mt
source-git-commit: 69db61bdfd9375df4d090add7d8ed08135d1f087
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 100%

---


# Tracking: Manueller Modus und Auto-Modus

Tracking bestimmt, wie Suchmaschinendaten von Ihrer Adobe Analytics-Implementierung verfolgt werden. Dieser Schritt ist erforderlich, um die Adobe Analytics-Daten ordnungsgemäß mit den Suchmaschinendaten zu ergänzen.

Zwei Trackingmodi werden unterstützt: Auto-Modus und Manueller Modus.

## Tracking im Auto-Modus {#concept_C4C6107838C947CFBB7F4E0CB94264F0}

Im Auto-Modus entscheidet die Advertising Cloud-Engine, wie die Suchmaschinendaten verarbeitet werden sollen. Dies ist der einfachere Ansatz, der jedoch möglicherweise nicht zum besten integrierten Datensatz führt.

Daher müssen Sie ein Kontrollkästchen zur Bestätigung aktivieren, wenn Sie den Auto-Modus aktivieren, bevor Sie die Kontoeinstellungen speichern können.

Beachten Sie, dass Sie für die folgenden Aktionen verantwortlich sind, wenn Sie ein Suchmaschinenkonto im „Auto-Modus“ konfigurieren möchten:

* Der Parameter `s_kwcid` und der Wert werden den Konto-Tracking-Vorlagen oder Landingpage-URLs in dem hinzugefügten Konto hinzugefügt. Die Einfügung erfolgt am Ende der URL. Zusätzliche Maßnahmen können von Ihrer Seite erforderlich sein, wenn Ihr Webserver ein bestimmtes „key=value“-Paar am Ende der URL ODER ein Update zur Unterstützung eines neuen „key=value“-Paares in der URL erfordert. **Sie müssen sicherstellen, dass die hinzugefügten URL-Parameter ordnungsgemäß und persistent auf die richtige Landingpage verweisen.**
* Darüber hinaus können Keywords als Teil des Wertes `s_kwcid` in die Landingpage-URL eingefügt werden. Wenn sie Sonderzeichen oder Symbole enthalten, überprüfen Sie bitte, ob Ihr Webserver diese Zeichen unterstützen kann. Beispiel: Ein häufig verwendetes Sonderzeichen ist „+“, das in „Broad Match Modified“-Keywords verwendet wird.

>[!IMPORTANT]
>
>Erfahren Sie mehr darüber, ob Sie den Parameter `s_kwcid` zu Ihrer [Richtlinie zur Inhaltssicherheit](https://docs.adobe.com/content/help/de-DE/id-service/using/reference/csp.html) hinzufügen sollten.

## Tracking im Manuellen Modus {#concept_87B28BA9E7F84BA5972F69E6F3482A33}

Im manuellen Modus müssen Sie angeben, wie die Suchmaschinendaten vom Advertising Analytics-Integrationsprozess verarbeitet werden sollen.

### Manuelles Tracking zu Google-Konto hinzufügen {#section_41C1EB1AEB034544A5BC291F53C05C67}

Weiter unten finden Sie die Zeichenfolge, die zu Ihrem Google-Konto hinzugefügt werden muss. Sie müssen die Zeichenfolge zu allen Tracking-Vorlagen hinzufügen, die innerhalb Ihres Kontos verwendet werden.

>[!IMPORTANT]
>
>Der Wert `<Advertising Analytics ID>` (unten in **Fettschrift**) ist nur ein allgemeiner Wert, den Sie **durch Ihre Konto-ID-Zeichenfolge ersetzen** müssen. Sie können Ihre Konto-ID-Zeichenfolge über den Bildschirm zur Kontoeinrichtung im Abschnitt „Tracking“ ermitteln.

**Tracking-Zeichenfolge für Kampagnen:**

```
s_kwcid=AL! 
<b><Advertising Analytics ID></b>!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

![](assets/Google.png)

Beispiele für Trackingcodes in verschiedenen Tracking-Vorlagenformaten:

**`{lpurl}`**

```
{lpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**`{lpurl}`mit zusätzlichem URL-Parameter**

```
{lpurl}?campaign=PPC&s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**Drittanbieter (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

**Drittanbieter (DoubleClick)`{lpurl}`**

Wenn die URL eine Umleitung durchläuft und nicht den Wert „unescapedlurl“ enthält, müssen Sie die Zeichenfolge oft genug codieren, damit sie auch nach der Umleitung persistent auf die finale Landingpage-URL verweist.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

### Manuelles Tracking zu Bing-Konto hinzufügen {#section_094F8ACA493C4D65B1F54A695558EBF2}

Weiter unten finden Sie die Zeichenfolge, die zu Ihrem Bing-Konto hinzugefügt werden muss. Sie müssen die Zeichenfolge zu allen finalen URL-Suffixen hinzufügen, die innerhalb Ihres Kontos verwendet werden.

>[!IMPORTANT]
>
>Der Wert `<Advertising Analytics ID>` (unten in **Fettschrift**) ist nur ein allgemeiner Wert, den Sie **durch Ihre Konto-ID-Zeichenfolge ersetzen** müssen. Sie können Ihre Konto-ID-Zeichenfolge über den Bildschirm zur Kontoeinrichtung im Abschnitt „Tracking“ ermitteln.

**Tracking-Zeichenfolge für Kampagnen:**

```
s_kwcid=AL!<Advertising Analytics ID>!10!{AdId}!{OrderItemId} 
```

![](assets/Bing.png)

Beispiele für Trackingcodes in verschiedenen finalen URL-Suffix-Formaten:

**{lpurl}**

```
{lpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**`{lpurl}`mit zusätzlichem URL-Parameter**

```
{lpurl}?campaign=PPC&
s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**Drittanbieter (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**Drittanbieter (DoubleClick)`{lpurl}`**

Wenn die URL eine Umleitung durchläuft und nicht den Wert „unescapedlurl“ enthält, müssen Sie die Zeichenfolge oft genug codieren, damit sie auch nach der Umleitung persistent auf die finale Landingpage-URL verweist.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!10!{AdId}!{OrderItemId}
```
