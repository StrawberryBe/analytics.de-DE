---
description: Data Warehouse bezieht sich auf die Kopie der Analytics-Daten für Speicherberichte und benutzerspezifische Berichte, die Sie durch Filtern der Daten ausführen können. Sie können Berichte anfordern, um erweiterte Datenbeziehungen aus Rohdaten basierend auf den für Sie relevanten Fragen anzuzeigen. Data Warehouse-Berichte werden per E-Mail an einen Cloud-Speicher-Provider gesendet oder an diesen gesendet. Die Verarbeitung kann bis zu 72 Stunden dauern. Die Verarbeitungsdauer ist abhängig von der Komplexität der Abfrage und der Menge der zu verarbeitenden Daten.
title: Data Warehouse-Übersicht
feature: Data Warehouse
uuid: 768557dd-1644-4ce6-bfc2-8c46dd6e1cd1
exl-id: 6a051d53-397b-4a55-9cca-1c83b31c9448
source-git-commit: 3af2cca02675e424b3f704a95d46de92886a88d8
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 58%

---

# Data Warehouse-Übersicht

Mit Data Warehouse können Sie Adobe Analytics-Daten kopieren, um sie zu speichern und benutzerdefinierte Berichte zu erstellen, die Sie durch Filtern der Daten ausführen können.

## Berichtübersicht

Data Warehouse-Berichte können erweiterte Datenbeziehungen aus Rohdaten basierend auf Ihren individuellen Fragen anzeigen. Sie können eine unbegrenzte Anzahl von Zeilen in eine einzelne Anforderung einschließen (für individuelle, terminierte und heruntergeladene Berichte).

>[!NOTE]
>
>Data Warehouse gibt in Berichten den ersten aufgefundenen Wert innerhalb des Berichtszeitraums aus.

>[!IMPORTANT]
>
>Bei der Segmentierung nach klassifizierten Werten behandeln Analysis Workspace und Data Warehouse „nicht spezifizierte“ Werte unterschiedlich. „Nicht spezifiziert“ in Workspace bezieht sich auf Werte, die nicht klassifiziert sind, während „nicht spezifiziert“ in Data Warehouse auf Werte verweist, die Sie als „nicht spezifiziert“ klassifiziert haben.

## Versandübersicht

Data Warehouse-Berichte werden per E-Mail an einen Cloud-Speicher-Provider versendet oder können bis zu 72 Stunden für die Verarbeitung benötigen. Die Verarbeitungsdauer ist abhängig von der Komplexität der Abfrage und der Menge der zu verarbeitenden Daten.

Data Warehouse ZIP-komprimiert automatisch Dateien, die größer als 1 MB sind. Die Maximalgröße für E-Mail-Anhänge beträgt 10 MB.

## Zugriff auf

Adobe aktiviert Data Warehouse nur für Benutzer auf Administratorebene und nur für bestimmte Report Suites. (Die Funktion kann für globale und untergeordnete Report Suites, jedoch nicht für Datenaggregations-Report Suites aktiviert werden.) Der Administrator kann eine Gruppe erstellen, die Zugriff auf Data Warehouse hat, und anschließend Benutzer, die sich nicht auf Administrator-Ebene befinden, dieser Gruppe zuweisen.

Siehe [Data Warehouse-Berechtigungen verwalten](/help/export/data-warehouse/t-dw-group.md).

## Erstellen einer Data Warehouse-Anforderung

Informationen zum Erstellen einer Data Warehouse-Anfrage finden Sie unter [Erstellen einer Data Warehouse-Anfrage](/help/export/data-warehouse/create-request/t-dw-create-request.md).

## Verwalten von Data Warehouse-Anforderungen

Informationen zum Verwalten von Data Warehouse-Anfragen finden Sie unter [Data Warehouse-Anforderungen verwalten](/help/export/data-warehouse/data-warehouse-requests-manage.md).

## Häufig gestellte Fragen

Eine Liste der häufig gestellten Fragen finden Sie unter [Data Warehouse-FAQs](/help/export/data-warehouse/faq.md).