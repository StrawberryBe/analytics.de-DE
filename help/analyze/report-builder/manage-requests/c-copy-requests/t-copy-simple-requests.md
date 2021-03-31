---
description: Kopieren Sie eher eine einfache Anforderung als eine Verweisanforderung. Eine einfache Anforderung enthält keine Verweise auf andere Anforderungen oder die Inhalte einer Zelle.
title: Einfache Anforderungen kopieren
uuid: ff20560a-01ee-47e7-8bd1-b73edb010456
feature: Report Builder
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 99%

---


# Einfache Anforderungen kopieren

Kopieren Sie eher eine einfache Anforderung als eine Verweisanforderung. Eine einfache Anforderung enthält keine Verweise auf andere Anforderungen oder die Inhalte einer Zelle.

Eine [Verweisanforderung](/help/analyze/report-builder/manage-requests/c-copy-requests/t-copy-referential-requests.md) verwendet Werte aus Zellen als Eingabe für Parameter, etwa als Daten- oder relationale Filter. Diese Filter verwenden entweder Übereinstimmungen oder Trenderstellung und basieren auf den Ergebnissen einer früheren Anforderung oder auf dem vom Benutzer eingegebenen Inhalt einer Zelle. Eine solche Zelle wird Eingabezelle genannt.
1. Es muss eine gültige Anforderung erstellt werden.
1. Klicken Sie mit der rechten Maustaste auf eine der Zellen, die der Anforderung zugeordnet ist, oder wählen Sie einen Bereich von Zellen aus, der Anforderungen enthält.

   Gehen Sie bei der Auswahl von zu kopierenden Zellen aus der Gruppe von Zellen, die von der Anforderung abgedeckt sind, einheitlich vor. Es bietet sich an, mit der Zelle ganz oben links in der Gruppe der Zellen, die von der Anforderung abgedeckt sind, zu beginnen und dann von links nach rechts weiterzumachen. Dies hat seine Ursache darin, dass ein Excel-Arbeitsblatt über hunderte von Spalten und tausende von Zeilen verfügt, die für die Erweiterung nach rechts und unten zur Verfügung stehen. Wenn Sie das Kopieren einer Anforderung mit einer Zelle beginnen, die sich am äußersten rechten oder unteren Rand des Bereichs von Zellen, die von der Anforderung abgedeckt sind, können Sie die Anforderung nicht einfügen, wenn der Bereich der einzufügenden Zellen über den linken oder oberen Rand des Arbeitsblatts hinausgeht.
1. Wählen Sie **[!UICONTROL Anforderung kopieren]**.
1. Klicken Sie in einem anderen Bereich des Arbeitsblatts mit der rechten Maustaste auf eine leere Zelle (d. h. eine Zelle, die keine Anforderung enthält).

   Damit keine bereits erstellten Anforderungen verloren gehen oder beschädigt werden, ist es nicht möglich, Zellen mit Anforderungen in Zellen zu kopieren, die bereits Anforderungen zugeordnet sind. Wenn Sie Zellen kopieren oder ausschneiden, die Anforderungen enthalten, ist im Kontextmenü beim Rechtsklicken auf Zellen (oder Zellenbereiche), die Anforderungen enthalten, die Option [!UICONTROL Anforderungen einfügen] nicht verfügbar. Sie müssen eine andere Zelle als Ziel der Einfügeoperation wählen, damit sich die Anforderungen nicht überschneiden. Dies gilt sowohl für einzelne Zellen, die einzufügende Anforderungen enthalten, als auch ganze Zellenbereiche.
1. Klicken Sie auf **[!UICONTROL Anforderungen einfügen]**.

   Eine Kopie der ursprünglichen Anforderung wird in den Zellen in einer Position bzw. Positionen relativ zur ursprünglichen Anforderung abgelegt.

   >[!NOTE]
   >
   >Nur die Anforderungen werden kopiert, nicht die Zelleninhalte. Wenn weitere Informationen vorhanden sind, die nicht auf Anforderungen basieren, aber für das Verständnis der in den Zellen angezeigten Daten erforderlich sind (z. B. Spalten- oder Zeilenbezeichnungen der Tabelle), verwenden Sie die Excel-Standardbefehle für das Kopieren und Einfügen.

   Da Excel für das Kopieren von Zellinhalten und das Kopieren von Anforderungen unterschiedliche Zwischenablagen verwendet, können Sie nicht aus Anforderungen stammende Inhalte und dann Anforderungen kopieren, indem Sie nacheinander „Kopieren“/„Einfügen“ und „Anforderungen kopieren“/„Anforderungen einfügen“ ausführen. Wenn Sie allerdings auf die Anforderungen im Arbeitsblatt vor dem Kopieren und Einfügen Formatierungen anwenden, wird die ursprüngliche Formatierung (hinsichtlich Rahmen, Schriften usw.) von ReportBuilder im Einfügebereich beibehalten.

   Durch das Ändern einer Anforderung, die Sie kopiert oder in die Zwischenablage ausgeschnitten haben, wird die Anforderung aus der Zwischenablage entfernt. Um die Anforderung in ihrem ursprünglichen Zustand zu belassen, ändern Sie sie nicht zwischen dem Zeitpunkt des Kopierens und dem Zeitpunkt des Einfügens.
