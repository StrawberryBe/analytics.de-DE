---
description: 'null'
seo-description: 'null'
seo-title: Von der Migration betroffene APIs
title: Von der Migration betroffene APIs
uuid: 9a5d43be-e146-476b-961e-49ea0a30b500
translation-type: tm+mt
source-git-commit: 56d27762320a752dff6ab4d9d763bbbf6e0deff5

---


# Von der Migration betroffene APIs{#apis-affected-by-the-migration}

## Von der Migration betroffene APIs {#topic-8d34296a67d74b1081c3f7e8f650f3ce}

Adobe migriert alle Analytics-Login-Unternehmen weg von [!DNL my.omniture.com] und hin zur Authentifizierung über die Adobe Experience Cloud. Once a company begins this migration, programmatic user creation and management through the Analytics-specific permissions and `GetLoginKey` methods available via v1.3 and v1.4 of the Analytics Admin API will no longer be supported. Solche Aktionen sind nun in der Experience Cloud über [!DNL adobe.io] möglich.

## Betroffenen API-Methoden {#section-d19051ac26cc49aeb124f767c4760254}

Die folgenden API-Methoden in den Versionen v1.3 und v1.4 der Admin-API werden nach Beginn der Benutzermigration nicht mehr unterstützt:

* Company.GetLoginKey
* Permissions.AddLogin
* Permissions.Authenticate
* Permissions.DeleteGroup
* Permissions.DeleteLogin
* Permissions.GetGroup
* Permissions.GetGroups
* Permissions.GetLogin
* Permissions.GetLogins
* Permissions.GetReportSuiteGroups
* Permissions.RemoveLoginSegment
* Permissions.SaveGroup
* Permissions.SaveLogin
* Permissions.GetLoginSegment

## Maßnahmen, die Sie ergreifen können {#section-8b0b89a862614f729ebdbe092ce99027}

Sollte Ihr Unternehmen diese Methoden derzeit verwenden, erhalten Sie nach dem 31. März 2018 eine Migrationsbenachrichtigung. Die Benachrichtigung erfolgt mindestens 30 Tage vor Beginn der Migration Ihres Unternehmens auf die Experience Cloud-Authentifizierung. Ab diesem Zeitpunkt werden diese Methoden nicht mehr unterstützt.

Wenn Ihr Unternehmen keine dieser Methoden verwendet, ist keine weitere Aktion erforderlich, außer sicherzustellen, dass Sie diese Methoden nicht verwenden.

Weitere Informationen:

* [Allgemeines User Management – Start](https://helpx.adobe.com/enterprise/help/users.html)
* [User Managements-APIs via adobe.io](https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html)
* [User Managements-API-Forum](https://forums.adobe.com/community/umapi/overview)
* [Migration des Analytics-Benutzerzugriffs und -managements zur Experience Cloud](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/)

