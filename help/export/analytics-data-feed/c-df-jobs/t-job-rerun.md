---
description: Sie können einen oder mehrere Aufträge in der Liste „Aufträge“ erneut ausführen.
keywords: Data Feed;job;rerun
solution: Analytics
title: Auftrag erneut ausführen
uuid: 5caf95da-dd88-4b1a-a081-684f4fd1f714
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Auftrag erneut ausführen

Sie können einen oder mehrere Aufträge in der Liste „Aufträge“ erneut ausführen.

1. Wählen Sie einen oder mehrere Aufräge für die erneute Ausführung aus.
1. Click **[!UICONTROL Rerun Job]**.

   Der Vorgang der erneuten Ausführung ist vom aktuellen Auftragsstatus abhängig:

   | Status | Dateiname auf Server zwischengespeichert | Verarbeitung |
   |---|---|---|
   | Abgeschlossen | Ja | Datei wird erneut gesendet. |
   | Abgeschlossen | Nein | Der Auftrag wird erneut verarbeitet und dann erneut gesendet. |
   | Fehlgeschlagen | Nein | Der Auftrag wird erneut verarbeitet und dann erneut gesendet. |
   | Anderer Status | Nicht zutreffend | Wird nicht unterstützt. |

