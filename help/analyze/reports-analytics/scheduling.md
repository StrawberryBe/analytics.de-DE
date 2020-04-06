---
description: Informationen zum Planen, Herunterladen und Verteilen von Berichten.
subtopic: Schedule
title: Berichtsplanung und -verteilung
topic: Reports and analytics
uuid: 1230b0f3-e026-4b83-b231-14d6f75a3836
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Berichtsplanung und -verteilung

Informationen zum Planen, Herunterladen und Verteilen von Berichten.

Wenn Sie einen Bericht für den Versand in einer Adobe Analytics-Anwendung planen, können Sie mit den Zeitplan- und Verteilungstools Ansichten darüber vornehmen, welche Dateien automatisch gesendet wurden, und die Versand ändern oder beenden.

Aufgrund der unterschiedlichen Verarbeitungsmechanismen und Plattformen gelten für die verschiedenen Typen von herunterladbaren und terminierten Berichten, die in Adobe Analytics verfügbar sind, unterschiedliche Einschränkungen hinsichtlich der Höchstzahl von Zeilen, die sie in einer einzigen Anforderung verarbeiten können. Hier sind die jeweiligen Einschränkungen:

* Word, CSV, Excel, HTML und PDF: Die gleiche Anzahl von Zeilen, die im Bericht angezeigt werden. Standardmäßig beträgt dieser Grenzwert 50 Zeilen, kann jedoch bis zu 200 Zeilen betragen. Für Unterteilungsberichte gilt eine feste Grenze von 50 Zeilen.
* Datenextrahierungen: 50.000 Zeilen
* Data Warehouse: Unbegrenzt

Diese Einschränkungen gelten für individuelle terminierte und heruntergeladene Berichte. Dashboards sind auf den Platz beschränkt, der in einem Reportlet verfügbar ist.

>[!NOTE] Der vom Benutzer unter „Zeitpunkt der Bereitstellung“ oder „Tageszeit“ eingegebene Zeitpunkt gibt an, ab wann mit der Verarbeitung des Berichts begonnen wird, und nicht, wann der Bericht bereitgestellt wird. Der tatsächliche Bereitstellungszeitpunkt des Berichts hängt in erster Linie davon ab, wie lange die Verarbeitung dauert (komplexe und umfangreiche Berichte benötigen mehr Verarbeitungszeit als einfachere Berichte). Wenn die Verarbeitung eines Berichts z. B. 15 Minuten dauert, liegt der tatsächliche Bereitstellungszeitpunkt mindestens 15 Minuten nach dem ursprünglich unter „Zeitpunkt der Bereitstellung“ oder „Tageszeit“ eingegebenen Zeitpunkt.
>Darüber hinaus gibt es eine Reihe zusätzlicher Faktoren, durch die sich die tatsächliche Berichtsbereitstellung weiter verzögern kann:
>
> * **Wenn Sie mehrere verschiedene Zeitpläne desselben Typs gleichzeitig ausführen** (z. B. mehrere Dashboards) ist das System möglicherweise überlastet. Das Planungssystem kann nur eine begrenzte Anzahl von Berichten (5 bis 10) des gleichen Typs auf einmal ausführen. Wenn also mehr als 5 bis 10 Berichte auf einmal geplant sind, müssen einige Berichte warten, bis die Verarbeitung anderer Berichte abgeschlossen ist. Sie können dieses Problem umgehen, indem Sie die Ausführung der Berichte Ihres Unternehmens über einen Tag oder eine Stunde staffeln, statt sie alle auf einmal auszuführen.
> * Darüber hinaus werden Berichte unabhängig vom Berichtstyp (Dashboards usw.) in die Warteschlange gestellt, wenn das Unternehmen **mehr als 15 bis 20 Berichte eines beliebigen Typs gleichzeitig geplant hat**. Auch dies kann dadurch umgangen werden, indem die Ausführungszeiten gestaffelt werden, statt viele Berichte zum gleichen Zeitpunkt auszuführen.
> * **Probleme bei nachgeschalteten Diensten**, von denen die Planung abhängt, können sich ebenfalls auf die Bereitstellung von Berichten auswirken. Wenn Sie z. B. die APIs sowohl zum Ausführen von Berichten als auch zum Füllen der API-Anforderungswarteschlange verwenden, kann es durch den Wettstreit um die Ressourcen zu Verzögerungen bei der Berichtsbereitstellung kommen.
> * Auch die **Report Suite-Latenz** (eine Verzögerung bei der Datenerfassung) kann die Bereitstellung einiger terminierter Berichte verzögern.



