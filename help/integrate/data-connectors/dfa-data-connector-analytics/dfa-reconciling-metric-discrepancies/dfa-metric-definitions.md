---
description: 'Bei Adobe werden für Metriken in Bezug auf die DFA-Integration folgende Termini verwendet '
keywords: DFA
seo-description: 'Bei Adobe werden für Metriken in Bezug auf die DFA-Integration folgende Termini verwendet '
seo-title: Metrikdefinitionen
solution: Analytics
title: Metrikdefinitionen
topic: Data Connectors
uuid: 062 f 6863-3 daa -4 e 8 a-b 6 ea -84279 d 49 c 388
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Metrikdefinitionen{#metric-definitions}

Bei Adobe werden für Metriken in Bezug auf die DFA-Integration folgende Termini verwendet:

**Impressionen**: Anzahl der Ansichten einer Anzeige Sie werden pro Anzeige gemeldet, können aber auch in Anzeigengruppen oder anderen Gruppierungen mit mehreren Anzeigen zusammengefasst werden. Die Impressionsmetrik wird in Analytics über den nächtlichen Datenquellimport aus DFA importiert.

**Klicks**: Anzahl der Klicks auf eine Werbeanzeige wie von DFA gemeldet Sie werden auf der DFA-Weiterleitungsseite erkannt, bevor Besucher auf die Kundenwebsite gelangen. Wie bei Impressionen wird die Klickmetrik in Analytics über den nächtlichen Datenquellimport aus DFA importiert.

**Clickthroughs**: Anzahl der Besucher, die nach Klicken auf eine Anzeige auf die Landingpage gelangt sind. Diese Metrik kann leicht von den Klicks abweichen.

**Durchsichten**: Anzahl der Besucher, die nach Ansicht einer Anzeige auf die Kundenwebsite gelangt sind, aber NICHT auf die Anzeige geklickt haben. Besucher müssen die Site innerhalb eines bestimmten Durchsichtszeitfensters aufrufen – in der Regel 30 Tage. Die Impression muss vor dem letzten Klick verzeichnet worden sein. Durchsichten werden einmal pro Kampagne und Besuch erfasst. Sie werden gezählt, wenn die Durchsichts-eVar von der Integration durch die DFA-Kampagnen-ID ersetzt wird und das Durchsichtsereignis eingestellt ist.
