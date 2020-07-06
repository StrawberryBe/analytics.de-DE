---
title: Städte
description: Die Stadt, von der der Treffer ausging.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Städte

Die Dimension &quot;Städte&quot;gibt die Stadt an, aus der der Treffer stammt. Diese Dimension ist hilfreich, um festzustellen, aus welchen Städten die Besucher beim Besuch Ihrer Site stammen. Sie könnten diese Daten nutzen, um sich auf lokale Werbung in diesen Städten zu konzentrieren, wie etwa Plakatwände oder Werbespots.

## Diese Dimension mit Daten füllen

Diese Dimension bezieht sich auf Nachschlageregeln, die in Adobe enthalten sind. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um Suchvorgänge zwischen IP-Adresse und Stadt zu verwalten. Diese Dimension funktioniert bei allen Implementierungen standardmäßig.

>[!TIP]
>
>Wenn Ihr Unternehmen strengen Datenschutzbestimmungen folgt, bei denen die [Verschleierung der IP-Adresse](/help/admin/admin/general-acct-settings-admin.md) nicht ausreicht, können Sie die vollständige Deaktivierung der Geolocation-Daten anfordern. Wenden Sie sich an den Kundendienst mit der Report Suite-ID und fordern Sie an, die Option &quot;Geografie&quot;für die Report Suite zu deaktivieren.

## Dimensionswerte

Zu den Dimensionswerten zählen Städte auf der ganzen Welt. Zu den Beispielwerten gehören `"New York (New York, United States)"`, `"Bangalore (Karnataka, India)"`oder `"London (London, United Kingdom)"`.

## Unterschiede zwischen gemeldeter und tatsächlicher Position

Da diese Dimension auf der IP-Adresse basiert, können einige Szenarien einen Unterschied zwischen dem gemeldeten Ort und dem tatsächlichen Ort anzeigen:

* **IP-Adressen, die Unternehmensvertreter** repräsentieren: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Ort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Das mobile IP-Targeting funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Fluggesellschaften baut den IP-Verkehr über zentrale oder regionale Standorte auf.
* **Satellitennutzer** des ISP: Die Identifizierung des spezifischen Standorts dieser Benutzer ist schwierig, da sie in der Regel vom Uplink-Speicherort ausgehen.
* **Militärische und staatliche IPs**: Stellt Mitarbeiter dar, die durch den Erdball reisen und über ihren Heimatort einreisen, und nicht über den Standort oder das Büro, an dem sie derzeit stationiert sind.
