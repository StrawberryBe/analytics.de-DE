---
description: Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.
keywords: Analytics-Implementierung
seo-description: Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.
seo-title: Identifizieren Sie individuelle Besucher.
solution: Analytics
subtopic: Besuchern
title: Identifizieren Sie individuelle Besucher.
topic: Entwickler und Implementierung
uuid: ed 4 dee 75-ecfb -4715-8122-461983 c 7 dd 8 f
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Identifizieren Sie individuelle Besucher.

Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.

## Reihenfolge Analytics-Besucher-ID {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Adobe Analytics bietet verschiedene Mechanismen zur Identifizierung von Besuchern. Die folgende Tabelle listet verschiedene Methoden auf, mit denen ein Besucher in Analytics identifiziert werden kann (in der bevorzugten Reihenfolge):

| Verwendete Reihenfolge | Anfrageparameter (Erfassungsmethode) | Vorhanden, wenn |
|---|---|---|
| ![](assets/step1_icon.png) | [vid (s.visitorID)](../../../implement/js-implementation/c-unique-visitors/visid-custom.md#concept_4A2000F4B6ED41E99CA6118A6D74ECE8) | s.visitorID festgelegt ist. |
| ![](assets/step2_icon.png) | [aid (s_vi-Cookie)](../../../implement/js-implementation/c-unique-visitors/visid-analytics.md#concept_74F6B4B9B2FA415AB5D029A1F8F099BC) | der Besucher über bestehendes s_vi-Cookie verfügt, bevor Sie den Besucher-ID-Dienst bereitgestellt haben, oder wenn Sie eine Schonfrist für die Besucher-ID konfiguriert haben. |
| ![](assets/step3_icon.png) | [mid (AMCV_-Cookie, der vom Experience Cloud-Besucher-ID-Dienst gesetzt wird)](https://marketing.adobe.com/resources/help/en_US/mcvid/) | der Browser des Besuchers Cookies (von Erstanbietern) akzeptiert. |
| ![](assets/step4_icon.png) | [fid (Ausweichcookie für H.25.3 oder AppMeasurement für JavaScript)](../../../implement/js-implementation/c-unique-visitors/visid-fallback.md#concept_EBCBF9EB390E45A2BA20DB6BE931C505) | der Browser des Besuchers Cookies (von Erstanbietern) akzeptiert. |
| ![](assets/step5_icon.png) | [IP-Adresse, Benutzeragent, Gateway-IP-Adresse](../../../implement/js-implementation/c-unique-visitors/visid-fallback.md#section_104819D74C594ECE879144FCC5DEF4BF) | der Browser des Besuchers keine Cookies akzeptiert. |

In vielen Szenarien sehen Sie möglicherweise 2 oder 3 verschiedene IDs für einen Aufruf, jedoch verwendet Analytics die erste vorhandene ID aus der vorigen Tabelle als offizielle Besucher-ID. Wenn Sie zum Beispiel eine benutzerdefinierte Besucher-ID (im Abfrageparameter „vid“ enthalten) festlegen, wird diese ID vor anderen IDs verwendet, die möglicherweise bei dem gleichen Treffer vorhanden sind.

>[!NOTE]
>
>Jede Analytics-Besucher-ID ist mit einem Besucherprofil auf Adobe-Servern verknüpft. Besucherprofile werden nach einer Inaktivität von mindestens 13 Monaten gelöscht, unabhängig vom Ablauf der Besucher-ID-Cookies.
