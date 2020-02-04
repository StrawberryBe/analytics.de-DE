---
title: Konfigurationsvariablen
description: Verwenden Sie Konfigurationsvariablen, um festzustellen, wie Daten erfasst werden.
translation-type: tm+mt
source-git-commit: e9a876a1f562333056387d63de46a9cfe3fb3939

---


# Konfigurationsvariablen-Übersicht

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Sie enthalten normalerweise keine Dimensions- oder Metrikwerte.

## Konfigurationsvariablen festlegen

Bei JavaScript-Implementierungen mit `AppMeasurement.js`werden Konfigurationsvariablen normalerweise oben in der JS-Datei festgelegt.

Bei Implementierungen mit Adobe Experience Platform Launch werden Konfigurationsvariablen normalerweise durch Konfigurieren der Adobe Analytics-Erweiterung gefunden:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die Eigenschaft, die Sie bearbeiten möchten.
3. Click the [!UICONTROL Extensions] tab, then Click [!UICONTROL Configure] under Adobe Analytics.

> [!IMPORTANT] Stellen Sie sicher, dass alle Konfigurationsvariablen festgelegt sind, bevor Sie eine Verfolgungsfunktion (`t()` oder `tl()`) aufrufen. Vermeiden Sie das Festlegen von Konfigurationsvariablen in der `doPlugins()` Funktion.
