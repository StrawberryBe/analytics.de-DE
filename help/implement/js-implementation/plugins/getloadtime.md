---
description: Ruft die Ladezeit für die Seite bis auf die Zehntelsekunde genau ab und ermöglicht das Speichern des Werts in einem Ereignis „prop“ und „eVar“ und/oder in einem numerischen Ereignis.
keywords: Analytics Implementation
title: getLoadTime
topic: Developer and implementation
uuid: 5d26a69b-cbde-4be1-bac1-5ee8a4e55ca3
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getLoadTime

Ruft die Ladezeit für die Seite bis auf die Zehntelsekunde genau ab und ermöglicht das Speichern des Werts in einem Ereignis „prop“ und „eVar“ und/oder in einem numerischen Ereignis.

Um dieses Plug-in zu verwenden, fügen Sie den Funktionscode ein und rufen die Funktion anschließend zwei Mal in der Datei [!DNL s_code.js] auf. Einmal am Anfang der Datei und ein zweites Mal im Abschnitt `doPlugins`. Dieses Plug-in wurde bewusst nicht als eine Methode des Objekts „s“ definiert. Dies hätte zu einer erhöhten berechneten Ladezeit für die Seite geführt.

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code und -Implementierung {#section_968AC379C3004C359A85AFED5A48D5AE}

**Funktion hinzufügen**

Fügen Sie die folgende Definition der Funktion `s_getLoadTime` irgendwo oberhalb des Abschnitts „DO NOT ALTER ANYTHING BELOW THIS LINE“ in die Datei [!DNL s_code.js] ein:

```js
function s_getLoadTime(){if(!window.s_loadT){var b=new Date().getTime(),o=window.performance?performance.timing:0,a=o?o.requestStart:window.inHeadTS||0;s_loadT=a?Math.round((b-a)/100):''}return s_loadT}
```

**Erstmaliger Aufruf der Funktion**

Fügen Sie dem Plug-in `s_getLoadTime()` im Bereich des Anfangs von [!DNL s_code.js] und außerhalb jeglicher Funktionen einen Aufruf hinzu.

**Letzter Aufruf der Funktion**

Fügen Sie dem Plug-in `s_getLoadTime()` innerhalb der Funktion `s_doPlugins()` einen weiteren Aufruf hinzu und speichern Sie den zurückgegebenen Wert in einem „prop“, „eVar“ und/oder in einem numerischen Ereignis.

Anwendungsbeispiel 1 – Speichern der Ladezeit für die Seite in „prop10“ und „eVar20“:

```js
s.eVar20=s.prop10=s_getLoadTime();
```

Anwendungsbeispiel 2 – Speichern der Ladezeit für die Seite im numerischen Ereignis „event99“:

```js
if(s_getLoadTime())s.events=s.apl(s.events,'event90='+s_getLoadTime(),',',1);
```

**(Optional) Hinzufügen der Unterstützung für ältere Browser**

Um ältere Browser zu unterstützen, die nicht über die Eigenschaft [window.performance.timing](https://www.html5rocks.com/en/tutorials/webperformance/basics/) verfügen, fügen Sie im HTML-Code dem Abschnitt „HEAD“ im Anfangsbereich, aber vor dem Aufruf von .js-, .css- oder anderen Dateien die folgende Zeile hinzu:

```
<script type="text/javascript">var inHeadTS=(new Date()).getTime();</script>
```

