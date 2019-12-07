---
description: Mithilfe der geräteübergreifenden Identifizierung erkennen Sie Ihre Besucher auch auf anderen Geräten wieder. Bei der geräteübergreifenden Besucherkennung werden Benutzer mithilfe der Besucherkennungsvariablen „s.visitorID“ geräteübergreifend zugeordnet.
keywords: Analytics Implementation
subtopic: Visitors
title: Benutzer geräteübergreifend verbinden
topic: Developer and implementation
uuid: 6243957b-5cc1-49ef-aa94-5b5ec4eac313
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Benutzer geräteübergreifend verbinden

> [!IMPORTANT] Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Siehe [Geräteübergreifende Analyse](/help/components/cda/cda-home.md) im Komponenten-Benutzerhandbuch.

Mithilfe der geräteübergreifenden Identifizierung erkennen Sie Ihre Besucher auch auf anderen Geräten wieder. Cross-device visitor identification uses the `visitorID` variable to associate a user across devices. Die `visitorID` Variable hat beim [Identifizieren individueller Besucher](../c-unique-visitors/visid-overview.md)die höchste Priorität.

Wenn Sie einen Treffer mit einer benutzerdefinierten Besucher-ID senden, sucht Adobe nach Besucherprofilen mit einer übereinstimmenden Besucher-ID. Wenn eines vorhanden ist, wird das Besucherprofil, das sich bereits im System befindet, ab diesem Zeitpunkt verwendet und das vorherige Besucherprofil wird nicht mehr verwendet.

Setting the `visitorID` variable is typically set after authentication, or after a visitor performs some other action that allows you to uniquely identify them independently of the device that is used. Zu den wirksamen Identifikatoren gehören ein Hash ihres Benutzernamens, ihrer E-Mail-Adresse oder einer internen ID, die keine persönlichen Informationen enthält.

Nachdem sich der Kunde von jedem Gerät aus angemeldet hat, sind alle an dasselbe Benutzerprofil gebunden. Wenn sich der Besucher später auf einem Gerät abmeldet, gehört er weiterhin zum gleichen Besucherprofil, da Adobe erkennt, dass das Browser-Cookie auf jedem Gerät zum gleichen Besucherprofil gehört. Adobe empfiehlt, die `visitorID` Variable nach Möglichkeit zu verwenden, wenn das Browsercookie gelöscht wird.

## Einschränkungen

Die Verwendung eigener benutzerspezifischer Besucher-IDs gibt Ihnen mehr Kontrolle darüber, wie Besucher identifiziert werden, allerdings mit Einschränkungen.

* **Die Besucherdeduplizierung ist nicht rückwirkend**: Wenn ein Besucher Ihre Site zum ersten Mal aufruft und sich dann authentifiziert, werden zwei individuelle Besucher gezählt. Ein individueller Besucher zählt automatisch für die generische Analytics-ID und ein anderer für die benutzerdefinierte Besucher-ID, wenn er sich anmeldet. Diese Duplizierung individueller Besucher erfolgt immer dann, wenn ein Besucher ein neues Gerät verwendet oder seine Cookies löscht.
* **Inkompatibilität mit dem Experience Cloud ID-Dienst**: Seit der Einführung der geräteübergreifenden Besucheridentifizierung hat Adobe leistungsfähigere und zuverlässigere Methoden zur geräteübergreifenden Verfolgung von Besuchern eingeführt. Diese neuen Identifizierungsmethoden sind nicht mit der Außerkraftsetzung der benutzerdefinierten Besucher-ID kompatibel. Wenn Sie planen, den ID-Dienst, geräteübergreifende Analytics (CDA) oder die Gerätekooperation zu verwenden, empfiehlt Adobe dringend, die `visitorID` Variable nicht zu verwenden.
