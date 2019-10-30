---
description: Die JavaScript-Bibliotheksdatei soll nach dem ersten Laden einer Seite im Browser des Benutzers zwischengespeichert bleiben.
keywords: Analytics-Implementierung
seo-description: Die JavaScript-Bibliotheksdatei soll nach dem ersten Laden einer Seite im Browser des Benutzers zwischengespeichert bleiben.
seo-title: Caching-Anweisungen
solution: Analytics
subtopic: Fehlerbehebung
title: Caching-Anweisungen
topic: Entwickler und Implementierung
uuid: 6bd2c26d-93ee-4039-8beb-6a6b16218a07
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Caching-Anweisungen

Die JavaScript-Bibliotheksdatei soll nach dem ersten Laden einer Seite im Browser des Benutzers zwischengespeichert bleiben.

Adobe-Kunden müssen sicherstellen, dass ihre Webserver so eingerichtet sind, dass sie von dieser Funktion Gebrauch machen. So müssen Sie zum Beispiel darauf achten, dass die Einstellung „NO-CACHE“ auf „false“ festgelegt ist. Außerdem müssen Sie darauf achten, dass ein ausreichend langer Ablaufzeitraum eingestellt ist. Und überprüfen Sie, dass alle Proxycaches korrekt konfiguriert sind. Mehr Informationen dazu finden Sie in der Dokumentation Ihres Webservers.
