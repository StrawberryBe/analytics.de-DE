---
description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
seo-description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
seo-title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
uuid: ecd 0 bc 9 b-ebf 7-414 e -88 a 2-ebba 3 fd 75 c 92
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Häufig gestellte Fragen zur serverseitigen Weiterleitung

Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.

## Tracking-Server {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Frage | Antwort |
|--- |--- |
| F: Wie verhält es sich, wenn ich derzeit die alte, Tracking-Server-basierte, serverseitige Weiterleitung verwende? | Die alte, Tracking-Server-basierte, serverseitige Weiterleitungsmethode leitet weiterhin Daten aus Analytics an Audience Manager weiter. Wenn Sie jedoch Audience Manager-Segmente in Analytics senden möchten, ist die neue Report Suite-basierte, serverseitige Weiterleitung erforderlich. Zudem stellt die Aktivierung einer Report Suite für die serverseitige Weiterleitung zusätzlich zur Tracking-Server-Konfiguration keinen Nachteil dar – in allen Konfliktsituationen wird die neue serverseitige Weiterleitungseinstellung der Report Suite verwendet. |
| F: Sollte ich eine Migration von meiner alten Tracking-Server-basierten, serverseitigen Weiterleitung auf die neue Report Suite-basierte, serverseitige Weiterleitung durchführen? | Die Tracking-Server-basierte, serverseitige Weiterleitung wird in absehbarer Zukunft weiterhin unterstützt. Wenn Sie jedoch den Vorteil der Integration von Audience Manager in Analytics (Segmentfreigabe für Analytics) nutzen möchten, müssen Sie die neue Report Suite-basierte, serverseitige Weiterleitung für alle relevanten Report Suites aktivieren. Es besteht jedoch kein triftiger Grund, die alte Tracking-Server-basierte, serverseitige Weiterleitung zu deaktivieren. |

## Taggen und Berichterstellung {#section_71391BA901AC47B9A2286281644FF281}

| Frage | Antwort |
|--- |--- |
| F: Wie verhält es sich, wenn ich auf meiner Site das Multi-Suite-Taggen verwende? Werden meine Serveraufrufe an Audience Manager durch die serverseitige Weiterleitung verdoppelt? | Nein, ein von Analytics an Audience Manager weitergeleiteter Treffer wird nur einmal an Audience Manager weitergeleitet. Die Anzahl der Report Suites bei dem Treffer ist dabei unerheblich. Wenn Sie für die einzelnen Report Suites des Treffers über entsprechende Datenquellen in Audience Manager verfügen, werden sie jeweils über den einzelnen Treffer gefüllt.  Beachten Sie jedoch, dass Sie die Serveraufrufe an Audience Manager verdoppeln, wenn Sie momentan die clientseitige Datenerfassung (DIL) verwenden und Sie die serverseitige Weiterleitung aktivieren, ohne das Zielgruppen-Management-Modul zu installieren. Dabei ist die Anzahl der Report Suites im Analytics-Treffer unerheblich. |
| Q: Was passiert, wenn Multi-Suite-Tagged Report Suites zugeordnet sind, die separaten Experience Cloud-Orgs zugeordnet sind? | Sie sollten niemals Daten aus einem einzelnen Analytics-Treffer an zwei Report Suites senden, die zu getrennten Experience Cloud-Orgs gehören. Wenn dies jedoch geschieht, leiten wir den Treffer nur an Experience Cloud-Org weiter, der auf der Seite eingerichtet ist. |
| Q: Was ist, wenn ich Multi-Suite-Tagging habe und nur eine meiner Report Suites meiner Experience Cloud Org zugeordnet ist und die andere nicht? | Wir leiten den Treffer an den entsprechenden Datenerfassungsserver für die Experience Cloud-Org in Ihrer zugeordneten Report Suite weiter. Da die nicht zugeordnete Report Suite in Audience Manager keine zugehörige Datenquelle aufweist, werden keine Daten für die nicht zugeordnete Report Suite in Audience Manager aufgezeichnet. |
| Q: Was ist, wenn ich eine Report Suite habe, die mehreren Experience Cloud-Orgs zugeordnet ist? | Analytics betrachtet diese Report Suite als nicht zugewiesen und lässt nicht zu, dass die serverseitige Weiterleitung für diese Report Suite aktiviert wird. Wenden Sie sich an den Kundendienst, um dieses Zuweisungsproblem zu beheben. |
| F: Ist die Report Suite-basierte, serverseitige Weiterleitungsmethode langsamer als die Tracking-Server-basierte, serverseitige Weiterleitung? | Nein, die Antwortzeit ist dieselbe. |
| Q: Was passiert, wenn wir zwei Experience Cloud-Orgs (oder AAM-Instanzen) haben und Daten zwischen Experience Cloud-Orgs freigeben möchten? Kann ein einzelner Analytics-Treffer auf mehrere Experience Cloud-Orgs weitergeleitet werden? | Nein. Wenn Sie Daten freigeben müssen, die mit einer Experience Cloud-Org in eine andere Experience Cloud-Org erfasst werden, empfehlen wir, alle zutreffenden Zielgruppen von einer Audience Manager-Instanz in eine andere Instanz mit dem Audience Marketplace zu senden. |
| F: Führt die serverseitige Weiterleitung zu einer zusätzlichen Rechnungsstellung in Audience Manager oder Analytics? | In Analytics erfolgt keine zusätzliche Rechnungsstellung. In Audience Manager werden weitergeleitete Treffer wie andere Treffer behandelt und abgerechnet.  Daher ist es wichtig, dass DIL und die serverseitige Weiterleitung nicht gleichzeitig aktiviert sind. Dies könnte zu einer doppelten Rechnungsstellung und einer Duplizierung der Daten führen. |

>[!MORE_ LIKE_ THIS]
>
>* [Serverseitige Weiterleitung](ssf.md#concept_9563FCADF29748928E770EC5221B2685)

