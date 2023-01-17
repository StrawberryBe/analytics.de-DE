---
title: Browser
description: Name und Version des verwendeten Browsers.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
source-git-commit: 39f1ac66fb6374c62f790f9a38a52fba3bf9bda1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 38%

---

# Browser

Der[!UICONTROL Browser]&quot;Dimension zeigt den Namen und die Version des Browsers an, der den Treffer sendet. Diese Dimension ist nützlich, um die gängigsten Browser zu verstehen, die Besucher verwenden. Beim Testen neuer Versionen Ihrer Site können Sie diese Tests mit den wichtigsten Browsern in dieser Dimension ausführen, um den Aufwand für die Qualitätssicherung zu optimieren.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf eine interne Tabelle von Adobe. Der Wert basiert auf der HTTP-Kopfzeile `User-Agent` in den Bildanforderungen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Tags in Adobe Experience Platform), ist diese Dimension vorkonfiguriert.

## Dimensionselemente

Zu den Dimensionselementen gehören die verwendeten Browsernamen und -versionen. Verschiedene Versionen desselben Browsers sind separate Dimensionselemente.

Einige Dimensionselemente enthalten `"(unknown version)"` anstelle ihrer Versionsnummer. Dieses Dimensionselement verweist auf eine kürzlich veröffentlichte Browserversion, die von der Adobe nicht zu denn Suchtabellen hinzugefügt wurde. Da Browser häufig aktualisiert werden, ist `"(unknown version)"` für einen bestimmten Browser üblich und vorübergehend. Adobe aktualisiert die Suchtabellen in der Regel während der monatlichen Wartungsversionen.

## Änderungen der Kennzeichnung und Definition

Nachstehend finden Sie eine Liste der Änderungen, die an der Darstellung von Browsern in Berichten vorgenommen wurden. Diese Änderungen können sich auf Ihre Berichterstellung oder auf eine Logik, wie Segmente, auswirken, die von diesen Werten abhängt.

### Entfernen des Unternehmens aus dem Browser

Ab Version 100 wird der Unternehmensname für Chrome-, Edge- und Firefox-Browser nicht mehr vor dem Browser angezeigt. Dies kann sich auf Benutzer auswirken, wenn sie Segmentdefinitionen basierend auf dem Namen des Browsers haben. Beispielsweise werden in einem Segment, das eine Definition enthält, wonach &quot;Browser&quot;&quot;Google&quot;enthält, keine Chrome-Browser mehr identifiziert, die mit Version 110 beginnen.

Beispiele:

Version 109 von Chrome wird als &quot;Google Chrome 109&quot;angezeigt.
Version 110 von Chrome wird als &quot;Chrome 109&quot;angezeigt.

### Entfernung der Unterscheidung zwischen mobil und nicht mobil für Chrome

Ab Chrome 110 werden sowohl mobile als auch nicht mobile Versionen von Chrome als identisch gekennzeichnet. Derzeit sind mobile und nicht mobile Versionen separat gekennzeichnet. Wichtig ist, dass dadurch die Bedeutung des Namens ohne &quot;mobile&quot;geändert wird. &quot;Chrome 109&quot;ist nicht mobil (d. h. Desktop) &quot;Chrome 110&quot;ist mobil und nicht mobil. Auch wenn Sie Segmentdefinitionen haben, die im Browsernamen auf &quot;mobile&quot;verweisen, funktionieren diese möglicherweise nicht mehr erwartungsgemäß. Sie können die mobile Segmentierung und Aufschlüsselungen verwenden, um mobilen mit nicht mobilem Traffic zu vergleichen.

Beispiele:

Mobile Chrome 109 wird als &quot;Chrome Mobile 109&quot;angezeigt.
Nicht-Mobilgerät Chrome 109 wird als &quot;Chrome 109&quot;angezeigt.

Mobile Chrome 110 wird als &quot;Chrome 110&quot;angezeigt.
Nicht-Mobilgerät Chrome 110 wird als &quot;Chrome 110&quot;angezeigt.
