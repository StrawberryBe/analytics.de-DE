---
description: Wenn Sie die Arbeit mit dem Segmentaufbau in Ad Hoc Analysis gewohnt sind, erfahren Sie in diesen häufig gestellten Fragen, was mit bestehenden Segmenten und Ordnern passiert und welche Aktionen von Ihrer Seite erforderlich sind.
keywords: Segmentierung;Segmente
title: Übergangsleitfaden für Ad Hoc Analysis
feature: Segmentierung
uuid: d409d71a-f8d9-42a2-add2-37d426cd40d1
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 100%

---


# Übergangsleitfaden für Ad Hoc Analysis

Wenn Sie die Arbeit mit dem Segmentaufbau in Ad Hoc Analysis gewohnt sind, erfahren Sie in diesen häufig gestellten Fragen, was mit bestehenden Segmenten und Ordnern passiert und welche Aktionen von Ihrer Seite erforderlich sind.

## Funktionen   {#section_BD58629D1A9346BF879E229FA6BEC7A2}

* Alle Segmente gelten nun für alle Report Suites. Bisher waren Segmente spezifisch für eine Report Suite.
* Ad Hoc Analysis umfassen Aktualisierungen für den Segment Builder und ein vollständiges Update des Segment-Managers.
* Sie können Segmente nun zum Organisieren und Suchen taggen, anstatt Ordner zu verwenden. Bisher wurden Ordner in [!DNL Ad Hoc Analysis] verwendet, um Segmente zu organisieren.

## Was ist mit meinen vorhandenen Segmenten passiert? {#section_76CF47142D1A4FB6A0718AD9073049FE}

Ihre vorhandenen Segmente funktionieren weiterhin wie bisher. Alle Berichte, auf die diese Segmente angewendet wurden, funktionieren weiterhin korrekt.

Die meisten bisherigen vordefinierten und Suite-Segmente werden als Segmentvorlagen in den Segmentaufbau migriert. Segmentvorlagen werden verwendet, um schnell benutzerdefinierte Segmente mit gängigen Zielgruppen zu erstellen. Segmentvorlagen können nicht direkt auf einen Bericht angewendet werden, sie können aber problemlos in einem benutzerdefinierten Segment gespeichert werden.

Segmentvorlagen sind im Segmentaufbau durch ein spezielles Symbol gekennzeichnet.

## Was ist mit meinen vorhandenen Segmentordnern passiert?    {#section_FB04DCF775694E69B761DCA53F301C30}

Anstelle der Ad-hoc-Analysenordner verwendet der Segment-Manager Tags. Ihre Ordnernamen werden automatisch zu Tags, die auf die jeweiligen Segmente angewendet werden.

## Was ist mit terminierten Berichten passiert, auf die Segmente angewendet sind?    {#section_81D1B215533C46E99E17BAE7A3376FDF}

Terminierte Berichte werden weiterhin fehlerfrei mit den von Ihnen definierten Segmenten ausgeführt.

Wenn Sie ein Segment löschen, funktionieren terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, weiter normal, d. h., das Segment bzw. das Dashboard verwendet weiterhin das gelöschte Segment.

## Was ist ein Trefferbehälter? Unterscheidet er sich vom Seitenansichtscontainer?    {#section_65BBE60A836C4001938830DDA15DC256}

Der Seitenansichts-Container wurde in Treffer-Container umbenannt, um anzuzeigen, dass dieser Container alle Datentypen segmentiert und nicht nur Seitenansichten. So werden z. B. Linktracking-Aufrufe und trackAction-Aufrufe aus den Mobile SDKs durch den Treffercontainer vollständig ein- oder ausgeschlossen.

Beachten Sie, dass sich die Funktionsweise dieses Containers nicht geändert hat. Er wurde lediglich umbenannt.

## Welche Rechte und Privilegien benötige ich, um Segmente zu verwenden, zu erstellen und zu verwalten?    {#section_648DFA3A882146C485A84ED014EEC707}

Alle Benutzer können persönliche Segmente erstellen und bearbeiten. Diese Segmente können direkt für andere Analytics-Benutzer freigegeben werden. Benutzer von Ad Hoc Analysis können jeweils die erstellten und die direkt mit dem Benutzer geteilten Segmente sehen.

In der Webkonsole „Einheitliche Segmentierung“ können Administratoren jedes Segment bearbeiten und Segmente mit Gruppen und allen Angehörigen der Organisation teilen.

## Kann ich alle in meinem Unternehmen vorhandenen Segmente sehen?    {#section_AC2D328C7410419E80C7C17971CD95B3}

Alle Ad-hoc-Analysen-Segmente, die Sie besitzen, sowie Segmente, die spezifisch mit Ihnen geteilt werden, werden angezeigt.

## Kann ich alle Analytics-Segmente im Segment-Manager verwalten?    {#section_AF5EDD72C74A4739BD40C4AF125CE489}

