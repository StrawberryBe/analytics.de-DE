---
description: Sie können Links voneinander abgrenzen, indem Sie die Link-ID mithilfe der Variablen s_objectID, die Region oder die Activity Map-Moduldatei AppMeasurement anpassen.
title: Links mit Verweis auf dieselbe Link-ID und Region unterscheiden
uuid: f2da0cda-a33b-4a12-8d99-1f58386d6d30
feature: Activity Map
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: f9d9c7dbaf5fde5bd51c929d927d4cd3f61cb63b
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 61%

---


# Links mit Verweis auf dieselbe Link-ID und Region unterscheiden

Sie können Links voneinander abgrenzen, indem Sie die Link-ID mithilfe der Variablen s_objectID, die Region oder die Activity Map-Moduldatei AppMeasurement anpassen.

Beispiel: Angenommen, Sie haben mehrere Links des Typs „Buy“, die von Activity Map unter der gleichen Link-ID und Region identifiziert werden:

<table id="table_3020E2C0175D455C84E794CF51BE5A93">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Code-Beispiel </th>
   <th colname="col2" class="entry"> Link-ID </th>
   <th colname="col3" class="entry"> Region </th>
  </tr>
 </thead>
  <tbody>
  <tr>
   <td colname="col1">
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td>
   <td colname="col2">
     <br/>
     <br/>
    Kaufen<br/>
     <br/>
     <br/>
    Kaufen<br/>
     <br/>
     <br/>
    Kaufen<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    Empfehlungsbereich<br/>
     <br/>
     <br/>
    Empfehlungsbedienfeld<br/>
     <br/>
     <br/>
    Empfehlungsbereich<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

Wie können Sie Ihre Webseite und das Tagging anpassen, um die Werte dieser Links zu unterscheiden? Sie haben drei Optionen: Sie können die Link-ID anpassen, die Region anpassen oder die Activity Map-Moduldatei AppMeasurement anpassen.

## Link-ID mit s_objectID anpassen  {#section_01B0D463397B4837B2D46F087A6E5937}

Durch Erstellen einer eindeutigen Objekt-ID (`s_objectID`) für einen Link oder eine Link-Position auf einer Seite können Sie die Activity Map-Verfolgung verbessern oder Activity Map verwenden, um einen Link-Typ oder eine Link-Position zu melden, anstatt die Link-URL. Klicken Sie [hier](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/page-vars/page-variables.html), um weitere Informationen zur Variablen zu erhalten.`s_objectID`

>[!IMPORTANT]
>
>Beachten Sie, dass ein nachfolgender Semikolon (`;`) erforderlich ist, wenn `s_objectID` in Activity Map verwendet wird.
<table id="table_9439A5F320304E439A19842CF3EBA456">
 <thead>
  <tr>
   <th colname="col02" class="entry"> Code-Beispiel </th>
   <th colname="col2" class="entry"> Link-ID </th>
   <th colname="col3" class="entry"> Region </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col02">
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product1';"&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&gt; </code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product2';"&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt; </code><br/>
    <code>&nbsp;&lt;div&gt; </code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;onClick="s_objectID='Product3';"&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td> 
   <td colname="col2">
     <br/>
     <br/>
    Produkt1<br/>
     <br/>
     <br/>
    Produkt2<br/>
     <br/>
     <br/>
    Produkt3<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    Empfehlungsbereich<br/>
     <br/>
     <br/>
    Empfehlungsbedienfeld<br/>
     <br/>
     <br/>
    Empfehlungsbereich<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

## Region anpassen   {#section_6B1EF302573B445DBAF44176D0A12DB9}

Sie können die Region anpassen, indem Sie sicherstellen, dass für jeden Link &quot;Kaufen&quot;eine eigene Region definiert ist. Fügen Sie dazu einen Parameter `"id"` zu einem der übergeordneten Elemente jedes Verankerungs-Tags &quot;Buy&quot;hinzu.

>[!NOTE]
>Sie sind nicht streng auf den Parameter `"id"` als Regionsbezeichner beschränkt. Sie können Ihre eigene ID auch mit der JavaScript-Variablen `"s.ActivityMap.regionIDAttribute"` festlegen.
>
>
><table id="table_250DB52A869C466B942517BABA1C287B">
 <thead>
  <tr>
   <th colname="col02" class="entry"> Code-Beispiel </th>
   <th colname="col2" class="entry"> Link-ID </th>
   <th colname="col3" class="entry"> Region </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col02">
    <code>&lt;div&nbsp;id="recommendation&nbsp;panel"&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;a"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product1.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;b"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product2.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;div&nbsp;id="region&nbsp;c"&gt;</code><br/>
    <code>&nbsp;&nbsp;&nbsp;&nbsp;&lt;a&nbsp;href="product3.html"&gt;Buy&lt;/a&gt;</code><br/>
    <code>&nbsp;&nbsp;&lt;/div&gt;</code><br/>
    <code>&lt;/div&gt;</code>
   </td> 
   <td colname="col2">
     <br/>
     <br/>
    Kaufen<br/>
     <br/>
     <br/>
    Kaufen<br/>
     <br/>
     <br/>
    Kaufen<br/>
     <br/>
     <br/>
   </td> 
   <td colname="col3">
     <br/>
     <br/>
    region a<br/>
     <br/>
     <br/>
    region b<br/>
     <br/>
     <br/>
    region c<br/>
     <br/>
     <br/>
   </td>
  </tr>
 </tbody>
</table>

## Activity Map-Moduldatei AppMeasurement anpassen   {#section_B933BB9F944E4D5389002908A5A881F8}

>[!CAUTION]
Sie sollten den geänderten Code unbedingt testen, um sicherzustellen, dass er ordnungsgemäß funktioniert. Adobe übernimmt keine Verantwortung für das Verhalten des geänderten Codes.

Im Folgenden finden Sie einige Beispiele für **allgemeine** Link-/Regionsfunktionen, die Sie (in geänderter Form) in die Datei AppMeasurement.js einschließen können.

```
s.ActivityMap.link = function(ele, linkName) {
  if (linkName) {
    return linkName;
  }
  if (ele) {
    if (ele.tagName == 'A' && ele.href) {
      return ele.href;
    }
  }
}
```

Das `linkName` wird bei Aufrufen an `s.tl()` weitergeleitet.

```
s.ActivityMap.region = function(ele) {
  var className,
  classNames = {
    'header': 1,
    'navbar': 1,
    'left-content': 1,
    'main-content': 1,
    'footer': 1,
  }; 
  while ((ele && (ele = ele.parentNode))) {
    if ((className=ele.className) && classNames[className]) {
      return className;
    }
  }
  return "BODY";
}
```
