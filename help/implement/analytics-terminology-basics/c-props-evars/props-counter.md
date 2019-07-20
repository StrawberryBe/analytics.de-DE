---
description: Zähler dienen zur Speicherung (und manchmal auch Anzeige) einer Zahl, die angibt, wie oft ein bestimmtes Ereignis oder ein bestimmter Vorgang eingetreten ist.
keywords: Analytics-Implementierung; props; s. prop; custom traffic; Zähler
seo-description: Zähler dienen zur Speicherung (und manchmal auch Anzeige) einer Zahl, die angibt, wie oft ein bestimmtes Ereignis oder ein bestimmter Vorgang eingetreten ist.
seo-title: Props als Zähler verwenden
solution: Analytics
title: Props als Zähler verwenden
topic: Entwickler und Implementierung
uuid: ab 83 bd 7 e -10 d 9-49 f 9-b 9 e 7-c 50397 e 95 c 17
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Props als Zähler verwenden

Zähler dienen zur Speicherung (und manchmal auch Anzeige) einer Zahl, die angibt, wie oft ein bestimmtes Ereignis oder ein bestimmter Vorgang eingetreten ist.

Sie können eine Eigenschaftsvariable verwenden, um zu zählen, wie oft ein Ereignis eintritt. So können Sie zum Beispiel verfolgen, wie oft auf Ihrer Site der Real Player im Vergleich zum Windows Media Player eingesetzt wird. Jede Seite enthält [!UICONTROL Einfügecode], in dem [!UICONTROL s.prop]-Variablen stehen. Verwenden Sie [!UICONTROL s.prop]1 zur Verfolgung der Player. Geben Sie für die Seite A einen Wert in [!UICONTROL s.prop]1 ein, der für „Real Player“ stehen soll.

```js
s.prop1="RealPlayer"
```

Geben Sie für die Seite B einen ähnlichen Wert in [!UICONTROL s.prop]1 ein, der für „Windows Media Player“ stehen soll:

```js
s.prop1="WindowsMP"
```

>[!NOTE]
>
>Adobe offers up to 75 [!UICONTROL s.prop] variables for you to use.

Wenn Besucher Ihre Site betreten und die Seiten anzeigen, auf denen sich der Real Player bzw. Windows Media Player befinden, kann [!DNL Analytics] die Benutzer anhand der besuchten Seiten aufteilen. Im Bericht [!UICONTROL Benutzerspezifischer Traffic] wird dann angezeigt, wie viele Besuche auf jeder Seite verzeichnet wurden.

>[!NOTE]
>
>The name of the [!UICONTROL Custom Traffic] report can be customized. So können Sie ihn zum Beispiel in [!UICONTROL Bericht zu den Player-Typen] umbenennen.

