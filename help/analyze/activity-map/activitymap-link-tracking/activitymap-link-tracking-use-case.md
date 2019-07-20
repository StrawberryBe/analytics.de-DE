---
description: Sie können Links voneinander abgrenzen, indem Sie die Link-ID mithilfe der Variablen s_objectID anpassen, die Region und die Activity Map-Moduldatei AppMeasurement anpassen.
seo-description: Sie können Links voneinander abgrenzen, indem Sie die Link-ID mithilfe der Variablen s_objectID anpassen, die Region und die Activity Map-Moduldatei AppMeasurement anpassen.
seo-title: Unterscheiden Sie Links, die auf dieselbe Link-ID und Region verweisen.
solution: Analytics
title: Unterscheiden Sie Links, die auf dieselbe Link-ID und Region verweisen.
topic: Activity Map
uuid: f 2 da 0 cda-a 33 b -4 a 12-8 d 99-1 f 8386 d 6 d 30
translation-type: tm+mt
source-git-commit: 4f313ae50c4d5a0f3bfec493c2d554bc8614aeef

---


# Unterscheiden Sie Links, die auf dieselbe Link-ID und Region verweisen.

Sie können Links voneinander abgrenzen, indem Sie die Link-ID mithilfe der Variablen s_objectID anpassen, die Region und die Activity Map-Moduldatei AppMeasurement anpassen.

Beispiel: Angenommen, Sie haben mehrere Links des Typs „Buy“, die von Activity Map unter der gleichen Link-ID und Region identifiziert werden.

<table id="table_3020E2C0175D455C84E794CF51BE5A93"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Codebeispiel </th> 
   <th colname="col2" class="entry"> Link-ID </th> 
   <th colname="col3" class="entry"> Region </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <code>&lt; div id = "recommendation panel" &gt; 
 &lt; div &gt; 
 &lt; a href = "product1.html" &gt; Buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a href = "product2.html" &gt; Buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a href = "product3.html" &gt; Buy &lt;/a &gt; 
 &lt;/div &gt; </code>
  </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p> <p> </p>Buy <p> </p> <p> </p> <p>Buy </p> <p> </p> <p> </p> <p>Buy </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p> <p> </p>Bereich für Empfehlungen <p> </p> <p> </p> <p>Bereich für Empfehlungen </p> <p> </p> <p> </p> <p>Bereich für Empfehlungen </p> </td> 
  </tr> 
 </tbody> 
</table>

Wie können Sie Ihre Webseite und das Tagging anpassen, um die Werte dieser Links zu unterscheiden? Sie haben drei Optionen: Sie können die Link-ID anpassen, die Region anpassen oder die Activity Map-Moduldatei AppMeasurement anpassen.

## Link-ID mit s_objectID anpassen {#section_01B0D463397B4837B2D46F087A6E5937}

Durch Erstellung einer eindeutigen Objekt-ID für einen Link oder eine Linkposition auf einer Seite können Sie die Activity Map-Verfolgung verbessern. Sie können Activity Map auch zum Generieren von Berichten zum Linktyp oder zur Linkposition anstelle der Link-URL verwenden. Klicken Sie [hier](https://marketing.adobe.com/resources/help/en_US/sc/implement/s_objectID.html), um weitere Informationen zur Variablen s_objectID zu erhalten.

>[!IMPORTANT]
>
>Beachten Sie, dass ein Semikolon (;) erforderlich ist, wenn s_ objectid in Activity Map verwendet wird.

<table id="table_9439A5F320304E439A19842CF3EBA456"> 
 <thead> 
  <tr> 
   <th colname="col02" class="entry"> Codebeispiel </th> 
   <th colname="col2" class="entry"> Link-ID </th> 
   <th colname="col3" class="entry"> Region </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col02"> 
    <code>&lt; div id = "recommendation panel" &gt; 
 &lt; div &gt; 
 &lt; a onclick = "s_ objectid =' Product 1 '; " href = "product1.html" &gt; Kaufen &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a onclick = "s_ objectid =' Product 2 '; " href = "product2.html" &gt; Kaufen &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div &gt; 
 &lt; a onclick = "s_ objectid =' Product 3 '; " href = "product3.html" &gt; Kaufen &lt;/a &gt; 
 &lt;/div &gt; </code>
  </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p>Product1 <p> </p> <p> </p> <p>Product2 </p> <p> </p> <p> </p> <p>Product3 </p> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p> <p>Bereich für Empfehlungen </p> <p> </p> <p> </p> <p>Bereich für Empfehlungen </p> <p> </p> <p> </p> <p>Bereich für Empfehlungen </p> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Region anpassen {#section_6B1EF302573B445DBAF44176D0A12DB9}

Sie können die Region anpassen, indem Sie sicherstellen, dass für jeden Link vom Typ „buy“ eine eigene Region definiert ist. Dazu fügen Sie einem der übergeordneten Elemente jedes Anker-Tags „Buy“ den Parameter „id“ hinzu.

>[!NOTE]
>
>Sie sind nicht auf den Parameter "id" als Regionskennung beschränkt. Sie können auch Ihre eigene ID mithilfe der javascript-Variablen "s. activitymap. regionidattribute" festlegen.

<table id="table_250DB52A869C466B942517BABA1C287B"> 
 <thead> 
  <tr> 
   <th colname="col02" class="entry"> Codebeispiel </th> 
   <th colname="col2" class="entry"> Link-ID </th> 
   <th colname="col3" class="entry"> Region </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col02"> 
    <code>&lt; div id = "recommendation panel" &gt; 
 &lt; div id = "region a" &gt; 
 &lt; a href = "product1.html" &gt; Buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div id = "region b" &gt; 
 &lt; a href = "product2.html" &gt; Buy &lt;/a &gt; 
 &lt;/div &gt; 
 &lt; div id = "region c" &gt; 
 &lt; a href = "product3.html" &gt; Buy &lt;/a &gt; 
 &lt;/div &gt; </code>
  </td> 
   <td colname="col2"> <p> </p> <p> </p> <p> </p> <p>Buy </p> <p> </p> <p> </p> <p>Buy </p> <p> </p> <p> </p> <p>Buy </p> </td> 
   <td colname="col3"> <p> </p> <p> </p> <p> </p>Region a <p> </p> <p> </p> <p>Region b </p> <p> </p> <p> </p> <p>Region c </p> </td> 
  </tr> 
 </tbody> 
</table>

## Activity Map-Moduldatei AppMeasurement anpassen {#section_B933BB9F944E4D5389002908A5A881F8}

>[!CAUTION]
>
>Testen Sie den geänderten Code, um sicherzustellen, dass er ordnungsgemäß funktioniert. Adobe übernimmt keine Verantwortung für das Verhalten des geänderten Codes.

Im Folgenden finden Sie einige Beispiele für** generische** Link-/Regionsfunktionen, die Sie (im geänderten Formular) in Ihre Datei appmeasurement. js aufnehmen können.

```
s.ActivityMap.link = function(ele,linkName){ 
if(linkName){ 
return linkName; 
} 
if(ele){ 
if(ele.tagName == 'A' && ele.href){ 
return ele.href; 
} 
} 
} 
```

Der linkName wird bei Aufrufen an s.tl. übergeben.

```
s.ActivityMap.region = function(ele){ 
var className, 
classNames = { 
'header': 1, 
'navbar': 1, 
'left-content': 1, 
'main-content': 1, 
'footer': 1, 
}; 
  while( (ele && (ele = ele.parentNode))){ 
if( (className=ele.className) && classNames[className]){ 
return className; 
} 
} 
return "BODY"; 
} 
```

