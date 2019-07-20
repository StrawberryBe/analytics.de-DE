---
description: Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.
keywords: Analytics-Implementierung
seo-description: Beschreibt, wie Instanzen auf Merchandising-Variablen angerechnet werden.
seo-title: Instanzen bei Merchandising-Variablen
solution: Analytics
title: Instanzen bei Merchandising-Variablen
topic: Entwickler und Implementierung
uuid: 4 cdfd 53 e -88 aa -48 cf-a 135-98 f 7 fc 8 dcece
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Instanzen bei Merchandising-Variablen

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

>[!NOTE]
>
>Die aktuelle Funktion zum Zählen von Instanzen bei Merchandising-Variablen wird überarbeitet und in einer kommenden Version geplant.

