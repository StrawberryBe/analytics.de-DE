---
title: AppMeasurement mit iframes verwenden
description: Greifen Sie auf Adobe Analytics-Variablen innerhalb eines iFrame oder einer übergeordneten Seite zu, während Sie sich in einem iframe befinden.
translation-type: tm+mt
source-git-commit: 355985a6baa1a1112e75446012be72f5c0a1d0c2
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 6%

---


# AppMeasurement mit iframes verwenden

Sie können AppMeasurement-Variablen sowohl von untergeordneten als auch von übergeordneten iframes referenzieren. Es ist erforderlich, alle Variablen am selben Speicherort zu definieren, an dem sich die AppMeasurement-Bibliothek befindet. In den folgenden Beispielen wird erläutert, wie Sie grundlegende AppMeasurement-Variablen und -Methoden innerhalb und außerhalb eines iFrames festlegen.

Wenn Sie Adobe Experience Platform Launch verwenden, stellen Sie sicher, dass das Trackerobjekt global verfügbar ist. Siehe [Adobe Analytics Extension-Übersicht](https://docs.adobe.com/content/help/de-DE/launch/using/extensions-ref/adobe-extension/analytics-extension/overview.html) im Benutzerhandbuch zum Starten.

>!![CAUTION]
Vermeiden Sie, AppMeasurement-Bibliotheken sowohl auf einer übergeordneten Seite als auch auf einem iframe zu verwenden. Dadurch entstehen Risiken beim Senden mehrerer Bildanforderungen, wodurch die Anzahl der Berichte steigt und die Anzahl der gebührenpflichtigen Serveraufrufe steigt.

## Zugriff auf AppMeasurement, das sich in einem iframe befindet

Sie können über das iframe-Objekt auf AppMeasurement-Variablen zugreifen. In diesen Beispielen wird [pageName](../vars/page-vars/pagename.md) festgelegt und die [t()-Methode](../vars/functions/t-method.md) mit zwei verschiedenen Methoden aufgerufen, um auf das iframe-Objekt zu verweisen.

```js
// Reference AppMeasurement code that resides within an iframe and send an image request
document.getElementById('targetFrame').contentWindow.s.pageName="Page name within iframe";
document.getElementById('targetFrame').contentWindow.s.t();

// An alternate method to the above if there's only one iframe on the page
window.frames[0].contentWindow.s.pageName = "Page name within iframe";
window.frames[0].contentWindow.s.t();
```

## Zugriff auf AppMeasurement von innerhalb eines iframe

Sie können von einem iframe aus auf AppMeasurement-Variablen auf einer übergeordneten Seite zugreifen. In diesem Beispiel wird [pageName](../vars/page-vars/pagename.md) festgelegt und die [t()-Methode](../vars/functions/t-method.md) mit der [`parent`](https://www.w3schools.com/jsref/prop_win_parent.asp) Eigenschaft aufgerufen.

```js
// Reference AppMeasurement code on a parent page from within an iframe and send an image request
parent.s.pageName = "Page Name on Hosted Window";
parent.s.t();
```

## Verwenden `postMessage` und Ereignis-Listener

Alternativ können Sie Variablen mit `postMessage` und mit Ereignis-Listenern festlegen. Für diese Methode ist kein direkter Verweis auf einen iframe erforderlich.

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

* Wie bei anderen JavaScript-Codes können iframes nur dann kommunizieren, wenn Domänen und Protokolle übereinstimmen. Diese Beispiele funktionieren nicht, wenn sich der iframe-Inhalt in einer anderen Domäne als die übergeordnete Domäne befindet.
* Wenn sich AppMeasurement in einem iframe befindet, wird die [`referrer`](../vars/page-vars/referrer.md) Variable auf die übergeordnete URL und nicht auf die tatsächliche verweisende URL eingestellt. Sie können die `referrer` Variable manuell einstellen, um dieses Problem zu beheben.
* Der [Adobe Experience Cloud-Debugger](https://docs.adobe.com/content/help/de-DE/debugger/using/experience-cloud-debugger.html) erkennt keine Bildanforderungen, die innerhalb von iframes ausgelöst werden.
* Activity Map zeigt die Heatmap nicht über Links an, die innerhalb von iframes angeklickt wurden. Stattdessen wird der gesamte iframe hervorgehoben.
