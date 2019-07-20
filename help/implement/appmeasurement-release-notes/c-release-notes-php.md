---
description: 'null '
seo-description: 'null '
seo-title: PHP
solution: Analytics
subtopic: Versionshinweise
title: PHP
topic: Entwickler und Implementierung
uuid: 65 a 644 ef -8 e 50-406 b -8 b 12-0582495 d 130 a
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# PHP{#php}

>[!NOTE]
>
>Aktivieren Sie die Debug-Protokollierung, um die aktuelle Bibliotheksversion zu finden.

## Version 1.2.2 {#section_0D547871DC684417B6CE1370E5C6AAC2}

Releasedatum: **August 2014**

* Es wurden interne Veränderungen zur Unterstützung neuer Funktionen vorgenommen.

## Version 1.2.1 {#section_5717907F67AB482F860F1DFBCB4198C7}

Releasedatum: **Juli 2012**

* Added a check for the "off" returned for the $_SERVER['HTTPS'] in IIS. Without this check, typecasting to boolean ((bool)$_SERVER['HTTPS']) returned true in IE whether the request was made through HTTP or HTTPS. Dadurch konnten nichtsichere Seiten versuchen, eine sichere Bildanforderung durchzuführen.

## Version 1.1 {#section_8F4479681ED642FCB9233459E04FF702}

Measurement Library für PHP 1.1 beinhaltet die folgenden Updates aus Version 1.0:

* Bessere GeoSegmentation-Präzision (wenn `sendFromServer` aktiviert ist).
* Fehler behoben, damit der Benutzer nun an die Variable `userAgent` angehängt werden kann.
* Bild-Beacon ist jetzt mit mehr mobilen Browsern kompatibel.
* Die Variable `imageDimensions` wird jetzt standardmäßig auf 5 x 5 festgelegt, wenn die Mobiloption aktiviert ist.
* Bot-Erkennungsliste optimiert.
* Debug-Informationen (HTTP-Header, Antwort, Fehler usw.) hinzugefügt (wenn `debugTracking` und `sendFromServer` aktiviert sind).

* `debugFilename` Die Variable (sofern `sendFromServer` aktiviert) wurde hinzugefügt.

* The pagename variable defaults to `$_SERVER['SCRIPT_NAME']` when neither `pagename` nor `pageURL` are set.

* Vollständige Unterstützung für CGI-Implementierungen von PHP.
* Leistungsoptimierung.

