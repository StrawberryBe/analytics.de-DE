---
description: Zeigt Daten zum Speicherort des Besuchers an. GeoSegmentation-Berichte umfassen Länder, Regionen, Städte, US-Bundesstaaten und US-DMA (Digital Marketing Area). GeoSegmentation-Berichte sind für alle Kunden aktiviert.
title: GeoSegmentation
topic: Reports
uuid: 66aa22c4-dcbc-491a-b23c-0c3d87444d23
translation-type: tm+mt
source-git-commit: 5e47974fcf95625def21a9011ad981197ae39c99

---


# GeoSegmentation

Zeigt Daten zum Speicherort des Besuchers an. GeoSegmentation-Berichte umfassen Länder, Regionen, Städte, US-Bundesstaaten und US-DMA (Digital Marketing Area). GeoSegmentation-Berichte sind für alle Kunden aktiviert.

Alle Metriken, die an anderen Stellen in Reports &amp; Analysen für Sie verfügbar sind, werden automatisch in die Berichte Länder, Regionen, Städte, US-Bundesstaaten und DMA aufgenommen: Konversions- und besuchsbasierte Metriken sowie berechnete Metriken. For more information, see this Adobe [blog](https://blogs.adobe.com/digitalmarketing/analytics/introducing-new-metrics-in-geosegmentation-and-more/) post.

<table id="table_566CFFC82E1149D8BAFE6641627FCF1F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bericht </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Länder </td> 
   <td colname="col2"> <p> Die größte geografische Division. Neben den standardmäßigen Rang- und Trendansichten, die in den meisten Berichten verfügbar sind, gibt es hier auch eine Landkartenansicht, in der die Länder je nach Beitrag zum gesamten Verkehrsaufkommen farbkodiert angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Regionen </td> 
   <td colname="col2"> <p> Ein geografisches Gebiet, das kleiner als ein Land, aber größer als eine Stadt ist. In einigen Ländern ist eine Region ein Staat, eine Provinz oder eine Präfektur. In anderen Bereichen handelt es sich um ein konstituierendes Land, eine Abteilung oder eine Metropolregion. Rechts neben der jeweiligen Region wird das Land in Klammern dargestellt. </p> <p>Klicken Sie in den Tabellendetails auf Städtebericht für diese Region ausführen (Lupe), um einen Bericht auszuführen, der zeigt, wie die Städte in einer ausgewählten Region im Vergleich zu anderen Städten in der Region abschneiden. </p> <p>See <a href="/help/components/c-variables/dimensionslist/reports-geosegmentation-reference.md"  > GeoSegmentation Regions and Postal Code usage by Country</a> to see which countries use regions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Städte </td> 
   <td colname="col2"> <p> Die kleinste geografische Einteilung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> U.S.-Bundesstaaten </td> 
   <td colname="col2"> <p> Eine Heatmap mit Besuchern zu jedem Bundesstaat der Vereinigten Staaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> U.S. DMA (Designierter Marktbereich) </td> 
   <td colname="col2"> <p> (Digital Marketing Area) Medienmarktbereiche für Radio und Fernsehen in den Vereinigten Staaten. Sie können den Bericht so filtern, dass nur Marketingbereiche innerhalb eines bestimmten Status angezeigt werden. Diese Daten werden durch eine Partnerschaft zwischen Adobe und Nielsen Media Research, Inc. bereitgestellt. </p> <p>Hinweis: Der Eintrag „Nicht angegeben“ in US-DMA-Berichten zeigt Besucher an, die keinem bestimmten DMA zugeordnet werden konnten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Berichtsgenauigkeit </td> 
   <td colname="col2"> <p>Adobe arbeitet mit Digital Envoy zusammen, einem führenden Anbieter von IP-Intelligence- und Authentifizierungslösungen, um GeoSegmentation, eine geografische Messungsfunktion, die auf den IP-Adressen der Endbenutzer basiert, zu Angebot zu machen. Obwohl die Genauigkeit auf der Grundlage einzelner Datensätze variieren kann, ist die Genauigkeit von Digital Envoy-Angeboten im Allgemeinen zu 99 % auf Landesebene, zu über 97 % auf Regionsebene und zu über 90 % auf Stadtebene unterschiedlich. </p> <p>Note: These numbers assume that <a href="/help/admin/admin/general-acct-settings-admin.md">the setting</a> to remove the last octet of the IP address is NOT enabled. </p> <p>IP-Adressen werden Postleitzahlen zugeordnet. Alle Städte werden über die Postleitzahlen definiert, die durch die lokalen Behörden für die jeweiligen Städte festgelegt wurden. So sind z. B. die Randbezirke von Berlin nicht in der Definition von Berlin enthalten, jedoch jeweils separat aufgeführt, weil davon ausgegangen wird, dass die IP-Adressen einer exakten Postleitzahl in einer dieser Städte zugeordnet werden können. </p> <p>Einige Faktoren, die GeoSegmentation-Daten beeinflussen können, sind: </p> 
    <ul id="ul_1B05024AD5174232A8DB8145753FB09B"> 
     <li id="li_C3A21E7C1186490EB9A236634DB45E7F">IP-Adressen, die Unternehmensvertreter repräsentieren. Diese können als Traffic erscheinen, der über das Unternehmensnetzwerk des Benutzers kommt, was tatsächlich ein anderer Ort sein kann, wenn der Benutzer remote arbeitet. </li> 
     <li id="li_56FC36B3598C420F9246D4E8772822A7">Mobile IP-Adressen. Das mobile IP-Targeting funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Luftfahrtunternehmen baut den IP-Verkehr über zentrale oder regionale POP auf. </li> 
     <li id="li_C1EED854AE584489BCBC2A7AA20B8EF1">IP-Adressen von Benutzern von Satelliten-ISPs. Die Identifizierung des spezifischen Standorts dieser Benutzer ist schwierig, da sie normalerweise vom Standort des Uplink kommen. </li> 
     <li id="li_A735756F39554DF19E05D251CA614F02">Militärische und staatliche IPs. Dabei handelt es sich häufig um Mitarbeiter, die auf Reisen um den Globus und über ihren Heimatort statt über den Standort oder das Büro, in dem sie derzeit stationiert sind, einreisen. </li> 
     <li id="li_ACFF1B8094684173B8325A44304CA32B">Unsere GeoSegmentation/IP-Daten werden von einem Drittanbieter bereitgestellt und regelmäßig auf der Grundlage von Informationen aktualisiert, die von ISPs und anderen Netzwerkquellen bereitgestellt werden. IP-Lookups sind von Natur aus unbeständig, da sie häufig auf der ganzen Welt gekauft und verkauft werden. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

