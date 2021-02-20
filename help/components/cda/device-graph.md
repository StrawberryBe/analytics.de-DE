---
title: Gerätediagramm
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen der Datenzuordnung mithilfe des Gerätediagramms vertraut.
translation-type: tm+mt
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 100%

---


# Gerätediagramm

Cross-Device Analytics bietet zwei verschiedene Methoden der Datenzuordnung. Diese Methode verwendet das Co-op-Diagramm oder das private Diagramm des Adobe Experience Platform Identity Service, um Daten zuzuordnen. Die geräteübergreifende Analyse kommuniziert regelmäßig mit dem Gerätediagramm, um Geräte miteinander zu verknüpfen.

## Unterschiede zwischen Co-op-Diagramm und privatem Diagramm

Adobe bietet im Rahmen des ID-Dienstes zwei Arten von Gerätediagrammen an:

* **Co-op-Diagramm**: Ein Repository mit Hash-Geräte-IDs, zu dem jeder Kunde beitragen und auf das er verweisen kann. Da diese Art von Gerätediagramm kollaborativ ist, entspricht es normalerweise mehr Geräten als ein privates Diagramm.
* **Privates Diagramm**: Ein Repository mit Hash-Geräte-IDs, auf das nur Ihr Unternehmen verweist.

## Besondere Voraussetzungen für das Gerätediagramm

Wenn Sie die geräteübergreifende Analyse mithilfe der Gerätediagrammmethode implementieren möchten, ist Folgendes erforderlich. Arbeiten Sie mit Teams in Ihrer Organisation und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie alle folgenden Kriterien erfüllen.

>[!IMPORTANT]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.

* Alle auf der [Übersichtsseite](overview.md) aufgeführten Voraussetzungen.
* Ihre Organisation muss das Co-op-Diagramm oder das private Diagramm des Identity Service der Adobe Experience Platform verwenden. Weitere Informationen finden Sie unter [Startseite](https://docs.adobe.com/content/help/de-DE/device-co-op/using/home.html) im Benutzerhandbuch zur Co-op-Funktion des Geräts.
* Ihre Implementierung muss die aktuelle Version des Experience Cloud Identity Service verwenden. Weitere Informationen finden Sie unter [Startseite](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) im Benutzerhandbuch des Experience Cloud ID-Dienstes. Bei den meisten Implementierungen mit Adobe Experience Platform Launch ist ECID wahrscheinlich bereits bereitgestellt.
* Ihre Implementierung muss die `setCustomerIDs`-Funktion (oder das SDK-Äquivalent) immer dann aufrufen, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Weitere Informationen finden Sie unter [`setCustomerIDs`](https://docs.adobe.com/content/help/de-DE/id-service/using/id-service-api/methods/setcustomerids.html) im Benutzerhandbuch des Experience Cloud Identity Service.

## Besondere Einschränkungen für das Gerätediagramm

* Veraltete Analytics-IDs werden nicht unterstützt. Nur Besucher mit Experience Cloud IDs werden zugeordnet.
* Wenn Ihr Unternehmen ein privates Diagramm verwendet, dauert es bis zu 24 Stunden, bis neue Geräte zugeordnet werden.
* Wenn Ihr Unternehmen das Co-op-Diagramm verwendet, kann es bis zu zwei Wochen dauern, bis neue Geräte, die Ihre Site besuchen, zugeordnet werden. Die Zuordnungsrate in der geräteübergreifenden Analyse in den letzten zwei Wochen ist in der Regel niedriger als in Datumsbereichen, die älter als zwei Wochen sind.
* Gerätediagramme von Drittanbietern werden nicht unterstützt.

## Nächste Schritte

Sobald Ihre Organisation alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie mit der [Einrichtung der geräteübergreifenden Analyse](setup.md) beginnen.

