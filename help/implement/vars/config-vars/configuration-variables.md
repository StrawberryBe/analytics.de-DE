---
title: Konfigurationsvariablen
description: Verwenden Sie Konfigurationsvariablen, um festzustellen, wie Daten erfasst werden.
exl-id: 3f017a94-b71d-47da-8ab4-daf32475ed34
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '125'
ht-degree: 100%

---

# Übersicht über Konfigurationsvariablen

Konfigurationsvariablen bestimmen darüber, wie Daten bei der Berichterstellung erfasst und verarbeitet werden. Sie enthalten normalerweise keine Dimensions- oder Metrikwerte.

## Festlegen von Konfigurationsvariablen

Bei JavaScript-Implementierungen mit `AppMeasurement.js` werden die Konfigurationsvariablen normalerweise oben in der JS-Datei festgelegt.

Bei Implementierungen, bei denen Adobe Experience Platform-Tags verwendet werden, werden die Konfigurationsvariablen normalerweise durch die Konfiguration der Adobe Analytics-Erweiterung gefunden:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
1. Klicken Sie auf die Eigenschaft, die Sie bearbeiten möchten.
1. Klicken Sie auf die Registerkarte [!UICONTROL Erweiterungen] und dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].

>[!IMPORTANT]
>
>Stellen Sie sicher, dass alle Konfigurationsvariablen festgelegt sind, bevor Sie eine Tracking-Methode ([`t()`](../functions/t-method.md) oder [`tl()`](../functions/tl-method.md)) aufrufen. Vermeiden Sie das Festlegen von Konfigurationsvariablen in der [`doPlugins()`](../functions/doplugins.md)-Funktion.
