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


# kanal

Die Variable „“ wird meist verwendet, um einen Abschnitt einer Website zu identifizieren.


<!-- 

channel.xml

 -->

So könnten bei einem Händler zum Beispiel die Abschnitte „Elektronik“, „Spielzeug“ oder „Kleidung“ heißen. Eine Mediensite könnte die Abschnitte „Nachrichten“, „Sport“ oder „Wirtschaft“ enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | CH | „Site-Content“ &gt; „Site-Abschnitte“ | "" |

Adobe empfiehlt, die Kanalvariable auf jeder Seite mit Werten zu füllen. Sie können auch eine Korrelation zwischen den Variablen *`channel`* und [!UICONTROL page name] aktivieren.

Wenn Bereiche eine oder mehrere Ebenen mit Unterbereichen aufweisen, können Sie diese Bereiche in der Variable *`channel`* zeigen oder mithilfe von gesonderten Variablen ausweisen.

**Syntax und mögliche Werte**

```js
s.channel="value"
```

Für die Variable *`channel`* gibt es keine speziellen Einschränkungen.

**Beispiele** {#section_2527B2BB1CFD46CB952178ABF7A9028A}

```js
s.channel="Electronics"
```

```js
s.channel="Media"
```

**Probleme, Fragen und Tipps** {#section_61941D5E4E644B59A267A4F44FD5DE8C}

Wenn Ihre Site mehrere Ebenen enthält, können Sie die Variable *`hierarchy`* oder eine andere Variable verwenden, um diese Ebenen zu bezeichnen. Der Wert *`channel`* ist nicht beständig, aber die auf der gleichen Seite ausgelösten Erfolgsereignisse werden dem Wert *`channel`* zugeordnet.
