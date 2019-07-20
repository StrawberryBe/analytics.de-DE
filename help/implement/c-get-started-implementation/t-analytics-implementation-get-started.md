---
description: Setzen Sie mit den Erfahrungen von Erstkonsumenten Adobe Analytics-Implementierungen um.
keywords: Erste Schritte
seo-description: Setzen Sie mit den Erfahrungen von Erstkonsumenten Adobe Analytics-Implementierungen um.
seo-title: Vereinfachte Implementierung
solution: Analytics
subtopic: Analysis Workspace
title: Vereinfachte Implementierung
topic: Reports and Analytics
uuid: 6 path 2 c 1 f -476 c -4985-90 df -7 c 222 e 751 ddc
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Vereinfachte Implementierung

Setzen Sie mit den Erfahrungen von Erstkonsumenten Adobe Analytics-Implementierungen um.

<!-- 

<p>https://activation.adobedtm.com/index.php?redirected=1 </p>

 -->

New users can quickly create your first [!DNL Analytics] report suite (data repository) using this *`Getting Started with Adobe Analytics`* setup modal. Then, you can deploy [!DNL Analytics] code using [!DNL Dynamic Tag Management].

[!DNL Dynamic Tag Management] ermöglicht Ihnen, Ihre Adobe Analytics-Implementierung zu verwalten, ohne jedes Mal Änderungen an Ihrer Site vorzunehmen. Wenn Sie eine mobile Anwendung implementieren, können Sie das SDK erhalten, das Sie benötigen, um wertvolle Daten aus Ihren Anwendungen zu erfassen.

Diese Vorgehensweise ermöglicht Ihnen Folgendes:

* Schnelles Erstellen Ihrer ersten   [Report Suite](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html).
* Deploy [!DNL Analytics] and the [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/).

* Ausführen von Berichten für grundlegende Daten auf Seitenebene.

>[!NOTE]
>
>Before you begin, verify that Analytics is [enabled in the Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/core_services.html) (the solution provisioning process). Wenn Sie eine E-Mail mit einer Einladung erhalten haben, sich bei Analytics im Enterprise Dashboard anzumelden, haben Sie diese Voraussetzung erfüllt.

**So führen Sie die vereinfachte Implementierung aus**

