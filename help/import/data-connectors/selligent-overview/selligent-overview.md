---
description: 'null'
title: Selektiver Data Connector für Adobe Analytics
uuid: e16c3ca6-b131-44b1-a36c-e39697677a96
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Selligent Data Connector for Adobe Analytics{#selligent-data-connector-for-adobe-analytics}

Diese Integration umfasst die folgenden Hauptvorteile:

* Konsolidieren Sie E-Mail-Marketing- und Analysedaten in einer Berichtsschnittstelle.
* Optimieren Sie E-Mail-Kampagnen nach Konversion und Beitrag zum Umsatz und zum Site-Erfolg.
* Markieren Sie anhand dynamischer Marketing-Segmente erneut wichtige Besucher und Marktsegmente.

## Dynamische Marketingsegmente {#section-a2216f3339304636bd5417249bd635a4}

Diese E-Mail-Integration unterstützt dynamische Marketingsegmente, die Sie bei der Förderung Ihres Unternehmens unterstützen. Diese Integration umfasst die folgenden Marketingsegmente standardmäßig:

| Segment | Beschreibung |
|---|---|
| **Einkaufswagenabbruchprofil** | hilft Besuchern, sich durch Feinabstimmungskampagnen zu Kunden zu konvertieren, die speziell für diejenigen entwickelt wurden, die zögern, Einkaufswagen abzuschließen. |
| **Kaufprofil** | Erhöhen Sie Wiederholungsbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf die Kaufmuster der Besucher ausgerichtet sind. |
| **Verhaltensprofil "Produkt/Inhalt"** | Kontaktieren Sie potenzielle Kunden über Marketingsegmente, die auf Produktansichten und der Erstellung von Inhaltsprofilen basieren. |
| **Benutzerspezifische Remarketing-Segmente** | Kunden können auch benutzerspezifische Remarketing-Segmente erstellen und planen, die den Anforderungen ihrer Benutzer entsprechen. |

## Vor Aktivierung dieser Integration{#before-you-activate-this-integration}

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Punkte in Bezug auf Ihre Implementierungen von Adobe Analytics und Ihrer E-Mail-Software.

Auf diese Weise wird sichergestellt, dass vor der Aktivierung geeignete Best Practices und Voraussetzungen vorhanden sind. Dies führt zu einer optimalen und erfolgreichen Integration.

## Voraussetzungen für Adobe Analytics{#prerequisites-for-adobe-analytics}

Listet die erforderlichen Aktionen auf, die in Adobe Analytics durchgeführt werden müssen, bevor Sie die Integration bereitstellen können.

| Voraussetzung | Hinweise |
|---|---|
| Report Suite auswählen | Beachten Sie, dass diese Integration spezifisch für Report Suites ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren. |
| Analytics-Variablen konfigurieren | Für diese Integration sind benutzerdefinierte Ereignisse und benutzerdefinierte eVars sowie optional zusätzliche Ereignisse und eVars erforderlich. Siehe Konfigurieren von Analytics-Variablen für Selligent. |
| Bevollmächtigter | Achten Sie darauf, dass Ihre Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe erhebt. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein Bevollmächtigter Ihres Unternehmens sind. und somit ist Ihr Unternehmen bereit, die in der oben beschriebenen Servicevereinbarung genannten Gebühren zu zahlen, sofern vorhanden. |
| Adobe Data Warehouse™ aktivieren | Für diese Integration muss Data Warehouse aktiviert sein, damit Remarketing-Segmente generiert werden können. Wenn Sie Adobe Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe. |
| Recipient ID | Die Integration erfordert, dass wir eine "Besucher-ID"in einer Analytics-Variablen (eVar) erfassen und speichern. Die Besucher-ID (häufig als "Empfänger-ID"bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse des Selligent-Systems. Diese "Empfänger-ID"ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft. die in das Selligent-System zurückgezogen werden und für Remarketing-Zwecke genutzt werden können. Während des Setupprozesses müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden. |
| Externe Verfolgung | Wenn Sie derzeit nicht die Best Practice zur Aktivierung der externen Verfolgung für jede gesendete E-Mail-Kampagne befolgen, müssen Sie dies tun, um eine erfolgreiche Integration sicherzustellen. Weitere Informationen finden Sie im Abschnitt Selligent. |
| Datenschutzbestimmungen | Sie sollten sich bewusst sein, dass diese Funktion durch Aktivierung der Empfänger- oder Besucher-ID-Verfolgung persönlich identifizierbare Informationen über Ihre Site-Besucher verfolgen kann. Dies hat Auswirkungen auf die Privatsphäre, die die Implementierung geeigneter Verfahren durch Ihr Unternehmen erfordern, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher. |

## Analytics-Variablen für Selligent konfigurieren{#configure-analytics-variables-for-selligent}

Für diese Integration müssen zwei eVars für jede Report Suite-Implementierung reserviert werden.

Neben diesen eVars können abhängig von den Daten von Selligent, die Sie in Analytics sehen möchten, einige Ereignisse reserviert werden. Diese eVars und Ereignisse werden wie folgt beschrieben:

<table id="table_2FFB865DBD80412F90DA8E224B12FB62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Variablenname </th> 
   <th colname="col3" class="entry"> Verwendung </th> 
   <th colname="col4" class="entry"> Einstellungen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> Zur Erfassung der Kampagnenidentifizierung der einzelnen E-Mail-Nachrichten. </td> 
   <td colname="col4"> <p><b>Status</b>: Aktiviert </p> <p><b>Zuordnung</b>: Zuletzt verwendet </p> <p><b>Läuft ab nach</b>: "Geschäftsentscheidung" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eV </td> 
   <td colname="col2"> Recipient ID </td> 
   <td colname="col3"> Zur Erfassung der anonymen ID für Ihren Kunden, der auf die E-Mail-Kampagne geklickt hat. </td> 
   <td colname="col4"> <p><b>Status</b>: Aktiviert </p> <p><b>Zuordnung</b>: Zuletzt verwendet </p> <p><b>Läuft ab nach</b>: "Geschäftsentscheidung" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Gesendet </td> 
   <td colname="col3"> Zum Speichern der Anzahl der von Selligent gesendeten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Ausgeliefert </td> 
   <td colname="col3"> So speichern Sie die Anzahl der ausgelieferten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Ansichten </td> 
   <td colname="col3"> Zum Speichern der Anzahl der angezeigten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Klicks </td> 
   <td colname="col3"> Um zu speichern, wie oft auf eine E-Mail geklickt wurde. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Absprungen </td> 
   <td colname="col3"> Zum Speichern der Anzahl der abgesetzten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Nummerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voraussetzungen für Selligent{#prerequisites-for-selligent}

Listet die erforderlichen Informationen auf, die Sie über Ihr Selligent-Konto bereitstellen müssen, bevor Sie die Integration bereitstellen können.

**Gültiges eigenständiges Konto**

Zur Verwendung dieser Data Connectors-Integration benötigen Sie ein gültiges Selligent-Konto.

**Kontoinformationen**

Sie benötigen während der Integration die folgenden Informationen zu Ihrem Selligent-Konto:

* **Adobe-Dienst-URL**:

   Die URL kann von der URL abgeleitet werden, die zum Anmelden bei der Selligent Marketing Solution verwendet wird. Ersetzen Sie den Teil "/simweb/login.aspx"der URL durch "/automation/omniture.asmx".

   z. B: `http://<client-specific install url>/automation/omniture.asmx`

* **** Abfragezeichenfolgenparameter: Diese werden an die URL der Einstiegsseite für Nachrichten-ID und Empfänger-ID(Besucher-ID) angehängt. Dabei handelt es sich immer um MID und RID für Nachrichten-ID und Empfänger-ID.

* **Integrationstoken** Starten Sie das Manager-Tool von Simweb aus und gehen Sie zu **[!UICONTROL Konfiguration]** &gt; **[!UICONTROL Systemeinstellungen]** &gt; **[!UICONTROL Allgemein]** &gt; **[!UICONTROL System]**. Unter **[!UICONTROL Sicherheit]** finden Sie das Integrationstoken.

   ![](assets/selligent-integration_token.png)
