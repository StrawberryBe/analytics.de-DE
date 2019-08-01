---
description: Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe Integration-Assistenten angegeben werden können.
seo-description: Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe Integration-Assistenten angegeben werden können.
seo-title: Demandbase benutzerdefinierte Dimensionen
title: Demandbase benutzerdefinierte Dimensionen
uuid: d 1621046-3 aa 2-46 b 9-a 536-4 a 8 fb 792 b 69 f
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Demandbase Custom Dimensions{#demandbase-custom-dimensions}

Listet optionale Dimensionskennungen auf, die in Schritt 4 des Adobe Integration-Assistenten angegeben werden können.

Wenn Sie sich nicht sicher sind, welche API-ID in den Assistenten eingegeben wurde, wenden Sie sich bitte an Ihren Demandbase-Kundenbetreuer.

>[!IMPORTANT]
>
>Es wird dringend empfohlen, IP-Adressen NICHT als benutzerdefinierte Dimension EINZUSCHLIESSEN. Die sehr hohe Anzahl individueller Werte kann zu Leistungsproblemen bei der Berichterstellung führen. Darüber hinaus wird die IP-Adresse über die Adobe Data Warehouse-Berichterstellung bereits als Berichtsoption angeboten.

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
   <td colname="col3"> Gibt an, ob die Organisation als ISP klassifiziert ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketing Alias </td> 
   <td colname="col2"> marketing_ alias </td> 
   <td colname="col3"> Bereinigter und/oder gekürzter Unternehmensname (32 Zeichen oder weniger) für die Verwendung in Anzeigen, Nachrichten oder Marketingkopien. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kontoüberwachungstags </td> 
   <td colname="col2"> watch_ list (benutzerdefiniert) </td> 
   <td colname="col3">Unbegrenzte Anzahl von Tags, die vom Kunden definiert werden, die ihren API-Antwortdaten durch Organisation hinzugefügt werden können. <p><b>Beispiel</b>: Wenn Sie ein Watch-Tag mit dem Namen Q 4 Target haben, wird das API-Feld </p> <code> watch_ list_ q 4_ target</code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Fortune 1000 </td> 
   <td colname="col2"> fortune_ 1000 </td> 
   <td colname="col3"> Gibt an, ob sich die Organisation in der Liste Fortune 1000 befindet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Forbes 2000 </td> 
   <td colname="col2"> forbes_ 2000 </td> 
   <td colname="col3"> Gibt an, ob sich die Organisation in der Liste "Forbes 2000" befindet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mitarbeiteranzahl </td> 
   <td colname="col2"> employee_ count </td> 
   <td colname="col3"> Die Anzahl der Personen, die im Unternehmen beschäftigt sind. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Jährliche Verkäufe </td> 
   <td colname="col2"> annual_ sales </td> 
   <td colname="col3"> Bei öffentlichen Entitäten basiert der jährliche Umsatz auf öffentlich gemeldeten öffentlichen Datensätzen für das globale HQ an allen Orten. Für private Organisationen basiert er auf einer Konsensschätzung für die Anzahl der jährlichen Verkäufe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Telefonnummer </td> 
   <td colname="col2"> Telefon </td> 
   <td colname="col3"> Die Telefonnummer der identifizierten Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Straße </td> 
   <td colname="col2"> street_ address </td> 
   <td colname="col3"> Die Straße, die die Organisation identifiziert hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stadt </td> 
   <td colname="col2"> Stadt </td> 
   <td colname="col3"> Die Stadt der Organisation identifiziert. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Land </td> 
   <td colname="col2"> state </td> 
   <td colname="col3"> Der Status des identifizierten Unternehmens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ländercode </td> 
   <td colname="col2"> country_ code </td> 
   <td colname="col3"> Der ISO-Code des zweistelligen ISO-Zeichens der Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Landesname </td> 
   <td colname="col2"> country_ name </td> 
   <td colname="col3"> Der Ländername des Landes für die Zeichenfolge des Landes für die identifizierte Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> PLZ </td> 
   <td colname="col2"> zip </td> 
   <td colname="col3"> Die Postleitzahl des Landes/Bundeslandes für die Organisation, die identifiziert wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Website </td> 
   <td colname="col2"> web_ site </td> 
   <td colname="col3"> Die URL, die von der Organisation verwendet wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Aktienticker </td> 
   <td colname="col2"> stock_ ticker </td> 
   <td colname="col3"> Der Aktienticker, wenn die Organisation öffentlich gehandelt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Primärer SIC-Code </td> 
   <td colname="col2"> primary_ arts </td> 
   <td colname="col3"> Der für die Organisation festgelegte Konsens-SIC-Code. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Breitengrad </td> 
   <td colname="col2"> breitengrad </td> 
   <td colname="col3"> Breitengrad für den Standort der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Längengrad </td> 
   <td colname="col2"> Längengrad </td> 
   <td colname="col3"> Längengrad für den Speicherort der angegebenen Organisation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Traffic- </td> 
   <td colname="col2"> Traffic </td> 
   <td colname="col3"> Der Webseiten-Traffic, der auf niedrig, mittel oder hoch oder sehr hoch geschätzt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2B </td> 
   <td colname="col2"> b2b </td> 
   <td colname="col3"> Gibt an, dass das identifizierte Unternehmen hauptsächlich zu anderen Unternehmen verkauft wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> B2C </td> 
   <td colname="col2"> b2c </td> 
   <td colname="col3"> Gibt an, dass das identifizierte Unternehmen hauptsächlich an Verbraucher oder Personen verkauft wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Technology Insight </td> 
   <td colname="col2"> ??? </td> 
   <td colname="col3"> Bis zu 75 Technologiekategorien, die von Kunden über Kategorie, Anbieter und Produkte für die Verwendung von Targeting und/oder Anpassung von Anzeigen, Nachrichten oder Marketingkopien definiert werden. </td> 
  </tr> 
 </tbody> 
</table>

