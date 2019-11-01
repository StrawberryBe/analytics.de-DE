---
description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
seo-description: Häufig gestellte Fragen zu den Funktionen, der Funktionalität und den Problemen bezüglich der serverseitigen Weiterleitung.
seo-title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
title: Häufig gestellte Fragen zur serverseitigen Weiterleitung
uuid: ecd0bc9b-ebf7-414e-88a2-ebba3fd75c92
translation-type: tm+mt
source-git-commit: ed22e0520bf1c7427ead039fb1d0391f2f1e567f

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
| Q: Was ist, wenn ich Report Suites mit mehreren Suites und Tags habe, die separaten Experience Cloud-Orgs zugeordnet sind? | Sie sollten niemals Daten von einem einzelnen Analytics-Treffer an zwei Report Suites senden, die zu separaten Experience Cloud-Orgs gehören. In diesem Fall wird der Treffer jedoch nur an den Experience Cloud-Org weitergeleitet, der mit dem Identitätsdienst auf der Seite übereinstimmt. |
| Q: Was ist, wenn ich Multi-Suite-Tagging verwende und nur eine meiner Report Suites meinem Experience Cloud-Org zugeordnet ist und die andere nicht? | Der Treffer wird an den entsprechenden Datenerfassungsserver für die Experience Cloud-Organisation in Ihrer zugeordneten Report Suite weitergeleitet. Da jedoch die nicht zugeordnete Report Suite in Audience Manager über keine zugehörige Datenquelle verfügt, werden keine Daten für die nicht zugeordnete Report Suite in Audience Manager aufgezeichnet. |
| Q: Was geschieht, wenn ich eine Report Suite habe, die mehreren Experience Cloud-Organisatoren zugeordnet ist? | Analytics betrachtet diese Report Suite als nicht zugewiesen und lässt nicht zu, dass die serverseitige Weiterleitung für diese Report Suite aktiviert wird. Wenden Sie sich an den Kundendienst, um dieses Zuweisungsproblem zu beheben. |
| F: Ist die Report Suite-basierte, serverseitige Weiterleitungsmethode langsamer als die Tracking-Server-basierte, serverseitige Weiterleitung? | Nein, die Antwortzeit ist dieselbe. |
| Q: Was ist, wenn wir über zwei Experience Cloud-Orgs (oder AAM-Instanzen) verfügen und Daten zwischen beiden Experience Cloud-Orgs gemeinsam nutzen möchten? Kann ich einen einzelnen Analytics-Treffer serverseitig an mehrere Experience Cloud-Orgs weiterleiten? | Nein. Wenn Sie Daten, die unter einem Experience Cloud-Org gesammelt wurden, an ein anderes Experience Cloud-Org weitergeben müssen, empfehlen wir, alle relevanten Zielgruppen über den Zielgruppen-Marketplace von einer Audience Manager-Instanz an eine andere zu senden. |
| F: Führt die serverseitige Weiterleitung zu einer zusätzlichen Rechnungsstellung in Audience Manager oder Analytics? | In Analytics erfolgt keine zusätzliche Rechnungsstellung. In Audience Manager werden weitergeleitete Treffer wie andere Treffer behandelt und abgerechnet.  Daher ist es wichtig, dass DIL und die serverseitige Weiterleitung nicht gleichzeitig aktiviert sind. Dies könnte zu einer doppelten Rechnungsstellung und einer Duplizierung der Daten führen. |

>[!MORELIKETHIS]
>
>* [Serverseitige Weiterleitung](/help/admin/admin/c-server-side-forwarding/ssf.md)

