---
description: Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe-Integrationsassistenten angegeben werden können.
title: Benutzerdefinierte Demandbase-Dimensionen
uuid: d1621046-3aa2-46b9-a536-4a8fb792b69f
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 100%

---


# Benutzerdefinierte Demandbase-Dimensionen {#demandbase-custom-dimensions}

Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe-Integrationsassistenten angegeben werden können.

Wenn Sie sich nicht sicher sind, welche API-ID exakt in den Assistenten eingegeben werden soll, wenden Sie sich an Ihren Demandbase-Kundenbetreuer.

>[!IMPORTANT]
>
>Es wird dringend empfohlen, „IP-Adresse“ NICHT als benutzerspezifische Dimension einzubeziehen. Die extrem hohe Anzahl individueller Werte kann zu Leistungsproblemen bei der Berichterstellung führen. Darüber hinaus wird „IP-Adresse“ bereits als Berichtsoption über die Adobe Data Warehouse-Berichterstellung angeboten.

<table id="table_3B44A18BE5FE45BC83389F89B48D9B97"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Dimension </th> 
   <th colname="col2" class="entry"> API-IDs </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> ISP </td> 
   <td colname="col2"> ISP </td> 
   <td colname="col3"> Gibt an, ob die identifizierte Organisation als ISP eingestuft ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketing-Alias </td> 
   <td colname="col2"> marketing_alias </td> 
   <td colname="col3"> Bereinigter bzw. gekürzter Organisationsname (höchstens 32 Zeichen) zur Verwendung in Anzeigen, Nachrichten oder Marketingtexten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tags für Kontoüberwachung </td> 
   <td colname="col2"> watch_list (benutzerspezifisch) </td> 
   <td colname="col3">Unbegrenzte Anzahl von Tags, die vom Client definiert wurden und die ihren API-Antwortdaten nach Organisation hinzugefügt werden können. <p><b>Beispiel</b>: Wenn Sie über ein Überwachungstag namens Q4-Target verfügen, gibt das API-Feld </p> <code> watch_list_q4_target</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fortune 1000 </td> 
   <td colname="col2"> fortune_1000 </td> 
   <td colname="col3"> an, ob die Organisation in der Liste „Fortune 1000“ aufgeführt ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Forbes 2000 </td> 
   <td colname="col2"> forbes_2000 </td> 
   <td colname="col3"> an, ob die Organisation in der Liste „Forbes 2000“ aufgeführt ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mitarbeiterzahl </td> 
   <td colname="col2"> employee_count </td> 
   <td colname="col3"> Die Anzahl der in der Organisation beschäftigten Personen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Jahresumsatz </td> 
   <td colname="col2"> annual_sales </td> 
   <td colname="col3"> Bei öffentlichen Einrichtungen basieren die jährlichen Einnahmen auf den von der Firma gemeldeten öffentlichen Aufzeichnungen des globalen Hauptquartiers an allen Standorten. Bei privaten Organisationen basiert die Schätzung auf einer Konsensschätzung der jährlichen Umsätze. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Telefonnummer </td> 
   <td colname="col2"> phone </td> 
   <td colname="col3"> Die Telefonnummer der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Straße &amp; Hausnr. </td> 
   <td colname="col2"> street_address </td> 
   <td colname="col3"> Straße und Hausnummer der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stadt </td> 
   <td colname="col2"> city </td> 
   <td colname="col3"> Die Stadt der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Land </td> 
   <td colname="col2"> state </td> 
   <td colname="col3"> Das Land der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ländercode </td> 
   <td colname="col2"> country_code </td> 
   <td colname="col3"> Der aus zwei Zeichen bestehende ISO-Ländercode der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Landesname </td> 
   <td colname="col2"> country_name </td> 
   <td colname="col3"> Die Zeichenfolge mit dem Landesnamen des Landes für die angegebene Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zip </td> 
   <td colname="col2"> zip </td> 
   <td colname="col3"> Die Postleitzahl des Landes/Bundeslands der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Website </td> 
   <td colname="col2"> web_site </td> 
   <td colname="col3"> Die von der angegebenen Organisation verwendete URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Börsenticker </td> 
   <td colname="col2"> stock_ticker </td> 
   <td colname="col3"> Der Börsenticker, wenn die angegebene Organisation öffentlich gehandelt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Primärer SIC-Code </td> 
   <td colname="col2"> primary_sic </td> 
   <td colname="col3"> Einheitlicher SIC-Code, welcher der angegebenen Organisation zugewiesen wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breitengrad </td> 
   <td colname="col2"> latitude </td> 
   <td colname="col3"> Breitengrad für den Standort der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Längengrad </td> 
   <td colname="col2"> longitude </td> 
   <td colname="col3"> Längengrad für den Standort der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Traffic </td> 
   <td colname="col2"> traffic </td> 
   <td colname="col3"> Das Volumen des Website-Traffics, das auf niedrig, mittel, hoch oder sehr hoch geschätzt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2B </td> 
   <td colname="col2"> b2b </td> 
   <td colname="col3"> Gibt an, dass die identifizierte Firma hauptsächlich an andere Unternehmen verkauft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2C </td> 
   <td colname="col2"> b2c </td> 
   <td colname="col3"> Gibt an, dass die identifizierte Firma hauptsächlich an Verbraucher oder Einzelanwender verkauft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Technology Insight </td> 
   <td colname="col2"> ??? </td> 
   <td colname="col3"> Bis zu 75 Technologiekategorien, die von Kunden über Kategorie, Anbieter und Produkte zum Targeting bzw. Anpassen von Anzeigen, Mitteilungen oder Marketingtexten definiert werden. </td> 
  </tr> 
 </tbody> 
</table>

