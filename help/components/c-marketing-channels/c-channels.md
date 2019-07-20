---
description: Hinzufügen oder Aktivieren von Marketingkanälen im Marketingkanal-Manager. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).
seo-description: Hinzufügen oder Aktivieren von Marketingkanälen im Marketingkanal-Manager. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).
seo-title: Verwalten von Marketingkanälen
solution: Analytics
subtopic: Marketingkanäle
title: Verwalten von Marketingkanälen
topic: Reports and Analytics
uuid: 9 d 367 bb 6-a 17 b -49 b 8-9 cd 5-24 fac 35 ae 982
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Verwalten von Marketingkanälen

Hinzufügen oder Aktivieren von Marketingkanälen im Marketingkanal-Manager. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).

## Manage marketing channels {#topic_45CF1C6A783B4F96ABF6317EAB6A854F}

Add or enable marketing channels in the [!UICONTROL Marketing Channel Manager]. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).

Beachten Sie bei der Erstellung von Kanälen die folgenden Richtlinien:

* Richten Sie in der Vorbereitung eine Liste aller Kanäle ein, so dass alle Besucherzugriffe in die richtigen Kanäle eingeordnet werden.
* Denken Sie daran, immer Kanäle in den Trefferkategorien [Intern](../../components/c-marketing-channels/c-faq.md#section_179A2BE5C8E24719A9E5C0DC09AF0947) und [Direkt](../../components/c-marketing-channels/c-faq.md#section_D0A1DD9D5EEF4A05A1CC81F9EADC074A) in die Liste aufzunehmen.

Der Zusatz von Kanälen in der [!UICONTROL Marketingkanal]-Seite erfolgt separat von der Regelerstellung in der Seite der [Marketingkanal-Verarbeitungsregeln](../../components/c-marketing-channels/t-rules.md#task_84EDE9F46F404CB9B7CA0537328CEE08). Bei der Regelerstellung verbinden Sie Regeln mit Kanälen.

## Hinzufügen von Marketingkanälen {#task_98C9D3F5DBBC4B198E0A9ED4D3891E03}

Fügen Sie im Marketingkanal-Manager Marketingkanäle hinzu.

>[!NOTE]
>
>Kanal kann nicht gelöscht werden. Wenn Sie einen Kanal nicht verwenden möchten, können Sie ihn deaktivieren oder umbenennen oder ihn zur späteren Verwendung aufbewahren.

1. Click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**.
1. Wählen Sie im [!UICONTROL „Report Suite Manager“] die Report Suite aus.

   Wenn Sie mehrere Report Suites auswählen, wählen Sie eine Vorlage aus, die die Einstellungen aus der Vorlage in die jeweiligen Report Suites kopiert.

   Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](../../components/c-marketing-channels/t-template.md#task_0DE0A320EDA94FC5A6E5912868B6E2DC).

1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Marketing Channels]** &gt; **[!UICONTROL Marketing Channel Manager]**.

   If your report suite does not have channels defined, the [Auto Setup](../../components/c-marketing-channels/c-channel-autosetup.md#topic_E9ABE9E9E71B4E40A4E7EA9AD2C0372B) page displays.

1. Klicken Sie auf der Seite [!UICONTROL Marketingkanal-Manager]**auf[!UICONTROL Kanal hinzufügen]**.

   Diese Option steht nicht zur Verfügung, wenn 25 Kanäle definiert wurden.

1. Click **[!UICONTROL Save.]**
1. To configure rules for the channel, click **[!UICONTROL Marketing Channel Processing Rules]**.

   See [Create Marketing Channel processing rules](../../components/c-marketing-channels/t-rules.md#task_84EDE9F46F404CB9B7CA0537328CEE08).

## Marketing Channel Manager - interface definitions {#reference_01779A2928054BF48339897D4033AFB9}

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
   <td colname="col1"> <p>Kanaltyp </p> </td> 
   <td colname="col2"> <p> Zeigt an, wie der Benutzer zu Ihrer Site gelangt ist. Sie können <span class="uicontrol">Online</span> oder <span class="uicontrol">Offline</span> auswählen. Online-Kanäle lassen sich z. B. für Besucher einsetzen, die über eine Suchmaschine oder E-Mail-Kampagne zu Ihrer Site gelangten. Offline-Kanäle gelten beispielsweise für Besucher, die Ihre Site durch Anzeigen in Zeitungen oder Zeitschriften fanden. Offlinekanäle beinhalten in der Regel Daten, die über Berichterstellungs-Data Sources importiert wurden. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/sc/datasources/" scope="external" format="http">Data Sources</a>. </p> <p>See <a href="../../components/c-marketing-channels/t-offline-data.md#task_FC96E6A48F0D4D37A79BD234E90DAA26" type="task" format="dita" scope="local"> Add Offline Data</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kanalfarbe </p> </td> 
   <td colname="col2"> <p>Die mit diesem Marketingkanal verbundene Farbe. Die Farbe stellt den Kanal im <span class="wintitle">Marketingkanal</span>bericht dar. </p> </td> 
  </tr> 
 </tbody> 
</table>

