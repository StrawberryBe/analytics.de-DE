---
title: Produktprofile für Adobe Analytics
description: Erfahren Sie, wie Profil als Berechtigungsvorgaben verwendet werden können, die Produktadministratoren Benutzern innerhalb eines Unternehmens zuweisen können.
exl-id: 834e4cf1-20b0-4c9d-939a-19e00494c8dd
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 97%

---

# Produktprofile für Adobe Analytics

Produktprofile sind Berechtigungsvorgaben, die Produktadministratoren Benutzern in einer Organisation zuweisen können. Wenn Sie ein Produktprofil erstellen und diesem Produktprofil einen Experience Cloud-Benutzer zuweisen, übernehmen diese die im Produktprofil enthaltenen Berechtigungselemente.

Allgemeine Informationen zu Produktprofilen finden Sie unter [Verwalten von Produkten und Profilen](https://helpx.adobe.com/de/enterprise/using/manage-products-and-profiles.html) im Enterprise-Benutzerhandbuch.

## Produktprofiladministratoren

Produktprofiladministratoren sind eine optionale Gruppe, die Benutzer zu diesem Produktprofil hinzufügen oder entfernen kann. Beachten Sie, dass ein Produktprofiladministrator nicht mit einem Produktadministrator identisch ist:

* Produktprofiladministratoren haben keinen vollständigen Zugriff auf Adobe Analytics. Der uneingeschränkte Zugriff auf Adobe Analytics ist Produktadministratoren vorbehalten.
* Produktprofiladministratoren können die Berechtigungselemente in ihrem Produktprofil anpassen.
* Produktprofiladministratoren können Benutzergruppen Produktprofile zuweisen oder entziehen.
* Produktprofiladministratoren eignen sich ideal für Teamleiter oder Manager, die für ihr Team den Zugriff auf Adobe Analytics gewähren und verwalten müssen. Für Einzelpersonen ist es nicht erforderlich, dass Systemadministratoren oder Produktadministratoren sich die Mühe geben, Zugriff auf Adobe Analytics zu gewähren.

## Adobe Analytics-Berechtigungselemente

Für den Zugriff auf Adobe Analytics sind in einem Produktprofil mindestens folgende Berechtigungen erforderlich:

* Das Produktprofil muss Zugriff auf mindestens eine Report Suite haben
* Das Produktprofil muss zum Berechtigungselement **Zugriff auf Analysis Workspace** (oder **Zugriff auf Reports &amp; Analytics**) in Analytics Tools gehören

### Report Suites

Ermöglicht Zugriff auf Report Suites, die zu Ihrer Organisation in Analytics gehören. Ein Benutzer muss zu mindestens einer Report Suite gehören, um Zugriff auf Adobe Analytics erhalten zu können.

### Metriken

Ermöglicht Zugriff auf Metriken in Ihrer Report Suite. Metriken werden als ihre jeweilige Komponente in Analysis Workspace aufgelistet, oder wenn die Metrik in Reports &amp; Analytics verfügbar ist, als Menüpunkt unter „Site-Metriken“.

Benutzerdefinierte Metriken werden als „Benutzerspezifisches Ereignis 1-1000“ bezeichnet, um sie unabhängig von Report Suites zu halten. Wenn „Benutzerspezifisches Ereignis 1“ ein aktiviertes Berechtigungselement ist, hat dieser Benutzer Zugriff auf „event1“ in allen Report Suites des Produktprofils.

### Dimensionen

Gewährt Zugriff auf Dimensionen in Ihrer Report Suite. Dimensionen werden als ihre jeweilige Komponente in Analysis Workspace aufgelistet, oder wenn die Dimension in Reports &amp; Analytics verfügbar ist, als Menüpunkt.

Benutzerdefinierte Variablen, wie z. B. eVars, werden als „Benutzerspezifische Konversion 1-250“ bezeichnet, um sie unabhängig von Report Suites zu halten. Wenn „Benutzerspezifische Konversion 1“ ein aktiviertes Berechtigungselement ist, hat dieser Benutzer Zugriff auf „eVar1“ in allen Report Suites des Produktprofils.

### Report Suite-Tools

Die Berechtigungselemente der Report Suite-Tools gewähren Zugriff auf Funktionen, die spezifisch für die Report Suites sind, auf die der Benutzer Zugriff hat. Eine vollständige Liste der Berechtigungselemente und Beschreibungen finden Sie unter [Report Suite-Tools](report-suite-tools.md).

### Analytics-Tools

Die Berechtigungselemente der Analytics-Tools gewähren Zugriff auf Funktionen, die unabhängig von den Report Suite-Einstellungen sind. Eine vollständige Liste der Berechtigungselemente und Beschreibungen finden Sie bei den [Produktprofilberechtigungen für Analytics-Werkzeuge](analytics-tools.md).

## Produktprofilentwickler

Entwickler ähneln Benutzern, allerdings können sie die Experience Cloud API auf Adobe I/O verwenden. Weitere Informationen finden Sie unter [Verwalten von Entwicklern](https://helpx.adobe.com/de/enterprise/using/manage-developers.html) im Enterprise-Benutzerhandbuch. Wenn einem Benutzer Entwicklerzugriff für ein beliebiges Profil gewährt wird, kann er auf Developer Console (console.adobe.io) zugreifen und Adobe Analytics-Integrationen bearbeiten. Die für den Benutzer autorisierten Analytics-API-Aufrufe und -Antworten hängen von den Netzberechtigungen aller Profile ab, bei denen der Benutzer Entwicklerzugriff hat.

Beispielsweise könnte ein Nutzer mit Entwicklerzugriff bei einem Profil, bei dem die Profilberechtigungen alle Metriken, alle Dimensionen und eine Report Suite mit einschließen, API-Aufrufe für jede Komponente in der jeweiligen Suite durchführen. Wenn die Anomalieerkennung hinzugefügt wird, können die Berichte umfassendere Antworten enthalten und die Anomaliedaten mit aufnehmen. Als Faustregel gilt: Wenn ein Profil Zugriff auf ein Szenario innerhalb der Adobe Analytics-Oberfläche gewährt, werden mit Entwicklerzugriff auf ein ähnlich definiertes Profil entsprechende API-Aufrufe und -Antworten ermöglicht.
