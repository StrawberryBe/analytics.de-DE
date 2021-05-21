---
title: Vergleich verschiedener Methoden zum Ausschluss von Bots
description: Ermöglicht den Vergleich verschiedener Methoden zum Ausschluss von Bots.
exl-id: c54ba98a-b396-479e-bfe8-dc6211b26f61
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '325'
ht-degree: 100%

---

# Vergleich verschiedener Methoden zum Ausschluss von Bots

Die folgende Tabelle zeigt verschiedene Methoden zum Ausschluss von Bots und wie sie im Vergleich abschneiden.

| Methode | Bot-Regeln | Nach IP-Adresse ausschließen | Kundenattribute | Segmentierung | Bewertung durch Dritte + Segmentierung | Unterdrücken des Server-Aufrufs für Bots zur Laufzeit | Benutzerspezifische DB VISTA-Regel |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Beschreibung der Methode zum Ausschluss von Daten** | Ausschluss basierend auf Benutzer-Agent, IP-Adresse oder IP-Adressbereich | IP-Adresse | Eine Markierung in Kundenattributen, die ECID als Bot identifiziert | Kriterien in einem Analytics-Segment, das bekannte Bots basierend auf dem Verhalten von Bots identifiziert | Ein Drittanbieter wie z. B. [Perimeter X](https://www.perimeterx.com) oder [Akamai Bot Manager](https://www.akamai.com/de/de/products/security/bot-manager.jsp) weist jeder Seitenansicht einen Wert zu, der angibt, mit welcher Wahrscheinlichkeit es sich um einen Bot handelt. Die Bewertung wird an Analytics gesendet und Segmente können verwendet werden, um Daten basierend auf dem Ergebnis auszufiltern. | Client-seitige Logik verhindert, dass der Server-Aufruf von Analytics für Bots ausgeführt wird. | Eine VISTA-Regel verschiebt Traffic von Bots, die bestimmte Kriterien erfüllen, in eine separate Report Suite. |
| **Sind Bot-Namen für das Reporting verfügbar?** | Ja | Nein | Nein | Nein | Nein | Nein | Ja |
| **Kann angezeigt werden, welche Seiten von Bots besucht werden?** | Ja | Nein | Nein | Nein | Ja | Nein | Ja |
| &#x200B;**Entstehen Kosten für Server-Aufrufe wegen Bots?** | Ja | Ja | Ja | Ja | Ja | Nein | Ja |
| **Sind Bot-Daten in Daten-Feeds verfügbar?** | Nein | Nein | Ja | Ja | Ja | Nein | Ja |
| **Ist es möglich, Berichte zu Traffic durch Bots zu erstellen, als ob es sich um tatsächliche Server-Aufrufe handelt?** | Nein | Nein | Ja | Ja | Ja | Ja | Nein |
| **Können Daten nachträglich aus einem Datensatz entfernt werden?** | Nein | Nein | Ja, nachdem deklarierte IDs implementiert wurden | Ja | Ja, sobald die Bewertungen implementiert wurden | Nein | Nein |
| **Gibt es bei den Kriterien Beschränkungen für Unique-Werte?** | Nein | Nein | Nein | Ja | Nein | Nein | Nein |
| **Fallen zusätzliche Kosten an?** | Nein | Nein | Möglich, je nach Analytics-SKU | Nein | Ja | Nein | Ja – es gibt Kosten für die Implementierung und Pflege einer VISTA-Regel |
