---
description: Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.
seo-description: Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.
seo-title: Datenanforderung planen
solution: Analytics
title: Datenanforderung planen
topic: ReportBuilder
uuid: f 6 d 8 c 90 f-e 185-4 d 60-8035-f 20 f 74 bfcd 89
translation-type: tm+mt
source-git-commit: ed8cfa41a2495c884f1096ea54624820bf3a9e07

---


# Arbeitsmappen planen

Sie können Arbeitsmappen planen, erweiterte Bereitstellungsoptionen festlegen, Empfänger angeben und den Planverlauf anzeigen. Mit erweiterten Auslieferungsoptionen können Sie Arbeitsmappen konfigurieren, die Sie zu einem bestimmten Zeitpunkt oder in Intervallen senden möchten. Sie können auch das Dateiformat angeben, in dem die Arbeitsmappe gesendet werden soll.

For example, you can schedule workbooks to be delivered immediately or on a recurring schedule, and specify the file format in [!DNL Advanced Delivery Options]. Die maximale Dateigröße beträgt 5 MB für einen Arbeitsmappen-Upload.

Additionally, after you create a workbook schedule in Report Builder, you can view and edit the schedule in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Reports]**. (Siehe [Berichtsplanung und -verteilung](/help/analyze/reports-analytics/scheduling.md) in der Hilfe zu Reports &amp; Analysen.)

>[!NOTE]
>
>Zum Planen einer Arbeitsmappe muss Excel 2007 oder das Compatibility Pack installiert sein. Pro Reportbuilder-Lizenz können maximal 10 geplante Arbeitsmappen verwendet werden. Jedoch können Sie diese Zahl erhöhen, indem Sie bei anderen Lizenzen die benötigte Menge an Arbeitsmappen wegnehmen. To do so, go to **[!UICONTROL Admin]** &gt; **[!UICONTROL Company Settings]** &gt; **[!UICONTROL Report Builder Reports]**. Eine Arbeitsmappe, die geplant (oder in die Arbeitsmappen-Bibliothek hochgeladen) wurde und in über 28 Monaten nicht weiter verwendet (aktualisiert, ersetzt) wurde, wird gelöscht.

>[!NOTE]
>
>Die vom Benutzer eingegebene "Auslieferungszeit" /" Tageszeit" gibt den Zeitpunkt an, zu dem die Arbeitsmappe mit der Verarbeitung beginnen soll, nicht den Zeitpunkt, zu dem sie tatsächlich bereitgestellt wird. Die tatsächliche Zeit, an der die Arbeitsmappe bereitgestellt wird, basiert hauptsächlich darauf, wie lange es dauert (komplexe und große Arbeitsmappen verarbeiten die Verarbeitung länger als einfache Arbeitsmappen). Wenn eine Arbeitsmappe z. B. 15 Minuten zur Verarbeitung benötigt, beträgt die tatsächliche Bereitstellungszeit mindestens 15 Minuten nach der ursprünglich angegebenen "Lieferzeit" /" Tageszeit" .
>Darüber hinaus gibt es eine Reihe weiterer Faktoren, die die Verzögerung noch erhöhen können, bevor die Arbeitsmappe tatsächlich bereitgestellt wird:
>
> * **Die gleichzeitige Ausführung verschiedener Zeitpläne desselben Typs** kann das System überladen. Das Planungssystem erlaubt nur einige (bis 10) Arbeitsmappen eines Typs, die gleichzeitig ausgeführt werden sollen. Wenn also mehr als 5-10 gleichzeitig geplant werden, müssen einige andere Arbeitsmappen auf die Fertigstellung warten, bevor sie mit der Verarbeitung beginnen können. Dieses Problem kann reduziert werden, indem die Arbeitsmappen eines Unternehmens zu stagnierenden Zeiten außerhalb des Tages oder der Stunde eingeplant werden und nicht gleichzeitig.
> * Abgesehen vom jeweiligen Arbeitsmappen-Typ werden Arbeitsmappen auch dann gewartet, wenn das Unternehmen **über 15-20 jedes beliebigen Arbeitsmappen-Typs gleichzeitig geplant hat (für alle anderen Arbeitsmappen-Typen)**. Dies kann durch die plötzliche Zeitplanung reduziert werden, anstatt dass viele Ausführungsvorgänge gleichzeitig ausgeführt werden.
> * **Probleme in Downstream Services** , auf die der Scheduler angewiesen ist, können auch die Bereitstellung von Arbeitsmappen beeinträchtigen. Wenn Sie beispielsweise die apis unabhängig verwenden, um Arbeitsmappen auszuführen und die API-Anforderungswarteschlange auszufüllen, können Ihre geplanten Arbeitsmappen langsam bereitgestellt werden, während Sie auf diese Ressource konkurrieren.
> * **Die Report Suite-Latenz** (Verzögerung bei der Datenerfassung) kann auch einige geplante Arbeitsmappen verzögern.


## Arbeitsmappe planen

1. Erstellen und speichern Sie eine Arbeitsmappe.
1. On the Report Builder Toolbar, click **[!UICONTROL Schedule]**.

   Die Registerkarte „[!UICONTROL Terminierte Berichte]“ enthält eine Zusammenfassung aller von Ihnen erstellten Aufgaben sowie die Anzahl der verbleibenden Aufgaben.
