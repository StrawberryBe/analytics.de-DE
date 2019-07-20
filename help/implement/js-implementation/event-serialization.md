---
description: 'Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in die Analytics-Berichterstattung aufgenommen werden. Dazu kann es kommen, wenn ein Benutzer die Seite mehrmals aktualisiert, mehrmals zu einer bestimmten Seite navigiert oder die Webseite auf einem Computer speichert. (Beispiel: Wenn ein Kunde eine Kaufbestätigungsseite auf seinem Computer speichert, würden Bestellungen und Umsatz jedes Mal, wenn der Kunde die Seite anzeigt, erneut gezählt, wenn die Ereignis-Serialisierung nicht eingerichtet wäre.)'
keywords: Analytics-Implementierung
seo-description: 'Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in die Analytics-Berichterstattung aufgenommen werden. Dazu kann es kommen, wenn ein Benutzer die Seite mehrmals aktualisiert, mehrmals zu einer bestimmten Seite navigiert oder die Webseite auf einem Computer speichert. (Beispiel: Wenn ein Kunde eine Kaufbestätigungsseite auf seinem Computer speichert, würden Bestellungen und Umsatz jedes Mal, wenn der Kunde die Seite anzeigt, erneut gezählt, wenn die Ereignis-Serialisierung nicht eingerichtet wäre.)'
seo-title: Übersicht über die Ereignis-Serialisierung
solution: Analytics
title: Übersicht über die Ereignis-Serialisierung
topic: Entwickler und Implementierung
uuid: 8 c 7883 bb -5 ba 4-4440-af 80-c 0 d 15867570 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Übersicht über die Ereignis-Serialisierung

Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in die Analytics-Berichterstattung aufgenommen werden. Dazu kann es kommen, wenn ein Benutzer die Seite mehrmals aktualisiert, mehrmals zu einer bestimmten Seite navigiert oder die Webseite auf einem Computer speichert. (Beispiel: Wenn ein Kunde eine Kaufbestätigungsseite auf seinem Computer speichert, würden Bestellungen und Umsatz jedes Mal, wenn der Kunde die Seite anzeigt, erneut gezählt, wenn die Ereignis-Serialisierung nicht eingerichtet wäre.)

Die [!UICONTROL Ereignis-Serialisierung] ist in den folgenden Fällen nützlich:

* Eine Seite wird erneut geladen oder aktualisiert und sendet dann ein Ereignis, das schon einmal registriert wurde. Mittels [!UICONTROL Ereignis-Serialisierung] kann verhindert werden, dass Ereignisse mehrfach gezählt werden.
* Der Benutzer speichert die Seite lokal auf seinem Computer, um sie später anschauen zu können. Dieses Problem tritt besonders häufig bei Bestätigungsseiten für Einkäufe auf, die vom Benutzer gespeichert werden, um die Kaufbestätigungen überprüfen zu können. Mittels [!UICONTROL Ereignis-Serialisierung] kann verhindert werden, dass spätere Seitenaufrufe mehrfach als Ladeereignis gezählt werden.

>[!NOTE]
>
>Data Sources unterstützt keine Ereignis-Serialisierung oder Deduplizierung.

In diesem Dokument wird die Vorgehensweise zum Implementieren von [!UICONTROL Ereignis-Serialisierung] für [!UICONTROL Konversions]- und [!UICONTROL benutzerspezifische] Ereignisse beschrieben. To use [!UICONTROL Event serialization], you must first enable it in  **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suite]** &gt; **[!UICONTROL[select report suite]]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Success Events]** . Wählen Sie dann in der Spalte „[!UICONTROL Eindeutige Ereignisaufzeichnung]“ aus, welche Ereignisse aufgezeichnet werden sollen.

## Standardmäßige Verhaltensweise {#section_892BB2BEFC434B69869D4504A8B54308}

Die standardmäßige Verhaltensweise besteht darin, dass jedes einzelne Eintreten eines Ereignisses gezählt wird. Ein Ereignis wird für jede [!UICONTROL Seitenansicht] festgelegt, die gezählt wird (selbst wenn die Seite nur aktualisiert oder erneut geladen wird). Mithilfe der Variablen [!UICONTROL s.purchaseID] werden die einzelnen Bestellungen (Einkäufe) eindeutig identifiziert. Dadurch werden Bestellungen, Umsätze oder Produkte nicht mehrmals gezählt, wenn ein Benutzer seine Seite erneut lädt. Eine ähnliche Funktion ist bei allen Ereignissen verfügbar. Dazu gehören vordefinierte Ereignisse wie [!UICONTROL prodView] und [!UICONTROL scCheckout] sowie alle benutzerspezifischen Ereignisse.

<!-- 

event_serialization_impl.xml

 -->

To use [!UICONTROL Event serialization], you must first enable it in  **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suite]** &gt; **[!UICONTROL[select report suite]]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Success Events]** . Wählen Sie dann in der Spalte „[!UICONTROL Eindeutige Ereignisaufzeichnung]“ aus, welche Ereignisse aufgezeichnet werden sollen. Ein Ereignis kann auf drei unterschiedliche Einstellungen gesetzt werden.

