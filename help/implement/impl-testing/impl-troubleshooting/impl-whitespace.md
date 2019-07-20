---
description: In HTML gibt es mehrere Zeichen, die zu einem Leerzeichen führen.
keywords: Analytics-Implementierung
seo-description: In HTML gibt es mehrere Zeichen, die zu einem Leerzeichen führen.
seo-title: Leerraum in Variablenwerten verwenden
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Leerraum in Variablenwerten verwenden
topic: Entwickler und Implementierung
uuid: 1 edd 7934-9 b 3 e -43 e 2-9 f 24-65 f 42 cb 306 e 2
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Leerraum in Variablenwerten verwenden

In HTML gibt es mehrere Zeichen, die zu einem Leerzeichen führen.

Dazu gehören Leerzeichen, Tabulatoren und Wagenrücklauf (oder Zeilenvorschub). Siehe folgendes Beispiel:

```js
<head> 
 <title> 
   Home Page 
 </title> 
</head> 
<body> 
<script language="javascript"> 
 s.pageName=document.title 
</script> 
```

In diesem Fall füllt „document.title“ [!UICONTROL s.pageName] auf, das den Wert von „Home Page“ erhalten würde. Beachten Sie, dass vor „Home Page“ ein Leerzeichen steht. Dieses Leerzeichen wird nicht in allen Browsern auf die gleiche Weise interpretiert. Das Ergebnis kann dann wie folgt aussehen:

```js
s.pageName="Home Page"
```

```js
s.pageName="        Home Page"
```

Der erste Wert wird korrekt dargestellt. Beim zweiten Wert stehen jedoch leere Stellen vor dem Text. [!DNL Analytics] würde dies als unterschiedliche Werte für die Variable [!UICONTROL s.pageName] behandeln. Die [!DNL Analytics]-API schneidet beim zweiten Wert die vorangestellten Leerzeichen ab. Das Ergebnis ist ein Bericht, der wie folgt aussieht:

![](assets/white_space.jpg)

Dieser Implementierungsfehler führt dazu, dass der Variablenwert über mehrere Zeilen verteilt wird. In [!DNL SAINT] sind vorangestellte Leerzeichen in Schlüsselwerten nicht erlaubt. Das bedeutet, dass es bei diesem Problem nicht als Workaround eingesetzt werden kann, um mehrere Zeilenelemente zusammenzufassen. Die einzige Möglichkeit, dieses Problem zu beheben, besteht darin, den gewünschten Variablenwert (hier der Wert der Eigenschaft „document.title“) vorab so zu verarbeiten, dass alle Leerzeichen am Anfang (oder am Ende) entfernt werden.

Im oben gezeigten Beispiel wird die Variable [!UICONTROL s.pageName] bei der Eigenschaft „document.title“ verwendet. Adobe rät davon ab, „document.title“ als Seitennamen zu verwenden. Außerdem betrifft dieses Problem nicht nur die Variable [!UICONTROL s.pageName]. Jede Variable, deren Wert vorangestellte oder abschließende Leerzeichen enthält, kann davon betroffen sein.
