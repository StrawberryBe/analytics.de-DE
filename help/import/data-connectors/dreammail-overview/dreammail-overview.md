---
description: Diese Adobe® Data Connectors™-E-Mail-Integration kombiniert Verhaltensdaten aus Analytics® mit E-Mail-Marketing zum Schaffen eines leistungsfähigen Tools, um die Erfolgsmessung neu zu definieren und Zielgruppen mit relevanterem Messaging anzusprechen.
title: DreamMail-Data Connector für Adobe Analytics
uuid: f6c01bf8-4e6a-4163-9d41-f24fb5f06bdc
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 98%

---


# DreamMail-Data Connector für Adobe Analytics {#dreammail-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Am 1. August 2021 werden wir die Adobe Data Connector-Technologie beenden. [Weitere Informationen ...](/help/import/data-connectors/data-connectors-eol.md)

Diese Adobe® Data Connectors™-E-Mail-Integration kombiniert Verhaltensdaten aus Analytics® mit E-Mail-Marketing zum Schaffen eines leistungsfähigen Tools, um die Erfolgsmessung neu zu definieren und Zielgruppen mit relevanterem Messaging anzusprechen.

Die Bereitstellung relevanter E-Mail-Nachrichten für diese Marktsegmente kann zu völlig neuen Umsatzmöglichkeiten führen, wodurch die Konvertierung und der Umsatz neuer und vorhandener E-Mail-Kampagnen gesteigert werden. So hat zum Beispiel die Bereitstellung relevanter E-Mail-Nachrichten auf Grundlage von Produkten, die während eines Besuchs angesehen wurden, oder von Produkten, die in einem Warenkorb zurückgelassen wurden, nachweislich erhebliche Auswirkungen auf den Umsatz bei minimalen Auswirkungen auf die Kosten, weil dadurch lediglich die Daten Ihrer Websitebenutzer genutzt werden.

Diese Steigerung der Marketingeffizienz ist einer der wichtigsten Vorteile der Integration von [!DNL Analytics] in [!DNL ~Partner~]. Darüber hinaus synchronisiert diese Integration E-Mail-Metriken automatisch mit [!DNL Analytics]-Daten stündlich für Closed-Loop-Berichte.

## Hauptvorteile und Funktionen {#key-benefits-and-features}

Diese Integration umfasst die folgenden Hauptvorteile:

* Zusammenfassen von E-Mail-Marketing- und Analysedaten auf einer Berichtsoberfläche.
* Optimieren von E-Mail-Kampagnen nach Konversion und Beitrag zum Umsatz und zum Site-Erfolg.
* Auf dynamischen Marketingsegmenten basierendes Remarketing für wichtige Besucher und Marktsegmente.

## Dynamische Marketingsegmente {#dynamic-marketing-segments}

Diese Integration umfasst die folgenden dynamischen Marketingsegmente:

* **Profile für Kauf**: Erhöhen Sie Nachbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf das Kaufverhalten der Besucher ausgerichtet sind.
* **Profil für das Verhalten der Produkt-/Inhaltsansicht**: Erreichen Sie potenzielle Kunden durch Marketingsegmente, die auf Produktansichten und Inhaltszugriffsprofilen basieren.
* **Profil für Warenkorbabbruch:** Mit auf sie speziell abgestimmten Kampagnen können Sie Besucher, die zögern, ihren Einkaufswagen abzuschließen, in Kunden umwandeln.
* Kunden können auch benutzerspezifische Remarketing-Segmente erstellen und planen, die speziell auf die Bedürfnisse ihrer Benutzer abgestimmt sind.

## Vor der Aktivierung {#before-you-activate}

Bevor Sie die Data Connectors-Integration für starten, sollten Sie die folgenden Anforderungen erfüllen:

## Anforderungen für Adobe Analytics {#section-960e70fd2eae4a1cb88a2e4b53a97313}

* **Report Suite-spezifisch**: Beachten Sie, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **Verfügbare und konfigurierte Analytics-Variablen**: Für diese Integration sind benutzerspezifische Ereignisse und benutzerspezifische eVars sowie optional zusätzliche Ereignisse und zusätzliche eVars erforderlich.

* **Beauftragter Vertreter**: Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.
* **Data Warehouse™:** Für diese Integration muss Data Warehouse aktiviert sein, damit Remarketing-Segmente generiert werden können. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe.
* **[!DNL ~Partner~]:** Die Integration erfordert, dass wir eine E-Mail-Adresse in einer Analytics-Variablen (eVar) erfassen und speichern. Der „[!DNL ~Partner~]“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das [!DNL ~Partner~]-System übertragen und kann für Remarketing-Zwecke genutzt werden. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Externes Tracking**: Zum Gewährleisten einer erfolgreichen Integration sollten Sie die Best Practice zur Aktivierung des externen Trackings für jede gesendete E-Mail-Kampagne befolgen. Weitere Informationen finden Sie unten im Abschnitt [!DNL ~Partner~].
* **Datenschutz-Compliance**: Sie sollten sich darüber im Klaren sein, dass durch die Aktivierung des Empfänger- oder Besucher-ID-Trackings diese Funktion persönliche Informationen Ihrer Site-Besucher verfolgen kann. Dies wirkt sich auf den Datenschutz aus, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

## Preise {#pricing}

 Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen.

Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.

### Hinweise zu Adobe-Preisen {#section-1f4f46c0d969435db57d38c1c310a05a}

Diese Integration kann mit wiederkehrenden und Implementierungsgebühren verbunden sein, einschließlich der Kosten für eine erhöhte Anzahl von Serveraufrufen, die durch diese Integration entstehen. Details zu den Preisen erhalten Sie von Ihrem Adobe-Kundenbetreuer.

### Hinweise zu ~Partner~-Preisen {#section-f8ca71df32224412a5101efb6e356529}

Diese Integration kann mit wiederkehrenden und Implementierungsgebühren verbunden sein. Kontaktieren Sie [!DNL DreamMail] in Bezug auf Preisdetails.

## Analytics-Integrationsvariablen {#analytics-integration-variables}

Für diese Integration sind Analytics-Variablen zur Verfolgung von Metriken erforderlich.

Nachdem Sie die Ereignisse und eVars identifiziert haben, die in dieser Integration verwendet werden sollen, müssen sie in der Analytics Admin Console aktiviert werden (Anweisungen hierzu finden Sie unter [Report Suites](https://docs.adobe.com/content/help/de-DE/analytics/admin/manage-report-suites/report-suites-admin.html)).
