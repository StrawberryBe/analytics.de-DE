---
description: Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.
keywords: Analytics Implementation
title: Instanzen auf Merchandising-Variablen
topic: Developer and implementation
uuid: 4cdfd53e-88aa-48cf-a135-98f7fc8dcece
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Instanzen auf Merchandising-Variablen

Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.

Instanzen werden derzeit nicht für Merchandising-Variablen unterstützt. Wenn Sie Instanzen in einem Bericht mit einer Merchandising-Variablen bemerken, deutet dies darauf hin, dass die eVar an einigen Stellen außerhalb der Produktzeichenfolge festgelegt wird und nicht als echte Anzahl von Instanzen für die ausgewählte Merchandising-Variable betrachtet werden sollte.

Wenn Sie die Konversionsvariablensyntax verwenden, wird jedes Mal, wenn die Variable festgelegt wird, eine Instanz gezählt. Die Instanz wird jedoch auf &quot;Keine&quot;zurückgeführt, es sei denn, jedes Mal, wenn die Variable festgelegt wird, erfolgt Folgendes:

* Es wird ein Bindungs-Ereignis festgelegt.
* Die Variable &quot;products&quot;wird eingestellt.
* Die Merchandising-eVar hat einen Wert.

Beispielsweise wird die folgende Instanz von eVar1 &quot;Outdoors:Skibrille&quot;zugeordnet:

```js
s.eVar1="Outdoors:Ski Goggles" 
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

Im nächsten Beispiel wird die Instanz von eVar1 jedoch &quot;Keine&quot;zugeordnet, da bei Einstellung der eVar nicht alle Bedingungen erfüllt sind (es gibt kein Binding-Ereignis und die Produktvariable ist nicht festgelegt):

Seite 1 des Besuchs:

```js
s.eVar1="Outdoors:Ski Goggles"
```

Seite 2 des Besuchs:

```js
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

Die Zuordnung auf &quot;Keine&quot;erfolgt, wenn Sie einen Wert für eine eVar auf einer Seite festlegen, auf der kein Binding-Ereignis auftritt, oder wenn Sie den eVar-Wert in der Produktzeichenfolge ohne Binding-Ereignis festlegen.

>[!NOTE] Die aktuelle Funktion zum Zählen von Instanzen für Merchandising-Variablen wird derzeit überarbeitet und im Rahmen eines zukünftigen Releases geändert.

