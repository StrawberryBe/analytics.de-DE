---
title: Externes E-Mail-Tracking
description: Verwenden Sie Adobe Analytics, um E-Mail-Inhalte zu verfolgen.
translation-type: tm+mt
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 100%

---


# Externes E-Mail-Tracking

Firmen setzen Analytics ein, um den Erfolg einer E-Mail-Kampagne zu ermitteln.

[!DNL Analytics] kann Berichte mit Analysedaten zu E-Mail-Kampagnen erstellen, die die folgenden Schlüsselmetriken enthalten:

| Metrik | Beschreibung |
|---|---|
| Clickthrough-Rate | Zeigt die Anzahl der Clickthroughs an, die aus der E-Mail auf die Landingpage verfolgt wurden. |
| Käufe und/oder Erfolge | Zeigt die Anzahl der Käufe an, die aus der E-Mail resultierten. |
| Bestellungen | Zeigt die Anzahl der Bestellungen an, die infolge der E-Mail abgegeben wurden. |
| Ertrag | Zeigt den Geldbetrag pro Besuch an, den die E-Mail eingebracht hat. |
| Konversion | Zeigt die Anzahl von Leads, Registrierungen, oder anderer Erfolgsereignisse an, zu denen die E-Mail geführt hat. |

Um die oben genannten Schlüsselmetriken zu erfassen, müssen im HTML-Textteil der E-Mail und in der JavaScript-Bibliothek Änderungen vorgenommen werden.

## Implementierung {#section_8A42A8F4A6CD4A1BAF4B9F99F709AF7A}

Damit in einem Bericht brauchbare Analysedaten zu einer E-Mail-Kampagne angezeigt werden, müssen einige Schritte durchgeführt werden. Diese sehen wie folgt aus:

1. Erstellen Sie eindeutige Trackingcodes.

   Benutzer fragen oft nach Empfehlungen zur Verfolgung einer bestimmten Kampagne. Dies bleibt jedem selbst überlassen. Man sollte sich für die Lösung entscheiden, die am besten funktioniert. Jeder Benutzer ist anders. Adobe empfiehlt, verständliche Trackingcodes zu generieren. Das könnte zum Beispiel so aussehen:

   * sc_cid=A1123A321 > „P“ zeigt eine Partnerkampagne an.
   * sc_cid=EM033007 > „EM“ steht für eine E-Mail-Kampagne.
   * sc_cid=GG987123 > „GG“ steht für „Google“ und zeigt eine kostenpflichtige Suchmaschinenkampagne an.

   Für detaillierte Informationen zur Einrichtung und Verwendung von Trackingcodes wenden Sie sich bitte an Adobe [!DNL Customer Care].

1. Fügen Sie Links in HTML-E-Mails Abfragezeichenfolgenparameter hinzu.

   Um die Clickthroughs des jeweiligen Empfängers und die sich daraus ergebenden Erfolgsereignisse nachverfolgen zu können, muss für jeden in der E-Mail enthaltenen Link ein Abfragezeichenfolgenparameter hinzugefügt werden. Sie können wählen, ob Sie jeden Link einzeln oder alle Links zusammen nachverfolgen möchten. Jeder Link kann über einen eindeutigen Trackingcode verfügen, oder alle Links können den gleichen Code besitzen. Ein Link in einer E-Mail, der zu einer Website führt, könnte zum Beispiel wie folgt aussehen:

   ```js
   <a href="https://www.example.com/index.asp">Visit our home page</a>
   ```

   Mit dem Abfragezeichenfolgenparameter „?sc_cid=112233B“ würde dieser Link wie folgt aussehen:

   ```js
   <a href= "https://www.example.com/index.asp?sc_cid=112233B">Visit our home page</a>
   ```

