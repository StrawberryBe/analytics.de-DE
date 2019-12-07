---
description: Informationen zum Planen, Herunterladen und Verteilen von Berichten.
subtopic: Schedule
title: Berichtsplanung und -verteilung
topic: Reports and analytics
uuid: 1230b0f3-e026-4b83-b231-14d6f75a3836
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Berichtsplanung und -verteilung

Informationen zum Planen, Herunterladen und Verteilen von Berichten.

Verwenden Sie die Zeitplan- und Verteilungstools, um einen Bericht zur Bereitstellung in einer Adobe Analytics-Anwendung vorzumerken, den automatischen Versand von Dateien zu prüfen und die Bereitstellung abzuändern oder zu beenden.

Aufgrund der unterschiedlichen Verarbeitungsmechanismen und Plattformen gelten für die unterschiedlichen Arten von herunterladbaren und terminierten Berichten von Adobe Analytics verschiedene Einschränkungen hinsichtlich der Höchstzahl an Zeilen, die sie in einer einzigen Anforderung verarbeiten können. Hier sind die Grenzen für jede Art:

* Word, CSV, Excel, HTML und PDF: Dieselbe Anzahl an Zeilen, die im Bericht zu sehen sind. Standardmäßig ist die Grenze auf 50 Zeilen festgelegt. Sie können sie jedoch auch auf maximal 200 erhöhen. Detailbericht haben eine feste Höchstgrenze von 50 Zeilen.
* Datenextraktion: 50.000 Zeilen
* Data Warehouse: Unbegrenzt

Diese Einschränkungen gelten für einzelne terminierte und heruntergeladene Berichte. Dashboards sind auf den verfügbaren Speicherplatz in einem Reportlet beschränkt.

> [!NOTE] Die vom Benutzer eingegebene "Bereitstellungszeit"/"Tageszeit"gibt den Zeitpunkt an, zu dem der Bericht verarbeitet werden soll, und nicht den Zeitpunkt, zu dem er tatsächlich bereitgestellt wird. Die tatsächliche Dauer der Berichtauslieferung hängt in erster Linie davon ab, wie lange die Verarbeitung dauert (komplexe und große Berichte benötigen mehr Verarbeitungszeit als einfachere Berichte). Wenn die Verarbeitung eines Berichts z. B. 15 Minuten dauert, beträgt die tatsächliche Lieferzeit mindestens 15 Minuten nach der ursprünglich angegebenen "Bereitstellungszeit"/"Tageszeit".
>Darüber hinaus gibt es eine Reihe weiterer Faktoren, die die Verzögerung vor der tatsächlichen Übermittlung des Berichts noch verstärken können:
>
> * **Mehrere verschiedene Zeitpläne desselben Typs gleichzeitig** ausführen (z. B. viele Dashboards usw.) kann das System überladen. Das Planungssystem ermöglicht nur die gleichzeitige Ausführung einiger (5-10) Berichte eines beliebigen Typs. Wenn also mehr als 5-10 Berichte auf einmal geplant sind, müssen einige sofort warten, bis andere Berichte fertig gestellt sind, bevor sie mit der Verarbeitung beginnen können. Dieses Problem kann durch die Planung der Unternehmensberichte zu gestaffelten Zeiten über den gesamten Tag oder die Stunde hinweg und nicht gleichzeitig behoben werden.
> * Neben dem jeweiligen Berichtstyp (Dashboards usw.) warten Berichte auch in der Warteschlange, wenn das Unternehmen **mehr als 15 bis 20 von beliebigen Berichtstypen gleichzeitig (über alle Berichtstypen hinweg)** geplant hat. Dies kann durch atemberaubende Zeitpläne abgemildert werden, anstatt dass viele gleichzeitig ausgeführt werden.
> * **Probleme bei den nachgelagerten Diensten** , auf denen der Zeitplan basiert, können sich auch auf die Bereitstellung von Berichten auswirken. Wenn Sie z. B. unabhängig die APIs zum Ausführen von Berichten und zum Ausfüllen der API-Anforderungswarteschlange verwenden, werden Ihre terminierten Berichte möglicherweise langsam bereitgestellt, während Sie um diese Ressource konkurrieren.
> * **Die Report Suite-Latenz** (Verzögerung bei der Datenerfassung) kann auch einige geplante Berichte verzögern.



