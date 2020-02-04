---
title: Übersicht über Zusatzmodule
description: Fügen Sie Code auf Ihrer Site ein, um neue Funktionen einzuführen.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b

---


# Übersicht über Zusatzmodule

Plug-ins sind Codefragmente, die mehrere erweiterte Funktionen ausführen, um Ihre Analytics-Implementierung zu unterstützen. Diese Plug-ins erweitern den Funktionsumfang Ihrer JavaScript-Datei um Funktionen, die bei einer Basisimplementierung nicht vorhanden sind. Im Rahmen erweiterter Lösungen bietet Adobe noch andere Plug-ins an.

> [!IMPORTANT] Plug-ins werden von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Die Adobe-Kundenunterstützung bietet keine Unterstützung für diese Plug-ins, einschließlich Installation oder Fehlerbehebung. Wenn Sie Hilfe bei einem Plug-In benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Adobe bietet mehrere Möglichkeiten, ein bestimmtes Plug-In zu installieren:

1. Verwenden Sie die Erweiterung &quot;Common Analytics Plugins&quot;mit Adobe Experience Platform Launch
2. Fügen Sie Plug-in-Code mit dem Editor Benutzerdefinierten Code starten ein.
3. Fügen Sie den Plug-in-Code in Ihre `AppMeasurement.js` Datei ein

Jedes Unternehmen hat unterschiedliche Implementierungsanforderungen, sodass Sie entscheiden können, wie Sie sie in Ihre Implementierung einbeziehen möchten. Stellen Sie sicher, dass Sie die folgenden Kriterien erfüllen, wenn Sie den Code auf Ihrer Site einbeziehen:

1. Instanziieren Sie zuerst das Analytics-Verfolgungsobjekt (unter Verwendung `s_gi`).
   * Beim Laden von Adobe Analytics wird das Verfolgungsobjekt automatisch instanziiert.
   * Implementierungen, bei denen das Verfolgungsobjekt `AppMeasurement.js` normalerweise oben in der JavaScript-Datei initialisiert wird.
2. Fügen Sie Plug-in-Code Sekunde ein.
   * Die Erweiterung &quot;Common Analytics Plugins&quot;verfügt über eine Aktionskonfiguration, in der Sie Plug-ins initialisieren können.
   * Wenn Sie das Plug-in nicht verwenden möchten, können Sie beim Konfigurieren der Analytics-Erweiterung den Plug-in-Code im Editor für benutzerspezifischen Code einfügen.
   * Wenn in Ihrer Implementierung &quot;Launch&quot;nicht verwendet wird, können Sie nach der Instanziierung des Verfolgungsobjekts Plug-in-Code an einer beliebigen `AppMeasurement.js` Stelle einfügen.
3. Rufen Sie das Plug-in dritt auf.
   * Alle Implementierungen, sowohl innerhalb als auch außerhalb von Launch, verwenden JavaScript, um Plug-ins aufzurufen. Rufen Sie das Plug-In in dem Format auf, das auf der Seite dieses Plug-Ins beschrieben ist.
4. Validieren Sie Ihre Implementierung und veröffentlichen Sie sie.

Viele Unternehmen rufen Plug-ins über die [`doPlugins`](../functions/doplugins.md) Funktion auf. Diese Funktion ist zwar nicht erforderlich, Adobe hält sie jedoch für eine Best Practice. AppMeasurement ruft diese Funktion kurz vor dem Kompilieren und Senden einer Bildanforderung auf. Dies ist ideal, da mehrere Plug-ins von anderen Analytics-Variablen abhängen.
