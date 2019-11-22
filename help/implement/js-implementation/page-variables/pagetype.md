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


# pageType

Die Variable „“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).


<!-- 

pageType.xml

 -->

<table id="table_0492B136E9D14070A6CA49ED534BCA4C"> 
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
   <td> 20 Byte </td> 
   <td> pageType </td> 
   <td> Pfade &gt; Seiten &gt; Seiten <p>nicht gefunden </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

The *`pageType`* variable captures the errant URL when a 404 Error page is displayed, which allows you to quickly find broken links and paths that are no longer valid on the custom site. Richten Sie die Variable *`pageType`* auf der Fehlerseite genau wie unten dargestellt ein.

Verwenden Sie auf 404-Fehlerseiten nicht die Variable „pageName“. Die Variable *`pageType`* wird nur für die 404-Fehlerseite verwendet.

Die 404-Fehlerseite ist in den meisten Fällen eine statische Seite, die fest einprogrammiert ist. In solchen Situationen ist es wichtig, dass als Verweis auf die JS-Datei ein entsprechender globaler oder relativer Pfad/Verzeichnis festgelegt ist.

**Syntax und mögliche Werte** {#section_C1C59968226446559B05F6EE7374D525}

Der einzige zulässige Wert von *`pageType`* ist „errorPage“, wie unten dargestellt.

```js
s.pageType="errorPage"
```

**Beispiele** {#section_6CE22FCB835B4A19B633B7F67E73A115}

```js
s.pageType="errorPage"
```

**Konfigurationseinstellungen** {#section_3B304A6D3A6C48F2BE90B4DA92A39DDB}

Keine

**Probleme, Fragen und Tipps** {#section_943681AB01FE47BEAC72E93CB60C53C8}

Wenn Sie andere Server-seitige Fehler erfassen möchten (z. B. Fehler aus der 500-Reihe), speichern Sie die Fehlermeldung in einer Prop und setzen Sie in der Variable *`pageName`* den Wert `500 Error: <URL>`, wobei `<URL>` die angeforderte URL ist. Auf diese Weise können Sie in [!UICONTROL Pfadsetzungsberichten] erkennen, welche Pfade bei Benutzern zu Fehlern der 500-Reihe geführt haben. Die vom Server angegebene Fehlermeldung wird in der Eigenschaftsvariablen erklärt.