1. Aktualisieren Sie die JavaScript-Bibliothek.

   Durch Änderungen am Code in der JavaScript-Datei [!DNL s_code.js] können Sie erfassen, wie viele (und welche) Benutzer über die E-Mail auf Ihre Website gelangt sind und an nachfolgenden Erfolgsereignissen beteiligt waren. Das Aktualisieren der JavaScript-Bibliothek erfolgt in zwei Schritten.

   1. Anpassen von [!DNL s_code.js] durch Aufruf von [!UICONTROL getQueryParam]

      Die Datei [!DNL s_code.js] sollte sich auf dem Webserver an einem Speicherort befinden, auf den jede Webseite zugreifen kann. Die Funktion *`doPlugins`* in dieser Datei muss so geändert werden, dass sie die Abfragezeichenfolgenparameter in den E-Mail-Links erfasst. Beispiel:

      ```js
      /* Plugin Config */ 
      s.usePlugins=true 
      function s_doPlugins(s) { 
       /* Add calls to plugins here */ 
       // External Campaigns 
      s.campaign=s.getQueryParam('source') 
      } 
      s.doPlugins=s_doPlugins 
      ```

      Es sollte für jeden Abfragezeichenfolgenparameter, der in eine Variable kopiert werden soll, einen [!UICONTROL getQueryParam]-Aufruf geben. Im oben gezeigten Beispiel wird der Abfragezeichenfolgenparameter [!UICONTROL sc_cid] nach  *`campaign`*.

      Für das Erfassen von Clickthroughs ist nur der erste [!UICONTROL getQueryParam]-Aufruf erforderlich. Wenden Sie sich an Adobe [!DNL Customer Care], wenn Sie diese Funktion implementieren möchten und nicht genau wissen, ob das [!UICONTROL getQueryParam]-Plug-in in Ihrer Version der JavaScript-Datei enthalten ist.

   1. Stellen Sie sicher, dass sich auf allen Landingpages die Tags für Code zum Einfügen von JavaScript befinden. Dieser Code zum Einfügen muss auf die Version von [!DNL s_code.js] verweisen, die im Punkt A modifiziert wurde.

      Beim Aktualisieren der JavaScript-Bibliothek ist auf die folgenden Punkte zu achten Diese Punkte sind unten aufgeführt.

      * Der Abfragezeichenfolgenparameter [!UICONTROL sc_cid] muss in der URL auf der endgültigen Landingpage sichtbar sein, sonst wird keine Clickthrough-Konversion erfasst.
      * Der Parameter [!UICONTROL sc_cid] ist ein Beispiel für einen Abfragezeichenfolgenparameter. Jeder Abfragezeichenfolgenparameter kann verwendet und mit dem [!UICONTROL getQueryParam]-Plug-in erfasst werden. Achten Sie darauf, die Abfragezeichenfolgenparameter nur zur Kampagnenverfolgung einzusetzen. Sobald die Parameter in einer Abfragezeichenfolgen vorhanden sind, werden deren Werte nach  *`campaign`*.

1. Mit [!UICONTROL SAINT] können Sie Kampagnen-Trackingcodes klassifizieren.

   Mit dem [!UICONTROL SAINT-Kampagnenverfolgungstool] können Trackingcodes in leicht verständlichere Namen umgewandelt werden. Das Tool kann auch eingesetzt werden, um die Erfolge jeder E-Mail-Kampagne zusammenzufassen. Die Vorgehensweise zum Einrichten einer E-Mail-Kampagne wird unten in Schritt 5 beschrieben.

1. Anzeigen von Pfaden nach der E-Mail-Kampagne (optional)

   Pfadanalysen nach der E-Mail-Kampagne erfolgen ähnlich wie bei anderen Kampagnen. Auf die folgende Weise können Sie mithilfe einer Variablen die Pfadverläufe nach der Kampagne anzeigen:

   1. Wenden Sie sich an Adobe [!DNL Customer Care], damit das Pathing für eine [!UICONTROL Custom Insight]-Variable (prop) aktiviert wird.

   1. Kopieren Sie auf allen Seiten den Seitennamen in die dafür vorgesehene [!DNL s.prop].
   1. Hängen Sie auf der E-Mail-Landingpage den Namen der E-Mail-Kampagne an die Eigenschaftsvariable an. Das Ergebnis sollte wie folgt aussehen:

      ```js
      s.prop1="Home Page : 123456"
      ```

      Wenn die Pfadfunktion für die [!UICONTROL Custom Insight]-Variable aktiviert ist, können Sie in [!UICONTROL Pfadsetzungsberichten] (wie [!UICONTROL Nächster Seitenfluss] oder [!UICONTROL Trichteranalyse]) erkennen, welche Pfade die Besucher von der Landingpage aus eingeschlagen haben.

