---
description: Projektfreigabe und Projektrollen in Workspace
keywords: Analysis Workspace-Freigabe
title: Freigeben von Projekten
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 4b11a7057177bec9d2e9d7c435ad0d5476a46602
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 35%

---

# Freigeben von Projekten

Sie können ein Analysis Workspace-Projekt für die folgenden Personentypen freigeben:

* Benutzer und Gruppen in Ihrem Unternehmen, die Zugriff auf Adobe Analytics haben

* Benutzer und Gruppen in Ihrem Unternehmen, die keinen Zugriff auf Adobe Analytics haben

* Personen außerhalb Ihrer Organisation

Alle [Kuratierung](curate.md) Sie vor der Freigabe beantragen, wird beim Öffnen des Projekts durch die Empfänger angezeigt.

Im Folgenden finden Sie eine Videoübersicht zur gemeinsamen Nutzung von Projekten:

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## Freigeben für Adobe Analytics-Benutzer und -Gruppen in Ihrer Organisation {#Add}

Sie können ein Projekt für bestehende Adobe Analytics-Benutzer oder -Gruppen in Ihrem Unternehmen freigeben. Wenn Sie ein Projekt wie in diesem Abschnitt beschrieben freigeben, müssen die Benutzer, für die Sie freigeben, bereits über ein Adobe Analytics-Konto verfügen.

Sie können eine bestimmte Rolle für Benutzer oder Gruppen freigeben oder einen Link freigeben.

* [Freigeben einer bestimmten Projektrolle](#share-a-specific-project-role)

* [Link zu einem Projekt freigeben](#share-a-link-to-a-project)

### Freigeben einer bestimmten Projektrolle

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

### Link zu einem Projekt freigeben

Beachten Sie bei der Freigabe eines Links wie in diesem Abschnitt beschrieben Folgendes:

* Empfänger, die den Link verwenden, müssen sich bei Adobe Analytics anmelden, bevor sie Zugriff auf das Projekt erhalten.

* Wenn einem Empfänger keine Rolle zugewiesen wurde und er eine [link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=de) an das Projekt (**[!UICONTROL Freigeben] > [!UICONTROL Projekt-Link abrufen]**), erhalten sie standardmäßig eine Rolle. Administratoren erhalten die Rolle **[!UICONTROL Kann bearbeiten]** und Nicht-Administratoren erhalten **[!UICONTROL Kann duplizieren]**.

So geben Sie die Projektverknüpfung für Benutzer in Ihrer Organisation frei:

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projekt freigeben]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Wenn nicht gespeicherte Änderungen vorhanden sind, werden Sie aufgefordert, Ihr Projekt zuerst zu speichern.

   ![](assets/share-proj-modal.png)

1. Klicken **[!UICONTROL Link kopieren]** neben dem **[!UICONTROL URL-Feld freigeben]**.

1. Geben Sie den Link für Benutzer in Ihrer Organisation frei. Sie können sie beispielsweise in eine E-Mail, eine interne Website usw. einfügen.

## Öffentlichen Link für alle freigeben (keine Anmeldung erforderlich) {#share-public-link}

{{release-limited-testing-section}}

Sie können Analysis Workspace-Projekte für Personen freigeben, die keinen Zugriff auf Adobe Analytics haben. Dies kann Folgendes umfassen:

* Personen außerhalb Ihrer Organisation

* Personen in Ihrem Unternehmen, die nicht für Adobe Analytics bereitgestellt werden

>[!NOTE]
>
>Diese Option kann vom Analytics-Administrator deaktiviert werden, wie unter [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md). Wenn Sie einen öffentlichen Link nicht wie in diesem Abschnitt beschrieben freigeben können, hat Ihr Analytics-Administrator diese Möglichkeit deaktiviert.

So geben Sie einen öffentlichen Link zu einem Analysis Workspace-Projekt frei:

1. Öffnen Sie das Analysis Workspace-Projekt, das Sie freigeben möchten.

1. Klicken **[!UICONTROL Freigeben]** > **[!UICONTROL Öffentlichen Link freigeben]**.

   Wenn nicht gespeicherte Änderungen vorhanden sind, werden Sie aufgefordert, Ihr Projekt zu speichern.

   <!-- Add screen shot of new modal -->

1. Aktivieren Sie die **[!UICONTROL Link-aktiv]** -Option, wenn sie noch nicht aktiviert ist.

1. Wählen Sie aus, ob die folgenden Sicherheitsoptionen aktiviert werden sollen (diese Optionen können von Ihrem Analytics-Administrator gesteuert werden):

   * **[!UICONTROL Authentifizierung mit Single Sign-on (SSO) erfordern]:**

      Personen mit dem Link müssen sich über SSO authentifizieren, bevor sie Zugriff auf das freigegebene Projekt erhalten. Wählen Sie diese Option aus, wenn das Projekt nur für Benutzer in Ihrer Organisation zugänglich sein soll.

      Analytics-Administratoren können diese Voreinstellung für das Unternehmen festlegen, wie unter [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md). Je nachdem, wie der Administrator diese Option konfiguriert hat, können die folgenden Szenarien auftreten:

      * Wenn diese Option nicht angezeigt wird, ist die einmalige Anmeldung für Ihr Unternehmen nicht aktiviert oder Ihr Analytics-Administrator hat diese Funktion nicht aktiviert.

      * Wenn diese Option aktiviert und abgeblendet ist, benötigt Ihr Analytics-Administrator eine SSO-Authentifizierung, um auf alle öffentlichen Links zugreifen zu können.
   * **[!UICONTROL Kennwort erforderlich]:** Personen mit dem Link müssen ein Kennwort angeben, bevor sie auf das Analysis Workspace-Projekt zugreifen können. Dies bietet ein zusätzliches Sicherheitsniveau für Ihr Projekt.

      Wenn Sie diese Option auswählen, geben Sie ein Kennwort an. Denken Sie daran, dieses Kennwort zusammen mit dem Projekt-Link zu teilen, wenn Sie es für andere freigeben. <!--go through this workflow and see how it works.-->

      Wenn diese Option aktiviert und abgeblendet ist, erfordert Ihr Analytics-Administrator, dass alle öffentlichen Links kennwortgeschützt sind. Analytics-Administratoren können diese Voreinstellung für das Unternehmen festlegen, wie unter [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md).


1. Neben dem **[!UICONTROL Mit anderen teilen (keine Anmeldung erforderlich)]** und klicken Sie auf das **Link kopieren** -Symbol, um den Link in die Zwischenablage Ihres Systems zu kopieren.

1. Geben Sie den Link für die Personen frei, die Zugriff auf das Projekt haben möchten. Sie können beispielsweise den Link in eine E-Mail einfügen.

   Alle Personen, für die Sie den Link freigeben, können das Analysis Workspace-Projekt anzeigen. Wenn Sie sich dafür entschieden haben, ein Passwort zu benötigen, müssen Sie das Passwort auch für alle freigeben, die auf den Link zugreifen möchten.

1. Auswählen **[!UICONTROL Schließen]** , um das Dialogfeld &quot;Freigeben&quot;zu schließen. Ihre Änderungen werden automatisch gespeichert. <!-- True? -->


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
