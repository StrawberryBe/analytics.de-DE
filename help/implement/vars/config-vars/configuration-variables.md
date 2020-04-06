---
title: Konfigurationsvariablen
description: Verwenden Sie Konfigurationsvariablen, um festzustellen, wie Daten erfasst werden.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Sie enthalten normalerweise keine Dimensions- oder Metrikwerte.

## Festlegen von Konfigurationsvariablen

Bei JavaScript-Implementierungen mit `AppMeasurement.js` werden die Konfigurationsvariablen normalerweise oben in der JS-Datei festgelegt.

Bei Implementierungen mit Adobe Experience Platform Launch werden die Konfigurationsvariablen normalerweise durch die Konfiguration der Adobe Analytics-Erweiterung gefunden:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die Eigenschaft, die Sie bearbeiten möchten.
3. Click the [!UICONTROL Extensions] tab, then Click [!UICONTROL Configure] under Adobe Analytics.

>[!IMPORTANT] Vergewissern Sie sich, dass alle Konfigurationsvariablen festgelegt sind, bevor Sie eine Verfolgungsmethode ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) aufrufen. Vermeiden Sie das Festlegen von Konfigurationsvariablen in der [`doPlugins()`](../functions/doplugins.md)-Funktion.
