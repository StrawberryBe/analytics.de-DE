---
title: Länder
description: Das Land, aus dem der Treffer stammt.
translation-type: tm+mt
source-git-commit: 52e00470df0f0c6bff84b26c1548e64ff5114fb8
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---


# Länder

Die Dimension &quot;Länder&quot;zeigt das Land an, aus dem der Treffer stammt. Diese Dimension ist nützlich, um festzustellen, aus welchen Ländern die beliebtesten Besucher bei Besuch Ihrer Site stammen. Mithilfe dieser Daten können Sie sich auf Marketingbemühungen in diesen Ländern konzentrieren oder sicherstellen, dass Ihr Site-Erlebnis in Ländern mit unterschiedlichen Hauptsprachen optimal ist.

## Diese Dimension mit Daten füllen

Diese Dimension bezieht sich auf Nachschlageregeln, die in Adobe enthalten sind. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Suche zwischen IP-Adresse und Land aufrechtzuerhalten. Diese Dimension funktioniert bei allen Implementierungen standardmäßig.

> [!TIP] Wenn Ihr Unternehmen strengen Datenschutzbestimmungen folgt, bei denen die [Verschleierung der IP-Adresse](/help/admin/admin/general-acct-settings-admin.md) nicht ausreicht, können Sie die vollständige Deaktivierung der Geolocation-Daten anfordern. Wenden Sie sich an den Kundendienst mit der Report Suite-ID und fordern Sie an, die Option &quot;Geografie&quot;für die Report Suite zu deaktivieren.

## Dimensionswerte

Zu den Dimensionswerten gehören Länder auf der ganzen Welt. Zu den Beispielwerten gehören `"United States"`, `"United Kingdom"`oder `"India"`.

## Unterschiede zwischen gemeldeter und tatsächlicher Position

Da diese Dimension auf der IP-Adresse basiert, können einige Szenarien einen Unterschied zwischen dem gemeldeten Ort und dem tatsächlichen Ort anzeigen:

* **IP-Adressen, die Unternehmensvertreter** repräsentieren: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Ort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Das mobile IP-Targeting funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Fluggesellschaften baut den IP-Verkehr über zentrale oder regionale Standorte auf.
* **Satellitennutzer** des ISP: Die Identifizierung des spezifischen Standorts dieser Benutzer ist schwierig, da sie in der Regel vom Uplink-Speicherort ausgehen.
* **Militärische und staatliche IPs**: Stellt Mitarbeiter dar, die durch den Erdball reisen und über ihren Heimatort einreisen, und nicht über den Standort oder das Büro, an dem sie derzeit stationiert sind.
