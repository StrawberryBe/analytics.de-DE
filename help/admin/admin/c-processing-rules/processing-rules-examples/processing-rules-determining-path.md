---
description: Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.
seo-description: Sie können den Wert einer eVar-Variable in eine Prop kopieren, um die Pfadsetzung zu aktivieren.
seo-title: Pfad durch Kopieren eines eVar-Werts in eine Eigenschaft bestimmen
solution: Analytics
subtopic: Verarbeitungsregeln
title: Pfad durch Kopieren eines eVar-Werts in eine Eigenschaft bestimmen
topic: Admin Tools
uuid: 8d7647c7-aa91-466b-8d31-fb4dce83f04a
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Pfad durch Kopieren eines eVar-Werts in eine Eigenschaft bestimmen

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

