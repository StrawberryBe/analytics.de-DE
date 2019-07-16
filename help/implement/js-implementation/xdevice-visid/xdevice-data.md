---
description: Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten
keywords: Analytics-Implementierung
seo-description: Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten
seo-title: Auswirkungen auf die geräteübergreifende Besucheridentifizierung
solution: Analytics
subtopic: Besuchern
title: Auswirkungen auf die geräteübergreifende Besucheridentifizierung
topic: Entwickler und Implementierung
uuid: 1 db 4 d 149-cd 50-4 b 41-a 850-988901 f 25051
translation-type: tm+mt
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Auswirkungen auf die geräteübergreifende Besucheridentifizierung

>[!IMPORTANT]
>
>Diese Methode zur Identifizierung von Besuchern auf Gerätegeräten wird nicht mehr empfohlen. Please refer to the [Adobe Experience Cloud Device Co-op Documentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten

Um verstehen zu können, wie sich diese Funktion auf die Datenerfassung auswirkt, müssen Sie die Besucherdatenfelder in einem Besucherprofil kennen:

| Datenfeld | Beschreibung |
|---|---|
| Besucher-ID-Cookie | ID, die beim ersten Besuch von einem Gerät oder Browser aus automatisch generiert und im Cookie `s_vi` gespeichert wird. |
| Besucher-ID-Variable | Optionale [!UICONTROL Besucher-ID], die mithilfe der Variablen `s.visitorID` festgelegt wird. Dieser Wert wird aufgefüllt, nachdem ein Benutzer authentifiziert wurde, und kann mit einer ID übereinstimmen, die Ihr Unternehmen verwendet, um einen Benutzer über mehrere digitale Marketingkanäle verfolgen zu können. |
| Effektive Besucher-ID | Die effektive [!UICONTROL Besucher-ID] ist die eigentliche ID für das Benutzerprofil. Dieser Wert ist im [!UICONTROL Besucher-ID]-Cookie oder in der [!UICONTROL Besucher-ID]-Variablen (wenn angegeben) festgelegt. |

