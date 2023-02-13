---
title: Unterstützte HTTPS-Verschlüsselungsalgorithmen
description: Ab 23. Juni 2022 werden keine TLS 1.2-Chiffren mehr unterstützt, die SHA1 oder CBC für Kunden verwenden, deren Chiffrier-Sicherheitsstufe auf „Hoch“ eingestellt ist.
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: 84a8dc9c6052d34e9dea370e444c83e84bf17852
workflow-type: ht
source-wordcount: '285'
ht-degree: 100%

---

# Unterstützte HTTPS-Verschlüsselungsalgorithmen

Adobe bietet zwei Chiffrier-Sicherheitsstufen an, die den unterschiedlichen Sicherheitsanforderungen bei der Erfassung von First-Party-Daten gerecht werden. Diese Stufen bestimmen, welche Verschlüsselungsalgorithmen bei HTTPS-Verbindungen mit unseren Servern unterstützt werden. Die Standardeinstellung „Standard“ unterstützt nur moderne Verschlüsselungsalgorithmen. Die Einstellung „Hoch“ unterstützt eine kleinere Gruppe von Verschlüsselungsalgorithmen für Kunden, die mehr Sicherheit in Bezug auf diese Verbindungen wünschen. Für beide Sicherheitsstufen aktualisiert Adobe regelmäßig die unterstützten Algorithmen auf der Grundlage aktueller Sicherheitspraktiken. Wenden Sie sich an die Kundenunterstützung, wenn Sie Ihre Chiffrier-Sicherheitseinstellungen ändern möchten.

Ab 23. Juni 2022 werden keine TLS 1.2-Chiffren mehr unterstützt, die SHA1 oder CBC für Kunden verwenden, deren Chiffrier-Sicherheitsstufe auf „Hoch“ eingestellt ist. Diese Änderung wirkt sich auf die sichere Datenerfassung von Endbenutzern und Endbenutzerinnen auf älteren Betriebssystemen aus.

Die folgenden TLS 1.2-Chiffren werden nicht mehr unterstützt:

* TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
* TLS_RSA_WITH_AES_128_CBC_SHA
* TLS_RSA_WITH_AES_256_CBC_SHA
* TLS_RSA_WITH_AES_128_GCM_SHA256
* TLS_RSA_WITH_AES_256_GCM_SHA384

Die folgenden Clients sind von dieser Änderung bekanntermaßen betroffen, da sie die aktuellen Verschlüsselungsstandards nicht unterstützen:

* Windows 8.1 und niedriger (zuletzt aktualisiert 2018)
* Windows Phone 8.1 und niedriger (zuletzt aktualisiert 2016)
* OS X 10.10 und niedriger (letzte Aktualisierung 2017)
* iOS 8.4 und niedriger (zuletzt aktualisiert 2015)

Android-Geräte sind von dieser Änderung nicht betroffen.

Auch Kunden mit der Sicherheitsstufe „Standard“ sind von dieser Änderung nicht betroffen.
