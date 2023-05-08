---
title: Unterstützte HTTPS-Verschlüsselungsalgorithmen
description: TLS bietet Sicherheitseinstellungen und Zertifikatstypen.
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: 1ca7f750387fd9ae034d10ebf3e47190cf33d4b7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 25%

---

# Unterstützte HTTPS-Verschlüsselungsalgorithmen

## Cipher Security Levels

Adobe bietet zwei Chiffrier-Sicherheitsstufen an, die den unterschiedlichen Sicherheitsanforderungen bei der Erfassung von First-Party-Daten gerecht werden. Diese Ebenen bestimmen, welche Verschlüsselungsalgorithmen für HTTPS-Verbindungen mit Adobe-Servern unterstützt werden. Adobe überprüft und aktualisiert regelmäßig den Satz unterstützter Algorithmen auf der Grundlage aktueller Sicherheitspraktiken. Wenden Sie sich an die Kundenunterstützung, wenn Sie die Sicherheitseinstellungen für die Chiffre ändern möchten.

&quot;Standard&quot;erfordert TLS 1.2 oder höher und mindestens 128-Bit-Verschlüsselung. Es wurde entwickelt, um die größtmögliche Gerätekompatibilität zu gewährleisten und gleichzeitig eine sichere Verschlüsselung zu gewährleisten.

Die Sicherheitsstufe &quot;Hoch&quot;erfordert TLS 1.2 oder höher und entfernt die Unterstützung für schwächere Chiffren. Es wurde für Kunden entwickelt, die die strengste Verschlüsselung wünschen und sich nicht um die Unterstützung älterer Geräte sorgen.

Die folgenden Clients sind bekanntermaßen nicht in der Lage, eine Verbindung mit der cipher-Sicherheit herzustellen, die auf &quot;Hoch&quot;gesetzt ist.

* Windows 8.1 und niedriger (zuletzt aktualisiert 2018)
* Windows Phone 8.1 und niedriger (zuletzt aktualisiert 2016)
* OS X 10.10 und niedriger (letzte Aktualisierung 2017)
* iOS 8.4 und niedriger (zuletzt aktualisiert 2015)

## Unterstützte HTTPS-Zertifikatstypen

Adobe unterstützt sowohl RSA- als auch ECC-Zertifikatstypen, um unterschiedlichen Kundenanforderungen gerecht zu werden. RSA-Zertifikate werden für Clients häufiger unterstützt, ECC-Zertifikate verwenden jedoch weniger Verarbeitung auf Server- und Client-Seite. Für von Adobe verwaltete Zertifikate werden sowohl RSA als auch ECC bereitgestellt. Für kundenverwaltete Zertifikate werden sowohl RSA als auch ECC empfohlen. Moderne Kunden unterstützen RSA und ECC. Die folgenden Clients unterstützen bekanntermaßen nur RSA-Zertifikate:

* Windows Vista und früher (zuletzt aktualisiert 2012)
* Windows Phone 8.0 und niedriger (zuletzt aktualisiert 2014)
* OS X 10.8 und niedriger (letzte Aktualisierung 2013)
* iOS 5.1 und niedriger (zuletzt aktualisiert 2012)
* Android 4.3 und früher (zuletzt aktualisiert 2013)