**Ereignis immer aufzeichnen**: Dies ist das vorgegebene Verhalten aller Ereignisse bei der erstmaligen Aktivierung. Alle in Bildanforderungen enthaltenen Ereignisse werden direkt an Analytics gesendet, einschließlich des Neuladens von Seiten.

**Einmal pro Besuch aufzeichnen**: Wenn diese Einstellung für ein Ereignis aktiviert ist, wird nur die erste Instanz dieses Ereignisses beim betreffenden Besuch aufgezeichnet. Bei einem neuen Besuch wird jedes Ereignis, für das diese Einstellung aktiviert ist, erneut nachverfolgt. So können doppelte Ereignisse aufgrund von Aktualisierungen des Browsers effektiv reduziert werden.

**Ereignis-ID verwenden**: Mit dieser Einstellung können Sie jedem Ereignis eine eindeutige ID zuweisen. Wenn Analytics eine eventID erkennt, die bereits zuvor mit dieser Variablen aufgetreten ist, wird das Ereignis nicht in den Bericht aufgenommen.

Das Kaufereignis ist das einzige Ereignis, für das keine Ereignis-Serialisierung aktiviert werden kann, da es die Variable s.purchaseID verwendet. Für alle anderen E-Commerce-Ereignisse und benutzerspezifischen Ereignisse können diese Einstellungen aktiviert werden.

* Einsatz einer eindeutigen ID, damit ein Ereignis für jede individuelle ID nur einmal ausgelöst wird
* Senden mehrerer Ereignisse und dann entsprechende Konfiguration von Analytics, sodass ein Ereignis nur einmal pro Besuch ausgelöst wird

Für die Implementierung von [!UICONTROL Ereignis-Serialisierung] geben Sie für das Ereignis eine eindeutige ID an (z. B. event1:1234ABCD).

## Ereignis-Serialisierung – Einmal pro eindeutiger ID {#section_8806E48B497546F5A335383FB8627694}

Wenn nach der Implementierung von [!UICONTROL Ereignis-Serialisierung] IDs mehrmals bei [!DNL Analytics] eingehen, wird das Ereignis ignoriert. Ein Ereignis wird nur einmal pro eindeutigem Wert gezählt. Wenn die Nummer eindeutig ist, wird dies als ein weiteres Eintreten des Ereignisses gezählt (siehe Beispiel):

| Benutzername | Beschreibung | Syntax für das Ereignis | In Analytics vermerkte Gesamtanzahl von Event1 |
|---|---|---|---|
| John | Der Benutzer zeigt die Seite zum ersten Mal an. | event1:1000 | 1 |
| John | Der Benutzer lädt die Seite erneut (möglicherweise ist die Übermittlung eines Formulars fehlgeschlagen, sodass die Seite erneut geladen wird). | event1:1000 | 1 |
| Stacy | Der Benutzer zeigt die Seite zum ersten Mal an. | event1:1001 | 2 |
| Stacy | Der Benutzer lädt die Seite erneut (möglicherweise ist die Übermittlung eines Formulars fehlgeschlagen, sodass die Seite erneut geladen wird). | event1:1001 | 2 |
| Jill | Der Benutzer zeigt die Seite zum ersten Mal an, gibt Informationen korrekt ein und wechselt zur nächsten Seite. | event1:1002 | 3 |
| Jamie | Der Benutzer zeigt die Seite zum ersten Mal an. | event1 | 4 |
| Jamie | Der Benutzer vergisst, seinen Nachnamen in das Formular einzugeben. Das Formular wird erneut angezeigt, wobei die fehlende Angabe markiert ist. | event1 | 5 |

Beachten Sie Folgendes beim Auswählen von Serialisierungs-IDs:

* Serialisierungs-IDs dürfen maximal 20 Zeichen umfassen.
* Serialisierungs-IDs müssen aus alphanumerischen Zeichen bestehen.
* Serialisierungs-IDs werden für jedes Erfolgsereignis einzeln vergeben. Daher können Sie dieselbe ID für mehrere Erfolgsereignisse verwenden, aber nie dieselbe ID für zwei gleiche Erfolgsereignisse.
* Serialisierungs-IDs sind mit der Report Suite verknüpft. Beachten Sie dies, wenn Sie Multi-Site-Tagging verwenden, um Daten an mehrere Report Suites zu senden.
* Serialisierungs-IDs laufen niemals ab. Wenn dieselbe ID also selbst nach Jahren wieder verwendet wird, wird das Erfolgsereignis nicht erneut gezählt.
* Die Serialisierung von Ereignis-IDs wird nicht durch das Löschen von Cookies beeinträchtigt, da Serialisierungs-IDs auf Adobe-Servern gespeichert und nicht von Cookies abhängig sind.
* Das einzige Erfolgsereignis, für das keine Serialisierung der Ereignis-IDs möglich ist, ist das Kaufereignis, da dies für die Serialisierung die gesonderte Variable „s.purchaseID“ verwendet.

## Ereignis-Serialisierung – einmal pro Besuch {#section_C919D44F321A47FBBF043D0C57A2A050}

[!DNL Analytics] verfügt über ein Feature, mit dem ein Ereignis nur einmal pro Besuch ausgelöst werden kann.

This can be enabled from the UI:  **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suite]** &gt; **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL Conversion]** &gt; **[!UICONTROL Success Events]** .
