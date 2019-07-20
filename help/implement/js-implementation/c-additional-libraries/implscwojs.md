---
description: Analytics mithilfe von HTML-Bild-Tags implementieren (fest codierte Bildanforderung).
keywords: Analytics-Implementierung; html image tag; fest programmierte Bildanforderung
seo-description: Analytics mithilfe von HTML-Bild-Tags implementieren (fest codierte Bildanforderung).
seo-title: Analytics mithilfe von HTML-Bild-Tags implementieren
solution: Analytics
title: Analytics mithilfe von HTML-Bild-Tags implementieren
topic: Entwickler und Implementierung
uuid: 0 c 98 a 57-7 c 71-4362-812 c -36 e 37848 a 5 ae ae
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Analytics mithilfe von HTML-Bild-Tags implementieren

Analytics mithilfe von HTML-Bild-Tags implementieren (fest codierte Bildanforderung).

Dieses Bild wird dann vom Browser angefordert. Bei der Anforderung dieses Bildes werden über Variablen in der Abfragezeichenfolge der Bildanforderung Daten transportiert. Das JavaScript fasst Browservariable mit Seitenvariablen zusammen, um eine umfassende Datenerfassung zu ermöglichen. In einigen Fällen ist ein Bild-Tag angebracht, das komplett serverseitig erstellt wird. Eine JavaScript-basierte Implementierung enthält die folgenden Standardelemente:

<table id="table_20BBE4387F234CF199E6C99741AF265C"> 
 <tbody> 
  <tr> 
   <td> HTML-Code </td> 
   <td> Dieser Teil besteht aus JavaScript-Code, der sich in HTML-Seiten (oder Vorlagen) befindet, in dem der Wert von JavaScript-Variablen festgelegt wird. </td> 
  </tr> 
  <tr> 
   <td> JavaScript-Bibliothek </td> 
   <td> <p>Diese Datei enthält gewöhnlichen Code zum: </p> 
    <ul id="ul_ED50D66F2B2B476E8D9063099995998D"> 
     <li id="li_E88F6F28EC8946469ADCEAFF2F0A4EBA">Abfragen des Browsers hinsichtlich verschiedener Eigenschaften, wie JavaScript-Version, BS-Version, Größe und Auflösung des verwendeten Bildschirms und anderer Variablen. </li> 
     <li id="li_5CEBE37709D943B7921447FA7054A565">Kodieren und Verketten aller Variablen zu einer Bildanforderung(&lt;img&gt;), über die diese Variablen zu den Datenerfassungsservern gelangen. Dann wird auf eine JavaScript-Bibliotheksdatei verwiesen, die geladen und ausgeführt wird. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> &lt;noscript&gt;-Tag </td> 
   <td> Eine vereinfachte Version der Bildanforderung wird in einem &lt;noscript&gt;-Tag platziert, das ausgeführt wird, wenn JavaScript beim Benutzer deaktiviert oder nicht vorhanden ist. Dieser Teil der Implementierung ist optional und nur an rund 2 % der Internetnutzer gerichtet. </td> 
  </tr> 
 </tbody> 
</table>

JavaScript kann Browsereinstellungen ermitteln, auf die der Server keinen Zugriff hat, wie Höhe und Breite des Browser-Fensters, Bildschirmauflösung und Netscape-Plug-ins. Bei Einsatz einer serverseitigen Methode zur Erstellung eines Bild-Tags können diese Variablen nicht erfasst werden. Das JavaScript legt in der Bildanforderung eine Zufallszahl fest, um eine Zwischenspeicherung im Browser und auf dem Proxyserver zu verhindern. Dadurch wird es möglich, alle Seitenansichten genau nachzuverfolgen. Unter bestimmten Umständen hat serverseitiger Code Vorteile gegenüber JavaScript-basiertem Code, wie zum Beispiel:

* JavaScript ist sehr genau (98 bis 100 %). Manchmal ist eine höchstmögliche Genauigkeit gefragt, selbst in Situationen, in denen Benutzer schnell auf eine andere Seite weiterklicken, bevor das JavaScript ausgeführt wurde. Durch eine serverseitige Erstellung des Bild-Tags wird die Genauigkeit um einige Prozentpunkte gesteigert.
* Für die Nachverfolgung von Konversionsereignissen wie Einkäufen, in denen die Genauigkeit besonders wichtig ist.
* Diese Strategie kann auch verwendet werden, um die Bildanforderung vollständig in der <noscript> für die Verfolgung von Benutzern ohne javascript oder mit deaktiviertem javascript.

>[!NOTE]
>
>Die Verwendung von servergenerierten Image-Tags erfordert die Implementierung und ist schwieriger zu debuggen, bereitzustellen und zu warten. Adobe empfiehlt Kunden daher, bei jeder Seite wenn möglich eine JavaScript-basierte Datenerfassung zu bevorzugen. Bei Wahl dieser Implementierungsmethode werden verschiedene Berichte und Funktionen – wie Besucherklickzuordnung, Download-Links, Exitlinks und browserbasierte Variablen (Browserbreite, -höhe usw.) – nicht unterstützt oder können nicht erfasst werden.

