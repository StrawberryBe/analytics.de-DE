---
description: Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.
keywords: Analytics-Implementierung;benutzerspezifisches Ereignis
seo-description: Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.
seo-title: Was ist ein benutzerspezifisches Ereignis?
solution: Analytics
title: Was ist ein benutzerspezifisches Ereignis?
topic: Entwickler und Implementierung
uuid: 8e78ba04-9b4c-4566-980c-c24dd9d82236
translation-type: ht
source-git-commit: d7056c233e784a073c75c55f396ff43c9e0d1c71

---


# Was ist ein benutzerspezifisches Ereignis?

Mit benutzerspezifischen Ereignissen können Sie den Typ von Erfolg festlegen, den Sie verfolgen lassen möchten.

Sie funktionieren ähnlich wie [!UICONTROL vordefinierte] Ereignisse, allerdings können Sie mit [!UICONTROL benutzerspezifischen] Ereignissen Ihre eigenen Erfolgsmetriken selbst festlegen. So wäre zum Beispiel bei einem eigenen Newsletter eine _Registrierung_ ein Erfolgsereignis. Solch eine _Registrierung_ ist in den [!UICONTROL vordefinierten] Ereignissen nicht enthalten. Mithilfe eines [!UICONTROL benutzerspezifischen] Ereignisses können Sie nachverfolgen, wie viele Besucher sich für Ihren Newsletter registrieren. Die Standardsyntax von [!UICONTROL benutzerspezifischen] Ereignissen sieht wie folgt aus:

```js
s.events="event3"
```

Dieser Code zeigt, wie ein Ereignis der _Ereignisvariable_ zugewiesen wird. Wenn Sie den Ereignisnamen nicht ändern, würde in der Oberfläche _event3_ angezeigt werden.

In der Standardeinstellung werden Erfolgsereignisse als _Zählerereignisse_ konfiguriert. Zählerereignisse zählen einfach nur, wie oft ein Erfolgsereignis eintritt. In manchen Fällen soll dabei ein Ereignis um einen benutzerdefinierten Betrag erhöht werden. Solche Ereignisse können entweder als _numerische_ oder als _Währungs_-Ereignisse festgelegt werden. Den Ereignistyp können Sie in der Admin Console ändern.
