---
title: Zuordnung von Datenobjektvariablen zu Adobe Analytics
description: Anzeigen der Datenobjektfelder, die Edge automatisch Analytics-Variablen zuordnet
feature: Implementation Basics
role: Admin, Developer
source-git-commit: 12347957a7a51dc1f8dfb46d489b59a450c2745a
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 5%

---

# Zuordnung von Datenobjektvariablen zu Adobe Analytics

Die folgende Tabelle zeigt die Datenobjektvariablen, die das Adobe Experience Platform Edge Network automatisch Adobe Analytics zuordnet. Wenn Sie diese Datenobjektfeldpfade verwenden, ist keine zusätzliche Konfiguration erforderlich, um Daten an Adobe Analytics zu senden.

Die Verwendung dieser Felder wird empfohlen, wenn Sie in Zukunft Customer Journey Analytics verwenden möchten. Mit dieser Implementierungsmethode kann Ihr Unternehmen Daten mit dem Web SDK an Adobe senden, ohne ein XDM-Schema zu erfüllen. Wenn Ihr Unternehmen bereit ist, Daten an Adobe Experience Platform zu senden, können Sie [Datenspeicherzuordnung](https://experienceleague.adobe.com/docs/experience-platform/datastreams/data-prep.html#mapping) , um Datenobjektfelder auf ihre jeweiligen XDM-Felder zu verweisen.

## Wertprioritäten

Die meisten Datenobjektfelder in dieser Tabelle entsprechen einem [Zugeordnetes XDM-Feld](xdm-var-mapping.md). Wenn Sie beide `data` -Objektfeld und dem entsprechenden XDM-Feld hat das Datenobjektfeld Priorität. Wenn Sie sowohl das XDM-Objektfeld als auch das Datenobjektfeld verwenden, empfiehlt Adobe, benutzerdefinierte Ereignisse mithilfe des Datenobjektfelds festzulegen. Wenn das Feld `data.__adobe.analytics.events` vorhanden ist, werden alle XDM-Objektfelder, die mit Commerce- und benutzerspezifischen Ereignissen verknüpft sind, überschrieben.

Einige Datenobjektfelder unterstützen auch ihre jeweiligen [Abfrageparameterwert](../validate/query-parameters.md) als Kurzwerte. Sie können standardmäßige Datenobjektfelder und kurze Datenobjektfelder synonym verwenden, sofern sie jeweils für eindeutige Variablen gelten. Vermeiden Sie es, gleichzeitig ein standardmäßiges Datenobjektfeld und das entsprechende Kurzdatenobjektfeld festzulegen. Adobe kann nicht garantieren, welches Feld Priorität hat.

## Datenobjektfeldzuordnung

Vorherige Aktualisierungen dieser Tabelle finden Sie auf der Seite [Commit-Verlauf auf GitHub](https://github.com/AdobeDocs/analytics.en/commits/main/help/implement/aep-edge/data-var-mapping.md).

| Datenobjektfeldpfad | Analytics-Variable und -Beschreibung |
| --- | --- |
| `data.__adobe.analytics.browserHeight` | Die [Browserhöhe](../../components/dimensions/browser-height.md) Dimension. Das Kurzfeld `data.__adobe.analytics.bh` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.browserWidth` | Die [Browser-Breite](../../components/dimensions/browser-width.md) Dimension. Das Kurzfeld `data.__adobe.analytics.bw` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.campaign` | Die [Trackingcode](../../components/dimensions/tracking-code.md) Dimension. Das Kurzfeld `data.__adobe.analytics.v0` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.channel` | Die [Website-Bereich](../../components/dimensions/site-section.md) Dimension. Das Kurzfeld `data.__adobe.analytics.ch` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.colorDepth` | Die [Farbtiefe](../../components/dimensions/color-depth.md) Dimension. Das Kurzfeld `data.__adobe.analytics.c` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.connectionType` | Die [Verbindungstyp](../../components/dimensions/connection-type.md) Dimension. Das Kurzfeld `data.__adobe.analytics.ct` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.contextData` | [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md). |
| `data.__adobe.analytics.cookiesEnabled` | Die [Cookie-Unterstützung](../../components/dimensions/cookie-support.md) Dimension. Das Kurzfeld `data.__adobe.analytics.k` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.currencyCode` | Die [`currencyCode`](../vars/config-vars/currencycode.md) Implementierungsvariable. Das Kurzfeld `data.__adobe.analytics.cc` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.dynamicVariablePrefix` | Die [`dynamicVariablePrefix`](../vars/config-vars/dynamicvariableprefix.md) Implementierungsvariable. |
| `data.__adobe.analytics.eVar1` - `data.__adobe.analytics.eVar250` | [eVar](../../components/dimensions/evar.md) Dimensionen. Die Kurzfelder `data.__adobe.analytics.v1` - `data.__adobe.analytics.v250` werden auch unterstützt. |
| `data.__adobe.analytics.events` | [Benutzerspezifische Ereignisse](../../components/metrics/custom-events.md). Formatieren Sie dieses Feld ähnlich dem [`events`](../vars/page-vars/events/events-overview.md) Implementierungsvariable. |
| `data.__adobe.analytics.javaEnabled` | Die [Java aktiviert](../../components/dimensions/java-enabled.md) Dimension. Das Kurzfeld `data.__adobe.analytics.v` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.latitude` | Hilft beim Festlegen der [Standort](../../components/dimensions/lifecycle-dimensions.md) Mobile Lebenszyklusdimensionen. Das Kurzfeld `data.__adobe.analytics.lat` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkName` | Die [Benutzerspezifischer Link](../../components/dimensions/custom-link.md), [Downloadlink](../../components/dimensions/download-link.md)oder [Exitlink](../../components/dimensions/exit-link.md) Dimension, abhängig vom Wert in `data.__adobe.analytics.linkType`. Das Kurzfeld `data.__adobe.analytics.pev2` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkURL` | Die [`linkURL`](../vars/config-vars/linkurl.md) Implementierungsvariable. Das Kurzfeld `data.__adobe.analytics.pev1` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.linkType` | Bestimmt den Typ des angeklickten Links. Gültige Werte sind `o` (Benutzerspezifische Links), `d` (Downloadlinks) und `e` (Exitlinks). Das Kurzfeld `data.__adobe.analytics.pe` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.list1` - `data.__adobe.analytics.list3` | [`list`](/help/implement/vars/page-vars/list.md) Implementierungsvariablen. Die Kurzfelder `data.__adobe.analytics.l1` - `data.__adobe.analytics.list3` werden auch unterstützt. |
| `data.__adobe.analytics.longitude` | Hilfesatz [Standort](../../components/dimensions/lifecycle-dimensions.md) Mobile Lebenszyklusdimensionen. Das Kurzfeld `data.__adobe.analytics.lon` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.pageName` | Die Dimension [Seite](/help/components/dimensions/page.md). |
| `data.__adobe.analytics.pageURL` | Die [Seiten-URL](/help/components/dimensions/page-url.md) Dimension. Das Kurzfeld `data.__adobe.analytics.g` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.pageType` | Die [`pageType`](../vars/page-vars/pagetype.md) Implementierungsvariable. |
| `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75` | [Prop](../../components/dimensions/prop.md) Dimensionen. Die Kurzfelder `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` werden auch unterstützt. |
| `data.__adobe.analytics.purchaseID` | Die [`purchaseID`](../vars/page-vars/purchaseid.md) Implementierungsvariable. |
| `data.__adobe.analytics.products` | Die [`products`](../vars/page-vars/products.md) Implementierungsvariable, ähnlich formatiert. |
| `data.__adobe.analytics.referrer` | Die Dimension [Referrer](/help/components/dimensions/referrer.md). |
| `data.__adobe.analytics.resolution` | Die [Bildschirmauflösung](../../components/dimensions/monitor-resolution.md) Dimension. Das Kurzfeld `data.__adobe.analytics.s` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.server` | Die Dimension [Server](/help/components/dimensions/server.md). |
| `data.__adobe.analytics.tnta` | Wird in A4T-Integrationen verwendet. |
| `data.__adobe.analytics.transactionID` | Die [`transactionID`](../vars/page-vars/transactionid.md) Implementierungsvariable. Das Kurzfeld `data.__adobe.analytics.xact` wird ebenfalls unterstützt. |
| `data.__adobe.analytics.zip` | Die [Postleitzahl](../../components/dimensions/zip-code.md) Dimension. |

{style="table-layout:auto"}
