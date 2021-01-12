---
description: Diese Integration kombiniert die Leistungsfähigkeit des in E-Mail-Marketingsoftware integrierten Feedback-Systems und der verhaltensbasierten Berichterstattung von Adobe Analytics, um leistungsstarke Analyse- und Optimierungsmöglichkeiten für Ihre Organisation zu schaffen.
title: optivo® broadmail-Data Connector für Adobe Analytics
uuid: bd713080-9d1a-49ee-aad0-86dd5c37c34a
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 98%

---


# optivo® broadmail-Data Connector für Adobe Analytics {#optivo-broadmail-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Am 1. August 2021 werden wir die Adobe Data Connector-Technologie beenden. [Weitere Informationen ...](/help/import/data-connectors/data-connectors-eol.md)

Diese Integration kombiniert die Leistungsfähigkeit des in E-Mail-Marketingsoftware integrierten Feedback-Systems und der verhaltensbasierten Berichterstattung von Adobe Analytics, um leistungsstarke Analyse- und Optimierungsmöglichkeiten für Ihre Organisation zu schaffen.

[!DNL ~Partner~] ist eine professionelle E-Mail-Marketingsoftware. Ihre Hauptfunktion besteht darin, Newsletter- und E-Mail-Kampagnen zu erstellen, zu versenden und auszuwerten. `[~Partner~]` ist als Cloud Service (Software-as-a-Service) verfügbar.

Die `[~Partner~]`-Integration bietet automatisierte Remarketing- und Datensynchronisation, was zu höheren Konversionen und einem höheren Umsatz führt. Die Integration ermöglicht es Marketingexperten, automatisch Segmente für ihre Kunden zu synchronisieren, basierend auf ihrer E-Mail-Interaktion und ihrem Site-Verhalten. Mit dem automatisierten Datenaustausch der anpassbaren Segmente können Sie hochgradig zielgruppenorientierte und zugleich umsatzsteigernde E-Mail-Kampagnen erstellen, beispielsweise Warenkorbabbrüche und das Remarketing nach dem Kauf, um Produkte per Cross-, Up- und Reselling-Initiativen zu verkaufen.

Bei dieser Integration werden auch Metriken erfolgreicher E-Mail-Kampagnen von `[~Partner~]` zu Adobe Analytics ausgetauscht. Wichtige Daten werden zentral in der Übersicht Ihrer E-Mail-Kampagne angezeigt.

## Data Connectors-Laborprogramm {#section-51f9864851b64d96873127b9ac9c9a2b}

Dieses Programm ist eine schnelle Methode, mit der Adobe-Drittanbieter-Plattformpartner Integrationen erstellen und diese für unseren gemeinsamen Markt bereitstellen können. Die Integrationen werden von unseren Partnern vollständig entwickelt und in der Adobe Experience Cloud unter Berücksichtigung von Community-Methoden bereitgestellt. Sie werden Adobe-Kunden von Adobe Analytics und anderen Lösungen ohne zusätzlichen Aufpreis zur Verfügung gestellt und werden aufgrund der Drittanbieterbeschaffenheit der Integrationen ohne implizite Garantien von Adobe bereitgestellt.

Wenden Sie sich bei Fragen zu Ihrem aktuellen Service, Ihrer Garantie oder Ihrer Lizenzierung an Ihren Adobe-Kundenbetreuer.

## Hauptvorteile und Funktionen {#key-benefits-and-features}

Diese Integration umfasst die folgenden Hauptvorteile:

* Zurückgewinnung von stöbernden und den Kaufvorgang abbrechenden Käufern
* Umsatzsteigerung durch zielgerichtetes Crosssell- und Up-Sell-Remarketing
* Automatische segmentbasierte Kampagnen
* Optimierte Kampagnen in Bearbeitung
* Segmente in [!DNL ~Partner~] für zielgerichtetes Remarketing
* Konstante Aktualisierungen der Kampagnenmetrik
* Automatisierte Konversationsauslöser

## Dynamische Marketingsegmente {#dynamic-marketing-segments}

Diese Integration umfasst die folgenden dynamischen Marketingsegmente:

* **Profile für Kauf**: Erhöhen Sie Nachbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf das Kaufverhalten der Besucher ausgerichtet sind.
* **Profil für das Verhalten der Produkt-/Inhaltsansicht**: Erreichen Sie potenzielle Kunden durch Marketingsegmente, die auf Produktansichten und Inhaltszugriffsprofilen basieren.
* **Profil für Warenkorbabbruch:** Mit auf sie speziell abgestimmten Kampagnen können Sie Besucher, die zögern, ihren Einkaufswagen abzuschließen, in Kunden umwandeln.
* **Effektives Remarketing:** Kunden können auch benutzerspezifische Remarketing-Segmente erstellen und planen, die speziell auf die Bedürfnisse ihrer Benutzer abgestimmt sind.

