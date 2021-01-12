---
description: 'null'
title: Selligent-Data Connector für Adobe Analytics
uuid: e16c3ca6-b131-44b1-a36c-e39697677a96
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 98%

---


# Selligent-Data Connector für Adobe Analytics {#selligent-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Am 1. August 2021 werden wir die Adobe Data Connector-Technologie beenden. [Weitere Informationen ...](/help/import/data-connectors/data-connectors-eol.md)

Diese Integration umfasst die folgenden Hauptvorteile:

* Zusammenfassen von E-Mail-Marketing- und Analysedaten auf einer Berichtsoberfläche.
* Optimieren von E-Mail-Kampagnen nach Konversion und Beitrag zum Umsatz und zum Site-Erfolg.
* Auf dynamischen Marketingsegmenten basierendes Remarketing für wichtige Besucher und Marktsegmente.

## Dynamische Marketingsegmente {#section-a2216f3339304636bd5417249bd635a4}

Diese E-Mail-Integration unterstützt dynamische Marketingsegmente, die Sie bei der Förderung Ihres Unternehmens unterstützen. Diese Integration umfasst standardmäßig die folgenden Marketingsegmente:

| Segment | Beschreibung |
|---|---|
| **Profil für Warenkorbabbruch** |  Mit auf sie speziell abgestimmten Kampagnen können Sie Besucher, die zögern, ihren Einkaufswagen abzuschließen, in Kunden umwandeln. |
| **Profile für Kauf** |  Erhöhen Sie Nachbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf das Kaufverhalten der Besucher ausgerichtet sind. |
| **Profil für das Verhalten der Produkt-/Inhaltsansicht** |  Erreichen Sie potenzielle Kunden durch Marketingsegmente, die auf Produktansichten und Inhaltszugriffsprofilen basieren. |
| **Benutzerspezifische Remarketing-Segmente** | Kunden können auch benutzerspezifische Remarketing-Segmente erstellen und planen, die speziell auf die Bedürfnisse ihrer Benutzer abgestimmt sind. |

## Vor der Aktivierung dieser Integration {#before-you-activate-this-integration}

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente anhand Ihrer Implementierungen von Adobe Analytics und Ihrer E-Mail-Software.

Auf diese Weise wird sichergestellt, dass vor der Aktivierung geeignete Best Practices angewendet werden und die entsprechenden Voraussetzungen vorliegen. Dies führt zu einer optimalen und erfolgreichen Integration.

## Voraussetzungen für Adobe Analytics {#prerequisites-for-adobe-analytics}

Führt die erforderlichen Aktionen auf, die in Adobe Analytics durchgeführt werden müssen, bevor Sie die Integration bereitstellen können.

