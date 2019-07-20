---
description: Mit den folgenden Variablen und Funktionen können Sie Messaufrufe speichern, wenn die Anwendung offline ist.
keywords: Analytics-Implementierung
seo-description: Mit den folgenden Variablen und Funktionen können Sie Messaufrufe speichern, wenn die Anwendung offline ist.
seo-title: Offline-Verfolgung
solution: Analytics
title: Offline-Verfolgung
topic: Entwickler und Implementierung
uuid: f 7 c 55 aef -28 a 4-4 f 2 f -8 f 47-792 a 05 f 9525 b
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Offline-Verfolgung

Mit den folgenden Variablen und Funktionen können Sie Messaufrufe speichern, wenn die Anwendung offline ist.

>[!NOTE]
>
>Zur Aktivierung der Offline-Verfolgung muss Ihre Report Suite zeitstempelfähig sein. Wenn Zeitstempel für Ihre Report Suite aktiviert sind, `trackOffline`muss Ihre Konfigurationseigenschaft ** wahr sein. Wenn Zeitstempel nicht für Ihre Report Suite aktiviert sind, `trackOffline`muss die Konfigurationseigenschaft ** „false“ lauten. Wenn dies nicht ordnungsgemäß konfiguriert ist, gehen Daten verloren. Wenn Sie sich nicht sicher sind, ob Zeitstempel für Ihre Report Suite aktiviert sind, [wenden Sie sich an den Kundendienst](https://helpx.adobe.com/contact/enterprise-support.ec.html#analytics)

Sofern Offline-AppMeasurement aktiviert ist, verhält es sich folgendermaßen:

* Die Anwendung sendet einen Server-Aufruf, aber es kommt zu einem Fehler bei der Datenübertragung.
* AppMeasurement generiert einen Zeitstempel für den aktuellen Treffer.
* AppMeasurement puffert die Trefferdaten und sichert die gepufferten Trefferdaten im beständigen Speicher, um Datenverlust zu vermeiden.

Bei jedem folgenden Treffer bzw. nach einem durch `offlineThrottleDelay` definierten Intervall versucht AppMeasurement, die gepufferten Trefferdaten zu senden, und bewahrt dabei die ursprüngliche Trefferfolge. Wenn die Datenübertragung fehlschlägt, werden die Trefferdaten weiterhin gepuffert (auch dann, wenn das Gerät offline ist).

<table id="table_E8FD8C89025C4E819FE2FEBC7A78984D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Eigenschaft oder Methode </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>trackOffline </p> </td> 
   <td colname="col2"> <p>Standardeinstellung: Falsch </p> <p>Aktiviert bzw. deaktiviert Offline-Verfolgung für die Measurement Library. </p> <p> <b>Beispiele:</b> </p> 
    <code class="syntax c">s. trackoffline = true; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>offlineLimit </p> </td> 
   <td colname="col2"> <p>Standardeinstellung: keine Begrenzung </p> <p>Maximale Anzahl der in der Warteschlange gespeicherten Treffer.  </p> <p> <b>Beispiele:</b> </p> 
    <code class="syntax c">s. offlinehitlimit = 100; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>offlineThrottleDelay </p> </td> 
   <td colname="col2"> <p>Standardeinstellung: 0 </p> <p>Legt eine Verzögerung in Millisekunden für das Senden von gepufferten Trefferdaten fest, wenn AppMeasurement eine aktive Netzwerkverbindung erkennt. Damit kann beim Senden von mehreren Treffern die Leistungsbeeinträchtigung der Anwendung reduziert werden. </p> <p>Wenn z. B. „offlineThrottleDelay=1000“ festgelegt wurde und das Senden der Trefferdaten 300 ms dauert, wartet AppMeasurement 700 ms bis zum Senden des nächsten gepufferten Treffers. </p> 
    <code class="syntax c">s. offlinethrottledelay = 1000; </code>
  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>forceOnline </p> <p>forceOffline </p> </td> 
   <td colname="col2"> <p> Hiermit wird der Online- bzw. Offline-Zustand des Messungsobjekts manuell festgelegt. Die Bibliothek erkennt automatisch, wann das Gerät offline oder online ist, sodass diese Methoden nur dann benötigt werden, wenn Sie die Offline-Messung erzwingen möchten. <code> forceOnline</code> wird nur verwendet, um zum Onlinezustand zurückzukehren, nachdem der Offlinezustand manuell hergestellt wurde. </p> <p>Wenn die Messung offline ist: </p> 
    <ul id="ul_5A9CFD2968F64F938652C1D779EB7589"> 
     <li id="li_AF074C55DFED4DC8BD8CF3D25805040C"> Wenn <code>trackOffline</code> wahr ist: Treffer werden gespeichert, bis die Messung online ist. </li> 
     <li id="li_6A623377462548DB97C31654EADCFAF3"> Wenn <code>trackOffline</code> falsch ist: Treffer werden verworfen. </li> 
    </ul> <p> <b>Beispiele:</b> </p> 
    <code class="syntax c">s. forceoffline ();

s.forceOnline();
</code> </td>
</tr> 
 </tbody> 
</table>
