---
description: Wenn Pathing-Informationen nicht erfasst und in Berichten angezeigt werden, finden Sie hier eine Liste der möglichen Ursachen.
keywords: Analytics-Implementierung
seo-description: Wenn Pathing-Informationen nicht erfasst und in Berichten angezeigt werden, finden Sie hier eine Liste der möglichen Ursachen.
seo-title: Ursachen dafür, warum Pfade möglicherweise nicht erfasst werden
solution: Analytics
title: Ursachen dafür, warum Pfade möglicherweise nicht erfasst werden
topic: Entwickler und Implementierung
uuid: 9985b7f7-75ea-4c94-97a3-520f92630989
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Ursachen dafür, warum Pfade möglicherweise nicht erfasst werden

Wenn Pathing-Informationen nicht erfasst und in Berichten angezeigt werden, finden Sie hier eine Liste der möglichen Ursachen.

* Das Pathing-Feature wurde für die jeweilige Eigenschaft in der Report Suite nicht aktiviert. Die Aktivierung erfolgt pro Report Suite.
* Daten werden nicht in die richtige Eigenschaft weitergegeben.
* Das Pathing-Feature wurde aktiviert und die Daten sind in der Eigenschaft vorhanden, werden jedoch nicht in den Berichten angezeigt. Während die [!UICONTROL sprop]-Daten innerhalb von 10 Minuten sichtbar sind, werden die Pathing-Daten erst nach Abschluss der Sitzung des Besuchers angezeigt. Die Sitzung endet nach einem Zeitraum von 30 Minuten ohne Aktivitäten. Analytics benötigt dann weitere 10 Minuten, um die Verarbeitung der Pfaddaten für die endgültige Anzeige in Berichten abzuschließen.

Wenn Sie diese Punkte alle überprüft haben und trotzdem noch keine Daten sichtbar sind, wenden Sie sich zur weiteren Fehlersuche an den Kundendienst.
