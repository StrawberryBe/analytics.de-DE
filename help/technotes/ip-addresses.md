---
title: Von Adobe Analytics verwendete IPs und Domänen
description: Wenn die Firewall Ihres Unternehmens IP-Adressen blockiert, die von der Adobe stammen, verwenden Sie diese Liste, um Ihre Firewall-Einstellungen zu aktualisieren.
exl-id: e24a70e4-9ed4-4b87-8bab-4ed0aebedd1f
translation-type: tm+mt
source-git-commit: 8986b30ca08224e2b992e8ed238e74e40e9a7b41
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 86%

---

# Von Adobe Analytics verwendete IPs und Domänen

Einige Firewall-Konfigurationen blockieren IP-Adressen, die von Adobes Datenerfassungs-Servern oder Servern stammen, die für den Datenzugriff zuständig sind. Sie können diese Liste von Bereichen verwenden, um die Firewall-Einstellungen Ihres Unternehmens so zu ändern, dass der Zugriff und das Senden von Daten aus Ihrem Unternehmen heraus möglich ist.

>[!IMPORTANT]
>
>Adobe bemüht sich nach besten Kräften, dieses Dokument aktuell zu halten, kann jedoch nicht garantieren, dass die Liste der IP-Bereiche unverändert bleibt. Zu den möglichen Änderungen gehören Wachstum und Erweiterung des Unternehmens, eine Internet-Registrierung erfordert Änderungen am IP-Adressraum von Adobe, oder ein Internet-Dienstleister funktioniert nicht mehr.

## Abhängige Technologiedomänen zulassen

Adobe Analytics verwendet die folgenden Hosts, um die Leistung und das Produkterlebnis zu verbessern. Adobe empfiehlt, diese Domänen zur Zulassungsliste Ihrer Firewall hinzuzufügen, um eine optimale Nutzung von Adobe Analytics zu gewährleisten.

| Technologie | Domäne |
| --- | --- |
| Adobe Analytics-Domänen | `adobe.com`, `adobe.net`, `adobe.io` |
| Veraltete Adobe Analytics-Domäne | `omniture.com` |
| Amazon AWS | `aaui-879784980514.s3.us-east-2.amazonaws.com` |
| Amazon CloudFront | `d30ln29764hddd.cloudfront.net` |
| Gainsight | `esp.aptrinsic.com` |
| LaunchDarkly | `app.launchdarkly.com` |
| Microsoft Azure Blob Storage | `awaascicdprodva7.blob.core.windows.net` |
| Microsoft Azure CDN | `aauicdnva7.azureedge.net` |

## Alle IP-Adressblöcke der Adobe Analytics-Datenerfassung

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

Wenn Ihr Unternehmen es vorzieht, bestimmte IP-Adressbereiche zuzulassen, können Sie die folgende Tabelle verwenden. Alle Bereiche in diesem Abschnitt sind in der obigen Tabelle enthalten.

| Standort | IP-Bereich (CIDR-Notation) |
| --- | --- |
| Amsterdam | `66.117.28.0/23` |
| Dallas | `205.219.231.0/24` |
| Dallas | `66.235.152.0/22` |
| Dallas | `66.235.140.0/22` |
| Dallas | `63.140.32.0/21` |
| Dallas | `172.82.208.0/22` |
| Sonderverwaltungsregion Hongkong der Volksrepublik China | `66.117.24.0/22` |
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

Adobe Analytics verwendet Amazon Web Services als Teil des Datenerfassungsprozesses. Die folgende Tabelle enthält AWS-Hosts, die für Adobe reserviert sind. Diese Hosts sind **nicht** im obigen aggregierten Blockbereich enthalten.

| Standort | Host |
| --- | --- |
| Australien | `13.238.77.77` |
| Australien | `52.62.21.192` |
| Australien | `54.66.152.159` |
| China | `52.81.111.133` |
| China | `140.179.22.22` |
| Frankreich | `15.237.76.117` |
| Frankreich | `15.237.136.106` |
| Frankreich | `35.181.18.61` |
| Indien | `65.0.114.116` |
| Indien | `65.0.115.179` |
| Indien | `65.0.25.111` |
| Irland | `18.202.158.78` |
| Irland | `54.72.205.114` |
| Irland | `54.78.36.71` |
| Oregon | `44.233.255.254` |
| Oregon | `44.237.54.118` |
| Oregon | `44.238.157.95` |
| Singapur | `52.220.116.94` |
| Singapur | `52.76.68.91` |
| Singapur | `54.179.114.68` |
| Tokio | `18.182.161.178` |
| Tokio | `54.168.58.167` |
| Tokio | `54.178.61.109` |
| Virginia | `3.213.168.181` |
| Virginia | `3.219.249.186` |
| Virginia | `3.220.129.153` |
| Virginia | `18.206.109.10` |
| Virginia | `18.211.197.67` |
| Virginia | `34.227.41.189` |
| Virginia | `34.228.124.176` |
| Virginia | `54.90.190.103` |
| Virginia | `54.174.149.161` |
