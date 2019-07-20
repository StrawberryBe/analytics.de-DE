---
description: Wenn Pathing-Informationen nicht erfasst und in Berichten angezeigt werden, finden Sie hier eine Liste der möglichen Ursachen.
keywords: Analytics-Implementierung
seo-description: Wenn Pathing-Informationen nicht erfasst und in Berichten angezeigt werden, finden Sie hier eine Liste der möglichen Ursachen.
seo-title: Mögliche Ursachen für die Pfadsetzung
solution: Analytics
title: Mögliche Ursachen für die Pfadsetzung
topic: Entwickler und Implementierung
uuid: 9985 b 7 f 7-75 ea -4 c 94-97 a 3-520 f 92630989
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# Mögliche Ursachen für die Pfadsetzung

Wenn Pathing-Informationen nicht erfasst und in Berichten angezeigt werden, finden Sie hier eine Liste der möglichen Ursachen.

* Das Pathing-Feature wurde für die jeweilige Eigenschaft in der Report Suite nicht aktiviert. Die Aktivierung erfolgt pro Report Suite.
* Daten werden nicht in die richtige Eigenschaft weitergegeben.
* Das Pathing-Feature wurde aktiviert und die Daten sind in der Eigenschaft vorhanden, werden jedoch nicht in den Berichten angezeigt. Während die [!UICONTROL sprop]-Daten innerhalb von 10 Minuten sichtbar sind, werden die Pathing-Daten erst nach Abschluss der Sitzung des Besuchers angezeigt. Die Sitzung endet nach einem Zeitraum von 30 Minuten ohne Aktivitäten. Analytics benötigt dann weitere 10 Minuten, um die Verarbeitung der Pfaddaten für die endgültige Anzeige in Berichten abzuschließen.

Wenn Sie diese Punkte alle überprüft haben und trotzdem noch keine Daten sichtbar sind, wenden Sie sich zur weiteren Fehlersuche an den Kundendienst.
