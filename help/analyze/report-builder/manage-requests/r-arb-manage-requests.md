---
description: Feldbeschreibungen zur Verwaltung von Anforderungen in Report Builder.
title: Anforderungen verwalten – Definitionen
topic: Report builder
uuid: 01b21d0e-c870-4df8-95b9-f4aef1f4d16b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Anforderungen verwalten – Definitionen

Feldbeschreibungen zur Verwaltung von Anforderungen in Report Builder.

## Überblick {#section_75C288C945FA4781A4EDF806711A5660}

Die [!UICONTROL Request Manager] bietet eine detaillierte Ansicht des Status aller Anforderungen, die Sie für alle Arbeitsblätter oder nur für ein Arbeitsblatt der aktiven Arbeitsmappe erstellt haben. Sie können auch eine Anforderung hinzufügen, bearbeiten, aktualisieren und löschen (Funktionen, die normalerweise mit [!UICONTROL Request Wizard] und verknüpft sind), indem Sie mit der rechten Maustaste auf eine verfügbare Zelle im Excel-Arbeitsblatt klicken, die frühere Anforderungen enthält. [!UICONTROL Request Manager])

The [!UICONTROL Request Manager] displays when you click **[!UICONTROL Manage]** ( ![](assets/edit_request.gif) in the Report Builder toolbar.

>[!NOTE] Adobe Report Builder erzwingt Anforderungsabhängigkeiten nur innerhalb desselben Arbeitsblatts, nicht aber über Arbeitsblätter hinweg. Die Einschränkung auf Abhängigkeiten innerhalb eines einzigen Arbeitsblatts stellt eine zeitgerechte Ausführung sicher.

## Definitionen {#section_FD29D8614DE74F32A0027FA130F40304}

<table id="table_0880204181074BDBBA37E3DF2972A672"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Feld </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Alle Blätter </p> </td> 
   <td colname="col2"> <p>Die Anforderungen aus allen Arbeitsblättern der aktiven Arbeitsmappe werden angezeigt. Wenn Sie Anforderungen aus bestimmten Arbeitsblättern anzeigen möchten, müssen Sie diese Option deaktivieren. Wenn Sie diese Option deaktivieren, müssen Sie auf die Registerkarte für ein Arbeitsblatt am unteren Rand des Excel-Berichts klicken, um die zugehörigen Anforderungen im <span class="wintitle">Anforderungs-Manager</span> anzuzeigen. Die Beschriftung neben dem Kontrollkästchen gibt an, welches Arbeitsblatt der Arbeitsmappe derzeit den Fokus hat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sheet </p> </td> 
   <td colname="col2"> <p>Zeigt den Namen der Arbeitsblätter in der Arbeitsmappe an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Suite </p> </td> 
   <td colname="col2"> <p>Zeigt den Namen der Report Suite an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumsbereich </p> </td> 
   <td colname="col2"> <p>Zeigt den angegebenen Datumsbereich des Berichts an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Granularität </p> </td> 
   <td colname="col2"> <p>Gibt die Granularität der Anforderung an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Letzte Ausführung </p> </td> 
   <td colname="col2"> <p>Es wird das Datum angezeigt, an dem die Anforderung zuletzt von Report Builder verarbeitet wurde. In dieser Tabelle werden in der Spalte <span class="wintitle">Letzte Ausführung</span> auch gegebenenfalls erforderliche diagnostische Meldungen angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fügen Sie </p> </td> 
   <td colname="col2"> <p>Zeigt das Dialogfeld Anforderungs-Assistent an. Siehe <a href="/help/analyze/report-builder/data-requests/t-create-a-data-request.md"   >Eine Datenanforderung erstellen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorlage </p> </td> 
   <td colname="col2"> <p> (oder Mehrere Anforderungen bearbeiten) Bearbeitet eine ausgewählte Anforderung. Das System zeigt den <span class="wintitle">Anforderungs-Assistenten</span> an. Siehe <a href="/help/analyze/report-builder/manage-requests/t-edit-multiple-requests.md"   > Mehrere Anforderungen bearbeiten</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Löschen </p> </td> 
   <td colname="col2"> <p>Löscht Anforderungen. Sie können mehrere Anforderungen gleichzeitig löschen. Sie können eine Anforderung auch in der Liste löschen, indem Sie die Anforderung auswählen und auf der Tastatur die Taste Löschen drücken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Alle auswählen </p> </td> 
   <td colname="col2"> <p>Wählen Sie alle Anforderungen aus. Die Anzahl der von Ihnen ausgewählten Anforderungen wird im <span class="wintitle">Anforderungs-Manager</span> am unteren Ende der Anforderungsliste angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Von Zelle </p> </td> 
   <td colname="col2"> <p>Ruft Daten für eine Anforderung aus dem Arbeitsblatt ab. Wenn eine Anforderung mit der aktuell ausgewählten Zelle im aktiven Arbeitsblatt verknüpft ist, wird die zugehörige Anforderung in der Liste ausgewählt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Aktualisieren </p> </td> 
   <td colname="col2"> <p>Aktualisiert eine einzelne Anforderung oder eine Auswahl von Anforderungen. (See <a href="/help/analyze/report-builder/manage-requests/t-refresh-a-request.md"   > Refresh a Request</a>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Liste aktualisieren </p> </td> 
   <td colname="col2"> <p>Aktualisiert alle angezeigten Anforderungen. Die Aktualisierung aller Anforderungen in Ihren Bericht mit den Daten vom Server nimmt um so mehr Zeit in Anspruch, je komplexer die Anforderungen in dem Bericht sind. Bei sehr großen Berichten kann die Aktualisierung aller Anforderungen mehrere Minuten in Anspruch nehmen. Aus diesem Grund könnte es von Vorteil sein, dringende Anforderungen möglichst einzeln zu aktualisieren und <span class="wintitle">Alle aktualisieren</span> erst zu einem späteren Zeitpunkt zu wählen, wenn keine Dringlichkeit geboten ist. </p> <p> <p>Hinweis: Es wird empfohlen, dass Sie bei der Aktualisierung einer Arbeitsmappe mit mehreren Anforderungen die Ergebnisse öfter im <span class="wintitle">Anforderungs-Manager</span> überprüfen. Wenn ein Anforderungsfehler auftritt, hilft Ihnen die Fehlermeldung in der Spalte "Diagnose"bei der Identifizierung der Fehlerquelle. Während in den meisten Fällen eine Fehlermeldung angezeigt wird, wenn eine Anforderung fehlschlägt, beachten Sie, dass gelegentlich keine Fehlermeldung generiert wird. Möglicherweise werden die Daten in einer Zelle, die einen Verweis enthält, durch eine Aktualisierung nicht aktualisiert oder die Daten aus der Zelle entfernt. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

