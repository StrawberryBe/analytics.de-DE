---
title: US-Staaten
description: Der US-Bundesstaat des Besuchers.
feature: Dimensions
exl-id: d4506e59-c1ff-4348-912d-c1ad73278f56
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 77%

---

# US-Bundesstaat

Der &quot;US-Staat&quot; [Dimension](overview.md) erfasst den Status des Besuchers in den Vereinigten Staaten von Amerika. Sie ähnelt der Dimension [Regionen](regions.md), allerdings ist diese Dimension spezifisch für die USA. Die Verwendung dieser Dimension ist hilfreich, wenn Sie Einblicke wünschen, die detaillierter sind als [Länder](countries.md), aber nicht so detailliert wie [Städte](cities.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Suche zwischen IP-Adresse und Land zu unterstützen.

* Bei AppMeasurement-Implementierungen funktioniert diese Dimension standardmäßig.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] when [Konfigurieren eines Datenspeichers](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Dimensionselemente

Zu den Dimensionselementen gehören Regionen und das Land, in dem sich die Region befindet. Zu den Beispielwerten gehören `"California"`, `"Texas"` oder `"Virginia"`. Das Dimensionselement `"Unspecified"` umfasst den gesamten internationalen Traffic außerhalb der Vereinigten Staaten.

Diese Dimension kann `"AOL"`, einen DFÜ-Dienstleister umfassen. Abonnenten dieses Dienstes wird ein Zugangspunkt zugewiesen. AOL-Benutzer verwenden die IP-Adresse dieses Zugriffspunkts. Da diese Dimension auf der IP-Adresse basiert, wird die Geolokalisierung des Zugangspunktes anstelle des tatsächlichen Standortes des Besuchers verwendet.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Einige Netzbetreiber transportieren den IP-Traffic über zentralisierte oder regionale Standorte.
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
* **Proxys, die IP-Adressen aus Datenschutzgründen verdecken**: Dienste wie der Private Relay von Apple verbergen die wahre IP-Adresse, indem Daten per Zufall über einen Vermittler oder Proxy gesendet werden. Dieser Proxy ersetzt dann eine andere IP-Adresse, bevor er an Adobe weitergeleitet wird.
