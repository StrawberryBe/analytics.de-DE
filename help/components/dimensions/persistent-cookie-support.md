---
title: Unterstützung persistenter Cookies
description: Bestimmt, ob der Besucher persistente Cookies unterstützen kann.
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
source-git-commit: 82d6137bc9229bbaa997c6856690bf76c20b755c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 11%

---

# Unterstützung persistenter Cookies

Die Dimension &quot;Unterstützung persistenter Cookies&quot;zeigt an, ob der Treffer eine Besucher-ID verwendet hat, die aus einer persistenten Quelle stammt. Die häufigste persistente Quelle ist ein Cookie, kann aber auch mobile Header und andere Quellen verwenden.

## Füllen dieser Dimension mit Daten

Die Adobe bestimmt den Wert dieser Dimension Server-seitig anhand der Quelle der Kennung des Treffers. Es gibt keine Möglichkeit, sie direkt festzulegen. Sie ist bei allen Implementierungen vorkonfiguriert.

## Dimensionselemente

* **`Enabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die normalerweise beibehalten wird. Die häufigsten Beispiele sind Abfragezeichenfolgenparameter `aid`, `fid` oder `mid` , da diese ihre Werte aus einem Cookie ableiten.
* **`Disabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die von der Adobe nicht als beständig erkannt wird, z. B. IP + Benutzeragenten-Zeichenfolge. Dieses Dimensionselement enthält auch benutzerdefinierte Besucher-IDs, die die Variable [`visitorID`](/help/implement/vars/config-vars/visitorid.md) verwenden.

## Unterschied zwischen &quot;Cookie-Unterstützung&quot;und &quot;Unterstützung persistenter Cookies&quot;

* **Cookie-Unterstützung**: AppMeasurement versucht, ein allgemeines Cookie zu setzen. Das Dimensionselement basiert auf der erfolgreichen Einstellung des Cookies.
* **Unterstützung persistenter Cookies**: Das Dimensionselement basiert auf , ob die Kennung des Treffers aus einer persistenten Quelle wie einem Cookie stammt.
