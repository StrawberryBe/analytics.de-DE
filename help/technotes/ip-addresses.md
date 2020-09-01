---
title: Von Adobe Analytics verwendete IPs und Domänen
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von der Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
translation-type: tm+mt
source-git-commit: 4faa557120f937eb240e6d12ab0e2fc0ae7372ab
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 16%

---


# Von Adobe Analytics verwendete IPs und Domänen

Einige Firewall-Konfigurationen blockieren IP-Adressen, die von Datenerfassungsservern der Adobe oder von Servern stammen, die für den Zugriff auf Daten zuständig sind. Sie können diese Liste von Bereichen verwenden, um die Firewall-Einstellungen Ihres Unternehmens zu ändern, um den Zugriff zu ermöglichen und Daten aus Ihrem Unternehmen zu senden.

>[!IMPORTANT]
>
>Während Adobe ihr Bestes tut, um dieses Dokument aktuell zu halten, kann sie nicht garantieren, dass die Liste der IP-Bereiche gleich bleibt. Mögliche Änderungen beinhalten das Geschäftswachstum und die Geschäftsausweitung, eine Internetregistrierung erfordert Änderungen am IP-Adressenraum der Adobe, oder ein Dienstleister funktioniert nicht mehr.

## Abhängige Technologiedomänen zulassen

Adobe Analytics verwendet die folgenden Hosts, um die Leistung und das Produkterlebnis zu verbessern. Adobe empfiehlt, diese Domänen zur Zulassungsliste Ihrer Firewall hinzuzufügen, um eine optimale Nutzung von Adobe Analytics zu ermöglichen.

| Technologie | Domäne |
| --- | --- |
| Adobe Analytics-Domäne | `adobe.com` |
| Adobe Analytics-Domäne | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Gainsight | `esp.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azurblase-Datenspeicherung | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Agar CDN | `aauicdnva7.azureedge.net` |

## Alle IP-Adressblöcke von Adobe Analytics

Die folgende Tabelle enthält alle Standarddatenerfassungsserver und regionalen Datenerfassungsserver für Adobe Analytics. Sie enthalten keine einzelnen AWS-Hosts.

| IP-Block (CIDR-Notation) |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.224.0/19` |
| `205.219.231.0/24` |
| `208.67.40.0/22` |
| `208.77.136.0/22` |

## Datenerfassungs- und FTP-IP-Adressblöcke

Wenn Ihr Unternehmen bestimmte IP-Adressbereiche bevorzugt, können Sie die folgende Tabelle verwenden. Alle Bereiche in diesem Abschnitt sind in der obigen Tabelle enthalten.

| Standort | IP-Bereich (CIDR-Notation) |
| --- | --- |
| Amsterdam | `66.117.28.0/23` |
| Dallas | `205.219.231.0/24` |
| Dallas | `66.235.152.0/22` |
| Dallas | `66.235.140.0/22` |
| Dallas | `63.140.32.0/21` |
| Dallas | `172.82.208.0/22` |
| Hongkong SAR China | `66.117.24.0/22` |
| London | `66.235.156.0/24` |
| London | `66.235.148.0/23` |
| London | `63.140.40.0/22` |
| London | `208.67.41.0/24` |
| London | `192.243.254.0/23` |
| London | `192.243.244.0/22` |
| London | `185.34.188.0/23` |
| London | `130.248.152.0/21` |
| London | `172.82.224.0/21` |
| London | `172.82.232.0/21` |
| Oregon | `192.243.240.0/22` |
| Oregon | `192.243.232.0/21` |
| Oregon | `192.243.224.0/21` |
| Oregon | `130.248.160.0/21` |
| Oregon | `130.248.148.0/22` |
| Oregon | `172.82.192.0/21` |
| Oregon | `172.82.216.0/21` |
| Paris | `208.67.40.0/24` |
| Singapur | `66.235.150.0/24` |
| Singapur | `66.235.130.0/23` |
| Singapur | `63.140.44.0/22` |
| Singapur | `208.67.43.0/24` |
| Singapur | `172.82.240.0/22` |
| Singapur | `172.82.246.0/23` |
| Singapur | `172.82.248.0/21` |
| San Jose | `66.117.20.0/24` |
| San Jose | `66.235.132.0/22` |
| San Jose | `130.248.128.0/22` |
| San Jose | `192.243.248.0/23` |
| San Jose | `172.82.200.0/22` |
| San Jose | `66.235.136.0/22` |
| San Jose | `208.91.175.0/24` |
| San Jose | `208.91.174.0/24` |
| San Jose | `208.91.169.0/24` |
| Sydney | `216.104.216.0/23` |
| Tokio | `66.235.159.0/24` |
| Tokio | `66.117.21.0/24` |
| Tokio | `63.140.52.0/24` |
| Tokio | `63.140.50.0/23` |
| Virginia | `66.235.144.0/22` |
| Virginia | `208.77.138.0/23` |
| Virginia | `208.77.136.0/23` |
| Virginia | `192.243.250.0/23` |
| Virginia | `130.248.144.0/22` |
| Virginia | `172.82.204.0/22` |
| Virginia | `172.82.212.0/22` |
| Virginia | Siehe AWS-Hosts |

