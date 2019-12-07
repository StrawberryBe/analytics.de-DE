---
description: Setzen Sie mit den Erfahrungen von Erstkonsumenten Adobe Analytics-Implementierungen um.
keywords: Getting Started
subtopic: Analysis Workspace
title: Vereinfachte Implementierung
topic: Reports and analytics
uuid: 6fad2c1f-476c-4985-90df-7c222e751ddc
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Vereinfachte Implementierung

Setzen Sie mit den Erfahrungen von Erstkonsumenten Adobe Analytics-Implementierungen um.

<!-- 

<p>https://activation.adobedtm.com/index.php?redirected=1 </p>

 -->

Als neuer Benutzer können Sie Ihre erste [!DNL Analytics] Report Suite (Daten-repository) mit diesem Einrichtungs-Leitfaden *`Getting Started with Adobe Analytics`* erstellen. Anschließend können Sie [!DNL Analytics]-Code mit [!DNL Dynamic Tag Management] bereitstellen.

[!DNL Dynamic Tag Management] ermöglicht Ihnen, Ihre Adobe Analytics-Implementierung zu verwalten, ohne jedes Mal Änderungen an Ihrer Site vorzunehmen. Wenn Sie eine mobile Anwendung implementieren, können Sie das SDK erhalten, das Sie benötigen, um wertvolle Daten aus Ihren Anwendungen zu erfassen.

Diese Vorgehensweise ermöglicht Ihnen Folgendes:

* Schnelles Erstellen Ihrer ersten [Report Suite](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html).
* Bereitstellen [!DNL Analytics] und [Identitätsdienst](https://marketing.adobe.com/resources/help/en_US/mcvid/).

* Ausführen von Berichten für grundlegende Daten auf Seitenebene.

> [!NOTE] Bevor Sie beginnen, überprüfen Sie, ob Analytics in der Adobe Experience Cloud[ (Lösungsbereitstellungsprozess) ](https://marketing.adobe.com/resources/help/en_US/mcloud/core_services.html)aktiviert ist. Wenn Sie eine E-Mail mit einer Einladung erhalten haben, sich bei Analytics im Enterprise Dashboard anzumelden, haben Sie diese Voraussetzung erfüllt.

**So führen Sie die vereinfachte Implementierung aus**

1. Log in to the [!DNL Adobe Experience Cloud] ( [experiencecloud.adobe.com](https://experiencecloud.adobe.com)).

   Beim Zugriff auf [!DNL Analytics] stellt das System fest, ob Sie eine Report Suite besitzen. Wenn das nicht der Fall ist, wird die Seite [!UICONTROL Erste Schritte – Adobe Analytics] angezeigt.

   ![](assets/analytics-implementation-rs-wizard.png)

   Alternativ können Sie diese Einrichtung in [!DNL Analytics] ausführen, indem Sie auf **[!UICONTROL Hilfe]** &gt; **[!UICONTROL Willkommen bei Adobe Analytics]** klicken.

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
       <td colname="col2"> <p>(Empfohlen) Ein JavaScript-Array, das zum Speichern von Informationen verwendet wird. Wenn Sie die automatische Einrichtung mithilfe des Dynamic Tag Managements durchführen, verwenden Sie eine Datenschicht. </p> <p>Einen Blog zu Datenschichten finden Sie unter <a href="https://blogs.adobe.com/digitalmarketing/analytics/data-layers-buzzword-best-practice/">Data Layers: From Buzzword to Best Practice</a>. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Daten-Repository (Report Suite) </p> </td> 
       <td colname="col2"> <p> Eine <a href="https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html">Report Suite</a> ist ein eigenständiger Datensatz, der typischerweise einem einzelnen Objekt (Site oder Anwendung) oder einer Marke entspricht. Jede Report Suite verfügt über einen eigenen Satz von Berichten und Metriken. </p> </td> 
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

1. Klicken Sie auf **[!UICONTROL Weiter]**.

   Das System erstellt eine Report Suite.

1. Um die Implementierung zu starten, klicken Sie auf **[!UICONTROL Weiter]** und dann auf eine der folgenden Optionen:

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
       <td colname="col2"> <p> Startet das <span class="keyword">Dynamic Tag Management</span>, wo Sie sich anmelden und Analytics bereitstellen können. Dieser Prozess implementiert automatisch die <span class="filepath">AppMeasurement.js</span>-Datei und den Identitätsdienst (<span class="filepath"> VisitorAPI.js</span>). </p> <p> <p>Wichtig: In einer neuen Browserregisterkarte wird eine Hilfeseite angezeigt, die Sie durch die <span class="keyword">Adobe Analytics</span>-Implementierung mithilfe des Dynamic Tag Managements führt. </p> </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>Download </p> </td> 
       <td colname="col2"> <p> Laden Sie die Installationsdatei mit dem Namen <span class="filepath">INSTALL-ME &lt;Report Suite-Name&gt;.js</span> herunter. Diese Option ist für erfahrene Benutzer geeignet, die über Kenntnisse auf dem Gebiet der <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html">JavaScript-Implementierung</a> verfügen. </p> <p> <p>Wichtig: Durch Herunterladen des Codes wird <span class="keyword">Analytics</span> noch nicht bereitgestellt. Dies ist eine manuelle Implementierung, die Sie auf den Seiten Ihrer Website oder mithilfe der Beratungsdienstleistungen von Adobe durchführen. </p> </p> </td> 
      </tr> 
     </tbody> 
    </table>

1. Einen Bericht ausführen.

   Nach der Bereitstellung des Analytics-Werkzeugs können Sie einen Bericht in Reports &amp; Analytics ausführen, um sicherzugehen, dass Daten auf Ihre Site gelangen. (Siehe   [Anmeldung und Navigation](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/analytics-navigation.html), um die Benutzeroberfläche von Analytics kennenzulernen.)

   Beispielsweise können Sie mit **[!UICONTROL Sitemetriken]** &gt; Echtzeit **[!UICONTROL sofort Daten sehen]**.

   >[!NOTE]
   >
   >Hinweis: Der [!UICONTROL Echtzeit]bericht muss konfiguriert werden, bevor er ausgeführt werden kann. Siehe [Konfiguration von Echtzeitberichten](https://marketing.adobe.com/resources/help/en_US/reference/t_realtime_admin.html).

**Beispiel für einen Echtzeitbericht**

![](assets/real-time-report.png)
