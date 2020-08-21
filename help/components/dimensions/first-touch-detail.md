---
title: Erstkontakt-Kanaldetail
description: Details zum ersten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 77%

---


# Erstkontakt-Kanaldetail

Die Dimension „Erstkontakt-Kanaldetail“ enthält Details zum ersten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist nützlich, um zu verstehen, was dazu beigetragen hat, dass der Treffer einem Marketing-Kanal entsprach. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.

## Füllen dieser Dimension mit Daten

Diese Dimension kopiert Werte aus anderen Variablen. Die verwendete Variable referenziert den Kanalwert in jeder [Marketing-Kanalverarbeitungsregel](/help/admin/admin/marketing-channels-admin.md). Wenn ein Treffer mit einer Marketing-Kanalverarbeitungsregel übereinstimmt, wird die Dimension [Letztkontakt-Kanal](last-touch-channel.md) auf den Kanalnamen festgelegt und diese Dimension auf den in der Regel festgelegten Kanalwert gesetzt.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Vergewissern Sie sich, dass sich das gewünschte Dimensionselement in einem Trefferattribut oder einer benutzerspezifischen Variablen befindet.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie den gewünschten Dropdown-Wert in der Marketing-Kanalverarbeitungsregel unter [!UICONTROL Kanalwert setzen].
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind, _und_ der erste Marketing-Kanalwert sein, auf den dies im Interaktionszeitraum des Besuchers zutrifft.

Wenn ein nachfolgender Treffer Kriterien unter einem anderen Marketing-Kanal erfüllt, wird diese Dimension nicht mit dem neuen Marketing-Kanal überschrieben.

## Dimensionen

Elemente der Dimension hängen vom Dropdown-Menü Kanal ab. Wenn Sie beispielsweise den Wert des Kanals auf &quot;Seiten-URL&quot;setzen, enthalten Dimensionselemente Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf Verweisende Domäne einstellen, enthalten Dimensionselemente Domänen, die Besucher durchgeklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension Aggregat alle Detail-Dimensionselemente, unabhängig davon, in welchem Kanal sie sich befinden.

Adobe empfiehlt, Kanalwerte für den Marketing-Kanal festzulegen, um Einblick in die Kanaldetails zu erhalten.
