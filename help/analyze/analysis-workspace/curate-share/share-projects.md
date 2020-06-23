---
description: Projektfreigabe und Projektrollen in Workspace
keywords: Analysis Workspace sharing
title: Freigeben von Workspace-Projekten
translation-type: tm+mt
source-git-commit: 324460b89adf55c450d68bdb4fdc884e53f86257
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 6%

---


# Freigeben von Workspace-Projekten

Durch Freigabe wird ein Projekt anderen Analysis Workspaces in Ihrem Unternehmen zur Verfügung gestellt. Jede [Kuration](curate.md) , die Sie vorgenommen haben, wird angezeigt, wenn Empfänger das Projekt öffnen.

## Projektrollen {#Roles}

Sie können einer von drei Projektrollen Empfänger hinzufügen. Projektrollen sind mit dem Benutzer und der spezifischen Projekt-ID verknüpft. Projektrollen sind unabhängig von Benutzerberechtigungen, die in der [Adobe Experience Cloud-Admin-Konsole](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/admin-getting-started.html)verwaltet werden.

| Rolle | Projektsteuerung |
|---|---|
| Kann bearbeiten | Empfänger können Änderungen an einem Projekt „Speichern“ und als Miteigentümer auftreten. Diese Rolle ist nützlich, wenn Sie Projekte mit anderen Kollegen gemeinsam bearbeiten möchten.<br>Hinweis: Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. Es wird daher empfohlen, ein Projekt zu einem bestimmten Zeitpunkt nur von einem Benutzer zu bearbeiten. Wenn Projekte gleichzeitig gespeichert werden, wird die letzte Version beibehalten. |
| Kann duplizieren | Empfänger können &quot;Speichern unter&quot;wählen und auf die linke Leiste zugreifen. Projektinteraktionen sind in dieser Rolle nicht beschränkt. Diese Rolle ist nützlich, wenn Sie ein Projekt für Benutzer freigeben möchten, die die Daten Ihres Unternehmens und die Verwendung von Analysis Workspace verstehen, Ihr Projekt jedoch nicht ändern möchten. |
| Kann anzeigen | Empfänger können nicht speichern unter und haben keinen Zugriff auf die linke Leiste. Auch die Projektinteraktionen sind begrenzt. Diese Rolle ist hilfreich, wenn Sie ein Projekt für Benutzer freigeben möchten, die mit der Datenstruktur Ihres Unternehmens, dem Analysis Workspace oder Adobe Analytics im Allgemeinen nicht so vertraut sind. Sie möchten jedoch weiterhin, dass sie Daten und Erkenntnisse in einer sicheren Umgebung nutzen.<br>Erfahren Sie mehr über das Projekterlebnis [Can Ansicht](/help/analyze/analysis-workspace/curate-share/view-only-projects.md). |

>[!IMPORTANT]
> Vor dem 18. Juni 2020 hinzugefügte Empfänger wurden in eine Projektrolle migriert. Administratorbenutzer migrierten in die Rolle &quot; **[!UICONTROL Kann bearbeiten]** &quot;und Nicht-Admin-Benutzer migrierten in die Rolle &quot; **[!UICONTROL Kann-Duplikat]** &quot;. Diese Rollen bieten die gleiche Projekterfahrung wie zuvor. Außerdem wurden alle Gruppen (einschließlich &quot;Alle&quot;) in die Rolle &quot; **[!UICONTROL Kann-Duplikat]** &quot;migriert.

### Keine Rolle zugewiesen

Wenn einem Empfänger keine Rolle zugewiesen wurde und er einen Link zum Projekt erhält (**[!UICONTROL Freigeben]> Projektverknüpfung[!UICONTROL abrufen]**), wird er standardmäßig in der Rolle &quot; **[!UICONTROL Kann Ansicht]** &quot;platziert.

### Mehrere Rollen zugewiesen

Wenn ein Empfänger in mehreren Rollen platziert wird, erhalten sie immer das höchste Erlebnis. Dies kann vorkommen, wenn ein Benutzer sowohl als Einzelperson als auch als Teil einer Gruppe hinzugefügt wird. Wenn einem Benutzer beispielsweise die Rolle &quot; **[!UICONTROL Kann bearbeiten]** &quot;als Einzelperson und die Rolle &quot; **[!UICONTROL Kann-Ansicht]** &quot;als Gruppenmitglied zugewiesen wird, erhält er eine **[!UICONTROL Kann-Bearbeitung]** .

### Administratoren und Rollen

Administratoren, die in die Rolle &quot; **[!UICONTROL Können-Duplikat]** &quot;oder &quot; **[!UICONTROL Können-Ansicht]** &quot;aufgenommen werden, erhalten diese eingeschränkten Erlebnisse, wenn sie ein Projekt öffnen. Falls gewünscht, kann ein Administrator seine Rolle auf **[!UICONTROL Kann jederzeit bearbeiten]** über **[!UICONTROL Komponenten]>[!UICONTROL Projekte]** erhöhen.

## Empfänger für freigegebene Projekte Hinzufügen {#Add}

So fügen Sie Ihrem freigegebenen Projekt Empfänger hinzu:

