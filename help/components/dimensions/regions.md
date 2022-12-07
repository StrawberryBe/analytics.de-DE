---
title: Regionen
description: Die geografische Region des Besuchers.
feature: Dimensions
exl-id: 95ab4c7e-71e8-490f-88a4-25201331d848
source-git-commit: 146d622f370fd7469a8e5f0f2fe68cb31fa91844
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 89%

---

# Regionen

Die Dimension „Regionen“ gibt die geografische Region des Besuchers an. Dies ist ein geografischer Bereich, der kleiner als ein Land, jedoch größer als eine Stadt ist. In einigen Ländern ist unter einer Region ein Bundesstaat, eine Provinz oder eine Präfektur zu verstehen. In anderen Bereichen handelt es sich um ein eigenständiges Land, ein Distrikt oder eine Metropolregion. Die Verwendung dieser Dimension ist hilfreich, wenn Sie Einblicke wünschen, die detaillierter sind als [Länder](countries.md), aber nicht so detailliert wie [Städte](cities.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Suche zwischen IP-Adresse und Land zu unterstützen. Diese Dimension ist bei allen Implementierungen vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören Regionen und das Land, in dem sich die Region befindet. Zu den Beispielwerten gehören `"California (United States)"`, `"Tokyo (Japan)"` oder `"Sao Paulo (Brazil)"`.

Einige Dimensionselemente können `"AOL"`, einen DFÜ-Dienstleister umfassen. Abonnenten dieses Dienstes wird ein Zugangspunkt zugewiesen, der auf dem Land basiert, in dem ihre Kontonummer eingerichtet ist. AOL-Benutzer verwenden die IP-Adresse dieses Zugriffspunkts. Da diese Dimension auf der IP-Adresse basiert, wird die Geolokalisierung des Zugangspunktes anstelle des tatsächlichen Standortes des Besuchers verwendet.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Netzbetreibern transportiert den IP-Traffic über zentralisierte oder regionale POPs (Points of Presence).
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
* **Proxys, die IP-Adressen aus Datenschutzgründen verdecken**: Dienste wie der Private Relay von Apple verbergen die wahre IP-Adresse, indem Daten zufällig über einen Vermittler oder Proxy gesendet werden. Dieser Proxy ersetzt dann eine andere IP-Adresse, bevor er an Adobe weitergeleitet wird.
