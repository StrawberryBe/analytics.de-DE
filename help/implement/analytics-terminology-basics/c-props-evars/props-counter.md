---
description: Zähler dienen zur Speicherung (und manchmal auch Anzeige) einer Zahl, die angibt, wie oft ein bestimmtes Ereignis oder ein bestimmter Vorgang eingetreten ist.
keywords: Analytics Implementation;props;s.prop;custom traffic;counters
title: Verwenden von Eigenschaften als Zähler
topic: Developer and implementation
uuid: ab83bd7e-10d9-49f9-b9e7-c50397e95c17
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Verwenden von Eigenschaften als Zähler

Zähler dienen zur Speicherung (und manchmal auch Anzeige) einer Zahl, die angibt, wie oft ein bestimmtes Ereignis oder ein bestimmter Vorgang eingetreten ist.

Sie können eine Eigenschaftsvariable verwenden, um zu zählen, wie oft ein Ereignis eintritt. So können Sie zum Beispiel verfolgen, wie oft auf Ihrer Site der Real Player im Vergleich zum Windows Media Player eingesetzt wird. Jede Seite enthält [!UICONTROL Einfügecode], in dem [!UICONTROL s.prop]-Variablen stehen. Verwenden Sie [!UICONTROL s.prop]1 zur Verfolgung der Player. Geben Sie für die Seite A einen Wert in [!UICONTROL s.prop]1 ein, der für „Real Player“ stehen soll.

```js
s.prop1="RealPlayer"
```

Geben Sie für die Seite B einen ähnlichen Wert in [!UICONTROL s.prop]1 ein, der für „Windows Media Player“ stehen soll:

```js
s.prop1="WindowsMP"
```

> [!NOTE] Adobe bietet Ihnen bis zu 75 [!UICONTROL s.prop]-Variablen an, die Sie nutzen können.

Wenn Besucher Ihre Site betreten und die Seiten anzeigen, auf denen sich der Real Player bzw. Windows Media Player befinden, kann [!DNL Analytics] die Benutzer anhand der besuchten Seiten aufteilen. Im Bericht [!UICONTROL Benutzerspezifischer Traffic] wird dann angezeigt, wie viele Besuche auf jeder Seite verzeichnet wurden.

> [!NOTE] Der Name des Berichts [!UICONTROL Benutzerspezifischer Traffic] kann angepasst werden. So können Sie ihn zum Beispiel in [!UICONTROL Bericht zu den Player-Typen] umbenennen.

