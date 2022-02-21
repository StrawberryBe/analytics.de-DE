---
title: Unterstützung persistenter Cookies
description: Bestimmt, ob der Besucher persistente Cookies unterstützen kann.
feature: Dimensions
exl-id: ced69e41-d992-4c5a-8541-920aeb7186ae
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 100%

---

# Unterstützung persistenter Cookies

Die Dimension „Unterstützung persistenter Cookies“ zeigt an, ob der Treffer eine Besucher-ID verwendet hat, die aus einer persistenten Quelle stammt. Die häufigste persistente Quelle ist ein Cookie, aber auch mobile Header und andere Quellen sind möglich.

## Diese Dimension mit Daten füllen

Adobe bestimmt den Wert dieser Dimension Server-seitig anhand der Quelle der Trefferkennung. Es gibt keine Möglichkeit, ihn direkt festzulegen. Dies ist bei allen Implementierungen vorkonfiguriert.

## Dimensionselemente

* **`Enabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die persistent ist. Die häufigsten Beispiele sind die Abfragezeichenfolgenparameter `aid`, `fid` oder `mid`, da diese ihre Werte von einem Cookie beziehen.
* **`Disabled`**: Die Besucher-ID des Treffers stammt aus einer Quelle, die von Adobe nicht als persistent erachtet wird, z. B. IP + Benutzeragenten-Zeichenfolge. Dieses Dimensionselement enthält auch benutzerdefinierte Besucher-IDs, die die Variable [`visitorID`](/help/implement/vars/config-vars/visitorid.md) verwenden.

## Unterschied zwischen „Unterstützung von Cookies“ und „Unterstützung persistenter Cookies“

* **Unterstützung von Cookies**: AppMeasurement versucht, ein generisches Cookie zu setzen. Das Dimensionselement basiert auf dem erfolgreichen Setzen des Cookies.
* **Unterstützung persistenter Cookies**: Das Dimensionselement basiert darauf, ob die Kennung des Treffers von einer persistenten Quelle wie einem Cookie stammt.
