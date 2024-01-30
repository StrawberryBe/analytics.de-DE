---
title: Von Adobe Analytics verwendete IPs und Domains
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
feature: Data Configuration and Collection
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
source-git-commit: e4f8467e9c2e3f461857b4ea3d4e5cbe643d57a0
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 67%

---

# Von Adobe Analytics verwendete IPs und Domains

Einige Firewall-Konfigurationen blockieren IP-Adressen, die von den Adobe-Datenerfassungs-Servern oder -Servern stammen, die für den Datenzugriff zuständig sind. Sie können diese Bereichsliste verwenden, um die Firewall-Einstellungen Ihres Unternehmens zu ändern und den Zugriff auf und das Senden von Daten aus Ihrem Unternehmen zu ermöglichen. Diese Seite enthält sowohl eingehende Systeme (z. B. Datenerfassung) als auch ausgehende Systeme (z. B. Daten-Feeds), die von Adobe verwendet werden.

>[!IMPORTANT]
>
>Adobe versucht zwar nach besten Kräften, dieses Dokument aktuell zu halten, kann aber nicht garantieren, dass die Liste der IP-Bereiche unverändert bleibt. Zu den möglichen Änderungen gehören Wachstum und Erweiterung des Unternehmens, eine Internet-Registrierung erfordert Änderungen am IP-Adressraum von Adobe, oder ein Internet-Dienstleister funktioniert nicht mehr.

## Abhängige Technologiedomänen zulassen

Adobe Analytics verwendet die folgenden Hosts, um die Leistung und das Produkterlebnis zu verbessern. Adobe empfiehlt, diese Domänen über die Firewall Ihres Unternehmens zuzulassen, damit eine optimale Nutzung von Adobe Analytics gewährleistet ist.

| Technologie | Domain |
| --- | --- |
| Adobe Analytics-Domains | `adobe.com`, `adobe.net`, `adobe.io` |
| Veraltete Adobe Analytics-Domäne | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Gainsight | `esp.aptrinsic.com`, `esp-m.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob Storage | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

## Alle Adobe Analytics-IP-Adressblöcke

Die folgende Tabelle enthält alle für Adobe Analytics verwendeten Adobe-eigenen IP-Adressen. Sie umfassen nicht alle Dienste, die in öffentlichen Clouds gehostet werden.

| IP-Block (CIDR-Notation) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `185.34.188.0/22` |

## Datenerfassungs- und FTP-IP-Adressblöcke

Wenn Ihr Unternehmen es vorzieht, bestimmte IP-Adressbereiche zuzulassen, können Sie die folgende Tabelle verwenden. Alle Bereiche in diesem Abschnitt sind in der obigen Tabelle enthalten. FTP-Verbindungen für Data Warehouse- und Daten-Feeds stammen nur von den Standorten London, Oregon und Singapur.

| Standort | IP-Bereich (CIDR-Notation) |
| --- | --- |
| Australien | `63.140.55.0/24` |
| Australien | `63.140.56.0/23` |
| Kalifornien | `63.140.32.0/23` |
| Kalifornien | `63.140.34.0/24` |
| Frankreich | `63.140.62.0/23` |
| Indien | `66.117.20.0/24` |
| Indien | `66.117.22.0/23` |
| Japan | `130.248.169.0/23` |
| Japan | `63.140.50.0/23` |
| Japan | `66.117.31.0/24` |
| London | `66.235.156.0/24` |
| London | `185.34.188.0/22` |
| London | `130.248.152.0/22` |
| London | `130.248.244.0/23` |
| Oregon | `66.235.132.0/22` |
| Oregon | `130.248.130.0/23` |
| Oregon | `130.248.150.0/24` |
| Oregon | `130.248.160.0/21` |
| Oregon | `192.243.242.0/24` |
| Singapur | `130.248.170.0/23` |
| Singapur | `130.248.240.0/24` |
| Singapur | `63.140.44.0/22` |
| Singapur | `63.140.48.0/23` |
| Singapur | `66.117.30.0/24` |
| Virginia | `63.140.38.0/23` |
| Virginia | `63.140.54.0/24` |

## AWS-Hosts

Adobe Analytics verwendet Amazon Web Services als Teil des Datenerfassungsprozesses. Die folgende Tabelle enthält AWS IPv4-Hostadressen, die für Adobe reserviert sind. Diese Hosts sind **nicht** im obigen aggregierten Blockbereich enthalten.

| Standort | Host |
| --- | --- |
| China | `52.80.168.159` |
| China | `52.80.199.104` |
| China | `54.223.199.8` |

Die folgende Tabelle enthält IPv6-Adressblöcke von AWS, die von Adobe verwendet werden. Diese Hosts sind **nicht** im obigen aggregierten Blockbereich enthalten.

| Standort | Host |
| --- | --- |
| Australien | `2406:da1c:406:1a00::/56` |
| Australien | `2406:da1c:ce5:b400::/56` |
| Kalifornien | `2600:1f1c:366:d900::/56` |
| Frankreich | `2a05:d012:706:d000::/56` |
| Indien | `2406:da1a:f34:6a00::/56` |
| Irland | `2a05:d018:309:600::/56` |
| Japan | `2406:da14:b07:ab00::/56` |
| Oregon | `2600:1f14:1eb:7d00::/56` |
| Oregon | `2600:1f14:9d3:2b00::/56` |
| Singapur | `2406:da18:6e8:1e00::/56` |
| Virginia | `2600:1f18:1a20:e800::/56` |
| Virginia | `2600:1f18:4fd:6000::/56` |
| Virginia | `2600:1f18:b00:e100::/56` |
| Virginia | `2600:1f18:d1f:bd00::/56` |
