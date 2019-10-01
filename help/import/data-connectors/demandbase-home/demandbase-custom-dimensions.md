---
description: Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe Integration-Assistenten angegeben werden können.
seo-description: Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe Integration-Assistenten angegeben werden können.
seo-title: Benutzerdefinierte Dimensionen der Demandbase
title: Benutzerdefinierte Dimensionen der Demandbase
uuid: d1621046-3aa2-46b9-a536-4a8fb792b69f
translation-type: tm+mt
source-git-commit: a31f25e8a4681cf34525a7994b00580aa3aac15d

---


# Benutzerdefinierte Dimensionen der Demandbase{#demandbase-custom-dimensions}

Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe Integration-Assistenten angegeben werden können.

Wenn Sie sich nicht sicher sind, welche API-ID exakt in den Assistenten eingegeben werden soll, wenden Sie sich an Ihren Demandbase-Kundenbetreuer.

>[!IMPORTANT]
>
>Es wird dringend empfohlen, IP-Adresse NICHT als benutzerdefinierte Dimension einzubeziehen. Die extrem hohe Anzahl individueller Werte kann zu Leistungsproblemen bei der Berichterstellung führen. Darüber hinaus wird IP-Adresse bereits als Berichtsoption über die Adobe Data Warehouse-Berichterstellung angeboten.

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
   <td colname="col2"> isp </td> 
   <td colname="col3"> Gibt an, ob die identifizierte Organisation als ISP eingestuft ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketingalias </td> 
   <td colname="col2"> marketing_alias </td> 
   <td colname="col3"> Gereinigter und/oder gekürzter Unternehmensname (höchstens 32 Zeichen) zur Verwendung in Anzeigen, Nachrichten oder Marketingkopien. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tags der Kontoüberwachung </td> 
   <td colname="col2"> watch_list (benutzerdefiniert) </td> 
   <td colname="col3">Unbegrenzte Anzahl von Tags, die vom Client definiert wurden und die ihren API-Antwortdaten nach Unternehmen hinzugefügt werden können. <p><b>Beispiel</b>: Wenn Sie über ein Überwachungstag namens Q4-Target verfügen, wird das API-Feld </p> <code> watch_list_q4_target</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fortune 1000 </td> 
   <td colname="col2"> privilege_1000 </td> 
   <td colname="col3"> Gibt an, ob sich die Organisation in der Liste "Fortune 1000"befindet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Forbes 2000 </td> 
   <td colname="col2"> forbes_2000 </td> 
   <td colname="col3"> Gibt an, ob die Organisation in der Liste "Forbes 2000"aufgeführt ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mitarbeiterzahl </td> 
   <td colname="col2"> employee_count </td> 
   <td colname="col3"> Die Anzahl der in der Organisation beschäftigten Personen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Jahresumsatz </td> 
   <td colname="col2"> year_sales </td> 
   <td colname="col3"> Bei öffentlichen Einrichtungen basieren die jährlichen Einnahmen auf den von Unternehmen gemeldeten öffentlichen Aufzeichnungen des globalen Hauptquartiers an allen Standorten. Bei privaten Organisationen basiert die Schätzung auf einer Konsensschätzung der jährlichen Umsatzzahl. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Telefonnummer </td> 
   <td colname="col2"> Telefon </td> 
   <td colname="col3"> Die Telefonnummer der benannten Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Straße </td> 
   <td colname="col2"> street_address </td> 
   <td colname="col3"> Die Straße der identifizierten Einrichtung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stadt </td> 
   <td colname="col2"> Ort </td> 
   <td colname="col3"> Die Stadt der benannten Einrichtung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Land </td> 
   <td colname="col2"> state </td> 
   <td colname="col3"> Der Status der identifizierten Einrichtung. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ländercode </td> 
   <td colname="col2"> country_code </td> 
   <td colname="col3"> Der aus zwei Zeichen bestehende ISO-Ländercode der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Landesname </td> 
   <td colname="col2"> country_name </td> 
   <td colname="col3"> Der Zeichenfolgenwert country name des Landes für die identifizierte Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zip </td> 
   <td colname="col2"> zip </td> 
   <td colname="col3"> Die Postleitzahl des Landes/Bundesstaates der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Webseite </td> 
   <td colname="col2"> web_site </td> 
   <td colname="col3"> Die von der identifizierten Organisation verwendete URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stock Ticker </td> 
   <td colname="col2"> stock_ticker </td> 
   <td colname="col3"> Der Aktienticker, wenn die identifizierte Organisation öffentlich gehandelt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Primärer SIC-Code </td> 
   <td colname="col2"> primary_sic </td> 
   <td colname="col3"> Konsenses SIC-Code, der der angegebenen Organisation zugewiesen wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breitengrad </td> 
   <td colname="col2"> Breitengrad </td> 
   <td colname="col3"> Breitengrad für den Speicherort der identifizierten Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Längengrad </td> 
   <td colname="col2"> Längengrad </td> 
   <td colname="col3"> Länge des Standorts der identifizierten Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Traffic </td> 
   <td colname="col2"> traffic </td> 
   <td colname="col3"> Der Umfang des Website-Traffics, der auf niedrig, mittel oder hoch oder sehr hoch geschätzt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2B </td> 
   <td colname="col2"> b2b </td> 
   <td colname="col3"> Gibt an, dass das identifizierte Unternehmen hauptsächlich an andere Unternehmen verkauft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2C </td> 
   <td colname="col2"> b2c </td> 
   <td colname="col3"> Gibt an, dass das identifizierte Unternehmen hauptsächlich an Verbraucher oder Einzelpersonen verkauft. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Technology Insight </td> 
   <td colname="col2"> ??? </td> 
   <td colname="col3"> Bis zu 75 Technologiekategorien, die von Kunden über Kategorie, Anbieter und Produkte zur Verwendung von Targeting und/oder Anpassen von Anzeigen, Nachrichten oder Marketingkopien definiert werden. </td> 
  </tr> 
 </tbody> 
</table>

