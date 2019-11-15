---
description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
solution: Analytics
subtopic: Processing rules
title: Kampagnen-ID-Einträge aus einem Abfragezeichenfolgen-Parameter auffüllen
topic: Admin tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Kampagnen-ID-Einträge aus einem Abfragezeichenfolgen-Parameter auffüllen

Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.

In den meisten Fällen erfolgt das Auffüllen von Variablen aus der Abfragezeichenfolge über ein Plug-in. Wenn das Auffüllen aufgrund eines Schreibfehlers oder einer vergleichbaren Ursache fehlschlägt, können Sie die Variable mit Hilfe von Verarbeitungsregeln auffüllen.

Prüfen Sie vor dem Überschreiben stets nach, ob ein Wert leer ist oder den erwarteten Wert enthält.

| Regelsatz | Wert |
|---|---|
| Bedingung | Kampagne nicht festgelegt |
| Aktion | Kampagnenwert durch Abfragezeichenfolgenparameter „cpid“ überschreiben |

Beispiel:

![](assets/set-campaign-conditionally.png)

