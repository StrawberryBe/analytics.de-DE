---
description: Sie können Berichte entsprechend der von Ihnen festgelegten Datums- und Dateiformate planen.
title: Eine Datenanforderung planen
uuid: f6d8c90f-e185-4d60-8035-f20f74bfcd89
feature: Report Builder
role: Business Practitioner, Administrator
exl-id: 6aaadaa8-d68f-4a03-8838-53a61b152e31
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 98%

---

# Arbeitsmappen planen

Sie können Arbeitsmappen planen, erweiterte Bereitstellungsoptionen festlegen, Empfänger definieren und sich frühere Zeitpläne ansehen. Erweiterte Bereitstellungsoptionen ermöglichen die Konfigurierung von Arbeitsmappen, die Sie zu einem bestimmten Zeitpunkt oder in regelmäßigen Abständen senden möchten. Sie können außerdem das Dateiformat der Arbeitsmappe festlegen.

Beispielsweise können Sie unter [!DNL Advanced Delivery Options] Arbeitsmappen so planen, dass sie umgehend oder in regelmäßigen Zeitintervallen gesendet werden, und das Dateiformat angeben. Die Dateigröße ist für einen Arbeitsmappen-Upload auf 5 MB begrenzt.

Nachdem Sie einen Arbeitsmappen-Zeitplan in Report Builder erstellt haben, können Sie den Plan auch unter **[!UICONTROL Analysen]** > **[!UICONTROL Berichte]** anzeigen und bearbeiten. (Siehe [Berichtsplanung und -verteilung](/help/analyze/reports-analytics/scheduling.md) in der Hilfe zu Reports &amp; Analytics.)

>[!NOTE]
>
>Sie müssen über Excel 2007 verfügen oder das Compatibility Pack installieren, um eine Arbeitsmappe planen zu können. Sie können pro Report Builder-Lizenz über maximal 10 geplante Arbeitsmappen verfügen. Jedoch können Sie diese Zahl erhöhen, indem Sie bei anderen Lizenzen die benötigte Menge an Arbeitsmappen wegnehmen. Gehen Sie dazu zu **[!UICONTROL Admin]** > **[!UICONTROL Alle Admin]** > **[!UICONTROL Einstellungen für die Firma]** > **[!UICONTROL Report Builder-Berichte]**. Eine Arbeitsmappe, die geplant (oder in die Arbeitsmappen-Bibliothek hochgeladen) wurde und innerhalb von 28 Monaten nicht weiterverwendet (aktualisiert, ersetzt) wurde, wird gelöscht.

>[!NOTE]
>
>Der vom Benutzer eingegebene Wert „Zeitpunkt der Auslieferung“/„Uhrzeit“ gibt den Zeitpunkt an, zu dem die Verarbeitung der Arbeitsmappe beginnt, und nicht den Zeitpunkt, zu dem sie tatsächlich bereitgestellt wird. Die tatsächliche Bereitstellungszeit der Arbeitsmappe hängt in erster Linie davon ab, wie lange die Verarbeitung dauert (bei komplexen und großen Arbeitsmappen dauert die Verarbeitung länger als bei einfacheren Arbeitsmappen). Wenn die Verarbeitung einer Arbeitsmappe z. B. 15 Minuten dauert, ist die tatsächliche Auslieferungszeit frühestens 15 Minuten nach dem ursprünglich angegebenen „Zeitpunkt der Auslieferung“/„Uhrzeit“.
>Darüber hinaus gibt es weitere Faktoren, die die Verzögerung vor der tatsächlichen Auslieferung der Arbeitsmappe weiter erhöhen können:
>
> * **Das gleichzeitige Ausführen vieler verschiedener Zeitpläne desselben Typs** kann das System überlasten. Das Planungssystem erlaubt nur die gleichzeitige Ausführung einiger (5–10) Arbeitsmappen eines Typs. Wenn also mehr als 5–10 gleichzeitig geplant sind, müssen einige warten, bis andere Arbeitsmappen fertig sind, bevor mit deren Verarbeitung begonnen werden kann. Dieses Problem kann behoben werden, indem die Arbeitsmappen eines Unternehmens über den ganzen Tag oder eine Stunde hinweg gestaffelt und nicht gleichzeitig ausgeführt werden.
> * Neben dem Arbeitsmappentyp liegen Arbeitsmappen auch dann in der Warteschlange, wenn das Unternehmen **mehr als 15–20 Arbeitsmappen einer Art gleichzeitig geplant hat (alle Arbeitsmappentypen)**. Dieses Problem kann durch gestaffelte Zeitpläne gelöst werden, sodass nicht viele gleichzeitig ausgeführt werden.
> * **Probleme bei den nachgelagerten Diensten**, auf denen die Planung basiert, können sich auch auf die Bereitstellung von Arbeitsmappen auswirken. Wenn Sie beispielsweise unabhängig voneinander die APIs zum Ausführen von Arbeitsmappen und zum Füllen der API-Anforderungswarteschlange verwenden, werden Ihre geplanten Arbeitsmappen möglicherweise langsam bereitgestellt, da Sie diese Ressource mit einer anderen Funktion teilen.
> * **Die Report Suite-Latenz** (Verzögerung bei der Datenerfassung) kann auch eine Verzögerung bei geplanten Arbeitsmappen bewirken.


## Arbeitsmappe planen

1. Erzeugen Sie eine Arbeitsmappe und speichern Sie ihn.
1. Klicken Sie auf der Report Builder-Symbolleiste auf **[!UICONTROL Plan]**.

   Die Registerkarte [!UICONTROL Terminierte Berichte] enthält eine Zusammenfassung aller von Ihnen erstellten Aufgaben sowie die Anzahl der verbleibenden Aufgaben.
