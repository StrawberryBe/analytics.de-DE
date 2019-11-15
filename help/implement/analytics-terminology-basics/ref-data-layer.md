---
description: Eine „Datenschicht“ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen.
keywords: Analytics Implementation;data layer;digitalData
solution: Analytics
title: Datenschicht
topic: Developer and implementation
uuid: dedb2a50-06f3-4354-8993-a25d4952ce1e
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Datenschicht

Eine _Datenschicht_ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen. Datenschichten können von Tracking-Tools (einschließlich Tag Management-Systemen wie Adobe Experience Platform Launch und Dynamic Tag Management) verwendet werden, um Berichte auszufüllen.

Die Implementierung einer Datenschicht auf Ihrer Site bietet Ihnen die ultimative Kontrolle und Flexibilität über Ihre Implementierung und ermöglicht eine einfache Wartung in zukünftigen Phasen. Die Namen dieser JavaScript-Objekte sind theoretisch beliebig, als Best Practice wird jedoch empfohlen, konsistente und vorhersagbare Bezeichnungen zu verwenden. Die Entwickler verfügen möglicherweise bereits über eine Datenschicht oder bevorzugen ein bestimmtes Format. Die Tracking-Community hat verschiedene Standards als Ausgangspunkt erstellt. Das Spezifikationsdokument [Data Layer for Analytics Implementation](assets/datalayer-documentation.pdf) (Datenschicht für die Analytics-Implementierung) verwendet das W3C-Standardobjekt „digitalData“, das von einem Großteil der Tracking-Technologien akzeptiert wird, falls die Datenschicht für mehr als diese DTM-Implementierung benötigt wird.
