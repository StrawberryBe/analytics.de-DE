---
description: In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.
keywords: Data Feed;job;metrics;pre column;post column;bots;date filtering;event string;common;formulas
solution: Analytics
title: Berechnete Metriken
topic: Reports and analytics
uuid: a45ea5bb-7c83-468f-b94a-63add78931d7
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Verwenden von Datenfeeds zur Berechnung allgemeiner Metriken

In diesem Abschnitt wird erläutert, wie häufig verwendete Metriken mithilfe von Datenfeeds berechnet werden.

> [!IMPORTANT] Treffer, die normalerweise aus Adobe Analytics ausgeschlossen werden, werden in Data Feeds eingeschlossen. Mit dieser Option können Sie ausgeschlossene Treffer aus Abfragen von Rohdaten entfernen. `exclude_hit > 0` Datenbezogene Daten werden auch in Datenfeeds eingeschlossen. Wenn Sie Datenquellen ausschließen möchten, schließen Sie alle Zeilen mit `hit_source = 5,7,8,9`aus.

## Seitenansichten

1. Zählt die Anzahl der Zeilen, in denen sich ein Wert befindet `post_pagename` oder `post_page_url`.

## Besuche

1. Verketten `post_visid_high`, `post_visid_low`, `visit_num`und `visit_start_time_gmt`.
1. Zählen Sie die eindeutige Anzahl der Werte.

> [!NOTE] Internet-Unregelmäßigkeiten, Systemunregelmäßigkeiten oder die Verwendung benutzerspezifischer Besucher-IDs können selten dieselben `visit_num` Werte für verschiedene Besuche verwenden. Verwenden Sie `visit_start_time_gmt` beim Zählen von Besuchen, um sicherzustellen, dass diese Besuche gezählt werden.

## Besucher

Alle Methoden, die Adobe zur Identifizierung individueller Besucher verwendet (benutzerdefinierte Besucher-ID, Experience Cloud ID-Dienst usw.) werden alle letztendlich als Wert in `post_visid_high` und `post_visid_low`. Die Verkettung dieser beiden Spalten kann als Standard zur Identifizierung individueller Besucher verwendet werden, unabhängig davon, wie sie als individueller Besucher identifiziert wurden. Wenn Sie wissen möchten, welche Methode Adobe zur Identifizierung eines Unique Visitors verwendet hat, verwenden Sie die Spalte `post_visid_type`.

1. Verketten `post_visid_high` und `post_visid_low`.
2. Zählen Sie die eindeutige Anzahl der Werte.

## Benutzerspezifische Links, Download- oder Exitlinks

1. Zählt die Anzahl der Zeilen, bei denen:
   * `post_page_event = 100` für benutzerspezifische Links
   * `post_page_event = 101` für Downloadlinks
   * `post_page_event = 102` für Ausstiegslinks

## Benutzerspezifische Ereignisse

Alle Metriken werden in der `post_event_list` Spalte als kommagetrennte Ganzzahlen gezählt. Verwenden Sie diese Option, `event.tsv` um numerische Werte mit dem gewünschten Ereignis abzugleichen. Gibt beispielsweise `post_event_list = 1,200` an, dass der Treffer ein Kaufereignis und ein benutzerdefiniertes Ereignis 1 enthielt.

1. Count the number of times the event lookup value appears in `post_event_list`.

## Besuchszeit

Treffer müssen zunächst nach Besuchen gruppiert und dann nach der Trefferanzahl innerhalb des Besuchs geordnet werden.

1. Verketten `post_visid_high`, `post_visid_low`, `visit_num`und `visit_start_time_gmt`.
2. Sortieren Sie nach diesem verketteten Wert und wenden Sie dann eine sekundäre Sortierung nach `visit_page_num`.
3. Wenn ein Treffer nicht der letzte während eines Besuchs ist, ziehen Sie den `post_cust_hit_time` Wert vom `post_cust_hit_time` Wert des nachfolgenden Treffers ab.
4. Diese Zahl ist die Zeitdauer (in Sekunden) für den Treffer. Filter können angewendet werden, um sich auf Dimensionswerte oder Ereignisse zu konzentrieren.

## Bestellungen, Artikel und Umsatz

Wenn der `currency` Wert eines Treffers nicht mit der Währung einer Report Suite übereinstimmt, wird er mit der Konvertierungsrate dieses Tages konvertiert. Die Spalte `post_product_list` verwendet den konvertierten Währungswert, sodass alle Treffer dieselbe Währung in dieser Spalte verwenden.

1. Exclude all rows where `duplicate_purchase = 1`.
2. Schließen Sie nur Zeilen ein, in denen das Kaufereignis `event_list` enthalten ist.
3. Analysieren Sie die `post_product_list` Spalte, um alle Preisdaten zu extrahieren. Die `post_product_list` Spalte ist genauso formatiert wie die `s.products` Variable.
4. Berechnen Sie die gewünschte Metrik:
   * Anzahl der Zeilen zur Berechnung der Bestellungen
   * Summe der Anzahl der Einheiten `quantity` in der Produktzeichenfolge
   * Summe der Anzahl `price` in der Produktzeichenfolge zur Berechnung des Umsatzes
