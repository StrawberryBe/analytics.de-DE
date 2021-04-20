---
description: Feldbeschreibungen zur Verwaltung von Anforderungen in Report Builder.
title: Anforderungen verwalten – Definitionen
uuid: 01b21d0e-c870-4df8-95b9-f4aef1f4d16b
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 99%

---


# Anforderungen verwalten – Definitionen

Feldbeschreibungen zur Verwaltung von Anforderungen in Report Builder.

## Überblick {#section_75C288C945FA4781A4EDF806711A5660}

Der [!UICONTROL Anforderungs-Manager] bietet eine detaillierte Übersicht der von Ihnen erstellten Anforderungen, entweder aller Anforderungen in allen Arbeitsblättern oder nur der Anforderungen der aktiven Arbeitsmappe. Sie können außerdem Anforderungen hinzufügen, bearbeiten, aktualisieren und löschen (also typische Funktionen des [!UICONTROL Anforderungs-Assistenten] bzw. des [!UICONTROL Anforderungs-Managers] ausführen), indem Sie mit der rechten Maustaste auf eine verfügbare Zelle im Excel-Arbeitsblatt klicken, die bereits erstellte Anforderungen enthält.

Der [!UICONTROL Anforderungs-Manager] wird angezeigt, wenn Sie auf **[!UICONTROL Verwalten]** klicken (![](assets/edit_request.gif) in der Report Builder-Symbolleiste).

>[!NOTE]
>
>Adobe Report Builder erzwingt Anforderungsabhängigkeiten nur innerhalb desselben Arbeitsblatts, nicht aber über Arbeitsblätter hinweg. Die Einschränkung auf Abhängigkeiten innerhalb eines einzigen Arbeitsblatts stellt eine zeitgerechte Ausführung sicher.

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
   <td colname="col2"> <p>Die Anforderungen aus allen Arbeitsblättern der aktiven Arbeitsmappe werden angezeigt. Wenn Sie Anforderungen aus bestimmten Arbeitsblättern anzeigen möchten, müssen Sie diese Option deaktivieren. Wenn Sie diese Option deaktivieren, müssen Sie auf die Registerkarte für ein Arbeitsblatt am unteren Rand des Excel-Berichts klicken, um die zugehörigen Anforderungen im <span class="wintitle">Anforderungs-Manager</span> anzuzeigen. Der Bezeichnung neben dem Kontrollkästchen können Sie entnehmen, welches Arbeitsblatt der Arbeitsmappe aktuell im Fokus ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Blatt </p> </td> 
   <td colname="col2"> <p>Der Name der Arbeitsblätter in der Arbeitsmappe wird angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Report Suite </p> </td> 
   <td colname="col2"> <p>Der Name der Report Suite wird angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datumsbereich </p> </td> 
   <td colname="col2"> <p>Der für den Bericht angegebene Datumsbereich wird angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Granularität </p> </td> 
   <td colname="col2"> <p>Die Granularität des Berichts wird angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Letzter Lauf </p> </td> 
   <td colname="col2"> <p>Es wird das Datum angezeigt, an dem die Anforderung zuletzt von Report Builder verarbeitet wurde. In dieser Tabelle werden in der Spalte <span class="wintitle">Letzte Ausführung</span> auch gegebenenfalls erforderliche diagnostische Meldungen angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Fügen Sie </p> </td> 
   <td colname="col2"> <p>Hierdurch wird der Anforderungs-Assistent angezeigt. Siehe <a href="/help/analyze/report-builder/data-requests/t-create-a-data-request.md"   >Eine Datenanforderung erstellen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vorlage </p> </td> 
   <td colname="col2"> <p> (bzw. Mehrere Anforderungen bearbeiten) Eine ausgewählte Anforderung wird bearbeitet. Das System zeigt den <span class="wintitle">Anforderungs-Assistenten</span> an. Siehe <a href="/help/analyze/report-builder/manage-requests/t-edit-multiple-requests.md"   > Mehrere Anforderungen bearbeiten</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Löschen </p> </td> 
   <td colname="col2"> <p>Zum Löschen von Anforderungen. Sie können mehrere Anforderungen gleichzeitig löschen. Sie können außerdem eine Anforderung in der Liste löschen, indem Sie die Anforderung auswählen und auf die Löschtaste auf der Tastatur drücken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Alle auswählen </p> </td> 
   <td colname="col2"> <p>Es werden alle Anforderungen ausgewählt. Die Anzahl der von Ihnen ausgewählten Anforderungen wird im <span class="wintitle">Anforderungs-Manager</span> am unteren Ende der Anforderungsliste angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Von Zelle </p> </td> 
   <td colname="col2"> <p>Ruft Daten für eine Anforderung aus dem Arbeitsblatt ab. Wenn die Anforderung mit der aktuell ausgewählten Zelle im aktiven Arbeitsblatt verknüpft ist, wird die zugehörige Anforderung in der Anforderungsliste hervorgehoben dargestellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Aktualisieren </p> </td> 
   <td colname="col2"> <p>Aktualisierung einer einzelnen Anforderung oder einer Auswahl von Anforderungen. (Siehe <a href="/help/analyze/report-builder/manage-requests/t-refresh-a-request.md"   > Eine Anforderung aktualisieren</a>.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Liste aktualisieren </p> </td> 
   <td colname="col2"> <p>Alle angezeigten Anforderungen werden aktualisiert. Die Aktualisierung aller Anforderungen in Ihren Bericht mit den Daten vom Server nimmt um so mehr Zeit in Anspruch, je komplexer die Anforderungen in dem Bericht sind. Bei sehr großen Berichten kann die Aktualisierung aller Anforderungen mehrere Minuten in Anspruch nehmen. Aus diesem Grund könnte es von Vorteil sein, dringende Anforderungen möglichst einzeln zu aktualisieren und <span class="wintitle">Alle aktualisieren</span> erst zu einem späteren Zeitpunkt zu wählen, wenn keine Dringlichkeit geboten ist. </p> <p> <p>Hinweis: Es wird empfohlen, dass Sie bei der Aktualisierung einer Arbeitsmappe mit mehreren Anforderungen die Ergebnisse öfter im <span class="wintitle">Anforderungs-Manager</span> überprüfen. Wenn es bei einer Anforderung zu einem Fehler kommt, hilft Ihnen die Fehlermeldung in der Spalte mit den diagnostischen Meldungen dabei, die Ursache näher einzugrenzen. Wenn eine Anforderung nicht ausgeführt werden kann, wird in der Regel eine Fehlermeldung ausgegeben, dies kann aber gelegentlich auch nicht der Fall sein. Möglicherweise fällt Ihnen auf, dass die Daten in einer Zelle, die einen Verweis enthält, sich bei einer Aktualisierung nicht ändern oder dass die Daten in einer Zelle durch eine Aktualisierung verschwinden. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

