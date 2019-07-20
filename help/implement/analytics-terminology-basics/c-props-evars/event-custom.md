---
description: Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.
keywords: Analytics-Implementierung; benutzerspezifisches Ereignis
seo-description: Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.
seo-title: Was ist ein benutzerspezifisches Ereignis?
solution: Analytics
title: Was ist ein benutzerspezifisches Ereignis?
topic: Entwickler und Implementierung
uuid: 8 e 78 ba 04-9 b 4 c -4566-980 c-c 24 dd 9 d 82236
translation-type: tm+mt
source-git-commit: d7056c233e784a073c75c55f396ff43c9e0d1c71

---


# Was ist ein benutzerspezifisches Ereignis?

Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.

Sie funktionieren ähnlich wie [!UICONTROL vordefinierte] Ereignisse, allerdings können Sie mit [!UICONTROL benutzerspezifischen] Ereignissen Ihre eigenen Erfolgsmetriken selbst festlegen. For example, if you have a newsletter, your success event could be _Registration_. _Die Registrierung_ ist nicht Teil der [!UICONTROL vordefinierten] Ereignisse. Mithilfe eines [!UICONTROL benutzerspezifischen] Ereignisses können Sie nachverfolgen, wie viele Besucher sich für Ihren Newsletter registrieren. Die Standardsyntax von [!UICONTROL benutzerspezifischen] Ereignissen sieht wie folgt aus:

```js
s.events="event3"
```

Dieser Code zeigt, wie ein Ereignis zur Variablen _Ereignisvariablen_ . If you do not modify the event name in the interface, _event3_ would display in the interface.

In der Standardeinstellung werden Erfolgsereignisse als _Zählerereignisse_ konfiguriert. Zählerereignisse zählen einfach nur, wie oft ein Erfolgsereignis eintritt. Bei einigen Erfolgsereignissen wird ein Ereignis um einen benutzerdefinierten Betrag erhöht. These events can be set either as _numeric_ events or _currency_ events. Sie können den Ereignistyp in der Admin-Konsole ändern.
