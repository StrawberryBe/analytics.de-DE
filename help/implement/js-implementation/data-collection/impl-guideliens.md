---
description: Bei Einhaltung dieser Anleitung werden überall die gleichen Cookie-Domänen verwendet, sodass Besuche auch über verschiedene Typen von Implementierungen hinweg verfolgt werden können.
keywords: Analytics Implementation
title: Richtlinien für die Implementierung
topic: Developer and implementation
uuid: 2917f4af-19bd-4666-ae4b-056e7e33f642
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Richtlinien für die Implementierung

Bei Einhaltung dieser Anleitung werden überall die gleichen Cookie-Domänen verwendet, sodass Besuche auch über verschiedene Typen von Implementierungen hinweg verfolgt werden können.

* **RSID:** Die [!UICONTROL Report Suite-ID]
* **VNS:** (Visitor Name Space) Der Namespace des Besuchers, die Subdomäne von [!DNL 2o7.net] oder [!DNL omtrdc.net], in der das [!UICONTROL Besucher-ID]-Cookie gespeichert wird
* **COOKIEDOMAIN:** Ihr VNS + trackingServer. Je nach Rechenzentrum und RDC-Standort können diese unterschiedlich sein. [Wenden Sie sich an den Kundendienst](https://helpx.adobe.com/contact/enterprise-support.ec.html#analytics) , wenn Sie sich bezüglich Ihrer Datenerfassungsdomäne nicht sicher sind.

## Javascript

```javascript
var s_account="RSID" 
s.visitorNamespace="VNS" 
s.trackingServer="VNS.COOKIEDOMAIN.net" 
```

## AppMeasurement

```javascript
var s_account="RSID" 
s.visitorNamespace="VNS" 
s.trackingServer="VNS.COOKIEDOMAIN.net" 
```

## Fest programmierte Bildanforderung

```javascript
<img border="0" alt="" src="https://VNS.COOKIEDOMAIN.net/b/ss/RSID/5?ns=VNS" width="1" height="1" /> 

<!-- Note that the visitor namespace is defined twice in hardcoded image requests; once in the http subdomain, and another using the ns= query string parameter! -->
```

Bei Implementierungen mit einem Erstanbieter-Cookie kann `VNS.COOKIEDOMAIN.net` durch die verwendete Erstanbieter-Cookie-Domäne ersetzt werden. Wenn Sie beispielsweise Erstanbieter-Cookies in `adobe.com` verwenden, wird dies durch `metrics.adobe.com` (oder Ähnliches) ersetzt.
