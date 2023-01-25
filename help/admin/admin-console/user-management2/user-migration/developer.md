---
description: Listet die von der Benutzermigration betroffenen APIs auf
title: Von der Benutzermigration betroffene APIs
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: ht
source-wordcount: '240'
ht-degree: 100%

---

# Von der Benutzermigration betroffene APIs{#apis-affected-by-the-migration}

Adobe migriert alle Analytics-Anmeldeunternehmen weg von [!DNL my.omniture.com] und hin zur Authentifizierung über Adobe Experience Cloud. Sobald ein Unternehmen mit dieser Migration beginnt, wird die programmgemäße Benutzererstellung und -verwaltung durch die Analytics-spezifischen Berechtigungen und `GetLoginKey`-Methoden, die mit den Versionen 1.3 und 1.4 der Analytics Admin-API verfügbar sind, nicht mehr unterstützt. Solche Aktionen sind nun in Experience Cloud über [!DNL adobe.io] möglich.

## Betroffene API-Methoden {#section-d19051ac26cc49aeb124f767c4760254}

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

* [Allgemeines User Management – Start](https://helpx.adobe.com/de/enterprise/help/users.html)
* [User Managements-APIs via adobe.io](https://developer.adobe.com/UMAPI/)
* [User Managements-API-Forum](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Migration des Analytics-Benutzerzugriffs und -managements zur Experience Cloud](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=de)
