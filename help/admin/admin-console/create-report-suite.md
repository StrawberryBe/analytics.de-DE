---
title: Erstellen einer Report Suite
description: Erstellen Sie einen einfachen Container für die Datenerfassung in Adobe Analytics.
translation-type: tm+mt
source-git-commit: 6efb60ae2f565e67426c78bf830ada655e29b3af
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 100%

---


# Erstellen einer Report Suite

Bei einer Report Suite handelt es sich um einen Datenspeicher, mit dem Adobe Analytics Berichte abruft. Eine Organisation kann über viele Report Suites verfügen, die jeweils unterschiedliche Datensätze enthalten. Auch wenn in der Vergangenheit separate Report Suites wichtig waren, hat sich eine einzelne Report Suite als vorteilhafter erwiesen. Die Einführung in Virtual Report Suites und die Verarbeitung von Berichtszeiten ermöglichen es dem Benutzer, eigene Datenuntergruppen zu erstellen, sodass er flexibel sowohl globale als auch Site-spezifische Daten abrufen kann.

Dieser Artikel wurde für Administratoren oder Analytics-Administratoren auf Systemebene zur Vorbereitung auf die Datenerfassung erstellt.

## Voraussetzungen

[Adobe Analytics-Handbuch für erste Administratoren](first-admin-guide.md): Vergewissern Sie sich, dass Ihnen ein Systemadministrator über die Experience Cloud Admin Console Zugriff auf Adobe Analytics gewährt hat.

## Erstellen einer Report Suite {#create-report-suite}

>[!NOTE]
>
>Es gibt auch eine Möglichkeit, eine Report Suite in Adobe Analytics mithilfe des veralteten Administrators zu erstellen. Adobe empfiehlt die Verwendung des hier beschriebenen Assistenten zur Report Suite-Einrichtung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
1. Das modale Fenster „Willkommen bei Adobe Analytics“ sollte automatisch angezeigt werden. Wenn nicht, klicken Sie auf das Hilfesymbol oben rechts und wählen Sie dann „Willkommen bei Adobe Analytics“ aus.
1. Klicken Sie im modalen Fenster auf „Einrichtung beginnen“.
1. Folgen Sie jeder Eingabeaufforderung, die die Grundlagen wie Eigenschaftstyp, Branchen und Zeitzone beschreibt. Klicken Sie auf „Weiter“.
1. Die Report Suite wird jetzt erstellt. Adobe empfiehlt auch eine Entwicklungs-Report Suite, sodass Tests keine Kundendaten beeinträchtigen. Klicken Sie oben rechts auf das Hilfesymbol und wählen Sie dann erneut „Willkommen bei Adobe Analytics“ aus.
1. Klicken Sie im modalen Fenster auf „Einrichtung beginnen“.
Geben Sie dieser Report Suite denselben Namen und hängen Sie am Ende „- DEV“an. Da diese Report Suite nur internen Traffic erhält, kann die geschätzte Größe die kleinste sein.
1. Klicken Sie auf „Weiter“, um Ihre dev-Report Suite zu erstellen.

Weitere Informationen zu den Schritten in diesem modalen Fenster finden Sie unter [Implementierungs-Modal](/help/implement/prepare/implementation-modal.md) im Benutzerhandbuch zu Implementierungen.

## Fehlerbehebung

**Nach der Anmeldung bei Experience Cloud ist das Analytics-Symbol grau ausgeblendet.**

Das bedeutet, dass Ihrem Konto nicht die richtigen Berechtigungen für Analytics erteilt wurden. Arbeiten Sie mit einem Administrator auf Systemebene in Ihrer Organisation zusammen, um sicherzustellen, dass Sie zu einem Profil gehören, das über ausreichende Zugriffsberechtigungen für Adobe Analytics verfügt.

**Nach der Anmeldung bei Adobe Analytics fehlt das Popup- und Dropdown-Menü „Willkommen bei Adobe Analytics“.**

Stellen Sie sicher, dass Sie sich über Experience Cloud und nicht über my.omniture.com angemeldet haben. Für Benutzer, die sich über my.omniture.com anmelden, steht der Assistent zur Report Suite-Einrichtung nicht zur Verfügung.

## Nächste Schritte

[Erstellen und Konfigurieren einer Eigenschaft für Adobe Analytics in Launch](/help/implement/launch/create-analytics-property.md): Erstellen Sie einen Bereich zur Verwaltung Ihrer Analytics-Implementierung
