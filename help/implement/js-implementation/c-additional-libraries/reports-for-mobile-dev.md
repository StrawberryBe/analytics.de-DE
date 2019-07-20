---
description: Da mobile Geräte über kleine Datenpakete namens „Beacon“ verfolgt werden (so wie sonst Besucher), stehen für diesen Zweck die meisten Berichte zur Verfügung und enthalten korrekte Daten.
keywords: Analytics-Implementierung; Berichte; mobile Protokolle; Suchmaschinen; keywords; Verweisende Domänen; referrers; geosegmentation; domains; Verbindungstyp; Zeitzone; Cookies; java; javascript; Bildschirmfarben; Bildschirmauflösung; Browserbreite; height; netscape plug-in
seo-description: Da mobile Geräte über kleine Datenpakete namens „Beacon“ verfolgt werden (so wie sonst Besucher), stehen für diesen Zweck die meisten Berichte zur Verfügung und enthalten korrekte Daten.
seo-title: Berichte für Geräte mit Mobilfunkprotokollen
solution: Analytics
title: Berichte für Geräte mit Mobilfunkprotokollen
topic: Entwickler und Implementierung
uuid: 4 aab 125 d-c 131-4402-9 bc 8-1 c 7 fd 1 bb 2 bee
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Berichte für Geräte mit Mobilfunkprotokollen

Da mobile Geräte über kleine Datenpakete namens „Beacon“ verfolgt werden (so wie sonst Besucher), stehen für diesen Zweck die meisten Berichte zur Verfügung und enthalten korrekte Daten.

Zum Ändern von Daten, die über die mobile oder normale Methode erfasst wurden, kann [!DNL VISTA] eingesetzt werden. Alle [!UICONTROL Custom][!UICONTROL Insight]- ([!UICONTROL Eigenschaftsvariablen] und [!UICONTROL eVars]), [!UICONTROL Ereignis]-, [!UICONTROL Site-Traffic]- und [!UICONTROL Pfadsetzungsberichte] werden unterstützt.

## Suchmaschinen, Keywords, verweisende Domänen und Referrer {#section_184D2EF9D906443FBDED04A09CDC50E9}

Diese Berichte enthalten nur dann Daten, wenn der Referrer in der Bildanforderung, die von der mobilen Seite gesendet wird, aufgefüllt ist. Der Referrer wird mithilfe des Abfragezeichenfolgen-Parameters „r“ aufgefüllt, wie im Whitepaper „Implementing without JavaScript“ (Implementieren ohne JavaScript) beschrieben. Die Referrer-Informationen müssen manuell in die Bildanforderung eingetragen werden.

Der Abfragezeichenfolgenparameter „r“ muss das Protokoll der verweisenden Instanz enthalten. Wenn das Protokoll weggelassen wird, wird der Bericht der verweisenden Instanz nicht weitergegeben. `r=https://msn.com``r=msn.com`Verwenden Sie beispielsweise nicht.

## Geosegmentation und Domänen {#section_2B4E9443AAFE4ECA961F9E993592E628}

Geosegmentation-Berichte basieren auf der IP-Adresse des Geräts, von dem die Anforderung stammt. Da mobile Geräte ihre Bildanforderungen über ein Gateway an Adobe-Server richten, wird der geografische Standort des Benutzers aus der IP-Adresse des Gateways bestimmt. Da Gateways und deren IP-Adressen bei großen Netzwerken registriert sind, ist der zugehörige geografische Standort oftmals nicht sehr genau.

Auch Domänen basieren auf der IP-Adresse des Gateways, weshalb der Domänenbericht häufig den Namen des Betreibers enthält, dem das Gateway gehört. Aufgrund von Betreibern virtueller Mobilfunknetze (Mobile Virtual Network Operators, MVNOs) ist diese Angabe nicht immer sehr genau.

## Verbindungstypen {#section_0E7FA18178B848AEBB839B1694B4D691}

Adobe pflegt einen bekannten Bereich von IP-Adressen, die zu Mobilnetzbetreibern gehören. Wenn ein Treffer aus einem IP-Bereich erhalten wird, der zu einem bekannten Mobilnetzbetreiber gehört, wird der Treffer als „Mobilnetzbetreiber“ im Verbindungstypbericht angezeigt. Andernfalls wird mobiler Datenverkehr unter „LAN/WiFi“ aufgeführt.

## Zeitzonen, Cookies, Java, JavaScript, Bildschirmfarben und -auflösungen, Browserbreite und -höhe sowie Netscape-Plug-ins {#section_158C848273AE4691B4413767E849E846}

In diesen Berichten wird JavaScript eingesetzt, um bestimmte Einstellungen des Browsers zu ermitteln. Da das Bild-Beacon bei mobilen Geräten nicht mittels JavaScript erstellt wird, enthalten diese Berichte keine Daten von mobilen Benutzern.
