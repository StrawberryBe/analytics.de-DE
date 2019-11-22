---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# transactionID

[!UICONTROL Integration-Data Sources] verwenden eine [!UICONTROL Transaktions-ID], um Offlinedaten mit einer Onlinetransaktion (z. B. Leads oder online generierte Einkäufe) zu verknüpfen.


<!-- 

transactionID.xml

 -->

Jede eindeutige an Adobe gesendete *`transactionID`* wird bei der Vorbereitung eines [!UICONTROL Data Sources]-Uploads von Offlineinformationen zu dieser Transaktion aufgezeichnet. Siehe [Data Sources](https://marketing.adobe.com/resources/help/en_US/sc/datasources/).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | xact | Keine | "" |

**Aktivieren des Transaktions-ID-Speichers** {#section_3EA2C9DC9D4C4F0FBE4AB67981BCB52E}

Bevor *`transactionID`*-Werte aufgezeichnet werden, muss [!UICONTROL Transaktions-ID-Speicherung] für die im Report Suite Manager ausgewählte Report Suite aktiviert sein. Diese Einstellung nehmen Sie hier vor:

```
Analytics > Admin > Report Suites > Edit Settings > General > General Account Settings.
```

Ob bei einer Report Suite *`transactionID Storage`* aktiviert ist, sehen Sie hier:

```
Analytics > Admin > Data Sources > Manage
```

**Syntax und mögliche Werte** {#section_0C18329203DC45E989DBAE70C0FB4801}

```js
s.transactionID="unique_id"
```

*`transactionID`* sollte nur alphanumerische Zeichen enthalten. Wenn bei einem einzelnen Treffer mehrere [!UICONTROL transactionIDs] aufgezeichnet werden sollen, können Sie die einzelnen Werte mit einem Komma voneinander trennen.

**Beispiele** {#section_A4C1F0E54CB54AD7B86A22147E9B5FEF}

```js
s.transactionID="11123456"
```

```js
s.transactionID="lead_12345xyz"
```

```js
s.transactionID=s.purchaseID
```

**Probleme, Fragen und Tipps** {#section_4299BAD5D0154DBC88A9EF0E2C252BB4}

* Wenn die *`transactionID`*-Aufzeichnung nicht aktiviert ist, werden *`transactionID`*-Werte verworfen und stehen für die Verwendung mit [!UICONTROL Integrationsdatenquellen] nicht zur Verfügung. Stellen Sie sicher, dass auf der Seite, auf der *`transactionID`* gesetzt ist, eine Konversionsvariable oder ein Ereignis (eVar bzw. Ereignisvariable) festgelegt ist. Andernfalls werden keine Daten für *`transactionID`* aufgezeichnet.

* Wenn Sie [!UICONTROL transactionIDs] für mehrere Systeme wie Einkäufe und Interessenten aufzeichnen, stellen Sie sicher, dass der Wert in *`transactionID`* immer eindeutig ist. Zu diesem Zweck können Sie der ID eine entsprechende Zeichenfolge voranstellen (z. B. „Lead_1234“ oder „Einkauf_1234“). [!UICONTROL Integrationsdatenquellen] funktionieren nicht wie erwartet ([!UICONTROL Datenquellen]-Daten werden an die falschen Daten gebunden), wenn eine eindeutige *`transactionID`* zweimal erfasst wird.

* Standardmäßig werden *`transactionID`*-Werte 90 Tage lang gespeichert. Wenn die Offline-Interaktion länger als 90 Tage dauert, lassen Sie diese Zeitspanne vom Kundendienst verlängern.

> [!NOTE] Die Variable *`transactionID`* kann jedes beliebige Zeichen außer einem Komma enthalten. Sie sollte sich an der gleichen Stelle befinden, an der die Zeichenbegrenzung (100 Byte) angegeben ist. Bei Verwendung von Multi-Byte-Zeichen muss Multi-Byte-Zeichen-Unterstützung aktiviert werden, damit es nicht zu Problemen kommt, weil unerwartete Zeichen in *`transactionID`*.
