---
description: Gelegentlich fallen einige Metriken beim Vergleich von Adobe Analytics- und DFA-Metriken gegebenenfalls nicht in eine akzeptable Differenz. Unten finden Sie eine Liste mit Metrikdefinitionen und möglichen Ursachen für Abweichungen.
keywords: DFA
title: Abgleich von Metrikdiskrepanzen
feature: Data Connectors
uuid: aa3ca006-d3cf-410e-a000-781ab17fb9e3
exl-id: bfe0f9cb-1bbc-40f9-b996-0002d5143889
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '1270'
ht-degree: 100%

---

# Abgleich von Metrikdiskrepanzen {#reconciling-metric-discrepancies}

Gelegentlich fallen einige Metriken beim Vergleich von Adobe Analytics- und DFA-Metriken gegebenenfalls nicht in eine akzeptable Differenz. Unten finden Sie eine Liste mit Metrikdefinitionen und möglichen Ursachen für Abweichungen.

Dieser Abschnitt enthält folgende Themen:

## Metrikdefinitionen {#metric-definitions}

Bei Adobe werden für Metriken in Bezug auf die DFA-Integration folgende Termini verwendet:

**Impressionen**: Anzahl der Ansichten einer Anzeige Sie werden pro Anzeige gemeldet, können aber auch in Anzeigengruppen oder anderen Gruppierungen mit mehreren Anzeigen zusammengefasst werden. Die Impressionsmetrik wird in Analytics über den nächtlichen Datenquellimport aus DFA importiert.

**Klicks**: Anzahl der Klicks auf eine Werbeanzeige wie von DFA gemeldet Sie werden auf der DFA-Weiterleitungsseite erkannt, bevor Besucher auf die Kundenwebsite gelangen. Wie bei Impressionen wird die Klickmetrik in Analytics über den nächtlichen Datenquellimport aus DFA importiert.

**Clickthroughs**: Anzahl der Besucher, die nach Klicken auf eine Anzeige auf die Landingpage gelangt sind. Diese Metrik kann leicht von den Klicks abweichen.

**Durchsichten**: Anzahl der Besucher, die nach Ansicht einer Anzeige auf die Kundenwebsite gelangt sind, aber NICHT auf die Anzeige geklickt haben. Besucher müssen die Site innerhalb eines bestimmten Durchsichtszeitfensters aufrufen – in der Regel 30 Tage. Die Impression muss vor dem letzten Klick verzeichnet worden sein. Durchsichten werden einmal pro Kampagne und Besuch erfasst. Sie werden gezählt, wenn die Durchsichts-eVar von der Integration durch die DFA-Kampagnen-ID ersetzt wird und das Durchsichtsereignis eingestellt ist.

## Mögliche Ursachen für Diskrepanzen {#possible-reasons-for-discrepancies}

Liste mit Ursachen für Datendiskrepanzen zwischen Adobe Analytics und DFA-Berichten

### Benutzer von Safari und anderen Browsern mit geblockten Drittanbietercookies  {#section-4b0dc429a54a4744a33976b0bb2d1b2a}

Meistens werden Diskrepanzen zwischen Adobe Analytics und DFA durch nicht zugelassene Drittanbietercookies verursacht. Bei Safari und einigen anderen Browsern werden Drittanbietercookies standardmäßig geblockt. Erstanbietercookies, die von den meisten Analytics-Implementationen verwendet werden, werden also standardmäßig von Safari und manchen anderen Browsern zugelassen, während die von DFA verwendeten Drittanbietercookies abgelehnt werden.

Anhand von Beispieldaten zu unseren Analytics 15 Beta-Kunden haben wir festgestellt, dass weniger als 0,5 % der Benutzer Erstanbietercookies in der Regel ablehnen, während 5-12% Drittanbietercookies ablehnen (ein Großteil davon ist wahrscheinlich auf Browserstandardeinstellungen zurückzuführen).

Diese Diskrepanz kann zu starken Abweichungen zwischen den von Analytics und den von DFA erfassten Daten führen.

