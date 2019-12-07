---
description: Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.
keywords: Analytics Implementation
subtopic: Visitors
title: Unique Visitors identifizieren
topic: Developer and implementation
uuid: ed4dee75-ecfb-4715-8122-461983c7dd8f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Unique Visitors identifizieren

Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.

## Reihenfolge Analytics-Besucher-ID {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Adobe Analytics bietet verschiedene Mechanismen zur Identifizierung von Besuchern. Die folgende Tabelle listet verschiedene Methoden auf, mit denen ein Besucher in Analytics identifiziert werden kann (in der bevorzugten Reihenfolge):

| Verwendete Reihenfolge | Anfrageparameter (Erfassungsmethode) | Vorhanden, wenn |
|---|---|---|
| ![](assets/step1_icon.png) | [vid (s.visitorID)](/help/implement/js-implementation/c-unique-visitors/visid-custom.md) | s.visitorID festgelegt ist. |
| ![](assets/step2_icon.png) | [aid (s_vi-Cookie)](/help/implement/js-implementation/c-unique-visitors/visid-analytics.md) | der Besucher über bestehendes s_vi-Cookie verfügt, bevor Sie den Besucher-ID-Dienst bereitgestellt haben, oder wenn Sie eine Schonfrist für die Besucher-ID konfiguriert haben. |
| ![](assets/step3_icon.png) | [mid (AMCV_-Cookie, der vom Experience Cloud-Besucher-ID-Dienst gesetzt wird)](https://marketing.adobe.com/resources/help/en_US/mcvid/) | der Browser des Besuchers Cookies (von Erstanbietern) akzeptiert. |
| ![](assets/step4_icon.png) | [fid (Ausweichcookie für H.25.3 oder AppMeasurement für JavaScript)](/help/implement/js-implementation/c-unique-visitors/visid-fallback.md) | der Browser des Besuchers Cookies (von Erstanbietern) akzeptiert. |
| ![](assets/step5_icon.png) | [IP-Adresse, Benutzeragent, Gateway-IP-Adresse](/help/implement/js-implementation/c-unique-visitors/visid-fallback.md#section_104819D74C594ECE879144FCC5DEF4BF) | der Browser des Besuchers keine Cookies akzeptiert. |

In vielen Szenarien sehen Sie möglicherweise 2 oder 3 verschiedene IDs für einen Aufruf, jedoch verwendet Analytics die erste vorhandene ID aus der vorigen Tabelle als offizielle Besucher-ID. Wenn Sie zum Beispiel eine benutzerdefinierte Besucher-ID (im Abfrageparameter „vid“ enthalten) festlegen, wird diese ID vor anderen IDs verwendet, die möglicherweise bei dem gleichen Treffer vorhanden sind.

> [!NOTE] Jede Analytics-Besucher-ID ist einem Besucherprofil auf Adobe-Servern zugewiesen. Besucherprofile werden nach einer Inaktivität von mindestens 13 Monaten gelöscht, unabhängig vom Ablauf der Besucher-ID-Cookies.
