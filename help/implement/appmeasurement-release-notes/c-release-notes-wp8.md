---
description: 'null '
seo-description: 'null '
seo-title: Windows Phone 8
solution: Analytics, Marketing Cloud
subtopic: Versionshinweise
title: Windows Phone 8
topic: Entwickler und Implementierung
uuid: 7378969 a-d 219-42 bf -9750-141 acc 9 e 4 b 7 d
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Windows Phone 8{#windows-phone}

>[!NOTE]
>
>Aktivieren Sie die Debug-Protokollierung, um die aktuelle Bibliotheksversion zu finden.

Mobile library [downloads](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) are available on [!DNL Developer Connection].

>[!NOTE]
>
>The [!DNL Windows] Phone 8 SDK is replaced by the [Windows 8.1 Universal App Store](../appmeasurement-release-notes/c-release-notes-winu.md) SDK. An diesem SDK wird keine weitere Entwicklung vorgenommen.

## Version 3.0.4 {#section_51A8A53CDFB24F6F9D882E9C30ECDB49}

Releasedatum: **21. August 2013**

* In Kontextdaten-Schlüsseln können nun Unterstriche verwendet werden.

## Version 3.0.5 {#section_DFE58939E33C447FBBF8B04E612A96B5}

Releasedatum: **22. Mai 2013**

* Fehlerbehebungen und kleinere Verbesserungen.

## Version 3.0.4 {#section_F303B6E5955248CF8BDA6C7CB994BAD5}

Releasedatum: **18. April 2013**

* Problem behoben, bei dem die Länge der vorherigen Sitzung in manchen Fällen fehlerhaft berechnet wurde.

## Version 3.0.3 {#section_0159586C3EC94865A485A8E586862DF6}

Releasedatum: **21. März 2013**

* Lokalisierungsproblem mit `DateTime`-Objekten behoben.

## Version 3.0.2 {#section_296C375729EA4474BDF3FD6ADD4BEAFB}

Releasedatum: **26. Februar 2013**

* `ADMS_Measurement.visitorID` wird jetzt mit dem Standardwert vorausgefüllt.
* Problem behoben, das manchmal automatische Antworten aus dem Cache verursachte.

## Version 3.0.1 {#section_5865E881249441ADBB03A9637548650F}

Releasedatum: **21. Februar 2013**

* Aufgrund der Thread-Optimierung ist die Einstellung `offlineThrottleDelay` veraltet und nicht mehr erforderlich. Die Einstellung ist noch vorhanden, um die Rückwärtskompatibilität zu gewährleisten, hat jedoch keine Auswirkung mehr.
* `DayOfWeek` ist nun 1-basiert mit Start am Sonntag, um mit den auf anderen Plattformen erfassten Werten übereinzustimmen.
* Behebung eines Problems bei der Offline-Speicherung, das manchmal den Absturz der Anwendung verursachte.

