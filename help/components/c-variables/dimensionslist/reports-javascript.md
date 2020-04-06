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

Der JavaScript-Bericht entspricht der Spalte &quot;javascript&quot;in den Rohdaten.

javascript ist ein Feld auf Besuchsebene, daher wird der Wert des ersten Treffers im Besuch beibehalten. Die Spalte &quot;javascript&quot;basiert auf dem ersten Wert in der Spalte &quot;j_jscript&quot;(wie ein visit_Werber nur den ersten Werber des Besuchs beibehalten wird).

j_jscript wird aus dem Parameter j aus der Adobe Analytics-Bildanforderung gefüllt.

Siehe folgendes Beispiel:

| Treffer | j_jscript | javascript |
|---|---|---|
| 1 |  | 0 |
| 2 | 1,6 | 0 |
| 3 | 1,6 | 0 |

Daher ist es nicht wichtig, ob Sie eine JavaScript-Version zu einem bestimmten Zeitpunkt des Besuchs angegeben haben - es wird immer so angezeigt, als ob sie nicht Javascript ist, da der erste Treffer keinen Wert für j_jscript enthielt.
