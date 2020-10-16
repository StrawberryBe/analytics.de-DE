---
source-git-commit: 81f351588ef25b0ee0376f471c947391387afb6e
workflow-type: tm+mt
translation-type: tm+mt
source-wordcount: '643'
ht-degree: 72%

---
# Produktprofile in Adobe Analytics

Produktprofile sind eine Berechtigungsvorgabe, die Produktadministratoren Benutzern in einer Organisation zuweisen können. Wenn Sie ein Produktprofil erstellen und diesem Produktprofil einen Experience Cloud-Benutzer zuweisen, übernehmen diese die im Produktprofil enthaltenen Berechtigungselemente.

Allgemeine Informationen zu Produktprofilen finden Sie unter [Verwalten von Produkten und Profilen](https://helpx.adobe.com/de/enterprise/using/manage-products-and-profiles.html) im Enterprise-Benutzerhandbuch.

## Produktprofiladministratoren

Produktprofiladministratoren sind eine optionale Gruppe, die Benutzer zu diesem Produktprofil hinzufügen oder entfernen kann. Beachten Sie, dass ein Produktprofiladministrator nicht mit einem Produktadministrator identisch ist:

* Produktprofiladministratoren haben keinen vollständigen Zugriff auf Adobe Analytics. Der uneingeschränkte Zugriff auf Adobe Analytics ist Produktadministratoren vorbehalten.
* Produktadministratoren können die Berechtigungselemente in ihrem Produkt-Profil anpassen.
* Produktadministratoren können Benutzergruppen Produktgruppen Profil zuweisen oder entfernen.
* Produktadministratoren eignen sich ideal für Teamleiter oder Manager, die Adobe Analytics für ihr Profil zuweisen und verwalten müssen. Für Einzelpersonen ist es nicht erforderlich, dass Systemadministratoren oder Produktadministratoren sich die Mühe geben, Zugriff auf Adobe Analytics zu gewähren.

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

Die Berechtigungselemente der Analytics-Tools gewähren Zugriff auf Funktionen, die unabhängig von den Report Suite-Einstellungen sind. Eine vollständige Liste der Berechtigungselemente und Beschreibungen finden Sie unter [Analytics-Tools](analytics-tools.md).

## Produktprofilentwickler

Entwickler ähneln Benutzern, allerdings können sie die Experience Cloud API auf Adobe I/O verwenden. Weitere Informationen finden Sie unter [Verwalten von Entwicklern](https://helpx.adobe.com/de/enterprise/using/manage-developers.html) im Enterprise-Benutzerhandbuch. Wenn einem Benutzer Entwicklerzugriff für ein beliebiges Profil gewährt wird, kann er auf die Dev-Konsole (console.adobe.io) zugreifen und Adobe Analytics-Integrationen bearbeiten. Die für den Benutzer autorisierten Analytics-API-Aufrufe und -Antworten hängen von den Netzberechtigungen aller Profil ab, auf denen der Benutzer Zugriff auf Entwickler hat.

Beispielsweise könnte ein Entwicklerzugriffsmitglied des Profils mit Profil-Berechtigungen, einschließlich aller Metriken, aller Dimensionen und einer Report Suite, API-Aufrufe für jede Komponente in der jeweiligen Suite durchführen. Wenn die Anomalieerkennung hinzugefügt wird, können die Berichte umfassendere Antworten enthalten und die Anomaliedaten hinzufügen. Wenn ein Profil Zugriff auf ein Szenario innerhalb der Adobe Analytics-Oberfläche gewährt, aktivieren Entwickler-Zugriff auf ein ähnlich definiertes Profil im Prinzip entsprechende API-Aufrufe und -Antworten.
