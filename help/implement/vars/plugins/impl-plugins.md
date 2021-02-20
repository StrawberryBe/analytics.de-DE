---
title: Übersicht über Plug-ins
description: Fügen Sie Code auf Ihrer Website ein, um neue Funktionen einzuführen.
translation-type: tm+mt
source-git-commit: e758c070f402113b6d8a9069437b53633974a3e9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 100%

---


# Übersicht über Plug-ins

Plug-ins sind Codefragmente, die mehrere erweiterte Funktionen ausführen, um Ihre Analytics-Implementierung zu unterstützen. Diese Plug-ins erweitern den Funktionsumfang Ihrer JavaScript-Datei um Funktionen, die bei einer Basisimplementierung nicht vorhanden sind. Im Rahmen erweiterter Lösungen bietet Adobe noch andere Plug-ins an.

>[!IMPORTANT]
>
>Plug-ins werden von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für diese Plug-ins, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit einem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Adobe bietet mehrere Möglichkeiten, ein bestimmtes Plug-in zu installieren:

1. Verwenden der Erweiterung „Common Analytics Plugins“ mit Adobe Experience Platform Launch.
2. Einfügen des Plug-in-Codes mit dem benutzerdefinierten Code-Editor in Launch.
3. Einfügen des Plug-in-Codes in Ihre `AppMeasurement.js`-Datei.

Jedes Unternehmen hat unterschiedliche Implementierungsanforderungen, sodass Sie entscheiden können, wie Sie sie in Ihre Implementierung einbeziehen möchten. Stellen Sie sicher, dass Sie die folgenden Kriterien erfüllen, wenn Sie den Code auf Ihrer Website einbeziehen:

1. Instanziieren Sie zuerst das Analytics-Tracking-Objekt (unter Verwendung von [`s_gi`](../functions/s-gi.md)).
   * Launch instanziiert das Tracking-Objekt beim Laden von Adobe Analytics automatisch.
   * Implementierungen mit `AppMeasurement.js` initialisieren normalerweise das Tracking-Objekt am Anfang der JavaScript-Datei.
2. Fügen Sie als Zweites den Plug-in-Code ein.
   * Die Erweiterung „Common Analytics Plugins“ verfügt über eine Aktionskonfiguration, in der Sie Plug-ins initialisieren können.
   * Wenn Sie die Erweiterung nicht verwenden möchten, können Sie beim Konfigurieren der Analytics-Erweiterung den Plug-in-Code im Editor für benutzerdefinierten Code einfügen.
   * Wenn Ihre Implementierung Launch nicht verwendet, können Sie Plug-in-Code an einer beliebigen Stelle in `AppMeasurement.js` einfügen, nachdem Sie das Tracking-Objekt instanziiert haben.
3. Rufen Sie das Plug-in als Drittes auf.
   * Alle Implementierungen, sowohl innerhalb als auch außerhalb von Launch, verwenden JavaScript, um Plug-ins aufzurufen. Rufen Sie das Plug-in in dem Format auf, das auf der Seite des Plug-ins beschrieben ist.
4. Validieren Sie Ihre Implementierung und veröffentlichen Sie sie.

Viele Unternehmen rufen Plug-ins über die [`doPlugins`](../functions/doplugins.md)-Funktion auf. Diese Funktion ist zwar nicht erforderlich, Adobe hält sie jedoch für eine Best Practice. AppMeasurement ruft diese Funktion kurz vor dem Kompilieren und Senden einer Bildanforderung auf. Dies ist ideal, da mehrere Plug-ins von anderen Analytics-Variablen abhängen.

## Plug-ins mit nicht standardmäßigen Tracking-Objekten verwenden

Plug-ins funktionieren standardmäßig nicht mit anderen Tracking-Objekten als `s`. Sie können jedoch den Plug-in-Code ändern, um das benutzerdefinierte Tracking-Objekt aufzunehmen. Ersetzen Sie in einem gegebenen Plug-in alle Verweise auf `s` mit dem gewünschten Tracking-Objekt.
