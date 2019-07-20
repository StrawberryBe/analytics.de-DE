---
source-git-commit: d8f2458e7bae596dbabc8dab33ea5d2881047566
translation-type: tm+mt

---
# Produktprofile in Adobe Analytics

Produktprofile sind eine Berechtigungsvorgabe, die Produktadministratoren Benutzern innerhalb einer Organisation zuweisen können. Wenn Sie ein Produktprofil erstellen und diesem Produktprofil einen Experience Cloud-Benutzer zuweisen, übernehmen sie die im Produktprofil enthaltenen Berechtigungselemente.

See [Manage products and profiles](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) in the Enterprise user guide for general information on product profiles.

## Produktprofiladministratoren

Produktprofiladministratoren sind eine optionale Gruppe, die Benutzer diesem Produktprofil hinzufügen oder entfernen kann. Beachten Sie, dass ein Produktprofil-Administrator nicht mit einem Produkt-Admin identisch ist:

* Produktprofiladministratoren sind nur für die Benutzerliste eines Produktprofils verantwortlich.
* Produktprofiladministratoren haben keinen vollständigen Zugriff auf Adobe Analytics. Kompletter Zugriff auf Adobe Analytics ist für Produktadministratoren reserviert.
* Produktprofiladministratoren können Berechtigungselemente in ihrem Produktprofil nicht anpassen; Ein Produktadministrator muss Berechtigungsanpassungen vornehmen.
* Produktprofiladministratoren sind ideal für Team-Interessenten oder -manager, die einfach den Zugriff auf Adobe Analytics für ihr Team erteilen und verwalten müssen. Personen müssen Systemadministratoren oder Produktadministratoren nicht zur Verfügung stellen, um Zugriff auf Adobe Analytics zu gewähren.

## Berechtigungselemente von Adobe Analytics

Für den Zugriff auf Adobe Analytics sind die erforderlichen Berechtigungen in einem Produktprofil erforderlich:

* Das Produktprofil muss Zugriff auf mindestens eine Report Suite haben.
* The product profile must belong to the Analytics Tools permission item **Analysis Workspace Access** (or **Reports &amp; Analytics Access**)

### Report Suites

Gewährt Zugriff auf Report Suites, die zu Ihrer Analytics-Organisation gehören. Ein Benutzer muss mindestens einer Report Suite angehören, um Zugriff auf Adobe Analytics zu erhalten.

### Metriken

Gewährt Zugriff auf Metriken in Ihrer Report Suite. Metriken werden als ihre jeweilige Komponente im Analysis Workspace aufgeführt oder wenn die Metrik in Reports &amp; Analysen verfügbar ist, verfügbar als Menüelement unter Site-Metriken.

Benutzerspezifische Metriken sind mit "Benutzerdefiniertes Ereignis 1-1000" gekennzeichnet, um sie von Report Suites unabhängig zu halten. Wenn es sich bei "Benutzerspezifisches Ereignis 1" um ein aktiviertes Berechtigungselement handelt, hat dieser Benutzer Zugriff auf event 1 in allen Report Suites des Produktprofils.

### Dimensionen

Gewährt Zugriff auf Dimensionen in Ihrer Report Suite. Dimensionen werden als ihre jeweilige Komponente im Analysis Workspace oder, falls die Dimension in Reports &amp; Analysen verfügbar ist, als Menüelement aufgeführt.

Benutzerdefinierte Variablen wie evars sind mit "Benutzerspez. Umrechnung 1-250" beschriftet, um sie von Report Suites unabhängig zu halten. Wenn es sich bei "Custom Conversion 1" um ein aktiviertes Berechtigungselement handelt, hat dieser Benutzer Zugriff auf evar 1 in allen Report Suites des Produktprofils.

### Report Suite-Tools

Die Berechtigungselemente der Report Suite-Tools gewähren Zugriff auf Funktionen, die für die Report Suites gelten, auf die der Benutzer Zugriff hat. See [Report Suite Tools](report-suite-tools.md) for a full list of permission items and descriptions.

### Analytics-Tools

Berechtigungselemente von Analytics-Tools gewähren Zugriff auf Funktionen, die unabhängig von den Report Suite-Einstellungen sind. See [Analytics Tools](analytics-tools.md) for a full list of permission items and descriptions.

## Entwickler von Produktprofilen

Developers are similar to users, except they are granted the ability to use the Experience Cloud API on Adobe I/O. See [Manage Developers](https://helpx.adobe.com/enterprise/using/manage-developers.html) in the Enterprise user guide for more information.
