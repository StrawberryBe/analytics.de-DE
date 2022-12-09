---
title: Administratorrollen in Adobe Analytics
description: Hier erfahren Sie, wie Sie mit Adobe Analytics, allgemeinen Rollentypen und der Anmeldung bei der Benutzeroberfläche beginnen.
feature: Admin Tools
exl-id: 9d10716f-5b66-42dc-b288-af34da203c35
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 58%

---

# Administratorrollen in Adobe Analytics

Adobe Analytics unterstützt verschiedene Arten von Administratoren. Vollständige Adobe Analytics-Administratoren haben Zugriff auf alles in Adobe Analytics, während andere Administratoren und Benutzer speziellere Aufgaben ausführen können.

>[!NOTE]
>
>Bevor Benutzern in Adobe Analytics Benutzerrollen zugewiesen werden können, muss ein Benutzer als erster Administrator in Experience Cloud zugewiesen werden. Der erste Administrator kann dann Benutzer in der Organisation mit anderen Schlüsselrollen versorgen, wie in diesem Artikel beschrieben. Weitere Informationen zum ersten Administrator finden Sie unter [Erste Administratorhandbuch für Adobe Analytics](/help/admin/admin-console/first-admin-guide.md).


## Schlüsselrollen in Experience Cloud und Adobe Analytics

Beachten Sie bei der Verwendung von Adobe Analytics die folgenden Schlüsselrollen:

* **Vollständige Adobe Analytics-Administratoren:** Diese Benutzer haben vollen Zugriff auf alles in Adobe Analytics, einschließlich Report Suite-Einstellungen und Benutzerberechtigungen. Je nachdem, wie Ihre Organisation strukturiert ist, können verschiedene Mitarbeiter oder Teams für unterschiedliche Facetten der Analytics-Verwaltung verantwortlich sein. Beispielsweise ist eine Person für die Benennung der Variablen verantwortlich, die in einer Implementierung verwendet werden sollen. Eine andere Person kann dafür verantwortlich sein, dass Benutzer Berichte korrekt abrufen können, indem sie sicherstellt, dass jeder über die richtigen Berechtigungen verfügt. Identifizieren Sie mindestens einen Benutzer, der für die Einstellungen und Benutzerberechtigungen in Analytics verantwortlich sein kann. Dieser kann dann weitere Analytics-Administratoren einladen.
* **Datenerfassungs-Administratoren:** Diese Benutzer haben vollen Zugriff auf alles in der Adobe Experience Platform-Datenerfassung, einschließlich Veröffentlichungsberechtigungen, Erstellen von Containern und Benutzerberechtigungen. Diese Benutzer müssen nicht unbedingt Programmierer sein, aber zumindest Anfängerkenntnisse in HTML, CSS und JavaScript sind von Vorteil. Sie sind dafür verantwortlich, mit den Website-Eigentümern Ihres Unternehmens zusammenzuarbeiten, um Tags auf Ihrer Site implementieren zu können. Bestimmen Sie mindestens einen Benutzer, der für die Implementierung in Ihrer Organisation verantwortlich ist. Dieser kann dann weitere Datenerfassungs-Administratoren einladen.
* **Produktprofiladministratoren:** Diese Benutzer können Benutzer zu einem Produktprofil hinzufügen oder daraus entfernen, Berechtigungselemente in ihrem Produktprofil anpassen und Benutzergruppen Produktprofile zuweisen oder daraus entfernen. Produktprofiladministratoren haben keinen vollständigen Zugriff auf Adobe Analytics. Sie eignen sich jedoch ideal für Teamleiter oder Manager, die Zugriff auf Adobe Analytics für ihr Team gewähren und verwalten müssen. Weitere Informationen zu Produktprofilen finden Sie unter [Produktprofile für Adobe Analytics](/help/admin/admin-console/permissions/product-profile.md).
* **Support-//Beauftragter**: Auch als unterstützte Benutzer bezeichnet, haben sie keine zusätzlichen Berechtigungen in der Analytics-Oberfläche. Stattdessen erhalten sie bei der Kommunikation mit der Adobe-Kundenunterstützung zusätzliche Berechtigungen. Diese Benutzer sind fast immer auch Analytics-Administratoren, da sie der Kundenunterstützung bei der Fehlerbehebung helfen. Identifizieren Sie mindestens einen Analytics-Administrator, der für die Erleichterung der Interaktionen zwischen Endbenutzern und der Adobe-Kundenunterstützung zuständig ist.
* **Website-Verantwortliche:** Diese Personen oder Teams sind für die Codierung und Entwicklung Ihrer Website verantwortlich. Sie benötigen keine Konten, sollten jedoch mit Datenerfassungs-Administratoren zusammenarbeiten, um den Tag-Code zu erhalten und ihn auf Ihrer Website zu implementieren.
* **Endbenutzer:** Diese Benutzer zeigen in der Regel Berichte an und suchen nach Antworten auf Geschäftsfragen. Analytics-Administratoren gewähren diesen Benutzern die Berechtigung, im Produkt zu arbeiten.

## Vollständigen Produktadministratorzugriff für Analytics gewähren

Administratoren auf Systemebene haben keinen direkten Zugriff auf Produkte. Sie können sich jedoch Zugriff verschaffen, indem sie sich selbst als Administrator auf Produktebene hinzufügen.

