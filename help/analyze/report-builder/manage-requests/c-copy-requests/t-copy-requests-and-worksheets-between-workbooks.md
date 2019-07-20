---
description: Kopieren Sie ein ganzes Arbeitsblatt aus einer Quellarbeitsmappe in eine oder mehrere andere Arbeitsmappen.
seo-description: Kopieren Sie ein ganzes Arbeitsblatt aus einer Quellarbeitsmappe in eine oder mehrere andere Arbeitsmappen.
seo-title: Anforderungen und Arbeitsblätter zwischen Arbeitsmappen kopieren
solution: Analytics
title: Anforderungen und Arbeitsblätter zwischen Arbeitsmappen kopieren
topic: ReportBuilder
uuid: 6 b 2 c 4259-d 8 cb -430 e -819 f -38 e 213 dd 2661
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Anforderungen und Arbeitsblätter zwischen Arbeitsmappen kopieren

Kopieren Sie ein ganzes Arbeitsblatt aus einer Quellarbeitsmappe in eine oder mehrere andere Arbeitsmappen.

Hierfür müssen Sie mindestens zwei Arbeitsmappen in derselben Excel-Instanz geöffnet haben: Die erste Quellarbeitsmappe enthält eine Tabelle (Arbeitsblatt) mit Zellen zugeordneten Anforderungen, während die zusätzliche Zielarbeitsmappe die Zielorte enthält. Für jede neue Zielarbeitsmappe müssen Sie sich   bei derselben Report Suite wie die Quellarbeitsmappe anmelden, bevor Sie Tabellen, die Anforderungen enthalten, einfügen können.
1. Klicken Sie mit der rechten Maustaste auf das Arbeitsblatt in der Quellarbeitsmappe und wählen Sie **[!UICONTROL Arbeitsblatt mit Anforderungen kopieren]**.
1. In the destination workbook, right-click the spreadsheet and select **[!UICONTROL Paste Worksheet w/Requests]**.

   Dieselbe Instanz von Excel bedeutet, dass nur ein einziger Excel-Prozess ([!DNL excel.exe]) auf dem Computer ausgeführt wird. Wenn Sie zwei Instanzen von Excel starten und versuchen, eine Arbeitsmappe aus der ersten Instanz von Excel in eine Arbeitsmappe in die zweite Instanz von Excel zu kopieren, stellt ReportBuilder die Option zum Einfügen eines Arbeitsblatts im Kontextmenü der zweiten Instanz von Excel nicht zur Verfügung.

   Wenn Sie sich bei der Quell- und Zielarbeitsmappe für unterschiedliche Report Suites anmelden, sind als Ergebnis der Einfügeoperation in der Zielarbeitsmappe ausschließlich die Formatierungen sichtbar. ReportBuilder zeigt eine Meldung darüber an, dass die Informationen für die Anforderungen einer bestimmten Report Suite (in der Quellarbeitsmappe) nicht in der Zielarbeitsmappe verfügbar sind. Um die in die Zielarbeitsmappe eingefügten Anforderungen sichtbar zu machen, müssen Sie sich zuerst in der Zielarbeitsmappe für dieselbe Report Suite wie in der Quellarbeitsmappe anmelden.

   Sie können eine oder mehrere Anforderungen aus einem Arbeitsblatt in einer Arbeitsmappe kopieren und in ein Arbeitsblatt in einer anderen Arbeitsmappe einfügen, sofern die zweite Arbeitsmappe als weiteres Dokument in derselben Instanz von Excel geöffnet ist. Die Anforderungen in beiden Arbeitsmappen müssen mit Hilfe derselben Report Suite erstellt werden.
