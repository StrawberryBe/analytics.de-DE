---
title: Feldbasierte Heften
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen des Zusammenführens von Daten mithilfe der feldbasierten Suche vertraut.
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 23%

---


# Feldbasierte Heften

Geräteübergreifende Analytics bietet zwei verschiedene Methoden zum Zusammenfügen von Daten. Bei dieser Methode wird eine Analytics-Variable, z. B. eine [Eigenschaftsvariable](/help/implement/vars/page-vars/prop.md) oder eine [eVar](/help/implement/vars/page-vars/evar.md), verwendet, um eine Personenkennung zu enthalten. Diese Variable wird als Grundlage für die Verknüpfung von Geräten verwendet.

## Spezifische Voraussetzungen für das field-based stitching

Wenn Sie die geräteübergreifende Analyse mithilfe der feldbasierten Suche implementieren möchten, sind folgende Schritte erforderlich. Arbeiten Sie mit Teams in Ihrer Organisation und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie die folgenden Kriterien alle erfüllen.

>[!IMPORTANT]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.

* Alle auf der [Übersichtsseite](overview.md)aufgelisteten Voraussetzungen.
* In Ihrer Implementierung muss eine Eigenschaftsvariable oder eine eVar festgelegt werden, die eine Einzelperson nach Möglichkeit eindeutig identifiziert, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Weisen Sie die gewünschte identifizierende Variable Ihrem Kundenbetreuer zu, wenn sie für die feldbasierte Suche bereitgestellt wird.

## Spezifische Einschränkungen für das bereichsbasierte Heften

* Die feldbasierte Suche funktioniert am besten bei Report Suites mit einer hohen Benutzeridentifizierungsrate. Wenn Ihre Report Suite eine niedrige Identifizierungs- oder Anmelderate aufweist, sollten Sie das [Co-op-Diagramm](device-graph.md)verwenden.

## Nächste Schritte

Once your organization meets all requirements met and understands the limitations, you can start [Setting up Cross-Device Analytics](setup.md).