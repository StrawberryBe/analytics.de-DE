---
description: Durch das Überschreiben von Variablen können Sie den Wert einer Variablen für einen einzelnen Verfolgungs- oder Verfolgungslinkaufruf ändern.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Variablenüberschreibungen
topic: Developer and implementation
uuid: 3ec09ae8-b9df-426f-8065-42b4518e6c5f
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Variablenüberschreibungen

Durch das Überschreiben von Variablen können Sie den Wert einer Variablen für einen einzelnen Verfolgungs- oder Verfolgungslinkaufruf ändern.

Erstellen Sie dazu ein neues Objekt, weisen Sie Variablenwerte zu und übergeben Sie dieses Objekt als ersten Parameter an `s.t()` bzw. als vierten Parameter an `s.tl()`:

```js
s.eVar1="one"; 
s.eVar2="two"; 
s.eVar3="three"; 
  
overrides = new Object(); 
overrides.eVar1="1_one"; 
overrides.eVar2=""; 
  
s.t(overrides);  
// values passed: eVar1="1_one", eVar2="", eVar3="three"
```

```js
s.linkTrackVars="eVar1,eVar2,eVar3,events"; 
s.eVar1="one"; 
s.eVar2="two"; 
s.eVar3="three"; 
 
overrides = new Object(); 
overrides.eVar1="1_one"; 
overrides.eVar2=""; 
 
s.tl(this,'e','AnotherSite',overrides,'navigate')  
// values passed: eVar1="1_one", eVar2="", eVar3="three"
```

