---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: edf88e40cae8b6886b04257f266666c13a37f88d

---



# Listen-Props

Listen-Props sind eine Liste getrennter Werte, die in einer Variablen übergeben und in Berichten dann als einzelne Zeilenelemente behandelt werden. Listen-Props werden meist auf Seiten implementiert, die vom Benutzer auswählbare Werte enthalten (wie z. B. Artikellisten mit Kontrollkästchen oder Optionsschaltern). Sie sind nützlich, wenn Sie mehrere Werte in einer einzigen Variablen definieren möchten, ohne dass mehrere Bildanforderungen gesendet werden.

<!-- 

list_props.xml

 -->

**Zu beachten**

* Listen-Props sind nur für Traffic-Variablen ( [props](/help/implement/js-implementation/page-variables/propn.md)).
* Die Pathing-Funktion und Korrelationen können bei Listen-Props nicht aktiviert werden.
* Analytics gibt Besuche und Unique Visitors in fast jedem Bericht an (inklusive aller Listen-Props-Berichte).
* Für Listen-Props werden Classifications unterstützt.
* Jede benutzerspezifische Traffic-Variable kann zu einer Listen-Prop werden. (Ausnahmen: [pageName](/help/implement/js-implementation/page-variables/pagename.md), [channel](/help/implement/js-implementation/page-variables/channel.md) und [server](/help/implement/js-implementation/page-variables/server.md).)

* Wenn in einer Bildanforderung Werte doppelt definiert sind, werden Instanzen nicht dedupliziert.

Ein Prop kann auf der Seite „Admin Tools &gt; Report Suite &gt; Traffic-Variablen“ in ein Listen-Prop umgewandelt werden, indem Sie die Listenunterstützung aktivieren und anschließend ein Trennzeichen auswählen. Häufig verwendete Trennzeichen sind: Doppelpunkt, Semikolon, Komma oder senkrechter Strich (Pipe). Als Trennzeichen können grundsätzlich die ersten 127 ASCII-Zeichen verwendet werden.

**Implementierungsbeispiele**

Wenn Sie eine Aktivierung von Listen-Props anfordern, müssen Sie das Trennzeichen angeben, das Sie verwenden möchten. Nach Aktivierung der gewünschten *`s.prop`* können mehrere Werte in der Variable – wie in den folgenden Beispielen gezeigt – festgelegt werden:

Eine durch einen senkrechten Strich (Pipe) begrenzte Listen-Prop, die zwei Werte übergibt:

```js
s.prop1="Banner ad impression|Sidebar impression"
```

Eine durch ein Komma begrenzte Listen-Prop, die mehrere Werte übergibt:

```js
s.prop2="cerulean,vermilion,saffron"
```

Listen-Props können auch mit einem einzelnen Wert gesendet werden:

```js
s.prop3="Single value"
```

Das Trennzeichen kann jederzeit geändert werden. Die Implementierung muss aber dem neuen Trennzeichen entsprechen. Fehler bei der Verwendung des korrekten Trennzeichens im Wert der Listen-Prop führen dazu, dass der Wert bei der Berichterstellung als einzelner verketteter Zeileneintrag behandelt wird.

Da es sich bei einer Listen-Props weiterhin um eine Traffic-Variable handelt, unterliegt sie auch den Beschränkungen für Traffic-Variablen. Listen-Props sind auf 100 Byte an Daten begrenzt und unterliegen Einstellungen für die Groß-/Kleinschreibung.

