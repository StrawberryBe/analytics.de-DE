---
description: Da mobile Geräte über kleine Datenpakete namens „Beacon“ verfolgt werden (so wie sonst Besucher), stehen für diesen Zweck die meisten Berichte zur Verfügung und enthalten korrekte Daten.
keywords: Analytics Implementation;reports;mobile protocols;search engines;search keywords;referring domains;referrers;geosegmentation;domains;connection type;time zone;cookies;java;javascript;monitor colors;monitor resolution;browser width;height;netscape plug-in
title: Berichte für Geräte mit Mobilfunkprotokollen
topic: Developer and implementation
uuid: 4aab125d-c131-4402-9bc8-1c7fd1bb2bee
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Berichte für Geräte mit Mobilfunkprotokollen

Da mobile Geräte über kleine Datenpakete namens „Beacon“ verfolgt werden (so wie sonst Besucher), stehen für diesen Zweck die meisten Berichte zur Verfügung und enthalten korrekte Daten.

Zum Ändern von Daten, die über die mobile oder normale Methode erfasst wurden, kann [!DNL VISTA] eingesetzt werden. Alle [!UICONTROL Custom][!UICONTROL Insight]- ([!UICONTROL Eigenschaftsvariablen] und [!UICONTROL eVars]), [!UICONTROL Ereignis]-, [!UICONTROL Site-Traffic]- und [!UICONTROL Pfadsetzungsberichte] werden unterstützt.

## Suchmaschinen, Keywords, verweisende Domänen und Referrer {#section_184D2EF9D906443FBDED04A09CDC50E9}

Diese Berichte enthalten nur dann Daten, wenn der Referrer in der Bildanforderung, die von der mobilen Seite gesendet wird, aufgefüllt ist. Der Referrer wird mithilfe des Abfragezeichenfolgen-Parameters „r“ aufgefüllt, wie im Whitepaper „Implementing without JavaScript“ (Implementieren ohne JavaScript) beschrieben. Die Referrer-Informationen müssen manuell in die Bildanforderung eingetragen werden.

Der Abfragezeichenfolgenparameter "r"muss das Protokoll der verweisenden Stelle enthalten. Wenn das Protokoll weggelassen wird, wird der Bericht der verweisenden Instanz nicht weitergegeben. Verwenden Sie zum Beispiel `r=https://msn.com` anstatt von `r=msn.com`.

## Geosegmentation und Domänen {#section_2B4E9443AAFE4ECA961F9E993592E628}

Geosegmentation-Berichte basieren auf der IP-Adresse des Geräts, von dem die Anforderung stammt. Da mobile Geräte ihre Bildanforderungen über ein Gateway an Adobe-Server richten, wird der geografische Standort des Benutzers aus der IP-Adresse des Gateways bestimmt. Da Gateways und deren IP-Adressen bei großen Netzwerken registriert sind, ist der zugehörige geografische Standort oftmals nicht sehr genau.

Auch Domänen basieren auf der IP-Adresse des Gateways, weshalb der Domänenbericht häufig den Namen des Betreibers enthält, dem das Gateway gehört. Aufgrund von Betreibern virtueller Mobilfunknetze (Mobile Virtual Network Operators, MVNOs) ist diese Angabe nicht immer sehr genau.

## Verbindungstypen {#section_0E7FA18178B848AEBB839B1694B4D691}

Adobe pflegt einen bekannten Bereich von IP-Adressen, die zu Mobilnetzbetreibern gehören. Wenn ein Treffer aus einem IP-Bereich erhalten wird, der zu einem bekannten Mobilnetzbetreiber gehört, wird der Treffer als „Mobilnetzbetreiber“ im Verbindungstypbericht angezeigt. Andernfalls wird mobiler Datenverkehr unter „LAN/WiFi“ aufgeführt.

## Zeitzonen, Cookies, Java, JavaScript, Bildschirmfarben und -auflösungen, Browserbreite und -höhe sowie Netscape-Plug-ins {#section_158C848273AE4691B4413767E849E846}

In diesen Berichten wird JavaScript eingesetzt, um bestimmte Einstellungen des Browsers zu ermitteln. Da das Bild-Beacon bei mobilen Geräten nicht mittels JavaScript erstellt wird, enthalten diese Berichte keine Daten von mobilen Benutzern.