## Bericht senden {#task_27642CD33D484FD0BF59EBD159EEF52C}

In diesen Schritten wird beschrieben, wie Sie Berichte in einer Vielzahl von Formaten herunterladen und per E-Mail versenden können und wie Sie die Bereitstellung von Berichten planen.

1. Run a report, then click **[!UICONTROL More]** > **[!UICONTROL Send]**.
1. Legen Sie die Auslieferungsoptionen fest:

   | Option | Beschreibung |
   |--- |--- |
   | Format | Wählen Sie PDF oder HTML aus. |
   | Senden an | Geben Sie eine E-Mail-Adresse ein, um den Bericht zu erhalten. |
   | Betreff | Betreff der E-Mail |
   | Zeitplan | Wählen Sie diese Option, um den Bericht sofort oder in einem anderen Intervall zu senden. |

1. Klicken Sie auf **[!UICONTROL Advanced Delivery Options]** , um einen Zeitplan für den Versand festzulegen.

| Option | Beschreibung |
|--- |--- |
| Berichtsdateiname | Gibt den Namen des Berichts an. Das Standardformat ist `<report name> for <suite> - <report date range>`. Um einen benutzerdefinierten Namen anzugeben, wählen Sie [!UICONTROL Custom]. |
| Berichtsformat | Hier können Sie die Formate PDF, CSV, Excel, HTML, Word oder Mobil für den Versand angeben. Wenn Sie CSV auswählen, können Sie auch die Kodierung für CSV angeben:<ul><li>Shift-JIS: Japanische Zeichenkodierung.</li><li>EUC-JP: Extended Unix Code, hauptsächlich für Japanisch, Koreanisch und vereinfachtes Chinesisch.</li></ul> |
| Berichtsinhalt | <ul><li>Anzahl der Zeilen in der Tabelle: Gibt die Anzahl der Zeilen an, die in der versendeten Tabelle des Berichts angezeigt werden sollen.</li><li>Sprache für Kopf- und Fußzeile: Gibt die Sprache der Kopfzeile und Fußzeile an.</li><li>Kommentare: Gibt den Text an, der zu Beginn des Berichts erscheint.</li></ul> |
| Digitalsignaturdatei senden | Wenn Sie einen Bericht anfordern, z. B. einen mit Lesezeichen versehenen Bericht oder Data Warehouse-Anforderungen, können Sie eine Datensignatur anfordern. Die digitale Signatur von Adobe schränkt nicht den Kreis der Personen ein, die Zugriff auf die Daten haben. Der Zweck der digitalen Signaturdatei (.sig) ist vielmehr, die Gültigkeit der gelieferten Berichtsdatei zu verifizieren. Mithilfe der Digitalsignatur können die Empfänger des Berichts überprüfen, ob die Datei von Adobe stammt und nicht verändert wurde. |
| Berichtsziel | <ul><li>E-Mail: Hier können Sie die E-Mail-Adresseinstellungen, die Betreffzeile und Notizen konfigurieren.</li><li>FTP: Hier können Sie FTP-Einstellungen, z. B. Host, Port, Verzeichnis, Benutzername und Passwort, konfigurieren.</li></ul> |

1. Klicken Sie auf **[!UICONTROL Scheduling Options]**.

