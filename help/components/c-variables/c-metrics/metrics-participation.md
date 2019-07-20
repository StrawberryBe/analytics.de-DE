---
description: Die Beitragsmetrik schreibt den Erfolg allen Werten einer eVar gut, die während eines Besuchs übertragen wurden. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte den größten Beitrag zum Erfolg Ihrer Website leisten. Der Beitrag beruht auf den Besuchen. Alle eVar-Werte eines Besuchs bis einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten unabhängig von der Ablaufeinstellung Beitragsgutschriften.
seo-description: Die Beitragsmetrik schreibt den Erfolg allen Werten einer eVar gut, die während eines Besuchs übertragen wurden. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte den größten Beitrag zum Erfolg Ihrer Website leisten. Der Beitrag beruht auf den Besuchen. Alle eVar-Werte eines Besuchs bis einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten unabhängig von der Ablaufeinstellung Beitragsgutschriften.
seo-title: Beitrag
solution: Analytics
title: Beitrag
topic: Metriken
uuid: a 7 fa 791 d -0 a 77-429 e -808 e -4 f 97 bb 9 ae 5 fc
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Beitrag

Die Beitragsmetrik schreibt den Erfolg allen Werten einer eVar gut, die während eines Besuchs übertragen wurden. Beitragsmetriken sind hilfreich, um festzustellen, welche Seiten, Kampagnen oder anderen benutzerspezifischen Variablenwerte den größten Beitrag zum Erfolg Ihrer Website leisten. Der Beitrag beruht auf den Besuchen. Alle eVar-Werte eines Besuchs bis einschließlich des Treffers, wenn ein Ereignis eintritt, erhalten unabhängig von der Ablaufeinstellung Beitragsgutschriften.

See [Visitor Participation - Ad Hoc Analysis](../../../components/c-variables/c-metrics/metrics-visitor-participation.md#concept_ACBAE3626B224D9683257B5F73E0FB4A) for more information about how Ad Hoc Analysis uses participation.

Beitragsmetriken verfügen pro Konversionsereignis über zwei Einstellungen:

* **Deaktiviert**: Der Standardzustand von Konversionsereignissen. Für dieses Ereignis werden keine Beitragsdaten erfasst.
* **Aktiviert**: Für dieses Ereignis werden Beitragsdaten erfasst.

>[!NOTE]
>
>Sie können die Teilnahme für bis zu 100 benutzerspezifische Ereignisse aktivieren. Darüber hinaus können Sie im Generator für [berechnete Metriken](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics/participation_metric.html) Beitragsmetriken erstellen.

Nach der Aktivierung sind Beitragsmetriken automatisch in allen Konversionsberichten verfügbar. Beitragsmetriken können aber auf Anfrage auch in bestimmten Traffic-Berichten angezeigt werden. Sie können optional anfordern, dass Beitragsmetriken in bestimmten benutzerspezifischen Traffic-Berichten zur Verfügung stehen.

## Beispiel zum Umsatzbeitrag {#section_DAB6C348201B454BB4ED01313AA777AF}

Gehen Sie von der folgenden Abfolge aus:

1. Ein Benutzer navigiert zur Ihrer Site und sucht nach dem Begriff „Schuhe“.
1. Daraufhin sucht der Benutzer nach dem Begriff „Tennisschuhe“.
1. Der Benutzer klickt auf einen Link zur Produktseite, legt den Artikel in den Warenkorb und kauft ihn für 120 USD.

Wenn Sie im Bericht „Interne Suchbegriffe“ die Option „Umsatz“ aufrufen, erscheinen je nach ausgewählter Zuordnung folgende Informationen:

* **Erster**: „Schuhe“ werden 120 USD gutgeschrieben. „Tennisschuhe“ wird 0 USD gutgeschrieben.
* **Letzter**: „Tennisschuhe“ werden 120 USD gutgeschrieben. „Schuhe“ wird 0 USD gutgeschrieben.
* **Linear**: Jeder Kampagne werden 60 USD gutgeschrieben.

   Der Beitrag ähnelt der linearen Zuordnung, aber alle Werte erhalten die volle Gutschrift. Wenn Sie als Metrik jedoch „Umsatz (Beitrag)“ verwenden, wird keine Zuordnung berücksichtigt. Als „Umsatz (Beitrag)“ würde in diesem Beispiel 120 USD für beide Suchbegriffe angezeigt.

>[!MORE_ LIKE_ THIS]
>
>* [Metrikberechnungen](/help/components/c-variables/c-metrics/metrics-calculations.md)