### Woran kann es liegen, dass in DFA mehr Impressionen angezeigt werden als in Adobe Analytics?   {#section-db0ad070a65a4985bcc589b2d0d30b90}

* Daten werden in nächtlichen Batches von DFA an die Adobe-Datenerfassungsserver gesendet. Diese Daten in Analytics können also bis zu zwei Tage älter sein als die in DFA-Berichten.
* Adobe verwendet SAINT-Classifications zur Einteilung importierter DFA-Trackingcodes in verschiedene Sammelebenen (Kampagnenname, Platzierungsname, Anzeigenname usw.). Tritt die Diskrepanz beim Erstellen eines Classification-Berichts auf, können Sie anhand eines einfachen Tests herausfinden, ob die Klassifizierungen noch nicht mit den importierten Daten aktualisiert wurden:

   * Suchen Sie im Klassifizierungsbericht nach einem Zeilenelement mit der Bezeichnung „Ohne“.
   * Schlüsseln Sie dieses Zeilenelement nach derselben Variablen auf und verwenden Sie dabei den DFA-ID-Rohbericht (zum Beispiel Kampagnen-ID).
   * Notieren Sie sich aus diesem Bericht nicht klassifizierte DFA-Trackingcodes mit dem Format `DFA:XXXXX:XXXXX`.
   * Wenn Sie einen solchen Code finden, überprüfen Sie den nächtlichen SAINT-Classification-Prozess.

### Woran kann es liegen, dass in DFA mehr Klicks angezeigt werden als Clickthroughs in Adobe Analytics?   {#section-2fce4608ed044bdc9cf812cb719d5d35}

* DFA verzeichnet einen Klick, bevor Besucher auf die Kundenwebsite gelangen. Analytics verzeichnet Clickthroughs, nachdem die Landingpage geladen und das Adobe JavaScript-Beacon ausgeführt wurde. Solche Diskrepanzen entstehen also normalerweise dadurch, dass entweder Besucher nach dem Tracken eines Klicks durch DFA nicht auf die Landingpage gelangen oder  `s.maxDelay` abläuft.
* Stellen Sie sicher, dass alle Platzierungen und kreativen Inhalte in der Floodlight-Konfiguration „clickThroughParam“ in der Landingpage-URL (zum Beispiel „`?CID=1`“) enthalten. Wird dieser Parameter nicht eingestellt, werden Clickthroughs nach dem ersten Treffer des Besuchs nicht durch Adobe Analytics JavaScript verzeichnet.
* Überprüfen Sie, ob alle Platzierungen und kreativen Inhalte eine Landingpage aufweisen, die mit JavaScript getaggt ist und über das DFA Integrate-Modul verfügt, und ob die Floodlight-Konfigurations-ID auf dieser Landingpage mit der Floodlight-Konfigurations-ID der bereitgestellten Anzeigen übereinstimmt. Oft treten Diskrepanzen auf, weil die Anzeigenlandingpage auf eine Drittanbietersite oder auf bereitgestellte Anzeigen festgelegt ist.
* Stellen Sie sicher, dass der Besucherbrowser bei einem Treffer des DFA-Klicktrackers immer auch auf die Landingpage mit dem im Abfragestring enthaltenen `clickThroughParam` weitergeleitet wird, wenn Sie Rich Media- oder Flash-Anzeigen (swd) verwenden. Erfolgt keine Weiterleitung des Browsers, wird auch kein Clickthrough verzeichnet.
* Timeouts sind Fälle, in denen unter Umständen DFA-Daten verfügbar waren, aber bei JavaScript nicht rechtzeitig eine Reaktion einging. Gelangen Besucher auf die Landingpage, werden die Besucherinformationen durch Adobe JavaScript vom DFA-Service fls.doubleclick.net abgefragt. Durch den Parameter `s.maxDelay`wird festgelegt, wie lange JavaScript auf die Daten vom Floodlight-Service (FLS) wartet. Wenn `s.maxDelay` zu hoch eingestellt ist, kann es vorkommen, dass Besucher die Site verlassen, bevor Trefferdaten von Adobe erfasst werden können. In diesem Fall werden also keine Klickdaten verzeichnet. Wenn `s.maxDelay` zu niedrig eingestellt ist, können die FLS-Daten durch die Besucherinternetverbindung nicht rechtzeitig abgerufen werden. Es wird also ein Treffer ohne DFA-Klickinformationen an Adobe gesendet. 
* DFA-Klickzahlen können durch von Bots erzeugten Datenverkehr erhöht werden. Bots verfügen unter Umständen über Funktionen zum Klicken auf eine Anzeige, aber gegebenenfalls nicht über die Komplexität, ein Analytics-Beacon auszuführen oder das synchrone Script-Tag auszulösen, um die Floodlight-Serverabfragedaten zu laden. Werden diese Botaktivitäten nicht aus den Klickzahlen bereinigt, kann dies ebenfalls zu Diskrepanzen führen.
* Besucher, die die Seite verlassen, bevor  `s.maxDelay` abgelaufen ist und DFA-Daten zurückgegeben wurden, werden nicht erfasst und somit auch keine DFA- oder Besucherdaten zu ihnen.
* Analytics versucht, mehrfach auftretende Clickthroughs zu erkennen und zu entfernen, damit diese nur einmal pro Kampagne und Besuch gezählt werden. Bei DFA werden Besucher, die auf „Zurück“ klicken und mehrmals über die Anzeige weitergeleitet werden, als zusätzliche ACM-Klicks erfasst. Bei Analytics werden diese Clickthroughs nicht mehrfach gezählt.
* Für DFA Floodlight-Tags muss JavaScript nicht aktiviert sein, für Analytics schon. Daher kann es sein, dass DFA in einigen Fällen einen Treffer verzeichnet und Analytics nicht. Verwenden Sie den Analytics JavaScript-Bericht im Menü „Besucherprofil“, um herauszufinden, ob das ein Problem darstellen könnte.

