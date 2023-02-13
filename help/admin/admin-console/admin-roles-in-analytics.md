---
title: Administratorrollen in Adobe Analytics
description: Hier erfahren Sie mehr über die ersten Schritte mit Adobe Analytics, die unterschiedlichen Typen von Rollen und der Anmeldung bei der Benutzeroberfläche.
feature: Admin Tools
exl-id: 9d10716f-5b66-42dc-b288-af34da203c35
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: ht
source-wordcount: '1128'
ht-degree: 100%

---

# Administratorrollen in Adobe Analytics

In Adobe Analytics gibt es verschiedene Arten von Administrierenden. Adobe Analytics-Administrierende mit vollständigen Rechten haben Zugriff auf alle Komponenten von Adobe Analytics, während andere Administrierende und Benutzende nur speziellere Aufgaben ausführen können.

>[!NOTE]
>
>Bevor Benutzenden in Adobe Analytics Benutzerrollen zugewiesen werden können, muss ein Benutzer bzw. eine Benutzerin als erster Administrator bzw. erste Administratorin in Experience Cloud zugewiesen werden. Der erste Administrator bzw. die erste Administratorin kann dann Benutzenden in der Organisation wie in diesem Artikel beschrieben andere Rollen zuweisen. Weitere Informationen zum ersten Administrator bzw. zur ersten Administratorin finden Sie unter [Adobe Analytics-Handbuch für erste Administratoren](/help/admin/admin-console/first-admin-guide.md).


## Schlüsselrollen in Experience Cloud und Adobe Analytics

Beachten Sie bei der Verwendung von Adobe Analytics die folgenden Schlüsselrollen:

* **Adobe Analytics-Administrierende mit vollständigen Rechten:** Diese Benutzenden haben vollen Zugriff auf alle Funktionen in Adobe Analytics, einschließlich Report Suite-Einstellungen und Benutzerberechtigungen. Je nachdem, wie Ihre Organisation strukturiert ist, können verschiedene Mitarbeiter oder Teams für unterschiedliche Facetten der Analytics-Verwaltung verantwortlich sein. Beispielsweise ist eine Person für die Benennung der Variablen verantwortlich, die in einer Implementierung verwendet werden sollen. Eine andere Person kann dafür verantwortlich sein, dass Benutzer Berichte korrekt abrufen können, indem sie sicherstellt, dass jeder über die richtigen Berechtigungen verfügt. Identifizieren Sie mindestens einen Benutzer, der für die Einstellungen und Benutzerberechtigungen in Analytics verantwortlich sein kann. Dieser kann dann weitere Analytics-Administratoren einladen.
* **Datenerfassungs-Administrierende:** Diese Benutzenden haben vollen Zugriff auf alle Komponenten in der Adobe Experience Platform-Datenerfassung, einschließlich Veröffentlichungsberechtigungen, der Berechtigung zur Container-Erstellung und Benutzerberechtigungen. Diese Benutzenden müssen nicht unbedingt Programmierkenntnisse haben, doch zumindest Anfängerkenntnisse in HTML, CSS und JavaScript sind von Vorteil. Diese Personen sind dafür verantwortlich, unter Zusammenarbeit mit den Website-Verantwortlichen Ihrer Organisation Tags auf Ihrer Website zu implementieren. Bestimmen Sie mindestens einen Benutzer bzw. eine Benutzerin, der/die für die Implementierung dieser Tags verantwortlich ist. Dieser bzw. diese kann dann weitere Datenerfassungs-Administrierende einladen.
* **Produktprofil-Administrierende:** Diese Benutzenden können Benutzer bzw. Benutzerinnen zu einem Produktprofil hinzufügen oder daraus entfernen, Berechtigungselemente in ihrem Produktprofil anpassen und Benutzergruppen Produktprofile zuweisen oder daraus entfernen. Produktprofil-Administrierende haben keinen vollständigen Zugriff auf Adobe Analytics. Diese Rolle eignet sich aber ideal für Team-Leiter oder Manager, die für ihr Team den Zugriff auf Adobe Analytics gewähren und verwalten müssen. Weitere Informationen zu Produktprofilen finden Sie unter [Produktprofile für Adobe Analytics](/help/admin/admin-console/permissions/product-profile.md).
* **Support-//Beauftragter**: Auch als unterstützte Benutzer bezeichnet, haben sie keine zusätzlichen Berechtigungen in der Analytics-Oberfläche. Stattdessen erhalten sie bei der Kommunikation mit der Adobe-Kundenunterstützung zusätzliche Berechtigungen. Diese Benutzer sind fast immer auch Analytics-Administratoren, da sie der Kundenunterstützung bei der Fehlerbehebung helfen. Identifizieren Sie mindestens einen Analytics-Administrator, der für die Erleichterung der Interaktionen zwischen Endbenutzern und der Adobe-Kundenunterstützung zuständig ist.
* **Website-Verantwortliche:** Diese Personen oder Teams sind für die Codierung und Entwicklung Ihrer Website verantwortlich. Sie benötigen keine Konten, sollten jedoch mit Datenerfassungs-Administratoren zusammenarbeiten, um den Tag-Code zu erhalten und ihn auf Ihrer Website zu implementieren.
* **Endbenutzer:** Diese Benutzer zeigen in der Regel Berichte an und suchen nach Antworten auf Geschäftsfragen. Analytics-Administratoren gewähren diesen Benutzern die Berechtigung, im Produkt zu arbeiten.

## Vollständigen Produktadministratorzugriff für Analytics gewähren

Administrierende auf Systemebene haben keinen direkten Zugriff auf Produkte, können sich jedoch Zugriff verschaffen, indem sie sich selbst als Administrator bzw. Administratorin auf Produktebene hinzufügen.

