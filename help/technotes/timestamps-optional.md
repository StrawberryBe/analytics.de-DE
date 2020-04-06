---
description: In diesem Abschnitt erfahren Sie mehr zu den Vorteilen und Einschränkungen der Einstellung „Zeitstempel optional“.
keywords: Analytics Implementation
title: Verwendung von „Zeitstempel optional“
topic: Developer and implementation
uuid: 956aaa16-6ffa-4b63-b022-a659f5143e00
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Verwendung von „Zeitstempel optional“

In diesem Abschnitt erfahren Sie mehr zu den Vorteilen und Einschränkungen der Einstellung „Zeitstempel optional“.

&quot;Zeitstempel optional&quot;ist die Standardeinstellung für alle neuen Report Suites.

* Mischen Sie Daten mit und ohne Zeitstempel in derselben globalen Report Suite.
* Senden von Daten mit Zeitstempel von einer mobilen App an eine globale Report Suite
* Aktualisieren Sie Apps, um Zeitstempel zu verwenden, ohne eine neue Report Suite erstellen zu müssen.

>[!NOTE] Die Einstellung der optionalen Zeitstempel ist standardmäßig für alle neuen, aus einer Vorlage generierten Report Suites festgelegt. Neue Report Suites, die aus einer vorhandenen kopiert werden, übernehmen die Einstellungen der ursprünglichen Report Suite.

Weitere Informationen zur Einrichtung finden Sie unter [Zeitstempel optional](https://marketing.adobe.com/resources/help/de_DE/reference/timestamp-optional.html) .

## Zeitstempel optional: Integration von Daten mit und ohne Zeitstempel {#section_BF17CB593044462B993FD0D28EA56518}

Mit der Funktion &quot;Zeitstempel optional&quot;können Sie Daten ohne Zeitstempel mit Daten mit Zeitstempel kombinieren, ohne dass dabei Datenverluste auftreten. Offline-Daten mit Zeitstempeln, die von einem Mobilgerät generiert werden, können mit Live-Daten ohne Zeitstempel von einer Webseite kombiniert werden - oder mit Daten von einer beliebigen Plattform über einen clientseitigen Zeitstempelaufruf integriert werden.

* **Zeitstempeldaten**. Client-seitige Daten mit Zeitstempel werden erfasst und direkt mit den Gerätedaten über Client-seitige Zeitstempelvariablen übertragen: mittels Javascript von einer Webseite oder mittels eines Mobile SDK-Aufrufs ([!DNL offlineEnabled=true]) aus einer App.
* **Daten** ohne Zeitstempel. Adobe legt einen Zeitstempel für Daten ohne Zeitstempel in einer Report Suite fest, wenn die Daten auf die Erfassungsserver gelangen.


Eine Report Suite kann über eine der folgenden Zeitstempeleinstellungen verfügen:

* Keine Zeitstempel zulässig (Festlegen von visitorID unterstützt)
* Zeitstempel erforderlich (Festlegen von visitorID nicht unterstützt)
* Zeitstempel optional (Festlegen von visitorID unterstützt, aber nicht bei Treffern mit Zeitstempel)

## Informationen zu den Funktionen von „Zeitstempel optional“ {#section_63B2FA9A2AB24B3993E84D2C2B4BF2CE}

Mit &quot;Zeitstempel optional&quot;können Sie mehrere Report Suites mit oder ohne clientseitige Zeitstempel integrieren und Berichte darüber erstellen. Mit &quot;Zeitstempel optional&quot;können Sie Ihre App so aktualisieren, dass Zeitstempel verwendet werden, während Sie weiterhin Daten ohne Zeitstempel aus der vorherigen App verwenden.

| In früheren Versionen ... | Zusätzlich... |
|--- |--- |
| Daten mit Zeitstempel konnten nicht an eine globale Report Suite ohne Zeitstempel gesendet werden. Trefferdaten von Offline-Geräten wurden daher bei dem Versuch, sie einer Report Suite ohne Zeitstempel hinzuzufügen, verworfen. <br/><br/>Trefferdaten aus Offline-Daten wurden daher bei dem Versuch, sie einer Report Suite ohne Zeitstempel hinzuzufügen, verworfen. | Wenn Sie eine App so aktualisieren möchten, dass sie Zeitstempel erfasst und verwendet, müssen Sie eine neue Report Suite einrichten. <br/>Nach der Aktualisierung zur Verwendung von Zeitstempeln war ein Speichern in die alte Report Suite oder die Integration vorhandener Daten nicht mehr möglich. |

Mit **Zeitstempel optional** können Sie nicht zeitgestempelte Daten einer Live-Webseite mit Offline-Daten von mobilen Geräten integrieren oder Ihre App ohne Zeitstempel zu einer App aktualisieren, die Zeitstempel verwendet.

## Kombinieren von Daten zu einer globalen Report Suite {#section_5BE3BDF56007402BB1F5C3144D5FE1E0}

Sie können Daten auf verschiedene Weise zu einer globalen Report Suite kombinieren: über Multi-Suite-Tagging, Vista-Regeln und importierte Batchdateien aus Offline-Quellen.

>[!IMPORTANT] Nehmen Sie sich Zeit für die Planung des Designs jedes Komponenten-Datasets. Die Kombination in einer globalen Report Suite sollte schließlich sinnvoll sein.

## Best Practices in Verbindung mit Zeitstempeln {#section_9436394E5D7E4F8A8B369B6D11BB2B2B}

Im Folgenden finden Sie bewährte Verfahren sowie einige Anforderungen und Einschränkungen, die bei der Integration von Daten mit Zeitstempel mit Daten ohne Zeitstempel beachtet werden müssen.

* In der Regel müssen Zeitstempel für einen bestimmten Besucher oder Besuch in der richtigen chronologischen Reihenfolge bei Adobe eingehen.

   Zu den nicht in der Reihenfolge befindlichen Daten können Daten aus der Offline-Datenerfassung und verspätete Zugriffe oder nicht synchronisierte Uhren auf mobilen Offline-Geräten gehören. Daten außerhalb der Reihenfolge können Zeitberechnungen (wie Besuchszeitwerte), Zuordnungen (eVar-Persistenz), Besuchszahlen und Pfadsetzungsberichte negativ beeinflussen.

* Die Verwendung von Zeitstempeln beim Festlegen einer [s.visitorID](https://marketing.adobe.com/resources/help/de_DE/sc/implement/visid_custom.html) wird nicht empfohlen. Dies kann zu nicht sortierten Daten führen.

* Hybrid-Apps, die aus einer App (mit Zeitstempel, Offlinedaten) bestehen und einen Webbrowser öffnen (ohne Zeitstempel, Live-Daten), sollten keine Zeitstempel verwenden. Das Ergebnis ist ein ungenauer Berichte der Sitzung.

   Darüber hinaus sollten Hybridanwendungen keine Besucher-ID festlegen.
