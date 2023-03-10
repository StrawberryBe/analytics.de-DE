---
description: Projektfreigabe und Projektrollen in Workspace
keywords: Analysis Workspace-Freigabe
title: Freigeben von Projekten
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 66a02a6d0c6cc88752ea39172bd30b026908846b
workflow-type: tm+mt
source-wordcount: '1584'
ht-degree: 70%

---

# Freigeben von Projekten

Sie können ein Analysis Workspace-Projekt für die folgenden Personentypen freigeben:

* Benutzer und Gruppen in Ihrem Unternehmen, die Zugriff auf Adobe Analytics haben

   Sie können den Zugriff &quot;Bearbeiten&quot;, &quot;Duplizieren&quot;oder &quot;Anzeigen&quot;freigeben

* Benutzer und Gruppen in Ihrem Unternehmen, die keinen Zugriff auf Adobe Analytics haben

   Empfänger haben schreibgeschützten Zugriff

* Personen außerhalb Ihrer Organisation

   Empfänger haben schreibgeschützten Zugriff

Alle [Kuratierung](curate.md) Sie vor der Freigabe beantragen, wird beim Öffnen des Projekts durch die Empfänger angezeigt.

Im Folgenden finden Sie eine Videoübersicht zur gemeinsamen Nutzung von Projekten:

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## Freigeben für Adobe Analytics-Benutzer und -Gruppen in Ihrer Organisation {#Add}

Sie können ein Projekt für bestehende Adobe Analytics-Benutzende oder -Gruppen in Ihrer Organisation freigeben. Wenn Sie ein Projekt wie in diesem Abschnitt beschrieben freigeben, müssen die Benutzenden, für die Sie es freigeben, bereits über ein Adobe Analytics-Konto verfügen.

Sie können eine bestimmte Rolle für Benutzende oder Gruppen freigeben oder einen Link freigeben.

