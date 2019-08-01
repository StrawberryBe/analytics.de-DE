---
description: Listet die erforderlichen Informationen aus Ihrem Selligent-Konto auf, bevor Sie die Integration bereitstellen können.
seo-description: Listet die erforderlichen Informationen aus Ihrem Selligent-Konto auf, bevor Sie die Integration bereitstellen können.
seo-title: Voraussetzungen für Selligent
solution: Analytics
title: Voraussetzungen für Selligent
uuid: 3 a 43 a 1 c 0-5 f 51-4 bc 8-b 6 b 9-0 c 46 aa 00 ba 9 f
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Prerequisites for Selligent{#prerequisites-for-selligent}

Listet die erforderlichen Informationen aus Ihrem Selligent-Konto auf, bevor Sie die Integration bereitstellen können.

**Gültiges Selligent-Konto**

Um diese Data Connectors-Integration verwenden zu können, müssen Sie über ein gültiges Selligent-Konto verfügen.

**Kontoinformationen**

Sie benötigen während dieser Integration die folgenden Informationen zu Ihrem Selligent-Konto:

* **Adobe-Dienst-URL**:

   Die URL kann von der URL abgeleitet werden, die zur Anmeldung bei der Selligent Marketing-Lösung verwendet wird. Ersetzen Sie den Teil "/simweb/login. aspx" der URL durch"/automation/omniture. asmx" .

   z. B.: http://<client-specific install url>/automation/omniture.asmx

* **Abfragezeichenfolgenparameter:** Diese werden an die URL der Einstiegsseite für Nachrichten-ID und Empfänger-ID (Besucher-ID) angehängt. Diese sind immer MID und RID für Nachrichten-ID bzw. Empfänger-ID.

* **Integrationstoken** Starten Sie das Tool Manager aus dem Simweb und wechseln Sie zu **[!UICONTROL Konfiguration]** &gt; **[!UICONTROL Systemeinstellungen]** &gt; **[!UICONTROL Registerkarte Allgemein]** &gt; **[!UICONTROL System]**. Under **[!UICONTROL Security]**, you can find the Integration token.

   ![](assets/selligent-integration_token.png)

