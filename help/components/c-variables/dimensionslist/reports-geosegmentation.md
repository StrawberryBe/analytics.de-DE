---
description: Zeigt Daten zum Standort des Besuchers. GeoSegmentation-Berichte beinhalten Daten zu Ländern, Regionen, Städten, US-Bundesstaaten und US-DMA (Digital Marketing Areas). GeoSegmentation-Berichte sind für alle Kunden aktiviert.
seo-description: Zeigt Daten zum Standort des Besuchers. GeoSegmentation-Berichte beinhalten Daten zu Ländern, Regionen, Städten, US-Bundesstaaten und US-DMA (Digital Marketing Areas). GeoSegmentation-Berichte sind für alle Kunden aktiviert.
seo-title: GeoSegmentation
solution: Analytics
title: GeoSegmentation
topic: 'Berichte    '
uuid: 66 aa 22 c 4-dcbc -491 a-b 23 c -0 c 3 d 87444 d 23
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# GeoSegmentation

Zeigt Daten zum Standort des Besuchers. GeoSegmentation-Berichte beinhalten Daten zu Ländern, Regionen, Städten, US-Bundesstaaten und US-DMA (Digital Marketing Areas). GeoSegmentation-Berichte sind für alle Kunden aktiviert.

Alle Metriken, die an anderen Stellen in Reports &amp; Analytics für Sie verfügbar sind, werden automatisch in die Berichte zu Ländern, Regionen, Städten, US-Bundesstaaten und DMAs aufgenommen: konversions- und besuchsbasierte Metriken sowie berechnete Metriken. Weitere Informationen finden Sie in diesem Adobe [Blog](https://blogs.adobe.com/digitalmarketing/analytics/introducing-new-metrics-in-geosegmentation-and-more/)-Beitrag.

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
   <td colname="col2"> <p> Die größte geografische Einteilung. Neben den standardmäßigen Rang- und Trendansichten, die in den meisten Berichten verfügbar sind, gibt es hier auch eine Landkartenansicht, in der die Länder je nach Beitrag zum gesamten Verkehrsaufkommen farbkodiert angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Regionen </td> 
   <td colname="col2"> <p> Ein geografischer Bereich, der kleiner ist als ein Land, jedoch größer als eine Stadt. In einigen Ländern ist unter einer Region ein Bundesstaat, eine Provinz oder eine Präfektur zu verstehen. In anderen Bereichen handelt es sich um ein eigenständiges Land, ein Distrikt oder eine Metropolregion. Rechts neben der jeweiligen Region wird das Land in Klammern angezeigt. </p> <p>Klicken Sie in den Tabellendetails auf Städtebericht für diese Region ausführen (die Lupe), um einen Bericht auszuführen, der Leistungsdaten zu Städten in einer ausgewählten Region im Vergleich mit anderen Städten in der Region liefert. </p> <p>Siehe <a href="../../../components/c-variables/dimensionslist/reports-geosegmentation-reference.md#concept_F7D998B418544B39ACD8838B48B732F1" format="dita" scope="local"> Verwendung von GeoSegmentation-Regionen und Postleitzahlen nach Land</a>, um zu sehen, welche Länder Regionen verwenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Städte </td> 
   <td colname="col2"> <p> Die kleinste geografische Einteilung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> US-Bundesstaaten </td> 
   <td colname="col2"> <p> Eine „Heat Map“ zeigt Ihnen die Besucher aus allen Bundesstaaten in den USA an, die Ihre Site aufrufen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> U.S. DMA (Designierter Marktbereich) </td> 
   <td colname="col2"> <p> Medienmarktbereiche für Radio und Fernsehen in den USA. Sie können den Bericht filtern, um nur Marketingbereiche innerhalb eines bestimmten Bundesstaates anzuzeigen. Diese Daten stehen Ihnen aufgrund der Partnerschaft zwischen Adobe und Nielsen Media Research, Inc. zur Verfügung. </p> <p>Hinweis: Der Eintrag „Nicht angegeben“ in US-DMA-Berichten zeigt Besucher an, die keinem bestimmten DMA zugeordnet werden konnten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Genauigkeit von Berichten </td> 
   <td colname="col2"> <p>Adobe arbeitet mit Digital Envoy zusammen, einem führenden Anbieter von IP-Intelligence- und Authentifizierungslösungen, um GeoSegmentation anzubieten. Diese geografische Messfunktion basiert auf der IP-Adresse der Endbenutzer. Eine Genauigkeit, die auf einzelnen Datenreihen basiert, kann schwanken. Dagegen bietet Digital Envoy im Allgemeinen eine 99%ige Genauigkeit auf Landesebene, eine über 97%ige Genauigkeit auf Regionsebene und eine über 90%ige Genauigkeit auf Stadtebene. </p> <p>Hinweis: Diese Zahlen gehen davon aus, dass [die Einstellung] (/help/admin/admin/general-acct-settings-admin. md) zum Entfernen des letzten 8-Bit-Zeichens der IP-Adresse NICHT aktiviert ist. </p> <p>IP-Adressen werden Postleitzahlen zugeordnet. Alle Städte werden über die Postleitzahlen definiert, die durch die lokalen Behörden für die jeweiligen Städte festgelegt wurden. So sind z. B. die Randbezirke von Berlin nicht in der Definition von Berlin enthalten, jedoch jeweils separat aufgeführt, weil davon ausgegangen wird, dass die IP-Adressen einer exakten Postleitzahl in einer dieser Städte zugeordnet werden können. </p> <p>Folgende Faktoren können unter anderem die GeoSegmentierungsdaten beeinflussen: </p> 
    <ul id="ul_1B05024AD5174232A8DB8145753FB09B"> 
     <li id="li_C3A21E7C1186490EB9A236634DB45E7F">IP-Adressen, die Unternehmensproxys darstellen. Bei diesen Adressen kann Traffic so erscheinen, als würde er vom Unternehmensnetzwerk des Benutzer stammen. Tatsächlich kann er jedoch von einem anderen Ort übertragen werden, wenn der Benutzer remote arbeitet. </li> 
     <li id="li_56FC36B3598C420F9246D4E8772822A7">Mobile IP-Adressen. Die mobile IP-Zielerfassung funktioniert auf unterschiedlichen Ebenen, je nach Standort und Netzwerk. Eine Reihe von Netzbetreibern transportiert den IP-Traffic über zentralisierte oder regionale POPs. </li> 
     <li id="li_C1EED854AE584489BCBC2A7AA20B8EF1">IP-Adressen, die Benutzern von Satelliten-ISPs gehören. Es ist schwierig, den speziellen Standort dieser Benutzer zu ermitteln, da es aussieht, als würden sie sich am Standort des Uplinks befinden. </li> 
     <li id="li_A735756F39554DF19E05D251CA614F02">Militärische und Regierungs-IPs. Häufig sind die Mitarbeiter hier weltweit unterwegs und der Zugriff erfolgt eher über ihren Heimatstandort als von der Basis oder der Behörde aus, in der sie gegenwärtig beschäftigt sind. </li> 
     <li id="li_ACFF1B8094684173B8325A44304CA32B">Unsere GeoSegmentation-/IP-Daten werden von einem Drittanbieter bereitgestellt und regelmäßig auf Grundlage von Informationen von Internetdienstleistern und anderen Netzwerkquellen aktualisiert. Die Feststellung von IPs kann von Natur aus abweichende Ergebnisse liefern, da die Adressen weltweit ständig gekauft und wieder verkauft werden. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

