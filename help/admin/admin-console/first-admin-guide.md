---
title: Adobe Analytics-Handbuch für erste Administratoren
description: Hier erfahren Sie, wie Sie mit Adobe Analytics, allgemeinen Rollentypen und der Anmeldung bei der Benutzeroberfläche beginnen.
translation-type: ht
source-git-commit: 632fa007fecadf01e2cef67fd3c2519799636e46
workflow-type: ht
source-wordcount: '943'
ht-degree: 100%

---


# Adobe Analytics-Handbuch für erste Administratoren

Ein erster Administrator ist der Ausgangspunkt, um dem Rest der Organisation die Verwendung der einzelnen Experience Cloud-Lösungen zu ermöglichen. Nachdem ein Vertrag unterzeichnet wurde, bereitet ein Bereitstellungsteam von Adobe die Erstellung des Kontos vor. Der erste Administrator erhält vor dem Vertragsbeginn eine E-Mail mit Anmeldeinformationen. Es wird dringend empfohlen, sicherzustellen, dass die korrekten Kontaktinformationen des ersten Administrators vor Vertragsabschluss an Adobe weitergegeben werden.

## Schlüsselrollen bei der Verwendung von Experience Cloud

Wenn Ihre Organisation Adobe Analytics erworben hat, sollten Sie folgende wichtige Rollen berücksichtigen:

* **Adobe Analytics-Administratoren:** Diese Benutzer haben vollen Zugriff auf alle Funktionen in Adobe Analytics, einschließlich Report Suite-Einstellungen und Benutzerberechtigungen. Je nachdem, wie Ihre Organisation strukturiert ist, können verschiedene Mitarbeiter oder Teams für unterschiedliche Facetten der Analytics-Verwaltung verantwortlich sein. Beispielsweise ist eine Person für die Benennung der Variablen verantwortlich, die in einer Implementierung verwendet werden sollen. Eine andere Person kann dafür verantwortlich sein, dass Benutzer Berichte korrekt abrufen können, indem sie sicherstellt, dass jeder über die richtigen Berechtigungen verfügt. Identifizieren Sie mindestens einen Benutzer, der für die Einstellungen und Benutzerberechtigungen in Analytics verantwortlich sein kann. Dieser kann dann weitere Analytics-Administratoren einladen.
* **Adobe Experience Platform Launch-Administratoren:** Diese Benutzer haben vollen Zugriff auf alle Funktionen von Experience Platform Launch, einschließlich Veröffentlichungsberechtigungen, Erstellen von Containern und Benutzerberechtigungen. Diese Benutzer sind nicht unbedingt Programmierer, aber zumindest Anfängerkenntnisse in HTML, CSS und JavaScript sind von Vorteil. Sie sind dafür verantwortlich, mit den Website-Eigentümern Ihrer Organisation zusammenzuarbeiten, um den Experience Platform Launch-Code auf Ihrer Site implementieren zu können. Identifizieren Sie mindestens einen Benutzer, der für die Implementierung Ihrer Organisation verantwortlich ist. Dieser kann dann weitere Experience Platform Launch-Administratoren einladen.
* **Support-//Beauftragter**: Auch als unterstützte Benutzer bezeichnet, haben sie keine zusätzlichen Berechtigungen in der Analytics-Oberfläche. Stattdessen erhalten sie bei der Kommunikation mit der Adobe-Kundenunterstützung zusätzliche Berechtigungen. Diese Benutzer sind fast immer auch Analytics-Administratoren, da sie der Kundenunterstützung bei der Fehlerbehebung helfen. Identifizieren Sie mindestens einen Analytics-Administrator, der für die Erleichterung der Interaktionen zwischen Endbenutzern und der Adobe-Kundenunterstützung zuständig ist.
* **Website-Eigentümer:** Diese Personen oder Teams sind für die Codierung und Entwicklung Ihrer Website verantwortlich. Sie benötigen keine Konten, sollten jedoch mit Experience Platform Launch-Administratoren zusammenarbeiten, um den Experience Platform Launch-Code zu erhalten und ihn auf Ihrer Website zu implementieren.
* **Endbenutzer:** Diese Benutzer zeigen in der Regel Berichte an und suchen nach Antworten auf Geschäftsfragen. Analytics-Administratoren gewähren diesen Benutzern die Berechtigung, im Produkt zu arbeiten.

