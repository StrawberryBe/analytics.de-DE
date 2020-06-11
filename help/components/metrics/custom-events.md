---
title: Benutzerspezifische Ereignisse
description: Die Anzahl der Treffer, bei denen ein benutzerdefiniertes Ereignis vorhanden ist.
translation-type: tm+mt
source-git-commit: 554ced510600a4d5866e89806b058b5d2d9a3edf
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 19%

---


# Benutzerspezifische Ereignisse

*Auf dieser Hilfeseite wird beschrieben, wie benutzerspezifische Ereignis als Metrik funktionieren. Informationen dazu, wie benutzerspezifische Ereignis als Implementierungsvariable funktionieren, finden Sie unter Übersicht über die[Ereignisse](/help/implement/vars/page-vars/events/events-overview.md)im Benutzerhandbuch &quot;Implementierung&quot;.*

Die Metriken zum benutzerspezifischen Ereignis zeigen die Anzahl der Treffer an, bei denen ein bestimmtes benutzerdefiniertes Ereignis in einer Bildanforderung festgelegt wurde. Diese Metriken sind für viele Implementierungen unverzichtbar, da sie Einblicke in unternehmensspezifische Ereignis bieten.

## Berechnung dieser Metrik

Benutzerspezifische Ereignis werden je nach Typ unterschiedlich berechnet. Sie können den Typ eines Ereignisses in den Report Suite-Einstellungen unter &quot; [Erfolgsergebnisse](../../admin/admin/c-success-events/success-event.md) &quot;überprüfen.

* **Zähler-Ereignis**: Die Standardeinstellung für Ereignisse. Die meisten Ereignisse sind Gegenanzeigen Ereignisse. Zählt die Anzahl der Treffer, bei denen das passende benutzerdefinierte Ereignis `event1` - `event1000` in der [`events`](/help/implement/vars/page-vars/events/events-overview.md) Variablen vorhanden ist.
* **Numerische Ereignis**: Legt den dem Ereignis in der `events` Variablen zugewiesenen numerischen Wert fest.
* **Währungs-Ereignisse**: Wendet Währungsumrechnung auf den Wechselkurs dieses Tages an und summiert dann den numerischen Wert, der jedem Treffer in der `events` Variablen zugewiesen wird.

Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. In den meisten Unternehmen, die nicht über einen Altvertrag verfügen, stehen 1000 benutzerdefinierte Ereignisse zur Verfügung. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignisse für Sie verfügbar sind.

Adobe empfiehlt dringend, dass Sie die Verwendung der einzelnen Ereignis im [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)Ihres Unternehmens erfassen.
