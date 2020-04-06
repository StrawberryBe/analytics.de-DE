---
description: Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente anhand Ihrer Implementierungen von Adobe Analytics® und Ihrer E-Mail-Software.
title: Vor der Aktivierung dieser Integration
uuid: b911edc6-2265-48ed-9e3c-c79cc20dd9b2
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Vor der Aktivierung dieser Integration {#before-you-activate-this-integration}

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente anhand Ihrer Implementierungen von Adobe Analytics® und Ihrer E-Mail-Software.

So wird sichergestellt, dass vor der Aktivierung die entsprechenden Best Practices oder Voraussetzungen vorhanden sind, was zu einer optimalen und erfolgreichen Integration führt.

## Adobe Analytics {#adobe-analytics}

Überprüfen Sie die folgenden Informationen zu dieser Data Connectors-Integration in Bezug auf Adobe Analytics:

* **Report Suite-spezifisch**: Beachten Sie, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **Verfügbare und konfigurierte Analytics-Variablen**: Für diese Integration sind 5 benutzerspezifische Ereignisse und 2 benutzerspezifische eVars sowie optional 3 zusätzliche Ereignisse und 3 zusätzliche eVars erforderlich. Siehe [Analytics-Integrationsvariablen](/help/import/data-connectors/silverpop-overview/silverpop-variables.md).

* **Beauftragter Vertreter**: Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.
* **Data Warehouse™:** Für diese Integration muss Data Warehouse aktiviert sein, damit Remarketing-Segmente generiert werden können. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe.
* **Empfänger-ID:** Für die Integration muss eine „Besucher-ID“ in einer Analytics-Variablen (eVar) erfasst und gespeichert werden. Die Besucher-ID (häufig als „Empfänger-ID“ bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse aus dem Silverpop-System. Diese „Empfänger-ID“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird in das Silverpop-System übertragen und kann für Remarketing-Zecke genutzt werden. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Externes Tracking**: Zum Gewährleisten einer erfolgreichen Integration sollten Sie die Best Practice zur Aktivierung des externen Trackings für jede gesendete E-Mail-Kampagne befolgen. Weitere Informationen finden Sie unten im Abschnitt „Silverpop“.
* **Datenschutz-Compliance**: Sie sollten sich darüber im Klaren sein, dass durch die Aktivierung des Empfänger- oder Besucher-ID-Trackings diese Funktion persönliche Informationen Ihrer Site-Besucher verfolgen kann. Dies wirkt sich auf den Datenschutz aus, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

## Data Connector-Integration für Silverpop {#silverpop-data-connector-integration}

Überprüfen Sie die folgenden Informationen zu dieser Data Connector-Integration für Silverpop:

* **Gültiges Silverpop-Konto:** Um die Data Connectors-E-Mail-Integration verwenden zu können, muss ein Client über ein aktives Silverpop-Konto mit aktivierter E-Mail und aktiven Benutzeranmeldeinformationen verfügen.
* **Wenden Sie sich an Ihren Silverpop-Kundenbetreuer**. Diese Integration wird von Silverpop nicht automatisch aktiviert. Sie müssen sich an Ihren Silverpop-Kundenbetreuer wenden, um die Silverpop-Einrichtung zu initiieren, bevor Daten aus Analytics importiert oder exportiert werden.

>[!NOTE] Diese Integration funktioniert nur mit Engage-Organisationen (nicht mit Transact).

## Preise {#pricing}

Diese Data Connectors-Integration umfasst Hinweise zu Preisen, die Sie vor der Aktivierung berücksichtigen müssen.

### Hinweise zu Adobe-Preisen {#section-2d1c79c895a5479bad8fdd97961ba6a3}

Diese Integration kann mit wiederkehrenden und Implementierungsgebühren verbunden sein. Details zu den Preisen erhalten Sie von Ihrem Adobe-Kundenbetreuer.

### Hinweise zu Partner-Preisen {#section-c6afad08c34b43e3a7a3637eea3328c3}

Diese Integration kann mit Gebühren verbunden sein. Informationen zu Preisen erhalten Sie von Ihrem Beziehungsmanager.
