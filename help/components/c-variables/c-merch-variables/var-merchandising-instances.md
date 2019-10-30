---
description: Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.
keywords: Analytics-Implementierung
seo-description: Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.
seo-title: Instanzen auf Merchandising-Variablen
solution: Analytics
title: Instanzen auf Merchandising-Variablen
topic: Entwickler und Implementierung
uuid: 4cdfd53e-88aa-48cf-a135-98f7fc8dcece
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Instanzen auf Merchandising-Variablen

Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.

Instanzen werden derzeit nicht für Merchandising-Variablen unterstützt. Wenn Instanzen in einem Bericht eine Merchandising-Variable enthalten, deutet das darauf hin, dass die eVar sich außerhalb der Produktzeichenfolge befindet und daher nicht in den Instanzen für die ausgewählte Merchandising-Variable einbezogen werden sollte.

Wenn Sie die Konversionsvariablensyntax verwenden, wird für jedes Setzen der Variable eine Instanz gezählt. Die Instanz wird jedoch der Wert „Keine“ zugewiesen, es sei denn, Folgendes tritt bei jedem Setzen der Variable ein:

* Ein Binding-Ereignis wird gesetzt.
* Die Produktvariable wird gesetzt.
* Die Merchandising-eVar hat einen Wert.

Z. B. wird die folgende Instanz von „eVar1“ dem Wert „Outdoor:Skibrille“ zugeordnet:

```js
s.eVar1="Outdoors:Ski Goggles" 
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

Im nächsten Beispiel jedoch wird die Instanz von „eVar1“ dem Wert „Keine“ zugeordnet, da beim Setzen der „eVar“ keine der Bedingungen erfüllt ist (es gibt kein Binding-Ereignis und die Produktvariable ist nicht gesetzt):

Seite 1 des Besuchs:

```js
s.eVar1="Outdoors:Ski Goggles"
```

Seite 2 des Besuchs:

```js
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

Die Zuordnung auf den Wert „Keine“ tritt ein, wenn Sie einen Wert für eine „eVar“ auf einer Seite festlegen, auf der kein Binding-Ereignis stattfindet, oder Sie den eVar-Wert in der Produktzeichenfolge ohne Binding-Ereignis festlegen.

> [!NOTE] Die aktuelle Funktion zum Zählen von Instanzen für Merchandising-Variablen wird derzeit überprüft und in einer kommenden Version geändert.

