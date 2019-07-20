---
description: Um die Genauigkeit von Daten zu beurteilen, werden Daten aus einem Bericht mit bekannten und nachprüfbaren Datenpunkten verglichen.
keywords: Analytics-Implementierung
seo-description: Um die Genauigkeit von Daten zu beurteilen, werden Daten aus einem Bericht mit bekannten und nachprüfbaren Datenpunkten verglichen.
seo-title: Validierung der Genauigkeit von Daten
solution: Analytics
title: Validierung der Genauigkeit von Daten
topic: Entwickler und Implementierung
uuid: 267 f 6 c 61-705 a -41 cf -9 e 09-4 e 2 ce 2331 f 32
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Validierung der Genauigkeit von Daten

Um die Genauigkeit von Daten zu beurteilen, werden Daten aus einem Bericht mit bekannten und nachprüfbaren Datenpunkten verglichen.

Diese Beurteilung sollte von Mitarbeitern von Adobe durchgeführt werden, vorzugsweise vom Adobe-Berater (der mit den technischen Details der Implementierung am besten vertraut ist).

Nachfolgend sind die bevorzugten Datenpunkte für die Beurteilung in der Reihenfolge ihrer Priorität aufgeführt:

* (Econversion-Sites) Vergleich von econversion-Bestellungen eines einzelnen Tages
* Vergleich bekannter Erfolgsereignisse (insbesondere protokollierte Daten, bei denen die zugehörigen Angaben zur IP-Adresse und zum Browser, die für gewöhnlich in Webserverprotokollen gespeichert werden, mit den erfassten Daten verglichen werden können)
* Vergleich von Seitenansichten

>[!NOTE]
>
>Default pages, such as [!DNL index.html], often receive automated or monitoring traffic. Bei solchen Seiten treten bei der browserbasierten Datenerfassung größere Unterschiede als bei anderen besuchten Seiten auf.

Für alle drei Arten von Beurteilung muss für den fraglichen Zeitraum ein Debugprotokoll oder ein Datenfeed vorhanden sein. Dieser Zeitraum beträgt für gewöhnlich maximal einen Tag.

Bestellungen oder Erfolgsereignisse bei normalen JavaScript-basierten Implementierungen sollten mit einer Genauigkeit von 2 bis 3 % des tatsächlichen Wertes (manchmal sogar noch genauer) gemessen werden können. Dabei wird von einer SSL-Seite ausgegangen, da SSL-Seiten viel seltener zwischengespeichert werden und definitionsgemäß überhaupt nicht zwischengespeichert werden sollten. Bei Implementierungen mit komplett serverseitigen Bildanforderungen auf einer SSL-Seite sollte die Genauigkeit zwischen 0 und 1 % der tatsächlichen Werte liegen. Bei nicht sicheren Seiten können die Unterschiede größer sein, sollten jedoch immer noch weniger als 5 % betragen.

Beim Vergleich von Seitenansichten für einen einzigen Zeitraum ist zu erwarten, dass die Seitenansichten innerhalb von 5 % der tatsächlichen Werte liegen (Datenverkehr zu Überwachungszwecken – wie Keynote oder WhatsUpGold – oder automatisierter Datenverkehr – von Spiders, Bots und Skripten – nicht mitgerechnet).

Beim Vergleich der Genauigkeit von Daten müssen die folgenden Punkte berücksichtigt werden:

* QA oder andere Typen von internen Tests, die von IP-Adress- oder VISTA-Regeln gefiltert werden können
* „Smart Tags“, die Tags nur bei bestimmten Arten von Bestellungen oder Datenverkehr generieren
* Bei Abfragen zu Vergleichszwecken muss zudem berücksichtigt werden, was von der Website gemessen wird (z. B. Rückgaben nicht inklusive, Bestellungen, die von Mitarbeitern des Kundendienstes stammen, oder sonstige Besonderheiten).
* Stellen Sie sicher, dass die Zeitzone bei der Abfrage und der Report Suite übereinstimmt.
* Benutzerspezifischer Keynote- oder ähnlicher Datenverkehr (Keynote-Transaktion usw.), der beim Messen des Bestellprozesses anfällt, kann in Tags wiedergegeben, in Bestellsystemen jedoch entfernt sein.
* Berücksichtigen Sie auch die De-Duping-Prozesse des Kunden.
* Erneutes Laden der Bestellseite (Bestellungen werden mittels *`purchaseID`*).

