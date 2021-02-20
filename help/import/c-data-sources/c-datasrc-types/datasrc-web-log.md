---
description: Mit Webprotokoll-Datenquellen können Sie standardmäßige Webserver-Protokolldateien importieren.
subtopic: Data sources
title: Webprotokoll
topic: Developer and implementation
uuid: a0efed57-6d1b-43d8-97ce-dc31009805e0
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 100%

---


# Webprotokoll

Mit Webprotokoll-Datenquellen können Sie standardmäßige Webserver-Protokolldateien importieren.

Die folgenden allgemeinen Webserverprotokolltypen werden unterstützt:

| Spaltenname | Beschreibung |
|--- |--- |
| NCSA Allgemeines Protokoll | Apache-Standard |
| NCSA Erweitert (Kombo) | Apache |
| W3C erweitertes Protokoll | Verwendet von IIS 4.0 und später |
| Microsoft IIS Protokoll | Verwendet von IIS 3.0 und früher |

Zu den primären Protokolldateifeldern, die Data Sources verarbeitet, gehören IP-Adresse, Datum/Uhrzeit der Anforderung und die URL. In einigen Fällen, z. B. Format „NCSA Erweitert“, verarbeitet Data Sources auch die Felder „Verweisende Stelle“ und „Benutzeragent“.

Sie können Webprotokolldaten mit standardmäßigen Marketingberichten für Seitenansichten, Besuche und Besucher anzeigen. Da Berichtsmetriken vornehmlich auf Cookies basieren und Webserver-Protokolle auf der IP-Adresse basieren, empfiehlt Adobe den Import von Webserverprotokollen in eine speziell für diesen Zweck angelegte Report Suite.

Weitere Informationen zu Webserverprotokolldateien finden Sie in Ihrer Webserver-Dokumentation.
