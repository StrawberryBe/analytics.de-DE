---
title: Fehlerbehebung beim Versand von Data warehouse-Anfragen
description: Stellen Sie potenzielle Probleme bei einer Data warehouse-Anforderung fest, die die Versand verlängern kann.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Fehlerbehebung beim Versand von Data warehouse-Anfragen

Eine bestimmte Data warehouse-Anforderung kann zwischen einer Stunde und mehreren Tagen dauern. Aus folgenden Gründen ist es schwierig, den genauen Zeitraum für die Bearbeitung einer Anforderung zu schätzen:

* Der Datumsbereich der Anforderung
* Der Traffic, den Ihre Report Suite während des angeforderten Zeitraums erhalten hat
* Die Anzahl der Regeln innerhalb eines Segments und welche Variablen innerhalb eines Segments verwendet werden
* Wie viele Daten sind in das Segment eingeschlossen?
* Die Anzahl der verwendeten Aufschlüsselungen und die Anzahl der eindeutigen Werte in jeder Aufschlüsselung
* Die Anzahl der verwendeten Metriken
* Die Anzahl der gleichzeitig verarbeiteten Anforderungen
* VISTA-Regeln, falls für die Anwendung auf DataWarehouse-Anforderungen konfiguriert

Wenn Sie data warehouse-Anforderungen immer und immer wieder sehen, sollten Sie Ihre Anforderungen ändern, um Folgendes aufzunehmen:

* **Verwenden Sie ein Segment, das eine kleinere Datenstichprobe** enthält: Je weniger Daten eine Anforderung enthält, desto schneller wird ein Bericht zurückgegeben.
* **Anforderungen in Schritten von 14 Tagen oder weniger** ausführen: Kleinere Anforderungen werden schneller verarbeitet als große Anforderungen.
* **Verwenden Sie weniger Aufschlüsselungen:** Viele Aufschlüsselungen in einer Data warehouse-Anforderung erhöhen exponentiell die Verarbeitungszeit.

>[!IMPORTANT]
>
> *Es gibt keine Möglichkeit, den Versand einer Data warehouse-Anfrage zu beschleunigen.*

Wenn Sie diese Berichtstypen zeitnaher benötigen, sollten Sie die folgenden Alternativen in Betracht ziehen:

* **Analysis Workspace**: Obwohl keine unbegrenzten Dimensionselemente verfügbar sind, enthält sie fast alle anderen Anwendungsfälle, die von Data warehouse bereitgestellt werden.
* **Datenfeed**: Übernimmt alle Rohdaten in einer Report Suite täglich und sendet sie an eine FTP-Site. Sie können diese Daten dann in Ihre eigene Datenbank importieren und Abfragen ausführen, um die gesuchten Daten abzurufen.
* **Benutzerdefinierte Engineering Services-Lösung**: Adobe Engineering Services bieten eine individuelle Lösung für Ihr Unternehmen gegen Aufpreis. Weitere Informationen erhalten Sie vom Kundenbetreuer Ihres Unternehmens.
