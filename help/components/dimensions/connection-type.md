---
title: Verbindungstyp
description: Wie sich der Besucher mit dem Internet verbindet.
feature: Dimensions
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 100%

---

# Verbindungstyp

Die Dimension „Verbindungstyp“ gibt an, wie sich der Besucher mit dem Internet verbunden hat. Diese Dimension ist nützlich, um festzustellen, wie Besucher eine Internetverbindung herstellen, um auf Ihrer Site zu surfen. Damit können Sie den Site-Inhalt entsprechend der Verbindungsgeschwindigkeit der Besucher optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verwendet eine Kombination aus der [`ct` Abfragezeichenfolge](/help/implement/validate/query-parameters.md) und der Server-seitigen Logik von Adobe. Adobe setzt die folgenden Regeln ein, um den Wert der Dimension zu bestimmen:

1. Wenn die `ct` Abfragezeichenfolge `"modem"` entspricht, setze das Dimensionselement auf `"Modem"`. AppMeasurement erfasst diese Daten nur in nicht unterstützten Internet Explorer-Browsern, wodurch dieses Dimensionselement nicht oft vorkommt.
1. Überprüfen Sie die IP-Adresse des Treffers und referenzieren Sie sie auf eine Adobe-interne Nachschlagetabelle. Wenn die IP-Adresse von einem Mobilnetzbetreiber stammt, setze das Dimensionselement auf `"Mobile Carrier"`.
1. Wenn die `ct` Abfragezeichenfolge `"lan"` entspricht, setze das Dimensionselement auf `"LAN/Wifi"`.
1. Wenn der Treffer von einer [Datenquelle](/help/import/c-data-sources/datasrc-home.md) stammt oder anderweitig als spezieller Treffertyp gilt, setze das Dimensionselement auf `"Not specified"`.
1. Wenn keine der oben genannten Regeln erfüllt ist, verwende als Standard den Wert `"LAN/Wifi"`.

## Dimensionselemente

Zu den Dimensionselementen gehören `LAN/Wifi`, `Mobile Carrier`, `Modem` und `Not Specified`.

* **`LAN/Wifi`**: Besucher, die über das Festnetz oder einen WLAN-Hotspot mit dem Internet verbunden sind.
* **`Mobile Carrier`**: Besucher, die über einen Mobilnetzbetreiber mit dem Internet verbunden sind.
* **`Modem`**: Besucher, die über ein Modem über den nicht unterstützten Internet Explorer-Browser mit dem Internet verbunden sind.
* **`Not Specified`**: Der Treffer hatte keinen Verbindungstyp.
