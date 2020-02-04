---
title: Ausschluss-Links
description: Erfahren Sie, wie Sie Ausschluss-Links für Besucher Ihrer Site implementieren.
translation-type: tm+mt
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# Implementieren von Ausschluss-Links

> [!IMPORTANT] Adobe empfiehlt die Verwendung des Opt-in-Dienstes, insbesondere für Organisationen, die sich mit GDPR-Vorschriften befassen. See [Opt-in service overview](https://docs.adobe.com/content/help/en/id-service/using/implementation/opt-in-service/optin-overview.html) in the Experience Cloud Identity Service user guide.

Einige Besucher Ihrer Website ziehen es vor, ihre Browserinformationen nicht in Ihren Datensatz aufzunehmen. Adobe bietet die Möglichkeit, Besuchern Ihrer Website die Möglichkeit zu geben, sich von der Erfassung ihrer Informationen abzumelden. Alle Implementierungstypen sind untergebracht. Ihre Organisation ist für Ihre eigenen Datenschutzrichtlinien und die Einhaltung Ihrer unterzeichneten Bedingungen verantwortlich.

Wenn ein Besucher eine Ausschluss-URL erreicht, wird er aufgefordert, ein Ausschluss-Cookie zu installieren. Wenn ein Benutzer sich dafür entscheidet, nicht verfolgt zu werden und ein Ausschluss-Cookie gesetzt ist, sendet Ihre JavaScript-Datei weiterhin Daten an Adobe-Server. Diese Daten werden jedoch nicht verarbeitet oder in Berichte aufgenommen.

> [!TIP] Adobe bietet außerdem Datenschutzeinstellungen pro Report Suite an. Siehe [Datenschutzeinstellungen](../../admin/admin/privacy-settings.md) im Admin-Benutzerhandbuch.

## Ausschluss-URL

Die Ausschluss-Seite für Ihr Unternehmen hängt vom [`trackingServer`](../vars/config-vars/trackingserver.md) Variablenwert in Ihrer Implementierung ab.

* Starten der Adobe Experience Platform:
   1. Melden Sie sich bei [launch.adobe.com](https://launch.adobe.com) an und klicken Sie auf die gewünschte Eigenschaft.
   2. Click the [!UICONTROL Extensions] tab, then click [!UICONTROL Configure] under Adobe Analytics.
   3. Klicken Sie auf das Akkordeon &quot; [!UICONTROL Allgemein] &quot;und beachten Sie den Wert &quot; [!UICONTROL Tracking-Server] &quot;.

* In einer JavaScript-Implementierung:
   1. Öffnen Sie auf Ihrem Webserver die Datei AppMeasurement.js, die auf Ihrer Site verwendet wird, in einem Code- oder Texteditor.
   2. Notieren Sie den `trackingServer` Variablenwert.

* Using the [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html):
   1. Navigieren Sie mit dem Chrome-Browser zu Ihrer Site.
   2. Öffnen Sie den Experience Cloud-Debugger und gehen Sie dann zur Registerkarte [!UICONTROL Netzwerk].
   3. Notieren Sie den Wert [!UICONTROL Request URL - Hostname] .

Wenn Sie die `trackingServer` Domäne Ihrer Implementierung gefunden haben, hängen Sie den Pfad `/optout.html` an das Ende an. Beispiel:

* Drittanbieter-Cookies: `https://example.sc.omtrdc.net/optout.html`
* Erstanbieter-Cookies: `https://stats.example.com/optout.html`

## Abfragezeichenfolgen-Parameter für Ausschluss

Es gibt Einstellungen, die Sie mithilfe von Abfragezeichenfolgen automatisch auf diese Seite laden können.

### Gebietsschema

Wechseln Sie automatisch die Sprache der Ausschluss-Seite, indem Sie den Abfragezeichenfolgenparameter `locale` einbeziehen. Weisen Sie diesem Abfragezeichenfolgenparameter einen der folgenden Werte zu:

* en_US (Englisch, Standard)
* bg_BG (Bulgarisch)
* zh_CN (Vereinfachtes Chinesisch)
* zh_TW (traditionelles Chinesisch)
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

Zum Beispiel `https://example.sc.omtrdc.net/optout.html?locale=ko_KR` lädt die Ausschluss-Seite auf Koreanisch.

> [!TIP] Der Wert der `en_US` Abfragezeichenfolge ist nicht erforderlich, da die Seite standardmäßig in Englisch geladen wird.

### Popup

Fügt der Seite die Schaltfläche &quot;Fenster schließen&quot;hinzu, sodass die Ausschluss-Seite ein Popup-Fenster werden kann. Verwenden Sie den `popup` Abfragezeichenfolgenparameter und geben Sie ihm den Wert `1`.

Lädt beispielsweise die Ausschluss-Seite mit der Schaltfläche &quot;Fenster schließen&quot;. `https://example.sc.omtrdc.net/optout.html?popup=1`

> [!NOTE] Dieser Abfragezeichenfolgen-Parameter hat bisher ein Popup-Fenster erzwungen. Die meisten modernen Browser geben dem Endbenutzer jedoch Kontrolle über Popups.

### Ausschluss mit einem Klick

Ermöglicht dem Benutzer, die Verfolgung sofort abzuwählen. Fügen Sie die beiden Abfragezeichenfolgenparameter hinzu `opt_out` und `confirm_change`geben Sie jeweils den Wert `1`.

Beispielsweise wird das Ausschluss-Cookie sofort auf der Seite des Besuchers installiert `https://example.sc.omtrdc.net/optout.html?opt_out=1&confirm_change=1` .

### Single-Click-Teilnahme

Ermöglicht dem Benutzer, sich sofort wieder bei der Verfolgung anzumelden, indem er das Ausschluss-Cookie löscht. Fügen Sie die beiden Abfragezeichenfolgenparameter hinzu `opt_in` und `confirm_change`geben Sie jeweils den Wert `1`.

Löscht beispielsweise `https://example.sc.omtrdc.net/optout.html?opt_in=1&confirm_change=1` sofort das Ausschluss-Cookie für den Besucher.
