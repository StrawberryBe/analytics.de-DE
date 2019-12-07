---
description: Wenn andere Besucher-ID-Methoden fehlschlagen, setzt Adobe ein Ausweich-Cookie oder verwendet eine Kombination aus IP-Adresse und Benutzeragent, um den Besucher zu identifizieren.
keywords: Analytics Implementation
title: Ausweich-ID-Methoden
topic: Developer and implementation
uuid: f242d481-81f0-4287-be4f-52fd03eb01fc
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Ausweich-ID-Methoden

Wenn andere Besucher-ID-Methoden fehlschlagen, setzt Adobe ein Ausweich-Cookie oder verwendet eine Kombination aus IP-Adresse und Benutzeragent, um den Besucher zu identifizieren.

## Ausweichmethode zur Besucheridentifizierung {#section_2BA15E4FA6034C3EBF43859406343EB6}

AppMeasurement for JavaScript 1.x and JavaScript H.25.3 (released January 2013) contain a new fallback visitor identification method for visitors whose browser blocks the cookie set by Adobe's data collection servers (called `s_vi`). Bislang wurden Besucher, wenn ein Cookie nicht gesetzt werden konnte, bei der Datenkollektion anhand einer Kombination von IP-Adresse und Benutzeragentenzeichenfolge identifiziert.

Mit diesem Update wird, wenn das normale `s_vi`-Cookie nicht verfügbar ist, ein Ausweich-Cookie in der Domäne der Website mit einer zufällig generierten eindeutigen ID erstellt. Dieses Cookie mit dem Namen `s_fid` wird mit einem Ablaufzeitraum von 2 Jahren festgelegt und dient als Ausweichmöglichkeit bei zukünftigen Identifizierungen. Diese Änderung sollte zu erhöhter Genauigkeit bei der Besuchs- und Besucherzählung führen in Situationen, in denen das primäre Cookie (`AMCV_` oder `s_vi`) nicht gesetzt werden kann.

In den Besuchen insgesamt sind alle Besucher enthalten, die anhand des `s_vi`-Cookies oder nach einer Ausweichmethode identifiziert werden.

## IP-Adresse, Benutzeragent, Gateway-IP-Adresse {#section_104819D74C594ECE879144FCC5DEF4BF}

. Wenn die Cookies `AMCV_` oder `s_vi` und `s_fid` nicht gesetzt werden können, werden Besucher anhand einer Kombination aus IP-Adresse und Benutzeragent identifiziert.
