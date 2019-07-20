---
description: Bevor Sie anfangen, Virtual Report Suites zu erstellen, sollten Sie folgende Aspekte berücksichtigen.
keywords: Virtual Report Suite
seo-description: Bevor Sie anfangen, Virtual Report Suites zu erstellen, sollten Sie folgende Aspekte berücksichtigen.
seo-title: Virtuelle Report Suites erstellen
solution: Analytics
title: Virtuelle Report Suites erstellen
topic: Reports and Analytics
uuid: 022 a 6656-808 e -4 c 92-b 7 ec -4 d 2 a 42 e 84 fa 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Virtuelle Report Suites erstellen

Bevor Sie anfangen, Virtual Report Suites zu erstellen, sollten Sie folgende Aspekte berücksichtigen.

* Nicht-Admin-Benutzer können den Virtual Report Suite Manager nicht sehen.
* Virtual Report Suites können nicht freigegeben werden. Die Freigabe erfolgt über Gruppen/Berechtigungen.
* Im Virtual Report Suite Manager sehen Sie nur Ihre eigenen Virtual Report Suites. Sie müssen auf „Alle anzeigen“ klicken, um die aller anderen anzuzeigen.

1. Navigate to **[!UICONTROL Components]** &gt; **[!UICONTROL Virtual Report Suites]**.
1. Click **[!UICONTROL Add +]**.

   ![](assets/new_vrs.png)

1. Füllen Sie die Felder aus:

<table id="table_0F85B56480BB46CBA5BE236BBD70156D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Name </td> 
   <td colname="col2"> <p>Der Name der Virtual Report Suite wird nicht von der übergeordneten Report Suite geerbt und sollte eindeutig vergeben werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beschreibung </td> 
   <td colname="col2"> <p>Fügen Sie eine gute Beschreibung der Vorteile für Ihre geschäftlichen Benutzer hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tags </td> 
   <td colname="col2"> <p>Sie können Tags hinzufügen, um Ihre Report Suites zu organisieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gruppen </td> 
   <td colname="col2"> <p>Wählen Sie die Berechtigungsgruppen aus, die Zugriff auf diese VRS besitzen sollen. (Sie können Gruppenberechtigungen auch unter <span class="ignoretag"><span class="uicontrol">Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span></span> verwalten.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Übergeordnete Report Suite </td> 
   <td colname="col2"> <p>Die Report Suite, von der diese Virtual Report Suite die folgenden Einstellungen erbt. Die meisten Service-Levels und Funktionen (z. B. eVar-Einstellungen, Verarbeitungsregeln, Classifications usw.) werden vererbt. Möchten Sie Änderungen diesen geerbten Einstellungen einer VRS vornehmen, müssen Sie die übergeordnete Report Suite anpassen (<span class="ignoretag"><span class="uicontrol">Admin</span> &gt; <span class="uicontrol">Report Suites</span></span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zeitzone </td> 
   <td colname="col2"> <p>Die Auswahl einer Zeitzone ist optional. </p> <p>Wenn Sie eine Zeitzone auswählen, wird diese zusammen mit der VRS gespeichert. Wenn Sie keine Zeitzone auswählen, wird die Zeitzone der übergeordneten Report Suite verwendet. </p> <p>Bei der Bearbeitung einer VRS erscheint die mit ihr gespeicherte Zeitzone in einem Dropdown-Auswahlmenü. Wenn die VRS erstellt wurde, bevor Zeitzonen unterstützt wurden, wird die Zeitzone der übergeordneten Report Suite in der Dropdownauswahl angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Segmente </td> 
   <td colname="col2"> <p>Sie können nur ein Segment hinzufügen oder Sie können <a href="https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_stack.html" format="https" scope="external">Segmente stapeln</a>. </p> <p> <p>Hinweis: Beim Stapeln von zwei Segmenten werden diese durch eine AND-Anweisung verbunden. Dies kann nicht in eine ODER-Anweisung geändert werden. </p> </p> <p>Wenn Sie versuchen, ein Segment zu löschen oder zu ändern, das aktuell in einer Virtual Report Suite verwendet wird, wird eine Warnung angezeigt. </p> </td> 
  </tr> 
 </tbody> 
</table>

