---
description: In der folgenden Tabelle sind die Schritte aufgelistet, die Sie durchführen müssen, um Ihre Implementierung zu migrieren.
keywords: Analytics Implementation;appmeasurement;migrate;migrating;javascript
subtopic: JavaScript AppMeasurement
title: Migration zu AppMeasurement für JavaScript
topic: Developer and implementation
uuid: 5be345a8-5a95-4176-a2e6-97139b9b46ce
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Migration zu AppMeasurement für JavaScript

In der folgenden Tabelle sind die Schritte aufgelistet, die Sie durchführen müssen, um Ihre Implementierung zu migrieren.

>[!NOTE]
>
>Wir empfehlen die Migration zum [Identitätsdienst](/help/implement/js-implementation/c-unique-visitors/visid-service.md), wenn Sie zu [!DNL AppMeasurement] für JavaScript migrieren.

![](assets/step1_icon.png) Überprüfen der Plug-in-Kompatibilität

Dabei gilt: s\_code.js

Einige Plug-ins werden nicht mehr unterstützt. Siehe [AppMeasurement-Plug-in-Unterstützung](/help/implement/js-implementation/c-appmeasurement-js/plugins-support.md).

![](assets/step2_icon.png) Herunterladen der neuen Version von AppMeasurement

Wo: Admin &gt; Code-Manager

Die heruntergeladene ZIP-Datei enthält eine verkleinerte AppMeasurement.js-Datei und JavaScript-Dateien für die Media- und Integrate-Module.

![](assets/step3_icon.png) Kopieren Sie Ihre s\_code.js-Anpassungen nach `AppMeasurement.js`.

Wo: s\_code.js und AppMeasurement.js

Verschieben Sie sämtlichen Code, der vor dem Abschnitt `DO NOT ALTER ANYTHING BELOW THIS LINE` in s\_code.js steht, an den Anfang von AppMeasurement.js.

![](assets/step4_icon.png) (Optional) Aktualisieren von Plug-ins

Wo: AppMeasurement.js

Wenn Sie das getQueryParam-Plug-in verwenden, aktualisieren Sie diese Aufrufe zwecks Verwendung des neuen Hilfsprogramms [Util.get.QueryParam](/help/implement/js-implementation/util-getqueryparam.md)

![](assets/step5_icon.png) (Optional) Aktualisieren der Media- und Integrate-Module

Wo: AppMeasurement.js

Wenn Sie eines dieser beiden Module verwenden, kopieren Sie den Code aus AppMeasurement\_Module\_Media.js und/oder AppMeasurement\_Module\_Integrate.js und fügen Sie ihn unmittelbar vor `DO NOT ALTER ANYTHING BELOW THIS LINE` in AppMeasurement.js ein.

![](assets/step6_icon.png) Bereitstellen der neuen JavaScript-Datei

Wo: Ihre Website

Die neue JavaScript-Datei können Sie nach Ihrer standardmäßigen Vorgehensweise bereitstellen. Ihr bereits vorhandener Seiten-Code ist mit der neuen Version kompatibel.
