---
title: Konfigurationsvariablen
description: Verwenden Sie Konfigurationsvariablen, um festzustellen, wie Daten erfasst werden.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '123'
ht-degree: 100%

---


# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Sie enthalten normalerweise keine Dimensions- oder Metrikwerte.

## Festlegen von Konfigurationsvariablen

Bei JavaScript-Implementierungen mit `AppMeasurement.js` werden die Konfigurationsvariablen normalerweise oben in der JS-Datei festgelegt.

Bei Implementierungen mit Adobe Experience Platform Launch werden die Konfigurationsvariablen normalerweise durch die Konfiguration der Adobe Analytics-Erweiterung gefunden:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die Eigenschaft, die Sie bearbeiten möchten.
3. Klicken Sie auf die Registerkarte [!UICONTROL Erweiterungen] und dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].

>[!IMPORTANT]
>
>Stellen Sie sicher, dass alle Konfigurationsvariablen festgelegt sind, bevor Sie eine Tracking-Methode ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) aufrufen. Vermeiden Sie das Festlegen von Konfigurationsvariablen in der [`doPlugins()`](../functions/doplugins.md)-Funktion.
