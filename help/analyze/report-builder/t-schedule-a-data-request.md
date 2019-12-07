---
description: Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.
title: Planen einer Datenanforderung
topic: Report builder
uuid: f6d8c90f-e185-4d60-8035-f20f74bfcd89
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Arbeitsmappen planen

Sie können Arbeitsmappen planen, erweiterte Auslieferungsoptionen festlegen, Empfänger angeben und den Planverlauf anzeigen. Mit den erweiterten Auslieferungsoptionen können Sie Arbeitsmappen konfigurieren, die Sie zu einem bestimmten Zeitpunkt oder in bestimmten Abständen senden möchten. Sie können auch das Dateiformat angeben, in dem die Arbeitsmappe gesendet werden soll.

For example, you can schedule workbooks to be delivered immediately or on a recurring schedule, and specify the file format in [!DNL Advanced Delivery Options]. Die maximale Dateigröße beträgt 5 MB beim Hochladen einer Arbeitsmappe.

Additionally, after you create a workbook schedule in Report Builder, you can view and edit the schedule in **[!UICONTROL Analytics]** &gt; **[!UICONTROL Reports]**. (Siehe [Berichtsplanung und -verteilung](/help/analyze/reports-analytics/scheduling.md) in der Hilfe zu Reports &amp; Analysen.)

> [!NOTE] Sie müssen Excel 2007 oder das Kompatibilitätspaket installiert haben, um eine Arbeitsmappe planen zu können. Pro ReportBuilder-Lizenz können maximal 10 geplante Arbeitsmappen verwendet werden. Jedoch können Sie diese Zahl erhöhen, indem Sie bei anderen Lizenzen die benötigte Menge an Arbeitsmappen wegnehmen. To do so, go to **[!UICONTROL Admin]** &gt; **[!UICONTROL Company Settings]** &gt; **[!UICONTROL Report Builder Reports]**. Eine Arbeitsmappe, die geplant (oder in die Arbeitsmappen-Bibliothek hochgeladen) wurde und in mehr als 28 Monaten nicht angefasst (aktualisiert, ersetzt) wurde, wird gelöscht.