1. Klicken Sie auf de Registerkarte **** Geplante Berichte auf **[!UICONTROL Neu]**.
1. Das Fenster „Planungs-Assistent – Grundlegend“ wird angezeigt:

   ![](assets/simple-schedule-wizard.png)

1. Konfigurieren Sie im Fenster [!UICONTROL Planungs-Assistent – Grundlegend] die folgenden Optionen:

| Feld | Beschreibung |
|--- |--- |
| Bericht auswählen | Der Name der Arbeitsmappe. Bei neuen terminierten Berichten erscheint in diesem Feld automatisch der Name der aktiven Arbeitsmappe. |
| Auswählen | Hierdurch wird die Seite Bericht auswählen angezeigt. Sie können einen Bericht vom Server (wo alle früher geplanten Arbeitsmappen gespeichert sind) oder von Ihrem lokalen Computer auswählen. Wenn Sie einen Arbeitsmappe von der lokalen Festplatte im .xls-Format auswählen, wandelt das System sie in eine .xlsx-Datei um. Im Rahmen der Konversion wird die Datei in Excel geöffnet und aktiviert. Wenn die für den terminierten Bericht ausgewählte Arbeitsmappe denselben Dateinamen wie die derzeit in Excel geöffnete Arbeitsmappe hat, wählt das System statt der vorher hochgeladenen Datei die lokale Datei. Wenn Sie einen Bericht aus dem Repository planen, wird eine Kopie der Arbeitsmappe auf dem Server erstellt, wobei der Dateiname mit 1 aktualisiert wird. Der neu erstellte geplante Bericht verwendet die kopierte Arbeitsmappe. |
| Anpassen | Ermöglicht Ihnen, das Datumsformat anzupassen. |
| An | Zeigt Ihr gegebenenfalls vorhandenes Outlook-Adressbuch an. |
| Senden an: E-Mail | Der E-Mail-Empfänger der Arbeitsmappe. |
| Senden an: Veröffentlichungsliste | Hiermit zeigen Sie eine Liste der in Ihrem Unternehmen verfügbaren Veröffentlichungslisten an. |
| Power BI | Weitere Informationen finden Sie unter [Arbeitsmappe in Microsoft Power BI veröffentlichen](/help/analyze/report-builder/c-publish-power-bi/integration-power-bi.md). |
| Betreff | Eine benutzerdefinierte Beschreibung. |
| Zeitplan | Hier können Sie angeben, wann die Arbeitsmappe gesendet werden soll. (sofort, stündlich, täglich, wöchentlich oder jährlich). |

## Erweiterte Auslieferungsoptionen

1. Click **[!UICONTROL Advanced Delivery Options]** to configure file and publishing options:

| Feld | Beschreibung |
|--- |--- |
| Registerkarte **Zeitplan** |  |
| Zeitpunkt der Bereitstellung | Sie können die Arbeitsmappe sofort oder für einen späteren Zeitpunkt planen. Die Uhrzeit entspricht der Zeitzoneneinstellung auf Ihrem Computer. |
| Wiederholungsmuster | Sendet die Arbeitsmappe auf Grundlage Ihrer Auswahl. |
| Bereich der Wiederholung | Hier können Sie angeben, wann der Empfang der Arbeitsmappe beginnen und enden soll. Hinweis: Beim Planen einer Arbeitsmappe am ersten Tag eines aktuellen Zeitraums (Woche, Monat, Quartal oder Jahr) werden nur Daten für den ersten Tag zurückgegeben. |
| Registerkarte **Dateioptionen** |  |
| Dateiformat | Hier können Sie als Bereitstellungsformat Excel 2007 (.xlsx) oder 2003 (.xls), .pdf, .csv, .mht, .txt oder .xml auswählen. |
| Dateiziel | Hier wird die E-Mail- oder FTP-Adresse angegeben. Die verfügbaren Optionen wechseln ja nach der bisherigen Auswahl. Für FTP müssen Sie sicherstellen, dass der Host extern verfügbar ist. |
| Veröffentlichungsliste | Wenn Sie die geplante Arbeitsmappe an mehrere Veröffentlichungslisten senden, wird die Arbeitsmappe einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist. |
| Sprache des Dateiinhalts | Gibt die Sprache an, die für das Anschreiben verwendet werden soll. Zur Auswahl stehen Chinesisch (vereinfacht oder traditionell), Deutsch, Französisch, Japanisch, Koreanisch, Portugiesisch (Brasilien) oder Spanisch. |
| Registerkarte **Veröffentlichungsoptionen** |  |
| In Power BI veröffentlichen | <ul><li>Arbeitsmappe in Power BI veröffentlichen</li><li>Alle ReportBuilder-Anforderungen als Power BI-Datensätze veröffentlichen</li><li>Alle formatierten Tabellen als Power BI-Datensätze veröffentlichen</li></ul> |
| Diesen Power BI-Bericht bezeichnen als | Bezeichnungsdetails |

1. Click **[!UICONTROL OK]**, then click **[!UICONTROL Exit]**.

   Report Builder displays the scheduled workbook in the [Scheduled Task Manager](../../analyze/report-builder/r-arb-scheduled-reports.md#section_69306B8D833F4DF7BBFA53753B0E6C31).

