---
description: 'null'
subtopic: Release notes
title: PHP
topic: Developer and implementation
uuid: 65a644ef-8e50-406b-8b12-0582495d130a
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# PHP{#php}

> [!NOTE] Schalten Sie die Debug-Protokollierung ein, um die aktuelle Bibliotheksversion zu suchen.

## Version 1.2.2 {#section_0D547871DC684417B6CE1370E5C6AAC2}

Releasedatum: **August 2014**

* Es wurden interne Veränderungen zur Unterstützung neuer Funktionen vorgenommen.

## Version 1.2.1 {#section_5717907F67AB482F860F1DFBCB4198C7}

Releasedatum: **Juli 2012**

* Das „Aus“, das für $_SERVER['HTTPS'] in IIS zurückgegeben wurde, wird nun überprüft. Ohne diese Prüfung wurde durch die Typisierung der Verknüpfungsversion ((bool)$_SERVER['HTTPS']) in IE „true“ zurückgegeben, unabhängig davon, ob die Anforderung über HTTP oder HTTPS erfolgte. Dadurch konnten nichtsichere Seiten versuchen, eine sichere Bildanforderung durchzuführen.

## Version 1.1 {#section_8F4479681ED642FCB9233459E04FF702}

Measurement Library für PHP 1.1 beinhaltet die folgenden Updates aus Version 1.0:

* Bessere GeoSegmentation-Präzision (wenn `sendFromServer` aktiviert ist).
* Fehler behoben, damit der Benutzer nun an die Variable `userAgent` angehängt werden kann.
* Bild-Beacon ist jetzt mit mehr mobilen Browsern kompatibel.
* Die Variable `imageDimensions` wird jetzt standardmäßig auf 5 x 5 festgelegt, wenn die Mobiloption aktiviert ist.
* Bot-Erkennungsliste optimiert.
* Debug-Informationen (HTTP-Header, Antwort, Fehler usw.) hinzugefügt (wenn `debugTracking` und `sendFromServer` aktiviert sind).

* Variable `debugFilename` hinzugefügt (wenn `sendFromServer` aktiviert ist).

* Die Variable „pagename“ wird standardmäßig auf `$_SERVER['SCRIPT_NAME']` festgelegt, wenn weder `pagename` noch `pageURL` festgelegt ist.

* Vollständige Unterstützung für CGI-Implementierungen von PHP.
* Leistungsoptimierung.