## Bericht senden {#task_27642CD33D484FD0BF59EBD159EEF52C}

In diesen Schritten wird beschrieben, wie Sie Berichte in einer Vielzahl von Formaten herunterladen und per E-Mail versenden können und wie Sie die Bereitstellung von Berichten planen.

1. Run a report, then click **[!UICONTROL More]** &gt; **[!UICONTROL Send]**.
1. Legen Sie die Auslieferungsoptionen fest:

   | Option | Beschreibung |
   |--- |--- |
   | Format | Wählen Sie PDF oder HTML aus. |
   | Senden an | Geben Sie eine E-Mail-Adresse an, an die der Bericht gesendet werden kann. |
   | Betreff | Betreff der E-Mail |
   | Zeitplan | Wählen Sie aus, ob Sie den Bericht sofort oder in einem anderen Intervall senden möchten. |

1. Click **[!UICONTROL Advanced Delivery Options]** to specify a delivery schedule.

| Option | Beschreibung |
|--- |--- |
| Berichtsdateiname | Gibt den Namen des Berichts an. The default format is `<report name> for <suite> - <report date range>`. Um einen benutzerspezifischen Namen festzulegen wählen Sie [!UICONTROL Benutzerdefiniert] aus. |
| Berichtsformat | Ermöglicht die Auswahl des Formats für die Auslieferung (PDF, CSV, Excel, HTML, Word oder Mobil). Wenn Sie CSV auswählen können Sie auch die Kodierung für CSV auswählen:<ul><li>Shift-JIS: Japanische Zeichenkodierung.</li><li>EUC-JP: Erweiterter Unix-Code, hauptsächlich für Japanisch, Koreanisch und vereinfachtes Chinesisch.</li></ul> |
| Berichtsinhalt | <ul><li>Anzahl der Zeilen in der Tabelle: Gibt die Anzahl der Zeilen an, die in der versendeten Tabelle des Berichts angezeigt werden sollen.</li><li>Sprache für Kopf- und Fußzeile: Gibt die Sprache der Kopfzeile und Fußzeile an.</li><li>Kommentare: Gibt den Text an, der zu Beginn des Berichts erscheint.</li></ul> |
| Digitalsignaturdatei senden | Wenn Sie einen Bericht anfordern, z. B. einen mit Lesezeichen versehenen Bericht oder Data Warehouse-Anforderungen, können Sie eine Datenunterschrift anfordern. Die digitale Signatur von Adobe schränkt nicht die Personen ein, die Zugriff auf die Daten haben, aber der Zweck der digitalen Signaturdatei (.sig) ist es, die Gültigkeit der gelieferten Berichtsdatei zu überprüfen. Mithilfe der Digitalsignatur kann der Berichtempfänger sichergehen, dass die Datei von Adobe stammt und nicht unbefugterweise verändert wurde. |
| Berichtsziel | <ul><li>E-Mail: Hier können Sie die E-Mail-Adresseinstellungen, die Betreffzeile und Notizen konfigurieren.</li><li>FTP: Hier können Sie FTP-Einstellungen, z. B. Host, Port, Verzeichnis, Benutzername und Passwort, konfigurieren.</li></ul> |

1. Click **[!UICONTROL Scheduling Options]**.

