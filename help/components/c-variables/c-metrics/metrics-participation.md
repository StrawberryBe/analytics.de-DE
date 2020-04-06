---
description: Beitragsmetriken weisen allen Ereignissen einer eVar, die während eines Besuchs weitergegeben wurden, die volle Gutschrift zu. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte am meisten zum Erfolg Ihrer Site beitragen. Der Beitrag basiert auf Besuchen. Alle eVar-Werte in einem Besuch vor und einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten ungeachtet der Ablaufeinstellung eine Beitragsgutschrift.
title: Beitrag
topic: Metrics
uuid: a7fa791d-0a77-429e-808e-4f97bb9ae5fc
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Beitrag

Beitragsmetriken weisen allen Ereignissen einer eVar, die während eines Besuchs weitergegeben wurden, die volle Gutschrift zu. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte am meisten zum Erfolg Ihrer Site beitragen. Der Beitrag basiert auf Besuchen. Alle eVar-Werte in einem Besuch vor und einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten ungeachtet der Ablaufeinstellung eine Beitragsgutschrift.

Weitere Informationen dazu, wie die Beteiligung in Ad Hoc Analysis genutzt wird, finden Sie unter [Besucherbeteiligung – Ad Hoc Analysis](/help/components/c-variables/c-metrics/metrics-visitor-participation.md).

Beitragsmetriken haben zwei Einstellungen pro Konversions-Ereignis:

* **Deaktiviert**: Der Standardstatus jedes Konversions-Ereignisses. Beitragsdaten werden für dieses Ereignis nicht erfasst.
* **Aktiviert**: Beitragsdaten werden für dieses Ereignis erfasst.

>[!NOTE] Sie können die Beteiligung für bis zu 100 benutzerspezifische Ereignisse aktivieren. Darüber hinaus können Sie im Generator für [berechnete Metriken](https://marketing.adobe.com/resources/help/de_DE/analytics/calcmetrics/participation_metric.html) Beitragsmetriken erstellen.

Nach der Aktivierung sind Beitragsmetriken automatisch in allen Konversionsberichten verfügbar. Beitragsmetriken können jedoch auf Anforderung auch in bestimmten Traffic-Berichten angezeigt werden. Sie können optional anfordern, dass Beitragsmetriken in bestimmten benutzerspezifischen Traffic-Berichten zur Verfügung stehen.

## Beispiel zum Umsatzbeitrag  {#section_DAB6C348201B454BB4ED01313AA777AF}

Nehmen Sie die folgende Sequenz an:

1. Ein Benutzer navigiert zu Ihrer Site und sucht nach &quot;Schuhen&quot;.
1. Der Benutzer sucht dann nach &quot;Tennisschuhen&quot;.
1. Der Benutzer klickt auf einen Link zur Produktseite, fügt den Artikel zum Warenkorb hinzu und tätigt einen Kauf im Wert von 120 USD.

Bei der Anzeige des Umsatzes im Bericht &quot;Interne Suchbegriffe&quot;würden Sie je nach ausgewählter Zuordnung Folgendes sehen:

* **Erstens**: &quot;Schuhe&quot;würden 120 USD gutgeschrieben. &quot;Tennisschuhe&quot;erhalten 0 USD.
* **Letzter**: &quot;Tennisschuhe&quot;würden 120 Dollar gutgeschrieben. &quot;Schuhe&quot;erhalten 0 USD.
* **Linear**: Jede Kampagne erhält eine Gutschrift von 60 USD.

   Der Beitrag ähnelt der linearen Zuordnung, allerdings wird allen Werten der volle Anteil gutgeschrieben. Wenn Sie als Metrik &quot;Umsatz (Beitrag)&quot;verwenden, wird die Zuordnung nicht berücksichtigt. Umsatz (Beitrag) in diesem Beispiel würde 120 USD für beide Suchbegriffe melden.

>[!MORELIKETHIS]
>
>* [Metrikberechnungen](/help/components/c-variables/c-metrics/metrics-calculations.md)