## AWS-Hosts

Adobe Analytics verwendet Amazon Web Services als Teil des Datenerfassungsprozesses. Die folgende Tabelle enthält AWS-Hosts, die für die Adobe reserviert sind. Diese Hosts werden **nicht** im obigen Aggregat-Blockbereich enthalten.

| Standort | Host |
| --- | --- |
| Australien | `13.238.77.77` |
| Australien | `52.62.21.192` |
| Australien | `54.66.152.159` |
| Frankreich | `15.188.154.177` |
| Frankreich | `15.236.175.233` |
| Frankreich | `15.236.9.100` |
| Indien | `13.232.177.101` |
| Indien | `13.235.4.163` |
| Indien | `3.6.119.69` |
| Irland | `52.17.94.37` |
| Irland | `52.49.253.16` |
| Irland | `52.51.63.15` |
| London | `172.82.228.19` |
| Oregon | `52.42.60.49` |
| Oregon | `54.212.169.56` |
| Oregon | `54.214.170.191` |
| Singapur | `13.228.34.224` |
| Singapur | `18.136.20.161` |
| Singapur | `52.74.162.152` |
| Tokio | `13.112.72.86` |
| Tokio | `18.178.74.225` |
| Tokio | `18.179.88.228` |
| Virginia | `34.234.106.101` |
| Virginia | `52.22.231.198` |
| Virginia | `54.157.65.136` |
| Virginia | `107.23.142.4` |
| Virginia | `34.192.14.184` |
| Virginia | `34.192.146.173` |
| Virginia | `34.192.229.76` |
| Virginia | `34.196.183.216` |
| Virginia | `34.196.219.120` |
| Virginia | `34.196.54.55` |
| Virginia | `34.197.179.21` |
| Virginia | `34.197.45.49` |
| Virginia | `34.197.93.163` |
| Virginia | `34.198.80.27` |
| Virginia | `34.199.102.192` |
| Virginia | `34.199.46.40` |
| Virginia | `34.199.99.62` |
| Virginia | `34.200.67.35` |
| Virginia | `34.204.146.235` |
| Virginia | `34.204.164.1` |
| Virginia | `34.204.27.249` |
| Virginia | `34.205.224.111` |
| Virginia | `34.206.69.71` |
| Virginia | `52.193.88.44` |
| Virginia | `52.200.108.250` |
| Virginia | `52.200.171.156` |
| Virginia | `52.201.49.195` |
| Virginia | `52.205.244.105` |
| Virginia | `52.207.161.156` |
| Virginia | `52.22.148.55` |
| Virginia | `52.4.155.255` |
| Virginia | `52.72.182.205` |
| Virginia | `52.72.185.111` |
| Virginia | `54.152.218.194` |
| Virginia | `54.173.37.66` |
| Virginia | `54.173.69.38` |
| Virginia | `54.236.180.248` |
| Virginia | `54.236.71.218` |
| Virginia | `54.80.103.29` |
| Virginia | `54.88.180.124` |
