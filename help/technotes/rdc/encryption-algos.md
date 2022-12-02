---
title: Unterstützte HTTPS-Verschlüsselungsalgorithmen
description: Am 23. Juni 2022 werden wir die Unterstützung für TLS 1.2-Chiffren entfernen, die SHA1 oder CBC für Kunden verwenden, deren cipher-Sicherheitsstufe auf "Hoch"eingestellt ist.
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: 84a8dc9c6052d34e9dea370e444c83e84bf17852
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 5%

---

# Unterstützte HTTPS-Verschlüsselungsalgorithmen

Adobe bietet zwei Chiffrier-Sicherheitsstufen an, die den unterschiedlichen Sicherheitsanforderungen bei der Erfassung von First-Party-Daten gerecht werden. Diese Ebenen bestimmen, welche Verschlüsselungsalgorithmen für HTTPS-Verbindungen mit unseren Servern unterstützt werden. Kunden verwenden standardmäßig &quot;Standard&quot;, der nur moderne Verschlüsselungsalgorithmen unterstützt. &quot;Hoch&quot;unterstützt eine kleinere Liste von Verschlüsselungsalgorithmen für Kunden, die sich mehr um diese Verbindungen sorgen. Für beide Sicherheitsstufen aktualisiert Adobe regelmäßig den Satz der unterstützten Algorithmen auf der Grundlage aktueller Sicherheitspraktiken. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Sicherheitseinstellungen für die Chiffre ändern möchten.

Am 23. Juni 2022 werden wir die Unterstützung für TLS 1.2-Chiffren entfernen, die SHA1 oder CBC für Kunden verwenden, deren cipher-Sicherheitsstufe auf &quot;Hoch&quot;eingestellt ist.  Diese Änderung wirkt sich auf die sichere Datenerfassung für Endbenutzer auf älteren Betriebssystemen aus.

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

* Windows 8.1 und früher (zuletzt aktualisiert 2018)
* Windows Phone 8.1 und früher (zuletzt aktualisiert 2016)
* OS X 10.10 und früher (letzte Aktualisierung 2017)
* iOS 8.4 und früher (zuletzt aktualisiert 2015)

Android-Geräte sind von dieser Änderung nicht betroffen.

Kunden mit der Sicherheitsstufe &quot;Standard&quot;sind von dieser Änderung nicht betroffen.
