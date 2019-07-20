---
description: Bringen Sie den Aufruf für die JavaScript-Bibliotheksdatei am Anfang der Seite unter, damit dafür gesorgt ist, dass das Bild als eines der ersten Elemente geladen wird.
keywords: Analytics-Implementierung
seo-description: Bringen Sie den Aufruf für die JavaScript-Bibliotheksdatei am Anfang der Seite unter, damit dafür gesorgt ist, dass das Bild als eines der ersten Elemente geladen wird.
seo-title: Speicherort und Concurrence von javascript
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Speicherort und Concurrence von javascript
topic: Entwickler und Implementierung
uuid: ed 5118 a 8-b 142-4 fab -8 aa 1-92 d 931 cc 1439
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Speicherort und Concurrence von javascript

Bringen Sie den Aufruf für die JavaScript-Bibliotheksdatei am Anfang der Seite unter, damit dafür gesorgt ist, dass das Bild als eines der ersten Elemente geladen wird.

In den meisten Webbrowsern werden mehrere Bilder parallel heruntergeladen. Im Allgemeinen gilt, dass drei von vier Bildern gleichzeitig heruntergeladen werden.

Da in den meisten gängigen Webbrowsern (inklusive Internet Explorer) mehrere Elemente parallel heruntergeladen werden, ist die Angabe in der Statusleiste, welches Element gerade heruntergeladen wird, nicht wirklich exakt. Beispiel: In der Statusleiste wird angezeigt, dass der Browser auf den Download von Bild 1 wartet. Gemäß den Netzwerkpakettests hat der Browser jedoch das Bild 1 bereits erhalten und wartet derzeit auf Bild 2.

>[!NOTE]
>
>Da Internetleistungsanbieter von Drittanbietern (wie z. B. Keynote Systems) Seitenbildelemente nacheinander herunterladen und nicht gleichzeitig, imitieren sie die typische Benutzererfahrung nicht.

