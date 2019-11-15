---
description: Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten
keywords: Analytics Implementation
solution: Analytics
subtopic: Visitors
title: Auswirkungen der geräteübergreifenden Besucheridentifizierung auf die Daten
topic: Developer and implementation
uuid: 1db4d149-cd50-4b41-a850-988901f25051
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Auswirkungen der geräteübergreifenden Besucheridentifizierung auf die Daten

>[!IMPORTANT]
>
>Diese Methode zur geräteübergreifenden Identifizierung von Besuchern wird nicht mehr empfohlen. Weitere Informationen finden Sie in der [Adobe Experience Cloud Device Co-op-Dokumentation](https://marketing.adobe.com/resources/help/en_US/mcdc/).

Ein Überblick über die Auswirkungen von geräteübergreifender Besucheridentifizierung auf die in Berichten angezeigten Daten

Um verstehen zu können, wie sich diese Funktion auf die Datenerfassung auswirkt, müssen Sie die Besucherdatenfelder in einem Besucherprofil kennen:

| Datenfeld | Beschreibung |
|---|---|
| Visitor ID Cookie | ID, die beim ersten Besuch von einem Gerät oder Browser aus automatisch generiert und im Cookie `s_vi` gespeichert wird. |
| Besucher-ID-Variable | Optionale [!UICONTROL Besucher-ID], die mithilfe der Variablen `s.visitorID` festgelegt wird. Dieser Wert wird aufgefüllt, nachdem ein Benutzer authentifiziert wurde, und kann mit einer ID übereinstimmen, die Ihr Unternehmen verwendet, um einen Benutzer über mehrere digitale Marketingkanäle verfolgen zu können. |
| Effektive Besucher-ID | Die effektive [!UICONTROL Besucher-ID] ist die eigentliche ID für das Benutzerprofil. Dieser Wert ist im [!UICONTROL Besucher-ID]-Cookie oder in der [!UICONTROL Besucher-ID]-Variablen (wenn angegeben) festgelegt. |

