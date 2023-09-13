---
title: Fehlerbehebung bei Versandzeiten von Data Warehouse-Anforderungen
description: Ermitteln Sie potenzielle Probleme mit einer Data Warehouse-Anforderung, die die Versandzeiten verlängern können.
feature: Data Warehouse
exl-id: eed4d172-fffd-453f-ab5b-0fc2a79d5bd0
source-git-commit: fc6a2deabaf2012cefebf4864db19aef1825adf2
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 61%

---

# Fehlerbehebung bei Versandzeiten von Data Warehouse-Anforderungen

Eine bestimmte Data Warehouse-Anforderung kann zwischen einer Stunde und mehreren Tagen dauern. Aufgrund der folgenden Faktoren ist es schwierig, den genauen Zeitaufwand für die Bearbeitung einer Anforderung abzuschätzen:

* Datumsbereich der Anforderung,
* Traffic-Aufkommen, das Ihre Report Suite während des angeforderten Zeitraums erhalten hat,
* Die Anzahl der Regeln innerhalb eines Segments und welche Variablen innerhalb eines Segments verwendet werden,
* Die Datenmenge innerhalb eines Segments,
* Die Anzahl der verwendeten Aufschlüsselungen und die Anzahl der eindeutigen Werte in jeder Aufschlüsselung,
* Die Anzahl der verwendeten Metriken,
* Die Anzahl der gleichzeitig verarbeiteten Anforderungen,
* VISTA-Regeln, falls für die Anwendung auf Data Warehouse-Anforderungen konfiguriert.

## Anforderungen zur Beschleunigung des Versands ändern

Wenn Data Warehouse-Anfragen konsistent lange dauern, sollten Sie Ihre Anforderungen ändern. Das Ändern einer Anfrage ist die einzige Möglichkeit, die Bereitstellung einer Data Warehouse-Anfrage zu beschleunigen.

Um die Bereitstellung einer Data Warehouse-Anfrage zu beschleunigen, können Sie sie auf eine der folgenden Arten ändern:

* **Verwenden Sie ein Segment, das eine kleinere Stichprobe von Daten enthält**: Je weniger Daten eine Anforderung enthält, desto schneller wird ein Bericht zurückgegeben.
* **Ausführen von Anforderungen in Schritten von 14 Tagen oder weniger**: Kleinere Anforderungen werden schneller verarbeitet als große Anforderungen.
* **Weniger Aufschlüsselungen verwenden:** Viele Aufschlüsselungen in einer Anforderung erhöhen die Verarbeitungszeit exponentiell.

## Alternative Methode verwenden

Wenn Sie diese Art von Berichten schneller benötigen, ziehen Sie die folgenden Alternativen in Betracht:

* **Analysis Workspace**: Obwohl keine unbegrenzten Dimensionselemente verfügbar sind, sind fast alle anderen Anwendungsfälle enthalten, die von Data Warehouse bereitgestellt werden.
* **Daten-Feed**: Nimmt täglich alle Rohdaten in einer Report Suite auf und sendet sie an ein Cloud-Ziel. Sie können dann die Daten in Ihre eigene Datenbank importieren und Abfragen ausführen, um die benötigten Daten abzurufen.
* **Individuelle Engineering Services-Lösung**: Adobe Engineering Services bieten gegen Aufpreis eine individuelle Lösung für Ihr Unternehmen. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team.
