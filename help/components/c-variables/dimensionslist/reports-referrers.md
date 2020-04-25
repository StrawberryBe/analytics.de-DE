---
title: Verweisende Stellen
description: Zeigt die URL des vorherigen Treffers an, wenn dieser Treffer außerhalb Ihrer Site erfolgte.
translation-type: tm+mt
source-git-commit: f18fbd091333523cd9351bfa461a11f0c3f17bef

---


# Verweisende Stellen

Die Dimension &quot;Werber&quot;zeigt die URL an, von der Ihre Besucher kamen, bevor sie zu Ihrer Site gelangten. For example, if a visitor clicks a link from `example.com/example-page.html` and arrives on your site, `example.com/example-page.html` is the referrer if it is not defined as part of your domain.

Für diese Dimension müssen Sie die [internen URL-Filter](/help/admin/admin/internal-url-filter-admin.md)Ihrer Report Suite konfigurieren. Wenn Sie keine internen URL-Filter konfigurieren, betrachtet Adobe Analytics alle Domänen als intern für Ihre Site.

## Dimensionseigenschaften

* Diese Dimension verwendet standardmäßig die neueste Zuordnung.
* Diese Dimension läuft standardmäßig nach dem Besuch ab.
* Diese Dimension unterliegt der eindeutigen Beschränkung von 500 k, bevor Dimensionswerte unter (geringer Traffic) gruppiert werden. Data Warehouse hat keine eindeutige Beschränkung.
* Wenn für eine Metrik kein Werber vorhanden ist, wird dieser unter gruppiert `Typed/Bookmarked`.
* Diese Dimension wird in der Regel beim ersten Treffer des Besuchs festgelegt, kann aber während des Besuchs festgelegt werden.

## Fehlerbehebung

**Q: Warum sehe ich`googleusercontent.com`einen Dimensionswert?**

A: [Google](https://about.google/) verwendet die Domäne `googleusercontent.com` für ihre gehosteten Inhalte. Gehostete Inhalte umfassen:

* **Zwischengespeicherte Seiten**: Die Spider von Google durchsuchen ständig das Web und speichern Webseiten, falls sie offline oder anderweitig nicht verfügbar gemacht werden. Diese zwischengespeicherten Seiten stehen neben allen Suchergebnissen zur Verfügung, indem Sie auf den Link &quot;Zwischengespeichert&quot;einer der Google Suchergebnisseiten klicken. Wenn ein Benutzer auf diesen Link klickt und sich dann den Originalinhalt auf Ihrer Site ansieht, wird er als seine verweisende Domäne aufgeführt `googleusercontent.com` . Diese Seiten haben die Subdomäne `webcache.googleusercontent.com`.
* **Übersetzte Seiten**: Google Angebots ist ein robuster und bequemer Übersetzungsdienst. Wenn Sie eine Site mit diesem Dienst anzeigen, stammt sie von `googleusercontent.com`der Website. Die Dimension &quot;Werber&quot;zeigt URLs aus dieser Domäne an, wenn der Benutzer auf einen Link klickt, um zum Originalinhalt zurückzukehren. Diese Seiten haben die Subdomäne `translate.googleusercontent.com`.
