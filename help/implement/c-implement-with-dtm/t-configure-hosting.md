---
description: Sie können das Dynamic Tag Management mit einer oder mehreren der verfügbaren Hosting-Optionen bereitstellen.
keywords: Analytics-Implementierung; Implementierungsmethode; dynamisches Tag-Management; dtm; Hosting; Hosting-Optionen; akamai; self hosting; self-hosting; ftp delivery; ftp hosting; Bibliotheksdownload
seo-description: Sie können das Dynamic Tag Management mit einer oder mehreren der verfügbaren Hosting-Optionen bereitstellen.
seo-title: Hosting-Optionen konfigurieren
solution: Analytics
title: Hosting-Optionen konfigurieren
topic: Entwickler und Implementierung
uuid: 04268 f 2 d-e 76 f -4 fe 4-8 fcc-f 0 db 3 a 165002
translation-type: tm+mt
source-git-commit: 6250335d05c8e7799802fce26192896a7a6598fe

---


# Hosting-Optionen konfigurieren

You can deploy [!UICONTROL Dynamic Tag Management] using one or more of the available hosting options.

[!UICONTROL Das Dynamic Tag Management bietet verschiedene Möglichkeiten zum Hosten der erforderlichen JavaScript-Dateien.]

Detaillierte Informationen über das Hosten finden Sie im Abschnitt zu [Optionen für Einbettungscode und Hosting](https://marketing.adobe.com/resources/help/en_US/dtm/deployment.html) in der Produktdokumentation für das Dynamic Tag Management.

Wählen Sie auf der Registerkarte „Einbettung“ eine Hosting-Option.

<table id="table_229298207DB64838B6F2477DFFAE073F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Hosting-Option </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
   <th colname="col3" class="entry"> Implementierung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Akamai </p> </td> 
   <td colname="col2"> <p> Die am einfachsten zu implementierende Hosting-Option. </p> <p>Global verteiltes Auslieferungsnetzwerk. </p> <p>Ergänzt zusätzliche Drittanbieterinfrastruktur-Abhängigkeiten (DNS-Suche, Akamai-Verfügbarkeit). </p> <p>Detaillierte Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/dtm/akamai.html" format="html" scope="external">Akamai</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_EF148EF091A645B3962B084963B3C0B0"> 
     <li id="li_7ECE0C331EEE4907A563D581DF1DFEFE">Das Dynamic Tag Management erzeugt benutzerdefinierte JavaScript-Bibliotheken. </li> 
     <li id="li_8E2C858290EF4665B2F45ACAFA121CB3">Das Dynamic Tag Management exportiert die benutzerdefinierten JavaScript-Bibliotheken zu Akamai. </li> 
     <li id="li_CE88B10B6E844A56BBB8C575A9363BA9">Die Zielwebsite verweist direkt auf Seitenebene auf die von Akamai gehosteten Dynamic Tag Management-Bibliotheken. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Self-Hosting: FTP-Auslieferung </td> 
   <td colname="col2"> <p>A <span class="term"> push</span> approach, whereby Dynamic Tag Management exports custom JavaScript libraries directly to the web content server host via the FTP protocol. </p> <p>Für dieses Verfahren sind ein FTP-Server und Anmeldedaten für den Web-Content-Server erforderlich, um Änderungen an den benutzerdefinierten Dynamic Tag Management-Bibliotheken veröffentlichen zu können. </p> <p>Detaillierte Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/dtm/deployment_ftp.html" format="html" scope="external">FTP</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_60348F9C991D4F2B9457006B0F98C834"> 
     <li id="li_24A141C3C7074BF9897C022A22CAE78C">Das Dynamic Tag Management erzeugt benutzerdefinierte JavaScript-Bibliotheken. </li> 
     <li id="li_E1E0843060F7447E853EA416A0B033BE">Das Dynamic Tag Management exportiert die benutzerdefinierten JavaScript-Bibliotheken per FTP an den Host-Server. </li> 
     <li id="li_EAF5D2ABD03B4911A0CFA464AD8791CE">Die Zielwebsite verweist lokal auf die benutzerdefinierten Dynamic Tag Management-Bibliotheken. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Self-Hosting: Bibliotheksdownload </td> 
   <td colname="col2"> <p><span class="term"> Ein Pull</span> -Ansatz, bei dem die Anwendung benutzerdefinierte javascript-Bibliotheken
 <!-- to Amazon S3-->exportiert. Dort kann über einen gehosteten serverseitigen Vorgang auf die Bibliotheken zugegriffen werden. </p> <p>Darüber hinaus sind die Bibliotheken per Webdownload direkt über die Benutzeroberfläche für das Dynamic Tag Management verfügbar. </p> <p>Bei diesem Verfahren ist entweder ein manuelles Abrufen und Veröffentlichen der Dynamic Tag Management-Bibliotheken oder die Erstellung eines automatischen Prozesses erforderlich, der die Bibliotheken von Akamai auf dem Web-Content-Server abruft. </p> <p>Bei diesem Ansatz dauert die Einrichtung am längsten; allerdings handelt es sich auch um die sicherste und flexibelste Option. </p> <p>Um zu überprüfen, ob die aktuelle Version Ihrer Bibliotheksdatei referenziert wird, verwenden Sie in der Web-Konsole den Befehl </p> <p>Detaillierte Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/dtm/deployment_download.html" format="html" scope="external">Bibliotheksdownload</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_F40B721306FE473496BD657262DFD585"> 
     <li id="li_4EA4D6B555CE4E9CA476C7550C18C061">Das Dynamic Tag Management erzeugt benutzerdefinierte JavaScript-Bibliotheken. </li> 
     <li id="li_BA40EBD7AD1546F29D8A209034D06477">Das Dynamic Tag Management exportiert die benutzerdefinierten JavaScript-Bibliotheken zu Akamai. </li> 
     <li id="li_E107E69E386A40F3B067F9991C2979AF">Die benutzerdefinierten Dynamic Tag Management-Bibliotheken werden manuell oder programmgesteuert auf den Web-Content-Server verschoben. </li> 
     <li id="li_0809038453B544168A20CE09D7E5AC59">Die Zielwebsite verweist lokal auf die benutzerdefinierten Dynamic Tag Management-Bibliotheken. </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

Sie können mehrere Hosting-Optionen nutzen. Beispielsweise können Sie Ihre Stage-Dateien mit Akamai, Ihre Produktions-Website aber selbst hosten. Beachten Sie, dass jeder Hosting-Typ über einen eigenen Einbettungscode verfügt und nur ein Einbettungscode einer Seite hinzugefügt werden kann.