1. Klicken Sie auf **[!UICONTROL Freigeben]** > Projekt **[!UICONTROL freigeben]**.
Wenn noch nicht gespeicherte Änderungen vorhanden sind, werden Sie aufgefordert, das Projekt zuerst zu speichern.
1. Hinzufügen Empfänger oder Benutzergruppen.
Referenzieren Sie das Hilfesymbol oben für Beschreibungen der einzelnen Rollen.
1. (Optional) Geben Sie eingebettete Projektkomponenten (Segmente, berechnete Metriken und Datumsbereiche) für alle Empfänger frei.
Nach der Freigabe werden diese Komponenten in der Dropdown-Liste &quot;Komponenten&quot;des Arbeitsbereichs des Empfängers angezeigt. Beachten Sie, dass diese Einstellung nicht beibehalten wird. Es handelt sich um eine einzelne Aktion zum Zeitpunkt der Freigabe.
1. (Optional) Legen Sie diese Seite als Landingpage für Empfänger fest.
Diese Einstellung wird nicht beibehalten. Es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.
1. Klicken Sie auf Freigabe.
Sie können auch auf **[!UICONTROL Kuratieren und Freigeben]** klicken, um die Projektkuratierung automatisch anzuwenden. Wenn ein Projekt bereits freigegeben wurde, werden für diese Schaltflächen &quot; **[!UICONTROL Aktualisieren]** &quot;und &quot; **[!UICONTROL Kuratieren und Aktualisieren]**&quot;angezeigt. Weitere Informationen zur [Projektkuratierung](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/curate-share/curate.html).

![](assets/share-proj-modal.png)

## Für Empfänger freigeben {#Groups}

Alle Benutzer können Projekte für Gruppen freigeben, bei denen es sich um eine Sammlung von Empfängern handelt. In Adobe Analytics werden Gruppen durch Produkt-Profil in der [Adobe Experience Cloud-Admin-Konsole](https://docs.adobe.com/content/help/de-DE/core-services/interface/manage-users-and-products/admin-getting-started.html)definiert.

* Administratoren können für jede Gruppe freigeben, einschließlich &quot;Alle&quot;.
* Nichtadministratoren können Gruppen, denen sie angehören, mit Ausnahme von &quot;Alle&quot;freigeben.

## Freigeben von Projekten im Projektmanager {#Manager}

Projekte können auch über **[!UICONTROL Komponenten]>[!UICONTROL Projekte]** freigegeben werden. Ein einzelnes Projekt kann wie oben beschrieben freigegeben werden.

Wenn mehrere Projekte ausgewählt wurden, die freigegeben werden sollen, werden der bestehenden Liste der Empfänger für jedes Projekt Empfänger hinzugefügt. Beispiel:

* Projekt A wird für die Benutzer 1, 2, 3 freigegeben
* Projekt B wird für Benutzer 4, 5 und 6 freigegeben
* Bei Auswahl von Projekt A und B werden die Benutzer 4 und 7 zu den Listen des Empfängers hinzugefügt. Die Liste der neuen Empfänger für jedes Projekt lautet nun:
   * Projekt A: 1, 2, 3, 4, 7
   * Projekt B: 4, 5, 6, 7

   ![](assets/mult-proj-sharing.png)

## Häufig gestellte Fragen (FAQ){#FAQs}

| Frage | Antwort |
|---|---|
| Was passiert, wenn zwei Editoren gleichzeitig ein Projekt speichern? | Die Änderungen werden nicht zusammengeführt und die zuletzt gespeicherte Projektversion bleibt erhalten. Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. |
| Welche Projekterfahrung sehe ich als Administrator? | Administratoren, die in die Rolle &quot; **[!UICONTROL Können-Duplikat]** &quot;oder &quot; **[!UICONTROL Können-Ansicht]** &quot;aufgenommen werden, erhalten diese eingeschränkten Erlebnisse, wenn sie ein Projekt öffnen. Falls gewünscht, kann ein Administrator seine Rolle auf **[!UICONTROL Kann jederzeit bearbeiten]** über **[!UICONTROL Komponenten]>[!UICONTROL Projekte]** erhöhen. |
| Was passiert, wenn ein Benutzer in einer Rolle als Einzelperson und in einer anderen Rolle als Mitglied einer Gruppe platziert wird? | Wenn ein Empfänger in mehreren Rollen platziert wird, erhält er immer das höhere Erlebnis. Wenn einem Benutzer beispielsweise die Rolle &quot; **[!UICONTROL Kann bearbeiten]** &quot;als Einzelperson und die Rolle &quot; **[!UICONTROL Kann-Ansicht]** &quot;als Gruppenmitglied zugewiesen wird, erhält er eine **[!UICONTROL Kann-Bearbeitung]** . |
| Warum erhält ein Benutzer eine Ansicht, wenn er einen Projektlink erhält? | Wenn einem Empfänger keine Rolle zugewiesen wurde und er einen Link zum Projekt erhält (**[!UICONTROL Freigeben]> Projektverknüpfung[!UICONTROL abrufen]**), wird er standardmäßig in der Rolle &quot; **[!UICONTROL Kann Ansicht]** &quot;platziert. Wenn der Benutzer eine größere Rolle im Projekt haben möchte, kann der Projekteigentümer oder -editor sie dem Kann-Duplikat hinzufügen oder können die Rolle über das Projektfreigabemodal bearbeiten. |