So gewähren Sie Adobe Analytics Zugriff auf sich selbst oder andere:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Admin Console](https://adminconsole.adobe.com/) an.
1. Klicken Sie oben auf die Registerkarte **[!UICONTROL Produkte]**. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken **[!UICONTROL Adobe Analytics]** und klicken Sie dann auf **[!UICONTROL Neues Profil]** Schaltfläche.
1. Geben Sie diesem Profil den Namen &quot;Vollständiger Admin-Zugriff für Analytics&quot;und klicken Sie auf **[!UICONTROL Nächste]** > **[!UICONTROL Speichern]**.
1. Klicken Sie auf der Seite Produktprofile auf das neu erstellte Profil und dann auf die Registerkarte **[!UICONTROL Zugriffsberechtigungen]**.
1. Klicken Sie auf eine der Berechtigungszeilen. Wenn die **[!UICONTROL automatische Einbindung]** verfügbar ist, aktivieren Sie diese. Wenn **[!UICONTROL Automatisch einschließen]** ist nicht verfügbar, klicken Sie auf **[!UICONTROL Alle hinzufügen]**. Beide Optionen verschieben alle Berechtigungszeilen in die rechte Spalte.
1. Klicken Sie auf **[!UICONTROL Speichern]**.
Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Nachdem alle Berechtigungskategorien dem Profil zugewiesen wurden, kehren Sie zur Seite Produkte zurück, indem Sie auf **[!UICONTROL Produkt]** oben.
1. Klicken Sie unter der Kachel &quot;Adobe Analytics&quot;auf **[!UICONTROL Benutzer zuweisen]**.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf **[!UICONTROL Speichern]**.

Der Benutzer hat jetzt vollständigen Zugriff auf Adobe Analytics.

## Gewähren des Produktadministratorzugriffs für die Datenerfassung in Experience Platform

Das Gewähren des Produktadministratorzugriffs für die Datenerfassung in Experience Platform ist nahezu identisch mit dem Gewähren des Produktadministratorzugriffs für Analytics.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Adobe Admin Console](https://adminconsole.adobe.com) an.
1. Klicken Sie oben auf die Registerkarte **[!UICONTROL Produkte]**. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken Sie auf **[!UICONTROL Experience Platform Launch]** und dann auf **[!UICONTROL Neues Profil]**.
1. Geben Sie diesem Profil den Namen „Vollständiger Admin-Zugriff zur Datenerfassung“ und klicken Sie dann auf **[!UICONTROL Fertig]**.
1. Klicken Sie auf der Seite **[!UICONTROL Produktprofile]** auf das neu erstellte Profil und dann auf die Registerkarte **[!UICONTROL Zugriffsberechtigungen]**.
1. Klicken Sie auf eine der Berechtigungszeilen. Wenn die **[!UICONTROL automatische Einbindung]** verfügbar ist, aktivieren Sie diese. Wenn die automatische Einbindung nicht verfügbar ist, klicken Sie auf **[!UICONTROL Alle hinzufügen]**. Beide Optionen verschieben alle Berechtigungszeilen in die rechte Spalte.
1. Klicken Sie auf **[!UICONTROL Speichern]**. Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Sobald alle Zugriffsberechtigungskategorien dem Profil zugewiesen wurden, gehen Sie zur Seite „Überblick“ zurück, indem Sie oben auf **[!UICONTROL Überblick]** klicken.
1. Klicken Sie unter der Kachel [!UICONTROL Experience Platform Launch] auf **[!UICONTROL Benutzer zuweisen]**.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Der Benutzer hat jetzt vollständigen Zugriff auf die Datenerfassung in Experience Platform.

## Produktadministratorzugriff für Produktprofile gewähren

Informationen zum Zuweisen von Benutzern zu Produktprofiladministratoren finden Sie im Abschnitt &quot;Verwalten von Produktprofiladministratoren&quot;im Artikel, [Verwalten von Produktprofilen für Unternehmensbenutzer](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) im Enterprise-Benutzerhandbuch.

## Nächste Schritte

[Erstellen einer Report Suite](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Bitten Sie Ihren Analytics-Administrator, sich beim Tool anzumelden und eine Report Suite für die Datenerfassung zu erstellen

[Erstellen einer Analytics-Tag-Eigenschaft](/help/implement/launch/create-analytics-property.md): Bitten Sie Ihren Datenerfassungs-Administrator, sich beim Tool anzumelden und eine Eigenschaft zu erstellen, die auf Ihrer Site implementiert werden soll.

Bevor Benutzern in Adobe Analytics Benutzerrollen zugewiesen werden können, muss ein Benutzer als erster Administrator in Experience Cloud zugewiesen werden. Der erste Administrator kann dann Benutzer in der Organisation mit anderen Schlüsselrollen versorgen, wie in diesem Artikel beschrieben.

Ein erster Administrator ist der Ausgangspunkt, um dem Rest der Organisation die Verwendung der einzelnen Experience Cloud-Lösungen zu ermöglichen.

Nach Vertragsunterzeichnung

1. Das Bereitstellungsteam von Adobe bereitet die Erstellung des Kontos vor.

1. Der erste Administrator erhält vor dem Vertragsbeginn eine E-Mail mit Anmeldeinformationen.

>[!IMPORTANT]
>
>   Es wird dringend empfohlen, sicherzustellen, dass die korrekten Kontaktinformationen des ersten Administrators vor Vertragsabschluss an Adobe weitergegeben werden.
