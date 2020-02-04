---
title: Implementieren mit AJAX
description: Erfahren Sie, wie Sie Adobe Analytics mit AJAX auf einer Site implementieren.
translation-type: tm+mt
source-git-commit: 0439440e10dddf8a5d64e4ea8f9868b521e5ca20

---


# Implementieren mit AJAX

Bei AJAX werden JavaScript und HTML verwendet, um Inhalte zu löschen und zu generieren, ohne eine neue Seite zu laden.

Adobe Analytics verlässt sich normalerweise darauf, dass Seiten neu geladen werden, um das Analytics-Verfolgungsobjekt zurückzusetzen. Jedes Mal, wenn Sie zu einer anderen URL navigieren, werden alle Analytics-Variablen zurückgesetzt und können erneut definiert werden. Wenn Sie AJAX auf Ihrer Site verwenden, passen Sie Ihre Implementierung an, um zu vermeiden, dass die Seite aktualisiert wird, um sicherzustellen, dass die Daten nicht fälschlicherweise zwischen den Treffern beibehalten werden.

Sobald Sie über Maßnahmen zum Löschen von Variablenwerten verfügen, ist die Implementierung von Adobe Analytics auf Sites, die AJAX verwenden, im Wesentlichen mit anderen Implementierungsmethoden identisch.

## Festlegen von Interaktionen und Treffertypen

Da Seiten, die AJAX verwenden, in der Regel nicht neu geladen werden, gibt es mehrere Interaktionen, die ein Benutzer auf Ihrer Site ausführen kann. Achten Sie bei der Implementierung von Adobe Analytics darauf, Seitenansichten von Linktracking-Aufrufen zu unterscheiden. Berücksichtigen Sie die folgende Frage für jede Interaktion, die ein Benutzer auf Ihrer Site ausführen kann:

*Ändert sich diese Interaktion, wenn ein Benutzer mit meiner Site interagiert, genug Inhalt auf der Seite, um als neue Seite zu gelten?*

* Wenn die Antwort **ja** ist, sollten Sie einen Seitenansichtsverfolgungsaufruf (`s.t()`) verwenden.
* Wenn die Antwort **nein** ist, sollten Sie diese Interaktion mit einem Link-Verfolgungsaufruf (`s.tl()`) verfolgen.

> [!NOTE] Nicht alle Interaktionen oder Klicks müssen aufgezeichnet werden. Achten Sie sorgfältig darauf, welche Aktionen am wichtigsten sind, um sie zu verfolgen, und senden Sie Daten entsprechend an Adobe.

## Variablen auf jeder Seite löschen

Variablenwerte bleiben auf Seiten mit AJAX erhalten, da die Seite nicht neu geladen wird. Daher sind spezielle Vorkehrungen erforderlich, um Variablenwerte zu löschen, damit sie nicht fälschlicherweise über Treffer hinweg bestehen bleiben. Adobe bietet die [`clearVars`](../vars/functions/clearvars.md) Funktion zum einfachen Löschen von Variablenwerten. Stellen Sie sicher, dass Sie diese Funktion verwenden, nachdem Sie jeden Treffer an Adobe gesendet haben und bevor Sie Variablenwerte für den nächsten Treffer festlegen.

> [!TIP] Die `clearVars()` Funktion ist in H-Code nicht verfügbar. Wenn Sie noch nicht auf AppMeasurement aktualisiert haben, setzen Sie jeden Analytics-Variablenwert auf eine leere Zeichenfolge.

## Beispiele

Im folgenden Beispiel wird einfaches JavaScript verwendet, um vorhandene Variablenwerte zu löschen, neue Werte festzulegen und dann eine Bildanforderung an Adobe zu senden:

```js
s.clearVars();
s.pageName = "Example AJAX page";
s.eVar1="Example value";
void(s.t());
```

In dem folgenden Beispiel wird ein Tracking-Aufruf im Callback `done` der JQuery-`.ajax`-Funktion veranschaulicht:

```js
$.ajax({
  url: "example.html",
  dataType: "html"
})
  .done(function( response ) {
    $( "#content" ).html( response );
  s.clearVars();
  s.pageName = $( "h1:first" ).text();
  s.t();
  });
```
