---
description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
subtopic: Processing rules
title: Füllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter
topic: Admin tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Füllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter

Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.

In den meisten Fällen erfolgt das Auffüllen von Variablen aus der Abfragezeichenfolge über ein Plug-in. Wenn das Auffüllen aufgrund eines Schreibfehlers oder einer vergleichbaren Ursache fehlschlägt, können Sie die Variable mit Hilfe von Verarbeitungsregeln auffüllen.

Prüfen Sie vor dem Überschreiben stets nach, ob ein Wert leer ist oder den erwarteten Wert enthält.

| Regelsatz | Wert |
|---|---|
| Bedingung | Kampagne nicht festgelegt |
| Aktion | Kampagnenwert durch Abfragezeichenfolgenparameter „cpid“ überschreiben |

Beispiel:

![](assets/set-campaign-conditionally.png)

