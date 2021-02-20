---
description: Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen zur Verfolgung verschiedener Silverpop-Metriken.
title: Analytics-Integrationsvariablen
uuid: 3aef3caf-e24e-4fe7-b4d7-50ca0f6703b5
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 100%

---


# Analytics-Integrationsvariablen {#analytics-integration-variables}

Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen zur Verfolgung verschiedener Silverpop-Metriken.

Nachdem Sie die Ereignisse und eVars identifiziert haben, die mit der Silverpop-Integration verwendet werden sollen, verwenden Sie die Adobe Analytics Admin Console, um sie zu aktivieren (siehe [Report Suites](https://docs.adobe.com/content/help/de-DE/analytics/admin/manage-report-suites/report-suites-admin.html)).

In der folgenden Tabelle sind die für die Silverpop-Integration benötigten Analytics-Variablen aufgeführt.

## Erforderliche Variablen {#section-3ca8dc46bab0436cba0c9ef827c8356a}

| Variablentyp | Name | Erfassungsmethode | Beschreibung |
|---|---|---|---|
| event (numerisch) | Absprünge | Automatisch aus Silverpop importiert. | Das Ereignis „Absprünge“ zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. |
| event (numerisch) | Klicks | Automatisch aus Silverpop importiert. | Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. |
| event (numerisch) | Öffnungen | Automatisch aus Silverpop importiert. | Das Ereignis „Geöffnet“ zeigt die Anzahl der Besucher an, welche die E-Mail geöffnet haben. |
| event (numerisch) | Sendungen | Automatisch aus Silverpop importiert. | Das Ereignis „Sendungen“ zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. |
| event (numerisch) | Abonnementkündigungen | Automatisch aus Silverpop importiert. | Mit dem Ereignis „Abo storniert“ können Sie die Anzahl der Besucher anzeigen, welche die E-Mail-Nachricht geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. |
| eVar | Silverpop-ID/Besucher-ID | Wird über die automatisierte Erfassungsmethode oder über ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. | Eindeutige Besucher-ID |
| eVar oder s.campaign | Versand-ID | Wird über die automatisierte Erfassungsmethode oder über ein JavaScript-Plug-In aus Abfrageparametern in E-Mail-Links erfasst. | Dies wird häufig in der Kampagnenvariablen gespeichert. |

## Optionale Variablen {#section-5f0a32b0a2084c87a64b5f90c0d0fb53}

| Variablentyp | Name | Erfassungsmethode | Beschreibung |
|---|---|---|---|
| event (Zähler) | Datei heruntergeladen | Manuelle Erfassung über Analytics-Tags. | Dieses Ereignis wird zur Identifizierung von Benutzern verwendet, die eine Datei auf der Site heruntergeladen haben. |
| event (Zähler) | Formulare gestartet | Manuelle Erfassung über Analytics-Tags. | Mit „Formulare gestartet“ werden Benutzer identifiziert, die ein Formular beginnen, es aber nicht ausfüllen. |
| event (Zähler) | Ausgefülltes Formular | Manuelle Erfassung über Analytics-Tags. | Mit „Ausgefülltes Formular“ werden Besucheridentifiziert, die ein Formular beginnen, es aber nicht ausfüllen. |
| eVar | E-Mail-Adresse | Manuelle Erfassung über Analytics-Tags. | „E-Mail-Adresse“ dient zum manuellen Erfassen der E-Mail-Adresse bei der Registrierung, Anmeldung oder anderen Seiten, auf denen die E-Mail-Adresse erfasst wird. Diese Variable wird zum Remarketing an Benutzer verwendet, die sich für den E-Mail-Empfang entschieden haben, aber möglicherweise noch keine E-Mail durchgeklickt haben. |
| eVar | Heruntergeladene Datei | Manuelle Erfassung über Analytics-Tags. | „Heruntergeladene Datei“ gibt an, welche Datei ein Besucher heruntergeladen hat. |
| eVar | Name des Formulars | Manuelle Erfassung über Analytics-Tags. | „Name des Formulars“ gibt an, welches Formular ein Besucher verlassen hat. |

