---
description: Bei Verwendung einer gängigen Variablen wie „q“ können Sie zum Auffüllen von Suchbegriffen auf Verarbeitungsregeln zurückgreifen, mit denen die eVar für die internen Suchbegriffe mit diesen Suchbegriffen aufgefüllt wird.
subtopic: Processing rules
title: Füllen interner Suchbegriffe mithilfe eines Abfragezeichenfolgenparameters
feature: Admin Tools
uuid: 05ae2b0a-8797-468c-8f59-643beac614c5
exl-id: bc7cc712-0f2a-4260-a82c-ad0e48149e73
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 100%

---

# Füllen interner Suchbegriffe mithilfe eines Abfragezeichenfolgenparameters

Bei Verwendung einer gängigen Variablen wie „q“ können Sie zum Auffüllen von Suchbegriffen auf Verarbeitungsregeln zurückgreifen, mit denen die eVar für die internen Suchbegriffe mit diesen Suchbegriffen aufgefüllt wird.

Für die Nutzung in Verarbeitungsregeln müssen die Werte für die Abfragezeichenfolge in Unicode oder UTF-8 kodiert sein.

| Regelsatz | Wert |
|---|---|
| Bedingung | Falls der Abfragezeichenfolgenparameter „q“ festgelegt ist |
| Aktion | Wert des internen Suchbegriffs durch Abfragezeichenfolgenparameter „q“ überschreiben |

Beispiel:

![](assets/populate-internal-search-terms.png)