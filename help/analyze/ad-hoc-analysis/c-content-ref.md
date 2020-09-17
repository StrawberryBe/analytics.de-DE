---
description: Ad Hoc Analysis können in die Analytics-Segmentierungs-Umgebung integriert werden. So können Sie Besuchersegmente über Adobe-Produkte hinweg erstellen, teilen, verwalten und anwenden. Ad Hoc Analysis bietet für Segment Builder und Segment Manager dieselbe Java-basierte Benutzeroberfläche, die auch von anderen webbasierten Analytics-Werkzeugen verwendet wird. Dadurch können Server-Aufrufe abgestimmt und dieselben Funktionen wie in einer Java-basierten Konsole bereitgestellt werden.
title: Segmente erstellen
topic: Ad hoc analysis
uuid: e14fb777-900a-4700-8dc7-56a45c678d29
translation-type: tm+mt
source-git-commit: d4cb2acb4ecaecce3644a2f3cf29913440e5cd6a
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 93%

---


# Segmente erstellen

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 in den Status als lebensbedrohlich. [Weitere Infos...](https://adobe.ly/discoverworkspace).

Ad Hoc Analysis können in die Analytics-Segmentierungs-Umgebung integriert werden. So können Sie Besuchersegmente über Adobe-Produkte hinweg erstellen, teilen, verwalten und anwenden. Ad Hoc Analysis bietet für Segment Builder und Segment Manager dieselbe Java-basierte Benutzeroberfläche, die auch von anderen webbasierten Analytics-Werkzeugen verwendet wird. Dadurch können Server-Aufrufe abgestimmt und dieselben Funktionen wie in einer Java-basierten Konsole bereitgestellt werden.

Ad Hoc Analysis umfassen bewährte Funktionen zum Erstellen von Segmenten, aber auch neue Funktionsupgrades wie den [Segment Manager](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segmentation-workflow/seg-manage.html) zum Einrichten eines [Segmentverwaltungs arbeitsablaufs](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-workflow.html). Sie können wie gewohnt im [Segment-Builder](/help/components/segmentation/segmentation-workflow/seg-build.md) Segmente erstellen und speichern, [oder Sie können über die Ad Hoc Analysis-Konsole](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.html) Segmente aus einem Fallout-Bericht erstellen und dann die neuen oder erweiterten Segmente in der Zielgruppenbibliothek speichern, damit sie allgemein zugänglich sind und angewendet werden können.  ![](assets/seg__overview_ad_hoc.png)

## Einheitliche Segmentierung in Ad Hoc Analysis {#section_5FA03A06DE054448AD519CE30C39E294}

Informationen zum Erstellen und Verwalten von Segmenten in der Umgebung der einheitlichen Segmentierung, einschließlich der Ad-hoc-Analysefunktionen, finden Sie in der Dokumentation zum Bereich [Einheitliche Segmentierung](/help/components/segmentation/segmentation-workflow/seg-build.md).

* [Neue Funktionen](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_BD58629D1A9346BF879E229FA6BEC7A2)
* [Was ist mit meinen vorhandenen Segmenten passiert?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_76CF47142D1A4FB6A0718AD9073049FE)
* [Was ist mit meinen vorhandenen Segmentordnern passiert?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_FB04DCF775694E69B761DCA53F301C30)
* [Kann ich mit dem Segment-Manager alle Analytics-Segmente verwalten?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_AF5EDD72C74A4739BD40C4AF125CE489)
* [Was ist ein Treffer-Container? Unterscheidet er sich vom Seitenansichts-Container?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_65BBE60A836C4001938830DDA15DC256)
* [Welche Berechtigungen benötige ich, um Segmente zu verwenden, zu erstellen und zu verwalten?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_648DFA3A882146C485A84ED014EEC707)
* [Was soll ich mit doppelten Segmenten tun, die...](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_E2C3A1B4B4274D1B86CAA9C0359D049C)
* [Wie lautet die Empfehlung von Adobe für das Bereinigen von Segmenten?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_3AC2D265F9084557A24C6FB39DC6EE49)
* [Warum kann ich dieses Segment nicht löschen?](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_0FEB6711031A4ABCA915CDA745ECF38D)
* [Weitere Informationen zu bestehenden Segmenten](/help/analyze/ad-hoc-analysis/c-content-ref.md#section_83ACAB256F394DCD8B424D8920BDD853)

## Funktionen {#section_BD58629D1A9346BF879E229FA6BEC7A2}

* [Alle Segmente](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/seg-home.html) gelten nun für alle Report Suites. Bisher waren die Segmente spezifisch für die jeweilige Report Suite.
* Der neue [Segment-Manager](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segmentation-workflow/seg-manage.html) ermöglicht die Einrichtung von [Workflows](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-workflow.html) und bietet Funktionen zum Teilen, Taggen, Prüfen und Genehmigen.
* Der [Segment-Builder](/help/components/segmentation/segmentation-workflow/seg-build.md) wurde aktualisiert, um das Erstellen von Segmenten zu vereinfachen.
* Sie können Segmente zum Organisieren und Suchen [taggen](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-tag.html), anstatt Ordner zu verwenden. Bisher wurden Ordner verwendet (in [!DNL ad hoc analysis]), um Segmente zu organisieren.
* [Sequenzielle Segmente](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-sequential-build.html) können jetzt außerhalb von Ad Hoc Analysis erstellt werden.

   >[!NOTE]
   >
   >In Ad Hoc Analysis können Sie Segmenten keine Datumsbereiche hinzufügen. Diese Funktion ist in Analysis Workspace verfügbar. Außerdem können Sie „Nur vor Sequenz“ oder „Nur nach Sequenz“ in Ad Hoc Analysis nicht verwenden.

## Was ist mit meinen vorhandenen Segmenten passiert? {#section_76CF47142D1A4FB6A0718AD9073049FE}

Ihre vorhandenen Segmente funktionieren genau wie vor der Einführung der Analytics-Segmentierung. Alle Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei.

Die meisten bisherigen vordefinierten und Suite-Segmente werden als Segmentvorlagen in den Segmentaufbau migriert. Segmentvorlagen werden verwendet, um schnell benutzerdefinierte Segmente mit gängigen Zielgruppen zu erstellen. Segmentvorlagen können nicht direkt auf einen Bericht angewendet werden, sie können aber problemlos in einem benutzerdefinierten Segment gespeichert werden.

## Was ist mit meinen vorhandenen Segmentordnern passiert?  {#section_FB04DCF775694E69B761DCA53F301C30}

Anstatt der (Ad Hoc Analysis-) Ordner verwendet der Segment-Manager [Tags](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/seg-tag.html). Ihre Ordnernamen werden automatisch zu Tags, die auf die jeweiligen Segmente angewendet werden.

## Kann ich alle Analytics-Segmente im Segment-Manager verwalten?  {#section_AF5EDD72C74A4739BD40C4AF125CE489}

Im Segment Manager der Ad Hoc Analysis sehen Sie nur Ihre eigenen Segmente (Segmente, die Sie selbst erstellt haben) und Segmente, die für Sie freigegeben wurden.

## Was ist ein Trefferbehälter? Unterscheidet er sich vom Seitenansichtscontainer?  {#section_65BBE60A836C4001938830DDA15DC256}

Der Seitenansichts-Container wurde in Treffer-Container umbenannt, um anzuzeigen, dass dieser Container alle Datentypen segmentiert und nicht nur Seitenansichten. Zum Beispiel werden Linktracking-Aufrufe und [!DNL trackAction]-Aufrufe von mobilen SDKs vom Treffer-Container entweder komplett eingeschlossen oder ausgeschlossen.

Beachten Sie, dass sich die Funktionsweise dieses Containers nicht geändert hat. Er wurde lediglich umbenannt.

## Welche Rechte und Privilegien benötige ich, um Segmente zu verwenden, zu erstellen und zu verwalten?  {#section_648DFA3A882146C485A84ED014EEC707}

Alle Benutzer können persönliche Segmente erstellen und bearbeiten. Diese Segmente können direkt für andere Analytics-Benutzer freigegeben werden.

Admins können alle Segmente bearbeiten, [Segmente für Gruppen freigeben](https://docs.adobe.com/content/help/en/analytics/components/segmentation/segmentation-workflow/t-seg-share.html) und [Rechte](https://docs.adobe.com/content/help/de-DE/analytics/components/segmentation/segment-reference/seg-rights.html) für den Zugriff auf Segmente innerhalb der Organisation festlegen.

## Was mache ich mit doppelten Segmenten, die zwar denselben Namen, aber unterschiedliche Definitionen haben?  {#section_E2C3A1B4B4274D1B86CAA9C0359D049C}

Da Segmente jetzt von unterschiedlichen Report-Suites genutzt werden können, kann es vorkommen, dass Sie mehrere Segmente mit demselben Namen haben. Wir empfehlen Folgendes:

* Benennen Sie Segmente um, die denselben Namen, aber unterschiedliche Definitionen haben, oder
* Löschen Sie Segmente, die Sie nicht mehr benötigen.

## Welche Maßnahmen empfiehlt Adobe zum Aufräumen von Segmenten?  {#section_3AC2D265F9084557A24C6FB39DC6EE49}

* Markieren Sie alle alten Segmente mit einem Tag.
* Überprüfen Sie all Ihre Segmente.
* Fügen Sie Ihre Segmente gegebenenfalls zu einer Segmentbibliothek hinzu.
* Bestätigen Sie die vorschriftsgemäßen Segmente.
* Taggen Sie Segmente unter Einhaltung der  Best Practices.

## Warum kann ich dieses Segment nicht löschen?  {#section_0FEB6711031A4ABCA915CDA745ECF38D}

In der [Experience Cloud](https://docs.adobe.com/content/help/de-DE/core-services/interface/audiences/t-publish-audience-segment.html) veröffentlichte Segmente können nicht gelöscht oder bearbeitet werden. Sie können das Segment jedoch kopieren und die Kopie bearbeiten.

## Weitere Informationen zu bestehenden Segmenten  {#section_83ACAB256F394DCD8B424D8920BDD853}

<table id="table_0AE814A64D2A48ABB28402C4303F420E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Segmentkategorie </th> 
   <th colname="col2" class="entry"> Was geschieht mit diesen Segmenten? </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Favoriten (Ad Hoc Analysis) </td> 
   <td colname="col2">Diese Ad Hoc Analysis-Segmente werden in Adobe Analytics als gewöhnliche Segmente angezeigt. <p>Verwechseln Sie sie nicht mit der Favoriten-Funktion im Segment-Manager, über die Sie Segmente als Favoriten markieren können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Vorkonfigurierte Segmente: 
    <ul id="ul_BBF3C3F4D41A40AF98DA9DA6D299AD03"> 
     <li id="li_B65A004BDF8743FDABCD3332AEB8A010">Einzelseitenbesuche </li> 
     <li id="li_908CF5F964154C9D9EBBAC2A900DCB49">Besuche von Mobilgeräten </li> 
     <li id="li_4A715F49AA374463B501D731261A3A4C">Besuche über eine kostenlose Suche </li> 
     <li id="li_67CE51237EC34FD4B33942BA14584EBF">Besuche über eine gebührenpflichtige Suche </li> 
     <li id="li_C3820743178A4E9F9E5E5B5C47401DF2">Besuche mit Besucher-ID-Cookie </li> 
    </ul> </td> 
   <td colname="col2"> <p>Diese Segmente werden als  Segmentvorlagen in den Segmentaufbau migriert. </p> <p>Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei. </p> </td> 
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
   <td colname="col2"> <p> Die meisten dieser Segmente (ausgenommen die mit einem Sternchen * gekennzeichneten) werden als  Segmentvorlagen in den Segmentaufbau migriert. Darüber hinaus wurden einige neue Segmente hinzugefügt. </p> <p>Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1">Admin-Segmente <p>(auch „globale Segmente“ genannt) </p> </td> 
   <td colname="col2"> <p> <b>Admin</b>-Segmente werden in die neue Segmentoberfläche migriert und werden dort als für alle freigegebene Segmente angezeigt. </p> <p>Der Eigentümer dieser Segmente wird mit dem ältesten Konto in der Liste der Admin-Benutzer in der Organisation als Admin angelegt. Es können jedoch alle Administratoren diese Segmente löschen, bearbeiten und teilen. </p> <p>Die Segmentverwaltungsoberfläche der Admin Console, über die Administratoren diese globalen Segmente erstellen und verwalten konnten, gibt es nicht mehr. Administratoren können Segmente nun mit dem neuen Segment-Builder erstellen und diese mit den entsprechenden Gruppen oder Einzelpersonen oder mit allen teilen. </p> </td> 
  </tr> 
 </tbody> 
</table>

