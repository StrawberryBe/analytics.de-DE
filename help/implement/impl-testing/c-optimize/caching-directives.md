---
description: Die JavaScript-Bibliotheksdatei soll nach dem ersten Laden einer Seite im Browser des Benutzers zwischengespeichert bleiben.
keywords: Analytics Implementation
solution: Analytics
subtopic: Troubleshooting
title: Caching-Anweisungen
topic: Developer and implementation
uuid: 6bd2c26d-93ee-4039-8beb-6a6b16218a07
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Caching-Anweisungen

Die JavaScript-Bibliotheksdatei soll nach dem ersten Laden einer Seite im Browser des Benutzers zwischengespeichert bleiben.

Adobe-Kunden müssen sicherstellen, dass ihre Webserver so eingerichtet sind, dass sie von dieser Funktion Gebrauch machen. So müssen Sie zum Beispiel darauf achten, dass die Einstellung „NO-CACHE“ auf „false“ festgelegt ist. Außerdem müssen Sie darauf achten, dass ein ausreichend langer Ablaufzeitraum eingestellt ist. Und überprüfen Sie, dass alle Proxycaches korrekt konfiguriert sind. Mehr Informationen dazu finden Sie in der Dokumentation Ihres Webservers.