| Option | Beschreibung |
|--- |--- |
| Bericht jetzt senden | Sendet den Bericht sofort. |
| Für später einplanen | Zeigt Optionen zum Festlegen eines Zeitrahmens und von Optionen für den Versand an. |
| Berichtszeitraum | **Fest**: Verhindert, dass das Datum im Zeitverlauf angepasst wird. **Rollierend**: Ermöglicht, dass das Datum im Zeitverlauf angepasst wird. Einige Überlegungen:<ul><li>Wenn Sie für das Start- und Enddatum „Rollierend“ einstellen und einen täglichen Bericht des Vortags auswählen, erhalten Sie jeden Tag eine E-Mail mit einem Bericht des vorherigen Tags.</li><li>Wenn Sie für das Startdatum „Fest“ und für das Enddatum „Rollierend“ einstellen, erhalten Sie am ersten Tag einen Bericht für den vorherigen Tag. Am zweiten Tag erhalten Sie einen Bericht für die vorherigen zwei Tage, am dritten Tag einen Bericht für die vorherigen drei Tage usw.</li><li>Wenn Sie sowohl für das Start- als auch für das Enddatum Fest einstellen, erhalten Sie jeden Tag einen identischen Bericht für die angegebenen Tage.</li><li>Die Auswahl eines rollierenden Startdatums und feststehenden Enddatums ist nicht möglich.</li></ul> |
| Bereitstellungshäufigkeit | <ul><li>**Stündlich**: Die Auslieferung der E-Mail erfolgt jede Stunde, alle zwei Stunden oder in einem beliebigen anderen Stundenintervall.</li><li>**Täglich**: Sendet die E-Mail jeden Tag, jeden zweiten Tag, alle drei Tage oder in einem beliebigen anderen Tagesintervall. Sie können es auch jeden Wochentag senden lassen.</li><li>**Wöchentlich**: Die Auslieferung der E-Mail erfolgt jede Woche, jede zweite Woche, jede dritte Woche oder in einem beliebigen anderen Wochenintervall. Sie können auch den Wochentag angeben, an dem der Bericht gesendet wird.</li><li>**Monatlich**: Gibt das Intervall in der Anzahl der Monate an. Sie können auch den Tag des Monats auswählen, an dem das Intervall gesendet wird, oder den Wochentag in einer bestimmten Woche des Monats.</li><li>**Jährlich**: Gibt den Tag des Jahres an, an dem der Bericht gesendet wird, oder Sie können einen bestimmten Wochentag in einer beliebigen Woche des Jahres senden.</li><li>**Tageszeit**: Gilt für die Zeitzone, die der ausgewählten Report Suite zugeordnet ist.</li></ul> |
| Bereitstellungsoptionen beenden | <ul><li>**Niemals beenden**: Gibt kein Ende an.</li><li>**Nach`value`Vorfällen beenden**: Gibt die Anzahl der Vorfälle vor Beendigung der Auslieferung an.</li><li>**Beenden am**: Hier können Sie ein bestimmtes Datum angeben. Wenn Sie die Daten am selben Datum wie die Berichtsdaten verarbeiten möchten, enthält der Bericht nur Daten, die zum Zeitpunkt des Berichtversands in die Datenbank aufgenommen wurden. Da die Verarbeitung für einen Tag bis zu 24 Stunden dauern kann, stehen zum Zeitpunkt des Berichtversands möglicherweise keine vollständigen Daten zur Verfügung. Für vollständige Daten legen Sie die Verarbeitungszeit immer 24 Stunden nach dem Ende des Berichte fest.</li></ul> |

## Bericht drucken {#task_0F7CF6D6ED54462CAE4A793E271AF7E5}

In diesen Schritten wird beschrieben, wie Sie einen Bericht drucken.

1. Einen Bericht ausführen.
1. Klicken Sie auf **[!UICONTROL More]** > **[!UICONTROL Print]**.  ![](assets/print.png)

## Einen Bericht mit einfachen Optionen herunterladen {#task_43660107A1C9485D92981CD75B562577}

Sie können detaillierte Informationen zu einem bestimmten Bericht in den Exportformaten PDF, CSV, Excel oder als Rohdaten herunterladen.

1. In  **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** , select a report to view.
1. Klicken Sie auf **[!UICONTROL Download]**.

   ![](assets/download_basic.png)

