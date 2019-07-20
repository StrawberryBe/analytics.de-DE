---
description: Zeigt die Links auf der Seite zu Websites außerhalb Ihrer Website an, auf die die Benutzer am häufigsten klicken. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Websites. Es sind jedoch auch andere Websites möglich, auf die Sie einen externen Link gelegt haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.
seo-description: Zeigt die Links auf der Seite zu Websites außerhalb Ihrer Website an, auf die die Benutzer am häufigsten klicken. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Websites. Es sind jedoch auch andere Websites möglich, auf die Sie einen externen Link gelegt haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.
seo-title: Exitlinks
solution: Analytics
title: Exitlinks
topic: 'Berichte    '
uuid: e 1452 f 04-389 d -4 aa 3-8763-732880284302
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Exitlinks

Zeigt die Links auf der Seite zu Websites außerhalb Ihrer Website an, auf die die Benutzer am häufigsten klicken. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Websites. Es sind jedoch auch andere Websites möglich, auf die Sie einen externen Link gelegt haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.

Damit diese Seite ordnungsgemäß mit Daten gefüllt werden kann, müssen bestimmte Anforderungen erfüllt sein:

* Bei manuellen Linktracking von benutzerspezifischen Links muss eine *`s.tl()`*-Anforderung ausgelöst werden, bei der der mittlere Parameter auf *e* eingestellt ist.

* Bei automatischen Linktracking von benutzerspezifischen Links müssen alle Anforderungen erfüllt sein:
* 

   * [s.trackExternalLinks](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_trackexlinks) muss auf *True* eingestellt sein.

   * Der Link, auf den der Benutzer geklickt hat, darf nicht mit den Werten in der Variable [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_linkinfilters) übereinstimmen.
   * Wenn [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_linkinfilters) implementiert ist, muss der externe Link mit mindestens einem der in dieser Variablen festgelegten Werte übereinstimmen.

* Ist eine der obigen Anforderungen nicht erfüllt, wird der Treffer nicht in diesen Bericht aufgenommen.

* 
* Wie bei allen Linktracking-Treffern für benutzerspezifische Links wird die Variable [s.pageName](https://marketing.adobe.com/resources/help/en_US/sc/implement/index.html?f=c_pagename) aus der Bildanforderung entfernt, damit keine irrelevanten Seitenansichten gezählt werden.
* Sie können diesen Bericht als Trend- und als Rangansicht anzeigen.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* Sie können [Aufschlüsselungen](/help/analyze/reports-analytics/reports-customize/breakdowns.md) mit beliebigen anderen Variablen über Admin Tools.
* [Instanzen](../../../components/c-variables/c-metrics/metrics-instance.md#concept_E3D0FEC81E1F4987B39CC467F19FFCFF) sind die einzigen Metriken, die standardmäßig für diesen Bericht zur Verfügung stehen, wobei ermittelt wird, wie oft der Exitlink ausgelöst wird.
* Für diesen Bericht können Besucher pro Tag, Woche, Monat und Quartal aktiviert werden. Die Aktivierung ist jedoch nur durch einen Adobe-Support-Mitarbeiter möglich und ist kostenpflichtig. Wenn Unique Visitors für Variablen zu Linktracking benutzerspezifischer Links aktiviert werden, steigt die Latenz der Report Suite erheblich an.

