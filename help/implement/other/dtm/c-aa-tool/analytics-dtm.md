---
description: Stellen Sie Adobe Analytics mithilfe des Dynamic Tag Managements bereit, indem Sie das Adobe Analytics-Tool erstellen und den Seiten-Code entweder automatisch oder manuell konfigurieren. Für die meisten Benutzer wird die automatische Methode empfohlen.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;analytics tool;property;tool type;tool name;configuration method;analytics premium;evars;events
title: Adobe Analytics-Tool hinzufügen
topic: Developer and implementation
uuid: 1c54331e-de03-4f44-8002-a19723c585b0
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Adobe Analytics-Tool hinzufügen

Stellen Sie Adobe Analytics mithilfe des Dynamic Tag Managements bereit, indem Sie das Adobe Analytics-Tool erstellen und den Seiten-Code entweder automatisch oder manuell konfigurieren. Für die meisten Benutzer wird die automatische Methode empfohlen.

>[!NOTE] Für ein verbessertes Besucher-Tracking empfehlen wir dringend, den [Identitätsdienst](https://marketing.adobe.com/resources/help/de_DE/mcvid/) zu aktivieren.

## Hinzufügen eines Adobe Analytics-Tools {#section_D5066B21581B4F7F811AD0027BF44EA5}

1. Klicken Sie auf  **[!UICONTROL  *`Web Property Name`*]** > **[!UICONTROL Overview]** > **[!UICONTROL Add a Tool]** > **[!UICONTROL Adobe Analytics]** .

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
   <td colname="col2"> <p> <b>Automatisch</b> (empfohlen): Verwaltung der Konfiguration mit dem Dynamic Tag Management. Diese Methode ermöglicht die automatische Synchronisierung von <span class="keyword">Adobe Analytics</span>-Report Suites per <span class="keyword">Experience Cloud</span>-Anmeldung oder Web-Services-ID und verwaltet den AppMeasurement-Code. </p> <p>Sobald die Konten verknüpft sind, ruft das Dynamic Tag Management die IDs und Namen der <span class="keyword">Adobe Analytics</span>-Report Suite ab und fügt sie in die Benutzeroberfläche für die Tool-Konfiguration ein, wodurch Tools schneller und mit einem geringeren Risiko von Benutzerfehlern implementiert werden können. </p> <p> <p>Hinweis: Sie müssen die Option <span class="wintitle">Automatisch</span> wählen, wenn Sie <span class="keyword">Adobe Analytics Premium</span>-Kunde sind. </p> </p> <p>Füllen Sie die Felder der automatischen Konfiguration aus: </p> 
    <ul id="ul_8D9797B01E444B9C85B862A9F96B447C"> 
     <li id="li_0AC84C1F37B24C658F2178E50ECCC4B0"> <p> <b>Experience Cloud</b> (Standardwert): Verwendet <span class="keyword">Experience Cloud</span>-Single Sign-On. Geben Sie Ihre Experience Cloud-ID und Ihr Kennwort ein. </p> </li> 
     <li id="li_6C80468835D04CC09F4AEC46D1300310"> <p><b>Web-Services</b>: Geben Sie Ihren Web-Services-Benutzernamen und den gemeinsamen geheimen Schlüssel an. </p> <p>Die Anmeldedaten für gemeinsame geheime Schlüssel befinden sich unter <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Unternehmenseinstellungen</span> &gt; <a href="https://docs.adobe.com/content/help/de-DE/analytics/admin/company-settings/web-services-admin.html">Web-Services</a>. </p> <p>Entwickler finden unter <a href="https://marketing.adobe.com/developer/de_DE/get-started/enterprise-api/c-get-web-service-access-to-the-enterprise-api">Get Web Service Access to the Enterprise API</a> (Web-Service-Zugriff auf die Enterprise-API sichern) Informationen zum Abrufen der Web-Services-Anmeldedaten. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>Manuell</b>: Manuelle Verwaltung des AppMeasurement-Codes. Der <span class="keyword">Analytics</span><span class="keyword"> AppMeasurement</span> Code kann unter <span class="ignoretag"><span class="uicontrol"> Admin Tools</span> &gt; <span class="uicontrol"> Code-Manager</span></span> heruntergeladen werden. </p> <p>Klicken Sie auf <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/appmeasure_mjs.html">JavaScript (neu)</a>, um Informationen zum lokalen Download des Codes zu erhalten, damit Sie ihn kopieren und in das Feld <span class="wintitle">Code bearbeiten</span> in der <a href="/help/implement/other/dtm/c-aa-tool/library-management.md">Bibliotheksverwaltung</a> einfügen können. </p> <p>Füllen Sie die Felder für eine manuelle Konfiguration aus: </p> 
    <ul id="ul_CFB6CE78AEB743EF8B47BAAC42E2DB0A"> 
     <li id="li_5B7046CD95AB416F8C113B381A264D91"> <p><b>Produktionskonto-ID: </b>(Erforderlich) Ihr Produktionskonto für die Datenerfassung. Bei Analytics ist dies Ihre Report Suite-ID. Das Dynamic Tag Management installiert automatisch das richtige Konto in der Produktions- und Staging-Umgebung. </p> </li> 
     <li id="li_14E840FD79A0451BABEDD15DC0584768"> <p><b>Staging-Konto-ID: </b>(Erforderlich) Wird in Ihrer Entwicklungs- oder Testversion verwendet. Bei Analytics ist dies Ihre Report Suite-ID. Mit einem Staging-Konto werden Ihre Testdaten von der Produktion getrennt. </p> </li> 
     <li id="li_69E6C6A41F5240E1ABE8ABE0B9D151FC"> <p><b>Tracking-Server: Geben Sie die Informationen für Ihren Tracking-Server </b>an. </p> <p>Mit den Variablen <span class="wintitle">Tracking-Server</span> und <span class="wintitle">SSL-Tracking-Server</span> können Erstanbieter-Cookies bereitgestellt werden, in denen die Domäne enthalten ist, in der Bildabfrage und Cookie geschrieben wurden. Weitere Informationen finden Sie im Artikel zur <a href="https://helpx.adobe.com/de/analytics/kb/determining-data-center.html">ordnungsgemäßen Angabe der Variablen „trackingServer“ und „trackingServerSecure“</a>. </p> </li> 
     <li id="li_1A7271C68205428F8CA5548A96CACBEC"> <p><b>SSL-Tracking-Server:</b> Angabe der SSL-Tracking-Serverdaten. </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

1. Click **[!UICONTROL Create Tool]** to create the tool and display it for editing.

   Werkzeuge werden auf der [!UICONTROL Overview] Registerkarte angezeigt, unter [!UICONTROL Installed Tools].

1. (Bedingt) Konfigurieren Sie das Tool nach Bedarf weiter, indem Sie die Anweisungen unter den Links unten ( [!UICONTROL General], [!UICONTROL Library Management], [!UICONTROL Global Variables], [!UICONTROL Pageviews & Content], [!UICONTROL Link Tracking], [!UICONTROL Referrers & Campaigns], [!UICONTROL Cookies]und [!UICONTROL Customize Page Code]) befolgen.

Weiterführende Informationen finden Sie in den [häufig gestellten Fragen zu Adobe Analytics](/help/implement/faq.md).

## Ein bestehendes Adobe Analytics-Tool bearbeiten {#section_148B16AF429B4949B06238D90635B726}

Ein bestehendes Adobe Analytics-Tool kann bearbeitet werden, um die Konfigurierungseinstellungen anzupassen.

1. Click the  ![](assets/settings_gear.png) icon next to an installed tool from the [!UICONTROL Overview] tab.
1. Bearbeiten Sie die Felder nach Bedarf.

   Die folgende Tabelle enthält nur die Elemente, die sich von den Elementen unterscheiden, die beim Erstellen eines Analytics-Tools verfügbar sind (siehe Beschreibung oben). Sie können jedoch jedes beliebige Element auf der Seite ändern, wie in beiden Tabellen beschrieben.

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
   <td colname="col2"> <p>Hinweis: Durch Aktivierung dieser Einstellung wird eine manuell konfigurierte Implementierung zur automatischen Konfigurationsmethode geändert, die unter <span class="term">Konfigurationsmethode</span> beschrieben ist. </p> <p>Diese Option ermöglicht dem Dynamic Tag Management das automatische Abrufen Ihrer <span class="keyword">Adobe Analytics</span>-Kontokonfiguration. </p> <p>Es wird der neueste verfügbare AppMeasurement-Code verwendet und es werden Upgrade-Benachrichtigungen zur Auswahl angezeigt, sobald neue Versionen verfügbar werden. Sie können bei Bedarf, z. B. aus Kompatibilitätsgründen, auch frühere AppMeasurement-Versionen wiederherstellen. Es werden bis zu fünf frühere Versionen angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berechtigungen aktualisieren </p> </td> 
   <td colname="col2"> <p>Aktualisieren Sie beispielsweise die API, um mit einem Benutzer verbundene Report Suites zu aktualisieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (Bedingt) Konfigurieren Sie das Tool nach Bedarf weiter, indem Sie die Anweisungen unter den Links unten ( [!UICONTROL General], [!UICONTROL Library Management], [!UICONTROL Global Variables], [!UICONTROL Pageviews & Content], [!UICONTROL Link Tracking], [!UICONTROL Referrers & Campaigns], [!UICONTROL Cookies]und [!UICONTROL Customize Page Code]) befolgen.
1. Klicken Sie auf **[!UICONTROL Save Changes]**.
