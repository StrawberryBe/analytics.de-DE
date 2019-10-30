---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.cookieDomain

Die Variable bestimmt, in welcher Domäne die [!DNL Analytics]-Cookies `s_cc` und `s_sq` abgelegt werden.

Im Allgemeinen wird `s.cookieDomainPeriods` verwendet, um `s.cookieDomain` aus `window.location.hostname` zu generieren. Statt `s.cookieDomainPeriods` zu verwenden, können Sie für `s.cookieDomain` auch explizit das Element einstellen, das Sie in Ihrer Implementierung verwenden möchten. Beispielsweise können Sie Cookies bei einem vollständig qualifizierten Seitennamen ablegen, indem Sie Folgendes verwenden:

`s.cookieDomain = window.location.hostname;`
