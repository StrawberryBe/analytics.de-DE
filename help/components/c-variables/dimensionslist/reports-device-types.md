---
description: Gruppiert Mobilgeräte in Kategorien wie Mobiltelefone, Tablets, E-Reader, Spielekonsolen, Fernseher, Set-Top-Boxen, Media Player und weiteren hochwertigen Kategorien, um Ihnen die Verteilung zwischen Mobilgerätetypen zu veranschaulichen.
title: Gerätetypen
topic: Reports
uuid: e1224769-9a94-4cad-a1ed-e285d60d23f3
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Gerätetypen

Gruppiert Mobilgeräte in Kategorien wie Mobiltelefone, Tablets, E-Reader, Spielekonsolen, Fernseher, Set-Top-Boxen, Media Player und weiteren hochwertigen Kategorien, um Ihnen die Verteilung zwischen Mobilgerätetypen zu veranschaulichen.

Diese Dimension hilft auch bei der Definition von Segmenten für Telefon- und Tablet-Nutzer durch Segmentierung, wobei „Mobilgerätetyp“ identisch mit „Gerätetyp“ verwendet wird.

**Dynamische Gerätedaten**

Diese Dimension verwendet dynamische Gerätedaten, die im Zuge der Veröffentlichung und Ermittlung neuer Geräte fortlaufend aktualisiert werden. Beispielsweise kann ein neues Tablet, das während des aktuellen Monats veröffentlicht wird, fehlerhaft identifiziert werden, da es in der Gerätedatenbank noch nicht vorhanden ist. Wenn das neue Gerät in die Gerätedatenbank aufgenommen wird, werden die sich daraus ergebenden Änderungen auf alle zukünftigen Berichterstellungsdaten angewendet (nicht auf historische Daten). Daher kann es in diesem Bericht bei historischen Daten im Zeitablauf zu leichten Abweichungen kommen. Allgemein gilt, dass der neueste Bericht die genauesten Daten für jeden Berichtszeitraum enthält.

Die Daten für diesen Bericht werden mithilfe der Zeichenfolge des Benutzeragents des Besuchers ausgefüllt.

>[!NOTE]
>Nur Änderungen an einer bestehenden mobilen ID werden rückwirkend vorgenommen. Wenn das Gerät neu ist und noch keine mobile ID hat, beginnen die nur mit diesem Gerät verbundenen Daten mit dem Datum, an dem eine ID zur Gerätedatenbank hinzugefügt wird.
