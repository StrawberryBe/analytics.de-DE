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



# linkName

Die Variable „“ ist eine optionale Variable, die beim [!UICONTROL Linktracking] den Namen eines benutzerspezifischen Links, eines Exitlinks oder Downloadlinks angibt.


<!-- 

linkName.xml

 -->

Die Variable *`linkName`* ist normalerweise nicht erforderlich, da diese Variable durch den dritten Parameter in der Funktion *`tl()`* ersetzt wird.

<table id="table_4B0D1C9AADA542A59B626E077D5FC568"> 
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
   <td> pev2 </td> 
   <td> <p>Dateiladungen </p> <p>Benutzerspezifische Links </p> <p>Exitlinks </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL Benutzerspezifische Links] verweisen auf Links, die Rückverfolgungsdaten senden. Die Variable *`linkName`* (oder der dritte Parameter in der Funktion *`tl()`*) wird verwendet, um den Wert zu identifizieren, der im [!UICONTROL Benutzerspez.], [!UICONTROL Download-] oder [!UICONTROL Exitlinks-]Bericht erscheint. Wenn *`linkName`* nicht aufgefüllt ist, wird im Bericht die URL des Links angezeigt.

**Syntax und mögliche Werte** {#section_C8D89834C98B4C7A858C947293C4148E}

```js
s.linkName="Link Name"
```

*`linkName`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_5F68766210184E82A23D2A6ECD80BA0B}

```js
s.linkName="Nav Bar Home Link"
```

```js
s.linkName="Partner Link to A.com"
```

**Konfigurationseinstellungen** {#section_F15FF429FC274F708D50DF79D4668EA3}

Keine

**Probleme, Fragen und Tipps** {#section_170A78452A7340B5B229713AC1FB71FA}

* Die Variable *`linkName`* wird durch den dritten Parameter in der Funktion *`tl()`* ersetzt.

* Wenn die Variable *`linkName`* und der dritte Parameter in der Funktion *`tl()`* leer sind, wird die vollständige URL des Links (mit Ausnahme der Abfragezeichenfolge) im Bericht angezeigt (auch bei einem relativen Link).
