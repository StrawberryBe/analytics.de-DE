---
description: Mit Webprotokoll-Datenquellen können Sie standardmäßige Webserver-Protokolldateien importieren.
seo-description: Mit Webprotokoll-Datenquellen können Sie standardmäßige Webserver-Protokolldateien importieren.
seo-title: Webprotokoll
solution: Analytics
subtopic: Datenquellen
title: Webprotokoll
topic: Entwickler und Implementierung
uuid: a 0 efed 77-6 d 1 b -43 d 8-97 ce-dc 31009805 e 0
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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