> [!NOTE] Die vom Benutzer eingegebene "Bereitstellungszeit"/"Tageszeit"gibt den Zeitpunkt an, zu dem die Arbeitsmappe mit der Verarbeitung beginnen soll, und nicht den Zeitpunkt, zu dem sie tatsächlich bereitgestellt wird. Die tatsächliche Bereitstellungszeit der Arbeitsmappe hängt in erster Linie davon ab, wie lange die Verarbeitung dauert (komplexe und große Arbeitsmappen benötigen mehr Verarbeitungszeit als einfachere Arbeitsmappen). Wenn die Verarbeitung einer Arbeitsmappe z. B. 15 Minuten dauert, beträgt die tatsächliche Auslieferungszeit mindestens 15 Minuten nach der ursprünglich angegebenen "Auslieferungszeit"/"Tageszeit".
>Darüber hinaus gibt es eine Reihe weiterer Faktoren, die die Verzögerung vor der tatsächlichen Auslieferung der Arbeitsmappe weiter erhöhen können:
>
> * **Das gleichzeitige** Ausführen vieler verschiedener Zeitpläne desselben Typs kann das System überladen. Das Planungssystem erlaubt nur die gleichzeitige Ausführung einiger (5-10) Arbeitsmappen eines beliebigen Typs. Wenn also mehr als 5-10 gleichzeitig geplant sind, müssen einige sofort warten, bis andere Arbeitsmappen fertig sind, bevor sie mit der Verarbeitung beginnen können. Dieses Problem kann durch die Planung der Arbeitsmappen eines Unternehmens zu gestaffelten Zeiten über den ganzen Tag oder die Stunde hinweg und nicht gleichzeitig behoben werden.
> * Neben dem jeweiligen Arbeitsmappentyp warten Arbeitsmappen auch dann in der Warteschlange, wenn das Unternehmen **mehr als 15-20 Arbeitsmappen aller Art gleichzeitig geplant hat (über alle verschiedenen Arbeitsmappentypen)**. Dies kann durch atemberaubende Zeitpläne abgemildert werden, anstatt dass viele gleichzeitig ausgeführt werden.
> * **Probleme bei den nachgelagerten Diensten** , auf denen der Scheduler basiert, können sich auch auf die Bereitstellung von Arbeitsmappen auswirken. Wenn Sie beispielsweise unabhängig voneinander die APIs zum Ausführen von Arbeitsmappen und zum Ausfüllen der API-Anforderungswarteschlange verwenden, werden Ihre geplanten Arbeitsmappen möglicherweise langsam bereitgestellt, während Sie um diese Ressource konkurrieren.
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
| Auswählen | Hierdurch wird die Seite Bericht auswählen angezeigt. Sie können einen Bericht vom Server (wo alle früher geplanten Arbeitsmappen gespeichert sind) oder von Ihrem lokalen Computer auswählen. Wenn Sie einen Arbeitsmappe von der lokalen Festplatte im .xls-Format auswählen, wandelt das System sie in eine .xlsx-Datei um. Im Rahmen der Konversion wird die Datei in Excel geöffnet und aktiviert. Wenn die für den terminierten Bericht ausgewählte Arbeitsmappe denselben Dateinamen wie die derzeit in Excel geöffnete Arbeitsmappe hat, wählt das System statt der vorher hochgeladenen Datei die lokale Datei. Wenn Sie einen Bericht aus dem Zeitplan-Repository auswählen, wird eine Kopie der Arbeitsmappe auf dem Server erstellt, deren Dateiname mit 1 aktualisiert wird. Der neu erstellte terminierte Bericht verwendet die kopierte Arbeitsmappe. |
| Anpassen | Ermöglicht Ihnen, das Datumsformat anzupassen. |
| Hierzu | Zeigt Ihr gegebenenfalls vorhandenes Outlook-Adressbuch an. |
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
| Zeitpunkt der Bereitstellung | Damit können Sie die Arbeitsmappe sofort oder für einen späteren Zeitpunkt planen. Die Uhrzeit entspricht der Zeitzoneneinstellung auf Ihrem Computer. |
| Wiederholungsmuster | Sendet die Arbeitsmappe basierend auf Ihrer Auswahl. |
| Bereich der Wiederholung | Hier können Sie angeben, wann der Empfang der Arbeitsmappe gestartet und beendet werden soll.   Hinweis:  Beim Planen einer Arbeitsmappe am ersten Tag eines aktuellen Zeitraums (Woche, Monat, Quartal oder Jahr) werden nur Daten für den ersten Tag zurückgegeben. |
| Registerkarte **Dateioptionen** |  |
| Dateiformat | Hier können Sie als Bereitstellungsformat Excel 2007 (.xlsx) oder 2003 (.xls), .pdf, .csv, .mht, .txt oder .xml auswählen. |
| Dateiziel | Hier wird die E-Mail- oder FTP-Adresse angegeben. Die verfügbaren Optionen wechseln ja nach der bisherigen Auswahl. Für FTP müssen Sie sicherstellen, dass der Host extern verfügbar ist. |
| Veröffentlichungsliste | Wenn Sie die geplante Arbeitsmappe an mehrere Veröffentlichungslisten senden, wird die Arbeitsmappe für jede Liste einmal ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist. |
| Sprache des Dateiinhalts | Gibt die Sprache an, die für das Anschreiben verwendet werden soll. Zur Auswahl stehen Chinesisch (vereinfacht oder traditionell), Deutsch, Französisch, Japanisch, Koreanisch, Portugiesisch (Brasilien) oder Spanisch. |
| Registerkarte **Veröffentlichungsoptionen** |  |
| In Power BI veröffentlichen | <ul><li>Arbeitsmappe in Power BI veröffentlichen</li><li>Alle ReportBuilder-Anforderungen als Power BI-Datensätze veröffentlichen</li><li>Alle formatierten Tabellen als Power BI-Datensätze veröffentlichen</li></ul> |
| Diesen Power BI-Bericht bezeichnen als | Bezeichnungsdetails |

1. Click **[!UICONTROL OK]**, then click **[!UICONTROL Exit]**.

   Report Builder displays the scheduled workbook in the [Scheduled Task Manager](/help/analyze/report-builder/r-arb-scheduled-reports.md).

