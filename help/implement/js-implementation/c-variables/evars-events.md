---
description: 'Wenn Sie zusätzliche Informationen verfolgen möchten, aber nicht über genügend Variablen verfügen, haben Sie jetzt Zugriff auf zusätzliche eVars und Erfolgsereignisse '
keywords: Analytics Implementation;evars;events;evars number;how many evars;how many events
title: Zusätzliche eVars und Ereignisse
topic: Developer and implementation
uuid: 6f53069b-6941-40f1-9db6-2d1839822b8f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Zusätzliche eVars und Ereignisse

Wenn Sie zusätzliche Informationen verfolgen möchten, aber nicht über genügend Variablen verfügen, haben Sie jetzt Zugriff auf zusätzliche eVars und Erfolgsereignisse:

> [!NOTE] JavaScript-H-Code unterstützt diese zusätzlichen eVars und Ereignisse nicht.

## Berechtigungen für benutzerdefinierte Dimensionen und Ereignisse {#section_869EC3D8A5614036A9C586F2B74FA7DC}

| Adobe Analytics-Produkt |  |  |  |
|---|---|---|---|
| Adobe Analytics – Foundation | 75 Eigenschaftsvariablen | 200 eVars | 1000 Ereignisse |
| Adobe Analytics – [Select](https://www.adobe.com/data-analytics-cloud/analytics/select.html) | 75 Eigenschaftsvariablen | 200 eVars | 1000 Ereignisse |
| Adobe Analytics – [Prime](https://www.adobe.com/data-analytics-cloud/analytics/prime.html) | 75 Eigenschaftsvariablen | 200 eVars | 1000 Ereignisse |
| Adobe Analytics – [Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html) | 75 Eigenschaftsvariablen | 250 eVars | 1000 Ereignisse |

## Befüllen von Variablen und Ereignissen {#section_DEA51A22BCBB4B92BDD25814AAD296E4}

* Wenn Sie die folgenden Versionen von [!DNL AppMeasurement] verwenden, können die Variablen in der Datenerfassungsbibliothek befüllt werden:

   * AppMeasurement für JavaScript, Version 1.4+
   * AppMeasurement für Flash, Version 3.9+
   * AppMeasurement für Java, Version 1.2.8+
   * AppMeasurement für Silverlight/.NET, Version 1.4.2+
   * AppMeasurement für PHP, Version 1.2.2+

* Wenn Sie eine frühere Version von Code oder JavaScript H.* verwenden, können Sie Textdaten befüllen und Verarbeitungsregeln verwenden, um die Variablen zu befüllen.
* Alle Version des Datenerfassungscodes können die Ereignisse 101–1000 befüllen.
* Verarbeitungsregeln können verwendet werden, um eVars 76–250 basierend auf Kontextdaten oder anderen Variablen zu befüllen.

## Häufig gestellte Fragen {#section_E915B03236BD47DCA065F1FC5A6E30C6}

* **Haben Adobe Analytics-Schnittstellen sofort Zugriff auf diese neuen Variablen?** Diese Schnittstellen haben sofort Zugriff: [!UICONTROL Analysis Workspace], [!UICONTROL Reports &amp; Analytics], [!UICONTROL Report Builder], [!UICONTROL Ad Hoc Analysis], APIs und [!UICONTROL Data Workbench].

* **Werden diese zusätzlichen eVars und Ereignisse automatisch in meinen Data Feeds angezeigt?** Sobald die neuen Variablen aktiviert sind, können Data Feeds darauf zugreifen. Neue eVar-Spalten werden erst dann angezeigt, wenn Sie sie einschließen. Neue Ereignisse werden jedoch in der Spalte event_list angezeigt, sobald sie aktiviert sind, und die Tabelle für die Ereignissuche enthält die Ereignisnamen für diese Ereignis-IDs. Aktivieren Sie keine neuen Ereignisse, wenn Sie sie noch nicht in den Data Feeds verwenden möchten.

* **Wie fordere ich neue Data Feed-Spalten an?** Weitere Informationen zur Anforderung von Spalten erhalten Sie unter [Data Feeds konfigurieren](https://marketing.adobe.com/resources/help/en_US/sc/clickstream/datafeeds_configure.html).

* **Angenommen, ich bin Analytics Ultimate-Kunde und möchte wieder zu Analytics Prime zurückkehren, habe aber derzeit mehr als 200 eVars aktiviert. Was muss ich tun?** Adobe deaktiviert keine Ihrer vorhandenen eVars, Sie können jedoch keine weiteren eVars aktivieren. Wenn Sie eVars deaktivieren, können Sie sie erst wieder aktivieren, wenn Sie weniger als die für Analytics Prime zulässige Höchstzahl von 200 eVars aktiviert haben.

