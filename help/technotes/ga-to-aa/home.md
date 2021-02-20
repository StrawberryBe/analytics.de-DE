---
title: Umstieg von einer Drittanbieter-Analyseplattform auf Adobe Analytics
description: Erfahren Sie mehr über die wichtigsten Konzepte zum Abrufen von Berichten, die auf Anwender ausgerichtet sind, die mit anderen Plattformen wie Google Analytics vertraut sind.
translation-type: tm+mt
source-git-commit: 3211598c2ff43493b329a9be4fb6877ae29cf08b
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 100%

---


# Umstieg von einer Drittanbieter-Analyseplattform auf Adobe Analytics

In diesem Handbuch werden allgemeine Berichtstypen vorgestellt, die Ihnen helfen, Kernkonzepte und Workflows in Adobe Analytics zu erlernen, wobei der Schwerpunkt auf wichtigen Ähnlichkeiten und Unterschieden zwischen Adobe und anderen gängigen Tools liegt. Dieses Handbuch richtet sich an Analysten, die mit grundlegenden Konzepten der digitalen Analyse vertraut, aber neu bei Adobe Analytics sind. Es wird davon ausgegangen, dass das Unternehmen über eine funktionierende Implementierung verfügt, die Daten an Adobe-Datenerfassungs-Server sendet. Wenn Ihr Unternehmen noch keine Adobe Analytics-Implementierung eingerichtet hat, beginnen Sie mit dem [ersten Adobe Analytics-Administratorhandbuch](/help/admin/admin-console/first-admin-guide.md).

Sowohl Google Analytics als auch Adobe Analytics sind leistungsstarke Plattformen, um wertvolle Einblicke in die Leistung Ihrer Website zu erhalten. Jede Plattform verfügt über eine eigene Verarbeitungsarchitektur und eine eigene Benutzeroberfläche, durch die jede Plattform einzigartige Vorteile bietet. Dieses Handbuch soll dazu beitragen, dass Anwender mit Erfahrung in Google Analytics schneller mit Adobe Analytics arbeiten können.

In Adobe Analytics gibt es zwei Hauptwege, um nach der Anmeldung bei der Adobe Experience Cloud grundlegende Berichte abzurufen:

* **Reports &amp; Analytics** ist die alte Methode, um grundlegende Berichte zu erstellen. Das Menü auf der linken Seite enthält eine Liste vordefinierter Berichte, die es dem Anwender ermöglicht, zu einem gewünschten Bericht zu navigieren und Daten abzurufen. Segmente und Metriken ermöglichen zusätzliche Anpassungen. Anwender mit Erfahrung mit Google Analytics-Berichten finden dieses Layout möglicherweise vertraut.
* **Analysis Workspace** ist die derzeit empfohlene Methode für den Abruf der meisten Berichte. Im linken Menü können Anwender Komponenten per Drag-and-drop verschieben, um einen eigenen Bericht zu erstellen. Das ermöglicht viel mehr Freiheit, um die Berichtsanforderungen genau zu erfüllen. Anwender, die mit der Erstellung von Google Analytics-Dashboards und benutzerspezifischen Berichten vertraut sind, finden dieses Layout möglicherweise vertraut.

Die meisten Berichte können sowohl in [!UICONTROL Reports &amp; Analytics] als auch in [!UICONTROL Analysis Workspace] erstellt werden. Einige Berichte können jedoch nur auf der einen oder anderen Plattform abgerufen werden. In den meisten Fällen empfiehlt Adobe die Verwendung von [!UICONTROL Analysis Workspace], es sei denn, eine bestimmte Funktion ist nur in [!UICONTROL Reports &amp; Analytics] verfügbar.

## Empfohlener Lernpfad

Adobe empfiehlt, mit den absoluten Grundlagen des Abrufs von Berichtsdaten zu beginnen:

* [Basisbericht in Analysis Workspace für GA-Anwender erstellen](reports/create-report.md)

Sobald Sie sich mit den Komponenten in [!UICONTROL Analysis Workspace] vertraut gemacht haben, können Sie lernen, wie sich die meisten Berichte mithilfe der richtigen Komponenten nachbilden lassen.

* [Erstellen von Echtzeitberichten in Adobe Analytics](reports/realtime-reports.md)
* [Erstellen von Zielgruppenberichten in Adobe Analytics](reports/audience-reports.md)
* [Erstellen von Akquiseberichten in Adobe Analytics](reports/acquisition-reports.md)
* [Erstellen von Verhaltensberichten in Adobe Analytics](reports/behavior-reports.md)
* [Erstellen von Konversionsberichten in Adobe Analytics](reports/conversions-reports.md)

Nachdem Sie gelernt haben, Berichte abzurufen, sollten Sie die [Unterschiede bei Verarbeitung und Architektur](processing-differences.md) kennenlernen, um die unterschiedlichen Zahlen der verschiedenen Plattformen abzustimmen. Auch [FAQs](faq.md) stehen zur Verfügung.
