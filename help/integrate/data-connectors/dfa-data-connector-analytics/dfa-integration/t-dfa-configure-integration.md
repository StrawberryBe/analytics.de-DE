---
description: Gehen Sie die DFA-Data Connectors-Integration schrittweise durch.
seo-description: Gehen Sie die DFA-Data Connectors-Integration schrittweise durch.
seo-title: Konfigurieren der DFA-Integration
title: Konfigurieren der DFA-Integration
uuid: 4 c 2 ac 58 a -87 c 6-46 f 3-9033-9404 beb 18 c 39
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Konfigurieren der DFA-Integration{#configure-the-dfa-integration}

Gehen Sie die DFA-Data Connectors-Integration schrittweise durch.

Auf den Konfigurationsseiten erhalten Sie einen Überblick über die Integration sowie praktische Links für weitere Informationen. Für diese Integration fallen sowohl Adobe- als auch DoubleClick-Gebühren an. Wenden Sie sich an die jeweiligen Verkaufsmitarbeiter der beiden Unternehmen und versichern Sie sich, dass Sie die Zusammensetzung der Gebühren verstehen.

1. Log in to the [!DNL Adobe Analytics].
1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Data Connectors]**.

   ![](assets/data_connectors.png)

1. Locate **[!UICONTROL DoubleClick DFA]**, then click **[!UICONTROL Add New]**.

   ![Schritt Ergebnis](assets/wizard-01.png)

   Geben Sie auf den Seiten des Integrationsassistenten die jeweiligen Informationen an und klicken Sie auf **[!UICONTROL Weiter]**. In der folgenden Tabelle werden die Informationen näher erläutert, die für den Abschluss der Integration mithilfe des Assistenten erforderlich sind.

