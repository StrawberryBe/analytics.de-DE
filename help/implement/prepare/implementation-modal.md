---
title: Implementierung modal
description: Setzen Sie mit den Erfahrungen von Erstkonsumenten Adobe Analytics-Implementierungen um.
translation-type: tm+mt
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651

---


# Implementierung modal

<!-- https://activation.adobedtm.com/index.php?redirected=1 -->

Das modale Fenster &quot;Willkommen bei Adobe Analytics&quot;bietet einen vereinfachten Arbeitsablauf zum Erstellen einer Report Suite. Adobe empfiehlt, diesen Workflow zu verwenden, wenn in Ihrem Unternehmen mehr Report Suites benötigt werden.

![Modal-Screenshot](assets/implementation-modal.png)

## Voraussetzungen

Ihre Adobe-ID muss Zugriff auf Adobe Analytics und Adobe Experience Platform Launch haben. Wenn Sie keinen Zugriff auf Launch haben, können Sie in eine Authentifizierungs-Schleife eingefügt werden, in der Sie aufgefordert werden, Ihre Anmeldedaten unbegrenzt zu überprüfen. Wenden Sie sich an einen Systemadministrator in Ihrem Unternehmen, um Zugriff auf Launch zu erhalten.

## Zugriff auf das Modell

Greifen Sie auf das Modal zu, um eine Report Suite mit den folgenden Schritten zu erstellen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Click the 9-grid icon at the top, then click [!UICONTROL Adobe Analytics].
3. Wenn Sie noch keine Report Suite erstellt haben, wird das Modal automatisch angezeigt. Wenn für dieses Anmeldeunternehmen eine Report Suite vorhanden ist, klicken Sie auf das Hilfesymbol oben rechts und dann auf [!UICONTROL Willkommen bei Adobe Analytics].

> [!NOTE] Die Option &quot; [!UICONTROL Willkommen bei Adobe Analytics] &quot;wird nur angezeigt, wenn Sie sich über die Adobe Experience Cloud anmelden. Wenn Sie sich über veraltete Domänen anmelden, ist das Modal nicht verfügbar.

## Erstellen einer Report Suite

Klicken Sie auf die Schaltfläche &quot; [!UICONTROL Setup] starten&quot;, um den Arbeitsablauf zur Erstellung der Report Suite zu starten.

![RS-Assistent](assets/analytics-implementation-rs-wizard.png)

### Eigenschaftstyp

Mithilfe des Eigenschaftstyps kann Adobe einige Backend-Einstellungen anhand des Ortes ermitteln, an dem Sie Analytics implementieren möchten.

* **Website**: Wenn Sie Adobe Analytics nur für eine Website implementieren möchten.
* **Native mobile App**: Wenn Sie Adobe Analytics nur für eine mobile App implementieren möchten.
* **Beide**: Wenn diese Report Suite Daten für eine Website und eine mobile App enthält.

### Branchen

Geben Sie Ihr primäres Geschäftsmodell an. Diese Einstellung unterstützt Adobe bei der Vorkonfiguration einiger Variablennamen und Einstellungen, die auf Ihrem primären Geschäftsmodell basieren.

### Datenschicht

Eine [Datenschicht](data-layer.md) ist ein JavaScript-Objekt, das alle in Ihrer Implementierung verwendeten Variablen an einem einzigen hilfreichen Ort organisiert. See [Data layers](data-layer.md) for more information.

### Datenspeicher

Geben Sie der Report Suite einen benutzerfreundlichen Namen. Ihre Report Suite-ID (RSID) wird automatisch basierend auf dem Anzeigenamen und dem Anmeldeunternehmen generiert.

### Zeitzone

Stellen Sie sicher, dass Adobe die richtige Zeitzone für die Report Suite erkannt hat.

### Geschätzte Seitenansichten pro Tag

Schätzen Sie, wie viel Traffic Ihre Website oder App pro Tag erhält. Anhand dieser Informationen kann Adobe der Report Suite die richtige Menge an Verarbeitungsressourcen zuweisen.

### Basiswährung

Legen Sie fest, in welcher Währung die Report Suite Geldwerte speichert.

> [!IMPORTANT] Stellen Sie sicher, dass Sie die richtige Währung angeben, insbesondere wenn Sie Berichterstattungsanforderungen für den Umsatz haben. Es ist schwierig, die Basiswährung nach dem Beginn der Datenerfassung zu ändern.

## Ressourcen für die Implementierung

Nachdem die Report Suite erstellt wurde, haben Sie zwei Möglichkeiten, um mit der Implementierung fortzufahren:

* **Gehen Sie zu Adobe Experience Platform Launch**: Links zu [launch.adobe.com](https://launch.adobe.com) zum Konfigurieren der Implementierung und zum Herunterladen des Bereitstellungscodes. Siehe [Implementierung mit Launch](../launch/overview.md). Adobe empfiehlt in den meisten Fällen die Verwendung von Launch.
* **Implementierungscode** herunterladen: Bietet einen direkten Link zum Herunterladen von JavaScript-Dateien für eine manuelle JavaScript-Implementierung. Siehe [AppMeasurement für JavaScript](../js/overview.md).
