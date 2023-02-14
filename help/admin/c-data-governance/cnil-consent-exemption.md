---
description: Informieren Sie sich über die Richtlinien und Empfehlungen für die Zustimmung der Benutzer zum Speichern oder Lesen von nicht erforderlichen Cookies auf Geräten oder Browsern.
title: Was sind die CNIL-Richtlinien für Cookies und die Zustimmung der Benutzer?
feature: Data Governance
exl-id: 04179e58-dbba-45e2-ba57-7fe5fdedc483
source-git-commit: 9397f12dc95d0dda258beff4dfbb5dd57f01cb40
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# CNIL-Zustimmungsfreistellung

Am 1. Oktober 2020 veröffentlichte die französische Datenschutzbehörde (die &quot;CNIL&quot;) eine überarbeitete Version ihrer Cookie-Richtlinien (die &quot;Leitlinien&quot;) und ihrer endgültigen Empfehlungen zur Einholung der Zustimmung der Benutzer zur Speicherung oder zum Lesen nicht wesentlicher Cookies und ähnlicher Technologien auf Benutzergeräten oder -browsern (&quot;Recommendations&quot;).

Die Leitlinien sehen eine begrenzte Freistellung von der Genehmigungspflicht vor (&quot;Freistellung&quot;). Die Zustimmungsfreistellung gilt für Analytics-Cookies, deren Zweck nur auf die Messung der Zielgruppe der Site oder Mobile App im Auftrag des Web-Herausgebers beschränkt ist. Die Leitlinien sehen vor, dass für die Anwendung der Zustimmungsfreistellung die folgenden Bedingungen erfüllt sein müssen:

* Maximale Datenaufbewahrung über 25 Monate.  Sie können Ihre aktuellen Einstellungen zur Datenaufbewahrung unter [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Data Governance].  [Datenaufbewahrung](https://experienceleague.adobe.com/docs/analytics/technotes/data-retention.html?lang=de)
* Deaktivieren Sie Drittanbieter-Cookies in Experience Cloud Identifier. [disableThirdPartyCalls](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disablethirdpartycalls.html?lang=de#id-service-api), [disableThirdPartyCookies](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disable-cookies.html?lang=de#id-service-api) und [disableIdSyncs](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/configurations/disableidsync.html?lang=de#id-service-api)
* Cookie-Beschränkung auf 13 Monate. Mit der Variablen `cookieLifetime` können Sie den Ablauf Ihres Analytics-Cookies überschreiben. Experience Cloud-Cookies, einschließlich Analytics und ECID, verlängern das Cookie-Ablaufdatum mit jedem Besuch. Um einen statischen, nicht rollierenden Cookie-Ablauf festzulegen, haben Sie folgende Möglichkeiten: (1) Schreiben Sie benutzerdefinierten Code, um ein Datum festzulegen, an dem das Cookie gelöscht werden soll, oder (2) verwenden Sie Ihre CMP, um das Zurücksetzdatum des Cookies zu steuern. [cookieLifetime](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/cookielifetime.html?lang=de) und [Experience Cloud-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html?lang=de#ec-cookies)
* Eingeschränkter Umfang. Der Umfang des Cookies muss auf eine einzelne Site oder Anwendung beschränkt sein. [Browsercookies](https://experienceleague.adobe.com/docs/analytics/technotes/cookies/cookies.html#third-party-cookie-limitations)
* Anonymisierung. Anonymisieren des letzten Oktetts der IP-Adresse. [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
* Besucher-ID aus Berichten ausblenden.  Die Besucher-IDs sind in Adobe Workspace und Adobe Reports &amp; Analytics standardmäßig nicht sichtbar.  Besucher-IDs stehen in Daten-Feeds und Data Warehouse zur Verfügung.  Der Zugriff auf Daten-Feeds und Data Warehouse kann durch [Zugriffsberechtigungen in Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/administration/admin-getting-started.html?lang=de) beschränkt werden  und durch [Referenz zur Daten-Feed-Spalte](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=de#columns%2C-descriptions%2C-and-data-types)
* Geopositionsparameter. Die Geoposition darf nicht präziser sein als Postleitzahlen. [Zip-Option](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/zip.html?lang=de) und [Allgemeine Kontoeinstellungen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/general-acct-settings-admin.html?lang=de#admin-tools)
* Legen Sie die Opt-in-Optionen fest.  Mit dem Opt-in-Dienst können Sie Besucherprotokolle festlegen, um festzustellen, ob Sie beim Besuch Ihrer Site ein Cookie auf dem Gerät oder Browser des Benutzers setzen können. [Opt-in-Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=de)
* Datenfreigabe verhindern.  Um die Datenfreigabe für Adobe Audience Manager auszuschließen, verwenden Sie die Kontextvariable `opt.dmp` für [Privacy Reporting](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md), um zu verhindern, dass Treffer freigegeben werden.
* Zugriffs- und Löschmöglichkeit. Verwenden Sie den Privacy Service für Zugriffs- und Löschanforderungen. [Analytics &amp; Privacy Service](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html?lang=de)

## Zusätzliche Überlegungen zur Datenerfassung

Es gelten zusätzlich folgende Überlegungen:

* Adobe Analytics betreibt Datenverarbeitungszentren in den USA, Großbritannien und Singapur, um allen Kunden Flexibilität bei der Erfassung, Verarbeitung und Speicherung ihrer Daten auf regionaler Ebene zu bieten. Bei der Konfiguration der anfänglichen Einrichtung von Adobe Analytics können Kunden den gewünschten Standort im Datenverarbeitungscenter auswählen. Kundendaten werden letztendlich in ihrer ausgewählten Region für das Analytics-Hauptprodukt gespeichert.
* Ziehen Sie in Erwägung, den Opt-in-Status in einer Analytics-Variablen zu erfassen, um Opt-in-Daten und Opt-out-Daten bei der Segmentierung oder bei Virtual Report Suites zu trennen oder zu separaten Endpunkten weiterzuleiten.
* Keine Messung außerhalb der Site oder App ohne vorherige Zustimmung, z. B. keine Offsite-Kampagnen, E-Mail-Kampagnen oder iFrames.
* Die Erfassung personenbezogener Daten in Variablen ist ohne Zustimmung nicht gestattet. [Experience Cloud-Aktivitäten auf Basis des Benutzereinverständnisses steuern](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/use-opt-in-to-control-experience-cloud-activities-based-on-user-consent.html#implementing-opt-in-on-the-page)
* Daten dürfen nur zur Erstellung anonymer Statistiken verwendet werden, wobei sie nicht mit anderen Daten kombiniert werden dürfen.
* Die Daten werden nicht für Querverweisaktionen verwendet.
* GPS-Geopositionsdaten werden nicht erfasst.
* Wenn die Endbenutzer-Einwilligung erteilt wurde, können die oben genannten Einstellungen geändert und die Einschränkungen gelockert werden.

>[!IMPORTANT]
>
>Dieses Dokument ist nicht als rechtliche oder rechtliche Beratung gedacht und stellt keine Garantie oder vertragliche Verpflichtung seitens der Adobe dar. Wir empfehlen unseren Kunden, unabhängige Rechtsberatung zu den rechtlichen und regulatorischen Verpflichtungen des Kunden in Fragen zu diesem Thema anzufordern.


Weitere Informationen finden Sie auf der Website [CNIL Cookie Exemption](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications).
