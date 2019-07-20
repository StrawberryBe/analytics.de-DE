---
description: Mit dem apl-Plug-in (oder appendList) können Sie jeder getrennten Liste einen Wert anhängen und dabei festlegen, ob nach Groß- und Kleinschreibung unterschieden werden soll oder nicht, um sicherzustellen, dass der Wert nicht bereits in der Liste vorhanden ist. Auf das APL-Plug-in wird von diversen Standard-Plug-ins verwiesen, aber es kann auch in einer Reihe von Situationen direkt verwendet werden.
keywords: Analytics-Implementierung
seo-description: Mit dem apl-Plug-in (oder appendList) können Sie jeder getrennten Liste einen Wert anhängen und dabei festlegen, ob nach Groß- und Kleinschreibung unterschieden werden soll oder nicht, um sicherzustellen, dass der Wert nicht bereits in der Liste vorhanden ist. Auf das APL-Plug-in wird von diversen Standard-Plug-ins verwiesen, aber es kann auch in einer Reihe von Situationen direkt verwendet werden.
seo-title: appendList
solution: Analytics
subtopic: Plug-ins
title: appendList
topic: Entwickler und Implementierung
uuid: e 923 c 86 c-eaa 6-4 e 17-a 3 a 4-0 e 08 af 886674
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# appendList

Mit dem apl-Plug-in (oder appendList) können Sie jeder getrennten Liste einen Wert anhängen und dabei festlegen, ob nach Groß- und Kleinschreibung unterschieden werden soll oder nicht, um sicherzustellen, dass der Wert nicht bereits in der Liste vorhanden ist. Auf das APL-Plug-in wird von diversen Standard-Plug-ins verwiesen, aber es kann auch in einer Reihe von Situationen direkt verwendet werden.

Das Plug-in ist hilfreich, um:

* Ein Ereignis zur aktuellen „events“-Variablen hinzuzufügen
* Einen Wert zu einer „list“-Variablen hinzuzufügen, ohne einen Wert in der Liste zu duplizieren
* Ein Produkt auf Grundlage einer bestimmten Seitenlogik zur aktuellen Variablen „products“ hinzufügen
* Werte zu den Parametern hinzuzufügen: *`linkTrackVars`* und *`linkTrackEvents`*

**Fall 1**

<table id="table_5AAC1D9892CD4E5C9060E119EE4E7DC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Szenario </p> </td> 
   <td colname="col2"> <p>Fügen Sie <span class="term"> event 1 </span> zur aktuellen Ereignisvariablen, wobei sichergestellt wird, dass das Ereignis nicht dupliziert wird. </p> <p>s.events="scCheckout" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code </p> </td> 
   <td colname="col2"> <p>s.events=s.apl(s.events,"event1",",",1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ergebnisse </p> </td> 
   <td colname="col2"> <p>s.events="scCheckout,event1" </p> </td> 
  </tr> 
 </tbody> 
</table>

**Fall 2**

<table id="table_C4356C9AB95948F3929A7B75E07AE9E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Szenario </p> </td> 
   <td colname="col2"> <p>Fügen Sie den Wert <span class="term"> Verlauf </span> zur Listenvariablen <span class="varname"> prop 1 </span>, mit <span class="term"> Verlauf </span> und <span class="term"> Verlauf </span> als derselbe Wert. </p> <p>s.prop1="Naturwissenschaft,Geschichte" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code </p> </td> 
   <td colname="col2"> <p>s.prop1=s.apl(s.prop1,"geschichte",",",2) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ergebnisse </p> </td> 
   <td colname="col2"> <p>s.prop1="Naturwissenschaft,Geschichte" </p> <p> <span class="term"> Der Verlauf </span> wird nicht hinzugefügt, da <span class="term"> der Verlauf </span> bereits in der Liste aufgeführt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Implementierung {#section_F4C91CA2037F478C9F7B53F357E6A5F0}

Führen Sie diese Schritte aus, um das APL-Plug-in zu implementieren.

1. Fordern Sie den Plug-in-Code beim Kundendienst oder Ihrem zuständigen Adobe-Berater an.
1. Add call(s) to the API function as needed within the *`s_doPlugins`* function

So könnte der Code auf Ihrer Site aussehen:

```js
/* Plugin Config */ 
 
s.usePlugins=true 
 
function s_doPlugins(s) { 
 
/* Add calls to plugins here */ 
 
s.events=s.apl(s.events,"event1",",",1) 
 
} 
 
s.doPlugins=s_doPlugins
```

**Unterstützte Browser**

Für dieses Plug-in muss JavaScript 1.0 durch den Browser unterstützt werden.

**Informationen zum Plug-in**

<table id="table_7B9EDD616C164D6B8B53558337DF12C2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Informationen zum Plug-in </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Parameter </p> </td> 
   <td colname="col2"> <p>apl((L,v,d,u) </p> <p>L= Quellenliste, leere Listen werden akzeptiert </p> <p> v = anzuhängender Wert </p> <p> d = Listentrennzeichen </p> <p> u (optional, standardmäßig 0) Prüfung eindeutiger Werte. 0 = keine eindeutige Prüfung, Wert wird immer angehängt. 1 = Prüfung ohne Unterscheidung zwischen Groß- und Kleinschreibung; nur anhängen, wenn Wert nicht in Liste enthalten ist. 2 = Prüfung mit Unterscheidung zwischen Groß- und Kleinschreibung; nur anhängen, wenn Wert nicht in Liste enthalten ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rückgabewert </p> </td> 
   <td colname="col2"> <p>Originalliste, mit angehängtem Wert, falls dieser hinzugefügt wurde </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nutzungsbeispiele </p> </td> 
   <td colname="col2"> <p>s.events=s.apl(s.events,"event1",",",1); </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Quellenliste L kann eine leere Liste sein, z. B. *`L=""`*. Der Rückgabewert ist dann entweder eine leere Liste oder eine Liste mit einem Wert.

**Plug-in-Code**

```js
/******************************************************************** 
 * 
 * Main Plug-in code (should be in Plug-ins section) 
 * 
 *******************************************************************/ 
/* 
 * Plugin Utility: apl v1.1 
 */ 
s.apl=new Function("l","v","d","u","" 
+"var s=this,m=0;if(!l)l='';if(u){var i,n,a=s.split(l,d);for(i=0;i<a." 
+"length;i++){n=a[i];m=m||(u==1?(n==v):(n.toLowerCase()==v.toLowerCas" 
+"e()));}}if(!m)l=l?l+d+v:v;return l"); 
 
/******************************************************************** 
 * 
 * Commented example of how to use this is doPlugins function 
 * 
 *******************************************************************/ 
  
 Not Applicable - Utility function only 
 
/******************************************************************** 
 * 
 * Config variables (should be above doPlugins section) 
 * 
 *******************************************************************/ 
 
 None 
 
/******************************************************************** 
 * 
 * Utility functions that may be shared between plug-ins (name only) 
 * 
 *******************************************************************/ 
  
 s.split
```

