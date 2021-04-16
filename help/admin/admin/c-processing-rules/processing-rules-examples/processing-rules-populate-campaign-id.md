---
description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
subtopic: Processing rules
title: Füllen einer Kampagnen-ID aus einem Abfragezeichenfolgenparameter
feature: Admin Tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
exl-id: 526d2727-b7f6-4b41-be86-e5f5bc5e6c2b
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '114'
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
