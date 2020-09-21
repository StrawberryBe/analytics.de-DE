---
description: Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.
subtopic: Processing rules
title: Bestimmen eines Pfads durch Kopieren eines eVar-Werts in eine Eigenschaft
topic: Admin tools
uuid: 8d7647c7-aa91-466b-8d31-fb4dce83f04a
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: ht
source-wordcount: '128'
ht-degree: 100%

---


# Bestimmen eines Pfads durch Kopieren eines eVar-Werts in eine Eigenschaft

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

