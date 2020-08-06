---
title: Gerätediagramm
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen des Zusammenführens von Daten mithilfe des Gerätediagramms vertraut.
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 39%

---


# Gerätediagramm

Geräteübergreifende Analytics bietet zwei verschiedene Methoden zum Zusammenfügen von Daten. Diese Methode verwendet das Adobe Experience Platform Identity Service Co-op Graph oder Private Graph, um Daten zu verbinden. CDA kommuniziert regelmäßig mit dem Gerätediagramm, um Geräte miteinander zu verknüpfen.

## Unterschiede zwischen Co-op-Diagramm und privatem Diagramm

Adobe Angebot zwei Gerätetypen als Teil des ID-Diensts:

* **Koop-Diagramm**: Ein Repository mit Hash-Geräte-IDs, zu dem jeder Kunde beitragen und darauf verweisen kann. Da diese Art von Gerätediagramm kollaborativ ist, stimmt sie in der Regel mit mehr Geräten überein als mit einem privaten Diagramm.
* **Privates Diagramm**: Ein Repository mit Hash-Geräte-IDs, auf das nur Ihr Unternehmen verweist.

## Besondere Anforderungen an das Gerätediagramm

Wenn Sie geräteübergreifende Analysen mit der Diagrammmethode des Geräts implementieren möchten, ist Folgendes erforderlich. Arbeiten Sie mit Teams in Ihrer Organisation und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie die folgenden Kriterien alle erfüllen.

>[!IMPORTANT]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.

* Alle auf der [Übersichtsseite](overview.md)aufgelisteten Voraussetzungen.
* Ihre Organisation muss das Co-op-Diagramm oder das private Diagramm des Identity Service der Adobe Experience Platform verwenden. Weitere Informationen finden Sie unter [Startseite](https://docs.adobe.com/content/help/de-DE/device-co-op/using/home.html) im Benutzerhandbuch zur Co-op-Funktion des Geräts.
* Ihre Implementierung muss die neueste Version des Experience Cloud-ID-Diensts verwenden. Weitere Informationen finden Sie unter [Startseite](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) im Benutzerhandbuch des Experience Cloud ID-Dienstes. Bei den meisten Implementierungen mit Adobe Experience Platform Launch ist ECID wahrscheinlich bereits bereitgestellt.
* Your implementation must call the `setCustomerIDs` function (or SDK equivalent) whenever an individual can be identified, such as when a user logs in or opens an email. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. See [`setCustomerIDs`](https://docs.adobe.com/content/help/de-DE/id-service/using/id-service-api/methods/setcustomerids.html) in the Experience Cloud Identity Service user guide.

## Besondere Einschränkungen für das Gerätediagramm

* Veraltete Analytics-IDs werden nicht unterstützt. Nur Besucher mit Experience Cloud IDs werden zugeordnet.
* Wenn Ihr Unternehmen ein privates Diagramm verwendet, dauert die Zusammenführung neuer Geräte bis zu 24 Stunden.
* Wenn Ihr Unternehmen das Co-op-Diagramm verwendet, kann es bis zu zwei Wochen dauern, bis neue Geräte, die Ihre Site besuchen, zugeschnitten werden. Die Zuordnungsrate in der geräteübergreifenden Analyse in den letzten zwei Wochen ist in der Regel niedriger als in Datumsbereichen, die älter als zwei Wochen sind.
* Gerätediagramme von Drittanbietern werden nicht unterstützt.

## Nächste Schritte

Once your organization meets all requirements met and understands the limitations, you can start [Setting up Cross-Device Analytics](setup.md).

