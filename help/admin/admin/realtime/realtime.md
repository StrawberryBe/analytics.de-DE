---
description: Zeigt den Webseiten-Traffic an und sortiert die Ansichten der Seite in Echtzeit. Liefert relevante Daten, auf die Sie Ihre Geschäftsentscheidungen stützen können.
title: Echtzeitberichte
topic: Reports
uuid: c09cc605-0b3b-41ab-9b46-8c2a26f579a3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Echtzeitberichte

Zeigt den Webseiten-Traffic an und sortiert die Ansichten der Seite in Echtzeit. Liefert relevante Daten, auf die Sie Ihre Geschäftsentscheidungen stützen können.

>[!NOTE] Für den Echtzeitbericht sind keine zusätzlichen Implementierungen oder Taggings erforderlich. Sie nutzt die vorhandene Implementierung von Adobe Analytics. Informationen zum Konfigurieren von Echtzeitberichten finden Sie unter  [Konfiguration von Echtzeit-Berichten](/help/admin/admin/realtime/t-realtime-admin.md).

**[!UICONTROL Site Metrics]** > **[!UICONTROL Real-Time]**

In Echtzeit werden die folgenden Fragen beantwortet: Was ist der Trend auf meiner Site, und warum? Damit können Sie als Marketingspezialist schnell auf die Performance Ihrer Marketing-Inhalte und -Kampagnen reagieren und diese aktiv verwalten. Die gemeldeten Echtzeit-Daten sind weniger als zwei Minuten zu spät und werden jede Minute automatisch aktualisiert.

![](assets/report-realtime.png)

Das Dashboard umfasst Hochfrequenzmetriken und Site-Analysen von Adobe Analytics, um die Trends im Bereich Traffic und Ansicht von dynamischen Nachrichten- und Einzelhandels-Websites visuell zu verfolgen. Echtzeit versteht Trends in Ihren Daten von Minute zu Minute, innerhalb von Sekunden nach der Erfassung. Es erfasst und streamt Daten in eine automatisch aktualisierte Benutzeroberfläche, wobei eine Echtzeitkorrelation und Verfolgung von Inhalten und Konversionen verwendet wird.

Zwei der am häufigsten verwendeten Anwendungsszenarien sind Herausgeber, die Meldungen bei Änderungen der Aktivität von Benutzern fördern/abstufen möchten, und Marketingexperten, die den Start einer neuen Produktlinie verfolgen möchten.

Als Administrator können Sie

* Erstellen Sie bis zu 3 Echtzeitberichte pro Report Suite, wobei Sie vorhandene Dimensionen oder Classifications und Metriken verwenden. Verwenden Sie die sekundären Dimensionen, um sie mit der primären zu korrelieren (oder zu unterteilen).
* Hinzufügen 3 Dimensionen (oder Classifications) pro Bericht (eine primäre und zwei sekundäre) zusätzlich zu einer Site-weiten Metrik.
* Verwenden Sie ein beliebiges benutzerdefiniertes Ereignis, ein Einkaufswagen-Ereignis oder eine Instanz.
* Ansicht von bis zu 2 Stunden historischen Echtzeitdaten und Änderung dieser Einstellung:

   * Letzte 15 Minuten: Granularität von 1 Minute
   * Letzte 30 Minuten: Granularität von 1 Minute
   * Letzte 1 Stunde: Granularität von 2 Minuten
   * Letzte 2 Stunden: Granularität von 4 Minuten

* Vergleichen Sie beispielsweise die Werte der letzten Woche mit den Werten des letzten Jahres (sowie mit der Gesamtsumme von heute).

Denken Sie daran, dass eVars (Konversionsmetriken) nicht unterstützt werden, da kein Persistenzkonzept besteht. Sie können zwar Konversionsmetriken auswählen, diese funktionieren jedoch nur, wenn sie auf derselben Seite wie die Dimension(en) festgelegt sind. Weitere Informationen finden Sie in der Warnmeldung unter [Einrichten von Echtzeitberichten](/help/admin/admin/realtime/t-realtime-admin.md).

Das Einrichten und Anzeigen von Echtzeitberichten ist auf Administratoren oder andere Benutzer in den Berechtigungsgruppen &quot;Zugriff auf alle Berichte&quot;und &quot;Erweiterter Berichte&quot;beschränkt. In Echtzeit werden jedoch die Berechtigungen berücksichtigt. Wenn Sie z. B. nicht über die Berechtigung zum Anzeigen des Umsatzes verfügen, können Sie keinen Echtzeitbericht mit Umsatzdaten Ansicht haben.

## Datenlatenz als Folge der A4T-Konfiguration  {#section_806CE36354FC4C539A0DED9266A5C704}

Nachdem die A4T-Integration in Adobe Zielgruppe aktiviert wurde, wird eine zusätzliche Latenz von 5-10 Minuten in Adobe Analytics auftreten. Durch diese Erhöhung der Latenz können Daten aus Analytics und Zielgruppe bei demselben Treffer gespeichert werden, sodass Sie Tests nach Seite und Site-Abschnitt unterteilen können.

Diese Steigerung spiegelt sich in allen Adobe Analytics-Diensten und -Tools einschließlich Livestream und Echtzeit-Berichte wider und gilt für die folgenden Szenarien:

* Bei Live-Streams, Echtzeitberichten und API-Anforderungen und aktuellen Daten für Traffic-Variablen werden nur Treffer mit einer zusätzlichen Daten-ID verzögert.
* Bei aktuellen Daten zu Konversionsmetriken, finalisierten Daten und Datenfeeds werden alle Treffer um weitere 5-7 Minuten verzögert.

Achten Sie darauf, dass die Erhöhung der Latenz nach der Implementierung des Identity Service beginnt, auch wenn Sie diese Integration nicht vollständig implementiert haben.
