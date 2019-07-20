---
description: Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird.
keywords: Analytics-Implementierung; gateway; wap; i-mode; wbmp
seo-description: Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird.
seo-title: Mobilfunknetz-Gateway
solution: Analytics
title: Mobilfunknetz-Gateway
topic: Entwickler und Implementierung
uuid: a 2 c 92 ce 2-53 a 9-4 b 5 b-be 1 a -89 d 9 f 1 f 1 bf 776
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Mobilfunknetz-Gateway

Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird.

Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird. Der Webserver sendet eine Antwort an das Gateway, das die Anforderung an das Mobilgerät weiterleitet. Dieses Gateway agiert wie ein normaler Proxyserver. Es gibt jedoch die Benutzeragenten-Zeichenfolge des Mobilgeräts an den Webserver weiter. Dadurch kann der Webserver mit einer Seite antworten, die speziell für das Gerät geeignet ist, von dem die Anforderung stammt.

Da die Bildschirmgröße bei WAP-Mobilgeräten stark eingeschränkt ist, sind die Seiten sehr schlank ausgelegt und enthalten oft nur Text und ein zwischengespeichertes Bild. Wenn den Seiten das Image-Tag hinzugefügt ist, wird für jede Seite eine Anforderung nach einem Bild von Adobe-Servern gesendet. Bei der Rückgabe des Bildes (im WBMP-Format) weisen die Adobe-Server den Browser an, das Bild nicht zwischenzuspeichern. Demzufolge wird das Bild auf nachfolgenden Seiten immer wieder erneut angefordert. Die oben beschriebene Zufallszahl dient zum Schutz vor Browsern, die sich nicht an die „no-cache“-Anweisungen von Adobe halten.
