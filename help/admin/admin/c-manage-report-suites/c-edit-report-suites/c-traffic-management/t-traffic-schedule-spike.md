---
title: Planen einer Traffic-Spitze
description: Arbeiten Sie mit Adobe zusammen, um sicherzustellen, dass Ereignisse mit hohem Traffic keine Latenz erfahren.
feature: Traffic Management
exl-id: a6bbd975-6d31-40f5-8f80-491ec3a5c5f5
source-git-commit: c13e39e7bfe3d7fef07ea9ccda76255d28dde1c3
workflow-type: ht
source-wordcount: '738'
ht-degree: 100%

---

# Planen einer Traffic-Spitze

Adobe sucht die Partnerschaft mit Kunden, um den Erfolg eines Ereignisses mit hohem Traffic sicherzustellen. Die Planung von Traffic-Spitzen ist der Ausgangspunkt dieses Partnerschaftsprozesses. Im Abschnitt „Spitze planen“ können Sie Adobe vor temporären Traffic-Spitzen warnen, sodass ausreichende Ressourcen zugewiesen werden können. Sie können vergangene Server-Aufrufe schätzen, um eine bessere Vorstellung von der Traffic-Spitze zu bekommen, die Sie planen müssen.

Der erweiterte Server-seitige Datenausgleich mit mehreren dedizierten Mitarbeitern sorgt dafür, dass alle Kunden über die aktuellsten Berichte verfügen. Wenn Ihr Unternehmen Adobe über Traffic-Spitzen informiert, kann Adobe sicherstellen, dass der plötzliche Traffic-Anstieg ein positives Erlebnis darstellt. Wenn Adobe nicht über einen Traffic-Anstieg informiert wird, kann die Latenz in kritischen Reporting-Zeiträumen zunehmen.

{{$include /help/_includes/traffic-lead-time.md}}

## Planen einer Traffic-Spitze

So planen Sie eine Traffic-Spitze:

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Alle Administratoren]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie eine Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Traffic-Management]** > **[!UICONTROL Spitze planen]**.
1. (Optional) Sie können vergangene Server-Aufrufe schätzen, um eine bessere Vorstellung davon zu bekommen, wie groß die Traffic-Spitze ist, die Sie planen müssen.

   Hiermit können Sie beispielsweise die durchschnittliche Anzahl der Server-Aufrufe pro Tag im letzten Jahr innerhalb eines bestimmten Zeitrahmens abrufen und die erwartete Steigerung des Server-Aufrufvolumens für das aktuelle Jahr anzeigen. Anschließend können Sie anhand dieses Multiplikationsfaktors eine Traffic-Spitze planen.

   1. Wählen Sie unter **[!UICONTROL Vergangene Server-Aufrufe]** für die ausgewählten Report Suites ein Start- und ein Enddatum aus.

      Die Werte für [!UICONTROL **Spitzenwert pro Tag**], [!UICONTROL **Spitzenwert Server-Aufrufe pro Tag**] und [!UICONTROL **Tagesdurchschnitt an Server-Aufrufen**] werden generiert.

   1. Geben Sie einen Wert für den Multiplikationsfaktor ein und wählen Sie dann **[!UICONTROL Zum Multiplizieren und Festlegen klicken]** aus.

      Die Werte der einzelnen Spalten werden für die einzelnen Reports Suites multipliziert.
1. Geben Sie im Bereich [!UICONTROL **Spitzenparameter festlegen**] in das Feld **[!UICONTROL Spitzenstartdatum]** das Datum mit dem voraussichtlichen Beginn der Traffic-Spitze an.
1. Geben Sie im Feld **[!UICONTROL Spitzenenddatum]** ein, bis zu welchem Datum die Traffic-Spitze vermutlich anhalten wird.
1. Geben Sie in das Feld **[!UICONTROL Spitzenwert Server-Aufrufe pro Tag]** den erwarteten Spitzengesamtwert für die Seitenansichten pro Tag während der Traffic-Spitze an.
1. Geben Sie in das Feld **[!UICONTROL Spitzenwert Server-Aufrufe pro Stunde]** den erwarteten Spitzengesamtwert für die Seitenansichten pro Stunde während der Traffic-Spitze an.
1. Klicken Sie auf **[!UICONTROL Übermitteln]**.

   Achten Sie darauf, dass Sie die gesamten erwarteten Seitenaufrufe angeben, nicht nur die zusätzlichen Seitenaufrufe.

   >[!NOTE]
   >
   >Wenn Sie eine Traffic-Spitze planen, geben Sie bei Ihren Kontaktdaten eine Telefonnummer mit an, damit Adobe Sie bei Rückfragen erreichen kann.

## Warum es wichtig ist, Traffic-Spitzen immer zu planen

Wenn Kunden Adobe über Traffic-Spitzen für jede Report Suite informieren, unternimmt Adobe alles, um sicherzustellen, dass dies minimale Auswirkungen auf das Reporting hat.

* Organisationen mit geplanten Traffic-Spitzen erhalten Priorität, wenn Daten latent werden. Die Bedeutung dieses Konzepts ist besonders während der Urlaubszeit von entscheidender Bedeutung, wenn viele Unternehmen Traffic-Spitzen planen.
* Wenn Adobe feststellt, dass Sie den erwarteten Traffic im Vergleich zu Vorjahren erheblich überschätzt/unterschätzt haben, können Sie kontaktiert werden, um Genauigkeit sicherzustellen.
* Es ist wichtig, jedes Jahr eine Traffic-Spitze zu planen, auch wenn bei Ihrer Organisation jedes Jahr die gleiche Spitze vorliegt. Viele Unternehmen veröffentlichen im Laufe des Jahres neue Mobile Apps, kombinieren Report Suites und migrieren bzw. deaktivieren Report Suites. Adobe kann nur dann feststellen, welche Report Suites zusätzlichen Traffic erhalten, wenn Ihr Unternehmen jedes Mal eine Traffic-Spitze plant. Adobe nutzt Verlaufsdaten zur Einschätzung; und es ist wichtig, dass zusätzliche Ressourcen der richtigen Report Suite hinzugefügt werden.

## Aktionen, die Ihre Organisation unternehmen kann

Adobe möchte sicherstellen, dass Ihr Erlebnis mit aktuellem Reporting konsistent ist. Um diese Aufgabe optimal zu erfüllen, empfiehlt Adobe dringend Folgendes:

* Planen Sie Vorlaufzeiten für alle Traffic-Spitzen. **Es ist besonders wichtig, dass alle in den Monaten November und Dezember erwarteten Traffic-Spitzen bis zum 15. September geplant werden**. Wenn Sie die Frist verpassen, planen Sie Ihre Spitze so bald wie möglich. Weniger Vorlaufzeit ist besser als keine, und Adobe arbeitet mit den aktuellen Ressourcen, um Ihre Report Suites optimal zu berücksichtigen.
* Wenn Sie von Adobe bezüglich einer geplanten Traffic-Spitze kontaktiert werden, geben Sie auf jeden Fall an, ob Echtzeit-Reporting oder Reporting zur vollständigen Verarbeitung wichtiger ist. Einige Organisationen stützen sich mehr auf Echtzeit-Reporting als andere. Wenn Sie wissen, welchen Reporting-Typ Sie verwenden, können Sie Adobe bei der entsprechenden Priorisierung helfen.
* Wenn Sie Ihrem Account Manager mitteilen, welche Berichte am wichtigsten sind und wann Sie sie abrufen, können Sie unterstützt werden.