| Option | Beschreibung |
|--- |--- |
| Bericht jetzt senden | Sendet den Bericht sofort. |
| Für später einplanen | Zeigt Optionen für die Auswahl eines Zeitrahmens sowie Auslieferungsoptionen an. |
| Berichtszeitraum | **Fest**: Verhindert, dass das Datum im Zeitverlauf angepasst wird. **Rollierend**: Ermöglicht, dass das Datum im Zeitverlauf angepasst wird. Berücksichtigen Sie dabei:<ul><li>Wenn Sie für das Start- und Enddatum Rollierend einstellen und einen täglichen Bericht des Vortags auswählen, erhalten Sie jeden Tag eine E-Mail mit einem Bericht des vorherigen Tags.</li><li>Wenn Sie für den Starttag "Fest"und für den Endtag "rollierend"auswählen, erhalten Sie am ersten Tag einen Bericht für den vorherigen Tag. Am zweiten Tag erhalten Sie einen Bericht für die vorherigen zwei Tage, am dritten Tag einen Bericht für die vorherigen drei Tage usw.</li><li>Wenn Sie sowohl für das Start- als auch für das Enddatum Fest einstellen, erhalten Sie jeden Tag einen identischen Bericht für die angegebenen Tage.</li><li>Sie können kein rollierendes Startdatum und kein festes Enddatum auswählen.</li></ul> |
| Auslieferungshäufigkeit | <ul><li>**Stündlich**: Die Auslieferung der E-Mail erfolgt jede Stunde, alle zwei Stunden oder in einem beliebigen anderen Stundenintervall.</li><li>**Täglich**: Die Auslieferung der E-Mail erfolgt jeden Tag, jeden zweiten Tag, alle drei Tage oder in einem beliebigen anderen Tagesintervall. Die Auslieferung kann auch an allen Wochentagen erfolgen.</li><li>**Wöchentlich**: Die Auslieferung der E-Mail erfolgt jede Woche, jede zweite Woche, alle drei Wochen oder in einem beliebigen anderen Wochenintervall. Sie können auch den Wochentag festlegen, an dem die Auslieferung erfolgen soll.</li><li>**Monatlich**: Gibt das Intervall in der Anzahl der Monate an. Sie können auch einen bestimmten Tag im Monat bzw. einen Tag in einer bestimmten Woche des Monats für die Auslieferung festlegen.</li><li>**Jährlich**: Gibt an, an welchem Tag des Jahres die Auslieferung des Berichts erfolgt. Sie können auch einen bestimmten Wochentag in einer beliebigen Woche des Jahres für die Auslieferung festlegen.</li><li>**Tageszeit**: Bezieht sich auf die Zeitzone, die für die jeweilige Report Suite gilt.</li></ul> |
| Optionen für das Ende der Auslieferung | <ul><li>**Niemals beenden**: Gibt kein Ende an.</li><li>**Nach`value`Vorfällen** beenden: Gibt die Anzahl der Vorfälle vor Beendigung der Auslieferung an.</li><li>**Beenden am**: Hier können Sie ein bestimmtes Datum angeben. Sollen die Daten am selben Tag verarbeitet werden wie die Berichtsdaten, enthält der Bericht nur Daten, die zu dem Zeitpunkt in der Datenbank vorliegen, zu dem der Bericht gesendet wird. Da die Verarbeitung der Daten eines Tages bis zu 24 Stunden dauern kann, stehen vollständige Daten zum Zeitpunkt des Berichtversands eventuell nicht zur Verfügung. Um vollständige Daten zu erhalten, sollten Sie die Verarbeitungszeit stets auf 24 Stunden nach Ende des Berichtzeitraums einstellen.</li></ul> |

## Bericht drucken {#task_0F7CF6D6ED54462CAE4A793E271AF7E5}

In diesen Schritten wird beschrieben, wie Sie einen Bericht drucken.

1. Einen Bericht ausführen.
1. Click **[!UICONTROL More]** &gt; **[!UICONTROL Print]**.  ![](assets/print.png)

## Einen Bericht mit einfachen Optionen herunterladen {#task_43660107A1C9485D92981CD75B562577}

Sie können detaillierte Informationen zu einem bestimmten Bericht in den Exportformaten PDF, CSV, Excel oder als Rohdaten herunterladen.

1. In **Analytics** &gt; **[!UICONTROL Berichte]** können Sie einen Bericht zur Ansicht öffnen.
1. Klicken Sie auf **[!UICONTROL Herunterladen]**.

   ![](assets/download_basic.png)

