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



# linkType

Die Variable „“ ist optional und gibt bei der Linktracking an, in welchem Bericht ein Linkname oder eine Link-URL angezeigt wird (benutzerspezifische, Download- oder Exitlinks).


<!-- 

linkType.xml

 -->

Die Variable *`linkType`* ist normalerweise nicht erforderlich, da diese Variable durch den zweiten Parameter in der Funktion *`tl()`* ersetzt wird.

<table id="table_3D1A2FC1CECD4709BE2F9E32AC2DC730"> 
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
   <td> Ein Zeichen </td> 
   <td> pe=[lnk_o|lnk_d|lnk_e] </td> 
   <td> <p>Dateiladungen </p> <p>Benutzerdefinierte Links </p> <p>Exitlinks </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

Benutzerspezifische Links senden Daten nach Analytics Die Variable *`linkType`* (oder der zweite Parameter in der Funktion *`tl()`*) wird verwendet, um den Bericht zu identifizieren, in dem der Linkname oder die URL erscheint ( [!UICONTROL Benutzerspez.], [!UICONTROL Download-], oder [!UICONTROL Exitlinks-] Bericht).

Bei Exitlinks und Downloadlinks wird die Variable *`linkType`* automatisch gefüllt, je nachdem, ob es sich bei dem angeklickten Link um einen Exitlink oder Downloadlink handelt. Ein benutzerspezifischer Link kann konfiguriert werden, um Daten an einen dieser drei Berichte mit dieser Variablen oder den zweiten Parameter in der Funktion *`tl()`* zu senden. Durch die Einstellung von *`linkType`* auf „o“, „e“ oder „d“ wird *`linkName`* bzw. die Link-URL an den Bericht [!UICONTROL Benutzerspezifische Links], [!UICONTROL Exitlinks] bzw. [!UICONTROL Datei-Downloads] gesendet.

**Syntax und mögliche Werte** {#section_18DB3A8083FB4F75B970055ED336DA4E}

Die Syntax der Variable *`linkType`* hängt davon ab, ob Sie XML oder eine Abfragezeichenfolge verwenden.

Wenn Sie XML verwenden, darf die Variable nur ein einziges Zeichen, nämlich „o“ „e“ oder „d“, enthalten.

```js
s.tl(this,'o','Link Name');
```

Wenn Sie die Abfragezeichenfolge `pe` verwenden, müssen Sie `lnk_e`, `lnk_d` oder `lnk_o` hinzufügen.

**Beispiele** {#section_242B5DFFD1C9462A9A8EB1556B2E3160}

```js
<a href="index.html" onClick=" 
 var s=s_gi('rsid'); **see note below on the rsid** 
 s.tl(this,'o','Link Name'); 
 ">My Page</a> 
```

**Konfigurationseinstellungen** {#section_59738AD1B5E94294B8D36F4E772DEDB3}

Keine

**Probleme, Fragen und Tipps** {#section_F0D01DDE3FDA486C987162DA50A79C45}

* Wenn *`linkType`* nicht angegeben ist, wird von benutzerspezifischen Links („o“) ausgegangen.
