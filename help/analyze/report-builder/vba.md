---
title: Visual Basic-Makros in Report Builder
description: Erweitern Sie die Funktionalität von Excel-Arbeitsmappen und Report Builder mit VBA.
feature: Report Builder
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 98%

---


# Visual Basic-Makros in Report Builder

Mit VBA-Makros, auch Visual Basic-Makros genannt, können Sie Arbeitsmappen so bearbeiten, wie es Microsoft Excel allein nicht kann. Visual Basic hat Zugriff auf die Arbeitsmappe, Excel und sogar auf Windows.

Adobe unterstützt drei Report Builder-API-Methoden. Stellen Sie sicher, dass die neueste Version von Report Builder installiert ist, und melden Sie sich an, bevor Sie Makros ausführen.

>[!IMPORTANT]
>
>Aus Sicherheitsgründen ist es nicht möglich, eine Arbeitsmappe mit einem Makro zu planen.

## `RefreshAllReportBuilderRequests()`

Das `RefreshAllReportBuilderRequests()`-Makro aktualisiert alle Report Builder-Anforderungen in der aktiven Arbeitsmappe. Zunächst wird das COM-Add-In von Report Builder über seine Produkt-ID und anschließend der `RefreshAllRequests()`-API-Befehl aufgerufen:

```vba
Sub RefreshAllReportBuilderRequests()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshAllRequests(ActiveWorkbook)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInActiveWorksheet()`

Das `RefreshAllReportBuilderRequestsInActiveWorksheet()`-Makro aktualisiert alle Report Builder-Anforderungen im aktiven Arbeitsblatt. Der `RefreshWorksheetRequests()`-API-Aufruf verwendet ein Arbeitsblattobjekt als Argument. Sie können diesen Aufruf für jedes Arbeitsblatt verwenden, das Report Builder-Anforderungen enthält:

```vba
Sub RefreshAllReportBuilderRequestsInActiveWorksheet()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshWorksheetRequests(ActiveWorkbook.ActiveSheet)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInCellsRange()`

Das `RefreshAllReportBuilderRequestsInCellsRange()`-Makro aktualisiert alle Report Builder-Anforderungen, deren Zellenausgabe den angegebenen Zellbereich überschneidet. Der in diesem Beispiel verwendete Zellbereich verweist auf den Bereich `B1:B54` des „Data“-Arbeitsblatts in der aktiven Arbeitsmappe. Der Bereichsausdruck unterstützt alle unterstützten Bereichsausdrücke in Excel:

```vba
Sub RefreshAllReportBuilderRequestsInCellsRange()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshRequestsInCellsRange("'Data'!B1:B54")
  
End Sub
```
