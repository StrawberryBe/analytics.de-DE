---
description: Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen zur Verfolgung verschiedener Silverpop-Metriken.
title: Analytics-Integrationsvariablen
uuid: 3aef3caf-e24e-4fe7-b4d7-50ca0f6703b5
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Analytics Integration Variables{#analytics-integration-variables}

Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen zur Verfolgung verschiedener Silverpop-Metriken.

Nachdem Sie die Ereignisse und eVars identifiziert haben, die mit der Silverpop-Integration verwendet werden sollen, verwenden Sie die Adobe Analytics Admin-Konsole, um sie zu aktivieren (siehe [Report Suites](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)).

In der folgenden Tabelle werden die für die Silverpop-Integration erforderlichen Analytics-Variablen beschrieben.

## Erforderliche Variablen {#section-3ca8dc46bab0436cba0c9ef827c8356a}

| Variablentyp | Name | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| event (numerisch) | Absprünge | Automatisch aus Silverpop importiert. | Mit dem Bounces-Ereignis können Sie die Anzahl der E-Mail-Nachrichten anzeigen, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| event (numerisch) | Klicks | Automatisch aus Silverpop importiert. | Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| event (numerisch) | Öffnen | Automatisch aus Silverpop importiert. | Das Ereignis "Geöffnet"zeigt die Anzahl der Besucher an, die die E-Mail geöffnet haben. |
| event (numerisch) | Senden | Automatisch aus Silverpop importiert. | Mit dem Sends-Ereignis können Sie die Anzahl der gesendeten E-Mail-Nachrichten anzeigen. |
| event (numerisch) | Abonnements aufheben | Automatisch aus Silverpop importiert. | Mit dem Abmeldung-Ereignis können Sie sehen, wie viele Besucher die E-Mail-Nachricht geöffnet haben, aber dann auf den Link Abmelden geklickt haben, um zukünftige E-Mail-Nachrichten Ihres Unternehmens abzuwählen. |
| eVar | Silverpop-ID/Besucher-ID | Wird über die automatisierte Erfassungsmethode oder ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. | Unique Visitor-ID |
| eVar oder s.campaign | Mailing-ID | Wird über die automatisierte Erfassungsmethode oder ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. | Dies wird häufig in der Kampagnenvariablen gespeichert. |

## Optionale Variablen {#section-5f0a32b0a2084c87a64b5f90c0d0fb53}

| Variablentyp | Name | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| event (Zähler) | Datei heruntergeladen | Manuell über Analytics-Tags erfasst. | Dieses Ereignis wird zur Identifizierung von Benutzern verwendet, die eine Datei auf die Site heruntergeladen haben. |
| event (Zähler) | Formulare gestartet | Manuell über Analytics-Tags erfasst. | Mit "Formularstart"werden Benutzer identifiziert, die ein Formular beginnen, es aber nicht ausfüllen. |
| event (Zähler) | Ausgefülltes Formular | Manuell über Analytics-Tags erfasst. | Das ausgefüllte Formular dient zur Identifizierung von Besuchern, die ein Formular beginnen und es nicht ausfüllen. |
| eVar | Email Address | Manuell über Analytics-Tags erfasst. | Die E-Mail-Adresse dient zum manuellen Erfassen der E-Mail-Adresse bei der Anmeldung, Anmeldung oder anderen Seiten, auf denen die E-Mail-Adresse erfasst wird. Diese Variable dient zum Remarketing an Benutzer, die sich für den Empfang von E-Mails entschieden haben, jedoch in der Vergangenheit noch nicht über eine E-Mail geklickt haben. |
| eVar | heruntergeladene Datei | Manuell über Analytics-Tags erfasst. | Die heruntergeladene Datei gibt an, welche Datei ein Besucher heruntergeladen hat. |
| eVar | Name des Formulars | Manuell über Analytics-Tags erfasst. | Der Formularname gibt an, welches Formular ein Besucher verlassen hat. |

