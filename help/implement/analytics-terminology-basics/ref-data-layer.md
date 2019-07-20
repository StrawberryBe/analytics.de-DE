---
description: Eine „Datenschicht“ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen.
keywords: Analytics-Implementierung; data layer; Digitaldata
seo-description: Eine „Datenschicht“ ist ein Framework von JavaScript-Objekten, die Entwickler in Seiten einfügen. Datenschichten können von Tracking-Tools (einschließlich Tag Management-Systemen wie dem Dynamic Tag Management) verwendet werden, um Berichte auszufüllen.
seo-title: Datenschicht
solution: Analytics
title: Datenschicht
topic: Entwickler und Implementierung
uuid: dedb 2 a 50-06 f 3-4354-8993-a 25 d 4952 ce 1 e
translation-type: tm+mt
source-git-commit: 26c3cc9895c27d6abc452e0a4636771fb2415fb3

---


# Datenschicht

A _data layer_ is a framework of JavaScript objects that developers insert into pages. Die Datenschichten können mithilfe von Verfolgungswerkzeugen (einschließlich Tag-Management-Systemen wie Adobe Experience Platform Launch und dynamisches Tag-Management) verwendet werden, um Berichte auszufüllen.

Die Implementierung einer Datenschicht auf Ihrer Site bietet Ihnen die ultimative Kontrolle und Flexibilität über Ihre Implementierung und ermöglicht eine einfache Wartung in zukünftigen Phasen. Die Namen dieser JavaScript-Objekte sind theoretisch beliebig, als Best Practice wird jedoch empfohlen, konsistente und vorhersagbare Bezeichnungen zu verwenden. Die Entwickler verfügen möglicherweise bereits über eine Datenschicht oder eine Präferenz für das Format. Die Tracking-Community hat verschiedene Standards als Ausgangspunkt erstellt. Das Spezifikationsdokument [Data Layer for Analytics Implementation](assets/datalayer-documentation.pdf) (Datenschicht für die Analytics-Implementierung) verwendet das W3C-Standardobjekt „digitalData“, das von einem Großteil der Tracking-Technologien akzeptiert wird, falls die Datenschicht für mehr als diese DTM-Implementierung benötigt wird.