So gewähren Sie Adobe Analytics Zugriff auf sich selbst oder andere:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Admin Console](https://adminconsole.adobe.com/) an.
1. Klicken Sie oben auf die Registerkarte **[!UICONTROL Produkte]**. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken Sie auf **[!UICONTROL Adobe Analytics]** und dann auf die Schaltfläche **[!UICONTROL Neues Profil]**.
1. Geben Sie diesem Profil den Namen „Vollständiger Admin-Zugriff für Analytics“ und klicken Sie dann auf **[!UICONTROL Weiter]** > **[!UICONTROL Speichern]**.
1. Klicken Sie auf der Seite „Produktprofile“ auf das neu erstellte Profil und dann auf die Registerkarte **[!UICONTROL Zugriffsberechtigungen]**.
1. Klicken Sie auf eine der Berechtigungszeilen. Wenn die **[!UICONTROL automatische Einbindung]** verfügbar ist, aktivieren Sie diese. Wenn die **[!UICONTROL automatische Einbindung]** nicht verfügbar ist, klicken Sie auf **[!UICONTROL Alle hinzufügen]**. Mit beiden Optionen werden alle Berechtigungszeilen in die rechte Spalte verschoben.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Nachdem alle Zugriffsberechtigungskategorien dem Profil zugewiesen wurden, gehen Sie zur Produktseite zurück, indem Sie oben auf **[!UICONTROL Produkt]** klicken.
1. Klicken Sie unter der Kachel „Adobe Analytics“ auf **[!UICONTROL Benutzer zuweisen]**.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf **[!UICONTROL Speichern]**.

Der Benutzer hat jetzt vollständigen Zugriff auf Adobe Analytics.

## Gewähren des Produktadministratorzugriffs für die Datenerfassung in Experience Platform

Das Gewähren des Produktadministratorzugriffs für die Datenerfassung in Experience Platform ist nahezu identisch mit dem Gewähren des Produktadministratorzugriffs für Analytics.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Admin Console](https://adminconsole.adobe.com) an.
1. Klicken Sie oben auf die Registerkarte **[!UICONTROL Produkte]**. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken Sie auf **[!UICONTROL Experience Platform Launch]** und dann auf **[!UICONTROL Neues Profil]**.
1. Geben Sie diesem Profil den Namen „Vollständiger Admin-Zugriff zur Datenerfassung“ und klicken Sie dann auf **[!UICONTROL Fertig]**.
1. Klicken Sie auf der Seite **[!UICONTROL Produktprofile]** auf das neu erstellte Profil und dann auf die Registerkarte **[!UICONTROL Zugriffsberechtigungen]**.
1. Klicken Sie auf eine der Berechtigungszeilen. Wenn die **[!UICONTROL automatische Einbindung]** verfügbar ist, aktivieren Sie diese. Wenn die automatische Einbindung nicht verfügbar ist, klicken Sie auf **[!UICONTROL Alle hinzufügen]**. Mit beiden Optionen werden alle Berechtigungszeilen in die rechte Spalte verschoben.
1. Klicken Sie auf **[!UICONTROL Speichern]**. Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Sobald alle Zugriffsberechtigungskategorien dem Profil zugewiesen wurden, gehen Sie zur Seite „Überblick“ zurück, indem Sie oben auf **[!UICONTROL Überblick]** klicken.
1. Klicken Sie unter der Kachel [!UICONTROL Experience Platform Launch] auf **[!UICONTROL Benutzer zuweisen]**.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Der Benutzer hat jetzt vollständigen Zugriff auf die Datenerfassung in Experience Platform.

## Gewähren des Produktadministratorzugriffs für Produktprofile

Informationen zur Vergabe der Rolle von Produktprofil-Administrierenden an Benutzende finden Sie im Abschnitt „Verwalten von Produktprofil-Administrierenden“ im Artikel [Verwalten von Produktprofilen für Enterprise-Benutzende](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) im Enterprise-Benutzerhandbuch.

## Nächste Schritte

[Erstellen einer Report Suite](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Bitten Sie Ihren Analytics-Admininstrator bzw. Ihre Analytics-Administratorin, sich beim Tool anzumelden und eine Report Suite für die Datenerfassung zu erstellen

[Erstellen einer Analytics-Tag-Eigenschaft](/help/implement/launch/create-analytics-property.md): Bitten Sie Ihren Datenerfassungs-Administrator, sich beim Tool anzumelden und eine Eigenschaft zu erstellen, die auf Ihrer Site implementiert werden soll.

Bevor Benutzenden in Adobe Analytics Benutzerrollen zugewiesen werden können, muss ein Benutzer bzw. eine Benutzerin als erster Administrator bzw. erste Administratorin in Experience Cloud zugewiesen werden. Der erste Administrator bzw. die erste Administratorin kann dann Benutzenden in der Organisation wie in diesem Artikel beschrieben andere Rollen zuweisen.

Ein erster Administrator bzw. eine erste Administratorin ist der erste Schritt, um dem Rest der Organisation die Verwendung der einzelnen Experience Cloud-Lösungen zu ermöglichen.

Nach Vertragsunterzeichnung

1. Das Bereitstellungs-Team von Adobe bereitet die Erstellung des Kontos vor.

1. Der erste Administrator bzw. die erste Administratorin erhält vor dem Vertragsbeginn eine E-Mail mit Anmeldeinformationen.

>[!IMPORTANT]
>
>   Es wird dringend empfohlen zu überprüfen, ob die korrekten Kontaktinformationen des ersten Administrators bzw. der ersten Administratorin vor Vertragsabschluss an Adobe übermittelt wurden.
