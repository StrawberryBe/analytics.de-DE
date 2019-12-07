---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# pageName

Die Variable „“ enthält den Namen von jeder Seite Ihrer Website.


<!-- 

pageName.xml

 -->

<table id="table_0D09BAEC2FFD43F7905ED3649B3F8E05"> 
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
   <td> 100 Byte </td> 
   <td> pageName </td> 
   <td> <p>Seiten </p> <p>Pfade </p> </td> 
   <td> Seiten-URL </td> 
  </tr> 
 </tbody> 
</table>

Die Variable *`pageName`* sollten Werte stehen, die für die Benutzer in Ihrem Unternehmen intuitiv verständlich sind. In den meisten Fällen ist der *`pageName`*-Wert nicht die URL oder der Pfad zur Datei. Übliche *`pageName`*-Werte umfassen zum Beispiel „Homepage“, „Checkout“, „Vielen Dank für Ihren Einkauf“ oder „Registrierung“.

Achten Sie darauf, dass in „pageName“ oder anderen Variablen keine Zeichen für Zeilenumbrüche, Gedankenstriche (em- oder en-Dashes) oder HTML-Zeichen enthalten sind. Zeilenumbrüche werden von manchen Browsern gesendet, von anderen nicht – für Analytics wären das dann zwei unterschiedliche Seitennamen. Bindestriche werden in vielen Textverarbeitungen und E-Mail-Clients noch während der Eingabe automatisch in lange oder kurze Gedankenstriche umgewandelt. Da lange oder kurze Gedankenstriche in Analytics-Variablen nicht zulässig sind (wie alle ASCII-Zeichen mit einer Nummer über 127), würde Analytics bei solch einem unzulässigen Seitennamen stattdessen die URL angeben.

Wenn *`pageName`* leer ist, wird die URL als Seitenname angegeben. Das Leerlassen von *`pageName`* ist meist problematisch, da die URL bei einer Seite nicht immer gleich bleibt (so sind z. B. `www.mysite.com` und `mysite.com` zwar unterschiedliche URLs, aber es ist die gleiche Seite).

**Syntax und mögliche Werte** {#section_7A61EE70F1A84D26B414404998C84BA8}

Die Variable *`pageName`* sollte einen für geschäftliche Benutzer von Analytics verständlichen Bezeichner enthalten.

```js
s.pageName="page_name"
```

*`pageName`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_8BB4F86F84E246A08B72DEC47FFC0765}

```js
s.pageName="Search Results" 
```

```js
s.pageName="Standard Offer List"
```

**Konfigurationseinstellungen** {#section_58CBC68C805344A999EB47455FEBA8D5}

Administratoren haben die Möglichkeit, mit dem Tool Seiten benennen den Seitennamen zu ändern, der in [!UICONTROL Analytics] angezeigt wird. Das kann jedoch gefährlich sein und negative Folgen in Berichten haben. Bitte wenden Sie sich zuerst an den Adobe-Kundendienst, bevor Sie das Tool [!UICONTROL Seiten benennen] verwenden.

**Probleme, Fragen und Tipps** {#section_BB41DC9682C34385B9CAA80D5257C113}

Vergewissern Sie sich, dass *`pageName`* keine unzulässigen Zeichen enthält.
