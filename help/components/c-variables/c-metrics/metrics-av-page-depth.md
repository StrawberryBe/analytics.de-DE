---
description: Zeigt an, wie tief (in Bezug auf die Seitenposition) jeder Wert während eines Besuchs durchschnittlich ausgelöst wurde. Diese Metrik gibt Aufschluss darüber, wie tief (in Bezug auf die Seitenposition) Ihre Zielgruppe während eines Besuchs eine bestimmte Seite oder einen Eigenschaftswert erreicht. „Durchschnittliche Klicktiefe“ ist für jede Variable verfügbar, für die die Pfadsetzung aktiviert ist.
seo-description: Zeigt an, wie tief (in Bezug auf die Seitenposition) jeder Wert während eines Besuchs durchschnittlich ausgelöst wurde. Diese Metrik gibt Aufschluss darüber, wie tief (in Bezug auf die Seitenposition) Ihre Zielgruppe während eines Besuchs eine bestimmte Seite oder einen Eigenschaftswert erreicht. „Durchschnittliche Seitentiefe“ ist für jede Variable verfügbar, für die die Pfadsetzung aktiviert ist.
seo-title: Durchschnittl. Seitentiefe
solution: Analytics
title: Durchschnittliche Klicktiefe
topic: Metriken
uuid: 4 d 8 a 3 a 3 c-c 698-4210-8 dd 8-a 02 a 1638483 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Durchschnittliche Klicktiefe

Zeigt an, wie tief (in Bezug auf die Seitenposition) jeder Wert während eines Besuchs durchschnittlich ausgelöst wurde. Diese Metrik gibt Aufschluss darüber, wie tief (in Bezug auf die Seitenposition) Ihre Zielgruppe während eines Besuchs eine bestimmte Seite oder einen Eigenschaftswert erreicht. „Durchschnittliche Klicktiefe“ ist für jede Variable verfügbar, für die die Pfadsetzung aktiviert ist.

Wenn ein Besuch beispielsweise den Pfad „Seite A &gt; Seite B &gt; Seite C &gt; Seite D &gt; Seite E &gt; Seite F“ enthält, ist die Tiefe ein Index für die Position der Seite. Beispielsweise hat „Seite A“ eine Tiefe von 0 und „Seite F“ eine Tiefe von 5. Der Durchschnitt berechnet sich dann aus einer Kombination aller Besuche. Eine Klicktiefe von unter eins (z. B. 0,9) bezieht sich auf den Mittelwert aller Seiten, die vor der fraglichen Seite besucht wurden.

Anhand der [!UICONTROL Klicktiefe] können Sie erkennen, wo eine gegebene Seite in der Regel in einen Benutzerpfad fällt, unabhängig von den vorherigen oder nächsten Seiten in diesem Pfad. Damit hilft diese Angabe zu erkennen, wie sich die Seite in das Gesamtbild der Besucherwahrnehmung Ihrer Website einfügt. Am deutlichsten zu erkennen ist dies in einem [!UICONTROL Seitenbericht].

<table id="table_E92B185A487C40E28C70EA30EDF73A40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verwendet </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Traffic </td> 
   <td colname="col2"> <p>Die Berechnung der Seitenereignisse und der angezeigten Seiten dividiert durch die Besuche ergibt die durchschnittliche Klickanzahl einer Seite. Betrachten Sie denselben Besuchspfad: </p> <p>A &gt; B &gt; B &gt; C &gt; D &gt; B </p> <p>Die Klickanzahl wird für jede Seite und jedes Seitenereignis berechnet, einschließlich der Neuladungen, wenn die Option „Wiederholte Instanzen zählen“ aktiviert ist (standardmäßig aktiviert in Ad Hoc Analysis und immer aktiviert in Marketing Reports and Analytics). Für Seite A beträgt die Klickanzahl bei diesem Besuch 0. Für Seite B würde die Klickanzahl 1, 2 und 5 betragen. Die Berechnung des Durchschnitts würde folgendermaßen erfolgen: [(1+2+5) / 3] = 2,67 Durchschnittliche Klicktiefe für Seite B. </p> <p>Wenn die Option „Wiederholte Instanzen zählen“ deaktiviert ist, erhält Seite B 1 und 4. Die Sekunde würde nicht mitgezählt. Die Berechnung würde folgendermaßen erfolgen: [(1+4) / 2 = 2,5] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Konversion </td> 
   <td colname="col2"> Keine </td> 
  </tr> 
 </tbody> 
</table>

>[!MORE_ LIKE_ THIS]
>
>* [Klicktiefebericht](/help/components/c-variables/dimensionslist/reports-page-depth.md)

