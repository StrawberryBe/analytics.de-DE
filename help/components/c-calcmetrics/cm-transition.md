---
description: Diese Änderungen an der Funktionsweise von berechneten Metriken in Analytics können sich auf Sie auswirken.
title: Häufig gestellte Fragen
uuid: 9b7f1cd1-b969-4b15-8af1-969d816b65b8
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Häufig gestellte Fragen

Diese Änderungen an der Funktionsweise von berechneten Metriken in [!DNL Analytics] können sich auf Ihre Arbeit auswirken.

[Wie greife ich auf den Generator für berechnete Metriken zu?](/help/components/c-calcmetrics/cm-transition.md#section_D9AE9A0ACF824BACB5D05F0C2F7E9CA1)

[Wie greife ich auf den Manager für berechnete Metriken zu?](/help/components/c-calcmetrics/cm-transition.md#section_DD0BD13E9EC940268EBE8BC88241A152)

[Warum werden so viele berechnete Metriken mit demselben Namen angezeigt?](/help/components/c-calcmetrics/cm-transition.md#section_E15C5B6CCC58498CAEC3FBDA8988F0A1)

[Was ist mit meinen globalen berechneten Metriken passiert?](/help/components/c-calcmetrics/cm-transition.md#section_7351D4C7361F4ABAA1B43F8E89AAD211)

[Was ist mit globalen berechneten Metriken passiert, die über Anmeldeunternehmen hinweg freigegeben wurden?](/help/components/c-calcmetrics/cm-transition.md#section_59E5CD948ED643AE9AD3D2E4277647F8)

[Was ist mit berechneten Metriken mit der Classification Numerisch oder Numerisch2 passiert?](/help/components/c-calcmetrics/cm-transition.md#section_71AFE6C4A7CD4AA19AB3A9D3C41D115B)

[Was ist mit Lebensdauermetriken passiert?](/help/components/c-calcmetrics/cm-transition.md#section_AEDB02EF24584DAD8731BED9DDCE4F48)

[Was muss ich über berechnete Metriken basierend auf Metriken für tägliche/wöchentliche/monatliche/vierteljährliche/jährliche Unique Visitor wissen?](/help/components/c-calcmetrics/cm-transition.md#section_E9A77EBB41CE4881B196CC1C282B2DF3)

[Was passiert mit berechneten Metriken, die mit den alten Report Suite-API-Methoden erstellt oder verwaltet wurden?](/help/components/c-calcmetrics/cm-transition.md#section_13ED1BAD02634674BDAEB479B060A4B6)

[Unterstützt „Aktuelle Daten“ alle Typen an berechneten Metriken?](/help/components/c-calcmetrics/cm-transition.md#section_1DAA718BB8DB4413BAF8AD4B4FAAFFA2)

[Was bedeutet „Kein Name angegeben“ im Zusammenhang mit migrierten berechneten Metriken?](/help/components/c-calcmetrics/cm-transition.md#section_C90CBB72A67644F38D583301981F8D03)

[Was passiert mit den berechneten Metriken eines Benutzers, wenn dieser Benutzer gelöscht wird?](/help/components/c-calcmetrics/cm-transition.md#section_42ED4C15830540879C4A161423690E5A)

[Warum werden „unbekannte“ berechnete Metriken angezeigt, die nicht für andere Report Suites „gültigׅ“ sind, obwohl sie erstellt und auf diese Report Suites angewendet werden können?](/help/components/c-calcmetrics/cm-transition.md#section_6772818EFDED46E9B7095D64C3B77211)

[Warum wurden Änderungen an meinen alten berechneten Metriken nicht gespeichert?](/help/components/c-calcmetrics/cm-transition.md#section_81CDEFCA1FD542579AF183DA1494EAF0)

[Warum werden meine berechneten Metriken nicht im Marketing-Kanal-Bericht angezeigt?](/help/components/c-calcmetrics/cm-transition.md#section_FC350359A775433AB5F43C7CAB304D62)

[Warum enthalten einige der berechneten Metriken Formeln ohne die Klammern, die ich hinzugefügt habe?](/help/components/c-calcmetrics/cm-transition.md#section_AC0D1E9714AD487F9A1C73359F518B5E)

[(Nur Ad Hoc Analysis) Werden berechnete Metriken mit eingebetteten oder Inline-Segmentdefinitionen weiterhin unterstützt?](/help/components/c-calcmetrics/cm-transition.md#section_B25C924A282F49388AB604E3D826F44C)

[(Nur Report Builder) Warum sind berechnete Metriken aus meinen Anforderungen verschwunden?](/help/components/c-calcmetrics/cm-transition.md#section_DA4792FE5D7945218CD5E6328DE08E82)

[Wie werden Gesamtwerte für berechnete Metriken ermittelt?](/help/components/c-calcmetrics/cm-transition.md#section_57BA3A299C7948ABB82B0392A9B0F33E)

## Wie greife ich auf den Generator für berechnete Metriken zu? {#section_D9AE9A0ACF824BACB5D05F0C2F7E9CA1}

* Click **[!UICONTROL + Add]** at the top of the Calculated Metric Manager, or
* In any Analytics report, click the Metrics icon  ![](assets/metrics_icon.png) to the left of a report to bring up the Metrics rail, then click **[!UICONTROL Add]**.

## Wie greife ich auf den Manager für berechnete Metriken zu? {#section_DD0BD13E9EC940268EBE8BC88241A152}

* Go to  **[!UICONTROL Analytics]** > **[!UICONTROL Components]** in the left navigation. Klicken Sie danach auf **[!UICONTROL Calculated Metrics]**.

* In any [!DNL Analytics] report, click the Metrics icon  ![](assets/metrics_icon.png) to the left of a report to bring up the Metrics rail, then click **[!UICONTROL Manage]**.

## Warum werden so viele berechnete Metriken mit demselben Namen angezeigt? {#section_E15C5B6CCC58498CAEC3FBDA8988F0A1}

(Bisher gehörten globale berechnete Metriken keinem bestimmten Administrator und waren für alle Benutzer dieser Report Suite sichtbar. Die Metriken wurden nach Report Suite getrennt. Wenn eine Metrik in einer Report Suite denselben Namen wie eine Metrik in einer anderen Report Suite hat, wird sie den Benutzern beim Wechsel der Report Suites einfach als dieselbe Metrik angezeigt.)

Jetzt werden Metriken nicht mehr nach Report Suites getrennt. Wenn eine Metrik in einer Report Suite denselben Namen wie eine Metrik in einer anderen Report Suite hat, sind sie sowohl im Generator für berechnete Metriken als auch in der Metrikauswahl sichtbar und können als Duplikat-Metriken angezeigt werden, auch wenn sie möglicherweise nicht dieselbe Definition haben.

Berechnete Metriken, die denselben Namen aufweisen (aber in unterschiedlichen Report Suites erstellt wurden), werden nur angezeigt, wenn Sie das Kontrollkästchen (Nur `<report suite>`) wie hier gezeigt deaktivieren:

![](assets/report_suite.png)

**Was Sie tun müssen**

Erwägen Sie, berechnete Metriken mit ähnlichen Namen und Definitionen zu konsolidieren. Gehen Sie dabei jedoch vorsichtig vor. Sie können die Report Suite im Manager für berechnete Metriken auf eine errechnete Metrik überprüfen, um die ursprüngliche Report Suite zu überprüfen. Sie sollten beim Löschen potenzieller Duplikat auch die Definitionen der Metriken überprüfen, um sicherzustellen, dass Sie die Metriken korrekt konsolidieren.

>[!NOTE] Auch wenn berechnete Metriken nicht mehr an eine spezielle Report Suite gebunden sind und in jeder Report Suite verwendet werden können, die für das Anmeldeunternehmen sichtbar ist, wird die Report Suite, unter der die berechnete Metrik erstellt oder zuletzt gespeichert wurde, weiterhin im Manager für berechnete Metriken angezeigt.

>[!NOTE] Selbst wenn eine berechnete Metrik gelöscht wird, funktionieren alle Lesezeichen oder Dashboard-Berichte, die diese Metrik referenzieren, weiterhin.

## Was ist mit meinen globalen berechneten Metriken passiert? {#section_7351D4C7361F4ABAA1B43F8E89AAD211}

Bisher konnte ein Administrator berechnete Metriken (als „globale berechnete Metriken“ oder „berechnete Report Suite-Metriken“ bezeichnet) in einer Report Suite über Admin Tools erstellen.

Globale berechnete Metriken gehören nun dem ersten Admin-Benutzer in der Liste der Admin-Firmen. Sie werden standardmäßig für &quot;Alle&quot;freigegeben. Dieses Muster folgt demselben Freigabemodell und denselben Migrationsplänen wie Segmente.

**Was Sie tun müssen**

Nichts. Der neue Admin-Inhaber sollte jedoch beim Ändern oder Löschen dieser berechneten Metriken vorsichtig sein - sie können in einer Reihe mit Lesezeichen versehenen Berichten und Dashboards verwendet werden.

>[!NOTE] Selbst wenn eine berechnete Metrik gelöscht wird, funktionieren alle Lesezeichen oder Dashboard-Berichte, die diese Metrik referenzieren, weiterhin.

## Was ist mit globalen berechneten Metriken passiert, die über Anmeldeunternehmen hinweg freigegeben wurden? {#section_59E5CD948ED643AE9AD3D2E4277647F8}

Bisher konnte ein Administrator berechnete Metriken (als „globale berechnete Metriken“ oder „berechnete Report Suite-Metriken“ bezeichnet) in einer Report Suite über Admin Tools erstellen. Diese Metriken können dann über Anmeldedaten hinweg &quot;freigegeben&quot;werden, indem die Report Suite zu mehreren Firmen für die Anmeldung hinzugefügt wird.)

Globale berechnete Metriken können nicht mehr über Anmeldedaten hinweg freigegeben werden. Sie sind nicht mehr an eine bestimmte Report Suite gebunden, sondern an eine bestimmte Firma der Anmeldung gebunden. Berechnete Metriken, die über Anmeldedaten hinweg freigegeben wurden

* werden in alle Anmeldeunternehmen mit Zugriff auf diese Report Suite migriert;
* werden standardmäßig für alle freigegeben;
* werden zu von allen anderen Anmeldeunternehmen unabhängigen Kopien.

>[!NOTE] Wenn die berechnete Metrik in einem Lesezeichen, Dashboard, Warnhinweis oder terminierten Bericht verwendet wurde, wirkt sich die Bearbeitung der neuen Kopie NICHT auf die alte beibehaltene berechnete Metrik aus.

## Was ist mit berechneten Metriken mit der Classification Numerisch oder Numerisch2 passiert? {#section_71AFE6C4A7CD4AA19AB3A9D3C41D115B}

(Previously, calculated metrics with a Numeric or Numeric2 classification were only visible in [!UICONTROL Reports & Analytics], [!UICONTROL Report Builder], and the APIs.)

Now, calculated metrics with a Numeric or Numeric2 classification will continue to be visible in [!UICONTROL Reports & Analytics], [!UICONTROL Report Builder], and the APIs. Sie werden allerdings in keinem Bericht mit einem angewendeten Segment unterstützt.

Darüber hinaus werden berechnete Metriken mit der Classification Numerisch oder Numerisch2 in den folgenden Komponenten nicht unterstützt: [!UICONTROL Ad Hoc Analysis], [!UICONTROL Analysis Workspace], [!UICONTROL Real-Time] Berichte [!UICONTROL Anomaly Detection]und [!UICONTROL Contribution Analysis]. Wenn Sie eine berechnete Metrik mit der Classification Numerisch oder Numerisch 2 erstellen oder bearbeiten, wird eine Kompatibilitätswarnung angezeigt, dass die berechnete Metrik nicht mit bestimmten Bereichen des Produkts kompatibel ist.

**Was Sie tun müssen**

Erstellen Sie keine berechneten Metriken mit den Classifications Numerisch1 oder Numerisch2, wenn die Metrik mit einem Segment oder mit einer der nicht kompatiblen Komponenten verwendet werden soll.

## Was ist mit Lebensdauermetriken passiert? {#section_AEDB02EF24584DAD8731BED9DDCE4F48}

Lebensdauermetriken werden nicht mehr unterstützt und sind nicht mehr in der Benutzeroberfläche von [!UICONTROL Reports & Analytics] oder einer anderen Komponente sichtbar. Sie können nicht von der Bericht-API abgefragt werden.

Alle Lesezeichen, Dashboard, terminierten Berichte oder Warnungen, die eine Zeitmetrik enthielten, werden weiterhin ohne diese Metrik ausgeführt, solange sich mindestens eine andere gültige Metrik auch im Bericht befindet. Wenn die einzige Metrik im Lesezeichen, Dashboard, terminierten Bericht oder Warnhinweis eine Allzeitmetrik ist, wird der Bericht nicht mehr ausgeführt.

## Was muss ich über berechnete Metriken basierend auf Metriken für tägliche/wöchentliche/monatliche/vierteljährliche/jährliche Unique Visitor wissen? {#section_E9A77EBB41CE4881B196CC1C282B2DF3}

Calculated metrics based on Unique Visitor metrics will be visible in the following [!DNL Analytics] components: [!UICONTROL Reports & Analytics], [!UICONTROL Report Builder], and Reporting API.

Diese Metriken werden jedoch in den folgenden Komponenten nicht unterstützt: [!UICONTROL Segments], [!UICONTROL Analysis Workspace], [!UICONTROL Real-Time] Berichte [!UICONTROL Anomaly Detection]und [!UICONTROL Contribution Analysis]. Wenn Sie eine berechnete Metrik erstellen oder bearbeiten, die auf Unique Visitors-Metriken basiert, wird eine Kompatibilitätswarnung angezeigt, dass die Metrik mit bestimmten Produktbereichen nicht kompatibel ist.

Sie verwenden eine Basis-Metrik für individuelle Besucher in einem Bericht mit einem Segment. Sie können berechnete Metriken, die auf Unique Visitor-Metriken basieren, zwar erstellen, aber diese berechneten Metriken können nicht auf Berichte mit Segmenten angewendet werden. Außerdem können keine Segmente in diese berechneten Metriken eingebettet werden.

## Was passiert mit berechneten Metriken, die mit den alten Report Suite-API-Methoden erstellt oder verwaltet wurden? {#section_13ED1BAD02634674BDAEB479B060A4B6}

Zuvor war das Speichern einer berechneten Metrik mit der API-Methode (1.3 oder 1.4) ReportSuite.SaveCalculatedMetrics identisch mit dem Erstellen oder Aktualisieren einer berechneten Metrik in der Admin-Konsole. Dasselbe gilt für ReportSuite.DeleteCalculatedMetrics. Außerdem war die Liste der berechneten Metriken, die in der Admin-Konsole oder beim Aufruf von ReportSuite.GetCalculatedMetrics angezeigt wurden, identisch.

Nun werden berechnete Metriken mit den ReportSuite CalculatedMetrics-API-Methoden (1.3 oder 1.4) weiterhin mit dem alten Speicher gespeichert, gelöscht und abgerufen. Vorhandene berechnete Metriken werden migriert und im neuen Generator für berechnete Metriken angezeigt. **Neue berechnete Metriken, die mit den API-Methoden erstellt wurden, sind nur in der API sichtbar. Sie können weiterhin in der Berichte-API verwendet werden.**

**Was Sie tun müssen**

Wenn Sie sowohl die API als auch den Generator für berechnete Metriken verwenden müssen, sollten Sie die ReportSuite CalculatedMetrics-API-Methoden nicht mehr verwenden und stattdessen die neuen CalculatedMetrics-API-Methoden (Get, Save, Delete und GetFunctions) verwenden.

## Unterstützt „Aktuelle Daten“ alle Typen an berechneten Metriken? {#section_1DAA718BB8DB4413BAF8AD4B4FAAFFA2}

Die aktuellen Daten unterstützen keine berechneten Metriken, die Segmente oder statistische Funktionen enthalten. Die einzigen Funktionen, die unterstützt werden, sind grundlegende mathematische Funktionen wie Addition, Löschen, Multiplikation, Division und Negation (-x).

## Was bedeutet „Kein Name angegeben“ im Zusammenhang mit migrierten berechneten Metriken? {#section_C90CBB72A67644F38D583301981F8D03}

„Kein Name angegeben“ bedeutet, dass kein Metrikname mit dieser migrierten Metrik verknüpft ist (lediglich eine Formel ohne einen beschreibenden Namen).

## Was passiert mit den berechneten Metriken eines Benutzers, wenn dieser Benutzer gelöscht wird? {#section_42ED4C15830540879C4A161423690E5A}

Alle von diesem Benutzer erstellten berechneten Metriken werden ebenfalls gelöscht. Gelöschte berechnete Metriken funktionieren jedoch weiterhin als Teil gespeicherter Lesezeichen, Dashboard oder terminierter Berichte.

## Warum werden „unbekannte“ berechnete Metriken angezeigt, die nicht für andere Report Suites „gültigׅ“ sind, obwohl sie erstellt und auf diese Report Suites angewendet werden können? {#section_6772818EFDED46E9B7095D64C3B77211}

In der Benutzeroberfläche wird „Unbekannt“ angezeigt, wenn die berechnete Metrik Basismetriken oder Dimensionen enthält, die nicht für die gewählte Report Suite vorhanden sind.

## Warum wurden Änderungen an meinen alten berechneten Metriken nicht gespeichert? {#section_81CDEFCA1FD542579AF183DA1494EAF0}

Dies kann auf den Zeitpunkt der Migration zur neuen Datenbank für berechnete Metriken zurückzuführen sein, die zwischen dem 15. Juni und dem 18. Juni 2015 stattfand.

**Was Sie tun müssen**

Sie müssen die Änderungen an Ihren alten Metriken wiederholen.

## Warum werden meine berechneten Metriken nicht im Marketing-Kanal-Bericht angezeigt? {#section_FC350359A775433AB5F43C7CAB304D62}

(Bisher wurden alle berechneten Metriken in der Metrikauswahl in Marketing-Kanal-Berichten mit der Option &quot;Erstkontakt&quot;und &quot;Letztkontakt&quot;aufgeführt.)

Jetzt stehen nur die berechneten Metriken, deren Zuordnungstyp im Generator für berechnete Metriken spezifisch auf &quot;Erstkontakt&quot;oder &quot;Letztkontakt&quot;festgelegt ist, in der Metrikauswahl in Marketing-Kanal-Berichten zur Verfügung. Beachten Sie, dass alle berechneten Metriken, die bereits auf Marketing Kanal-Berichte angewendet wurden, weiterhin angewendet werden und wie zuvor funktionieren. Um eine berechnete Metrik für Marketing-Kanal zu erstellen, klicken Sie auf das Konfigurationssymbol im Metrikaufbau und wählen Sie entweder &quot;Erstkontakt&quot;oder &quot;Letztkontakt&quot;als Zuordnungstyp aus. Denken Sie daran, dass die berechnete Metrik dadurch ausschließlich mit Marketing-Kanal-Berichten kompatibel ist und in keinen anderen Berichten verwendet werden kann.

## Warum enthalten einige der berechneten Metriken Formeln ohne die Klammern, die ich hinzugefügt habe? {#section_AC0D1E9714AD487F9A1C73359F518B5E}

Während der Migration hat Adobe überflüssige Klammern aus einigen Formeln entfernt. Es wurden nur Klammern entfernt, die keinen Einfluss auf die Berechnung der Metrik haben. Die Daten werden dadurch nicht geändert, es wird lediglich die Formel vereinfacht.

## (Nur Ad Hoc Analysis) Werden berechnete Metriken mit eingebetteten oder Inline-Segmentdefinitionen weiterhin unterstützt? {#section_B25C924A282F49388AB604E3D826F44C}

Berechnete Metriken, die in Ad-hoc-Analysen erstellt wurden, könnten zuvor Inline-Segmentdefinitionen enthalten. Das ist nicht mehr möglich.

**Was Sie tun müssen**

Sie müssen das Segment explizit speichern. Vorhandene berechnete Metriken mit Inline-Segmentdefinitionen werden weiterhin ordnungsgemäß ausgeführt und können in Ad Hoc Analysis angezeigt werden. Sie können allerdings nicht gespeichert werden, ohne das Segment explizit zu speichern.

## (Nur Report Builder) Warum sind berechnete Metriken aus meinen Anforderungen verschwunden? {#section_DA4792FE5D7945218CD5E6328DE08E82}

Wenn die Anforderung in Version 5.2 erstellt wurde und berechnete Metriken enthält, sind diese Metriken nicht in Version 5.1 (oder früheren Versionen) sichtbar. Dies liegt daran, dass berechnete Metriken jetzt globale IDs (nicht Report Suite-spezifische IDs) verwenden.

**Was Sie tun müssen**

Sie müssen auf Version 5.2 aktualisieren, um diese Metriken sehen zu können.

## Wie werden Gesamtwerte für berechnete Metriken ermittelt? {#section_57BA3A299C7948ABB82B0392A9B0F33E}

When [!UICONTROL Reports & Analytics] shows a calculated metrics total in [!UICONTROL Reports & Analytics], it&#39;s just applying the formula to the total. Beispielsweise nimmt die Summe für die berechnete Metrik Bestellungen/Besuch die Gesamtbestellungen und dividiert sie durch die Gesamtbesuche. In einigen Fällen ist der berechnete Metrikgesamtwert jedoch nicht nur die Summe der Einzelposten, sondern ein Gesamtwert für die Site.

Beispiel 1: Besucher für einen Suchbegriff: derselbe Besucher hat möglicherweise nach mehreren Begriffen gesucht. In diesem Fall entspricht der Gesamtwert der Besucher nicht der Summe der Einzelelemente.

Beispiel 2: Ansichten auf der Seite zu Produkten: im Warenkorb können mehrere Ansichten vorhanden sein, sodass der Warenkorb mehrere Seiten enthält. Weitere Informationen zum Vergleich der Summe der Zeilenelemente mit den Gesamtwerten finden Sie in [diesem Knowledge Base-Artikel](https://helpx.adobe.com/de/analytics/kb/sum-line-items-different-from-total.html).
