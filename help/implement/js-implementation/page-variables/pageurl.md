---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# pageURL

Die Variable „“ überschreibt die tatsächliche URL der Seite.


<!-- 

pageURL.xml

 -->

In seltenen Fällen kann es vorkommen, dass die URL der Seite nicht die ist, die in Analytics-Berichten aufgeführt wird.

<table id="table_D4DC6B476FFD4BEEB36A5C6B2D026255"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Keine Einschränkung* </td> 
   <td> <p>G </p> </td> 
   <td> Datenverkehr &gt; Segmentierung &gt; Bevorzugte Seitenpfade </td> 
   <td> „Seiten-URL“ </td> 
  </tr> 
 </tbody> 
</table>

> [!NOTE] Adobe erlaubt *`pageURL`*-Werte von bis zu 64.000. Bei einigen Browsern gibt es eine Größenbeschränkung bei URLs von Bildanforderungen. Um das Abschneiden von anderen Daten zu verhindern, werden Seiten-URLs, die länger als 255 Byte sind, geteilt, wobei die ersten 255 Byte im Parameter `g=` und die verbleibenden Bytes später in der Abfragezeichenfolge im Abfrageparameter `-g=` integriert werden.

**Syntax und mögliche Werte** {#section_22AF3BF7C2F743549967B0C760A095C0}

Die Variable *`pageURL`* muss eine gültige URL mit einem gültigen Protokoll sein. Die Domäne wird zwangsweise in Kleinbuchstaben umgewandelt, bevor sie in Berichte aufgenommen wird. Die Abfragezeichenfolge kann je nach den Einstellungen in Analytics möglicherweise gekürzt sein.

```js
s.pageURL="proto://domain/path?query_string"
```

Als Seiten-URL sind nur URL-kompatible Zeichen zulässig.

> [!NOTE] Es wird dringend empfohlen, sich vor der Verwendung der Variable *`pageURL`* für benutzerdefinierte Zwecke an Ihren Adobe-Berater oder die Kundenunterstützung zu wenden.

**Beispiele** {#section_45158FDA3F8F4574BDEB5CBC9F7E6C97}

```js
s.pageURL="https://mysite.com/home.jsp?id=1224" 
```

```js
s.pageURL="https://www.mysite.com/"
```

**Konfigurationseinstellungen** {#section_A8F77DAD88164528ACC5C16C066B47DF}

Keine

