---
title: Exitlinks
description: Berichte zu den häufigsten Links, auf die Benutzer klicken, um Ihre Site zu verlassen.
translation-type: tm+mt
source-git-commit: be4c3ec95b9e93dda7603c0bdb178c0a54d800a0

---


# Exitlinks

Zeigt die häufigsten Links an, auf die Personen klicken, um Ihre Site zu verlassen. Diese Links verweisen in der Regel auf Partner- oder Affiliate-Sites. Sie können jedoch an jedem Ort sein, an dem Sie einen externen Link haben. In diesem Bericht können Sie die beliebtesten Affiliate-Links abrufen oder auch die Anzahl der Verweise überprüfen, die nach Angaben Ihrer Partner von Ihrer Website stammen.

Damit diese Seite ordnungsgemäß mit Daten gefüllt werden kann, müssen bestimmte Anforderungen erfüllt sein:
* Bei Verwendung der manuellen Verfolgung benutzerspezifischer Links muss eine `tl()` Anforderung ausgelöst werden, wobei der mittlere Parameter auf `e`.
* Bei automatischen Linktracking von benutzerspezifischen Links müssen alle Anforderungen erfüllt sein:
   * Die [Variable trackExternalLinks](/help/implement/vars/config-vars/trackexternallinks.md) muss aktiviert sein.
   * The link the user clicked on must not match any values within the [linkInternalFilters](/help/implement/vars/config-vars/linkinternalfilters.md) variable.
   * If the [linkExternalFilters](/help/implement/vars/config-vars/linkexternalfilters.md) variable exists, the external link must match at least one of the values set in this variable.
* Wenn eine der oben genannten Anforderungen nicht erfüllt wird, füllt der Treffer diesen Bericht nicht.
* Wie bei allen Treffern zur Verfolgung benutzerspezifischer Links wird die Variable &quot; [pageName](/help/implement/vars/page-vars/pagename.md) &quot;aus der Bildanforderung entfernt, um eine Erhöhung der Ansichten auf der Seite zu verhindern.
* Sie können diesen Bericht als Trend- und als Rangansicht anzeigen.
* In diesem Bericht können bestimmte Zeileneinträge mit einem Suchfilter ermittelt werden.
* Sie können [Aufschlüsselungen](/help/analyze/reports-analytics/reports-customize/breakdowns.md) mit jeder anderen Variablen.
