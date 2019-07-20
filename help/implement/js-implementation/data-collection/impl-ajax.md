---
description: Das Implementieren mit AJAX entspricht genau dem Bereitstellen von Code auf einer normalen HTML-Seite.
keywords: Analytics-Implementierung
seo-description: Das Implementieren mit AJAX entspricht genau dem Bereitstellen von Code auf einer normalen HTML-Seite.
seo-title: Implementieren mit AJAX
solution: Analytics
title: Implementieren mit AJAX
topic: Entwickler und Implementierung
uuid: 9 e 3477 ef -7 dea -4 c 76-ab 61-36 a 188222 be 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Implementieren mit AJAX

Das Implementieren mit AJAX entspricht genau dem Bereitstellen von Code auf einer normalen HTML-Seite.

Das Unternehmen hat Fragen, die beantwortet werden müssen, die erforderlichen Punkte werden festgelegt und Variablen werden zugewiesen. Anschließend wird das Design vorgenommen und bereitgestellt. Mit diesen Begriffen sollten Sie vertraut sein, wenn Sie schon die ersten Schritte bei der Implementierung absolviert haben.

## Entwerfen der Lösung {#section_78F1C7AFBB4E4175A6FE04A962C9C9D0}

Wenn bei dieser Mischung [!UICONTROL AJAX] ins Spiel kommt, muss zuerst in Erfahrung gebracht werden, wie detailliert die zu erfassenden Daten sein sollen. Welche Variablen festgelegt werden müssen und nach welcher Methode die Daten am besten an Adobe übermittelt werden, hängt davon ab, ob sich die Inhalte auf der Seite ändern (Makroebene) oder ob Attribute der Anwendung nachverfolgt werden sollen (Mikroebene).

## Bereitstellen des Codes {#section_F3FC6F07A3E148D89A4C9ABC442920C3}

Es gibt zwei Funktion im JavaScript-Code, mit denen Sie Daten senden können. Für die Auswahl der richtigen Methode gibt es bestimmte Leitlinien, an denen man sich orientieren sollte.
Wenn davor eine Bildanforderung für die gleiche Seite erfolgt ist, müssen Sie zuvor die Werte der zuvor festgelegten Variablen löschen. Use the `clearVars()` funtion in [!DNL AppMeasurement] for JavaScript, or write a simple JavaScript function to clear the variables if you are using H code. Set the values appropriate for the changed content, namely the *`pageName`* variable. After the variables are set call the *`t()`* function.

>[!NOTE]
>
>Before you call `s.t()`, you must clear any values on the s object that you do not want to persist. if you are using [!DNL AppMeasurement] for JavaScript, you can call `s.clearVars()`. Wenn Sie H-Code verwenden, schreiben Sie eine einfache Routine, mit der Variablen auf eine leere Zeichenfolge gesetzt werden.

```js
s.clearVars(); 
s.pageName="New Page" 
s.prop1="some value" 
void(s.t());
```

The following example shows a tracking call in the `done` callback of the JQuery `.ajax` function:

```
$.ajax({ 
  url: "test.html", 
  dataType: "html" 
}) 
  .done(function( response ) { 
    $( "#content" ).html( response ); 
  s.clearVars(); 
  s.pageName = $( "h1:first" ).text(); 
  s.t(); 
  }); 
```

Wenn davor eine Bildanforderung für die gleiche Seite erfolgte, löschen Sie die Werte der zuvor festgelegten Variablen. Dazu haben Sie die folgenden Möglichkeiten:

* Schreiben Sie eine einfache JavaScript-Funktion zum Löschen der Adobe-Variablen.
* Legen Sie die Variablen *`linkTrackVars`* und *`linkTrackEvents`* Variablen, wenn Sie sie noch nicht in der [!DNL s_code.js] Datei vorgenommen haben.

* Set the values appropriate for the changed content, namely the *`pageName`* variable.
* After the variables are set, call the *`tl()`* function.

```js
//set linkTrackVars and linkTrackEvents> (if applicable) 
//set new variables 
s.tl(this,'o','Link Name');
```

```js
s.linkTrackVars="prop1,eVar1,events"; s.linkTrackEvents="event1"; 
s.prop1="some value"; s.eVar1="another value"; s.events="event1"; 
s.tl(this,'o','My Link Name');
```

