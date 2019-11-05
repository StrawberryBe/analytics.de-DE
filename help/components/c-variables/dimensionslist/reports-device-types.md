---
description: Gruppiert Mobilgeräte in Kategorien wie Mobiltelefone, Tablets, E-Reader, Spielekonsolen, Fernseher, Set-Top-Boxen, Media Player und weitere hochwertige Kategorien, um Ihnen die Verteilung zwischen Mobilgerätetypen zu veranschaulichen.
seo-description: Gruppiert Mobilgeräte in Kategorien wie Mobiltelefone, Tablets, E-Reader, Spielekonsolen, Fernseher, Set-Top-Boxen, Media Player und weitere hochwertige Kategorien, um Ihnen die Verteilung zwischen Mobilgerätetypen zu veranschaulichen.
seo-title: Gerätetypen
solution: Analytics
title: Gerätetypen
topic: Berichte
uuid: e1224769-9a94-4cad-a1ed-e285d60d23f3
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# Gerätetypen

Gruppiert Mobilgeräte in Kategorien wie Mobiltelefone, Tablets, E-Reader, Spielekonsolen, Fernseher, Set-Top-Boxen, Media Player und weitere hochwertige Kategorien, um Ihnen die Verteilung zwischen Mobilgerätetypen zu veranschaulichen.

Diese Dimension ist auch hilfreich, um Segmente für Smartphone- und Tablet-Benutzer zu definieren, indem der Mobilgerätetyp mit dem Gerätetyp identisch ist.

**Dynamische Gerätedaten**

Diese Dimension verwendet dynamische Gerätedaten, die im Zuge der Veröffentlichung und Ermittlung neuer Geräte fortlaufend aktualisiert werden. Ein neues Tablet, das während des aktuellen Monats veröffentlicht wird, könnte beispielsweise fehlerhaft identifiziert werden, da es noch nicht in der Gerätedatenbank vorhanden ist. Wenn das neue Gerät in die Gerätedatenbank aufgenommen wird, werden die sich daraus ergebenden Änderungen auf alle zukünftigen Berichterstellungsdaten angewendet (nicht auf historische Daten). Daher kann es in diesem Bericht bei historischen Daten im Zeitablauf zu leichten Abweichungen kommen. Allgemein gilt, dass der neueste Bericht die genauesten Daten für jeden Berichtszeitraum enthält.

Die Daten für diesen Bericht werden mithilfe der Zeichenfolge des Benutzeragents des Besuchers ausgefüllt.

>[!Note]
>Nur Änderungen an einer vorhandenen mobilen ID sind rückwirkend. Wenn das Gerät neu ist und noch keine mobile ID hat, beginnen die einzigen Daten, die an dieses Gerät gebunden werden, an dem Tag, an dem der Gerätedatenbank eine ID hinzugefügt wird.
