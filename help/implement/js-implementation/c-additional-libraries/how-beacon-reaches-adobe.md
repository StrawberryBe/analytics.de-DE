---
description: Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird.
keywords: Analytics Implementation;gateway;wap;i-mode;wbmp
title: Mobilfunknetz-Protokoll-Gateway
topic: Developer and implementation
uuid: a2c92ce2-53a9-4b5b-be1a-89d9f1bf776f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Mobilfunknetz-Protokoll-Gateway

Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird.

Wenn ein Mobilgerät eine Seite von einem Webserver anfordert, wird die Anforderung über ein Gateway gesendet, das die Anforderung des Mobilgeräts (die meist über WAP oder i-mode erfolgt) in eine HTTP-Anforderung umwandelt, die dann an einen Webserver gesendet wird. Der Webserver sendet eine Antwort an das Gateway, das die Anforderung an das Mobilgerät weiterleitet. Dieses Gateway agiert wie ein normaler Proxyserver. Es gibt jedoch die Benutzeragenten-Zeichenfolge des Mobilgeräts an den Webserver weiter. Dadurch kann der Webserver mit einer Seite antworten, die speziell für das Gerät geeignet ist, von dem die Anforderung stammt.

Da die Bildschirmgröße bei WAP-Mobilgeräten stark eingeschränkt ist, sind die Seiten sehr schlank ausgelegt und enthalten oft nur Text und ein zwischengespeichertes Bild. Wenn den Seiten das Image-Tag hinzugefügt ist, wird für jede Seite eine Anforderung nach einem Bild von Adobe-Servern gesendet. Bei der Rückgabe des Bildes (im WBMP-Format) weisen die Adobe-Server den Browser an, das Bild nicht zwischenzuspeichern. Demzufolge wird das Bild auf nachfolgenden Seiten immer wieder erneut angefordert. Die oben beschriebene Zufallszahl dient zum Schutz vor Browsern, die sich nicht an die „no-cache“-Anweisungen von Adobe halten.
