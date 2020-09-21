---
description: Tipps und Best Practices für neue Benutzer von Virtual Report Suites.
keywords: Virtual Report Suite
title: Häufig gestellte Fragen zu VRS
topic: Reports and analytics
uuid: 91225743-765a-4145-9ce5-4268e80ea7e8
translation-type: ht
source-git-commit: 444a2b93a39cad0d2f62a4bf8d889b71ba726092
workflow-type: ht
source-wordcount: '898'
ht-degree: 100%

---


# Häufig gestellte Fragen zu VRS

Tipps und Best Practices für neue Benutzer von Virtual Report Suites.

<table id="table_4D9DE70984674B65AD7D40E3D1479CD2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Sollte ich meine Implementierung von mehreren Report Suites auf eine einzige globale Report Suite umstellen und dann Virtual Report Suites verwenden, um verschiedene Datensegmente für meine Benutzer verfügbar zu machen?</b> </td> 
   <td colname="col2"> <p>Eventuell. Es gibt bestimmte Umstände, unter denen Sie <b>weiterhin mit einzelnen Report Suites arbeiten sollten</b>: </p> 
    <ul> 
     <li>Wenn Sie Variablen/Dimensionen mit einer großen Anzahl individueller Werte haben, kann die Konsolidierung in einer einzigen Report Suite dazu führen, dass in dieser globalen Suite die monatlichen Grenzen für individuelle Werte überschritten werden, was eine Kürzung zur Folge hat („Geringer Datenverkehr“ als Zeilenelement in Berichten). </li> 
     <li>Wenn Sie für einzelne Segmente Ihrer Daten Berichte mit Echtzeit- oder aktuellen Daten benötigen (z. B. Marken, Geschäftsbereiche usw.) </li> 
     <li>Wenn Ihre verschiedenen Report Suites jeweils spezifische Tracking-Anforderungen haben (d. h., wenn diese Adobe Analytics-Variablen und -Ereignisse sehr unterschiedlich verwenden), müssen Sie bedenken, dass Sie mit einer konsolidierten globalen Report Suite keine zusätzlichen Variablen oder Ereignisse für das Tracking benutzen können. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Welche Einstellungen erben Virtual Report Suites von der übergeordneten Report Suite? </b> </td> 
   <td colname="col2"> <p>Eine Virtual Report Suite (VRS) erbt die meisten Service-Levels der übergeordneten Report Suite, wie die eVar-Einstellungen, Verarbeitungsregeln, Classifications usw. </p> <p>Die folgenden Einstellungen werden <b>NICHT</b> vererbt: </p> 
    <ul> 
     <li>Report Suite-ID </li> 
     <li>Name der Report Suite </li> 
     <li>Berechtigungsgruppen (Virtual Report Suites können eigenen Berechtigungsgruppen zugewiesen werden.) </li> 
    </ul> <p>Hinweis: Dies betrifft nicht die meisten von Benutzern erstellten Entitäten, wie Lesezeichen, Dashboards, terminierte Berichte usw.Diese Elemente werden nicht von der übergeordneten Report Suite geerbt und können spezifisch für die VRS erstellt und verwendet werden (weitere Einzelheiten liefert die Antwort auf die nächste Frage). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Wie unterscheidet sich das Arbeiten mit einer Virtual Report Suite in der Analytics-Benutzeroberfläche von dem mit einer Basis-Report Suite?</b> </td> 
   <td colname="col2"> <p>Nachdem sie erstellt wurde, wird eine Virtual Report Suite auf der Benutzeroberfläche genauso behandelt wie eine Basis-Report Suite und unterstützt die meisten erweiterten Funktionen. Beispiel: </p> 
    <ul> 
     <li>Virtual Report Suites werden in der Report Suite-Auswahl angezeigt und können, genau wie Basis-Report Suites, einzeln ausgewählt werden. </li> 
     <li>DL-Berichte, Lesezeichen, Dashboards, Zielgruppen, Warnhinweise, Segmente, berechnete Metriken usw. können für eine Virtual Report Suite erstellt werden und verhalten sich unabhängig von der übergeordneten Report Suite. </li> 
     <li>Virtual Report Suites können, genau wie jede andere Report Suite, einzeln zu Berechtigungsgruppen hinzugefügt werden. </li> 
     <li>Beim Ausführen von Berichten für VRS können weiterhin Segmente angewendet werden. Diese werden automatisch mit den Segmenten der Virtual Report Suite gestapelt, wenn die Berichtdaten abgerufen werden. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Wie werden Virtual Report Suites in der Admin Console und der Admin-API behandelt? Kann ich Features wie für Basis-Report Suites speichern? </b> </td> 
   <td colname="col2"> <p>Nein, Virtual Report Suites werden <b>für die meisten Admin-Features nicht unterstützt</b>. Wie oben bereits erwähnt, erbt eine VRS die meisten Service-Levels und Features von der übergeordneten Report Suite (z. B. eVar-Einstellungen, Verarbeitungsregeln, Classifications usw.). Daher können diese geerbten Einstellungen einer VRS nur geändert werden, indem die übergeordnete Report Suite geändert wird. </p> <p>Demzufolge werden Virtual Report Suites auf der Benutzeroberfläche <b>nur hier</b> angezeigt: </p> 
    <ul> 
     <li>im Virtual Report Suite Manager, in dem Sie VRS erstellen und bearbeiten. <p>( <span class="ignoretag"> <span class="uicontrol"> Analytics</span> &gt; <span class="uicontrol">Komponenten</span> &gt; <span class="uicontrol">Virtual Report Suites </span> </span>) </p> </li> 
     <li id="li_E2B3F61A3013402697DCF6E0D32A62DC"> in der Benutzerverwaltung, in der Sie die benutzerspezifischen Berechtigungsgruppen bearbeiten So können VRS-Konten zu einer Berechtigungsgruppe hinzugefügt werden. Oder sie werden verwendet, um eine Gruppe zu erstellen, die ausschließlich Zugriff auf Virtual Report Suites hat (wenn der Administrator den Zugriff auf die übergeordnete Report Suite verweigern und nur den Zugriff auf bestimmte Segmente erlauben möchte). <p>( <span class="ignoretag"> <span class="uicontrol"> Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung </span> </span>) </p> </li> 
    </ul> <p>Hinweis: Wenn Sie die Web-Services-API verwenden und versuchen, Feature-Einstellungen für eine VRS zu speichern, führt dies zu einem Ausnahmefehler. Features können nur für die Basis-Report Suites festgelegt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> Ich habe „Bei Start neuen Besuch beginnen“ ausgewählt. Warum sehe ich nach wie vor wesentlich mehr Besuche als Starts?</b> </td> 
   <td colname="col2"> <p> Wenn „Bei Start neuen Besuch beginnen“ aktiviert wird, gilt der Timeout nach wie vor. Wenn ein Benutzer also die App zehn Minuten lang mit einminütigen Pausen zwischen den einzelnen Aktionen verwendet, beginnt bei jedem Besuch ein neuer Start und dann werden neun zusätzliche Besuche erstellt, wenn es beim aktuellen Besuch zu einem Timeout kommt. Damit Starts und Besuche bei der Verwendung der Option „Bei Start neuen Besuch beginnen“ so nahe beieinander sind wie möglich, sollten Sie einen längeren Timeout als den im SDK festgelegten Sitzungstimeout verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> Ich habe „Bei Start neuen Besuch beginnen“ festgelegt und einen längeren als den in meinem SDK festgelegten Timeout eingestellt. Warum habe ich immer noch wesentlich weniger Starts als Besuche?</b> </td> 
   <td colname="col2"> <p> Wenn der Timeout höher als der im SDK festgelegte Wert ist, versendet Ihre App höchstwahrscheinlich im Hintergrund Treffer und diese Treffer werden als neue Besuche aufgezeichnet. Dies können Sie prüfen, indem Sie die Dimension „Art des Treffers“ auf die übergeordnete Report Suite anwenden, um festzustellen, ob es Hintergrund-Treffer gibt. </p> <p> <p>Hinweis: Zwischen Hintergrund- und Vordergrundtreffern wird nur in Version 4.13.6 und späteren Versionen des SDK unterschieden. Wenn Sie eine frühere Version verwenden, werden alle Treffer als Vordergrundtreffer angezeigt. Wenn Sie die korrekte Version des SDK verwenden, sollten Sie die Einstellung „Starten neuer Besuche durch Hintergrundtreffer verhindern“ festlegen. </p> </p> <p> <p>Hinweis: Wenn Sie die veraltete Verarbeitung von Hintergrundtreffern in der Admin Console deaktiviert haben, werden diese nicht in der übergeordneten Report Suite, sondern in der Virtual Report Suite angezeigt. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Welche Version des SDK benötige ich, um Hintergrundtreffer zu verfolgen?</b> </td> 
   <td colname="col2"> <p> Sie müssen Version 4.13.6 oder eine spätere Version des SDK verwenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