| Voraussetzung | Hinweise |
|---|---|
| Report Suite auswählen |  Beachten Sie, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren. |
| Analytics-Variablen konfigurieren |  Für diese Integration sind benutzerspezifische Ereignisse und benutzerspezifische eVars sowie optional zusätzliche Ereignisse und zusätzliche eVars erforderlich. Siehe „Konfigurieren von Analytics-Variablen für Selligent“. |
| Beauftragter Vertreter |  Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen. |
| Adobe Data Warehouse™ aktivieren |  Für diese Integration muss Data Warehouse aktiviert sein, damit Remarketing-Segmente generiert werden können. Wenn Sie Adobe Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe. |
| Empfänger-ID |  Für die Integration muss eine „Besucher-ID“ in einer Analytics-Variablen (eVar) erfasst und gespeichert werden. Die Besucher-ID (häufig als „Empfänger-ID“ bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse aus dem Selligent-System. Diese „Empfänger-ID“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird wiederum in das Selligent-System übertragen und kann für Remarketing-Zwecke genutzt werden. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden. |
| Externes Tracking |  Zum Gewährleisten einer erfolgreichen Integration sollten Sie die Best Practice zur Aktivierung des externen Trackings für jede gesendete E-Mail-Kampagne befolgen. Weitere Informationen finden Sie unten im Abschnitt „Selligent“.  |
| Datenschutz-Compliance |  Sie sollten sich darüber im Klaren sein, dass durch die Aktivierung des Empfänger- oder Besucher-ID-Trackings diese Funktion persönliche Informationen Ihrer Site-Besucher verfolgen kann. Dies wirkt sich auf den Datenschutz aus, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher. |

## Analytics-Variablen für Selligent konfigurieren {#configure-analytics-variables-for-selligent}

Für diese Integration müssen 2 eVars für jede Report Suite-Implementierung reserviert werden.

Abgesehen von diesen eVars können einige Ereignisse reserviert werden, je nachdem, welche Selligent-Daten in Analytics angezeigt werden sollen. Diese eVars und Ereignisse werden im Folgenden beschrieben:

<table id="table_2FFB865DBD80412F90DA8E224B12FB62"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Variablenname </th> 
   <th colname="col3" class="entry"> Verwendungsweise </th> 
   <th colname="col4" class="entry"> Einstellungen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> Zur Erfassung der Kampagnenidentifizierung der einzelnen E-Mail-Nachrichten. </td> 
   <td colname="col4"> <p><b>Status</b>: Aktiviert </p> <p><b>Zuordnung</b>: Zuletzt verwendet </p> <p><b>Läuft ab nach</b>: „Geschäftsentscheidung“ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eV ar </td> 
   <td colname="col2"> Empfänger-ID </td> 
   <td colname="col3"> Erfassen der anonymen Identifizierung Ihres Kunden, der auf die E-Mail-Kampagne geklickt hat. </td> 
   <td colname="col4"> <p><b>Status</b>: Aktiviert </p> <p><b>Zuordnung</b>: Zuletzt verwendet </p> <p><b>Läuft ab nach</b>: „Geschäftsentscheidung“ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Gesendet </td> 
   <td colname="col3"> Zum Speichern der Anzahl der von Selligent gesendeten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Numerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lieferung </td> 
   <td colname="col3"> Zum Speichern der Anzahl der zugestellten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Numerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Ansichten </td> 
   <td colname="col3"> Zum Speichern der Anzahl der angezeigten einmaligen E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Numerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Klicks </td> 
   <td colname="col3"> Zum Speichern der Anzahl, wie oft auf eine E-Mail geklickt wurde. </td> 
   <td colname="col4"> <p><b>Typ</b>: Numerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Nicht zugestellt </td> 
   <td colname="col3"> Zum Speichern der Anzahl der nicht zugestellten E-Mails. </td> 
   <td colname="col4"> <p><b>Typ</b>: Numerisch </p> <p><b>Beitrag</b>: Aktiviert </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voraussetzungen für Selligent {#prerequisites-for-selligent}

Führt die erforderlichen Informationen auf, die Sie über Ihr Selligent-Konto angeben müssen, bevor Sie die Integration bereitstellen können.

**Gültiges Selligent-Konto**

Zur Verwendung dieser Data Connectors-Integration benötigen Sie ein gültiges Selligent-Konto.

**Kontoinformationen**

Sie benötigen während der Einrichtung dieser Integration die folgenden Informationen zu Ihrem Selligent-Konto:

* **Adobe-Dienst-URL**:

   Die URL kann von der URL abgeleitet werden, die zum Anmelden bei der Selligent Marketing-Lösung verwendet wird. Ersetzen Sie den Teil „/simweb/login.aspx“ der URL durch „/automation/omniture.asmx“.

   z. B: `http://<client-specific install url>/automation/omniture.asmx`

* **Abfragezeichenfolgeparameter**: Diese werden an die URL der Landingpage für Nachrichten-ID und Empfänger-ID (Besucher-ID) angehängt. Dabei handelt es sich immer um die MID und RID für Nachrichten-ID bzw. Empfänger-ID.

* **Integrationstoken** Starten Sie das Manager-Tool in Simweb. Navigieren Sie dann zu **[!UICONTROL Configuration]** (Konfiguration) > **[!UICONTROL System Settings]** (Systemeinstellungen) > Registerkarte **[!UICONTROL General]** (Allgemein) > **[!UICONTROL System]**. Unter **[!UICONTROL Security]** (Sicherheit) finden Sie das Integrationstoken.

   ![](assets/selligent-integration_token.png)
