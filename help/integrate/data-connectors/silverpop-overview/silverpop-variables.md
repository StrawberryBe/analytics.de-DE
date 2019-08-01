---
description: Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen, um verschiedene Silverpop-Metriken zu verfolgen.
seo-description: Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen, um verschiedene Silverpop-Metriken zu verfolgen.
seo-title: Analytics-Integrationsvariablen
title: Analytics-Integrationsvariablen
uuid: 3 aef 3 caf-e 24 e -4 fe 7-b 4 d 7-50 ca 0 f 6703 b 5
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Analytics Integration Variables{#analytics-integration-variables}

Die Data Connectors-Integration für Silverpop verwendet Analytics-Variablen, um verschiedene Silverpop-Metriken zu verfolgen.

After identifying the Event and eVars to use with the Silverpop integration, use the Adobe Analytics Admin Console to enable them (see [Report Suites](http://microsite.omniture.com/t2/help/en_US/reference/index.html?f=report_suites_admin)).

Die folgende Tabelle beschreibt die Analytics-Variablen, die für die Silverpop-Integration benötigt werden.

## Required Variables {#section-3ca8dc46bab0436cba0c9ef827c8356a}

| Variablentyp | Name | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| Ereignis (numerisch) | Absprünge | Automatisch importiert von Silverpop. | Mit dem Absprünge-Ereignis können Sie die Anzahl der E-Email-Nachrichten anzeigen, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. |
| Ereignis (numerisch) | Klicks | Automatisch importiert von Silverpop. | Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. |
| Ereignis (numerisch) | Öffnet | Automatisch importiert von Silverpop. | Mit dem Ereignis "Geöffnet" können Sie erkennen, wie viele Besucher die E-Email geöffnet haben. |
| Ereignis (numerisch) | Sendet | Automatisch importiert von Silverpop. | Mit dem Ereignis "Sends" können Sie die Anzahl der gesendeten E-Email-Nachrichten anzeigen. |
| Ereignis (numerisch) | Abonnements | Automatisch importiert von Silverpop. | Mit dem nicht abonnierten Ereignis können Sie die Anzahl der Besucher anzeigen, die die E-Email-Nachricht geöffnet haben, dann aber auf den Link Abonnieren klicken, um zukünftige E-Email-Nachrichten aus Ihrer Organisation abzuwählen. |
| eVar | Silverpop ID/Besucher-ID | Wird aus Abfrageparametern in E-Email-Links über die automatisierte Erfassungsmethode oder ein javascript-Plug-in erfasst. | Eindeutige Besucher-ID |
| Evar oder s. campaign | Versand von Ids | Wird aus Abfrageparametern in E-Email-Links über die automatisierte Erfassungsmethode oder ein javascript-Plug-in erfasst. | Dies wird oft in der Kampagnenvariablen gespeichert. |

## Optionale Variablen {#section-5f0a32b0a2084c87a64b5f90c0d0fb53}

| Variablentyp | Name | Methode zum Ausfüllen | Beschreibung |
|---|---|---|---|
| event (Zähler) | Datei heruntergeladen | Manuell über Analytics-Tags erfasst. | Dieses Ereignis wird verwendet, um Benutzer zu identifizieren, die eine Datei auf der Site heruntergeladen haben. |
| event (Zähler) | Formular gestartet | Manuell über Analytics-Tags erfasst. | Das Formular wird verwendet, um Benutzer zu identifizieren, die ein Formular beginnen, es aber nicht abschließen. |
| event (Zähler) | Formular abgeschlossen | Manuell über Analytics-Tags erfasst. | Das ausgefüllte Formular wird verwendet, um Besucher zu identifizieren, die ein Formular beginnen und es nicht abschließen. |
| eVar | Email Address | Manuell über Analytics-Tags erfasst. | E-Mail-Adresse dient zum manuellen Erfassen der E-Email-Adresse bei Anmeldung, Anmeldung oder anderen Seiten, auf denen die E-Email-Adresse erfasst wird. Diese Variable wird verwendet, um den Benutzern, die sich für den Erhalt von E-Mails entschieden haben, zu reproduzieren, aber möglicherweise nicht bereits durch eine E-Mail in der Vergangenheit geklickt. |
| eVar | Heruntergeladene Datei | Manuell über Analytics-Tags erfasst. | Die heruntergeladene Datei identifiziert, welche Datei einen Besucher heruntergeladen hat. |
| eVar | Formularname | Manuell über Analytics-Tags erfasst. | Der Formularname identifiziert, welche Form ein Besucher abgebrochen hat. |