1. Klicken Sie auf der Registerkarte **[!UICONTROL Terminierte Berichte]** auf **[!UICONTROL Neu]**.
1. Das Fenster „Planungs-Assistent – Grundlegend“ wird angezeigt:

   ![](assets/simple-schedule-wizard.png)

1. Konfigurieren Sie im Fenster [!UICONTROL Planungs-Assistent – Grundlegend] die folgenden Optionen:

| Feld | Beschreibung |
|--- |--- |
| Bericht auswählen | Der Name der Arbeitsmappe. Bei neuen terminierten Berichten erscheint in diesem Feld automatisch der Name der aktiven Arbeitsmappe. |
| Auswählen | Hierdurch wird die Seite „Bericht auswählen“ angezeigt. Sie können einen Bericht vom Server (wo alle früher geplanten Arbeitsmappen gespeichert sind) oder von Ihrem lokalen Computer auswählen. Wenn Sie eine Arbeitsmappe von der lokalen Festplatte im .xls-Format auswählen, wandelt das System sie in eine .xlsx-Datei um. Im Rahmen der Konversion wird die Datei in Excel geöffnet und aktiviert. Wenn die für den terminierten Bericht ausgewählte Arbeitsmappe denselben Dateinamen wie die derzeit in Excel geöffnete Arbeitsmappe hat, wählt das System statt der vorher hochgeladenen Datei die lokale Datei. Wenn Sie einen Bericht aus dem Repository der terminierten Berichte wählen, wird eine Kopie der Arbeitsmappe auf dem Server erstellt und deren Dateiname um „1“ erweitert. Der neu terminierte Bericht verwendet die kopierte Arbeitsmappe. |
| Anpassen | Ermöglicht Ihnen, das Datumsformat anzupassen. |
| An | Zeigt Ihr gegebenenfalls vorhandenes Outlook-Adressbuch an. |
| Senden an: E-Mail | Die E-Mail-Adresse des Empfängers der Arbeitsmappe. |
| Senden an: Veröffentlichungsliste | Hiermit zeigen Sie eine Liste der in Ihrem Unternehmen verfügbaren Veröffentlichungslisten an. |
| Power BI | Weitere Informationen finden Sie unter [Arbeitsmappe in Microsoft Power BI veröffentlichen](/help/analyze/report-builder/c-publish-power-bi/integration-power-bi.md). |
| Betreff | Eine benutzerdefinierte Beschreibung. |
| Zeitplan | Hier können Sie angeben, wann die Arbeitsmappe gesendet werden soll (sofort, stündlich, täglich, wöchentlich oder jährlich). |

## Erweiterte Bereitstellungsoptionen

1. Klicken Sie auf **[!UICONTROL Erweiterte Bereitstellungsoptionen]**, um Datei- und Veröffentlichungsoptionen zu konfigurieren:

| Feld | Beschreibung |
|--- |--- |
| Registerkarte **Zeitplan** |  |
| Zeitpunkt der Bereitstellung | Hier können Sie eine sofortige oder spätere Auslieferung der Arbeitsmappe planen. Die Uhrzeit entspricht der Zeitzoneneinstellung auf Ihrem Computer. |
| Wiederholungsmuster | Hiermit wird die Arbeitsmappe entsprechend Ihrer Auswahl gesendet. |
| Bereich der Wiederholung | Hier geben Sie an, wann der Empfang der Arbeitsmappe beginnen und enden soll.   Hinweis: Wenn Sie eine Arbeitsmappe für den ersten Tag eines bestimmten Zeitraums (Woche, Monat, Quartal oder Jahr) planen, werden nur Daten für den ersten Tag zurückgegeben. |
| Registerkarte **Dateioptionen** |  |
| Dateiformat | Hier können Sie als Bereitstellungsformat Excel 2007 (.xlsx) oder 2003 (.xls), .pdf, .csv, .mht, .txt oder .xml auswählen. |
| Dateiziel | Hier wird die E-Mail- oder FTP-Adresse angegeben. Die verfügbaren Optionen wechseln ja nach der bisherigen Auswahl. Für FTP müssen Sie sicherstellen, dass der Host extern verfügbar ist. |
| Veröffentlichungsliste | Wenn Sie die terminierte Arbeitsmappe an mehrere Veröffentlichungslisten gleichzeitig senden, wird die Arbeitsmappe jeweils einmal pro Liste ausgeführt. Variable Report Suites werden durch die Report Suite ersetzt, die der Veröffentlichungsliste zugeordnet ist. |
| Sprache des Dateiinhalts | Gibt die Sprache an, die für das Anschreiben verwendet werden soll. Zur Auswahl stehen Chinesisch (vereinfacht oder traditionell), Deutsch, Französisch, Japanisch, Koreanisch, Portugiesisch (Brasilien) oder Spanisch. |
| Registerkarte **Veröffentlichungsoptionen** |  |
| In Power BI veröffentlichen | <ul><li>Arbeitsmappe in Power BI veröffentlichen</li><li>Alle Report Builder-Anforderungen als Power BI-Datensätze veröffentlichen</li><li>Alle formatierten Tabellen als Power BI-Datensätze veröffentlichen</li></ul> |
| Diesen Power BI-Bericht bezeichnen als | Bezeichnungsdetails |

1. Klicken Sie auf **[!UICONTROL OK]** und dann auf **[!UICONTROL Beenden]**.

   Report Builder zeigt die terminierte Arbeitsmappe im [Manager für geplante Aufgaben](/help/analyze/report-builder/r-arb-scheduled-reports.md) an.
