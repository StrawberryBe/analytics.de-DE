---
title: Gerätediagramm
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen der Datenzuordnung mithilfe des Gerätediagramms vertraut.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
source-git-commit: f7106ca52447988c90a3ccac6a1e1cc7514f1fc9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 69%

---

# Gerätediagramm

Geräteübergreifende Analysen können das private Diagramm verwenden, um Daten miteinander zu verknüpfen. Das private Diagramm ist ein Repository mit Hash-Geräte-IDs, das für Ihr Unternehmen spezifisch ist. Die geräteübergreifende Analyse kommuniziert regelmäßig mit dem Gerätediagramm, um Geräte miteinander zu verknüpfen.

## Besondere Voraussetzungen für das Gerätediagramm

Wenn Sie die geräteübergreifende Analyse mithilfe der Gerätediagrammmethode implementieren möchten, ist Folgendes erforderlich. Arbeiten Sie mit Teams in Ihrer Organisation und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie alle folgenden Kriterien erfüllen.

>[!WARNING]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.

* Alle auf der [Übersichtsseite](overview.md) aufgeführten Voraussetzungen.
* Ihr Unternehmen muss [Adobe Experience Platform Identity Service - Privates Diagramm](https://business.adobe.com/products/experience-platform/identity-service.html). Siehe auch [Startseite](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=de) im Benutzerhandbuch zu Identity Service.
* Ihre Implementierung muss die neueste Version des Experience Cloud ID-Diensts (ECID) verwenden. Siehe [Startseite](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de) im Benutzerhandbuch zum ID-Dienst. Die meisten Implementierungen mit [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=de) in Adobe Experience Platform wahrscheinlich bereits ID-Dienst bereitgestellt ist.
* Ihre Implementierung muss die `setCustomerIDs`-Funktion (oder das SDK-Äquivalent) immer dann aufrufen, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Siehe [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html?lang=de) im Benutzerhandbuch zum ID-Dienst.

## Besondere Einschränkungen für das Gerätediagramm

* Veraltete Analytics-IDs werden nicht unterstützt. Nur Besucher mit Experience Cloud IDs werden zugeordnet.
* Wenn Ihr Unternehmen ein privates Diagramm verwendet, dauert es bis zu 24 Stunden, bis neue Geräte zugeordnet werden.
* Gerätediagramme von Drittanbietern werden nicht unterstützt.

## Nächste Schritte

Sobald Ihre Organisation alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie mit der [Einrichtung der geräteübergreifenden Analyse](setup.md) beginnen.
