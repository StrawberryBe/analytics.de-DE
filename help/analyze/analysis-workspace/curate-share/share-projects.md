---
description: Projektfreigabe und Projektrollen in Workspace
keywords: Analysis Workspace-Freigabe
title: Freigeben von Projekten
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 5a670a6ef16a6dcfae12c9eb9801c51f4f1ea54c
workflow-type: tm+mt
source-wordcount: '1929'
ht-degree: 83%

---

# Freigeben von Projekten

Sie können ein Analysis Workspace-Projekt für die folgenden Personentypen freigeben:

* Personen und Gruppen in Ihrer Organisation, die Zugriff auf Adobe Analytics haben

  Sie können den Zugriff zum Bearbeiten, Duplizieren oder Anzeigen freigeben

* Personen und Gruppen in Ihrer Organisation, die keinen Zugriff auf Adobe Analytics haben

  Empfängerinnen und Empfänger haben schreibgeschützten Zugriff

* Personen außerhalb Ihrer Organisation

  Empfängerinnen und Empfänger haben schreibgeschützten Zugriff

Jede [Kuration](curate.md), die Sie vor der Freigabe vorgenommen haben, wird beim Öffnen des Projekts durch die Empfängerinnen bzw. Empfänger angezeigt.

Im Folgenden finden Sie eine Videoübersicht zur gemeinsamen Nutzung von Projekten:

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## Freigeben für Analysis Workspace-Benutzende und -Gruppen in Ihrer Organisation {#Add}

Sie können ein Projekt für bestehende Analysis Workspace-Benutzende oder -Gruppen in Ihrer Organisation freigeben. Wenn Sie ein Projekt wie in diesem Abschnitt beschrieben freigeben, müssen die Benutzenden, für die Sie es freigeben, bereits über Zugriff auf Adobe Analytics verfügen.

Sie können eine bestimmte Rolle für Benutzende oder Gruppen freigeben oder einen Link freigeben.

