---
title: Erstellen eines Classification-Sets
description: Verfügbare Felder und Beschreibungen beim Erstellen eines Classification-Sets.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
source-git-commit: d0e3b28590b24d630a192ee857a7d84c115dc8c1
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 28%

---

# Erstellen eines Classification-Sets

Sie können den Classification-Set-Manager verwenden, um einen Classification-Satz zu erstellen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen eines Classification-Sets stehen die folgenden Felder zur Verfügung.

* **[!UICONTROL Name]**: Ein Textfeld zur Identifizierung des Classification-Sets. Dieses Feld kann bei seiner Erstellung nicht bearbeitet werden, kann aber später umbenannt werden.
* **[!UICONTROL Spaltenname]**: Der Name der ersten Klassifizierungsdimension, die Sie erstellen möchten. Dieses Feld ist der in Analysis Workspace verwendete Dimensionsname und gleichzeitig der Spaltenname beim Exportieren von Klassifizierungsdaten. Sie können nach der Erstellung des Classification-Sets weitere Spaltennamen hinzufügen.
* **[!UICONTROL Typ]**: Optionsfelder, die den Typ der Klassifizierung angeben. Normalerweise werden primäre Klassifizierungen verwendet. Suchklassifizierungen stellen [Unterklassifizierungen](../../c-sub-classifications.md) dar.
* **[!UICONTROL Abonnements]** Die Report Suites und Dimensionen, für die dieser Classification-Satz gilt. Sie können einem Classification-Satz mehrere Report Suite- und Dimensionskombinationen hinzufügen.

![Erstellen eines Klassifizierungssatzes](../../assets/classification-set-create.png)

Wenn für eine bestimmte Report Suite + Variable ein Classification-Satz vorhanden ist, wird die Classification stattdessen zum Schema hinzugefügt. Eine Kombination aus Report Suite und Variable kann nicht zu mehreren Classification-Sets gehören.
