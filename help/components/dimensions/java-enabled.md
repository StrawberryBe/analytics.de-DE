---
title: Java aktiviert
description: Stellt fest, ob Java im Browser aktiviert ist.
translation-type: tm+mt
source-git-commit: 226c54b782651ea8c6f4b7bb8030a1513c440a1d
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 1%

---


# Java aktiviert

Die Dimension &quot;Java aktiviert&quot;bestimmt, ob Java im Browser aktiviert ist. Es ist hilfreich, wenn Sie Java-basierte Funktionen auf Ihrer Site einführen und wissen möchten, wie viele Besucher Java bereits aktiviert haben. Für diejenigen, die Java deaktiviert haben, können Sie eine Alternative oder Anweisungen zur Aktivierung bereitstellen.

## Diese Dimension mit Daten füllen

Diese Dimension ruft Daten aus der [`v` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen ab. AppMeasurement erfasst diese Daten, indem es erkennt, ob Java im Browser aktiviert ist. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), funktioniert diese Dimension standardmäßig. Wenn Sie eine Datenerfassungsmethode außerhalb von AppMeasurement verwenden (z. B. über die API), stellen Sie sicher, dass Sie den Parameter `v` für die Zeichenfolge mit &quot;Y&quot;oder &quot;N&quot;einschließen, wenn Sie diese Dimension verwenden möchten.

## Dimensionswerte

Zu den Dimensionswerten gehören &quot;Aktiviert&quot;, &quot;Deaktiviert&quot;und &quot;Unbekannt&quot;.

* **Aktiviert**: Java ist im Browser aktiviert. Die `v` Abfrage-Zeichenfolge enthielt den Wert &quot;Y&quot;.
* **Deaktiviert**: Java ist im Browser deaktiviert oder unterstützt Java anderweitig nicht. Die `v` Abfrage-Zeichenfolge enthielt den Wert &quot;N&quot;.
* **Unbekannt**: AppMeasurement konnte die Java-Unterstützung nicht ermitteln. Die `v` Abfrage-Zeichenfolge war in der Bildanforderung nicht vorhanden.
