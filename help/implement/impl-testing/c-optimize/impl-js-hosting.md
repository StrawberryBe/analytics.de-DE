---
description: Bringen Sie den Aufruf für die JavaScript-Bibliotheksdatei am Anfang der Seite unter, damit dafür gesorgt ist, dass das Bild als eines der ersten Elemente geladen wird.
keywords: Analytics-Implementierung
seo-description: Bringen Sie den Aufruf für die JavaScript-Bibliotheksdatei am Anfang der Seite unter, damit dafür gesorgt ist, dass das Bild als eines der ersten Elemente geladen wird.
seo-title: Speicherort der JavaScript-Datei und parallele Downloads
solution: Analytics
subtopic: Fehlerbehebung
title: Speicherort der JavaScript-Datei und parallele Downloads
topic: Entwickler und Implementierung
uuid: ed5118a8-b142-4fab-8aa1-92d931cc1439
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Speicherort der JavaScript-Datei und parallele Downloads

Bringen Sie den Aufruf für die JavaScript-Bibliotheksdatei am Anfang der Seite unter, damit dafür gesorgt ist, dass das Bild als eines der ersten Elemente geladen wird.

In den meisten Webbrowsern werden mehrere Bilder parallel heruntergeladen. Im Allgemeinen gilt, dass drei von vier Bildern gleichzeitig heruntergeladen werden.

Da in den meisten gängigen Webbrowsern (inklusive Internet Explorer) mehrere Elemente parallel heruntergeladen werden, ist die Angabe in der Statusleiste, welches Element gerade heruntergeladen wird, nicht wirklich exakt. Beispiel: In der Statusleiste wird angezeigt, dass der Browser auf den Download von Bild 1 wartet. Gemäß den Netzwerkpakettests hat der Browser jedoch das Bild 1 bereits erhalten und wartet derzeit auf Bild 2.

> [!NOTE] Da bei von Drittanbietern (wie z. B. Keynote Systems) durchgeführten Audits zur Internet-Leistung Seitenbildelemente nacheinander heruntergeladen werden (nicht parallel), spiegelt dies nicht das reale Verhalten von echten Benutzern wider.

