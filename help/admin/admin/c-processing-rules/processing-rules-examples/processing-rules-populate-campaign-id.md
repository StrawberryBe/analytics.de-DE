---
description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
subtopic: Processing rules
title: Füllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter
topic: Admin tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
translation-type: tm+mt
source-git-commit: 2ffa989156dd9bc4f6ef9a216e8c06425cc39440
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 100%

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

