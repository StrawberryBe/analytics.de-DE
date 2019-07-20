---
description: Sie können einen oder mehrere Aufträge in der Liste „Aufträge“ erneut ausführen.
keywords: Datenfeed; job; erneut ausführen
seo-description: Sie können einen oder mehrere Aufträge in der Liste „Aufträge“ erneut ausführen.
seo-title: Auftrag erneut ausführen
solution: Analytics
title: Auftrag erneut ausführen
uuid: 5 caf 95 da-dd 88-4 b 1 a-a 081-684 f 4 fd 1 f 714
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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

