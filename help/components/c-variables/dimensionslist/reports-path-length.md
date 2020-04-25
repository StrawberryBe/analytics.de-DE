---
description: Zeigt die Tiefe der einzelnen Besuche auf Ihrer Website nach Prozentsatz und Gesamtanzahl an. Anders ausgedrückt zeigt der Bericht, wie viele Seiten der Besucher in der Regel zur Ansicht aufruft, bevor er die Site verlässt.
title: Path Length
topic: Reports
uuid: f1c29e78-279a-46a5-b758-d4f0da629239
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Path Length

Zeigt die Tiefe der einzelnen Besuche auf Ihrer Website nach Prozentsatz und Gesamtanzahl an. Anders ausgedrückt zeigt der Bericht, wie viele Seiten der Besucher in der Regel zur Ansicht aufruft, bevor er die Site verlässt.

Benutzerspezifische Links (s.tl-Aufrufe) verlängern nicht die Pfadlänge für Seiten. Sie werden allerdings bei der Pfadlänge für Props (Traffic-Variablen) berücksichtigt.

Mehrere Instanzen desselben Werts (Neuladungen) verlängern den Pfad nicht. Beispiele:

**[!UICONTROL Seite A]** > **[!UICONTROL Seite B]** > **[!UICONTROL Benutzerspezifischer Link]** > **[!UICONTROL Seite B]** = Pfadlänge 2. (Beachten Sie, dass der benutzerspezifische Link und die Neuladung von Seite B keine Auswirkungen auf die Pfadlänge haben.)

**[!UICONTROL Prop A]** > **[!UICONTROL Benutzerspezifischer Link übergeht Prop B]** > **[!UICONTROL Prop C]** = Pfadlänge 3. (Beachten Sie, dass der benutzerspezifische Link für Prop B keine Auswirkungen auf die Pfadlänge hat.)
