---
title: Erstellen eines Klassifizierungssatzes
description: Verfügbare Felder und Beschreibungen beim Erstellen eines Klassifizierungssatzes.
exl-id: 6d692d90-8cc7-4306-a780-58d03db45be8
source-git-commit: 3b0e2bbe531692f26ed118b1d2adc0b5ed28a9bf
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Erstellen eines Klassifizierungssatzes

Sie können den Classification Set Manager verwenden, um einen Classification-Satz zu erstellen.

>[!NOTE]
>
>Diese Funktion ist derzeit in begrenztem Umfang verfügbar. Wenn Sie Zugriff auf diese Funktion wünschen, wenden Sie sich an die Kundenunterstützung von Adobe oder Ihren Kundenbetreuer, der Ihre Anfrage zur Bereitstellung an das Classifications-Team weiterleitet.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]** > **[!UICONTROL Sets]** > **[!UICONTROL Hinzufügen]**

Beim Erstellen eines Classification-Sets sind die folgenden Felder verfügbar.

* **[!UICONTROL Name]**: Ein Textfeld, mit dem der Klassifizierungssatz identifiziert wird. Dieses Feld kann bei seiner Erstellung nicht bearbeitet werden, kann aber später umbenannt werden.
* **[!UICONTROL Spaltenname]**: Der Name der Classification-Dimension, die Sie erstellen möchten. Dieses Feld ist der in Analysis Workspace verwendete Dimensionsname und der Spaltenname beim Exportieren von Classification-Daten.
* **[!UICONTROL Typ]**: Optionsfelder, die den Classification-Typ angeben. Normalerweise werden Primäre Klassifizierungen verwendet. Suchklassifizierungen stellen [Unterklassifizierungen](../c-sub-classifications.md).
* **[!UICONTROL Abonnements]** Die Report Suite und Dimension, für die dieser Classification-Satz gilt. Unterstützung für mehrere Report Suites ist geplant.

![Erstellen eines Klassifizierungssatzes](../assets/classification-set-create.png)

Wenn für eine bestimmte Report Suite + -Variable ein Classification-Satz vorhanden ist, wird stattdessen die Classification zum Schema hinzugefügt.
