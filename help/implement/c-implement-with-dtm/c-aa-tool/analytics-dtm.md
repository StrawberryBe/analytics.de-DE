---
description: Stellen Sie Adobe Analytics mithilfe des dynamischen Tag-Managements bereit, indem Sie das Adobe Analytics-Tool erstellen und den Seiten-Code entweder automatisch oder manuell konfigurieren. Für die meisten Benutzer wird die automatische Methode empfohlen.
keywords: Analytics-Implementierung;Implementierungsmethode;dynamisches Tag-Management;dtm;Analytics-Tool;Eigenschaft;Tool-Typ;Tool-Name;Konfigurationsmethode;Analytics-Premium;evars;Ereignisse
seo-description: Stellen Sie Adobe Analytics mithilfe des dynamischen Tag-Managements bereit, indem Sie das Adobe Analytics-Tool erstellen und den Seiten-Code entweder automatisch oder manuell konfigurieren. Für die meisten Benutzer wird die automatische Methode empfohlen.
seo-title: Adobe Analytics-Tool hinzufügen
solution: Analytics
title: Adobe Analytics-Tool hinzufügen
topic: Entwickler und Implementierung
uuid: 1c54331e-de03-4f44-8002-a19723c585b0
translation-type: tm+mt
source-git-commit: 831ae375a90f021feddc6817a2602464be0d8414

---


# Adobe Analytics-Tool hinzufügen

Stellen Sie Adobe Analytics mithilfe des dynamischen Tag-Managements bereit, indem Sie das Adobe Analytics-Tool erstellen und den Seiten-Code entweder automatisch oder manuell konfigurieren. Für die meisten Benutzer wird die automatische Methode empfohlen.