* [Freigeben einer bestimmten Projektrolle](#share-a-specific-project-role)

* [Freigeben eines Links zu einem Projekt](#share-a-link-to-a-project)

## Freigeben einer bestimmten Projektrolle

Beachten Sie beim Freigeben einer bestimmten Projektrolle für Benutzende und Gruppen in Ihrer Organisation Folgendes:

* Projektrollen (**[!UICONTROL Kann bearbeiten]**, **[!UICONTROL Kann duplizieren]** und **[!UICONTROL Kann anzeigen]**) sind an die Benutzenden und die spezifische Projekt-ID gebunden. Projektrollen sind unabhängig von Benutzerberechtigungen, die in der [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) verwaltet werden.

* In Adobe Analytics werden Gruppen durch Produktprofile in der [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) definiert. Die von Administrierenden durchgeführte Freigabe ist für jede Gruppe möglich, einschließlich „Alle“. Nichtadministrierende können Freigaben für Gruppen durchführen, denen sie angehören (mit Ausnahme von „Alle“).

* Benutzende, denen mehrere Rollen zugewiesen sind, erhalten immer die maximale Berechtigung. Dies kann vorkommen, wenn Benutzende sowohl als Einzelpersonen als auch als Gruppenmitglieder hinzugefügt werden. Wenn Benutzenden beispielsweise die Rolle **[!UICONTROL Kann bearbeiten]** als Einzelpersonen und die Rolle **[!UICONTROL Kann anzeigen]** als Gruppenmitgliedern zugewiesen wird, erhalten sie die Projektberechtigung **[!UICONTROL Kann bearbeiten]**.

* Administrierende, die die Rolle **[!UICONTROL Kann duplizieren]** oder **[!UICONTROL Kann anzeigen]** erhalten, verfügen über diese eingeschränkte Berechtigungen, wenn sie ein Projekt öffnen. Falls gewünscht, kann ein Administrator bzw. eine Administratorin seine/ihre Rolle jederzeit auf **[!UICONTROL Kann bearbeiten]** erhöhen, indem er/sie **[!UICONTROL Komponenten] > [!UICONTROL Projekte]** wählt.

So geben Sie eine bestimmte Projektrolle für Benutzende oder Gruppen in Ihrer Organisation frei:

1. Wechseln Sie zu dem Projekt, das Sie freigeben möchten, und klicken Sie dann auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projekt freigeben]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Wenn es nicht gespeicherte Änderungen gibt, werden Sie aufgefordert, das Projekt zuerst zu speichern.

   ![](assets/share-proj-modal.png)

   Informationen dazu, wie Sie mehrere Projekte gleichzeitig freigeben, finden Sie unter [Freigeben von Projekten im Projekt-Manager](#share-projects-in-the-project-manager).

1. Fügen Sie Empfänger und Empfängerinnen oder Empfängergruppen in eines der angegebenen Rollenfelder hinzu:

   **Kann bearbeiten**: Empfänger und Empfängerinnen können Änderungen an einem Projekt **[!UICONTROL speichern]** und als Co-Inhaber oder Co-Inhaberinnen auftreten. Diese Rolle ist nützlich, wenn Sie ein Projekt mit anderen Kollegen gemeinsam verwalten möchten. Dazu gehören das Bearbeiten, Löschen und Bearbeiten von Empfängerlisten für ein freigegebenes Projekt. <br>Hinweis: Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. Es wird daher empfohlen, dass zu jedem Zeitpunkt nur ein Benutzer ein Projekt bearbeitet. Wenn Projekte zum gleichen Zeitpunkt gespeichert werden, wird die letzte Version beibehalten.

   **Kann duplizieren:** Empfänger und Empfängerinnen können die Option **[!UICONTROL Speichern unter]** verwenden und auf die linke Leiste zugreifen. Projektinteraktionen sind in dieser Rolle nicht beschränkt. Diese Rolle ist nützlich, wenn Sie ein Projekt für Benutzende freigeben möchten, die mit der Datennutzung in Ihrem Unternehmen und der Verwendung von Analysis Workspace vertraut sind, Ihr Projekt jedoch nicht geändert werden soll.

   **Kann anzeigen:** Empfangende können nicht **[!UICONTROL speichern]** oder die Option **[!UICONTROL Speichern unter]** verwenden und haben keinen Zugriff auf die linke Leiste. Auch die Projektinteraktionen sind begrenzt. Diese Rolle ist hilfreich, wenn Sie ein Projekt für Benutzende freigeben möchten, die mit der Datenstruktur Ihres Unternehmens, Analysis Workspace oder Adobe Analytics im Allgemeinen nicht so vertraut sind. Sie möchten jedoch, dass sie Daten und Erkenntnisse in einer sicheren Umgebung einsehen können. Weitere Informationen zur [Projektrolle „Kann anzeigen“](/help/analyze/analysis-workspace/curate-share/view-only-projects.md).

1. Wählen Sie aus, ob beim Freigeben des Projekts die folgenden Optionen aktiviert werden sollen:

   * **Freigeben von eingebetteten Projektkomponenten**: Freigabe von Segmenten, berechneten Metriken und Datumsbereichen für alle Empfänger und Empfängerinnen. Nach der Freigabe werden diese Komponenten im Dropdown-Menü „Komponenten“ im Arbeitsbereich des Empfängers bzw. der Empfängerin angezeigt. Diese Einstellung wird nicht beibehalten. Es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.

   * **Als Landingpage für Empfänger und Empfängerinnen festlegen:** Legt diese Seite als Landingpage für Empfänger und Empfängerinnen fest. Diese Einstellung wird nicht beibehalten. Es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.

1. Klicken Sie auf **[!UICONTROL Freigabe]**. (Wenn das Projekt bereits freigegeben wurde, klicken Sie auf [!UICONTROL **Aktualisieren**].

   Oder

   Klicken **[!UICONTROL Kuratieren und freigeben]** , um die Projektkuratierung automatisch anzuwenden. (Wenn das Projekt bereits freigegeben wurde, klicken Sie auf **[!UICONTROL Kuratieren und aktualisieren]**. Weitere Informationen zur [Projektkuratierung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=de).

## Freigeben eines Links zu einem Projekt

Beachten Sie bei der Freigabe eines Links, wie in diesem Abschnitt beschrieben, Folgendes:

* Empfänger und Empfängerinnen, die den Link verwenden, müssen sich bei Adobe Analytics anmelden, bevor sie Zugriff auf das Projekt erhalten.

* Wenn Empfängern oder Empfängerinnen keine Rolle zugewiesen wurde und sie einen [Link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=de) zum Projekt erhalten (**[!UICONTROL Freigeben] > [!UICONTROL Projekt-Link abrufen]**), wird ihnen standardmäßig eine Rolle zugewiesen. Administrierende erhalten die Rolle **[!UICONTROL Kann bearbeiten]** und Nicht-Administrierende erhalten die Rolle **[!UICONTROL Kann duplizieren]**.

So geben Sie den Projekt-Link für Benutzende in Ihrer Organisation frei:

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Projekt freigeben]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Wenn es nicht gespeicherte Änderungen gibt, werden Sie aufgefordert, das Projekt zuerst zu speichern.

   ![](assets/share-proj-modal.png)

1. Klicken Sie auf **[!UICONTROL Link kopieren]** neben dem Feld **[!UICONTROL URL teilen]**.

1. Geben Sie den Link für Benutzende in Ihrer Organisation frei. Sie können ihn beispielsweise in eine E-Mail oder eine interne Website usw. einfügen.

## Öffentlichen Link für alle freigeben (keine Anmeldung erforderlich) {#share-public-link}

{{release-limited-testing-section}}

Sie können [Schreibgeschützter Zugriff](/help/analyze/analysis-workspace/curate-share/view-only-projects.md) für Analysis Workspace-Projekte für Personen, die keinen Zugriff auf Adobe Analytics haben. Dies kann Folgendes umfassen:

* Personen außerhalb Ihrer Organisation

* Personen in Ihrem Unternehmen, die nicht für Adobe Analytics bereitgestellt werden

>[!NOTE]
>
>Beachten Sie beim Freigeben eines öffentlichen Links Folgendes:
>
>* Die Möglichkeit, einen öffentlichen Zugriffslink freizugeben, kann vom Analytics-Administrator deaktiviert werden, wie unter [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md). Wenn Sie einen öffentlichen Link nicht wie in diesem Abschnitt beschrieben freigeben können, hat Ihr Analytics-Administrator diese Möglichkeit deaktiviert.
>
>* Projekte mit mehr als 14 erweiterten Visualisierungen können nicht über einen öffentlichen Zugriffslink freigegeben werden.


So geben Sie einen öffentlichen Link zu einem Analysis Workspace-Projekt frei:

1. Öffnen Sie das Analysis Workspace-Projekt, das Sie freigeben möchten.

1. Klicken **[!UICONTROL Freigeben]** > **[!UICONTROL Öffentlichen Link freigeben]**.

   Wenn nicht gespeicherte Änderungen vorhanden sind, werden Sie aufgefordert, Ihr Projekt zu speichern.

   <!-- Add screen shot of new modal -->

1. Aktivieren Sie die **[!UICONTROL Link-aktiv]** -Option, wenn sie noch nicht aktiviert ist.

1. Wählen Sie aus, ob die folgende Sicherheitsoption aktiviert werden soll (diese Option kann von Ihrem Analytics-Administrator gesteuert werden):

   * **[!UICONTROL Experience Cloud-Authentifizierung erforderlich]:**

      Wenn diese Option aktiviert ist, können nur Benutzer, die sich bei der Adobe Experience Cloud-Organisation anmelden können, in der das freigegebene Projekt erstellt wurde, diesen Link verwenden.

      Analytics-Administratoren können diese Voreinstellung für das Unternehmen konfigurieren, wie unter [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md). Je nachdem, wie der Administrator diese Option konfiguriert hat, können die folgenden Szenarien auftreten:

      * Wenn diese Option nicht angezeigt wird, hat Ihr Analytics-Administrator diese Funktion nicht aktiviert.

      * Wenn diese Option aktiviert und abgeblendet ist, benötigt Ihr Analytics-Administrator eine Experience Cloud-Authentifizierung, um auf alle öffentlichen Links zugreifen zu können.

1. Neben dem **[!UICONTROL Mit anderen teilen (keine Anmeldung erforderlich)]** und klicken Sie auf das **Link kopieren** -Symbol, um den Link in die Zwischenablage Ihres Systems zu kopieren.

1. Geben Sie den Link für die Personen frei, die Zugriff auf das Projekt haben möchten. Sie können beispielsweise den Link in eine E-Mail einfügen.

   Alle Personen, für die Sie den Link freigeben, können das Analysis Workspace-Projekt anzeigen. Wenn Sie sich dafür entschieden haben, ein Passwort zu benötigen, müssen Sie das Passwort auch für alle freigeben, die auf den Link zugreifen möchten.

1. Auswählen **[!UICONTROL Schließen]** , um das Dialogfeld &quot;Freigeben&quot;zu schließen. Ihre Änderungen werden automatisch gespeichert. <!-- True? -->

## Freigeben von Projekten im Projekt-Manager {#Manager}

Projekte können auch über **[!UICONTROL Komponenten] > [!UICONTROL Projekte]** freigegeben werden. Ein einzelnes Projekt kann wie oben beschrieben freigegeben werden.  Wenn mehrere Projekte zum Freigeben ausgewählt wurden, werden die Empfänger für jedes Projekt der bestehenden Empfängerliste hinzugefügt.

Zum Beispiel:

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
