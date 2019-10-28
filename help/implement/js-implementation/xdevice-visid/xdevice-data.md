---
description: Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten
keywords: Analytics-Implementierung
seo-description: Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten
seo-title: Auswirkungen der geräteübergreifenden Besucheridentifizierung auf die Daten
solution: Analytics
subtopic: Besucher
title: Auswirkungen der geräteübergreifenden Besucheridentifizierung auf die Daten
topic: Entwickler und Implementierung
uuid: 1db4d149-cd50-4b41-a850-988901f25051
translation-type: ht
source-git-commit: 67cc404c4502b1b7be3f089538d8a28d5cf7f659

---


# Auswirkungen der geräteübergreifenden Besucheridentifizierung auf die Daten

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud-Gerätekooperations-Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcdc/).

Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten

Um verstehen zu können, wie sich diese Funktion auf die Datenerfassung auswirkt, müssen Sie die Besucherdatenfelder in einem Besucherprofil kennen:

| Datenfeld | Beschreibung |
|---|---|
| Besucher-ID-Cookie | ID, die beim ersten Besuch von einem Gerät oder Browser aus automatisch generiert und im Cookie `s_vi` gespeichert wird. |
| Besucher-ID-Variable | Optionale [!UICONTROL Besucher-ID], die mithilfe der Variablen `s.visitorID` festgelegt wird. Dieser Wert wird aufgefüllt, nachdem ein Benutzer authentifiziert wurde, und kann mit einer ID übereinstimmen, die Ihr Unternehmen verwendet, um einen Benutzer über mehrere digitale Marketingkanäle verfolgen zu können. |
| Effektive Besucher-ID | Die effektive [!UICONTROL Besucher-ID] ist die eigentliche ID für das Benutzerprofil. Dieser Wert ist im [!UICONTROL Besucher-ID]-Cookie oder in der [!UICONTROL Besucher-ID]-Variablen (wenn angegeben) festgelegt. |

