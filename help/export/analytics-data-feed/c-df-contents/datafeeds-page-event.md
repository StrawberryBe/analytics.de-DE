---
description: Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.
keywords: Datenfeed; page; event; page_ event; post_ page_ event
seo-description: Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.
seo-title: Seitenereignissuche
solution: Analytics
title: Seitenereignissuche
topic: Reports and Analytics
uuid: 73 af 597 c -5560-466 e -94 b 2-ddd 1 d 64797 c 8
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Seitenereignissuche

Suchtabelle zur Bestimmung der Art eines Treffers auf der Grundlage des Werts „page_event“.

<table id="table_33AF375E0B41474696D7A4A92C652A5F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Treffertyp </th> 
   <th colname="col02" class="entry"> Wert „page_event“ </th> 
   <th colname="col2" class="entry"> Wert „post_page_event“ </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Seitenansichten </td> 
   <td colname="col02"> identisch mit „post“-Wert </td> 
   <td colname="col2"> <p>0 für alle Seitenansichten (<code>s.t()</code>-Aufrufe) </p> <p>0 für <code>trackState</code>-Aufrufe von mobilen SDKs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Linktracking </td> 
   <td colname="col02"> <p>10 für „Sonstige-Link“ </p> <p>10 für <code>trackAction</code>- und Lebenszyklusaufrufe von mobile SDKs. </p> <p>11 für „Download-Link“ </p> <p>12 für „externer Link oder Exitlink“ </p> </td> 
   <td colname="col2"> <p>100 für „Sonstige-Link“ </p> <p>100 für <code>trackAction</code>- und Lebenszyklusaufrufe von mobile SDKs. </p> <p>101 für „Download-Link“ </p> <p>102 für „externer Link oder Exitlink“ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meilenstein-Video </td> 
   <td colname="col02"> 
    <!--<p>30 - Legacy full media tracking event at the end of the video playback (no longer supported)</p>--> <p>31 – Ereignis Medium starten </p> <p>32 - Ereignis "Nur Medium aktualisieren" (keine evar- oder andere Variablenverarbeitung) </p> <p>33 – Ereignis Medium und andere Variable aktualisieren (einschließlich eVar- oder andere Variablenverarbeitung) </p> </td> 
   <td colname="col2"> 
    <!--<p> 75 - Legacy full media tracking event at theend of the video playback (no longer supported)</p>--> <p> 76 – Ereignis Medium starten </p> <p>77 – Ereignis Nur Medium aktualisieren (es wird keine eVar- oder andere Variablenverarbeitung ausgeführt) </p> <p>78 – Ereignis Medium und andere Variable aktualisieren (einschließlich eVar- oder andere Variablenverarbeitung) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heartbeat-Video </p> </td> 
   <td colname="col02"> identisch mit „post“-Wert </td> 
   <td colname="col2"> <p> 50 = (Nicht-Primetime) Medien-Stream-Start </p> <p> 51 = (Nicht-Primetime) Medien-Stream-Abschluss (Beenden/Abschließen) </p> <p> 52 = (Nicht-Primetime) Medien-Stream-Scrubbing </p> <p> 53 = (Nicht-Primetime) Medien-Stream-Keepalive </p> <p> 54 = (Nicht-Primetime) Medien-Stream-Anzeigenstart </p> <p> 55 = (Nicht-Primetime) Medien-Stream-Anzeigenbeendigung (Beenden/Abschließen) </p> <p> 56 = (Nicht-Primetime) Medien-Stream-Anzeigen-Suche </p> <p> 60 = Primetime-Medien-Stream-Start </p> <p> 61 = Primetime-Medien-Stream-Abschluss (Beenden/Abschließen) </p> <p> 62 = Primetime-Medien-Stream-Scrubbing </p> <p> 63 = Primetime-Medien-Stream-Keepalive </p> <p> 64 = Primetime-Medien-Stream-Anzeigenstart </p> <p> 65 = Primetime-Medien-Stream-Anzeigenabschluss (Beenden/Abschließen) </p> <p> 66 = Primetime-Medien-Stream-Anzeigen-Suche </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Survey </td> 
   <td colname="col02"> 40 </td> 
   <td colname="col2"> 80 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analytics für Target </td> 
   <td colname="col02"> 70 – Gibt einen Treffer an, der Zielaktivitätsdaten enthält. Dieser Wert beträgt 70 für Treffer, die möglicherweise mit einem Analytics-Aufruf in Verbindung stehen. </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

