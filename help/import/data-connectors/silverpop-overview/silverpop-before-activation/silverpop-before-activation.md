---
description: Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Punkte in Bezug auf Ihre Implementierungen von Adobe Analytics® und Ihrer E-Mail-Software.
title: Vor Aktivierung dieser Integration
uuid: b911edc6-2265-48ed-9e3c-c79cc20dd9b2
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Vor Aktivierung dieser Integration{#before-you-activate-this-integration}

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Punkte in Bezug auf Ihre Implementierungen von Adobe Analytics® und Ihrer E-Mail-Software.

Auf diese Weise wird sichergestellt, dass vor der Aktivierung geeignete Best Practices oder Voraussetzungen vorhanden sind, was zu einer optimalen und erfolgreichen Integration führt.

## Adobe Analytics{#adobe-analytics}

Überprüfen Sie die folgenden Informationen zur Data Connectors-Integration in Bezug auf Adobe Analytics:

* **** Report Suite-spezifisch: Beachten Sie, dass diese Integration spezifisch für Report Suites ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **** Verfügbare und konfigurierte Analytics-Variablen: Für diese Integration sind 5 benutzerspezifische Ereignisse und 2 benutzerspezifische eVars sowie optional 3 zusätzliche Ereignisse und 3 zusätzliche eVars erforderlich. Siehe [Analytics-Integrationsvariablen](/help/import/data-connectors/silverpop-overview/silverpop-variables.md).

* **** Bevollmächtigter: Achten Sie darauf, dass Ihre Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe erhebt. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein Bevollmächtigter Ihres Unternehmens sind. und somit ist Ihr Unternehmen bereit, die in der oben beschriebenen Servicevereinbarung genannten Gebühren zu zahlen, sofern vorhanden.
* **** Data Warehouse™:Für diese Integration muss Data Warehouse aktiviert sein, damit Remarketing-Segmente generiert werden können. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe.
* **** Empfänger-ID:Die Integration erfordert, dass wir eine "Besucher-ID"in einer Analytics-Variablen (eVar) erfassen und speichern. Die Besucher-ID (häufig als "Empfänger-ID"bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des Silverpop-Systems. Diese "Empfänger-ID"ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft. die in das Silverpop-System gezogen und für Remarketing-Zwecke genutzt werden können. Während des Setupprozesses müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **** Externe Verfolgung: Wenn Sie derzeit nicht die Best Practice zur Aktivierung der externen Verfolgung für jede gesendete E-Mail-Kampagne befolgen, müssen Sie dies tun, um eine erfolgreiche Integration sicherzustellen. Weitere Informationen finden Sie im Abschnitt Silverpop.
* **** Datenschutz: Sie sollten sich bewusst sein, dass diese Funktion durch Aktivierung der Empfänger- oder Besucher-ID-Verfolgung persönlich identifizierbare Informationen über Ihre Site-Besucher verfolgen kann. Dies hat Auswirkungen auf die Privatsphäre, die die Implementierung geeigneter Verfahren durch Ihr Unternehmen erfordern, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

## Silverpop Data Connector-Integration{#silverpop-data-connector-integration}

Überprüfen Sie die folgenden Informationen zu dieser Data Connector-Integration in Bezug auf Silverpop:

* **** Gültiges Silverpop-Konto: Um die Data Connectors-E-Mail-Integration verwenden zu können, muss ein Client über ein aktives Silverpop-Konto mit aktivierter E-Mail und aktiven Benutzeranmeldeinformationen verfügen.
* **Wenden Sie sich an Ihren Silverpop-Kundenbetreuer**. Diese Integration wird von Silverpop nicht automatisch aktiviert. Sie müssen sich an Ihren Silverpop-Kundenbetreuer wenden, um die Silverpop-Einrichtung zu starten, bevor Daten aus Analytics importiert oder exportiert werden.

> [!NOTE] Diese Integration funktioniert nur mit Engage-Organisationen (nicht mit Transact).

## Preise{#pricing}

Diese Data Connectors-Integration enthält Preisaspekte, die Sie vor der Aktivierung berücksichtigen müssen.

### Hinweise zu Adobe-Preisen {#section-2d1c79c895a5479bad8fdd97961ba6a3}

Diese Integration kann mit wiederkehrenden und Implementierungsgebühren verbunden sein. Informationen zu den Preisen erhalten Sie von Ihrem Adobe-Kundenbetreuer.

### Überlegungen zum Partnerpreis {#section-c6afad08c34b43e3a7a3637eea3328c3}

Diese Integration kann mit Gebühren verbunden sein. Informationen zu Preisen erhalten Sie bei Ihrem Kundenbetreuer.
