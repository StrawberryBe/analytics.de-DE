---
description: Das getAndPersistValue-Plug-in ruft einen Wert Ihrer Wahl ab und trägt ihn für einen bestimmten Zeitraum in eine Analytics-Variable ein. Normalerweise wird es genutzt, um zu sehen, wie viele Seitenaufrufe eine Kampagne nach einem Clickthrough generiert. So können Sie schnell die beliebtesten Seiten der einzelnen Kampagnen erfahren.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getAndPersistValue
topic: Developer and implementation
uuid: ddeab80c-260e-44b6-8483-8b8b369ec19b
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getAndPersistValue

Das getAndPersistValue-Plug-in ruft einen Wert Ihrer Wahl ab und trägt ihn für einen bestimmten Zeitraum in eine Analytics-Variable ein. Normalerweise wird es genutzt, um zu sehen, wie viele Seitenaufrufe eine Kampagne nach einem Clickthrough generiert. So können Sie schnell die beliebtesten Seiten der einzelnen Kampagnen erfahren.

>[!IMPORTANT]
>
>Dieses Plug-in wurde nicht auf Kompatibilität mit [AppMeasurement für JavaScript](/help/implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md) überprüft. Siehe [AppMeasurement-Plug-in-Unterstützung](/help/implement/js-implementation/c-appmeasurement-js/plugins-support.md).

Beispielsweise können Sie mit diesem Plug-in einen Kampagnen-Trackingcode aus der Variable *`campaign`* in eine benutzerspezifische Traffic-Variable (*`s.prop`*) für die Seitenansicht jedes Besuchers für die nächsten 30 Tage setzen. Mit diesem Beispiel können Sie ermitteln, wie viele Seitenaufrufe der Trackingcode als Ergebnis des ursprünglichen Clickthrough generiert hat.

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code und -Implementierung {#section_92E94A96A4764113B5588F1B83E3DE2C}

**CONFIG SECTION**: Für diesen Abschnitt sind keine Änderungen erforderlich.

**Plug-in-Konfiguration**

Fügen Sie den folgenden Code innerhalb der Funktion *`s_doPlugins()`* ein, die sich in der Datei *`s_code.js`* im Abschnitt *Plugin Config* befindet. Wählen Sie eine benutzerspezifische Traffic-Variable (s.prop) oder eine benutzerspezifische Konversionsvariable (s.eVar), um diese für die Erfassung von Daten zu persistenten Werten zu verwenden. Dies muss eine Variable sein, die über die Admin Console aktiviert wurde, die jedoch aktuell nicht für einen anderen Zweck verwendet wird. Sie können das folgende Beispiel verwenden und an Ihre Anforderungen anpassen.

`s.prop1=s.getAndPersistValue(s.campaign,'s_getval',30);`

*`s.getAndPersistValue`* hat drei Argumente:

1. Derzeit ausgefüllte Variable oder zu behaltender Wert (*`s.campaign`* wie oben gezeigt).
1. Cookie-Name, mit dem der Wert gespeichert wird (*`s_getval`* wie oben gezeigt).
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
