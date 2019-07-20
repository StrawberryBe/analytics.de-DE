---
title: Report Suite erstellen
seo-title: Erstellen einer Report Suite in Adobe Analytics
description: Erstellen Sie einen einfachen Container für die Datenerfassung in Adobe Analytics.
seo-description: Erstellen Sie einen einfachen Container für die Datenerfassung in Adobe Analytics.
translation-type: tm+mt
source-git-commit: d195fb85711f58383577bf1d7b4da4078b909427

---


# Report Suite erstellen

Eine Report Suite ist eine Silo von Daten, die Adobe Analytics zum Abrufen von Berichten verwendet. Eine Organisation kann über viele Report Suites verfügen, die jeweils unterschiedliche Datensätze enthalten. Obwohl in der Vergangenheit separate Report Suites wichtig waren, hat sich die Verwendung einer einzelnen Report Suite vorteilhafter. Die Einführung in Virtual Report Suites und die Berichtszeitverarbeitung ermöglicht es einem Benutzer, eigene Daten zu erstellen, wodurch die Flexibilität und die Site-spezifische Daten flexibel abgerufen werden können.

Dieser Artikel wurde für Administratoren auf Systemadministratoren oder Analytics-Administratoren entwickelt, um die Datenerfassung vorzubereiten.

## Voraussetzungen

[Adobe Analytics Erste Admin-Handbuch](first-admin-guide.md): Sicherstellen, dass ein Administrator auf Systemebene Ihnen über die Experience Cloud Admin-Konsole Zugriff auf Adobe Analytics gewährt hat

## Report Suite erstellen

> [!NOTE]Hinweis: Sie können auch eine Report Suite in Adobe Analytics mithilfe des Legacy-Administrators erstellen. Adobe empfiehlt die Verwendung des hier beschriebenen Setup-Assistenten für die Report Suite.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
1. Klicken Sie oben rechts auf das 9-quadratische Symbol und dann auf das farbige Analytics-Logo.
1. Das modale Fenster "Willkommen in Adobe Analytics" sollte automatisch geöffnet werden. Klicken Sie auf das Hilfesymbol oben rechts und wählen Sie dann "Willkommen bei Adobe Analytics" .
1. Klicken Sie im modalen Fenster auf "Einstellungen starten" .
1. Folgen Sie jeder Aufforderung, die die Grundlagen wie den Eigenschaftstyp, die Branche und die Zeitzone erläutert. Klicken Sie auf Weiter.
1. Die Report Suite wird jetzt erstellt. Adobe empfiehlt auch, eine Entwicklungs-Report Suite zu verwenden, sodass die Kundendaten keine Daten enthalten. Klicken Sie oben rechts auf das Hilfesymbol und wählen Sie dann erneut "Willkommen bei Adobe Analytics" .
1. Klicken Sie im modalen Fenster auf "Einstellungen starten" .
Benennen Sie diese Report Suite mit Ausnahme von "- DEV" am Ende. Da diese Report Suite nur internen Traffic erhält, kann die geschätzte Größe die kleinste sein.
1. Klicken Sie auf Weiter, um die dev-Report Suite zu erstellen.

## Fehlerbehebung 

**Nach der Anmeldung bei Experience Cloud wird das Analytics-Symbol grau abgeblendet.**

Das bedeutet, dass Ihrem Konto nicht die korrekten Berechtigungen für Analytics gewährt wurden. Arbeiten Sie mit einem Administrator auf Systemebene in Ihrer Organisation zusammen, um sicherzustellen, dass Sie einem Profil mit ausreichenden Berechtigungen für den Zugriff auf Adobe Analytics angehören.

**Nach der Anmeldung bei Adobe Analytics fehlt das Popup und die Dropdown-Liste "Willkommen bei Adobe Analytics" .**

Stellen Sie sicher, dass Sie sich über die Experience Cloud angemeldet haben und nicht über meine. omniture. com. Benutzer, die sich über my.omniture.com anmelden, verfügen nicht über den Report Suite-Setup-Assistenten.

## Nächste Schritte

[Erstellen und konfigurieren Sie eine Eigenschaft für Adobe Analytics im Start](../../implement/implement-with-launch/create-analytics-property.md): Erstellen eines Bereichs zur Verwaltung Ihrer Analytics-Implementierung
