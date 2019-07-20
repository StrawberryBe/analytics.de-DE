---
description: Wenn ein Fehler auftritt, wird in der Spalte „Auftragsstatus“ ein Fehler gemeldet.
keywords: Datenfeed; job; Fehlerbehebung; error; ftp; chdir; connect; login; put
seo-description: Wenn ein Fehler auftritt, wird in der Spalte „Auftragsstatus“ ein Fehler gemeldet.
seo-title: Fehlerbehebung bei Aufträgen
solution: Analytics
title: Fehlerbehebung bei Aufträgen
uuid: 8 fbb 914 e -03 db -434 e-b 4 d 3-8594144 ff 2 b 7
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Fehlerbehebung bei Aufträgen

Wenn ein Fehler auftritt, wird in der Spalte „Auftragsstatus“ ein Fehler gemeldet.

Die Fehler und möglichen Ursachen werden nachstehend aufgeführt:

<table id="table_BE2921B8E7C94B0EB88774321B8692F0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Fehler </th> 
   <th colname="col2" class="entry"> Mögliche Ursachen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> FTP Chdir-Fehler </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_79AB3EA974CC46A0A645A439BC612D88"> 
      <li id="li_4A6A5922275946908E06499E8EAAF18B"> Netzwerk- oder Zielserverfehler </li> 
      <li id="li_33393FF286624A63B12991DCE079841D">Problem mit der Lese-/Schreibberechtigung </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> FTP-Verbindungsfehler </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5F926078850D4495B83BC938395CAC6B"> 
      <li id="li_A72A357F6289438EA1A091AC4FD3A3D0"> Authentifizierungsproblem </li> 
      <li id="li_48532C78285E4DB6A47B1435A5FA549B"> Netzwerk- oder Zielserverfehler </li> 
      <li id="li_11DF6FA218CA48539C4561695234CA4D"> Problem mit der Lese-/Schreibberechtigung </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> FTP-Fehler </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_020BA1DC81F645FFABCAD07E51351D1E"> 
      <li id="li_8566EECEFD344BFDB638259474A8E8EA"> Datenträger voll oder Datenträgerkontingent überschritten </li> 
      <li id="li_15CD50ED54F846F79BFDF25359864C59"> Netzwerk- oder Zielserverfehler </li> 
      <li id="li_741A3315C0B940D3A9874F15C78B4F28"> Problem mit der Lese-/Schreibberechtigung </li> 
      <li id="li_49F707F7F65A443F8AC6E058E3D89B96"> Authentifizierungsproblem </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> FTP-Anmeldefehler </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F7F128ADF1FD4E9D8B79424A6432378E"> 
      <li id="li_68C377CAD50346B1B9937B77E7EB2AAD"> Authentifizierungsproblem </li> 
      <li id="li_7EA91C90FFC0493EA156292620EF1589"> Netzwerk- oder Zielserverfehler </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> FTP-Put-Fehler </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_760DA2CBD46B4C348BE3B7B43E803FD9"> 
      <li id="li_6578482722E14E998515B4B3EA370C44"> Datenträger voll oder Datenträgerkontingent überschritten </li> 
      <li id="li_342240DDD9D3423198C23123473D539C"> Netzwerk- oder Zielserverfehler </li> 
      <li id="li_44CEFE1D92A74842A6321C416637421F"> Problem mit der Lese-/Schreibberechtigung </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>