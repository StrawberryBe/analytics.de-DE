---
title: Verbindungstyp
description: Wie sich der Besucher mit dem Internet verbindet.
exl-id: 149b2353-6128-4e0c-a73a-bc5a37c66b52
source-git-commit: 82d6137bc9229bbaa997c6856690bf76c20b755c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 7%

---

# Verbindungstyp

Die Dimension &quot;Verbindungstyp&quot;zeigt an, wie sich der Besucher mit dem Internet verbunden hat. Diese Dimension ist nützlich, um zu bestimmen, wie Besucher eine Verbindung zum Internet herstellen, um Ihre Site zu durchsuchen. Sie können damit den Site-Inhalt basierend auf der Verbindungsgeschwindigkeit von Besuchern optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verwendet eine Kombination aus der [`ct`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) und der serverseitigen Logik der Adobe. Adobe verwendet die folgenden Regeln, um den Wert zu bestimmen:

1. Wenn die `ct`-Abfragezeichenfolge `"modem"` entspricht, setzen Sie das Dimensionselement auf `"Modem"`. AppMeasurement erfasst diese Daten nur in nicht unterstützten Internet Explorer-Browsern, wodurch dieses Dimensionselement ungewöhnlich wird.
1. Überprüfen Sie die IP-Adresse des Treffers und referenzieren Sie sie auf eine interne Nachschlagetabelle für die Adobe. Wenn die IP-Adresse von einem Mobilnetzbetreiber stammt, setzen Sie das Dimensionselement auf `"Mobile Carrier"`.
1. Wenn die `ct`-Abfragezeichenfolge `"lan"` entspricht, setzen Sie das Dimensionselement auf `"LAN/Wifi"`.
1. Wenn der Treffer von einer [Datenquelle](/help/import/c-data-sources/datasrc-home.md) stammt oder anderweitig als spezieller Treffertyp gilt, setzen Sie das Dimensionselement auf `"Not specified"`.
1. Wenn keine der oben genannten Regeln erfüllt ist, wird standardmäßig der Wert `"LAN/Wifi"` verwendet.

## Dimensionselemente

Zu den Dimension-Elementen gehören `LAN/Wifi`, `Mobile Carrier`, `Modem` und `Not Specified`.

* **`LAN/Wifi`**: Besucher, die über einen Festnetz- oder WLAN-Hotspot mit dem Internet verbunden sind.
* **`Mobile Carrier`**: Der Besucher, der über einen Mobilnetzbetreiber mit dem Internet verbunden ist.
* **`Modem`**: Der Besucher, der über ein Modem in einem nicht unterstützten Internet Explorer-Browser mit dem Internet verbunden ist.
* **`Not Specified`**: Der Treffer hatte keinen Verbindungstyp.
