---
description: Fügen Sie im Marketing-Kanal-Manager Marketingkanäle hinzu oder aktivieren Sie sie. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).
subtopic: Marketing channels
title: Marketing-Kanäle verwalten
topic: Reports and analytics
uuid: 9d367bb6-a17b-49b8-9cd5-24fac35ae982
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Marketing-Kanäle verwalten

Fügen Sie im Marketing-Kanal-Manager Marketingkanäle hinzu oder aktivieren Sie sie. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).

Beachten Sie bei der Erstellung von Kanälen die folgenden Richtlinien:

* Richten Sie in der Vorbereitung eine Liste aller Kanäle ein, so dass alle Besucherzugriffe in die richtigen Kanäle eingeordnet werden.
* Denken Sie daran, immer Kanäle in den Trefferkategorien [Intern](/help/components/c-marketing-channels/c-faq.md) und [Direkt](/help/components/c-marketing-channels/c-faq.md) in die Liste aufzunehmen.

Der Zusatz von Kanälen in der [!UICONTROL Marketingkanal]-Seite erfolgt separat von der Regelerstellung in der Seite der [Marketingkanal-Verarbeitungsregeln](/help/components/c-marketing-channels/t-rules.md). Bei der Regelerstellung verbinden Sie Regeln mit Kanälen.

## Hinzufügen von Marketingkanälen {#add-mktg-channels}

Fügen Sie im Marketingkanal-Manager Marketingkanäle hinzu.

> [!NOTE] Ein Kanal kann nicht gelöscht werden. Wenn Sie einen Kanal nicht verwenden möchten, können Sie ihn deaktivieren oder umbenennen oder ihn zur späteren Verwendung aufbewahren.

1. Klicken Sie auf **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Wählen Sie im [!UICONTROL „Report Suite Manager“] die Report Suite aus.

   Wenn Sie mehrere Report Suites auswählen, wählen Sie eine Vorlage aus, die die Einstellungen aus der Vorlage in die jeweiligen Report Suites kopiert.

   Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](/help/components/c-marketing-channels/t-template.md).

1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Marketing-Kanäle]** &gt; **[!UICONTROL Marketing-Kanal-Manager]**.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [Automatisches Setup](/help/components/c-marketing-channels/c-channel-autosetup.md) angezeigt.

1. Klicken Sie auf der Seite [!UICONTROL Marketingkanal-Manager]**auf[!UICONTROL Kanal hinzufügen]**.

   Diese Option steht nicht zur Verfügung, wenn 25 Kanäle definiert wurden.

1. Klicken Sie auf **[!UICONTROL Speichern.]**
1. Klicken Sie zur Regelkonfiguration für den Kanal auf **[!UICONTROL Marketing-Kanal-Verarbeitungsregeln]**.

   Weitere Informationen finden Sie unter [Einrichten von Marketing-Kanal-Verarbeitungsregeln](/help/components/c-marketing-channels/t-rules.md).

## Marketing-Kanal-Manager – Benutzeroberflächendefinitionen {#mktg-channel-mgr}

Felddefinitionen für die Seite [!UICONTROL Marketingkanal-Manager].

<table id="table_C18A0F1C9E214EB585A29801BA2400F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Feld </p> </th> 
   <th colname="col2" class="entry"> <p>Definition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aktiviert </p> </td> 
   <td colname="col2"> <p> Aktiviert oder deaktiviert den Marketingkanal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kanalname </p> </td> 
   <td colname="col2"> <p>Benutzerfreundlicher Name des Marketingkanals. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Last Touch-Kanal außer Kraft setzen </p> </td> 
   <td colname="col2"> <p> Ermöglicht Ihnen, je nach Bedarf einen vorhandenen, beständigen Last Touch-Kanal durch den gewählten Kanal außer Kraft zu setzen. Wenn Sie diese Option auswählen, könnte jeder beliebige Kanal (einschließlich Direkt und Intern) einen vorhandenen Last Touch-Kanal außer Kraft setzen. Dies führt dazu, dass Konversionen den falschen Kanälen gutgeschrieben werden. Diese Option kann beispielsweise sicherstellen, dass dem direkten Kanal keine Konversionen gutgeschrieben werden, wenn der Benutzer zuvor über den Kanal Kostenlose Suche angeworben wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kanalinseln </p> </td> 
   <td colname="col2"> <p>Ermöglicht die Unterteilung des Kanals nach diesem Wert. Sie können mögliche Kanalunterteilungen (Sub-Kanäle) bei der Erstellung von Marketingkanal-Classifications hinzufügen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Typ </p> </td> 
   <td colname="col2"> <p> Zeigt an, wie der Benutzer zu Ihrer Site gelangt ist. Sie können <span class="uicontrol">Online</span> oder <span class="uicontrol">Offline</span> auswählen. Online-Kanäle lassen sich z. B. für Besucher einsetzen, die über eine Suchmaschine oder E-Mail-Kampagne zu Ihrer Site gelangten. Offline-Kanäle gelten beispielsweise für Besucher, die Ihre Site durch Anzeigen in Zeitungen oder Zeitschriften fanden. Offlinekanäle beinhalten in der Regel Daten, die über Berichterstellungs-Data Sources importiert wurden. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/sc/datasources/"  >Data Sources</a>. </p> <p>Weitere Informationen finden Sie unter <a href="/help/components/c-marketing-channels/t-offline-data.md"   >Hinzufügen von Offline-Daten</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kanalfarbe </p> </td> 
   <td colname="col2"> <p>Die mit diesem Marketingkanal verbundene Farbe. Die Farbe stellt den Kanal im <span class="wintitle">Marketingkanal</span>bericht dar. </p> </td> 
  </tr> 
 </tbody> 
</table>

