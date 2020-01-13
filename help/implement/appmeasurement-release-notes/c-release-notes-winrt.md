---
description: 'null'
solution: Analytics,Experience Cloud
subtopic: Release notes
title: WinRT für Windows 8
topic: Developer and implementation
uuid: cec19d63-114c-4ef6-a55e-db6aad4e948b
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# WinRT für Windows 8{#winrt-for-windows}

>[!NOTE]
>
>Schalten Sie die Debug-Protokollierung ein, um die aktuelle Bibliotheksversion zu suchen.

[Downloads](https://marketing.adobe.com/developer/get-started/mobile/c-measuring-mobile-applications) mobiler Bibliotheken sind über [!DNL Developer Connection] verfügbar.

>[!NOTE]
>
>Das [!DNL WinRT] für [!DNL Windows] 8 SDK wird durch das SDK [Windows 8.1 Universal App Store](../appmeasurement-release-notes/c-release-notes-winu.md) ersetzt. An diesem SDK wird keine weitere Entwicklung vorgenommen.

## Version 4.0 {#section_248BF5A38F1843A5BCF6DBD62A5D3D59}

Releasedatum: **17. Juni 2014**

Neue Version mit neuen Funktionen, einschließlich des geografischen Standorts, Lebenszykluswerts, zeitgesteuerter Aktionen und Anmeldeunterstützung.

## Version 3.1.1 {#section_6E925545B72240BB816DA2333CA93E46}

Releasedatum: **22. Mai 2014**

Fehlerbehebungen und kleinere Verbesserungen.

## Version 3.1.0 {#section_F9059928B6FE43C99322A0DA35EB85C3}

Releasedatum: **17. Oktober 2013**

* [!DNL Windows]Kompatibilität mit 8.1

## Version 3.0.5 {#section_8F163FF1E88142F180091A88C9FD9D12}

Releasedatum: **18. April 2013**

* Problem behoben, bei dem die Länge der vorherigen Sitzung in manchen Fällen fehlerhaft berechnet wurde.

## Version 3.0.4 {#section_FD242F9BA3D1481090E45998883E4CDD}

Releasedatum: **21. März 2013**

* `ADMS_Measurement.visitorID` wird jetzt automatisch auf den Standardwert festgelegt.
* Problem beim Abrufen der Geräteinformationen behoben.

## Version 3.0.3 {#section_5865E881249441ADBB03A9637548650F}

Releasedatum: **21. Februar 2013**

* Aufgrund der Thread-Optimierung ist die Einstellung `offlineThrottleDelay` veraltet und nicht mehr erforderlich. Die Einstellung ist noch vorhanden, um die Rückwärtskompatibilität zu gewährleisten, hat jedoch keine Auswirkung mehr.
* `DayOfWeek` ist nun 1-basiert mit Start am Sonntag, um mit den auf anderen Plattformen erfassten Werten übereinzustimmen.
* Das automatische Abonnieren von Event-Listenern im TrackingHelper.js wurde hinzugefügt, um die Lebenszyklusverfolgung zu rationalisieren.

## Version 3.0.2 {#section_CCFAE5A29FB14DAD9A9F14FE8EE09B75}

Releasedatum: **November 2012**

* Bildschirmauflösung wird nun für C#-, C++- und HTML5-/WinJS-Plattformen ordnungsgemäß erfasst.
* Die Klasse `ADMS_Churn` ist jetzt intern. Um Best Practices für das Lebenszyklus-Tracking der Anwendung zu nutzen, verwenden Sie folgende Aufrufe:

   ```
   public void ADMS_Measurement.StartSession(); 
   public void ADMS_Measurement.StopSession();
   ```

* Variable `public double maxSessionLength` zu `ADMS_Measurement` hinzugefügt, um das Festlegen einer maximalen Sitzungslänge für die vorherige Benutzersitzung zu ermöglichen. Wenn die erkannte Sitzungslänge den Maximalwert überschreitet, wird die maximale Sitzungslänge gesendet. Standardmäßig beträgt `maxSessionLength` 3600 (Sekunden).
* Eine Konfigurationsvariable `lifecycleSessionTimeout` wurde hinzugefügt, durch die Sie angeben können, wie viel Zeit in Sekunden zwischen verschiedenen Startvorgängen einer Anwendung verstreichen muss, damit ein Startvorgang als neue Sitzung gilt.
* Den Lebenszyklusmetriken wurde die Metrik „Frühere Sitzungslänge“ hinzugefügt.
* TrackingHelper für mehr Klarheit aktualisiert.
* Ein Fehler im Medienmodul wurde behoben.

## Version 3.0.1 {#section_EA2E5F8550C348BDB948A9236BD35619}

**Oktober 2012**

Erstes Release.
