---
title: Java aktiviert
description: Bestimmt, ob Java im Browser aktiviert ist.
feature: Dimensions
exl-id: 2d4b4ea2-65ba-4d39-a040-f989b5eddc6e
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 100%

---

# Java aktiviert

Die Dimension „Java aktiviert“ bestimmt, ob Java zu diesem Zeitpunkt im Browser aktiviert ist. Das ist hilfreich, wenn Sie Java-basierte Funktionen auf Ihrer Site einführen und wissen möchten, wie viele Besucher Java bereits aktiviert haben. Für diejenigen, die Java deaktiviert haben, können Sie eine Alternative oder Anweisungen zur Aktivierung bereitstellen.

## Füllen dieser Dimension mit Daten

Diese Dimension ruft Daten aus der [`v` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten, indem erkennt wird, ob Java im Browser aktiviert ist. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Abfragezeichenfolgenparameter `v` mit „Y“ oder „N“ einschließen, wenn Sie diese Dimension verwenden möchten.

## Dimensionselemente

Zu den Dimensionselementen gehören „Aktiviert“, „Deaktiviert“ und „Nicht bekannt“.

* **Aktiviert**: Java ist im Browser aktiviert. Die Abfragezeichenfolge `v` enthielt den Wert „Y“.
* **Deaktiviert**: Java ist im Browser deaktiviert oder unterstützt Java anderweitig nicht. Die Abfragezeichenfolge `v` enthielt den Wert „N“.
* **Nicht bekannt**: AppMeasurement konnte die Java-Unterstützung nicht ermitteln. Die Abfragezeichenfolge `v` war in der Bildanforderung nicht vorhanden.