### Woran kann es liegen, dass in DFA mehr Post-Impressionsaktivitäten angezeigt werden als Durchsichten in Adobe Analytics?   {#section-5daa91039c404df48b6a3447c20406f7}

* Analytics versucht, mehrfach auftretende Clickthroughs zu erkennen und zu entfernen, damit diese nur einmal pro Kampagne und Besuch gezählt werden. Bei DFA werden Besucher, die auf „Zurück“ klicken und mehrmals über die Anzeige weitergeleitet werden, als zusätzliche ACM-Klicks erfasst. Bei Analytics werden diese Clickthroughs nicht mehrfach gezählt.
* Für DFA Floodlight-Tags muss JavaScript nicht deaktiviert sein, für Analytics schon. Daher kann es sein, dass DFA in einigen Fällen einen Treffer verzeichnet und Analytics nicht. 
* Bei DFA werden Post-Impressionsaktionen gezählt, wenn Floodlight-Tags verwendet werden, die auf der Kundenwebsite platziert werden können. Bei Analytics werden Durchsichten erfasst, nachdem das JavaScript-Beacon (Bildabfrage) ausgeführt wurde. Durch die Codeplatzierung auf der Webseite können Sie festlegen, ob ein Besuch auf einer nicht vollständig geladenen Seite als Post-Impressionsaktivität oder Durchsicht gezählt wird.

### Was kann ich tun, wenn die Diskrepanzen in einem nicht akzeptablen Rahmen liegen und die möglichen Ursachen oben nicht zutreffen?   {#section-ca50eb75dd5d4d0396f4668b44d7547c}

Wenden Sie sich an Ihren Integrationsberater oder den Kundendienst von Adobe, um die Diskrepanzen zu dokumentieren und sie dem Data Connectors-Technikteam zu melden. Sie können die Bearbeitung Ihrer Anfrage mit Vergleichsdaten der betroffenen Metriken (auf Kampagnencodeebene) aus zwei bis drei Tagen beschleunigen. Geben Sie bei Ihrer Anfrage alle Lösungsversuche zur Diskrepanz an, die Sie bereits unternommen haben.
