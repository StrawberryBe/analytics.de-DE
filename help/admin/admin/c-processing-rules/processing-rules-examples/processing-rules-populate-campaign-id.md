---
description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
seo-description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
seo-title: Auffüllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter
solution: Analytics
subtopic: Verarbeitungsregeln
title: Auffüllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter
topic: Admin Tools
uuid: 2 bc 61 f 9 f-d 8 d 2-41 b 7-bd 39-4 a 9 df 30 ff 013
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Auffüllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter

Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.

In den meisten Fällen erfolgt das Auffüllen von Variablen aus der Abfragezeichenfolge über ein Plug-in. Wenn das Auffüllen aufgrund eines Schreibfehlers oder einer vergleichbaren Ursache fehlschlägt, können Sie die Variable mit Hilfe von Verarbeitungsregeln auffüllen.

Prüfen Sie vor dem Überschreiben stets nach, ob ein Wert leer ist oder den erwarteten Wert enthält.

| Regelsatz | Wert |
|---|---|
| Bedingung | Kampagne nicht festgelegt |
| Aktion | Kampagnenwert durch Abfragezeichenfolgenparameter „cpid“ überschreiben |

Beispiel:

![](assets/set-campaign-conditionally.png)

