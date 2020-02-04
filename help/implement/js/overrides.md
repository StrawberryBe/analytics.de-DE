---
title: Variablenüberschreibungen
description: Durch das Überschreiben von Variablen können Sie den Wert einer Variablen für einen einzelnen Verfolgungs- oder Verfolgungslinkaufruf ändern.
translation-type: tm+mt
source-git-commit: 1f0fd2dcb0454ad9bc2e0c2141b5e17470c6a5de

---


# Variablenüberschreibungen

Mit Variablenüberschreibungen können Sie Analytics-Werte für einen einzelnen Treffer ändern, ohne dass sich dies auf vorhandene Variablen auf der Seite auswirkt.

## Arbeitsablauf

1. Erstellen Sie ein neues JavaScript-Objekt. Der Objektname kann beliebig sein.

   ```js
   var y = new Object();
   ```

2. Weisen Sie diesem Objekt gültige Analytics-Eigenschaften zu:

   ```js
   y.eVar1 = "New value";
   y.events = "event2";
   ```

3. Verwenden Sie das Objekt als Argument innerhalb des entsprechenden Verfolgungsaufrufs:

   ```js
   // Use the override object in a standard page view call
   s.t(y);
   
   // Use the override object in a link tracking call
   s.tl(this,'o','Example override link',y);
   ```

Wenn ein Verfolgungsaufruf ein Objekt im Parameter overrides empfängt, überschreiben alle gültigen Werte im Override-Objekt die Werte im Standard-Analytics-Objekt. Bereits in Ihrem vorhandenen Analytics-Objekt definierte Variablen sind davon nicht betroffen.
