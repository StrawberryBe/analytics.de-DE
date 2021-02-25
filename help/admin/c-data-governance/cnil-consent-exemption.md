---
description: Informieren Sie sich über die Richtlinien und Empfehlungen für die Zustimmung der Benutzer zum Speichern oder Lesen von nicht erforderlichen Cookies auf Geräten oder Browsern.
title: Was sind die CNIL Richtlinien für die Zustimmung der Benutzer und Cookies?
translation-type: tm+mt
source-git-commit: c5ebc92622e012699d64c27701b24a88429e9f4f
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# CNIL - Freistellung

Am 1. Oktober 2020 veröffentlichte die französische Datenschutzbehörde (im Folgenden &quot;CNIL&quot;) eine überarbeitete Fassung ihrer Cookie-Leitlinien (im Folgenden &quot;Leitlinien&quot;) und ihrer abschließenden Empfehlungen zur Einholung der Zustimmung der Nutzer, nicht wesentliche Cookies und ähnliche Technologien auf Geräten oder Browsern der Nutzer zu speichern oder zu lesen (im Folgenden &quot;Recommendations&quot;).

Die Leitlinien sehen eine begrenzte Freistellung von der Genehmigungspflicht vor (&quot;Freistellung von der Zustimmung&quot;). Die Freistellung von der Zustimmung gilt für Analytics-Cookies, deren Zweck auf die Messung der Audience der Site oder App nur im Auftrag des Web-Herausgebers beschränkt ist. Die Leitlinien sehen vor, dass für die Anwendung der Freistellung von der Zustimmung folgende Bedingungen gelten:

* Maximale Datenbindung über 25 Monate.  Sie können Ihre aktuellen Einstellungen zur Datenspeicherung unter Analytics > Admin > Datenverwaltung überprüfen.  [Datenaufbewahrung](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html)
* Cookie-Grenze von 13 Monaten.  Mit der Variablen `cookieLifetime` können Sie den Ablauf Ihres Analytics-Cookies überschreiben.  [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html)
* Eingeschränkter Umfang. Der Umfang des Cookies muss auf eine einzelne Site oder Anwendung beschränkt sein. [Browser-Cookies](https://experienceleague.adobe.com/docs/analytics/technotes/cookies.html?lang=en&quot;\l&quot;third-party-cookie-implementation)
* Anonymisierung. Anonymisieren des letzten Oktetts der IP-Adresse. [Allgemeine Kontoeinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html)
* Besucher-ID aus Berichte ausblenden.  Die Besucher-IDs sind in Adobe Workspace und Adobe Reports and Analytics standardmäßig nicht sichtbar.  Besucher-IDs stehen in Data Feeds und Data Warehouse zur Verfügung.  Der Zugriff auf Data Feeds und die Data Warehouse kann durch [Zugriffsberechtigungen in Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=en&quot;\l&quot;Aufgabe_040673FE3E3E429B9531FBCB8B6A4391) eingeschränkt werden
* Geolocation-Parameter. Geolocation kann nicht präziser sein als Postleitzahlen. [PLZ-](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=en&quot;\l&quot;zip-in-adobe-experience-platform-launch) Optionen und  [allgemeine Kontoeinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=en&quot;\l&quot;admin-tools)
* Legen Sie die Optionen für die Teilnahme fest.  Mit dem Einstiegsdienst können Sie Besucher-Protokolle festlegen, um festzustellen, ob Sie beim Besuch Ihrer Site ein Cookie auf dem Gerät oder Browser des Benutzers einrichten können. [Teilnahme-Dienst](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html)
* Datenfreigabe verhindern  Um die Datenfreigabe für Adobe Audience Manager auszuschließen, verwenden Sie die Kontextvariable `opt.dmp` für [Privacy Berichte](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/consent-variables.html?lang=en&quot;\l&quot;variables), um zu verhindern, dass Treffer freigegeben werden.
* Zugriff und Löschmöglichkeit. Verwenden Sie den Privacy Service zum Zugreifen und Löschen von Anforderungen. [Analytics und Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html)

## Zusätzliche Überlegungen zur Datenerfassung

Es gelten folgende zusätzliche Überlegungen:

* Keine Messung außerhalb der Site oder App ohne vorherige Zustimmung, z. B. keine Offsite-Kampagnen, E-Mail-Kampagnen oder iFrames.
* Die Erfassung personenbezogener Daten in Variablen ist ohne Zustimmung nicht gestattet.
* Daten dürfen nur zur Erstellung anonymer Statistiken verwendet werden, ohne dass dies mit anderen Daten kombiniert wird.
* Daten werden nicht für Querverweisaktionen verwendet.
* GPS-Geolocation-Daten werden nicht erfasst.

Weitere Informationen finden Sie auf der Website [CNIL Cookie Exemption](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications).
