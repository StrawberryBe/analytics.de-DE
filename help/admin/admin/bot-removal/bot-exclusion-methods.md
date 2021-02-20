---
title: Vergleich verschiedener Methoden zum Ausschluss von Boten
description: Ermöglicht den Vergleich verschiedener Methoden zum Ausschluss von Bots.
translation-type: tm+mt
source-git-commit: 76ee4a8db49765590e7cca864d6d4b152d7ba112
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 19%

---


# Vergleich verschiedener Methoden zum Ausschluss von Boten

Die folgende Tabelle zeigt verschiedene Methoden zum Ausschluss von Bots und wie diese gegeneinander stapeln.

| Methode | Bot-Regeln | Nach IP-Adresse ausschließen  | Kundenattribute | Segmentierung | Bewertung durch Dritte + Segmentierung | Unterdrücken der &#x200B; für Bots zur Laufzeit | Benutzerspezifische DB VISTA-Regel |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Beschreibung der Methode zum Ausschluss von Daten** | &#x200B; Ausschließen je nach Benutzeragent, IP-Adresse oder IP-Adressbereich | IP-Adresse | &#x200B; einer Kennzeichnung in Kundenattributen, die ECID als Bot identifiziert | &#x200B; Kriterien in einem Analytics-Segment, das bekannte Bots basierend auf dem Bot-Verhalten identifiziert | &#x200B; einem Drittanbieter wie z. B. [Perimeter X](https://www.perimeterx.com) oder [Akamai Bot Manager](https://www.akamai.com/us/en/products/security/bot-manager.jsp) weist jeder Ansicht eine Bewertung zu, wie wahrscheinlich ein Bot sein soll. Die Bewertung wird an Analytics gesendet und Segmente können verwendet werden, um Daten basierend auf dem Ergebnis auszufiltern. | &#x200B; clientseitige Logik verhindert, dass der Analytics-Server-Aufruf für Bots ausgeführt wird. | &#x200B; Eine VISTA-Regel verschiebt Traffic von Bots, die bestimmte Kriterien erfüllen, in eine separate Report Suite. |
| **&#x200B; Bot-Namen sind für den Berichte verfügbar?** | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
| **&#x200B; Sie sehen können, welche Seiten von Bots besucht werden?** | Ja | Nein | Nein | Nein | Ja | Nein | Ja |
| &#x200B;**Incurs server call cost for bots?** | Ja | Ja | Ja | Ja | Ja | Nein | Ja |
| **Bot-Daten in Data Feeds verfügbar?** | Nein | Nein | Ja | Ja | Ja | Nein | Ja |
| **Kann &#x200B; Berichte zum Bot-Traffic so erstellen, als wären sie echte Server-Aufrufe?** | Nein | Nein | Ja | Ja | Ja | Ja | Nein |
| **Können Daten nachträglich aus einem Datensatz entfernt werden?** | Nein | Nein | &#x200B; Ja, nachdem deklarierte IDs implementiert wurden | Ja | Ja, sobald Ergebnisse implementiert sind | Nein | Nein |
| **Unterliegt es in Kriterien individuellen Beschränkungen?** | Nein | Nein | Nein | Ja | Nein | Nein | Nein |
| **Ist &#x200B; mit zusätzlichen Kosten verbunden?** | Nein | Nein | &#x200B; möglich, je nach Analytics-SKU | Nein | Ja | Nein | &#x200B; Ja - Kosten für die Implementierung und Pflege einer VISTA-Regel |
