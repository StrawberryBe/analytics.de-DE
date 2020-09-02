---
source-git-commit: f20e0547c00f185659a2eabe0110f43c56c30114
workflow-type: tm+mt
translation-type: tm+mt
source-wordcount: '514'
ht-degree: 91%

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

Entwickler ähneln Benutzern, allerdings können sie die Experience Cloud API auf Adobe I/O verwenden. Weitere Informationen finden Sie unter [Verwalten von Entwicklern](https://helpx.adobe.com/de/enterprise/using/manage-developers.html) im Enterprise-Benutzerhandbuch.