## Vor der Aktivierung {#before-you-activate}

Bevor Sie die Data Connectors-Integration für starten, sollten Sie die folgenden Anforderungen erfüllen:

## Anforderungen für Adobe Analytics {#section-960e70fd2eae4a1cb88a2e4b53a97313}

* **Report Suite-spezifisch**: Beachten Sie, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **Verfügbare und konfigurierte Adobe Analytics-Variablen:** Für diese Integration sind benutzerspezifische Ereignisse und benutzerspezifische eVars erforderlich.

* **Beauftragter Vertreter**: Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.
* **Nachrichten-ID:** Für die Integration muss eine „Nachrichten-ID“ in einer Adobe Analytics-Variablen (eVar) erfasst und gespeichert werden. Diese IDs sind erforderlich, um die gesendeten Mailings zu identifizieren. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Partner:** Für die Integration muss ein [!UICONTROL ~Partner~] in einer Adobe Analytics-Variablen (eVar) erfasst und gespeichert werden. Diese ID ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des [!UICONTROL ~Partner~]-Systems. Dieser „[!UICONTROL ~Partner~]“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das [!UICONTROL ~Partner~]-System übertragen und kann für Remarketing-Zwecke genutzt werden. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Zeit nach dem Klick:** Als Teil des Einrichtungsprozesses muss diese Integration einer eVar zugewiesen werden, die dem Zeitpunkt einer Aktion nach dem Klicken entspricht. Dies ist erforderlich, um Informationen über eine Empfängeraktion an [!UICONTROL ~Partner~] zu übermitteln, nachdem der Empfänger auf einen Link in einem Mailing geklickt hat.

* **Nach dem Klick auf Produkt:** Als Teil des Einrichtungsprozesses muss diese Integration einer eVar zugewiesen werden, die dem angebotenen Produkt entspricht, das einer Aktion nach dem Klick zugeordnet ist. Dies ist erforderlich, um Informationen über eine Empfängeraktion an [!UICONTROL ~Partner~] zu übermitteln, nachdem der Empfänger auf einen Link in einem Mailing geklickt hat.

* **Aktionstyp nach dem Klick:** Als Teil des Einrichtungsprozesses muss diese Integration einer eVar zugewiesen werden, die dem Typ einer Aktion nach dem Klicken entspricht. Dies ist erforderlich, um Informationen über eine Empfängeraktion an [!UICONTROL ~Partner~] zu übermitteln, nachdem der Empfänger auf einen Link in einem Mailing geklickt hat.

* **Datenschutz-Compliance**: Sie sollten sich darüber im Klaren sein, dass durch die Aktivierung des Empfänger- oder Besucher-ID-Trackings diese Funktion persönliche Informationen Ihrer Site-Besucher verfolgen kann. Dies wirkt sich auf den Datenschutz aus, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

## Preise {#pricing}

 Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen.

Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.

### Hinweise zu Adobe-Preisen {#section-1f4f46c0d969435db57d38c1c310a05a}

Aktuellen Kunden der Adobe Analytics-Lösung entstehen keine zusätzlichen Kosten, wenn sie diese Data Connectors-Integration nutzen. Kunden, die noch nicht auf das neue Adobe Analytics-Produkt umgestiegen sind, sollten sich für weitere Informationen an ihren Adobe-Kundenbetreuer wenden.

### Hinweise zu Partner-Preisen {#section-f8ca71df32224412a5101efb6e356529}

Diese Integration steht [!DNL ~Partner~]-Kunden zur Verfügung. Es gelten jedoch zusätzliche Integrationsgebühren. Kontaktieren Sie sales@optivo.com in Bezug auf Preisdetails. Kontaktieren Sie [!DNL ~Partner~] in Bezug auf Preisdetails.

## Adobe Analytics-Variablen {#adobe-analytics-variables}

Für diese Integration sind Adobe Analytics-Variablen zur Verfolgung von Metriken erforderlich.

Nachdem Sie die Ereignisse und eVars identifiziert haben, die in dieser Integration verwendet werden sollen, müssen sie in der Analytics Admin Console aktiviert werden (Anweisungen hierzu finden Sie unter [Report Suites](https://docs.adobe.com/content/help/de-DE/analytics/admin/manage-report-suites/report-suites-admin.html)).