Ad-hoc-Analysen zeigt lediglich von Ihnen erstellte Segmente oder Segmente, die spezifisch mit Ihnen geteilt wurden, an. Lediglich für Ad-hoc-Analysen können Sie den Segment-Manager (Segmente organisieren) verwenden, um Ad-hoc-Analysen-Segmente zu verwalten. Verwenden Sie den Segment-Manager in „Einheitliche Segmentierung“, um alle Analysen-Segmente zu verwalten.

## Was mache ich mit doppelten Segmenten, die zwar denselben Namen, aber unterschiedliche Definitionen haben?    {#section_E2C3A1B4B4274D1B86CAA9C0359D049C}

Nachdem Segmente jetzt von unterschiedlichen Report-Suites genutzt werden können, kann es vorkommen, dass Sie mehrere Segmente mit demselben Namen haben. Wir empfehlen Folgendes:

* Benennen Sie Segmente um, die denselben Namen, aber unterschiedliche Definitionen haben, oder
* Löschen Sie Segmente, die Sie nicht mehr benötigen.

## Welche Maßnahmen empfiehlt Adobe zum Aufräumen von Segmenten?    {#section_3AC2D265F9084557A24C6FB39DC6EE49}

* Markieren Sie alle alten Segmente mit einem Tag.
* Überprüfen Sie all Ihre Segmente.
* Fügen Sie Ihre Segmente gegebenenfalls zu einer Segmentbibliothek hinzu.
* Genehmigen Sie vorschriftsmäßige Segmente.

## Warum kann ich dieses Segment nicht löschen?    {#section_0FEB6711031A4ABCA915CDA745ECF38D}

In der Experience Cloud veröffentlichte Segmente können nicht gelöscht oder bearbeitet werden. Sie können das Segment jedoch kopieren und die Kopie bearbeiten.

## Weitere Informationen zu bestehenden Segmenten    {#section_83ACAB256F394DCD8B424D8920BDD853}

<table id="table_0AE814A64D2A48ABB28402C4303F420E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Segmentkategorie </th> 
   <th colname="col2" class="entry"> Was passiert mit diesen Segmenten? </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Favoriten-Segmente in Ad Hoc Analysis </td> 
   <td colname="col2">Diese Ad Hoc Analysis-Segmente werden in Adobe Analytics als gewöhnliche Segmente angezeigt. <p>Verwechseln Sie sie nicht mit der Favoriten-Funktion im Segment-Manager, über die Sie Segmente als Favoriten markieren können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Vorkonfigurierte Segmente in Ad Hoc Analysis: 
    <ul id="ul_BBF3C3F4D41A40AF98DA9DA6D299AD03"> 
     <li id="li_B65A004BDF8743FDABCD3332AEB8A010">Einzelseitenbesuche </li> 
     <li id="li_908CF5F964154C9D9EBBAC2A900DCB49">Besuche von Mobilgeräten </li> 
     <li id="li_4A715F49AA374463B501D731261A3A4C">Besuche über eine kostenlose Suche </li> 
     <li id="li_67CE51237EC34FD4B33942BA14584EBF">Besuche über eine gebührenpflichtige Suche </li> 
     <li id="li_C3820743178A4E9F9E5E5B5C47401DF2">Besuche mit Besucher-ID-Cookie </li> 
    </ul> </td> 
   <td colname="col2"> <p>Diese Segmente werden als   Segmentvorlagen in den Segmentaufbau migriert. </p> <p>Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Experience Cloud (Suite)-Segmente: 
    <ul id="ul_6968AFF6DEDA4BC8A7885B07CC1F57DF"> 
     <li id="li_073D9496F0C64AEB855855D01E65C1BA">Nichtkäufer </li> 
     <li id="li_8958FD4272A14E16A9AA08216E8BC573">Käufern </li> 
     <li id="li_1436D7C9651D4AC38E10662DEDDD2B95">Erstbesuche </li> 
     <li id="li_69F42B4F6107407792B0014804A8AF7B">Besuche von sozialen Netzwerken aus </li> 
     <li id="li_29CA111186BE475C943E9F8450BDE8C8">Besuche, die länger als 10 Minuten dauern* </li> 
     <li id="li_1FEF207959DC4D2E9FC925DD43177AA0">Besuche mit mehr als 5 vorherigen Besuchen* </li> 
     <li id="li_219AB1D4FD7E469C9076A23D2CCC7C2C">Besuche von Facebook* </li> 
    </ul> </td> 
   <td colname="col2"> <p> Die meisten dieser Segmente (ausgenommen die mit einem Sternchen * gekennzeichneten) werden als Segmentvorlagen in den Segmentaufbau migriert. Darüber hinaus wurden einige neue Segmente hinzugefügt. </p> <p>Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei. </p> </td> 
  </tr> 
 </tbody> 
</table>

