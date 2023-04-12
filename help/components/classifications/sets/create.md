---
title: Erstellen eines Klassifizierungssatzes
description: Verfügbare Felder und Beschreibungen beim Erstellen eines Klassifizierungssatzes.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 100%

---

# Erstellen eines Klassifizierungssatzes

Sie können den Classification Set Manager verwenden, um einen Klassifizierungssatz zu erstellen.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen eines Klassifizierungssatzes sind die folgenden Felder verfügbar.

* **[!UICONTROL Name]**: Ein Textfeld, mit dem der Klassifizierungssatz identifiziert wird. Dieses Feld kann bei seiner Erstellung nicht bearbeitet werden, kann aber später umbenannt werden.
* **[!UICONTROL Spaltenname]**: Der Name der Klassifizierungsdimension, die Sie erstellen möchten. Dieses Feld ist der in Analysis Workspace verwendete Dimensionsname und gleichzeitig der Spaltenname beim Exportieren von Klassifizierungsdaten.
* **[!UICONTROL Typ]**: Optionsfelder, die den Typ der Klassifizierung angeben. Normalerweise werden primäre Klassifizierungen verwendet. Suchklassifizierungen stellen [Unterklassifizierungen](../c-sub-classifications.md) dar.
* **[!UICONTROL Abonnements]** Die Report Suite und Dimension, für die dieser Klassifizierungssatz gilt. Unterstützung für mehrere Report Suites ist geplant.

![Erstellen eines Klassifizierungssatzes](../assets/classification-set-create.png).

Wenn für eine bestimmte Report Suite und Variable ein Klassifizierungssatz vorhanden ist, wird stattdessen die Klassifizierung zum Schema hinzugefügt.
