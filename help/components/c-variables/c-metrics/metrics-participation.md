---
description: Die Beitragsmetrik schreibt den Erfolg allen Werten einer eVar gut, die während eines Besuchs übertragen wurden. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte den größten Beitrag zum Erfolg Ihrer Website leisten. Der Beitrag beruht auf den Besuchen. Alle eVar-Werte eines Besuchs bis einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten unabhängig von der Ablaufeinstellung Beitragsgutschriften.
title: Beitrag
topic: Metrics
uuid: a7fa791d-0a77-429e-808e-4f97bb9ae5fc
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Beitrag

Die Beitragsmetrik schreibt den Erfolg allen Werten einer eVar gut, die während eines Besuchs übertragen wurden. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte den größten Beitrag zum Erfolg Ihrer Website leisten. Der Beitrag beruht auf den Besuchen. Alle eVar-Werte eines Besuchs bis einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten unabhängig von der Ablaufeinstellung Beitragsgutschriften.

Weitere Informationen dazu, wie die Beteiligung in Ad Hoc Analysis genutzt wird, finden Sie unter [Besucherbeteiligung – Ad Hoc Analysis](/help/components/c-variables/c-metrics/metrics-visitor-participation.md).

Beitragsmetriken verfügen pro Konversionsereignis über zwei Einstellungen:

* **Deaktiviert**: Der Standardzustand von Konversionsereignissen. Für dieses Ereignis werden keine Beitragsdaten erfasst.
* **Aktiviert**: Für dieses Ereignis werden Beitragsdaten erfasst.

>[!NOTE] Sie können die Beteiligung für bis zu 100 benutzerspezifische Ereignisse aktivieren. Darüber hinaus können Sie im Generator für [berechnete Metriken](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/calcmetric-workflow/participation-metric.html) Beitragsmetriken erstellen.

Nach der Aktivierung sind Beitragsmetriken automatisch in allen Konversionsberichten verfügbar. Beitragsmetriken können aber auf Anfrage auch in bestimmten Traffic-Berichten angezeigt werden. Sie können optional anfordern, dass Beitragsmetriken in bestimmten benutzerspezifischen Traffic-Berichten zur Verfügung stehen.

## Beispiel zum Umsatzbeitrag  {#section_DAB6C348201B454BB4ED01313AA777AF}

Gehen Sie von der folgenden Abfolge aus:

1. Ein Benutzer navigiert zur Ihrer Site und sucht nach dem Begriff „Schuhe“.
1. Daraufhin sucht der Benutzer nach dem Begriff „Tennisschuhe“.
1. Der Benutzer klickt auf einen Link zur Produktseite, legt den Artikel in den Warenkorb und kauft ihn für 120 USD.

Wenn Sie im Bericht „Interne Suchbegriffe“ die Option „Umsatz“ aufrufen, erscheinen je nach ausgewählter Zuordnung folgende Informationen:

* **Erster**: „Schuhe“ werden 120 USD gutgeschrieben. „Tennisschuhe“ wird 0 USD gutgeschrieben.
* **Letzter**: „Tennisschuhe“ werden 120 USD gutgeschrieben. „Schuhe“ wird 0 USD gutgeschrieben.
* **Linear**: Jeder Kampagne werden 60 USD gutgeschrieben.

   Der Beitrag ähnelt der linearen Zuordnung, aber alle Werte erhalten die volle Gutschrift. Wenn Sie als Metrik jedoch „Umsatz (Beitrag)“ verwenden, wird keine Zuordnung berücksichtigt. Als „Umsatz (Beitrag)“ würde in diesem Beispiel 120 USD für beide Suchbegriffe angezeigt.

>[!MORELIKETHIS]
>
>* [Metrikberechnungen](/help/components/c-variables/c-metrics/metrics-calculations.md)

