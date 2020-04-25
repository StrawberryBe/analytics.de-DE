---
description: Legen Sie Benutzerrechte auf einer granularen Ebene fest, einschließlich eVars, Traffic-Berichten, Lösungsberichten und Pfadsetzungsberichten.
keywords: groups;permissions
subtopic: Users and groups
title: Anpassen von Dimensionsberechtigungen
topic: Admin tools
uuid: aaf164ad-3863-4129-864e-39ec71c6a8eb
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Anpassen von Dimensionsberechtigungen

>[!IMPORTANT] Die Verwaltung von Benutzern und Produkten erfolgt künftig von der [Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) aus. Sie werden von Adobe erfahren, wann Sie Benutzer migrieren müssen. Nachdem alle Benutzer migriert wurden, wird die Herausgabe neuer Hilfeinhalte für **[!UICONTROL Analytics]** > **[!UICONTROL Admin Tools]** > **[!UICONTROL Benutzerverwaltung]** eingestellt.

Legen Sie Benutzerrechte auf einer granularen Ebene fest, einschließlich eVars, Traffic-Berichten, Lösungsberichten und Pfadsetzungsberichten.

**[!UICONTROL User Management]** > **[!UICONTROL Gruppen]** > **[!UICONTROL Zugriff auf Berichte]** > **[!UICONTROL Dimensionen]** > **[!UICONTROL Anpassen]**

>[!IMPORTANT] Für einige Dimensionen sind aktuell keine Berechtigungen erforderlich. Es handelt sich um die folgenden Dimensionen: Mobile Lesezeichenlänge; Mobilgerätenummer; Mobil-DRM; Mobile Informationsdienste; Mobile Java-VM; Mobiles Mail-Design; Mobile Netzprotokolle; Mobilbetriebssystem; Mobiles PTT.
>
>Diese Dimensionen sind für alle Benutzer verfügbar, unabhängig von anderen Berechtigungen.

Die Einstellungen auf dieser Seite beziehen sich auf die Report Suites, die auf der Seite „[!UICONTROL Benutzergruppe definieren]“ ausgewählt wurden.

![](assets/permissions-dimensions.png)

Lesen Sie sich folgende Informationen zur Dimensionskategorie in den Berechtigungen aufmerksam durch.

* Individuelle Berechtigung für eVars 1–250.
* Sämtliche Traffic-Berichte sind Dimensionen.
* Video- und Mobilberichte sind Dimensionen, ebenso wie andere Analytics-Lösungsberichte (Experience Manager, Advertising Cloud, Social usw.).
* Pfadsetzungsberichte sind für Benutzer mit Zugang zu den übergeordneten Dimensionen verfügbar.
* Alle aktuellen Dimensionen und Metriken in benutzerdefinierten Gruppen wurden automatisch in die neuen Kategorien migriert. Wenn in einer bestehenden Gruppe Metriken aktiv sind, werden für diese Gruppe sämtliche Dimensionen, für die neue Berechtigungen erteilt werden (eVars und inhaltsbasiert), und Metriken als Standardeinstellungen festgelegt.
* Classifications Importer-Berechtigungen (bisher SAINT): Der Zugriff auf Klassifizierungen wird durch den Zugriff auf die [Variable](https://marketing.adobe.com/resources/help/de_DE/reference/c_classifications.html) bestimmt, auf die sich die Klassifizierung stützt.

Weitere Informationen finden Sie unter [Häufig gestellte Fragen zu geänderten Berechtigungen](https://marketing.adobe.com/resources/help/de_DE/reference/permissions_faq.html).

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
   <td colname="col1"> <p> <a href="/help/admin/admin/conversion-var-admin/conversion-var-admin.md"> eVars </a> </p> </td> 
   <td colname="col2"> <p>Individuelle Berechtigung für eVars 1–250. Bei eVars handelt es sich um benutzerdefinierte Konversionsvariablen, die zur Segmentkonversion von Erfolgsmetriken in benutzerspezifischen Berichten verwendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/props_eVars.html"> Props </a> </p> </td> 
   <td colname="col2"> <p>Props sind benutzerdefinierte Traffic-Variablen. </p> <p>Weitere Informationen finden Sie unter <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/props_eVars.html">Traffic-Props und Konversions-eVars</a> in der Implementierung von Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/hierN.html"> Hierarchy </a> </p> </td> 
   <td colname="col2"> <p> Die Hierarchievariable bestimmt die Positionierung einer Seite in der Hierarchie der Site oder Seitenstruktur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/listN.html"> Listvar </a> </p> </td> 
   <td colname="col2"> <p> Ähnlich wie bei Listen-Props sind bei Listenvariablen mehrere Werte in derselben Bildanforderung möglich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standard </p> </td> 
   <td colname="col2"> <p>Bezieht sich auf Standard- (vordefinierte) Dimensionen in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/em/"> AEM </a> </p> </td> 
   <td colname="col2"> <p>Adobe Experience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/media-optimizer/"> AMO </a> </p> </td> 
   <td colname="col2"> <p>Adobe Advertising Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/analytics/activitymap/"> Activity Map </a> </p> </td> 
   <td colname="col2"> <p> Activity Map-Berichtsdimensionen: Activity Map – Seite; Activity Map – Link; Activity Map – Region; Activity Map – Link nach Region; Activity Map XY </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/de_DE/mobile/"> Mobile </a> </p> </td> 
   <td colname="col2"> <p>Adobe Mobile Services </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Comscore </p> </td> 
   <td colname="col2"> <p>Diese Partnerintegration ist nicht mehr aktiv. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/de-DE/media-analytics/using/media-overview.html"> Nielsen </a> </p> </td> 
   <td colname="col2"> <p>Diese Partnerintegration ist nicht mehr aktiv. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Social </p> </td> 
   <td colname="col2"> <p>Nicht verwendet. </p> </td> 
  </tr> 
 </tbody> 
</table>
