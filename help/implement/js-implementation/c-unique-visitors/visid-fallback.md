---
description: Wenn andere Besucher-ID-Methoden fehlschlagen, setzt Adobe ein Ausweich-Cookie oder verwendet eine Kombination aus IP-Adresse und Benutzeragent, um den Besucher zu identifizieren.
keywords: Analytics-Implementierung
seo-description: Wenn andere Besucher-ID-Methoden fehlschlagen, setzt Adobe ein Ausweich-Cookie oder verwendet eine Kombination aus IP-Adresse und Benutzeragent, um den Besucher zu identifizieren.
seo-title: Fallback-ID-Methoden
solution: Analytics
title: Fallback-ID-Methoden
topic: Entwickler und Implementierung
uuid: f 242 d 481-81 f 0-4287-be 4 f -52 fd 03 eb 01 fc
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Fallback-ID-Methoden

Wenn andere Besucher-ID-Methoden fehlschlagen, setzt Adobe ein Ausweich-Cookie oder verwendet eine Kombination aus IP-Adresse und Benutzeragent, um den Besucher zu identifizieren.

## Ausweichmethode zur Besucheridentifizierung {#section_2BA15E4FA6034C3EBF43859406343EB6}

AppMeasurement für JavaScript 1.x und JavaScript H.25.3 (Januar 2013 veröffentlicht) enthalten eine neue Ausweichmethode zur Identifizierung von Besuchern, in deren Browsern das von Adobes Datenerfassungsservern gesetzte Cookie (`s_vi`) blockiert wird. Bislang wurden Besucher, wenn ein Cookie nicht gesetzt werden konnte, bei der Datenkollektion anhand einer Kombination von IP-Adresse und Benutzeragentenzeichenfolge identifiziert.

Mit diesem Update wird, wenn das normale `s_vi`-Cookie nicht verfügbar ist, ein Ausweich-Cookie in der Domäne der Website mit einer zufällig generierten eindeutigen ID erstellt. Dieses Cookie mit dem Namen `s_fid` wird mit einem Ablaufzeitraum von 2 Jahren festgelegt und dient als Ausweichmöglichkeit bei zukünftigen Identifizierungen. This change should result in increased accuracy in visit and visitor counts in situations where the primary cookie ( `AMCV_` or `s_vi`) cannot be set.

In den Besuchen insgesamt sind alle Besucher enthalten, die anhand des `s_vi`-Cookies oder nach einer Ausweichmethode identifiziert werden.

## IP-Adresse, Benutzeragent, Gateway-IP-Adresse {#section_104819D74C594ECE879144FCC5DEF4BF}

. If the `AMCV_` or `s_vi` and the `s_fid` cookies cannot be set, visitors are identified using a combination of IP address and User Agent.