Als erster Administrator kann Ihre Rolle mit einer oder mehreren dieser Rollen überlappen. Solange diese grundlegenden Aufgaben abgedeckt sind, können Sie Berechtigungen erteilen, damit andere Mitarbeiter in Ihrer Organisation arbeiten können.

## Gewähren des Produktadministratorzugriffs für Analytics

Administratoren auf Systemebene haben keinen direkten Zugriff auf Produkte, können sich jedoch Zugriff verschaffen, indem sie sich selbst als Administrator auf Produktebene hinzufügen. Wenn Sie sich oder anderen Zugriff auf Adobe Analytics gewähren möchten, führen Sie die folgenden Schritte aus.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Admin Console](https://adminconsole.adobe.com/) an.
1. Klicken Sie oben auf die Registerkarte „Produkte“. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken Sie auf „Adobe Analytics“ und dann auf die Schaltfläche „Neues Profil“.
1. Geben Sie diesem Profil den Namen „Vollständiger Admin-Zugriff für Analytics“ und klicken Sie dann auf „Fertig“.
1. Klicken Sie auf der Seite „Produktprofile“ auf das neu erstellte Profil und dann auf die Registerkarte „Zugriffsberechtigungen“.
1. Klicken Sie auf eine der Berechtigungspositionen. Wenn die automatische Einbindung verfügbar ist, aktivieren Sie diese. Wenn die automatische Einbindung nicht verfügbar ist, klicken Sie auf „Alle hinzufügen“. Beide Optionen verschieben alle Berechtigungselemente in die rechte Spalte.
1. Klicken Sie auf „Speichern“. Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Sobald alle Berechtigungskategorien dem Profil zugewiesen wurden, gehen Sie zur Seite „Überblick“ zurück, indem Sie oben auf „Überblick“ klicken.
1. Klicken Sie im Bereich „Adobe Analytics“ auf „Benutzer zuweisen“.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf „Speichern“.
1. Der Benutzer hat jetzt vollständigen Zugriff auf Adobe Analytics.

## Gewähren des Produktadministratorzugriffs für Experience Platform Launch

Der Produktadministratorzugriff für Experience Platform Launch ist nahezu identisch mit dem Gewähren des Produktadministratorzugriffs für Analytics.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der Admin Console an.
1. Klicken Sie oben auf die Registerkarte „Produkte“. Alle von Ihrer Organisation erworbenen Produkte befinden sich auf der linken Seite. Klicken Sie auf „Experience Platform Launch“ und dann auf die Schaltfläche „Neues Profil“.
1. Geben Sie diesem Profil den Namen „Vollständiger Admin-Zugriff für Experience Plattform Launch“ und klicken Sie dann auf „Fertig“.
1. Klicken Sie auf der Seite „Produktprofile“ auf das neu erstellte Profil und dann auf die Registerkarte „Zugriffsberechtigungen“.
1. Klicken Sie auf eine der Berechtigungspositionen. Wenn die automatische Einbindung verfügbar ist, aktivieren Sie diese. Wenn die automatische Einbindung nicht verfügbar ist, klicken Sie auf „Alle hinzufügen“. Beide Optionen verschieben alle Berechtigungselemente in die rechte Spalte.
1. Klicken Sie auf „Speichern“. Wiederholen Sie den obigen Schritt für alle Berechtigungskategorien.
1. Sobald alle Berechtigungskategorien dem Profil zugewiesen wurden, gehen Sie zur Seite „Überblick“ zurück, indem Sie oben auf „Überblick“ klicken.
1. Klicken Sie im Bereich „Experience Platform Launch“ auf „Benutzer zuweisen“.
1. Geben Sie die E-Mail-Adresse ein, der Sie vollständigen Zugriff auf Analytics gewähren möchten, und weisen Sie ihr das neu erstellte vollständige Administratorzugriffsprofil zu. Klicken Sie auf „Speichern“.
1. Der Benutzer hat jetzt vollständigen Zugriff auf Experience Platform Launch.

## Nächste Schritte

[Erstellen einer Report Suite](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Bitten Sie Ihren Analytics-Administrator, sich beim Tool anzumelden und eine Report Suite für die Datenerfassung zu erstellen

[Erstellen einer Eigenschaft in Experience Platform Launch](/help/implement/launch/create-analytics-property.md): Bitten Sie Ihren Experience Platform Launch-Administrator, sich beim Tool anzumelden und eine Eigenschaft zu erstellen, um Ihre Site zu implementieren
