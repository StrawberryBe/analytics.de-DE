---
description: Sie können das Dynamic Tag Management mit einer oder mehreren der verfügbaren Hosting-Optionen bereitstellen.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;hosting;hosting options;akamai;self hosting;self-hosting;ftp delivery;ftp hosting;library download
title: Hosting-Optionen konfigurieren
topic: Developer and implementation
uuid: 04268f2d-e76f-4fe4-8fcc-f0db3a016502
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Hosting-Optionen konfigurieren

Sie können das [!UICONTROL Dynamic Tag Management] mit einer oder mehreren der verfügbaren Hosting-Optionen bereitstellen.

[!UICONTROL Das Dynamic Tag Management bietet verschiedene Möglichkeiten zum Hosten der erforderlichen JavaScript-Dateien.]

Detaillierte Informationen über das Hosten finden Sie im Abschnitt zu [Optionen für Einbettungscode und Hosting](https://marketing.adobe.com/resources/help/de_DE/dtm/deployment.html) in der Produktdokumentation für das [!UICONTROL Dynamic Tag Management].

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
   <td colname="col2"> <p> Die am einfachsten zu implementierende Hosting-Option. </p> <p>Global verteiltes Auslieferungsnetzwerk. </p> <p>Ergänzt zusätzliche Drittanbieterinfrastruktur-Abhängigkeiten (DNS-Suche, Akamai-Verfügbarkeit). </p> <p>Detaillierte Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/de_DE/dtm/akamai.html">Akamai</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_EF148EF091A645B3962B084963B3C0B0"> 
     <li id="li_7ECE0C331EEE4907A563D581DF1DFEFE">Das Dynamic Tag Management erzeugt benutzerdefinierte JavaScript-Bibliotheken. </li> 
     <li id="li_8E2C858290EF4665B2F45ACAFA121CB3">Das Dynamic Tag Management exportiert die benutzerdefinierten JavaScript-Bibliotheken zu Akamai. </li> 
     <li id="li_CE88B10B6E844A56BBB8C575A9363BA9">Die Zielwebsite verweist direkt auf Seitenebene auf die von Akamai gehosteten Dynamic Tag Management-Bibliotheken. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Self-Hosting: FTP-Auslieferung </td> 
   <td colname="col2"> <p>Ein <span class="term">Push</span>-Ansatz, bei dem das Dynamic Tag Management benutzerdefinierte JavaScript-Bibliotheken direkt per FTP-Protokoll zum Web-Content-Server-Host exportiert. </p> <p>Für dieses Verfahren sind ein FTP-Server und Anmeldedaten für den Web-Content-Server erforderlich, um Änderungen an den benutzerdefinierten Dynamic Tag Management-Bibliotheken veröffentlichen zu können. </p> <p>Detaillierte Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/de_DE/dtm/deployment_ftp.html">FTP</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_60348F9C991D4F2B9457006B0F98C834"> 
     <li id="li_24A141C3C7074BF9897C022A22CAE78C">Das Dynamic Tag Management erzeugt benutzerdefinierte JavaScript-Bibliotheken. </li> 
     <li id="li_E1E0843060F7447E853EA416A0B033BE">Das Dynamic Tag Management exportiert die benutzerdefinierten JavaScript-Bibliotheken per FTP an den Host-Server. </li> 
     <li id="li_EAF5D2ABD03B4911A0CFA464AD8791CE">Die Zielwebsite verweist lokal auf die benutzerdefinierten Dynamic Tag Management-Bibliotheken. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Self-Hosting: Bibliotheksdownload </td> 
   <td colname="col2"> <p>Ein <span class="term">Pull</span>-Ansatz, bei dem die Applikation benutzerspezifische JavaScript-Bibliotheken exportiert<!-- to Amazon S3-->. Dort kann über einen gehosteten Server-seitigen Vorgang auf die Bibliotheken zugegriffen werden. </p> <p>Darüber hinaus sind die Bibliotheken per Webdownload direkt über die Benutzeroberfläche für das Dynamic Tag Management verfügbar. </p> <p>Bei diesem Verfahren ist entweder ein manuelles Abrufen und Veröffentlichen der Dynamic Tag Management-Bibliotheken oder die Erstellung eines automatischen Prozesses erforderlich, der die Bibliotheken von Akamai auf dem Web-Content-Server abruft. </p> <p>Bei diesem Ansatz dauert die Einrichtung am längsten; allerdings handelt es sich auch um die sicherste und flexibelste Option. </p> <p>Um zu überprüfen, ob die aktuelle Version Ihrer Bibliotheksdatei referenziert wird, verwenden Sie in der Web-Konsole den Befehl. </p> <p>Detaillierte Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/de_DE/dtm/deployment_download.html">Bibliotheksdownload</a> in der Produktdokumentation für das Dynamic Tag Management. </p> </td> 
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