1. Wählen Sie das gewünschte Format für den Bericht aus: 

   * **[!UICONTROL PDF]**: Legt fest, dass der Bericht im Adobe PDF-Format heruntergeladen wird, sodass Sie ihn an andere weitergeben können, unabhängig davon, welches Computersystem der Empfänger verwendet.
   * **[!UICONTROL CSV]**: Legt fest, dass der Bericht im Format [!DNL .csv] (Format mit durch Trennzeichen getrennten Werten) heruntergeladen wird.
   * **[!UICONTROL Excel]**: Legt fest, dass der Bericht im Microsoft Excel-Format heruntergeladen wird, sodass Sie ihn an andere weitergeben können, die ihn in einem Tabellenprogramm öffnen können.
   * **[!UICONTROL Word]**: Legt fest, dass der Bericht im Microsoft Word-Format heruntergeladen wird.
   >[!NOTE]
   >
   >Wenn Sie eines der Rohdatenexportformate verwenden möchten, um einen Bericht herunterzuladen und der Seitenname leer ist, hatte Adobe Analytics wahrscheinlich nicht genug Zeit, die Daten zu verarbeiten. Laden Sie den Bericht später herunter.

## Terminierte Berichte verwalten {#task_C17677C543454FF2B06D10EA5652DFBC}

Informationen über die Verwaltung von terminierten Berichten.

Im [!UICONTROL Schedule Reports Manager]Bericht können Sie wiederkehrende Versand bearbeiten und löschen. Sie können Zeitpläne für Versand erstellen, die Ihre Berichte per E-Mail oder FTP an eine bestimmte Adresse senden. Sie können diese Zeitpläne so konfigurieren, dass die Berichte in bestimmten Zeitabständen oder auf unbestimmte Zeit automatisch gesendet werden, oder den Versand eines sich wiederholenden Berichts beenden.

The [!UICONTROL Schedule Report Manager] shows the items that a specific user has created. Wenn das Benutzerkonto in der Anwendung deaktiviert wird, werden alle geplanten Bereitstellungen gestoppt.

1. Um auf den Manager zuzugreifen, klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL Scheduled Reports]**.

## Berichtlink freigeben {#task_9711DDE9E140451B8C914EC5513E21EC}

In diesen Schritten wird beschrieben, wie Sie einen Bericht freigeben, indem Sie einen Link (URL) für einen Bericht generieren, der an einen anderen Benutzer gesendet werden soll.

Wenn der Empfänger auf den Link klickt, fordert das System die Anmeldeinformationen (Firma, Benutzername und Kennwort) an. Nach der Anmeldung wird dem Empfänger der vom Originalbenutzer erstellte Bericht angezeigt. Es gelten die standardmäßigen Zugriffsbeschränkungen.

**So geben Sie einen Berichtslink frei**

1. Einen Bericht ausführen.
1. Klicken Sie auf **[!UICONTROL More]** > **[!UICONTROL Link to This Report]**.

## Abmeldung von terminierten Berichten {#concept_6B48360F935740B6851BA85D32DEF637}

Sie können das Abonnement für geplante Berichte aufheben. Sie erhalten den Bericht nicht mehr, selbst wenn Ihr Benutzername dem terminierten Bericht erneut hinzugefügt wird.

>[!IMPORTANT]
>
>Damit Sie den Bericht wieder erhalten, müssen Sie einen neuen Zeitplan erstellen.

So melden Sie sich von einem terminierten Bericht ab:

1. Öffnen Sie die E-Mail mit dem Link zu dem Bericht, von dem Sie sich abmelden möchten.

   ![](assets/unsubscribe-email.png)

1. Klicken Sie auf den **[!UICONTROL click here]** Link neben **[!UICONTROL To cancel automatic delivery of this report]**.

1. Vergewissern Sie sich, dass Sie den Bericht-Versand abbrechen möchten.

   >[!NOTE]
   >
   >Dieser Workflow ist immer gleich, egal, ob Sie der Planer oder der Empfänger des Berichts sind.

Die Abmeldung von einem Bericht bricht den terminierten Bericht nicht ab.

Um einen terminierten Bericht abzubrechen, rufen Sie den Zeitplan-Manager auf und klicken auf das rote X neben dem Berichtsnamen. [Mehr …](/help/analyze/reports-analytics/scheduling.md#task_C17677C543454FF2B06D10EA5652DFBC)