<table id="table_8F6F7F304C36431DA5FD6E5D54F60FC0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Assistentenseite Nr. </th> 
   <th colname="col2" class="entry"> Feld </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> Integrationsname </td> 
   <td colname="col3"> Der Integrationsname, der von Genesis in der aktiven Integrationsliste der Report Suite angezeigt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> Integrations-E-Mail-Adresse </td> 
   <td colname="col3"> Die E-Mail-Adresse, an die sämtliche Benachrichtigungen zu dieser Integration gesendet werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Benutzername </td> 
   <td colname="col3"> Der für diese Integration zu verwendende DFA-API-Benutzername. Überprüfen Sie das API-Attribut in der DFA-Oberfläche, um Benutzern die API-Anmeldung zu ermöglichen. Nach der Aktivierung der API-Anmeldung wird ein Feld angezeigt, in dem ein Passwort für den Benutzer angegeben werden muss. Dieses Passwort muss zur Authentifizierung gemeinsam mit dem Benutzernamen beim Assistenten eingegeben werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Passwort </td> 
   <td colname="col3"> Das DFA-API-Passwort </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Advertiser-ID </td> 
   <td colname="col3"> <p>Die DFA-Advertiser- bzw. übergeordnete Floodlight-Konfigurations-ID Data Connectors verwendet diese ID, um den zu trackenden DFA-Advertiser zu identifizieren (Version 1.5 der Integration). Diese Advertiser-ID wird in Version 2.0 der Integration nicht verwendet - die übergeordnete Floodlight-Konfigurations-ID wird gesucht und verwendet. Anweisungen werden auf dem Bildschirm angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3 </td> 
   <td colname="col2"> DFA-Anzeigenvariable </td> 
   <td colname="col3"> Die Analytics-eVar, die Daten zum DFA-Kampagnenattribut, Impressionen und Klicks empfängt Dabei handelt es sich im Normalfall um die Trackingcode-eVar ( <span class="varname"> s. campaign </span>), Sie können aber jede verfügbare evar auswählen. Data Connectors fügt außerdem die folgenden DFA-bezogenen Classifications zur ausgewählten eVar hinzu: <p><b>Kampagnen</b>: Eine Sammlung an Anzeigen mit gemeinsamer Botschaft, die auf mehreren Sites bereitgestellt werden </p> <p><b>Sitename</b>: Die Site, auf der die Anzeige bereitgestellt wurde </p> <p><b>Anzeigenname</b>: Der in Ihrem DFA-Konto festgelegte Anzeigenname </p> <p><b>Siteplatzierungsname</b>: Die Website und Seite, auf der die Anzeige bereitgestellt wurde </p> <p><b>Bereitstellungswerkzeug</b>: DoubleClick for Advertisers </p> <p><b>Kanal</b>: Banneranzeige </p> <p><b>Kostenzusammensetzung</b>: CPM, CPC oder fest, je nach Kostenzusammensetzung der Anzeige </p> <p><b>Creative-Name</b>: Der Name der kreativen Inhalte im Zusammenhang mit einer Anzeige/Platzierung/Creative-ID </p> <p><b>DFA &gt; SearchCenter-Deduplizierung</b>: Legt fest, dass DFA Werte in SearchCenter-Variablen eingibt, wenn DFA-Clickthrough- oder Durchsichtsaktionen ausgeführt werden. Weitere Informationen finden Sie unter <a href="../../dfa-data-connector-analytics/dfa-integration-features.md#concept-ff93289d1662410e98f62c200394b3e3" format="dita" scope="local">SearchCenter-Deduplizierung</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> Impressionen </td> 
   <td colname="col3"> Das benutzerspezifische Ereignis, an das DFA-Impressionsmetrikdaten gesendet werden. Impressionen stellen die Anzahl an Bereitstellungen der Anzeige dar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> Klicks </td> 
   <td colname="col3"> Wählen Sie das benutzerspezifische Ereignis, an das DFA-Klickmetrikdaten gesendet werden. Klicks stellen die Anzahl der wie durch die Weiterleitung von DFA gemessenen Klicks auf die Anzeige durch Besucher dar. Die Klickmetrik steht in Zusammenhang mit der Analytics-Clickthrough-Metrik. <p>Hinweis: DFA-Klicks und Analytics-Clickthroughs stimmen aufgrund von Unterschieden in der Erfassungsart der Daten unter Umständen nicht genau überein. For more information, see <a href="../../dfa-data-connector-analytics/dfa-reconciling-metric-discrepancies/dfa-metric-definitions.md#concept-2d5cd5ddd2594bb386a16a2764f30982" format="dita" scope="local"> Metric Definitions </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Durchsichtsvariable </td> 
   <td colname="col3"> <p>Die Analytics-eVar, an die DFA-Durchsichtsdaten gesendet werden Mithilfe der Durchsichtsvariable können Sie erfahren, auf welche Weise Durchsichten die Konversionsraten auf Ihrer Site beeinflussen. </p> <p>Data Connectors fügt dieselben DFA-bezogenen Classifications zu dieser eVar hinzu wie zur DFA-Anzeigenvariable (weitere Informationen finden Sie oben). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Zeit seit letzter Ansicht (Durchsichtszeit-Behältervariable) </td> 
   <td colname="col3"> Die Analytics-eVar, an die die Daten bezüglich der DFA-Zeit seit der letzten Ansicht gesendet werden Die Zeit seit der letzten Ansicht gibt an, wie viel Zeit seit der letzten Anzeigendurchsicht verstrichen ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Durchsichten </td> 
   <td colname="col3"> Das benutzerspezifische Ereignis, an das DFA-Durchsichtsmetrikdaten gesendet werden Verwenden Sie das Durchsichtsereignis mit der Durchsichtsvariable, um herauszufinden, welche Kampagnen keinen direkten Clickthrough veranlassen, aber unter Umständen eine Rolle bei der Erhöhung des Datenverkehrs auf der Site zu einem späteren Zeitpunkt gespielt haben. <p>Das ausgewählte benutzerdefinierte Ereignis wird durch Data Connectors in „Durchsichten“ umbenannt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> Fehlgeschlagene DFA-Abfrage </td> 
   <td colname="col3"> (Optional) Die Analytics-eVar, an die alle gemeldeten Benachrichtigungscodes zu fehlgeschlagenen DFA-Abfragen gesendet werden Mögliche DFA-Benachrichtigungscodes sind unter anderem: 
    <ul id="ul_85FC7FB19F7F4ADF83ABCA6DDB44CE19"> 
     <li id="li_0A3181DED5A149588A0D3F1584E2FE8B"><b>nc</b>: Kein DoubleClick-Cookie (No Cookie) </li> 
     <li id="li_D397AA73AD5E4086A18B87F271E4EC14"><b>oo</b>: Benutzer ist abgemeldet (Opted Out) </li> 
     <li id="li_5AC1D0C8049340B4AD857D88E275CBD6"><b>nh</b>: Kein Kampagnenverlauf (No History) </li> 
     <li id="li_73A8C5E905C54E2BB531A1FCDBC6AA1A"><b>qe</b>: Abfragefehler (Zeitüberschreitung, Serverausfall usw. – Query Error) </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> Timeout-Ereignis </td> 
   <td colname="col3"> <p>Das Analytics-Zählerereignis, dessen Wert bei jedem Ablauf von <span class="varname"> s. maxdelay- </span> Timer abläuft und von den DFA-Servern keine Antwort empfangen wurde. Use this event to configure the <span class="varname"> s.maxDelay </span> variable (see <a href="../../dfa-data-connector-analytics/dfa-integration/dfa-tuning-s-maxlelay.md#concept-6deb28eee18e414db220d6009d449f0d" format="dita" scope="local"> Tuning s.maxDelay </a>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

