---
title: SSL-Zertifikatslizenzierung
seo-title: SSL-Zertifikatslizenzierung von Adobe Analytics
description: null
seo-description: null
translation-type: tm+mt
source-git-commit: 1fdd14497171dbf5850ec1b1d873a06931d58435

---


# SSL-Zertifikatslizenzierung

Wenn Sie Erstanbieter-Cookies verwenden und sicheren Traffic messen, müssen Sie ausreichende SSL-Zertifikatslizenzen bereitstellen, um die RDC-Implementierung zu unterstützen.

Ihre SSL-Zertifikatslizenzen müssen die Installation auf bis zu 10 Servern unterstützen. Diese Zertifikate werden auf Load Balancern auf der ganzen Welt installiert. Wenn Adobe weitere Datenerfassungscenter online stellt, muss das SSL-Zertifikat geändert werden. Inwiefern sich dies mit der Zeit auf Ihre Zertifikatslizenzierungsanforderungen auswirkt, hängt vom Typ Ihrer Zertifikatslizenz ab:

* Serverbasierte Lizenzen: Lizenzanforderungen für RDC-Implementierungen wachsen mit der Zeit.
* Volumenbasierte Lizenzen: Lizenzanforderungen sind nicht von Änderungen der Infrastruktur betroffen, sondern nur von Änderungen im Traffic-Volumen.
* Unbegrenzte Lizenzen: Lizenzanforderungen sollten relativ stabil bleiben.

Bei Bereitstellung Ihres eigenen Zertifikats sind Sie dafür verantwortlich, diese SSL-Zertifikate zu kaufen und zu verwalten. Überprüfen Sie im Vertrag des Zertifikatanbieters, ob SSL-Zertifikate in mehreren Rechenzentren installiert werden können.

Alternativ dazu kann Adobe Ihr Zertifikat ohne zusätzliche Kosten über das [Adobe Managed Certificate-Programm](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html) verwalten.
