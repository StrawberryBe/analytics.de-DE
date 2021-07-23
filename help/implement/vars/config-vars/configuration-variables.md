---
title: Konfigurationsvariablen
description: Verwenden Sie Konfigurationsvariablen, um festzustellen, wie Daten erfasst werden.
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 64%

---

# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Sie enthalten normalerweise keine Dimensions- oder Metrikwerte.

## Festlegen von Konfigurationsvariablen

Bei JavaScript-Implementierungen mit `AppMeasurement.js` werden die Konfigurationsvariablen normalerweise oben in der JS-Datei festgelegt.

Bei Implementierungen mit Adobe Experience Platform-Tags werden Konfigurationsvariablen normalerweise durch Konfigurieren der Adobe Analytics-Erweiterung gefunden:

1. Gehen Sie zu `experience.adobe.com` und melden Sie sich bei entsprechender Aufforderung an.
1. Wählen Sie [!UICONTROL Launch/Data Collection] aus.
1. Klicken Sie auf [!UICONTROL Gehen Sie zu Launch/Data Collection] und wählen Sie [!UICONTROL Tags] aus.
1. Klicken Sie auf die Eigenschaft, die Sie bearbeiten möchten.
1. Klicken Sie auf die Registerkarte [!UICONTROL Erweiterungen] und dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].

>[!IMPORTANT]
>
>Stellen Sie sicher, dass alle Konfigurationsvariablen festgelegt sind, bevor Sie eine Tracking-Methode ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) aufrufen. Vermeiden Sie das Festlegen von Konfigurationsvariablen in der [`doPlugins()`](../functions/doplugins.md)-Funktion.
