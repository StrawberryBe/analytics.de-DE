---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# s_objectID

Die Variable ist eine globale Variable, die im [!UICONTROL onClick]-Ereignis eines Links festgelegt wird.


<!-- 

s_objectID.xml

 -->

Durch Erstellung einer eindeutigen Objekt-ID für einen Link oder eine Linkposition auf einer Seite können Sie das Tracking der Besucheraktivität verbessern oder [!UICONTROL Activity Map] zum Generieren von Berichten zum Linktyp oder zur Linkposition anstelle der Link-URL verwenden.

> [!NOTE] Bei Verwendung von s_objectID mit [Activity Map](https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/activitymap-link-tracking-use-case.html)ist ein nachfolgender Semikolon (;) erforderlich.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | OID | [!UICONTROL Activity Map], [!UICONTROL ClickMap] | Die absolute URL eines angeklickten Links |

Für die Verwendung von *`s_objectID`* gibt es drei gängige Gründe:

* Zusammenfassen von Besucheraktivitäten, die sich im Laufe eines Tages häufig ändern
* Herausfiltern von Link-Aktivitäten, die [!UICONTROL Activity Map] kombiniert.
* Verbessern der Genauigkeit der [!UICONTROL Activity Map]-Datenberichterstellung.

**Aggregieren von Klicks auf extrem dynamische Links** {#section_BA730A0393B149DDBCAA272C3C23A1C5}

Wenn Ihre Website sehr dynamisch ist und sich die Links auf einigen Seiten im Laufe des Tages ändern, kann *`s_objectID`* verwendet werden, um die Position eines Links auf der Seite zu identifizieren. Wenn *`s_objectID`* auf „links oben 1“ oder „links oben 2“ gesetzt wird, was beispielsweise den ersten Link oben links auf der Seite darstellt, werden alle Links, die an diesem Ort erscheinen (bzw. die den gleichen Wert wie *`s_objectID`* haben), zusammen mit der Besucher-ClickMap gemeldet. Wenn Sie *`s_objectID`* nicht verwenden, wird Ihnen zwar angezeigt, wie oft auf einen bestimmten Link geklickt wurde, Sie können jedoch nicht mehr erkennen, wie alle anderen Links an dieser Stelle von Besuchern verwendet wurden.

**Unterscheidung zusammengefasster Klicks** {#section_1AE91FB8A2D3423CBE064ACF02FEEA47}

Wenn die Variable *`pageName`* auf Ihrer Site verwendet wird, um den Abschnitt oder die Vorlage anzuzeigen, den/die ein Besucher anzeigt, und nicht die spezifische Seite, die der Besucher anzeigt, können Sie Links mit *`s_objectID`* trennen, die in mehreren Versionen dieser Seitenvorlage angezeigt werden sollen. Wenn Sie zum Beispiel über eine Vorlagenseite für alle Produkte auf Ihrer Site verfügen, enthält diese Vorlage sehr wahrscheinlich für alle Seiten einen Link zu Ihrer Homepage und zu einem Suchfeld. Wenn Sie sehen möchten, wie diese Links bei einzelnen Produkten genutzt werden (anstatt auf Basis einer Vorlage), können Sie in *`s_objectID`* einen produktspezifischen Wert eintragen (wie z. B. „Produkt 123789 Homepage“ oder „Produkt 123789 Suche“). Anschließend basieren [!UICONTROL Activity Map]-Berichte zu diesen Links auf einzelnen Produkten.

**Verbessern der[!UICONTROL Activity Map]-Genauigkeit** {#section_08B3406821294DCCABEEB99C90CF5C52}

In einigen Fällen werden andere Browser als Internet Explorer, Firefox, Netscape, Opera und Safari in Berichten nicht aufgeführt. Diese machen zwar nur einen kleinen prozentualen Anteil aus, tragen aber zu einigen Klicks und anderen Metriken mit bei. Verwenden Sie *`s_objectID`* in Links zur eindeutigen Identifizierung der Adressen des Browser-Berichtsproblems. Das folgende Beispiel zeigt, wie Sie Ihre Links zur Verwendung von *`s_objectID`*:

```js
<a href="/art.jsp?id=559" onClick="s_objectID='top left 1';">Article 559</a> 
<a href="/home.jsp" onClick="s_objectID='prod 123789 home page';">Home</a> 
```

**Syntax und mögliche Werte** {#section_85841DF9F06A4680953D9B2A884A1A5A}

In „s_objectID“ darf ein beliebiger Textbezeichner stehen.

```js
s_objectID="unique_id" 
```

*`s_objectID`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_33F119D532CA4ACAA3426253C42030BB}

```js
s_objectID="top left 2" 
```

```js
s_objectID="prod 123789 search"
```

**Konfigurationseinstellungen** {#section_95396657D55B41ECB66B83D0534EA827}

Keine
