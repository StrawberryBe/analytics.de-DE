---
title: Report Suite erstellen
description: Erstellen Sie einen einfachen Container für die Datenerfassung in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 6c57780d0ecf65669c1a5306dde267f6e48f1cc4

---


# Report Suite erstellen

Bei einer Report Suite handelt es sich um ein Datenwörterbuch, mit dem Adobe Analytics Berichte abruft. Eine Organisation kann über viele Report Suites verfügen, die jeweils unterschiedliche Datensätze enthalten. Auch wenn in der Vergangenheit separate Report Suites wichtig waren, hat sich die Verwendung einer einzelnen Report Suite noch verbessert. Die Einführung in Virtual Report Suites und die Verarbeitung der Berichtszeit ermöglichen es dem Benutzer, eigene Datenuntergruppen zu erstellen, sodass er flexibel sowohl globale als auch Site-spezifische Daten abrufen kann.

Dieser Artikel wurde für Administratoren oder Analytics-Administratoren auf Systemebene zur Vorbereitung auf die Datenerfassung entwickelt.

## Voraussetzungen

[Adobe Analytics First Admin Guide](first-admin-guide.md): Vergewissern Sie sich, dass Ihnen ein Systemadministrator über die Experience Cloud Admin Console Zugriff auf Adobe Analytics gewährt hat.

## Report Suite erstellen

> [!NOTE] Es gibt auch eine Möglichkeit, eine Report Suite in Adobe Analytics mit dem alten Administrator zu erstellen. Adobe empfiehlt die Verwendung des hier beschriebenen Assistenten zum Einrichten der Report Suite.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
1. Das modale Fenster "Willkommen bei Adobe Analytics"sollte automatisch angezeigt werden. Wenn nicht, klicken Sie auf das Hilfesymbol oben rechts und wählen Sie dann "Willkommen bei Adobe Analytics".
1. Klicken Sie im modalen Fenster auf Setup starten.
1. Folgen Sie jeder Eingabeaufforderung, die die Grundlagen wie Eigenschaftstyp, Branchen und Zeitzone skizziert. Klicken Sie auf Weiter.
1. Die Report Suite wird jetzt erstellt. Adobe empfiehlt auch eine Entwicklungs-Report Suite, sodass Tests keine Kundendaten beeinträchtigen. Klicken Sie oben rechts auf das Hilfesymbol und wählen Sie dann erneut "Willkommen bei Adobe Analytics".
1. Klicken Sie im modalen Fenster auf Setup starten.
Benennen Sie diese Report Suite gleich, außer am Ende "- DEV"anhängen. Da diese Report Suite nur internen Traffic erhält, kann die geschätzte Größe die kleinste sein.
1. Klicken Sie auf Weiter, um Ihre dev-Report Suite zu erstellen.

## Fehlerbehebung

**Nach der Anmeldung bei Experience Cloud ist das Analytics-Symbol grau ausgeblendet.**

Das bedeutet, dass Ihrem Konto nicht die richtigen Berechtigungen für Analytics erteilt wurden. Arbeiten Sie mit einem Administrator auf Systemebene in Ihrem Unternehmen zusammen, um sicherzustellen, dass Sie zu einem Profil gehören, das über ausreichende Zugriffsberechtigungen für Adobe Analytics verfügt.

**Nach der Anmeldung bei Adobe Analytics fehlt das Popup- und Dropdown-Menü "Willkommen bei Adobe Analytics".**

Stellen Sie sicher, dass Sie sich über die Experience Cloud und nicht über my.omniture.com angemeldet haben. Für Benutzer, die sich über my.omniture.com anmelden, steht der Assistent zum Einrichten der Report Suite nicht zur Verfügung.

## Nächste Schritte

[Erstellen und konfigurieren Sie eine Eigenschaft für Adobe Analytics in Launch](/help/implement/implement-with-launch/create-analytics-property.md): Erstellen eines Bereichs zur Verwaltung Ihrer Analytics-Implementierung
