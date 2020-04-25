---
description: Zeigt Metriken basierend darauf an, ob JavaScript beim Gerät aktiviert oder deaktiviert ist oder ob es als „nicht identifiziert“ gezählt wird.
title: JavaScript-Unterstützung
topic: Reports
uuid: 7b95001a-cd35-478a-8b24-54d30666110d
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# JavaScript-Unterstützung

Zeigt Metriken basierend darauf an, ob JavaScript beim Gerät aktiviert oder deaktiviert ist oder ob es als „nicht identifiziert“ gezählt wird.

>[!NOTE] Anfang November 2016 wird voraussichtlich die Beschränkung aufgehoben, durch die JavaScript immer aufgeführt ist als *`disabled / unidentified`* für Mobilgeräte.

Der JavaScript-Bericht entspricht der Spalte „javascript“ in den Rohdaten.

„javascript“ ist ein Feld auf Besuchsebene, daher bleibt der Wert des ersten Treffers des Besuchs erhalten. Die Spalte „javascript“ basiert auf dem ersten Wert in der Spalte „j_jscript“ (so wie in „visit_referrer“ nur der erste Referrer des Besuchs erhalten bleibt).

„j_jscript“ wird über den Parameter „j“ aus der Adobe Analytics-Bildanforderung gefüllt.

Siehe folgendes Beispiel:

| Treffer | j_jscript | javascript |
|---|---|---|
| 1 |  | 0 |
| 2 | 1,6 | 0 |
| 3 | 1,6 | 0 |

Demzufolge ist es unwichtig, ob Sie an irgendeinem Punkt des Besuchs eine JavaScript-Version festgelegt hatten – es kommt immer zu einer Nicht-JavaScript-Anzeige, weil der erste Treffer keinen Wert für „j_jscript“ enthalten hat.
