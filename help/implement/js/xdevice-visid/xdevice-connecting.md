---
description: Mithilfe der geräteübergreifenden Identifizierung erkennen Sie Ihre Besucher auch auf anderen Geräten wieder. Bei der geräteübergreifenden Besucherkennung werden Benutzer mithilfe der Besucherkennungsvariablen „s.visitorID“ geräteübergreifend zugeordnet.
keywords: Analytics Implementation
subtopic: Visitors
title: Benutzer geräteübergreifend verbinden
topic: Developer and implementation
uuid: 6243957b-5cc1-49ef-aa94-5b5ec4eac313
translation-type: ht
source-git-commit: 12c026fec44f2e66e2997e8b338823f2c7d790e4
workflow-type: ht
source-wordcount: '399'
ht-degree: 100%

---


# Benutzer geräteübergreifend verbinden

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie unter [Cross-Device Analytics](/help/components/cda/overview.md) im Benutzerhandbuch zu den Komponenten.

Mithilfe der geräteübergreifenden Identifizierung erkennen Sie Ihre Besucher auch auf anderen Geräten wieder. Bei der geräteübergreifende Besucheridentifizierung werden Benutzer mithilfe der `visitorID`-Variablen geräteübergreifend zugeordnet. Die `visitorID`-Variable hat bei der Identifizierung von Unique Visitors die höchste Priorität.

Wenn Sie einen Treffer mit einer benutzerdefinierten Besucher-ID senden, sucht Adobe nach Besucherprofilen mit einer übereinstimmenden Besucher-ID. Existiert ein solches Profil, wird ab diesem Punkt das bereits im System vorhandene Besucherprofil genutzt und das vorherige Besucherprofil wird nicht mehr eingesetzt.

Die `visitorID`-Variable wird für gewöhnlich festgelegt, nachdem sich ein Besucher authentifiziert hat oder eine andere Aktion durchgeführt hat, an der er – unabhängig davon, welches Gerät er verwendet hat – identifiziert werden kann. Zu den wirksamen Kennungen gehören ein Hash ihres Benutzernamens, ihrer E-Mail-Adresse oder einer internen ID, die keine persönlichen Informationen enthält.

Nachdem sich der Kunde von jedem Gerät aus angemeldet hat, sind alle an dasselbe Benutzerprofil gebunden. Wenn sich der Besucher später auf einem Gerät abmeldet, gehört er weiterhin zum gleichen Besucherprofil, da Adobe erkennt, dass das Browser-Cookie auf jedem Gerät zum gleichen Besucherprofil gehört. Adobe empfiehlt, die `visitorID`-Variable wann immer möglich zu verwenden, falls das Browser-Cookie gelöscht wird.

## Einschränkungen

Die Verwendung eigener benutzerdefinierter Besucher-IDs gibt Ihnen mehr Kontrolle darüber, wie Besucher identifiziert werden, allerdings mit Einschränkungen.

* **Die Besucherdeduplizierung ist nicht rückwirkend**: Wenn ein Besucher Ihre Website zum ersten Mal aufruft und sich dann authentifiziert, werden zwei Unique Visitors gezählt. Ein Unique Visitor wird für die generische Analytics-ID gezählt, die automatisch generiert wird, und ein weiterer für die benutzerdefinierte Besucher-ID, wenn er sich anmeldet. Diese Duplizierung von Unique Visitors erfolgt immer dann, wenn ein Besucher ein neues Gerät verwendet oder seine Cookies löscht.
* **Inkompatibilität mit dem Experience Cloud ID-Dienst**: Seit der Einführung der geräteübergreifenden Besucheridentifizierung hat Adobe leistungsfähigere und zuverlässigere Methoden zum geräteübergreifenden Tracking von Besuchern eingeführt. Diese neuen Identifikationsmethoden sind nicht mit der Überschreibung der benutzerdefinierten Besucher-ID kompatibel. Wenn Sie planen, den ID-Dienst, Cross-Device Analytics oder die Gerätekooperation zu verwenden, empfiehlt Adobe dringend, die `visitorID`-Variable nicht zu verwenden.
