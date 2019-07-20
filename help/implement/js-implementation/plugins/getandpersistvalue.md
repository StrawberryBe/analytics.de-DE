---
description: Das getAndPersistValue-Plug-in ruft einen Wert Ihrer Wahl ab und trägt ihn für einen bestimmten Zeitraum in eine Analytics-Variable ein. Normalerweise wird es genutzt, um zu sehen, wie viele Seitenaufrufe eine Kampagne nach einem Clickthrough generiert. So können Sie schnell die beliebtesten Seiten der einzelnen Kampagnen erfahren.
keywords: Analytics-Implementierung
seo-description: Das getAndPersistValue-Plug-in ruft einen Wert Ihrer Wahl ab und trägt ihn für einen bestimmten Zeitraum in eine Analytics-Variable ein. Normalerweise wird es genutzt, um zu sehen, wie viele Seitenaufrufe eine Kampagne nach einem Clickthrough generiert. So können Sie schnell die beliebtesten Seiten der einzelnen Kampagnen erfahren.
seo-title: getAndPersistValue
solution: Analytics
subtopic: Plug-ins
title: getAndPersistValue
topic: Entwickler und Implementierung
uuid: ddeab 80 c -260 e -44 b 6-8483-8 b 8 b 369 ec 19 b
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getAndPersistValue

Das getAndPersistValue-Plug-in ruft einen Wert Ihrer Wahl ab und trägt ihn für einen bestimmten Zeitraum in eine Analytics-Variable ein. Normalerweise wird es genutzt, um zu sehen, wie viele Seitenaufrufe eine Kampagne nach einem Clickthrough generiert. So können Sie schnell die beliebtesten Seiten der einzelnen Kampagnen erfahren.

>[!IMPORTANT]
>
>This plug-in has not been validated to be compatible with [AppMeasurement for JavaScript](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8). See [AppMeasurement Plug-in Support](../../../implement/js-implementation/c-appmeasurement-js/plugins-support.md#concept_E31A189BC8A547738666EB5E00D2252A).

For example, you might use this plug-in to set a campaign tracking code from the *`campaign`* variable into a Custom Traffic ( *`s.prop`*) variable on each visitor's page view made for the next 30 days. Mit diesem Beispiel können Sie ermitteln, wie viele Seitenaufrufe der Trackingcode als Ergebnis des ursprünglichen Clickthrough generiert hat.

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code und -Implementierung {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: Für diesen Abschnitt sind keine Änderungen erforderlich.

**Plug-in-Konfiguration**

Place the following code within the *`s_doPlugins()`* function, which is located in the area of the *`s_code.js`* file labeled *Plugin Config*. Wählen Sie eine benutzerspezifische Traffic-Variable (s.prop) oder eine benutzerspezifische Konversionsvariable (s.eVar), um diese für die Erfassung von Daten zu persistenten Werten zu verwenden. Dies muss eine Variable sein, die über die Admin Console aktiviert wurde, die jedoch aktuell nicht für einen anderen Zweck verwendet wird. Sie können das folgende Beispiel verwenden und an Ihre Anforderungen anpassen.

`s.prop1=s.getAndPersistValue(s.campaign,'s_getval',30);`

*`s.getAndPersistValue`* hat drei Argumente:

1. Currently populated variable or value to persist ( *`s.campaign`* shown above).
1. Cookie name, used to store the value ( *`s_getval`* shown above).
1. Der Zeitraum für die Persistenz in Tagen. Mit dem oben aufgeführten Wert von „30“ wird der Wert für die nächsten 30 Tage bei jedem Seitenaufruf durch den Benutzer in die ausgewählte Variable eingefügt. Wenn keine Angabe gemacht wird, wird die Standardeinstellung *Sitzung* verwendet.

**Plug-ins SECTION**: Fügen Sie in der Datei [!DNL s_code.js] den folgenden Code im Abschnitt Plug-ins SECTION hinzu. Nehmen Sie an diesem Teil des Plug-in-Codes keine Änderungen vor.

```js
/* 
 * Plugin: getAndPersistValue 0.3 - get a value on every page 
 */ 
s.getAndPersistValue=new Function("v","c","e","" 
+"var s=this,a=new Date;e=e?e:0;a.setTime(a.getTime()+e*86400000);if(" 
+"v)s.c_w(c,v,e?a:0);return s.c_r(c);");
```

Testen Sie die Installation von Plug-Ins stets ausführlich, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
