---
title: Regionen
description: Die geografische Region des Besuchers.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 7%

---


# Regionen

Die Dimension &quot;Regionen&quot;berichtet über die geografische Region des Besuchers. Es ist ein geografisches Gebiet, das kleiner ist als ein Land, aber größer als eine Stadt. In einigen Ländern ist unter einer Region ein Bundesstaat, eine Provinz oder eine Präfektur zu verstehen. In anderen Bereichen handelt es sich um ein eigenständiges Land, ein Distrikt oder eine Metropolregion. Die Verwendung dieser Dimension ist wertvoll, wenn Sie mehr Einblicke wünschen als [Länder](countries.md) , aber nicht so granular wie [Städte](cities.md).

## Diese Dimension mit Daten füllen

Diese Dimension bezieht sich auf Nachschlageregeln, die in Adobe enthalten sind. Der Suchwert basiert auf der mit dem Treffer gesendeten IP-Adresse. Adobe arbeitet mit [Digital Element](https://www.digitalelement.com/) zusammen, um die Suche zwischen IP-Adresse und Land aufrechtzuerhalten. Diese Dimension funktioniert bei allen Implementierungen standardmäßig.

>[!TIP]
>
>Wenn Ihr Unternehmen strengen Datenschutzbestimmungen folgt, bei denen die [Verschleierung der IP-Adresse](/help/admin/admin/general-acct-settings-admin.md) nicht ausreicht, können Sie die vollständige Deaktivierung der Geolocation-Daten anfordern. Wenden Sie sich an den Kundendienst mit der Report Suite-ID und fordern Sie an, die Option &quot;Geografie&quot;für die Report Suite zu deaktivieren.

## Dimensionswerte

Zu den Dimensionswerten gehören Regionen und das Land, in dem sich die Region befindet. Zu den Beispielwerten gehören `"California (United States)"`, `"Tokyo (Japan)"`oder `"Sao Paulo (Brazil)"`.

## Unterschiede zwischen gemeldeter und tatsächlicher Position

Da diese Dimension auf der IP-Adresse basiert, können einige Szenarien einen Unterschied zwischen dem gemeldeten Ort und dem tatsächlichen Ort anzeigen:

* **IP-Adressen, die Unternehmensvertreter** repräsentieren: Diese Besucher können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt. Dies kann ein anderer Ort sein, wenn der Benutzer remote arbeitet.
* **Mobile IP-Adressen**: Das mobile IP-Targeting funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Fluggesellschaften baut den IP-Verkehr über zentrale oder regionale Standorte auf.
* **Satellitennutzer** des ISP: Die Identifizierung des spezifischen Standorts dieser Benutzer ist schwierig, da sie in der Regel vom Uplink-Speicherort ausgehen.
* **Militärische und staatliche IPs**: Stellt Mitarbeiter dar, die durch den Erdball reisen und über ihren Heimatort einreisen, und nicht über den Standort oder das Büro, an dem sie derzeit stationiert sind.
