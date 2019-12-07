---
description: Das Implementieren mit AJAX entspricht genau dem Bereitstellen von Code auf einer normalen HTML-Seite.
keywords: Analytics Implementation
title: Implementieren mit AJAX
topic: Developer and implementation
uuid: 9e3477ef-7dea-4c76-ab61-36a188222be7
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Implementieren mit AJAX

Das Implementieren mit AJAX entspricht genau dem Bereitstellen von Code auf einer normalen HTML-Seite.

Das Unternehmen hat Fragen, die beantwortet werden müssen, die erforderlichen Punkte werden festgelegt und Variablen werden zugewiesen. Anschließend wird das Design vorgenommen und bereitgestellt. Mit diesen Begriffen sollten Sie vertraut sein, wenn Sie schon die ersten Schritte bei der Implementierung absolviert haben.

## Entwerfen der Lösung {#section_78F1C7AFBB4E4175A6FE04A962C9C9D0}

Wenn bei dieser Mischung [!UICONTROL AJAX] ins Spiel kommt, muss zuerst in Erfahrung gebracht werden, wie detailliert die zu erfassenden Daten sein sollen. Welche Variablen festgelegt werden müssen und nach welcher Methode die Daten am besten an Adobe übermittelt werden, hängt davon ab, ob sich die Inhalte auf der Seite ändern (Makroebene) oder ob Attribute der Anwendung nachverfolgt werden sollen (Mikroebene).

## Bereitstellen des Codes {#section_F3FC6F07A3E148D89A4C9ABC442920C3}

Es gibt zwei Funktion im JavaScript-Code, mit denen Sie Daten senden können. Für die Auswahl der richtigen Methode gibt es bestimmte Leitlinien, an denen man sich orientieren sollte.
Wenn davor eine Bildanforderung für die gleiche Seite erfolgt ist, müssen Sie zuvor die Werte der zuvor festgelegten Variablen löschen. Verwenden Sie die Funktion `clearVars()` in [!DNL AppMeasurement] für JavaScript oder schreiben Sie eine einfache JavaScript-Funktion zum Löschen der Variablen, wenn Sie H-Code verwenden. Stellen Sie die für den geänderten Inhalt geeigneten Werte ein, nämlich die Variable *`pageName`*. Nachdem die Variablen gesetzt sind, rufen Sie die Funktion *`t()`* auf.

> [!NOTE] Bevor Sie `s.t()` aufrufen, müssen Sie alle Werte des Objekts „s“ löschen, die nicht bestehen bleiben sollen. Wenn Sie [!DNL AppMeasurement] für JavaScript verwenden, können Sie `s.clearVars()` aufrufen. Wenn Sie H-Code verwenden, schreiben Sie eine einfache Routine, mit der Variablen auf eine leere Zeichenfolge gesetzt werden.

```js
s.clearVars(); 
s.pageName="New Page" 
s.prop1="some value" 
void(s.t());
```

In dem folgenden Beispiel wird ein Tracking-Aufruf im Callback `done` der JQuery-`.ajax`-Funktion veranschaulicht:

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
* Legen Sie die Variablen *`linkTrackVars`* und *`linkTrackEvents`* fest, falls Sie dies nicht schon in der [!DNL s_code.js]-Datei vorgenommen haben.

* Stellen Sie die für den geänderten Inhalt geeigneten Werte ein, nämlich die Variable *`pageName`*.
* Nachdem die Variablen gesetzt sind, rufen Sie die Funktion *`tl()`* auf.

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

