---
description: Zeigt Metriken basierend darauf an, ob JavaScript beim Gerät aktiviert oder deaktiviert ist oder ob es als „nicht identifiziert“ gezählt wird.
seo-description: Zeigt Metriken basierend darauf an, ob JavaScript beim Gerät aktiviert oder deaktiviert ist oder ob es als „nicht identifiziert“ gezählt wird.
seo-title: JavaScript-Unterstützung
solution: Analytics
title: JavaScript-Unterstützung
topic: 'Berichte    '
uuid: 7 b 95001 a-cd 35-478 a -8 b 24-54 d 30666110 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# JavaScript-Unterstützung

Zeigt Metriken basierend darauf an, ob JavaScript beim Gerät aktiviert oder deaktiviert ist oder ob es als „nicht identifiziert“ gezählt wird.

>[!NOTE]
>
>In early November 2016, we plan to remove the restriction where JavaScript is always listed as *`disabled / unidentified`* for Mobile devices.

Der JavaScript-Bericht entspricht der Spalte „javascript“ in den Rohdaten.

„javascript“ ist ein Feld auf Besuchsebene, daher bleibt der Wert des ersten Treffers des Besuchs erhalten. Die Spalte „javascript“ basiert auf dem ersten Wert in der Spalte „j_jscript“ (so wie in „visit_referrer“ nur der erste Referrer des Besuchs erhalten bleibt).

„j_jscript“ wird über den Parameter „j“ aus der Adobe Analytics-Bildanforderung gefüllt.

Siehe folgendes Beispiel:

| Treffer | j_jscript | javascript |
|---|---|---|
| 1 |  | 0 |
| 2 | 1.6 | 0 |
| 3 | 1.6 | 0 |

Demzufolge ist es unwichtig, ob Sie an irgendeinem Punkt des Besuchs eine JavaScript-Version festgelegt hatten – es kommt immer zu einer Nicht-JavaScript-Anzeige, weil der erste Treffer keinen Wert für „j_jscript“ enthalten hat.
