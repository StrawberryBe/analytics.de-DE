---
description: Zeigt die Links auf der Seite zu Websites außerhalb Ihrer Website an, auf die die Benutzer am häufigsten klicken. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Websites. Es sind jedoch auch andere Websites möglich, auf die Sie einen externen Link gelegt haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.
seo-description: Zeigt die Links auf der Seite zu Websites außerhalb Ihrer Website an, auf die die Benutzer am häufigsten klicken. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Websites. Es sind jedoch auch andere Websites möglich, auf die Sie einen externen Link gelegt haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.
seo-title: 'Ausstiegslinks '
solution: Analytics
title: 'Ausstiegslinks '
topic: Berichte
uuid: e1452f04-389d-4aa3-8763-732880284302
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Ausstiegslinks 

Zeigt die Links auf der Seite zu Websites außerhalb Ihrer Website an, auf die die Benutzer am häufigsten klicken. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Websites. Es sind jedoch auch andere Websites möglich, auf die Sie einen externen Link gelegt haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.

Damit diese Seite ordnungsgemäß mit Daten gefüllt werden kann, müssen bestimmte Anforderungen erfüllt sein:

* Bei manuellen Linktracking von benutzerspezifischen Links muss eine *`s.tl()`*-Anforderung ausgelöst werden, bei der der mittlere Parameter auf *e* eingestellt ist.

* Bei automatischen Linktracking von benutzerspezifischen Links müssen alle Anforderungen erfüllt sein:
* 

   * [s.trackExternalLinks](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_trackexlinks.html) muss auf *True* eingestellt sein.

   * Der Link, auf den der Benutzer geklickt hat, darf nicht mit den Werten in der Variable [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_linkinfilters.html) übereinstimmen.
   * Wenn [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_linkinfilters.html) implementiert ist, muss der externe Link mit mindestens einem der in dieser Variablen festgelegten Werte übereinstimmen.

* Ist eine der obigen Anforderungen nicht erfüllt, wird der Treffer nicht in diesen Bericht aufgenommen.

* 
* Wie bei allen Linktracking-Treffern für benutzerspezifische Links wird die Variable [s.pageName](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_pagename.html) aus der Bildanforderung entfernt, damit keine irrelevanten Seitenansichten gezählt werden.
* Sie können diesen Bericht als Trend- und als Rangansicht anzeigen.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* Sie können [breakdowns](/help/analyze/reports-analytics/reports-customize/breakdowns.md) with any other variable via Admin Tools.
* [Instanzen](../../../components/c-variables/c-metrics/metrics-instance.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF) sind die einzigen Metriken, die standardmäßig für diesen Bericht zur Verfügung stehen, wobei ermittelt wird, wie oft der Exitlink ausgelöst wird.
* Für diesen Bericht können Besucher pro Tag, Woche, Monat und Quartal aktiviert werden. Die Aktivierung ist jedoch nur durch einen Adobe-Support-Mitarbeiter möglich und ist kostenpflichtig. Wenn Unique Visitors für Variablen zu Linktracking benutzerspezifischer Links aktiviert werden, steigt die Latenz der Report Suite erheblich an.

