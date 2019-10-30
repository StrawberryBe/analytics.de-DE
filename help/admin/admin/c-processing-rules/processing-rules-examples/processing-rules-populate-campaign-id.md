---
description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
seo-description: Sie können eine Variable mithilfe eines Abfragezeichenfolgenparameters auffüllen.
seo-title: Kampagnen-ID-Einträge aus einem Abfragezeichenfolgen-Parameter auffüllen
solution: Analytics
subtopic: Verarbeitungsregeln
title: Kampagnen-ID-Einträge aus einem Abfragezeichenfolgen-Parameter auffüllen
topic: Admin Tools
uuid: 2bc61f9f-d8d2-41b7-bd39-4a9df30ff013
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

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

