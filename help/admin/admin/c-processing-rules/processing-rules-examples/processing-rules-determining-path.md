---
description: Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.
seo-description: Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.
seo-title: Einen Pfad bestimmen, indem Sie einen evar-Wert in eine prop kopieren
solution: Analytics
subtopic: Verarbeitungsregeln
title: Einen Pfad bestimmen, indem Sie einen evar-Wert in eine prop kopieren
topic: Admin Tools
uuid: 8 d 7647 c 7-aa 91-466 b -8 d 31-fb 4 dce 83 f 04 a
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Einen Pfad bestimmen, indem Sie einen evar-Wert in eine prop kopieren

Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.

Beim Festlegen von Werten erhält die Variable links den Wert der Variable rechts (auch wenn dieser Wert leer ist).

| Regelsatz | Wert |
|---|---|
| Bedingung | Keine (immer ausführen) |
| Aktion | Wert von Prop1 durch eVar1 überschreiben |

Sie können diese Regel zur Einstellung des Werts von Prop1 nur dann modifizieren, wenn sie nicht bereits einen Wert ähnlich dem Folgenden enthält:

| Regelsatz | Wert |
|---|---|
| Bedingung | Wenn Prop1 nicht eingestellt ist |
| Aktion | Wert von Prop1 durch eVar1 überschreiben |

Beispiel:

![](assets/overwrite-empty-prop.png)

