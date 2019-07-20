---
description: Beschreibungen der Felder und Optionen in den Bibliotheksverwaltungseinstellungen des Dynamic Tag Managements.
keywords: Bibliotheksverwaltung; page code; load library at; verwaltet von adobe; benutzerdefiniert; Code gehostet; s_ code gehostet
seo-description: Beschreibungen der Felder und Optionen in den Bibliotheksverwaltungseinstellungen des Dynamic Tag Managements.
seo-title: Bibliotheksverwaltung
solution: Marketing Cloud, dynamisches Tag-Management
title: Bibliotheksverwaltung
uuid: 4 cfa 47 f 9-ae 98-4 feb-a 58 d-a 3 a 6 e 45 f 8 d 5 b
translation-type: tm+mt
source-git-commit: 3489f00bd7dddefda0420fc361056416f6f10d3f

---


# Bibliotheksverwaltung

Beschreibungen der Felder und Optionen in den Bibliotheksverwaltungseinstellungen des Dynamic Tag Managements.

**[!UICONTROL *`Property`*]** &gt; ![](assets/settings_gear.png)**[!UICONTROL Tool bearbeiten]** &gt; **[!UICONTROL Bibliotheksverwaltung]**

>[!NOTE]
>
>Wenn in einer einzelnen Webeigenschaft mehr als ein Adobe Analytics-Tool verwendet wird, muss jedes Tool über einen eindeutigen Trackervariablennamen verfügen. Duplizierte Objektvariablennamen der Adobe Analytics-Tools in einer einzigen Webeigenschaft führen zu Konflikten.

<table id="table_2758C770C91B4025AD74009B360D71F7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Seiten-Code bereits vorhanden </p> </td> 
   <td colname="col2"> <p> Verhindert, dass durch das Dynamic Tag Management <span class="keyword">Adobe Analytics</span>-Seiten-Code installiert wird, wenn der Code bereits auf Ihrer Website vorhanden ist. </p> <p>Mit dieser Funktion können Sie das Dynamic Tag Management zum Hinzufügen Ihrer vorhandenen Implementierung nutzen, um nicht von Grund auf neu beginnen zu müssen. Stellen Sie sicher, dass der Tracker-Variablenname korrekt festgelegt ist, wenn Sie dieses Kontrollkästchen aktivieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bibliothek am &lt;<span class="term"> Seitenanfang</span> oder <span class="term"> Seite unten</span>&gt; </p> </td> 
   <td colname="col2"> <p>Gibt an, an welcher Position und wann der Seiten-Code geladen wird. Unabhängig von Ihrer Auswahl müssen alle Regeln, die das Analytics-Tool verwenden, über die gleiche Einstellung verfügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwaltet von Adobe (empfohlen) </p> </td> 
   <td colname="col2"> <p>Aktivieren Sie das Dynamic Tag Management für die Verwaltung Ihrer Bibliothek. </p> <p>Wenn Sie diese Option auswählen, wird die folgende Option verfügbar: </p> <p> <b>Bibliotheksversion:</b> Wählen Sie die neueste Version im Menü „<span class="wintitle">Bibliotheksversion</span>“ aus. Das Dynamic Tag Management benachrichtigt Sie, wenn neue Versionen verfügbar werden. Bei Bedarf können Sie eine frühere Version wiederherstellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Benutzerspezifisch </p> </td> 
   <td colname="col2"> <p>Sie können den Bibliothekscode konfigurieren. </p> <p>Wenn Sie diese Option auswählen, werden folgende Optionen verfügbar: </p> <p> <b>Report Suites mithilfe eines benutzerspezifischen Codes unten festlegen:</b> Ist dieses Kontrollkästchen aktiviert, sucht das Dynamic Tag Management in Ihrem benutzerdefinierten Code nach einer Variablen namens <span class="varname"> s_account</span>. Diese Variable sollte eine kommagetrennte Liste der Report Suites enthalten, an die Daten gesendet werden sollen. </p> <p> <b>Code gehostet:</b> Wählen Sie eine Option für das Hosting von <span class="filepath">s_code</span> aus: </p> 
    <ul id="ul_FC395283365A4BBAA8A5FE5871D16EC6"> 
     <li id="li_36D733C533CE40F1868309130551D4DE"> <b>In DTM</b>: Sie können den <span class="filepath">s_code</span> im Dynamic Tag Management hosten. Klicken Sie auf <span class="uicontrol">Code bearbeiten</span>, um die Datei direkt zu kopieren und in den Editor einzufügen. </li> 
     <li id="li_A64734C66D254079A5E16DC8DBEDA3F6"> <b>URL</b>: Wenn Sie eine leistungsstarke <span class="filepath">s_code</span>-Datei haben und diese nach Bedarf aktualisieren, können Sie die URL zu dieser Datei hier angeben. Das Dynamic Tag Management nutzt diese <span class="filepath">s_code</span>-Datei dann einfach für die Implementierung von <span class="keyword">Adobe Analytics</span>. </li> 
    </ul> <p> <b>Editor öffnen: </b>Ermöglicht den <a href="../../../implement/c-implement-with-dtm/c-aa-tool/t-appmeasurement-code.md#task_068D72664B2743359A64ADB8692D3658" format="dita" scope="local"> grundlegenden appmeasurement-Code</a>. This code is populated automatically when using the automatic configuration method described in <a href="../../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8" format="dita" scope="local"> Adobe Analytics Settings</a>. </p> <p> <b>Trackervariablenname: </b>Wenn Sie zwei Instanzen von <span class="keyword"> Adobe Analytics</span> parallel ausführen möchten (eine im dynamischen Tag-Management und eine native Instanz), können Sie <span class="term"> das</span> Hauptobjekt umbenennen. Durch die Umbenennung des Objektnamens wird möglichen Konflikten vorgebeugt. </p> </td> 
  </tr> 
 </tbody> 
</table>

