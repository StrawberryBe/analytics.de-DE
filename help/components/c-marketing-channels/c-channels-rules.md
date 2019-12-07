---
description: Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.
subtopic: Marketing channels
title: Informationen über Kanäle und Regeln
topic: Reports and analytics
uuid: 7d574790-4d0d-419d-8fb5-c16ec5a4a387
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Informationen über Kanäle und Regeln

Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.

Ein Kanal ist im Grunde nichts anderes als ein Behälter für Besuche und die Regeln ordnen die Besuche in den richtigen Behälter ein.

![](assets/buckets_2.png)

Adobe stellt während des [automatischen Setups](/help/components/c-marketing-channels/c-channel-autosetup.md) eine Reihe vordefinierter Kanäle bereit, die Sie an Ihre Anforderungen anpassen können.

>[!NOTE]
>
>Adobe empfiehlt, dass Sie Ihren Bericht in einer Report Suite einrichten, die Sie zu Testzwecken als Vorlage verwenden können. Verwenden Sie die Vorlage, um Kanal- und Regelsätze global auf eine oder mehrere Produktions-Report Suites anzuwenden.
>
>Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](/help/components/c-marketing-channels/t-template.md).

Lesen Sie folgende Themen durch:

* [Voraussetzungen](/help/components/c-marketing-channels/c-channels-rules.md#prereqs)
* [Wichtige Verarbeitungshinweise](/help/components/c-marketing-channels/c-channels-rules.md#important-proc-rules)

## Voraussetzungen {#prereqs}

Gegebenenfalls müssen Sie sich für Support zu den Voraussetzungen an die Kundenunterstützung wenden:

* Aktivieren Sie in den allgemeinen Kontoeinstellungen der Admin Console die Option **[!UICONTROL Konversionsstufe]** (E-Commerce) für die Report Suite.

   Weitere Informationen finden Sie unter [Allgemeine Kontoeinstellungen](https://marketing.adobe.com/resources/help/en_US/reference/general_acct_settings_admin.html) in der Hilfe zu Analytics.

* Richten Sie den Benutzergruppenzugriff auf den **[!UICONTROL Marketingkanalbericht ein]**.

   Weitere Informationen finden Sie unter [Konfigurieren des Benutzergruppenzugriffs](/help/components/c-marketing-channels/t-user-groups.md).

* Stellen Sie sicher, dass Ihr Kundenbetreuer die **[!UICONTROL Kanalberichte]** für Ihre Report Suite aktiviert hat.

## Wichtige Verarbeitungshinweise {#important-proc-rules}

* Das System verarbeitet die Regeln in der angegebenen Reihenfolge. Sobald eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.
* Regeln haben Zugriff auf Variablen, die von VISTA gesetzt wurden, können jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Kanäle speichern nur Konversionsmetriken. Traffic-Metriken stehen nicht zur Verfügung.
* Dasselbe Ereignis kann niemals zwei Marketingkanälen gutgeschrieben werden (wie Käufe oder Klicks). In dieser Hinsicht unterscheiden sich Marketingkanäle von eVars (dasselbe Ereignis kann zwei eVars gutgeschrieben werden).
* Der Bericht kann bis zu 25 Kanäle gleichzeitig verarbeiten.

