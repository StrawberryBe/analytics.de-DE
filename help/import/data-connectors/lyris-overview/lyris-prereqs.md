---
description: Beschreibt die Voraussetzungen für eine erfolgreiche Integration.
seo-description: Beschreibt die Voraussetzungen für eine erfolgreiche Integration.
seo-title: Voraussetzungen für die Integration
solution: Analytics
title: Voraussetzungen für die Integration
uuid: ac 93 bf 4 d-a 71-4 4 fac -9 d 42-c 4856463 cbb 6
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Voraussetzungen für die Integration{#integration-prerequisites}

Beschreibt die Voraussetzungen für eine erfolgreiche Integration.

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente für Ihre Implementierungen von Adobe Analytics und Ihrer E-Email-Software.

Dadurch wird sichergestellt, dass vor der Aktivierung geeignete Best Practices und Voraussetzungen vorhanden sind. Dies führt zu einer optimalen und erfolgreichen Integration.

## Voraussetzungen für Adobe Analytics {#section-ddb9d4f3b283438ea33788f47f35e69a}

* **Report Suite spezifisch**: Wir empfehlen, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren.
* **Verfügbare und konfigurierte Analytics-Variablen**: Für diese Integration sind benutzerspezifische Ereignisse und benutzerspezifische evars sowie optional zusätzliche Ereignisse und zusätzliche evars erforderlich.

   Siehe [Analytics-Variablen für Lyris konfigurieren](../lyris-overview/lyris-analytics-variables.md#task-e70a62dc096d4f548d5070a67822f5e7)

* **Autorisierter Vertreter**: Es wird empfohlen, dass Ihr Unternehmen bei Aktivierung dieser Integration Gebühren in Übereinstimmung mit Ihrem Servicevertrag mit Adobe, Inc. oder Ihrem Servicevertrag bei einem der vertrauenswürdigen Partner von Adobe erbringt. Durch Aktivierung dieser Integration stellen Sie sicher, dass Sie ein autorisierter Vertreter Ihres Unternehmens sind; und somit beschließt Ihr Unternehmen, die Gebühren, sofern vorhanden, in der oben beschriebenen Servicevereinbarung zu zahlen.
* **Adobe Analytics Data Warehouse**: Für diese Integration muss Adobe Analytics Data Warehouse aktiviert werden, um Remarketing-Segmente zu generieren. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich an Adobe.
* **Empfänger-ID**: Die Integration erfordert, dass wir eine Besucher-ID in einer Analytics-Variable (evar) erfassen und speichern. Die Besucher-ID (häufig auch als Empfänger-ID bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Email-Adresse aus dem Lyris-System. Diese "Empfänger-ID" ist mit dem nachgeordneten Besucherverhalten auf der Site verknüpft (Warenkorbabbrüche, Käufe usw.). das wieder in das Lyris-System geholt wird und für Neumarketing-Zwecke genutzt werden kann. Während des Setup-Prozesses müssen Sie eine evar zu diesem Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Externe Verfolgung**: Wenn Sie aktuell nicht die beste Vorgehensweise zur Aktivierung der externen Verfolgung für jede E-Mail-Kampagne haben, die Sie senden, müssen Sie eine erfolgreiche Integration sicherstellen. Weitere Informationen finden Sie im Abschnitt zu Lyris.
* **Datenschutzeinhaltung**: Sie sollten wissen, dass diese Funktion durch Aktivierung der Empfänger- oder Besucher-ID-Verfolgung personenbezogene Informationen zu Ihren Site-Besuchern nachverfolgen kann. Dies hat Auswirkungen auf Datenschutz, was die Implementierung angemessener Vorgehensweisen Ihres Unternehmens erfordert, z. B. die Bereitstellung und Zustimmung Ihrer Site-Besucher.

## Voraussetzungen für die Lyris-emaillabs {#section-84abae9401224a3699fed861f715ebde}

* **Gültiges Lyris-Konto**: Um diese Data Connector-Integration verwenden zu können, müssen Sie über ein gültiges Lyris-Konto verfügen.
* **Kontoinformationen**: Während dieser Integration benötigen Sie die folgenden Informationen zu Ihrem Lyris-Konto:

   * *Lyris-API-Schlüssel*: Für Datenpopulation verwendet
   * *Abfragezeichenfolgenparameter*: Diese werden an die URL der Einstiegsseite für Nachrichten-ID und Empfänger-ID (Besucher-ID) angehängt.
   * *Lyris-Server/URL*: Der Serverwert, den Sie im System "Lyris" verwenden.
   * *Site-ID für Lyris*: Dies wird auch als "Kunden-ID" bezeichnet. Dies ist der eindeutige Wert für Ihre Instanz von Lyris HQ. Dies befindet sich unter "Kundeninformationen" im Abschnitt" Kontostartseite" von emaillabs.

