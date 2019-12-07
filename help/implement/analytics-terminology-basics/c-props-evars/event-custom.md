---
description: Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.
keywords: Analytics Implementation;custom event
title: Was ist ein benutzerspezifisches Ereignis?
topic: Developer and implementation
uuid: 8e78ba04-9b4c-4566-980c-c24dd9d82236
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Was ist ein benutzerspezifisches Ereignis?

Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.

Sie funktionieren ähnlich wie [!UICONTROL vordefinierte] Ereignisse, allerdings können Sie mit [!UICONTROL benutzerspezifischen] Ereignissen Ihre eigenen Erfolgsmetriken selbst festlegen. So wäre zum Beispiel bei einem eigenen Newsletter eine _Registrierung_ ein Erfolgsereignis. Solch eine _Registrierung_ ist in den [!UICONTROL vordefinierten] Ereignissen nicht enthalten. Mithilfe eines [!UICONTROL benutzerspezifischen] Ereignisses können Sie nachverfolgen, wie viele Besucher sich für Ihren Newsletter registrieren. Die Standardsyntax von [!UICONTROL benutzerspezifischen] Ereignissen sieht wie folgt aus:

```js
s.events="event3"
```

Dieser Code zeigt, wie ein Ereignis der _Ereignisvariable_ zugewiesen wird. Wenn Sie den Ereignisnamen nicht ändern, würde in der Oberfläche _event3_ angezeigt werden.

In der Standardeinstellung werden Erfolgsereignisse als _Zählerereignisse_ konfiguriert. Zählerereignisse zählen einfach nur, wie oft ein Erfolgsereignis eintritt. In manchen Fällen soll dabei ein Ereignis um einen benutzerdefinierten Betrag erhöht werden. Solche Ereignisse können entweder als _numerische_ oder als _Währungs_-Ereignisse festgelegt werden. Den Ereignistyp können Sie in der Admin Console ändern.
