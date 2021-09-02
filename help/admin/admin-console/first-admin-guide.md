---
title: Adobe Analytics-Handbuch für erste Administratoren
description: Hier erfahren Sie, wie Sie mit Adobe Analytics, allgemeinen Rollentypen und der Anmeldung bei der Benutzeroberfläche beginnen.
exl-id: fbbbd335-0d22-473e-adef-f92f8eab7bf0
source-git-commit: 9a70d79a83d8274e17407229bab0273abbe80649
workflow-type: ht
source-wordcount: '942'
ht-degree: 100%

---

# Adobe Analytics-Handbuch für erste Administratoren

Ein erster Administrator ist der Ausgangspunkt, um dem Rest der Organisation die Verwendung der einzelnen Experience Cloud-Lösungen zu ermöglichen. Nachdem ein Vertrag unterzeichnet wurde, bereitet ein Bereitstellungsteam von Adobe die Erstellung des Kontos vor. Der erste Administrator erhält vor dem Vertragsbeginn eine E-Mail mit Anmeldeinformationen. Es wird dringend empfohlen, sicherzustellen, dass die korrekten Kontaktinformationen des ersten Administrators vor Vertragsabschluss an Adobe weitergegeben werden.

## Schlüsselrollen bei der Verwendung von Experience Cloud

Wenn Ihre Organisation Adobe Analytics erworben hat, sollten Sie folgende wichtige Rollen berücksichtigen:

* **Adobe Analytics-Administratoren:** Diese Benutzer haben vollen Zugriff auf alle Funktionen in Adobe Analytics, einschließlich Report Suite-Einstellungen und Benutzerberechtigungen. Je nachdem, wie Ihre Organisation strukturiert ist, können verschiedene Mitarbeiter oder Teams für unterschiedliche Facetten der Analytics-Verwaltung verantwortlich sein. Beispielsweise ist eine Person für die Benennung der Variablen verantwortlich, die in einer Implementierung verwendet werden sollen. Eine andere Person kann dafür verantwortlich sein, dass Benutzer Berichte korrekt abrufen können, indem sie sicherstellt, dass jeder über die richtigen Berechtigungen verfügt. Identifizieren Sie mindestens einen Benutzer, der für die Einstellungen und Benutzerberechtigungen in Analytics verantwortlich sein kann. Dieser kann dann weitere Analytics-Administratoren einladen.
* **Datenerfassungs-Administratoren**: Diese Benutzer haben vollen Zugriff auf alle Elemente in der Datenerfassungs-Benutzeroberfläche (ehemals Experience Platform Launch-Benutzeroberfläche), einschließlich Veröffentlichungsberechtigungen, der Berechtigung zur Erstellung von Containern und Benutzerberechtigungen. Diese Benutzer müssen nicht unbedingt Programmierer sein, aber zumindest Anfängerkenntnisse in HTML, CSS und JavaScript sind von Vorteil. Diese Personen sind dafür verantwortlich, mit den Website-Verantwortlichen Ihrer Organisation zusammenzuarbeiten, um die Experience Platform-Tags auf Ihrer Site zu implementieren. Bestimmen Sie mindestens einen Benutzer, der für die Implementierung in Ihrer Organisation verantwortlich ist. Dieser kann dann weitere Datenerfassungs-Administratoren einladen.
* **Support-//Beauftragter**: Auch als unterstützte Benutzer bezeichnet, haben sie keine zusätzlichen Berechtigungen in der Analytics-Oberfläche. Stattdessen erhalten sie bei der Kommunikation mit der Adobe-Kundenunterstützung zusätzliche Berechtigungen. Diese Benutzer sind fast immer auch Analytics-Administratoren, da sie der Kundenunterstützung bei der Fehlerbehebung helfen. Identifizieren Sie mindestens einen Analytics-Administrator, der für die Erleichterung der Interaktionen zwischen Endbenutzern und der Adobe-Kundenunterstützung zuständig ist.
* **Website-Verantwortliche:** Diese Personen oder Teams sind für die Codierung und Entwicklung Ihrer Website verantwortlich. Sie benötigen keine Konten, sollten jedoch mit Datenerfassungs-Administratoren zusammenarbeiten, um den Tag-Code zu erhalten und ihn auf Ihrer Website zu implementieren.
* **Endbenutzer:** Diese Benutzer zeigen in der Regel Berichte an und suchen nach Antworten auf Geschäftsfragen. Analytics-Administratoren gewähren diesen Benutzern die Berechtigung, im Produkt zu arbeiten.

Als erster Administrator kann Ihre Rolle mit einer oder mehreren dieser Rollen überlappen. Solange diese grundlegenden Aufgaben abgedeckt sind, können Sie Berechtigungen erteilen, damit andere Mitarbeiter in Ihrer Organisation arbeiten können.

## Gewähren des Produktadministratorzugriffs für Analytics

Administratoren auf Systemebene haben keinen direkten Zugriff auf Produkte, können sich jedoch Zugriff verschaffen, indem sie sich selbst als Administrator auf Produktebene hinzufügen. Wenn Sie sich oder anderen Zugriff auf Adobe Analytics gewähren möchten, führen Sie die folgenden Schritte aus.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Admin Console](https://adminconsole.adobe.com/) an.
1. Klicken Sie oben auf die Registerkarte „Produkte“. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken Sie auf „Adobe Analytics“ und dann auf die Schaltfläche „Neues Profil“.
1. Geben Sie diesem Profil den Namen „Vollständiger Admin-Zugriff für Analytics“ und klicken Sie dann auf „Fertig“.
1. Klicken Sie auf der Seite „Produktprofile“ auf das neu erstellte Profil und dann auf die Registerkarte „Zugriffsberechtigungen“.
1. Klicken Sie auf eine der Berechtigungszeilen. Wenn die automatische Einbindung verfügbar ist, aktivieren Sie diese. Wenn die automatische Einbindung nicht verfügbar ist, klicken Sie auf „Alle hinzufügen“. Beide Optionen verschieben alle Berechtigungszeilen in die rechte Spalte.
1. Klicken Sie auf „Speichern“. Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Sobald alle Berechtigungskategorien dem Profil zugewiesen wurden, gehen Sie zur Seite „Überblick“ zurück, indem Sie oben auf „Überblick“ klicken.
1. Klicken Sie im Bereich „Adobe Analytics“ auf „Benutzer zuweisen“.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf „Speichern“.
1. Der Benutzer hat jetzt vollständigen Zugriff auf Adobe Analytics.

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

## Nächste Schritte

[Erstellen einer Report Suite](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Bitten Sie Ihren Analytics-Administrator, sich beim Tool anzumelden und eine Report Suite für die Datenerfassung zu erstellen

[Erstellen einer Analytics-Tag-Eigenschaft](/help/implement/launch/create-analytics-property.md): Bitten Sie Ihren Datenerfassungs-Administrator, sich beim Tool anzumelden und eine Eigenschaft zu erstellen, die auf Ihrer Site implementiert werden soll.
