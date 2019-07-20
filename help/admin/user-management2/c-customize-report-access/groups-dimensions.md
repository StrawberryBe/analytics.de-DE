---
description: Legen Sie Benutzerrechte granular fest, einschließlich eVars, Traffic-Berichten, Lösungsberichten und Pfadsetzungsberichten.
keywords: Gruppen; Berechtigungen
seo-description: Legen Sie Benutzerrechte granular fest, einschließlich eVars, Traffic-Berichten, Lösungsberichten und Pfadsetzungsberichten.
seo-title: Dimensionsberechtigungen anpassen
solution: Analytics
subtopic: Benutzer und Gruppen
title: Dimensionsberechtigungen anpassen
topic: Admin Tools
uuid: aaf 164 ad -3863-4129-864 e -39 ec 71 c 6 a 8 eb
translation-type: tm+mt
source-git-commit: e3b1ac3139f26ca3a97f3d2228276e690ec4cb79

---


# Dimensionsberechtigungen anpassen

>[!IMPORTANT]
>
>User and product management is moving to the [Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html). Sie werden von Adobe erfahren, wann Sie Benutzer migrieren müssen. After all customers have migrated, help content for **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin Tools]** &gt; **[!UICONTROL User Management]** will be retired.

Legen Sie Benutzerrechte granular fest, einschließlich eVars, Traffic-Berichten, Lösungsberichten und Pfadsetzungsberichten.

**[!UICONTROL Benutzerverwaltung]** &gt; **[!UICONTROL Gruppen]** &gt; **[!UICONTROL Zugriff auf Bericht]** &gt; **[!UICONTROL Dimensionen]** &gt; **[!UICONTROL Anpassen]**

>[!IMPORTANT]
>
>Einige Dimensionen sind derzeit nicht möglich. Es handelt sich um die folgenden Dimensionen: Mobile Lesezeichenlänge; Mobilgerätenummer; Mobil-DRM; Mobile Informationsdienste; Mobile Java-VM; Mobiles Mail-Design; Mobile Netzprotokolle; Mobilbetriebssystem; Mobiles PTT.
>
>Diese Dimensionen sind für alle Benutzer verfügbar, unabhängig von anderen Berechtigungen.

Die Einstellungen auf dieser Seite beziehen sich auf die Report Suites, die auf der Seite „[!UICONTROL Benutzergruppe definieren]“ ausgewählt wurden.

![](assets/permissions-dimensions.png)

Lesen Sie sich folgende Informationen zur Dimensionskategorie in den Berechtigungen aufmerksam durch.

* Individuelle Berechtigung für eVars 1–250.
* Sämtliche Traffic-Berichte sind Dimensionen.
* Video- und Mobilberichte sind Dimensionen sowie andere Analytics-Lösungsberichte (Experience Manager, Advertising Cloud, Social und durchführen).
* Pfadsetzungsberichte sind für Benutzer mit Zugang zu den übergeordneten Dimensionen verfügbar.
* Alle aktuellen Dimensionen und Metriken in benutzerdefinierten Gruppen wurden automatisch in die neuen Kategorien migriert. Wenn in einer bestehenden Gruppe Metriken aktiv sind, werden für diese Gruppe sämtliche Dimensionen, für die neue Berechtigungen erteilt werden (eVars und inhaltsbasiert), und Metriken als Standardeinstellungen festgelegt.
* Classifications Importer (bisher SAINT) berechtigt für: Zugriff auf Classifications wird durch Zugriff auf die [Variable](https://marketing.adobe.com/resources/help/en_US/reference/c_classifications.html) bestimmt, auf der Classification basiert.

Weitere Informationen finden Sie unter [Häufig gestellte Fragen zu geänderten Berechtigungen](https://marketing.adobe.com/resources/help/en_US/reference/permissions_faq.html).

**Dimensionen anpassen**

Bei den folgenden Elementen handelt es sich um Dimensionen, für die Sie Zugriffsrechte zuweisen können.

<table id="table_F37D74A1619A4560A5F5651E855DAF1C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../admin/admin/conversion-var-admin/conversion-var-admin.md#concept_C02F7AA01DE242F1AA1A4E74022BE9DE" format="dita" scope="local"> eVars </a> </p> </td> 
   <td colname="col2"> <p>Individuelle Berechtigung für eVars 1–250. Bei eVars handelt es sich um benutzerdefinierte Konversionsvariablen, die zur Segmentkonversion von Erfolgsmetriken in benutzerspezifischen Berichten verwendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/props_eVars.html" format="html" scope="external"> Props </a> </p> </td> 
   <td colname="col2"> <p>Props sind benutzerdefinierte Traffic-Variablen. </p> <p>Weitere Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/props_eVars.html" format="html" scope="external">Traffic-Props und Konversions-eVars</a> in der Implementierung von Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/hierN.html" format="html" scope="external"> Hierarchie </a> </p> </td> 
   <td colname="col2"> <p> Die Hierarchievariable bestimmt die Positionierung einer Seite in der Hierarchie der Site oder Seitenstruktur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/listN.html" format="html" scope="external"> Listvar </a> </p> </td> 
   <td colname="col2"> <p> Ähnlich wie bei Listen-Props sind bei Listenvariablen mehrere Werte in derselben Bildanforderung möglich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standard </p> </td> 
   <td colname="col2"> <p>Bezieht sich auf Standard- (vordefinierte) Dimensionen in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/em/" format="https" scope="external"> AEM </a> </p> </td> 
   <td colname="col2"> <p>Adobe Experience Manager     </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/media-optimizer/" format="https" scope="external"> AMO </a> </p> </td> 
   <td colname="col2"> <p>Adobe Advertising Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/" format="https" scope="external"> Activity Map </a> </p> </td> 
   <td colname="col2"> <p> Activity Map-Berichtsdimensionen: Activity Map – Seite; Activity Map – Link; Activity Map – Region; Activity Map – Link nach Region; Activity Map XY </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/mobile/" format="https" scope="external"> Mobile </a> </p> </td> 
   <td colname="col2"> <p>Adobe Mobile Services </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Comscore </p> </td> 
   <td colname="col2"> <p>Diese Partnerintegration ist nicht mehr aktiv. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/hbvideo/nielsen-partnership.html" format="html" scope="external"> Nielsen </a> </p> </td> 
   <td colname="col2"> <p>Partnerintegrationen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Social </p> </td> 
   <td colname="col2"> <p>Nicht verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>

