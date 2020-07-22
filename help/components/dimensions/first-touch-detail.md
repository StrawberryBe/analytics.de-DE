---
title: First Touch-Kanal
description: Details zum ersten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---


# First Touch-Kanal

Die Dimension &quot;First Touch-Kanal-Detail&quot;enthält Details zum ersten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist wertvoll, um zu verstehen, was zum Trefferabgleich eines Marketing-Kanals beigetragen hat. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal für gebührenpflichtige Suchen übereinstimmt, können Sie mithilfe der Angaben zum Kanal sehen, welche Suchmaschine verwendet wurde oder nach welchem Suchbegriff sie gesucht hat.

## Diese Dimension mit Daten füllen

Diese Dimension kopiert Werte aus anderen Variablen. Die verwendete Variable referenziert den Kanal-Wert in jeder [Marketing Kanal-Verarbeitungsregel](/help/admin/admin/marketing-channels-admin.md). Wenn ein Treffer mit einer Verarbeitungsregel des Marketing-Kanals übereinstimmt, wird die Dimension &quot; [Last Touch-Kanal](last-touch-channel.md) &quot;auf den Kanal-Namen festgelegt und diese Dimension auf den in der Regel festgelegten Kanal-Wert gesetzt.

Wenn Sie diese Dimension auf einen bestimmten Wert setzen möchten, sind die folgenden Schritte erforderlich:

* Vergewissern Sie sich, dass sich das gewünschte Dimensionselement in einem Trefferattribut oder einer benutzerspezifischen Variablen befindet.
* Legen Sie eine Verarbeitungsregel für den Marketing Kanal fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie den gewünschten Dropdown-Wert unter [!UICONTROL Legen Sie den Wert] des Kanals in der Verarbeitungsregel Marketing Kanal fest.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Verarbeitungsregel für den Marketing-Kanal beschrieben sind, _und_ muss der erste Marketingwert sein, der dies im Interaktionszeitraum des Besuchers tut.

Wenn ein nachfolgender Treffer Kriterien unter einem anderen Marketing-Kanal erfüllt, wird diese Dimension nicht mit dem neuen Marketing-Kanal überschrieben.

## Dimensionselemente

Dimensionselemente hängen vom Dropdown-Menü &quot;Kanal&quot;ab. Wenn Sie beispielsweise den Wert des Kanals auf &quot;Seiten-URL&quot;setzen, enthalten Dimensionselemente Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf Verweisende Domäne einstellen, enthalten Dimensionselemente Domänen, die Besucher durchgeklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension Aggregat alle Detail-Dimensionselemente, unabhängig davon, in welchem Kanal sie sich befinden.

Adobe empfiehlt die Festlegung von Kanal-Werten für den Marketing-Kanal, um Einblicke in Details zu Kanälen zu erhalten.