* [Freigeben einer bestimmten Projektrolle](#share-a-specific-project-role)

* [Freigeben eines Links zu einem Projekt](#share-a-link-to-a-project)

## Freigeben einer bestimmten Projektrolle

Beachten Sie beim Freigeben einer bestimmten Projektrolle für Benutzende und Gruppen in Ihrer Organisation Folgendes:

* Projektrollen (**[!UICONTROL Original bearbeiten]**, **[!UICONTROL Kopie bearbeiten]** und **[!UICONTROL Schreibgeschützt]**) sind an die Benutzenden und die spezifische Projekt-ID gebunden. Projektrollen sind unabhängig von Benutzerberechtigungen, die in der [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) verwaltet werden.

* In Adobe Analytics werden Gruppen durch Produktprofile in der [Adobe Experience Cloud Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=de) definiert. Die von Administrierenden durchgeführte Freigabe ist für jede Gruppe möglich, einschließlich „Alle“. Nichtadministrierende können Freigaben für Gruppen durchführen, denen sie angehören (mit Ausnahme von „Alle“).

* Benutzende, denen mehrere Rollen zugewiesen sind, erhalten immer die maximale Berechtigung. Dies kann vorkommen, wenn Benutzende sowohl als Einzelpersonen als auch als Gruppenmitglieder hinzugefügt werden. Wenn Benutzenden beispielsweise die Rolle **[!UICONTROL Original bearbeiten]** als Einzelpersonen und die Rolle **[!UICONTROL Schreibgeschützt]** als Gruppenmitgliedern zugewiesen wird, erhalten sie die Projektberechtigung **[!UICONTROL Original bearbeiten]**.

* Admins, die die Rolle **[!UICONTROL Kopie bearbeiten]** oder **[!UICONTROL Schreibgeschützt]** erhalten, verfügen über diese eingeschränkten Berechtigungen, wenn sie ein Projekt öffnen. Ein Administrator kann seine Rolle in **[!UICONTROL Original bearbeiten]** durch Eigenbeteiligung des Projekts und Gewährung der **Bearbeiten** Rolle, wie im folgenden Verfahren beschrieben.

* Wenn mehrere Projekte zum Freigeben ausgewählt wurden, werden die Empfänger für jedes Projekt der bestehenden Empfängerliste hinzugefügt.

  Beispielsweise ist Projekt A bereits für die Empfänger 1, 2 und 3 freigegeben, während Projekt B bereits für die Empfänger 4, 5 und 6 freigegeben wurde.

  Die Projekte A und B werden dann für die Empfänger 4 und 7 freigegeben. Die neue Freigabeliste für Projekt A ist jetzt 1, 2, 3, 4 und 7, während die neue Freigabeliste für Projekt B 4, 5, 6 und 7 lautet.

So geben Sie eine bestimmte Projektrolle für Benutzende oder Gruppen in Ihrer Organisation frei:

1. Wählen Sie in Adobe Analytics die [!UICONTROL **Arbeitsbereich**] Registerkarte und wählen Sie [!UICONTROL **Projekte**] in der linken Leiste.

1. Aktivieren Sie das Kontrollkästchen neben einem oder mehreren freizugebenden Projekten und wählen Sie [!UICONTROL **Freigeben**].

   Oder

   Um nur ein einzelnes Projekt freizugeben, können Sie das Projekt öffnen, das Sie freigeben möchten, und dann **[!UICONTROL Freigeben]** > **[!UICONTROL Freigeben für Workspace-Benutzer]**.
Wenn es nicht gespeicherte Änderungen gibt, werden Sie aufgefordert, das Projekt zuerst zu speichern.

   Das Dialogfeld Projekt freigeben wird angezeigt. Die [!UICONTROL **Über Link freigeben**] und [!UICONTROL **Einstellungen**] -Abschnitte des Dialogfelds sind nur sichtbar, wenn ein einzelnes Projekt freigegeben wird.

   ![](assets/share-proj-modal.png)

1. Fügen Sie Empfänger und Empfängerinnen oder Empfängergruppen in eines der angegebenen Rollenfelder hinzu:

   **Original bearbeiten**: Empfängerinnen und Empfänger können Änderungen an einem Projekt **[!UICONTROL speichern]** und als Co-Inhaberinnen bzw. Co-Inhaber auftreten. Diese Rolle ist nützlich, wenn Sie ein Projekt mit anderen Kollegen gemeinsam verwalten möchten. Dazu gehören das Bearbeiten, Löschen und Bearbeiten von Empfängerlisten für ein freigegebenes Projekt. <br>Hinweis: Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. Es wird daher empfohlen, dass zu jedem Zeitpunkt nur ein Benutzer ein Projekt bearbeitet. Wenn Projekte zum gleichen Zeitpunkt gespeichert werden, wird die letzte Version beibehalten.

   **Kopie bearbeiten:** Empfängerinnen und Empfänger können die Option **[!UICONTROL Speichern unter]** verwenden und auf die linke Leiste zugreifen. Projektinteraktionen sind in dieser Rolle nicht beschränkt. Diese Rolle ist nützlich, wenn Sie ein Projekt für Benutzende freigeben möchten, die mit der Datennutzung in Ihrem Unternehmen und der Verwendung von Analysis Workspace vertraut sind, Ihr Projekt jedoch nicht geändert werden soll.

   **Schreibgeschützt:** Empfängerinnen und Empfänger können nicht **[!UICONTROL speichern]** oder die Option **[!UICONTROL Speichern unter]** verwenden und haben keinen Zugriff auf die linke Leiste. Auch die Projektinteraktionen sind begrenzt. Diese Rolle ist hilfreich, wenn Sie ein Projekt für Benutzende freigeben möchten, die mit der Datenstruktur Ihres Unternehmens, Analysis Workspace oder Adobe Analytics im Allgemeinen nicht so vertraut sind. Sie möchten jedoch, dass sie Daten und Erkenntnisse in einer sicheren Umgebung einsehen können. Erhalten Sie weitere Informationen zum [Erlebnis eines schreibgeschützten Projekts](/help/analyze/analysis-workspace/curate-share/view-only-projects.md).

1. (Bedingt) Wenn Sie ein einzelnes Projekt freigeben, wählen Sie aus, ob beim Freigeben des Projekts die folgenden Optionen aktiviert werden sollen:

   * **Freigeben von eingebetteten Projektkomponenten**: Freigabe von Segmenten, berechneten Metriken und Datumsbereichen für alle Empfänger und Empfängerinnen. Nach der Freigabe werden diese Komponenten im Dropdown-Menü „Komponenten“ im Arbeitsbereich des Empfängers bzw. der Empfängerin angezeigt. Diese Einstellung wird nicht beibehalten. Es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.

   * **Als Landingpage für Empfänger und Empfängerinnen festlegen:** Legt diese Seite als Landingpage für Empfänger und Empfängerinnen fest. Diese Einstellung wird nicht beibehalten. Es handelt sich um eine einmalige Aktion zum Zeitpunkt der Freigabe.

1. Auswählen **[!UICONTROL Freigeben]**. (Wenn das Projekt bereits freigegeben wurde, wählen Sie [!UICONTROL **Aktualisieren**].

   Oder

   Auswählen **[!UICONTROL Kuratieren und freigeben]** , um die Projektkuratierung automatisch anzuwenden. (Wenn das Projekt bereits freigegeben wurde, wählen Sie **[!UICONTROL Kuratieren und aktualisieren]**. Erhalten Sie weitere Informationen zur [Projektkuratierung](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=de).

## Freigeben eines Links zu einem Projekt

Beachten Sie bei der Freigabe eines Links, wie in diesem Abschnitt beschrieben, Folgendes:

* Empfänger und Empfängerinnen, die den Link verwenden, müssen sich bei Adobe Analytics anmelden, bevor sie Zugriff auf das Projekt erhalten.

* Wenn Empfängerinnen oder Empfängern keine Rolle zugewiesen wurde und sie einen [Link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html?lang=de) zum Projekt erhalten, wird ihnen standardmäßig eine Rolle zugewiesen. Admins erhalten **[!UICONTROL Original bearbeiten]** und Nicht-Admins erhalten **[!UICONTROL Kopie bearbeiten]**.

So geben Sie den Projekt-Link für Personen in Ihrer Organisation frei:

1. Speichern Sie das Projekt. Wenn es nicht gespeicherte Änderungen gibt, werden Sie aufgefordert, Ihr Projekt zu speichern, bevor Sie einen Link teilen.

1. Wählen Sie **[!UICONTROL Freigeben]** > **[!UICONTROL Freigeben für Workspace-Benutzende]** und anschließend **[!UICONTROL Kopieren]** neben dem Feld **[!UICONTROL Über Link freigeben]**.

   ![](assets/share-proj-modal.png)

1. Geben Sie den Link für Personen in Ihrer Organisation frei. Sie können ihn beispielsweise in eine E-Mail oder eine interne Website usw. einfügen.

## Freigeben eines Projekts für alle (keine Anmeldung erforderlich) {#share-public-link}

Sie können jetzt den [schreibgeschützten Zugriff](/help/analyze/analysis-workspace/curate-share/view-only-projects.md) auf Analysis Workspace-Projekte für Personen freischalten, die keinen Zugriff auf Adobe Analytics haben. Dazu können gehören:

* Personen außerhalb Ihrer Organisation

* Personen in Ihrem Unternehmen, die keinen Zugriff auf Adobe Analytics haben

>[!NOTE]
>
>Beachten Sie Folgendes bei der Freigabe eines Analysis Workspace-Projekts für Personen, die keinen Zugriff auf Adobe Analytics haben:
>
>* Die Fähigkeit, ein Projekt auf diese Weise freizugeben, kann von Analytics-Admins deaktiviert werden, wie in den [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md) erläutert. Wenn Sie ein Projekt nicht wie in diesem Abschnitt beschrieben freigeben können, haben Ihre Analytics-Admins diese Fähigkeit deaktiviert.
>
>* Projekte mit mehr als 50 erweiterten Visualisierungen können nicht für Personen freigegeben werden, die keinen Zugriff auf Adobe Analytics haben.
>
>* Personen, für die Sie das Projekt freigeben, können alle Filter anzeigen, die während der [Kuratierung](curate.md) auf das Projekt angewendet wurden.
> 
>* Personen, für die Sie das Projekt freigeben, können den Projektdatumsbereich ändern. Standardmäßig wird der Datumsbereich angezeigt, den Sie für das Projekt festgelegt haben.
>
>* Wenn viele Personen gleichzeitig versuchen, auf einen bestimmten Link zuzugreifen, ist das Projekt möglicherweise nicht mehr zugänglich. Standardmäßig können alle 5 Minuten mehr als 190 Personen auf einen einzelnen Link zugreifen. Sollte Ihr Unternehmen diese Grenze erreichen, warten Sie 5 Minuten und versuchen Sie dann erneut, den Link zu öffnen.

Die folgende Videodemonstration und die zugehörige Dokumentation beschreiben die Optionen im Zusammenhang mit der Freigabe eines Links für alle:

>[!VIDEO](https://video.tv.adobe.com/v/3420093/?learn=on)

So geben Sie ein Analysis Workspace-Projekt für Personen frei, die keinen Zugriff auf Adobe Analytics haben:

1. Öffnen Sie das Analysis Workspace-Projekt, das Sie freigeben möchten.

1. Klicken Sie auf **[!UICONTROL Freigeben]** > **[!UICONTROL Für alle freigeben]**.

   Wenn es nicht gespeicherte Änderungen gibt, werden Sie aufgefordert, das Projekt zuerst zu speichern.

   <!-- Add screen shot of new modal -->

1. Aktivieren Sie die Option **[!UICONTROL Link ist aktiv]**, falls diese nicht bereits aktiviert ist.

   Beim Auswählen dieser Option wird ein Link zum Projekt erstellt, der für alle freigegeben werden kann. Sie können den Zugriff auf das Projekt jederzeit deaktivieren, indem Sie diese Option deaktivieren.

   Die für das Projekt verantwortliche Person ist auch für diesen Link verantwortlich. Die Link-Verantwortung kann nur dann an andere Benutzende übertragen werden, wenn die Projektverantwortung übertragen wird, wie unter [Übertragen von Benutzer-Assets oder Festlegen des Kontoablaufs](/help/admin/admin/user-management2/users-assets.md) im Analytics-Admin-Handbuch beschrieben.

1. Wählen Sie aus, ob die folgende Sicherheitsoption aktiviert werden soll (diese Option kann von Ihren Analytics-Admins gesteuert werden):

   * **[!UICONTROL Experience Cloud-Authentifizierung verlangen]:**

     Wenn diese Option aktiviert ist, können nur Personen auf das Projekt zugreifen, die sich bei der Adobe Experience Cloud-Organisation anmelden können, in der das freigegebene Projekt erstellt wurde. Für Benutzende, für die Sie es freigeben, ist jedoch kein Zugriff auf Adobe Analytics erforderlich.

     Analytics-Admins können diese Voreinstellung für das Unternehmen konfigurieren, wie unter [Voreinstellungen](/help/analyze/analysis-workspace/user-preferences.md) beschrieben. Je nachdem, wie die Admins diese Option konfiguriert haben, können die folgenden Szenarien auftreten:

      * Wenn diese Option nicht angezeigt wird, haben Ihre Analytics-Admins diese Funktion nicht aktiviert.

      * Wenn diese Option aktiviert und abgeblendet ist, benötigen Ihre Analytics-Admins eine Experience Cloud-Authentifizierung für alle, die auf Analysis Workspace-Projekte zugreifen.

1. Klicken Sie neben dem Feld **[!UICONTROL Für alle freigeben (keine Anmeldung erforderlich)]** auf das Symbol **Link kopieren** ![Symbol „Link kopieren“](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Link_18_N.svg), um den Link in die Zwischenablage Ihres Systems zu kopieren.

1. Teilen Sie den Link mit den Personen, die Zugriff auf das Projekt haben sollen. Sie können beispielsweise den Link in eine E-Mail einfügen.

   Alle Personen, mit denen Sie den Link teilen, können das Analysis Workspace-Projekt ansehen.

1. (Optional) Sie können auf das Symbol **Neuen Link generieren** ![Symbol „Link generieren“](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) klicken, um den Zugriff von Personen zu entfernen, die zuvor einen Link zum Projekt erhalten haben. Es wird ein neuer Link generiert, den Sie für Benutzende freigeben können, die auf das Projekt zugreifen können sollen.

1. Wählen Sie **[!UICONTROL Schließen]** aus, um das Dialogfeld „Freigeben“ zu schließen. Ihre Änderungen werden automatisch gespeichert.

## Freigegebene Projekte anzeigen

Wenn jemand ein Projekt mit Ihnen teilt, indem er [Teilen einer bestimmten Projektrolle](#share-a-specific-project-role), können Sie über die [Registerkarte &quot;Projekte&quot;auf der Analytics-Landingpage](/help/analyze/landing.md#navigate-the-projects-tab).

Wenn ein Benutzer ein Projekt für Sie teilt, indem er einen Link teilt (entweder über die [Registerkarte Projekt freigeben](#share-a-link-to-a-project) oder mithilfe einer [für alle freigeben](#share-a-project-with-anyone-no-login-required) ), müssen Sie den Link verwenden, der für Sie freigegeben wurde, um auf das Projekt zugreifen zu können. Beispielsweise könnte der Link in einer E-Mail, auf einer internen Website usw. freigegeben worden sein.

## Freigeben von eingebetteten Komponenten

Im Folgenden finden Sie ein Video zum Thema:

>[!VIDEO](https://video.tv.adobe.com/v/24713/?quality=12)

## Häufig gestellte Fragen (FAQ) {#FAQs}

| Frage | Antwort |
| --- | --- |
| Was passiert, wenn zwei Bearbeiter ein Projekt gleichzeitig speichern? | Die Änderungen werden nicht zusammengeführt und die zuletzt gespeicherte Projektversion bleibt erhalten. Analysis Workspace unterstützt derzeit keine Live-Zusammenarbeit. |
| Was passiert, wenn ein Empfänger als Einzelperson einer Rolle und als Gruppenmitglied einer weiteren Rolle zugewiesen wird? | Wenn einem Empfänger mehrere Rollen zugewiesen werden, erhält er immer das höhere Erlebnis. Wenn Empfängerinnen oder Empfängern beispielsweise die Rolle **[!UICONTROL Original bearbeiten]** als Einzelpersonen und die Rolle **[!UICONTROL Schreibgeschützt]** als Gruppenmitgliedern zugewiesen wird, erhalten sie die Projektberechtigung **[!UICONTROL Original bearbeiten]**. |
| Welches Erlebnis erhält ein Empfänger, wenn er einen Projekt-Link öffnet? | Empfänger erhalten die Rolle, die Sie ihnen im Freigabe-Modal zugewiesen haben. Wenn Empfängerinnen oder Empfängern keine Rolle zugewiesen wurde und sie einen Link zum Projekt erhalten (**[!UICONTROL Freigeben]** > **[!UICONTROL Für Workspace-Benutzer freigeben]**, dann **[!UICONTROL Kopieren]** neben dem Feld **[!UICONTROL Über Link freigeben]** auswählen), werden sie standardmäßig in eine Rolle aufgenommen. Admins erhalten **[!UICONTROL Original bearbeiten]** und Nicht-Admins erhalten **[!UICONTROL Kopie bearbeiten]**. |
