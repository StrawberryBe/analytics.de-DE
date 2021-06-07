---
title: US-Staaten
description: Der US-Bundesstaat des Besuchers.
exl-id: d4506e59-c1ff-4348-912d-c1ad73278f56
source-git-commit: 9770f8e04089ff339d912d1787679257c87c7caa
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 100%

---

# US-Bundesstaat

Die Dimension „US-Bundesstaat“ gibt den Bundesstaat des Besuchers in den USA an. Sie ähnelt der Dimension [Regionen](regions.md), allerdings ist diese Dimension spezifisch für die USA. Die Verwendung dieser Dimension ist hilfreich, wenn Sie Einblicke wünschen, die detaillierter sind als [Länder](countries.md), aber nicht so detailliert wie [Städte](cities.md).

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://info.digitalelement.com/de/) zusammen, um die Suche zwischen IP-Adresse und Land zu unterstützen. Diese Dimension ist bei allen Implementierungen vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören Regionen und das Land, in dem sich die Region befindet. Zu den Beispielwerten gehören `"California"`, `"Texas"` oder `"Virginia"`. Das Dimensionselement `"Unspecified"` umfasst den gesamten internationalen Traffic außerhalb der Vereinigten Staaten.

Diese Dimension kann `"AOL"`, einen DFÜ-Dienstleister umfassen. Abonnenten dieses Dienstes wird ein Zugangspunkt zugewiesen. AOL-Benutzer verwenden die IP-Adresse dieses Zugriffspunkts. Da diese Dimension auf der IP-Adresse basiert, wird die Geolokalisierung des Zugangspunktes anstelle des tatsächlichen Standortes des Besuchers verwendet.

## Unterschiede zwischen gemeldetem und tatsächlichem Standort

Da diese Dimension auf der IP-Adresse basiert, kann in einigen Szenarien ein Unterschied zwischen dem gemeldeten und dem tatsächlichen Standort anzeigt werden:

* **IP-Adressen, die Unternehmensproxys darstellen**: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Standort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Netzbetreibern transportiert den IP-Traffic über zentralisierte oder regionale POPs (Points of Presence).
* **Satelliten-ISP-Benutzer**: Es ist schwierig, den spezifischen Standort dieser Benutzer zu identifizieren, da sie in der Regel vom Uplink-Standort zu stammen scheinen.
* **Militärische und staatliche IPs**: Die Mitarbeiter sind weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind.