1. Wählen Sie das gewünschte Format für den Bericht aus: 

   * **[!UICONTROL PDF]**: Legt fest, dass der Bericht im Adobe PDF-Format heruntergeladen wird, sodass Sie ihn an andere weitergeben können, unabhängig davon, welches Computersystem der Empfänger verwendet.
   * **[!UICONTROL CSV]**: Gibt an, dass der Bericht im [!DNL .csv] (kommagetrennten Wertformat) heruntergeladen wird.
   * **[!UICONTROL Excel]**: Legt fest, dass der Bericht im Microsoft Excel-Format heruntergeladen wird, sodass Sie ihn an andere weitergeben können, die den Bericht dann in einem Tabellenkalkulationsprogramm öffnen können.
   * **[!UICONTROL Word]**: Legt fest, dass der Bericht im Microsoft Word-Format heruntergeladen wird.
   >[!NOTE]
   >
   >Wenn Sie zum Herunterladen eines Berichts eines der Rohdatenexportformate verwenden und der Seitenname leer ist, hat Adobe Analytics wahrscheinlich nicht genug Zeit, die Daten zu verarbeiten. Laden Sie den Bericht später herunter.

## Terminierte Berichte verwalten {#task_C17677C543454FF2B06D10EA5652DFBC}

Informationen über die Verwaltung von terminierten Berichten

Im [!UICONTROL Manager für geplante Berichte] können regelmäßige Berichtauslieferungen bearbeitet und gelöscht werden. Richten Sie Auslieferungspläne ein, um Ihre Berichte per E-Mail oder FTP an bestimmte Adressen zu senden. Sie können diese Pläne zum automatischen Versand der Berichte in bestimmten, befristeten oder unbefristeten Intervallen konfigurieren oder die Auslieferung eines sich wiederholenden Berichts stoppen.

Im [!UICONTROL „Manager für geplante Berichte“] werden die Elemente angezeigt, die von einem bestimmten Benutzer erstellt wurden. Wenn das Benutzerkonto in der Anwendung deaktiviert wird, werden alle geplanten Bereitstellungen gestoppt.

1. To access the manager, click **[!UICONTROL Analytics]** &gt; **[!UICONTROL Components]** &gt; **[!UICONTROL Scheduled Reports]**.

## Berichtlink freigeben {#task_9711DDE9E140451B8C914EC5513E21EC}

In diesen Schritten wird beschrieben, wie Sie einen Bericht freigeben, indem Sie einen Link (URL) für den Bericht generieren, der an andere Benutzer gesendet werden kann.

Wenn der Empfänger auf den Link klickt, fordert das System zur Eingabe der Anmeldeangaben (Firmenname, Benutzername und Passwort) auf. Nach der Anmeldung wird dem Empfänger der vom Verfasser erstellte Bericht angezeigt. Dabei gelten die standardmäßigen Zugriffsrechte.

**So geben Sie einen Bericht-Link frei**

1. Einen Bericht ausführen.
1. Click **[!UICONTROL More]** &gt; **[!UICONTROL Link to This Report]**.

## Abmeldung von terminierten Berichten {#concept_6B48360F935740B6851BA85D32DEF637}

Sie können sich von terminierten Berichten abmelden. Sie erhalten dann den Bericht nicht mehr; selbst, wenn Ihr Benutzername erneut zum terminierten Bericht hinzugefügt wird.

>[!IMPORTANT]
>
>Damit Sie den Bericht erneut erhalten, muss ein neuer Zeitplan erstellt werden.

So melden Sie sich von einem terminierten Bericht ab:

1. Suchen Sie die E-Mail mit dem Link zu dem Bericht, von dem Sie sich abmelden möchten.

   ![](assets/unsubscribe-email.png)

1. Click the **[!UICONTROL click here]** link next to **[!UICONTROL To cancel automatic delivery of this report]**.

1. Bestätigen Sie, dass Sie keine weitere Zustellung des Berichts wünschen.

   >[!NOTE]
   >
   >Dieser Arbeitsablauf ist unabhängig davon, ob Sie der Berichtsplaner oder der Berichtempfänger sind, identisch.

Die Abmeldung von einem Bericht bricht den terminierten Bericht nicht ab.

Um einen terminierten Bericht abzubrechen, rufen Sie den Zeitplan-Manager auf und klicken auf das rote X neben dem Berichtsnamen. [Mehr …](/help/analyze/reports-analytics/scheduling.md#task_C17677C543454FF2B06D10EA5652DFBC)
