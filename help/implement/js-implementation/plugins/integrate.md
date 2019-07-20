---
title: Integrate-Modul
seo-title: Integrate-Modul für Adobe Analytics
description: Mit dem Integrate-Modul können Adobe-Partner ihre Datenerfassungsbemühungen in Ihr Unternehmen integrieren.
seo-description: Mit dem Integrate-Modul können Adobe-Partner ihre Datenerfassungsbemühungen in Ihr Unternehmen integrieren.
translation-type: tm+mt
source-git-commit: dae73042ace20eded9d0caf690a14203827f903a

---


# Integrate-Modul

Mit dem Integrate-Modul können Adobe-Partner ihre Datenerfassungsbemühungen in Ihr Unternehmen integrieren. Diese Integration bietet eine Zweiwege-Datenverbindung. Normalerweise wird die Verwendung des Integrate-Moduls von einem Adobe-Partner gesteuert.

> [!NOTE] Das Anfordern von Partnerdaten in Ihrer Implementierung kann die Verzögerungen zwischen Seitenladen und Daten erhöhen, die an Adobe-Datenerfassungsserver gesendet werden. Lädt ein Besucher eine neue Seite vor dem Senden der Daten ein, wird diese Seite nicht aufgezeichnet.

## Arbeitsablauf für Integrate-Module

1. A visitor to your site loads a page that initiates a `get` request for partner data.
2. The Adobe partner receives the `get` request and packages the appropriate variables in a JSON object. Das JSON-Objekt wird zurückgegeben.
3. Your site receives the JSON object and calls `setVars` to assign the information contained in the JSON object to Adobe Analytics variables
4. An die Adobe-Datenerfassungsserver wird eine Bildanforderung gesendet.

## Implementierung des Integrate-Moduls

Eine Organisation, die mit einem Adobe-Partner arbeitet, kann diese Schritte verwenden, um das Integrate-Modul erfolgreich zu nutzen.

### Integrate Integrate-Modulcode

Für das Abrufen des Modulcodes ist ein Benutzer mit Produktadministratorzugriff erforderlich, der zu einem Produktprofil mit Zugriff auf den Code-Manager gehört. Die Methode zum Abrufen des Modulcodes ist für alle Implementierungsmethoden identisch, einschließlich der Adobe Experience Platform Launch.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your Adobe ID credentials.
1. Klicken Sie oben rechts auf das 9-quadratische Symbol und dann auf das farbige Analytics-Logo.
1. In the top navigation, click [!UICONTROL Admin] &gt; [!UICONTROL Code Manager].
1. Laden Sie die neueste javascript appmeasurement Library herunter.
1. Once downloaded, unzip the file and locate `AppMeasurement_Module_Integrate.js`.

### Integrieren des Integrate-Moduls in Ihre Implementierung

Für die Implementierung des Integrate-Moduls auf Ihrer Site benötigen Sie Zugriff auf Adobe Experience Platform Launch. Wenn Sie eine Legacy-javascript-Implementierung verwenden, ist der Zugriff auf den Website-Quellcode Ihrer Organisation erforderlich.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your Adobe ID credentials.
2. Klicken Sie auf die Eigenschaft Start, die Sie bearbeiten möchten.
3. Klicken Sie auf die Registerkarte Erweiterungen und dann unter Adobe Analytics auf Konfigurieren.
4. Öffnen Sie Akkordeon "Tracker mit benutzerdefiniertem Code konfigurieren" und klicken Sie dann auf" &lt;/&gt; Editor öffnen" .
5. Fügen Sie den Integrate-Modulcode in das modale Fenster ein. Klicken Sie nach Abschluss des Vorgangs auf Speichern.

## Integrationsmodulmethoden

Sobald das Integrate-Modul implementiert wurde, konfigurieren Sie diese Methoden, um sie zum Senden und Empfangen von Daten vom gewünschten Adobe-Partner zu konfigurieren.

### hinzufügen

The `add` method instantiates a partner object, which serves as an intermediate store of variable data when sharing data between partner systems and your implementation. Diese Methode ist für alle Integrationen erforderlich. Für jeden individuellen Partner muss ein separates Partnerobjekt verwendet werden, wenn mehrere Partner in einer einzelnen Implementierung verwendet werden.

