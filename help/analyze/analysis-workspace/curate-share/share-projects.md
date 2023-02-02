---
description: Projektfreigabe und Projektrollen in Workspace
keywords: Analysis Workspace-Freigabe
title: Freigeben von Projekten
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 58abc4a8410441a3c76c6737ace8e2c5ab5c1374
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 49%

---

# Freigeben von Projekten

Sie können ein Projekt für bestehende Adobe Analytics-Benutzer oder -Gruppen in Ihrem Unternehmen freigeben. Wenn Sie ein Projekt wie in diesem Abschnitt beschrieben freigeben, müssen die Benutzer, für die Sie freigeben, bereits über ein Adobe Analytics-Konto verfügen.

Sie können eine bestimmte Rolle für Benutzer oder Gruppen freigeben oder einen Link freigeben.

* [Freigeben einer bestimmten Projektrolle](#share-a-specific-project-role)

* [Link zu einem Projekt freigeben](#share-a-link-to-a-project)

## Freigeben einer bestimmten Projektrolle

Beachten Sie beim Freigeben einer bestimmten Projektrolle für Benutzer und Gruppen in Ihrer Organisation Folgendes:

* Projektrollen (**[!UICONTROL Kann bearbeiten]**, **[!UICONTROL Kann duplizieren]** und **[!UICONTROL Kann anzeigen]**) sind an den Benutzer und die spezifische Projekt-ID gebunden. Projektrollen sind unabhängig von Benutzerberechtigungen, die in der [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) verwaltet werden.

* In Adobe Analytics werden Gruppen durch Produktprofile in der [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) definiert. Administratoren können für jede Gruppe freigeben, einschließlich &quot;Alle&quot;. Nicht-Administratoren können für alle Gruppen freigeben, denen sie angehören, mit Ausnahme von &quot;Alle&quot;.

* Benutzer, die mehreren Rollen zugewiesen sind, erhalten immer das höchste Erlebnis. Dies kann vorkommen, wenn ein Benutzer sowohl als Einzelperson als auch als Teil einer Gruppe hinzugefügt wird. Wenn einem Benutzer beispielsweise die Variable **[!UICONTROL Kann bearbeiten]** Rolle als Einzelperson und **[!UICONTROL Kann anzeigen]** Als Mitglied einer Gruppe erhalten sie eine **[!UICONTROL Kann bearbeiten]** Projekterlebnis.

* Administratoren, die im **[!UICONTROL Kann duplizieren]** oder **[!UICONTROL Kann anzeigen]** Rolle erhält diese eingeschränkten Erlebnisse beim Öffnen eines Projekts. Falls gewünscht, kann ein Administrator seine Rolle jederzeit auf **[!UICONTROL Kann bearbeiten]** erhöhen, indem er **[!UICONTROL Komponenten] > [!UICONTROL Projekte]** wählt.

So geben Sie eine bestimmte Projektrolle für Benutzer oder Gruppen in Ihrer Organisation frei:

1. Wechseln Sie zu dem Projekt, das Sie freigeben möchten, und klicken Sie dann auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projekt freigeben]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Wenn nicht gespeicherte Änderungen vorhanden sind, werden Sie aufgefordert, Ihr Projekt zuerst zu speichern.

   ![](assets/share-proj-modal.png)

   Informationen dazu, wie Sie mehrere Projekte gleichzeitig freigeben, finden Sie unter [Freigeben von Projekten im Projekt-Manager](#share-projects-in-the-project-manager).

1. Fügen Sie Empfänger oder Empfängergruppen in eines der angegebenen Rollenfelder hinzu:

   **Kann bearbeiten:** Empfänger können **[!UICONTROL Speichern]** Änderungen an einem Projekt vornehmen und als Miteigentümer fungieren. Diese Rolle ist nützlich, wenn Sie ein Projekt mit anderen Kollegen gemeinsam verwalten möchten. Dazu gehören das Bearbeiten, Löschen und Bearbeiten von Empfängerlisten für ein freigegebenes Projekt. <br>Hinweis: Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. Es wird daher empfohlen, dass zu jedem Zeitpunkt nur ein Benutzer ein Projekt bearbeitet. Wenn Projekte zum gleichen Zeitpunkt gespeichert werden, wird die letzte Version beibehalten.

   **Kann duplizieren:** Empfänger können **[!UICONTROL Speichern unter]** und haben Zugriff auf die linke Leiste. Projektinteraktionen sind in dieser Rolle nicht beschränkt. Diese Rolle ist nützlich, wenn Sie ein Projekt für Benutzer freigeben möchten, die die Daten Ihres Unternehmens und die Verwendung von Analysis Workspace verstehen, Ihr Projekt jedoch nicht ändern möchten.

   **Kann anzeigen:** Empfänger können **[!UICONTROL Speichern]** oder **[!UICONTROL Speichern unter]** und keinen Zugriff auf die linke Leiste haben. Auch die Projektinteraktionen sind begrenzt. Diese Rolle ist nützlich, wenn Sie ein Projekt für Benutzer freigeben möchten, die mit der Datenstruktur Ihres Unternehmens, Analysis Workspace oder Adobe Analytics im Allgemeinen weniger vertraut sind. Sie möchten jedoch, dass sie Daten und Erkenntnisse in einer sicheren Umgebung einsehen können. Weitere Informationen zum [Projekterlebnis „Kann anzeigen“](/help/analyze/analysis-workspace/curate-share/view-only-projects.md).

1. Wählen Sie aus, ob beim Freigeben des Projekts die folgenden Optionen aktiviert werden sollen:

   * **Freigeben eingebetteter Projektkomponenten:** Teilt Segmente, berechnete Metriken und Datumsbereiche für alle Empfänger. Nach der Freigabe werden diese Komponenten im Dropdown-Menü „Komponenten“ im Workspace des Empfängers angezeigt. Diese Einstellung bleibt nicht bestehen - es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.

   * **Als Landingpage für Empfänger festlegen:** Legt diese Seite als Landingpage für Empfänger fest. Diese Einstellung bleibt nicht bestehen - es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.

1. Klicken Sie auf **[!UICONTROL Freigabe]**.
Sie können auch auf **[!UICONTROL Kuratieren und freigeben]** klicken, um die Projektkuratierung automatisch anzuwenden. Wenn ein Projekt bereits freigegeben wurde, werden für diese Schaltflächen **[!UICONTROL Aktualisieren]** und **[!UICONTROL Kuratieren und aktualisieren]** angezeigt. Weitere Informationen zur [Projektkuratierung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=de).

## Link zu einem Projekt freigeben

Beachten Sie bei der Freigabe eines Links wie in diesem Abschnitt beschrieben Folgendes:

* Empfänger, die den Link verwenden, müssen sich bei Adobe Analytics anmelden, bevor sie Zugriff auf das Projekt erhalten.

* Wenn einem Empfänger keine Rolle zugewiesen wurde und er eine [link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=de) an das Projekt (**[!UICONTROL Freigeben] > [!UICONTROL Projekt-Link abrufen]**), erhalten sie standardmäßig eine Rolle. Administratoren erhalten die Rolle **[!UICONTROL Kann bearbeiten]** und Nicht-Administratoren erhalten **[!UICONTROL Kann duplizieren]**.

So geben Sie die Projektverknüpfung für Benutzer in Ihrer Organisation frei:

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projekt freigeben]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Wenn nicht gespeicherte Änderungen vorhanden sind, werden Sie aufgefordert, Ihr Projekt zuerst zu speichern.

   ![](assets/share-proj-modal.png)

1. Klicken **[!UICONTROL Link kopieren]** neben dem **[!UICONTROL URL-Feld freigeben]**.

1. Geben Sie den Link für Benutzer in Ihrer Organisation frei. Sie können sie beispielsweise in eine E-Mail, eine interne Website usw. einfügen.

## Freigeben von Projekten im Projekt-Manager {#Manager}

Projekte können auch über **[!UICONTROL Komponenten] > [!UICONTROL Projekte]** freigegeben werden. Ein einzelnes Projekt kann wie oben beschrieben freigegeben werden.  Wenn mehrere Projekte zum Freigeben ausgewählt wurden, werden die Empfänger für jedes Projekt der bestehenden Empfängerliste hinzugefügt.

Beispiel:

* Projekt A wird für die Empfänger 1, 2 und 3 freigegeben
* Projekt B wird für die Empfänger 4, 5 und 6 freigegeben

Während Projekt A und B ausgewählt sind, werden die Empfänger 4 und 7 den Freigabelisten hinzugefügt. Die neue Freigabeliste für jedes Projekt lautet nun:

* Projekt A: 1, 2, 3, 4, 7
* Projekt B: 4, 5, 6, 7

![](assets/mult-proj-sharing.png)

## Freigeben von eingebetteten Komponenten

Im Folgenden finden Sie ein Video zum Thema:

>[!VIDEO](https://video.tv.adobe.com/v/24713/?quality=12)

## Häufig gestellte Fragen (FAQ) {#FAQs}

| Frage | Antwort |
| --- | --- |
| Was passiert, wenn zwei Bearbeiter ein Projekt gleichzeitig speichern? | Die Änderungen werden nicht zusammengeführt und die zuletzt gespeicherte Projektversion bleibt erhalten. Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. |
| Welches Projekterlebnis sehe ich als Administrator? | Administratoren, die in die Rolle **[!UICONTROL Kann duplizieren]** oder **[!UICONTROL Kann anzeigen]** aufgenommen werden, erhalten diese eingeschränkten Erlebnisse, wenn sie ein Projekt öffnen. Falls gewünscht, kann ein Administrator seine Rolle jederzeit auf **[!UICONTROL Kann bearbeiten]** erhöhen, indem er **[!UICONTROL Komponenten] > [!UICONTROL Projekte]** wählt. |
| Was passiert, wenn ein Empfänger als Einzelperson einer Rolle und als Gruppenmitglied einer weiteren Rolle zugewiesen wird? | Wenn einem Empfänger mehrere Rollen zugewiesen werden, erhält er immer das höhere Erlebnis. Wenn einem Empfänger beispielsweise die Rolle **[!UICONTROL Kann bearbeiten]** als Einzelperson und die Rolle **[!UICONTROL Kann anzeigen]** als Gruppenmitglied zugewiesen wird, erhält er das Projekterlebnis **[!UICONTROL Kann bearbeiten]**. |
| Welches Erlebnis erhält ein Empfänger, wenn er einen Projekt-Link öffnet? | Empfänger erhalten die Rolle, die Sie ihnen im Freigabe-Modal zugewiesen haben. Wenn einem Empfänger keine Rolle zugewiesen wurde und er einen Link zum Projekt erhält (**[!UICONTROL Freigeben] > [!UICONTROL Projekt-Link abrufen]**), wird er standardmäßig in eine Rolle eingefügt. Administratoren erhalten die Rolle **[!UICONTROL Kann bearbeiten]** und Nicht-Administratoren erhalten **[!UICONTROL Kann duplizieren]**. |
