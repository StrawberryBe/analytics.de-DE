---
description: Eine Verweisanforderung verwendet Zellenwerte als Eingabe für Parameter, etwa als Daten- oder relationale Filter.
title: Verweisanforderungen kopieren
topic: Report builder
uuid: b6f64630-868f-455b-8682-471ff9fc596e
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Verweisanforderungen kopieren

Eine Verweisanforderung verwendet Zellenwerte als Eingabe für Parameter, etwa als Daten- oder relationale Filter.

Um Verweisanforderungen propagieren bzw. im Arbeitsblatt kopieren und einfügen zu können, muss das Arbeitsblatt mindestens eine gültige Anforderung enthalten. Darüber hinaus müssen die von der Anforderung erzeugten Daten eine Zelle enthalten, deren Wert entweder von einer Anforderung in einer anderen Zelle (mithilfe einer Aufschlüsselung oder eines passenden Filters) oder von einem Filter abhängt, der die Eingabe von Daten aus einer Zelle übernimmt.

Sie können außerdem Anforderungen erstellen, die auf Eingabefilter von Anforderungen in unterschiedlichen Arbeitsblättern verweisen, aber nicht in unterschiedlichen Arbeitsmappen. Beispielsweise kann eine Report Suite in Blatt 2 eine Report Suite aus einer bestimmten Zelle in Blatt 1 und einen Datumsbereich aus einer Zelle in Blatt 2 verwenden. Die neue Ausgabe kann in einem der beiden Blätter oder in einem neuen Blatt innerhalb der Arbeitsmappe positioniert werden. Wenn Sie eine relative Anforderung einfügen und sich ein Eingabefilter auf einem Arbeitsblatt befindet, das sich vom Arbeitsblatt, auf dem sich die Ausgabe der kopierten Anforderung befindet, unterscheidet, wird der Filter als absoluter Filter eingefügt.

>[!NOTE] Eine einzelne Anforderung kann nicht in mehreren Arbeitsblättern gleichzeitig ausgegeben werden. Darüber hinaus kann das System die kopierten Anforderungen nicht in neue Arbeitsmappen einfügen, wenn die Anforderungen Eingabefilter aus anderen Arbeitsblättern enthalten. Zu den Eingabeparametern zählen Report Suites aus Zellen, Datumsbereiche aus Filtern, Filter aus Zellen und andere zugehörige .

**So kopieren Sie Verweisanforderungen**

1. Wählen Sie die Zellen aus, die die zu kopierenden Anforderungen enthalten. Schließen Sie dabei die Eingabezelle oder die Zelle ein, auf die verwiesen wird.
1. Right-click within the highlighted cells and select **[!UICONTROL Copy Requests]** from the shortcut menu.

   Nach der Auswahl des Bereichs, in dem sich Anforderungen und Eingabezellen befinden, werden die Zellen mit diesen Elementen vom System hervorgehoben dargestellt.
1. Wählen Sie entweder eine Zelle oder einen Bereich angrenzender Zellen aus, in den die Anforderungen eingefügt werden sollen.

   Stellen Sie sicher, dass die ausgewählte Zelle bzw. der ausgewählte Bereich keine anderen Daten oder Anforderungen enthält.
1. Right-click the single cell or the top left-most cell in the range of cells and select **[!UICONTROL Paste Requests]**.

   Beim Einfügen von Anforderungen, die eine Eingabezelle enthalten, [!UICONTROL Paste Requests] umfassen die Optionen unter:

   **Absolute Eingabezelle verwenden:** Fügt eine Kopie der Anforderung(en) und der mit den ausgewählten Zellen verknüpften Formatierung in den von Ihnen markierten Einfügebereich ein. Die Eingabezelle (die Zelle, auf die in einer der ursprünglichen Anforderungen verwiesen wurde) wird nicht eingefügt. Stattdessen bleibt die Eingabezelle an derselben Position wie zuvor.

   **Relative Eingabezelle verwenden:** Fügt eine Kopie der Anforderung(en) und der mit den ausgewählten Zellen verknüpften Formatierung in den von Ihnen markierten Einfügebereich ein, einschließlich einer Kopie der Eingabezelle. Die räumliche Beziehung der Anforderung(en) zur Eingabezelle ist wie bei der/den ursprünglichen Anforderung(en). Während allerdings die neu eingefügten Zellen jetzt über eine Kopie der Anforderungen verfügen, befinden sich darin anfangs keine Inhalte. Dies liegt daran, dass bei der erneuten Erstellung der Eingabezelle durch die Einfügeoperation keine Daten damit verknüpft sind. Um Daten für die neu eingefügte(n) Anforderung(en) anzuzeigen, müssen Sie einen Wert in die Eingabezelle eingeben und dann die Anforderung(en) aktualisieren.