```JavaScript
s.Integrate.add("<partner_name>");
```

Ihr Unternehmen arbeitet in der Regel mit einem Adobe Partner zusammen, um den Wert für den Partnernamen zu ermitteln.

### Beacon

The `beacon` method creates an image request and points it to the specified URL. Diese Bildanforderungen unterscheiden sich von Standardbildanforderungen. Die Beacon-Methode sendet normalerweise Daten an den Adobe-Partner anstelle von Adobe-Datenerfassungsservern.

```JavaScript
p.beacon("<partner_url>/track?qs1=value1&qs2=value2");
```

Ihr Unternehmen arbeitet in der Regel mit dem Adobe Partner zusammen, um den Wert für den Partnernamen festzulegen. In der URL enthaltene Abfragezeichenfolgen sind optional und abhängig vom Partner. Das Integrate-Modul enthält automatisch eine Abfragezeichenfolge mit einer zufallszahl, um die Zwischenspeicherung des Browsers zu verhindern.

### delay

Adobe arbeitet intern mit Teams zusammen, um diese Methode zu dokumentieren.

### get

The `get` method lets a client import partner variables and store them in the partner object. Sobald sich die Daten im Partnerobjekt befinden, kann sie Analytics-Variablen zugewiesen und in einer Bildanforderung gesendet werden. Diese Methode ruft eine URL auf, die auf ein JSON-Objekt mit den gewünschten Daten verweist.

```JavaScript
s.Integrate.<partner_name>.get("<url_to_json_object>?pid=value1&pid2=value2");
```

* **Partnername:** Ihr Unternehmen arbeitet in der Regel mit dem Adobe Partner zusammen, um den Wert für den Partnernamen festzulegen.
* **URL für JSON-Objekt:** Die URL zu einem JSON-Objekt, das die Partnervariablen enthält, die in eine Image-Anforderung aufgenommen werden sollen.
* **Abfragezeichenfolgenparameter:** Partnerkontoinformationen, die Ihre Organisation im System des Partners identifizieren. Der Adobe-Partner verwendet diese Informationen, um Ihren Datensatz zu identifizieren.

Das Integrate-Modul fügt der URL automatisch weitere Abfragezeichenfolgen hinzu. Eine var-Abfragezeichenfolge gibt den Namen des JSON-Objekts an, das das Modul vom Partner zurückgibt. Eine Zufallszahl wird ebenfalls hinzugefügt, um die Zwischenspeicherung des Browsers zu verhindern.

### ready

Adobe arbeitet intern mit Teams zusammen, um diese Methode zu dokumentieren.

### Usevars

The `useVars` method lets the client share variable values with an Adobe partner.

```JavaScript
s.Integrate.<partner_name>.useVars = function (s,p) {
    p.<partner_var1> = s.eVar1;
    p.<partner_var2> = s.eVar2;
}
```

Ihr Unternehmen arbeitet in der Regel mit einem Adobe Partner zusammen, um die Werte für den Partner-Namen und die von Partnern verwendeten Variablen zu bestimmen.

### Setvars

The `setVars` method lets the client populate Analytics variables using partner data retrieved. Partner data can be the result of a `get` method, a static assignment, or any other mechanism that populates the partner object with data.

```JavaScript
s.Integrate.<partner_name>.setVars = function (s,p) {
    s.eVar1 = p.<partner_var1>;
    s.eVar2 = p.<partner_var2>;
}
```

Ihr Unternehmen arbeitet in der Regel mit einem Adobe Partner zusammen, um die Werte für den Partner-Namen und die von Partnern verwendeten Variablen zu bestimmen.

### script

The `script` method lets an Adobe partner to call additional JavaScript from the partner site if certain conditions are met (for example, if the campaign variable is set).

```JavaScript
p.script("<partner_url>/script?qs1=value1&qs2=value2");
```

Ihr Unternehmen arbeitet in der Regel mit dem Adobe Partner zusammen, um den Wert für den Partnernamen festzulegen. In der URL enthaltene Abfragezeichenfolgen sind optional und abhängig vom Partner. Das Integrate-Modul enthält automatisch eine Abfragezeichenfolge mit einer zufallszahl, um die Zwischenspeicherung des Browsers zu verhindern.