1. Log in to the [!DNL Adobe Experience Cloud] ( [experiencecloud.adobe.com](https://experiencecloud.adobe.com)).

   Beim Zugriff auf [!DNL Analytics] stellt das System fest, ob Sie eine Report Suite besitzen. Wenn das nicht der Fall ist, wird die Seite [!UICONTROL Erste Schritte – Adobe Analytics] angezeigt.

   ![](assets/analytics-implementation-rs-wizard.png)

   Alternatively, you can run this setup in [!DNL Analytics] by clicking **[!UICONTROL Help]** &gt; **[!UICONTROL Welcome to Adobe Analytics]**.

1. Geben Sie die folgenden grundlegenden Informationen über Ihr Unternehmen an:

   <table id="table_1741878A1B284CB78D297D531DC703D6"> 
     <thead> 
      <tr> 
       <th colname="col1" class="entry"> Element </th> 
       <th colname="col2" class="entry"> Beschreibung </th> 
      </tr> 
     </thead>
     <tbody> 
      <tr> 
       <td colname="col1"> <p>Eigenschaftstyp </p> </td> 
       <td colname="col2"> <p>Ist Ihre Implementierung für das Internet, mobile Geräte oder beides konzipiert? </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Branchen </p> </td> 
       <td colname="col2"> <p>Geben Sie an, woher die Einkünfte Ihres Unternehmens stammen (Produkte, Kundendienst, Leads, Markenbewusstsein und Anzeigen). </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Datenschicht </p> </td> 
       <td colname="col2"> <p>(Empfohlen) Ein JavaScript-Array, das zum Speichern von Informationen verwendet wird. Wenn Sie die automatische Einrichtung mithilfe des Dynamic Tag Managements durchführen, verwenden Sie eine Datenschicht. </p> <p>For a blog on data layers, see <a href="https://blogs.adobe.com/digitalmarketing/analytics/data-layers-buzzword-best-practice/" format="http" scope="external"> Data Layer: From Buzzword to Best Practice</a>. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Daten-Repository (Report Suite) </p> </td> 
       <td colname="col2"> <p> Eine <a href="https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html" format="html" scope="external">Report Suite</a> ist ein eigenständiger Datensatz, der typischerweise einem einzelnen Objekt (Site oder Anwendung) oder einer Marke entspricht. Jede Report Suite verfügt über einen eigenen Satz von Berichten und Metriken. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Zeitzone </p> </td> 
       <td colname="col2"> <p>Ihre lokale Zeitzone (wird automatisch erkannt). </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Geschätzte Seitenansichten </p> </td> 
       <td colname="col2"> <p>Die geschätzte Anzahl von Seiten, die auf Ihrer Site pro Tag angesehen werden. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Basiswährung </p> </td> 
       <td colname="col2"> <p>Die Geschäftswährung Ihres Unternehmens. </p> </td> 
      </tr> 
     </tbody> 
    </table>

1. Click **[!UICONTROL Next]**.

   Das System erstellt eine Report Suite.

1. To begin deployment, click **[!UICONTROL Next]**, then click one of the following options:

   <table id="table_71C7F7B9677346CD8D5130519D32464B"> 
     <thead> 
      <tr> 
       <th colname="col1" class="entry"> Element </th> 
       <th colname="col2" class="entry"> Beschreibung </th> 
      </tr> 
     </thead>
     <tbody> 
      <tr> 
       <td colname="col1"> <p>Bereitstellen </p> </td> 
       <td colname="col2"> <p> Startet das <span class="keyword">Dynamic Tag Management</span>, wo Sie sich anmelden und Analytics bereitstellen können. This process automatically implements the <span class="filepath"> AppMeasurement.js</span> file and the Identity Service (<span class="filepath"> VisitorAPI.js</span>). </p> <p> <p>Wichtig: In einer neuen Browserregisterkarte wird eine Hilfeseite angezeigt, die Sie durch die <span class="keyword">Adobe Analytics</span>-Implementierung mithilfe des Dynamic Tag Managements führt. </p> </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Download </p> </td> 
       <td colname="col2"> <p> Laden Sie die Installationsdatei mit dem Namen <span class="filepath">INSTALL-ME &lt;Report Suite-Name&gt;.js</span> herunter. Diese Option ist für erfahrene Benutzer geeignet, die über Kenntnisse auf dem Gebiet der <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html" format="html" scope="external">JavaScript-Implementierung</a> verfügen. </p> <p> <p>Wichtig: Durch Herunterladen des Codes wird <span class="keyword">Analytics</span> noch nicht bereitgestellt. Dies ist eine manuelle Implementierung, die Sie auf den Seiten Ihrer Website oder mithilfe der Beratungsdienstleistungen von Adobe durchführen. </p> </p> </td> 
      </tr> 
     </tbody> 
    </table>

1. Einen Bericht ausführen.

   Nach der Bereitstellung des Analytics-Werkzeugs können Sie einen Bericht in Reports &amp; Analytics ausführen, um sicherzugehen, dass Daten auf Ihre Site gelangen. (Siehe   [Anmeldung und Navigation](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/analytics-navigation.html), um die Benutzeroberfläche von Analytics kennenzulernen.)

   For example, a **[!UICONTROL Site Metrics]** &gt; **[!UICONTROL Real-Time]** lets you see immediate data.

   >[!NOTE]
   >
   >The [!UICONTROL Real-Time] report requires some configuration prior to running. Siehe [Konfiguration von Echtzeitberichten](https://marketing.adobe.com/resources/help/en_US/reference/t_realtime_admin.html).

**Beispiel für einen Echtzeitbericht**

![](assets/real-time-report.png)
