---
title: Ausschluss-Links
description: Erfahren Sie, wie Sie Ausschluss-Links für Besucher Ihrer Website implementieren.
feature: Implementation Basics
exl-id: 08b8c7cc-28c6-45e3-ab44-77471eea8ef1
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 100%

---

# Implementieren von Ausschluss-Links

>[!IMPORTANT]
>
>Adobe empfiehlt die Verwendung des Opt-in-Dienstes, insbesondere für Organisationen, die sich mit DSGVO-Vorschriften befassen. Weitere Informationen finden Sie unter [Übersicht über den Opt-in-Dienst](https://experienceleague.adobe.com/docs/id-service/using/implementation/opt-in-service/optin-overview.html?lang=de) im Benutzerhandbuch des Experience Cloud ID-Dienstes.

Einige Besucher Ihrer Website ziehen es vor, dass ihre Browsing-Informationen nicht in Ihrem Datensatz enthalten sind. Adobe bietet die Möglichkeit, den Besuchern Ihrer Website die Option bereitzustellen, sich von der Datenerfassung ausschließen zu lassen. Alle Implementierungsarten werden berücksichtigt; Ihre Organisation ist für Ihre eigene Datenschutzrichtlinie und für die Einhaltung der von Ihnen unterzeichneten Bedingungen verantwortlich.

Wenn ein Besucher eine Opt-out-URL erreicht, wird er aufgefordert, ein Opt-out-Cookie zu installieren. Wenn ein Benutzer sich entscheidet, nicht verfolgt zu werden, und ein Opt-out-Cookie gesetzt wird, sendet Ihre JavaScript-Datei weiterhin Daten an die Adobe-Server. Diese Daten werden jedoch nicht verarbeitet oder in Berichte aufgenommen.

>[!TIP]
>
>Adobe bietet außerdem Datenschutzeinstellungen pro Report Suite an. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Datenschutzeinstellungen](../../admin/admin/privacy-settings.md).

## Opt-out-URL

Die Opt-out-Seite für Ihr Unternehmen hängt vom Wert der [`trackingServer`](../vars/config-vars/trackingserver.md)-Variablen in Ihrer Implementierung ab.

* In der Datenerfassungs-Benutzeroberfläche:
   1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
   1. Klicken Sie auf die gewünschte Eigenschaft.
   1. Klicken Sie auf die Registerkarte [!UICONTROL Erweiterungen] und dann unter „Adobe Analytics“ auf [!UICONTROL Konfigurieren].
   1. Klicken Sie auf das Akkordeon [!UICONTROL Allgemein] und notieren Sie den Wert [!UICONTROL Tracking-Server].

* In einer JavaScript-Implementierung:
   1. Öffnen Sie auf Ihrem Webserver die Datei AppMeasurement.js, die auf Ihrer Website verwendet wird, in einem Code- oder Texteditor.
   1. Notieren Sie den Wert der `trackingServer`-Variablen.

* Mithilfe des [Adobe Experience Cloud-Debuggers](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=de):
   1. Navigieren Sie mit dem Chrome-Browser zu Ihrer Website.
   1. Öffnen Sie den Experience Cloud-Debugger und gehen Sie dann zur Registerkarte [!UICONTROL Netzwerk].
   1. Notieren Sie den Wert [!UICONTROL Anfrage-URL – Hostname].

Wenn Sie die `trackingServer`-Domain Ihrer Implementierung gefunden haben, hängen Sie den Pfad `/optout.html` an das Ende an. Beispiel:

* Drittanbieter-Cookies: `https://example.data.adobedc.net/optout.html`
* Erstanbieter-Cookies: `https://stats.example.com/optout.html`

## Opt-out-Abfragezeichenfolgenparameter

Es gibt Einstellungen, die Sie mithilfe von Abfragezeichenfolgen automatisch auf diese Seite laden können.

### Gebietsschema

Wechseln Sie automatisch die Sprache der Opt-out-Seite, indem Sie den Abfragezeichenfolgenparameter `locale` einbeziehen. Weisen Sie diesem Abfragezeichenfolgenparameter einen der folgenden Werte zu:

* en_US (Englisch, standardmäßig)
* bg_BG (Bulgarisch)
* zh_CN (Vereinfachtes Chinesisch)
* zh_TW (Traditionelles Chinesisch)
* cs_CZ (Tschechisch)
* da_NK (Dänisch)
* nl_NL (Niederländisch)
* et_EE (Estnisch)
* fi_FI (Finnisch)
* fr_FR (Französisch)
* de_DE (Deutsch)
* el_GR (Griechisch)
* it_IT (Italienisch)
* jp_JP (Japanisch)
* ko_KR (Koreanisch)
* lv_LV (Lettisch)
* lt_LT (Litauisch)
* nb_NO (Norwegisch)
* pl_PL (Polnisch)
* pt_BR (Portugiesisch)
* sk_SK (Slowakisch)
* es_ES (Spanisch)

Zum Beispiel lädt `https://example.data.adobedc.net/optout.html?locale=ko_KR` die Opt-out-Seite auf Koreanisch.

>[!TIP]
>
>Der Abfragezeichenfolgewert `en_US` ist nicht erforderlich, da die Seite standardmäßig in Englisch geladen wird.

### Popup

Fügt der Seite eine Schaltfläche „Fenster schließen“ hinzu, wodurch die Möglichkeit besteht, die Opt-out-Seite zu einem Popup-Fenster zu machen. Verwenden Sie den Abfragezeichenfolgenparameter `popup` und geben Sie ihm den Wert `1`.

Zum Beispiel lädt `https://example.data.adobedc.net/optout.html?popup=1` die Opt-out-Seite mit einer Schaltfläche „Fenster schließen“.

>[!NOTE]
>
>Dieser Abfragezeichenfolgenparameter hat bisher ein Popup-Fenster erzwungen. Die meisten modernen Browser geben dem Endbenutzer jedoch Kontrolle über Popups.

### Opt-out mit einem Klick

Ermöglicht dem Benutzer, das Tracking sofort abzuwählen. Fügen Sie die beiden Abfragezeichenfolgenparameter `opt_out` und `confirm_change` hinzu, wobei jeder den Wert `1` erhält.

Beispielsweise installiert `https://example.data.adobedc.net/optout.html?opt_out=1&confirm_change=1` sofort das Opt-out-Cookie auf der Seite des Besuchers.

### Opt-in mit einem Klick

Ermöglicht dem Benutzer, sich sofort wieder beim Tracking anzumelden, indem er das Opt-out-Cookie löscht. Fügen Sie die beiden Abfragezeichenfolgenparameter `opt_in` und `confirm_change` hinzu, wobei jeder den Wert `1` erhält.

Beispielsweise löscht `https://example.data.adobedc.net/optout.html?opt_in=1&confirm_change=1` sofort das Opt-out-Cookie für den Besucher.