>[!NOTE]
>
>Für eine verbesserte Besucherverfolgung empfehlen wir dringend, den [Identitätsdienst](https://marketing.adobe.com/resources/help/en_US/mcvid/)zu aktivieren.

## Ein Adobe Analytics-Tool hinzufügen {#section_D5066B21581B4F7F811AD0027BF44EA5}

1. Click  **[!UICONTROL *`Web Property Name`*]** &gt; **[!UICONTROL Overview]** &gt; **[!UICONTROL Add a Tool]** &gt; **[!UICONTROL Adobe Analytics]** .

   ![](assets/dtm-add-analytics-tool.png)

1. Füllen Sie die Felder aus:

<table id="table_1CFB53FE72E74CCB8CAA5D4E3873D286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tool-Typ </p> </td> 
   <td colname="col2">Der Typ des Tools, z. B. <span class="keyword">Adobe Analytics</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tool-Name </p> </td> 
   <td colname="col2">Ein beschreibender Name für dieses Tool. Dieser Name wird auf der Registerkarte <span class="wintitle">Übersicht</span> unter <span class="wintitle">Installierte Tools</span> angezeigt. </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Konfigurationsmethode </p> </td> 
   <td colname="col2"> <p> <b>Automatisch</b> (empfohlen): Verwaltung der Konfiguration mit dem Dynamic Tag Management. This method enables automatic synchronization of <span class="keyword"> Adobe Analytics</span> report suites via a <span class="keyword"> Experience Cloud</span> login or Web Services ID, and manages the [!DNL AppMeasurement] code. </p> <p>Sobald die Konten verknüpft sind, ruft das Dynamic Tag Management die IDs und Namen der <span class="keyword">Adobe Analytics</span>-Report Suite ab und fügt sie in die Benutzeroberfläche für die Tool-Konfiguration ein, wodurch Tools schneller und mit einem geringeren Risiko von Benutzerfehlern implementiert werden können. </p> <p> <p>Hinweis: Sie müssen die Option <span class="wintitle">Automatisch</span> wählen, wenn Sie <span class="keyword">Adobe Analytics Premium</span>-Kunde sind. Siehe Abschnitt <a href="../../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#section_AEAA44566B5A46D2922E17A11D7EA217" format="dita" scope="local">Adobe Analytics Premium aktivieren</a> unten. </p> </p> <p>Füllen Sie die Felder der automatischen Konfiguration aus: </p> 
    <ul id="ul_8D9797B01E444B9C85B862A9F96B447C"> 
     <li id="li_0AC84C1F37B24C658F2178E50ECCC4B0"> <p> <b>Experience Cloud</b> (Standardwert): Verwendet <span class="keyword">Experience Cloud</span>-Single Sign-On. Geben Sie Ihre Experience Cloud ID und Ihr Kennwort ein. </p> </li> 
     <li id="li_6C80468835D04CC09F4AEC46D1300310"> <p><b>Web-Services</b>: Geben Sie Ihren Web-Services-Benutzernamen und den gemeinsamen geheimen Schlüssel an. </p> <p>Die Anmeldedaten für gemeinsame geheime Schlüssel befinden sich unter <span class="uicontrol">Admin </span> &gt; <span class="uicontrol">Unternehmenseinstellungen</span> &gt; <a href="https://docs.adobe.com/content/help/en/analytics/admin/company-settings/web-services-admin.html" format="html" scope="external">Web-Services</a>. </p> <p>Entwickler finden unter <a href="https://marketing.adobe.com/developer/en_US/get-started/enterprise-api/c-get-web-service-access-to-the-enterprise-api" format="https" scope="external">Get Web Service Access to the Enterprise API</a> (Web-Service-Zugriff auf die Enterprise-API sichern) Informationen zum Abrufen der Web-Services-Anmeldedaten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>Manual: Manually manage the [!DNL AppMeasurement] code. </b> Der <span class="keyword">Analytics</span> <span class="keyword">AppMeasurement</span>-Code kann unter <span class="ignoretag"><span class="uicontrol">Admin Tools</span> &gt; <span class="uicontrol">Code-Manager</span></span> heruntergeladen werden. </p> <p>Click <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/appmeasure_mjs.html" format="https" scope="external"> JavaScript (new)</a> for information about downloading the code locally to copy and paste in the <span class="wintitle"> Edit Code</span> field in <a href="../../../implement/c-implement-with-dtm/c-aa-tool/library-management.md#concept_24654766343B4E82A9416A112D2125FE" format="dita" scope="local"> Library Management</a>. </p> <p>Füllen Sie die Felder der manuellen Konfiguration aus: </p> 
    <ul id="ul_CFB6CE78AEB743EF8B47BAAC42E2DB0A"> 
     <li id="li_5B7046CD95AB416F8C113B381A264D91"> <p><b>Produktionskonto-ID</b> (erforderlich): Ihr Produktionskonto für die Datenerfassung. Bei Analytics ist dies die Report Suite-ID. Das Dynamic Tag Management installiert automatisch das richtige Konto in der Produktions- und Staging-Umgebung. </p> </li> 
     <li id="li_14E840FD79A0451BABEDD15DC0584768"> <p><b>Staging-Konto-ID</b> (erforderlich): Wird in der Entwicklungs- oder Testumgebung eingesetzt. Bei Analytics ist dies die Report Suite-ID. Mit dem Staging-Konto werden Ihre Testdaten von der Produktion getrennt gehalten. </p> </li> 
     <li id="li_69E6C6A41F5240E1ABE8ABE0B9D151FC"> <p><b>Tracking-Server:</b> Angabe der Tracking-Server-Daten </p> <p>Mit den Variablen <span class="wintitle">Tracking-Server</span> und <span class="wintitle">SSL-Tracking-Server</span> können Erstanbieter-Cookies bereitgestellt werden, in denen die Domäne enthalten ist, in der Bildabfrage und Cookie geschrieben wurden. Weitere Informationen finden Sie im Artikel zur <a href="https://helpx.adobe.com/analytics/kb/determining-data-center.html" format="https" scope="external">ordnungsgemäßen Angabe der Variablen „trackingServer“ und „trackingServerSecure“</a>. </p> </li> 
     <li id="li_1A7271C68205428F8CA5548A96CACBEC"> <p><b>SSL-Tracking-Server:</b> Angabe der SSL-Tracking-Serverdaten. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

1. Klicken Sie auf **[!UICONTROL Tool erstellen], um das Tool und die Bearbeitungsanzeige zu erstellen.**

   Tools werden auf der Registerkarte „[!UICONTROL Übersicht]“ unter „[!UICONTROL Installierte Tools]“ angezeigt.

1. (Bedingt) Führen Sie bei Bedarf nach den Anweisungen unter den unten stehenden Links eine weitere Konfiguration des Tools durch ([!UICONTROL Allgemein], [!UICONTROL Bibliotheksverwaltung], [!UICONTROL globale Variablen], [!UICONTROL Seitenansichten und Inhalt], [!UICONTROL Linktracking], [!UICONTROL Referrer und Kampagnen], [!UICONTROL Cookies] und [!UICONTROL Seiten-Code anpassen]).

See [Frequently Asked Questions About the Adobe Analytics Tool](../../../implement/faq.md#concept_00DF9AF14D30469BB986BF56A448806B) for additional information about this tool.

## Ein bestehendes Adobe Analytics-Tool bearbeiten {#section_148B16AF429B4949B06238D90635B726}

Ein bestehendes Adobe Analytics-Tool kann bearbeitet werden, um die Konfigurierungseinstellungen anzupassen.

1. Klicken Sie auf das Symbol ![](assets/settings_gear.png) neben einem installierten Tool in der Registerkarte [!UICONTROL Übersicht].
1. Bearbeiten Sie die Felder wie gewünscht.

   In der folgenden Tabelle sind nur die Elemente enthalten, die von den verfügbaren Elementen abweichen, wenn (wie oben beschrieben) ein Analytics-Tool erstellt wird. Es kann jedoch jedes beliebige Element auf der Seite geändert werden, wie in beiden Tabellen beschrieben ist.

<table id="table_2B60CD109CFF4839AB7F91D61125EDFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Automatische Konfiguration aktivieren </p> </td> 
   <td colname="col2"> <p>Note: Enabling this setting changes a manually configured implementation to the automatic configuration method described in <span class="term"> Configuration Method</span>. </p> <p>Diese Option ermöglicht dem Dynamic Tag Management das automatische Abrufen Ihrer <span class="keyword">Adobe Analytics</span>-Kontokonfiguration. </p> <p>Der neueste verfügbare [!DNL AppMeasurement]-Code wird verwendet und es werden Upgrade-Benachrichtigungen zur Auswahl angezeigt, sobald neue Versionen verfügbar werden. Sie können bei Bedarf, z. B. aus Kompatibilitätsgründen, auch frühere [!DNL AppMeasurement]-Versionen wiederherstellen. Es werden bis zu fünf frühere Versionen angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Anmeldedaten aktualisieren </p> </td> 
   <td colname="col2"> <p>Sie können die API aktualisieren, beispielsweise um mit einem Benutzer verknüpfte Report Suites zu aktualisieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (Bedingt) Führen Sie bei Bedarf nach den Anweisungen unter den unten stehenden Links eine weitere Konfiguration des Tools durch ([!UICONTROL Allgemein], [!UICONTROL Bibliotheksverwaltung], [!UICONTROL globale Variablen], [!UICONTROL Seitenansichten und Inhalt], [!UICONTROL Linktracking], [!UICONTROL Referrer und Kampagnen], [!UICONTROL Cookies] und [!UICONTROL Seiten-Code anpassen]).
1. Klicken Sie auf **[!UICONTROL Änderungen speichern]**.
