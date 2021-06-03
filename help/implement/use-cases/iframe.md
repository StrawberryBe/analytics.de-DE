---
title: „AppMeasurement“ mit iFrames verwenden
description: Greifen Sie auf Adobe Analytics-Variablen innerhalb eines IFrame oder einer übergeordneten Seite zu, während Sie sich in einem IFrame befinden.
exl-id: 59b9cd4f-8599-41ee-8b54-a6a556198ecd
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 97%

---

# „AppMeasurement“ mit iFrames verwenden

Sie können „AppMeasurement“-Variablen sowohl von untergeordneten als auch von übergeordneten iFrames aus referenzieren. Es ist erforderlich, alle Variablen am selben Speicherort zu definieren, an dem sich die „AppMeasurement“-Bibliothek befindet. In den folgenden Beispielen wird erläutert, wie Sie einfache „AppMeasurement“-Variablen und -Methoden innerhalb und außerhalb eines iFrames festlegen.

Wenn Sie Adobe Experience Platform Launch verwenden, stellen Sie sicher, dass das Tracker-Objekt global verfügbar ist. Siehe [Übersicht über die Adobe Analytics-Erweiterung](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html) im Launch-Benutzerhandbuch.

>[!CAUTION]
>
>Vermeiden Sie, „AppMeasurement“-Bibliotheken sowohl auf einer übergeordneten Seite als auch in einem IFrame zu verwenden. Dadurch entstehen Risiken beim Senden mehrerer Bildanfragen, wodurch die Größe der Berichte und die Anzahl der gebührenpflichtigen Server-Aufrufe steigt.

## Zugriff auf „AppMeasurement“ in einem IFrame

Sie können über das IFrame-Objekt auf „AppMeasurement“-Variablen zugreifen. In diesen Beispielen wird [pageName](../vars/page-vars/pagename.md) gesetzt und die [t()-Methode](../vars/functions/t-method.md) mit zwei verschiedenen Referenzierungsarten des IFrame-Objekts aufgerufen.

```js
// Reference AppMeasurement code that resides within an iframe and send an image request
document.getElementById('targetFrame').contentWindow.s.pageName="Page name within iframe";
document.getElementById('targetFrame').contentWindow.s.t();

// An alternate method to the above if there's only one iframe on the page
window.frames[0].contentWindow.s.pageName = "Page name within iframe";
window.frames[0].contentWindow.s.t();
```

## Zugriff auf „AppMeasurement“ innerhalb eines IFrame

Sie können innerhalb eines IFrame auf „AppMeasurement“-Variablen auf einer übergeordneten Seite zugreifen. In diesem Beispiel wird [pageName](../vars/page-vars/pagename.md) gesetzt und die [t()-Methode](../vars/functions/t-method.md) mit der [`parent`](https://www.w3schools.com/jsref/prop_win_parent.asp)-Eigenschaft aufgerufen.

```js
// Reference AppMeasurement code on a parent page from within an iframe and send an image request
parent.s.pageName = "Page Name on Hosted Window";
parent.s.t();
```

## Verwenden von `postMessage`- und Ereignis-Listenern

Alternativ können Sie Variablen mit `postMessage`- und Ereignis-Listenern festlegen. Für diese Methode ist kein direkter Verweis auf einen IFrame erforderlich.

```js
// Place this code in your parent window
function listenMessage(e) {
    if(e.data == "Example page view call") {
        s.pageName = "Page name using postMessage";
        s.t();
    }
}
window.addEventListener("message", listenMessage, false);

// Place this code in the iframe
window.top.postMessage("Example page view call","https://example.com");
```

## Einschränkungen

* Wie bei anderen JavaScript-Codes können iFrames nur dann kommunizieren, wenn Domains und Protokolle übereinstimmen. Diese Beispiele funktionieren nicht, wenn sich der IFrame-Inhalt in einer anderen Domain als die übergeordnete Domain befindet.
* Wenn sich „AppMeasurement“ in einem IFrame befindet, wird die [`referrer`](../vars/page-vars/referrer.md)-Variable auf die übergeordnete URL festgelegt und nicht auf die tatsächlich verweisende URL. Sie können zur Lösung dieses Problems die `referrer`-Variable manuell festlegen.
* Der [Adobe Experience Cloud-Debugger](https://docs.adobe.com/content/help/de-DE/experience-cloud/user-guides/home.translate.html) erkennt keine Bildanforderungen, die innerhalb von iFrames ausgelöst werden.
* Activity Map zeigt die Heatmap nicht über Links an, auf die innerhalb von iFrames geklickt wurde. Stattdessen wird der gesamte IFrame hervorgehoben.
