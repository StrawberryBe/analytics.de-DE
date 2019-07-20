---
description: 'null '
seo-description: 'null'
seo-title: Adobe Analytics GDPR-Arbeitsablauf
title: Adobe Analytics GDPR-Arbeitsablauf
uuid: f 24 e 8 be 3-8 b 5 c -409 b-ad 6 b -770198 ae 2549
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Adobe Analytics GDPR-Arbeitsablauf

Willkommen beim DSGVO-Workflow von Adobe Analytics! Dieser Workflow beinhaltet die erforderlichen Schritte, die Sie durchführen müssen, damit Ihre Adobe Analytics-Implementierung die DSGVO-Zugriffs- und -Löschberechtigungen von Datensubjekten unterstützt.

<table id="table_0E561F62247A4D01B6E7180560082DC9"> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> Beschreibung der Aufgabe </th> 
   <th colname="col3" class="entry"> Links zu Anweisungen und weiteren Informationen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step1_icon.png" id="image_15849358972A4846A54FCB51997576D5" /> Stellen Sie sicher, dass all Ihre Report Suites, die möglicherweise DSGVO-relevante Daten enthalten, Ihrer Experience Cloud- oder IMS-Organisation zugewiesen sind. </p> <p>DSGVO-Anfragen werden unter Verwendung einer Experience Cloud-Organisation eingereicht und auf alle Report Suites dieser Organisation angewendet. Anfragen gelten nicht für Report Suites, die nicht der entsprechenden Organisation zugeordnet sind, selbst wenn sie Ihrem Anmeldeunternehmen angehören. </p> </td> 
   <td colname="col3"> <p>Weitere Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/report-suite-mapping.html" format="html" scope="external">Report Suites einer Organisation zuordnen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step2_icon.png" id="image_372B2C65DFAD46E39AE4D715313ABD0E"/> Legen Sie Ihre Richtlinie zur Datenaufbewahrung fest. </p> </td> 
   <td colname="col3"> <p>Die Richtlinie zur Datenaufbewahrung muss vorhanden sein, damit Adobe DSGVO-Zugriffs- und -Löschanfragen bearbeiten kann. </p> <p>Weitere Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/reference/data-retention-client-table-faq.html" format="html" scope="external">Häufig gestellte Fragen zur Datenaufbewahrung in Analytics</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step3_icon.png" id="image_30DB956290CC4E64A7085B46364BE059" /> Machen Sie sich mit den DULE/GDPR-Beschriftungen, Adobe Analytics-IDs, Namensräumen und der ID-Erweiterung vertraut. </p> </td> 
   <td colname="col3"> <p> Lesen Sie hierzu folgende Themen dieser Dokumentation: 
     <ul id="ul_F6E94B9281D446DB8F1F859F6056543B"> 
      <li id="li_6389D094B4B04CA181E5F077BF8C0F8E"><a href="../../admin/c-data-governance/gdpr-labels.md#concept_F4061E29353446B5B0A7CF248D54E6F2" format="dita" scope="local"> DSGVO-Beschriftungen für Analytics-Variablen</a> </li> 
      <li id="li_CEEF2106E37845A49E0EA1225D5CFF14">Listenelement </li> 
      <li id="li_0B79CEBD074A4C68923EE9C9766D4B9D"><a href="../../admin/c-data-governance/gdpr-analytics-ids.md#concept_1BC4CA94B559481F8B08776DA100B23E" format="dita" scope="local"> Best Practices für Beschriftungen</a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img  src="assets/step4_icon.png" id="image_FE2039B8345248BCA303B44C10B68EA1" placement="break" /> Weisen Sie jeder Variablen in einer Report Suite Beschriftungen zu Identität, Vertraulichkeit und Data Governance zu. </p> <p>Hinweis: Beachten Sie, dass die Beschriftung bei jeder Erstellung einer neuen Report Suite überprüft werden muss und immer dann, wenn für eine vorhandene Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein. </p> </td> 
   <td colname="col3"> <p> Follow the instructions in <a href="../../admin/c-data-governance/gdpr-setup-reportsuite.md#concept_FAA948AD8CEA4BC38CB482EAF3648731" format="dita" scope="local"> Label Report Suite Data</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step5_icon.png" id="image_E9BEF83BF30F4528A030F23F71E5E5D8" /> Stellen Sie eine Verbindung zur Adobe-DSGVO-API her und reichen Sie Löschanfragen ein. </p> </td> 
   <td colname="col3"> <p>Als Adobe Analytics-Kunde können Sie einzelne DSGVO-Anfragen für Zugriff oder Löschung von Kundendaten durch einen Aufruf der <a href="https://www.adobe.io/apis/cloudplatform/gdpr.html" format="html" scope="external">DSGVO-API von Adobe Experience Cloud</a> einreichen. </p> <p>Sie können in den Anfragen neben den entsprechenden Namespace-IDs (Datenquellen-IDs) beliebige Analytics-IDs hinzufügen (siehe <a href="../../admin/c-data-governance/gdpr-analytics-ids.md#concept_1BC4CA94B559481F8B08776DA100B23E" format="dita" scope="local">Best Practices für Beschriftungen</a>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p><img placement="break"  src="assets/step6_icon.png" id="image_5CF03706FECD4F8BBAE0D0C19F98B8BB" /> Zeigen Sie die DSGVO-Einstellungen Ihrer Report Suite an und verwalten Sie sie. </p> </td> 
   <td colname="col3"> <p>Follow the instructions in <a href="../../admin/c-data-governance/gdpr-view-settings.md#concept_7759BAD6F3174901A94116D189AEF80E" format="dita" scope="local"> View Report Suite's Data Governance Settings</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>
