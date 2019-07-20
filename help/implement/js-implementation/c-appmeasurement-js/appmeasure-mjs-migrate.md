---
description: In der folgenden Tabelle sind die Schritte aufgelistet, die Sie durchführen müssen, um Ihre Implementierung zu migrieren.
keywords: Analytics-Implementierung; appmeasurement; migrieren; migrieren; javascript
seo-description: In der folgenden Tabelle sind die Schritte aufgelistet, die Sie durchführen müssen, um Ihre Implementierung zu migrieren.
seo-title: Migration zu AppMeasurement for JavaScript
solution: Analytics
subtopic: JavaScript AppMeasurement
title: Migration zu AppMeasurement für JavaScript
topic: Entwickler und Implementierung
uuid: 5 be be 345 a 8-5 a 95-4176-a 2 e 6-97139 b 9 b 46 ce
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Migration zu AppMeasurement für JavaScript

In der folgenden Tabelle sind die Schritte aufgelistet, die Sie durchführen müssen, um Ihre Implementierung zu migrieren.

>[!NOTE]
>
>We recommend migrating to the [Identity Service](../../../implement/js-implementation/c-unique-visitors/visid-service.md#concept_230F8759826E47789EA8DEE08FA09B07) when you migrate to [!DNL AppMeasurement] for JavaScript.

![](assets/step1_icon.png) Überprüfen der Plug-in-Kompatibilität

Wo: s\_ code. js

Einige Plug-ins werden nicht mehr unterstützt. See [AppMeasurement Plug-in Support](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A) .

![](assets/step2_icon.png) Herunterladen der neuen Version von AppMeasurement

Wo: Admin &gt; Code-Manager

Die heruntergeladene ZIP-Datei enthält eine verkleinerte AppMeasurement.js-Datei und JavaScript-Dateien für die Media- und Integrate-Module.

![](assets/step3_icon.png) Kopieren Sie Ihre s\_ code. js-Anpassung in `AppMeasurement.js`.

Wo: s\_ code. js und appmeasurement. js

Move all code that appears before the `DO NOT ALTER ANYTHING BELOW THIS LINE` section in s\_code.js to the beginning of AppMeasurement.js.

![](assets/step4_icon.png) (Optional) Aktualisieren von Plug-ins

Wo: Appmeasurement. js

If you are using the getQueryParam plug-in, update these calls to use the new utility, [Util.getQueryParam](../../../implement/js-implementation/util-getqueryparam.md#concept_763AD2621BB44A3990204BE72D3C9FA5).

![](assets/step5_icon.png) (Optional) Aktualisieren der Media- und Integrate-Module

Wo: Appmeasurement. js

If you are using either of these modules, copy and paste the code from AppMeasurement\_Module\_Media.js and/or AppMeasurement\_Module\_Integrate.js and paste it just before the `DO NOT ALTER ANYTHING BELOW THIS LINE` in AppMeasurement.js.

![](assets/step6_icon.png) Bereitstellen der neuen JavaScript-Datei

Wo: Ihre Website

Die neue JavaScript-Datei können Sie nach Ihrer standardmäßigen Vorgehensweise bereitstellen. Ihr bereits vorhandener Seiten-Code ist mit der neuen Version kompatibel.