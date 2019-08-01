---
description: 'null '
seo-description: 'null '
seo-title: Von der Migration betroffene APIs
title: Von der Migration betroffene APIs
uuid: 9 a 5 d 43 be-e 146-476 b -961 e -49 ea 0 a 30 b 500
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2fcd72e6c61f8004268e583b934e9cf474e5e44f

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

