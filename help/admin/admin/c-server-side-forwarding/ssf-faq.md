---
description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
uuid: ecd0bc9b-ebf7-414e-88a2-ebba3fd75c92
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 100%

---


# Häufig gestellte Fragen zur serverseitigen Weiterleitung

Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.

## Tracking-Server {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Frage | Antwort |
|--- |--- |
| F: Wie verhält es sich, wenn ich derzeit die alte, Tracking-Server-basierte, serverseitige Weiterleitung verwende? | Die alte, Tracking-Server-basierte, serverseitige Weiterleitungsmethode leitet weiterhin Daten aus Analytics an Audience Manager weiter. Wenn Sie jedoch Audience Manager-Segmente in Analytics senden möchten, ist die neue Report Suite-basierte, serverseitige Weiterleitung erforderlich. Zudem stellt die Aktivierung einer Report Suite für die serverseitige Weiterleitung zusätzlich zur Tracking-Server-Konfiguration keinen Nachteil dar – in allen Konfliktsituationen wird die neue serverseitige Weiterleitungseinstellung der Report Suite verwendet. |
| F: Sollte ich eine Migration von meiner alten Tracking-Server-basierten, serverseitigen Weiterleitung auf die neue Report Suite-basierte, serverseitige Weiterleitung durchführen? | Die Tracking-Server-basierte, serverseitige Weiterleitung wird in absehbarer Zukunft weiterhin unterstützt. Wenn Sie jedoch den Vorteil der Integration von Audience Manager in Analytics (Segmentfreigabe für Analytics) nutzen möchten, müssen Sie die neue Report Suite-basierte, serverseitige Weiterleitung für alle relevanten Report Suites aktivieren. Es besteht jedoch kein triftiger Grund, die alte Tracking-Server-basierte, serverseitige Weiterleitung zu deaktivieren. |

## Taggen und Berichterstellung  {#section_71391BA901AC47B9A2286281644FF281}

| Frage | Antwort |
|--- |--- |
| F: Wie verhält es sich, wenn ich auf meiner Site Multi-Suite-Tagging verwende? Werden meine Serveraufrufe an Audience Manager durch die serverseitige Weiterleitung verdoppelt? | Nein, ein von Analytics an Audience Manager weitergeleiteter Hit wird nur einmal an Audience Manager weitergeleitet. Die Anzahl der Report Suites des Hits ist dabei unerheblich. Wenn Sie für die einzelnen Report Suites des Hits über entsprechende Datenquellen in Audience Manager verfügen, wird jede davon entsprechend aus diesem einen Hit ausgefüllt.  Beachten Sie jedoch, dass Sie die Serveraufrufe an Audience Manager verdoppeln, wenn Sie momentan die clientseitige Datenerfassung (DIL) verwenden und Sie die serverseitige Weiterleitung aktivieren, ohne das Zielgruppen-Management-Modul zu installieren. Dabei ist die Anzahl der Report Suites im Analytics-Hit unerheblich. |
| F: Wie verhält es sich, wenn ich mit mehreren Suites getaggte Report Suites verwende, die separaten Experience Cloud-Org. zugewiesen sind? | Sie sollten nie Daten aus einem einzelnen Analytics-Hit an zwei Report Suites senden, die zu separaten Experience Cloud-Org. gehören. Tritt dieser Fall jedoch ein, wird der Hit nur an die Experience Cloud-Org. weitergeleitet, die mit der Identity Service-Konfiguration auf der Seite übereinstimmt. |
| F: Wie verhält es sich, wenn ich das Multi-Suite-Taggen verwende und nur eine meiner Report Suites meiner Experience Cloud-Org. zugewiesen ist und die andere nicht? | Der Hit wird an den entsprechenden Datenerfassungsserver für die Experience Cloud-Org. der zugewiesenen Report Suite weitergeleitet. Da die nicht zugewiesene Report Suite jedoch keine zugeordnete Datenquelle in Audience Manager hat, werden für die nicht zugewiesene Report Suite in Audience Manager keine Daten aufgezeichnet. |
| F: Wie verhält es sich, wenn ich eine Report Suite verwende, die mehreren Experience Cloud-Org. zugewiesen ist? | Analytics betrachtet diese Report Suite als nicht zugewiesen und lässt nicht zu, dass die serverseitige Weiterleitung für diese Report Suite aktiviert wird. Wenden Sie sich an den Kundendienst, um dieses Zuweisungsproblem zu beheben. |
| F: Ist die Report Suite-basierte, serverseitige Weiterleitungsmethode langsamer als die Tracking-Server-basierte, serverseitige Weiterleitung? | Nein, die Antwortzeit ist dieselbe. |
| F: Wie verhält es sich, wenn ich zwei Experience Cloud-Org. (oder AAM-Instanzen) verwende und Daten zwischen beiden Experience Cloud-Org. freigeben möchte? Kann ich einen einzelnen Analytics-Hit mithilfe der serverseitigen Methode an mehrere Experience Cloud-Org. weiterleiten? | Nein. Wenn Sie unter einer Experience Cloud-Org. erfasste Daten für eine andere Experience Cloud-Org. freigeben müssen, wird empfohlen, die relevanten Zielgruppen mithilfe des Audience Marketplace aus einer Audience Manager-Instanz an eine andere zu senden. |
| F: Führt die serverseitige Weiterleitung zu einer zusätzlichen Rechnungsstellung in Audience Manager oder Analytics? | In Analytics erfolgt keine zusätzliche Rechnungsstellung. In Audience Manager werden weitergeleitete Hits wie andere Hits behandelt und abgerechnet.  Daher ist es wichtig, dass DIL und die serverseitige Weiterleitung nicht gleichzeitig aktiviert sind. Dies könnte zu einer doppelten Rechnungsstellung und einer Duplizierung der Daten führen. |

>[!MORELIKETHIS]
>
>* [Serverseitige Weiterleitung](/help/admin/admin/c-server-side-forwarding/ssf.md)

