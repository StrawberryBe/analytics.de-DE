---
title: Integrationsmodul
description: Mit dem Integrationsmodul können Adobe-Partner ihre Datenerfassung mit Ihrem Unternehmen integrieren.
exl-id: 378ba77b-be81-49af-8f36-81c65bd01a53
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 98%

---

# Integrationsmodul

Mit dem Integrationsmodul können Adobe-Partner ihre Datenerfassung mit Ihrem Unternehmen integrieren. Diese Integration bietet die Möglichkeit einer Datenverbindung in beide Richtungen. Normalerweise wird die Verwendung des Integrationsmoduls von einem Adobe-Partner gesteuert.

>[!NOTE]
>
>Das Anfordern von Partnerdaten in Ihrer Implementierung kann zu Verzögerungen zwischen dem Laden der Seite und den an die Adobe-Datenerfassungs-Server gesendeten Daten führen. Wenn ein Besucher eine neue Seite lädt, bevor Daten gesendet werden, wird diese Seite nicht aufgezeichnet.

## Arbeitsablauf für Integrationsmodule

1. Ein Besucher Ihrer Site lädt eine Seite, die eine `get`-Anforderung von Partnerdaten auslöst.
2. Der Adobe-Partner erhält die `get`-Anforderung und packt die entsprechenden Variablen in ein JSON-Objekt. Das JSON-Objekt wird zurückgegeben.
3. Ihre Site empfängt das JSON-Objekt und ruft dazu `setVars` auf, um die im JSON-Objekt enthaltenen Informationen Adobe Analytics-Variablen zuzuweisen.
4. An die Adobe-Datenerfassungsserver wird eine Bildanforderung gesendet.

## Implementierung von Integrationsmodulen

Eine Organisation, die mit einem Adobe-Partner zusammenarbeitet, kann diese Schritte verwenden, um erfolgreich mit der Verwendung des Integrationsmoduls zu beginnen.

### Integrationsmodulcode abrufen

Für den Erhalt des Modulcodes ist ein Benutzer mit Produktadministratorzugriff erforderlich, der zu einem Produktprofil mit Zugriff auf den Code-Manager gehört. Die Methode zum Abrufen des Modulcodes ist für alle Implementierungsmethoden gleich, einschließlich Adobe Experience Platform Launch.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
1. Klicken Sie oben rechts auf das 9-Quadrat-Symbol und dann auf das farbige Analytics-Logo.
1. Klicken Sie in der oberen Navigation auf **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Code-Manager]**.
1. Laden Sie die neueste JavaScript AppMeasurement-Bibliothek herunter.
1. Entpacken Sie die Datei nach dem Herunterladen und suchen Sie `AppMeasurement_Module_Integrate.js`.

### Platzieren Sie das Integrationsmodul in Ihrer Implementierung

Für die Implementierung des Integrationsmoduls auf Ihrer Site ist der Zugriff auf Adobe Experience Platform Launch erforderlich. Wenn Sie eine ältere JavaScript-Implementierung verwenden, ist der Zugriff auf den Quellcode der Website Ihres Unternehmens erforderlich.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die Launch-Eigenschaft, die Sie bearbeiten möchten.
3. Klicken Sie auf die Registerkarte „Erweiterungen“ und dann unter „Adobe Analytics“ auf „Konfigurieren“.
4. Öffnen Sie „Tracker mit benutzerdefiniertem Code konfigurieren“ und klicken Sie dann auf „Editor öffnen“.
5. Fügen Sie den Integrationsmodulcode in das modale Codefenster ein. Klicken Sie auf „Nach Abschluss speichern“.

## Integrationsmodulmethoden

Nachdem das Integrationsmodul implementiert wurde, konfigurieren Sie es mit diesen Methoden, um Daten vom gewünschten Adobe-Partner zu senden und zu empfangen.

### add

Die `add`-Methode instanziiert ein Partnerobjekt, das als Zwischenspeicher variabler Daten dient, wenn Daten zwischen Partnersystemen und Ihrer Implementierung freigegeben werden. Diese Methode ist für alle Integrationen erforderlich. Für jeden eindeutigen Partner muss ein separates Partnerobjekt verwendet werden, wenn in einer Implementierung mehrere Partner verwendet werden.

```JavaScript
s.Integrate.add("<partner_name>");
```

Ihr Unternehmen arbeitet normalerweise mit einem Adobe-Partner zusammen, um den Wert für den Partnernamen zu ermitteln.

### Beacon

Die `beacon`-Methode erstellt eine Bildanforderung und verweist sie auf die angegebene URL. Diese Bildanforderungen unterscheiden sich von den Standard-Bildanforderungen. Die Beacon-Methode sendet normalerweise Daten an den Adobe-Partner und nicht an Adobe-Datenerfassungsserver.

```JavaScript
p.beacon("<partner_url>/track?qs1=value1&qs2=value2");
```

Ihr Unternehmen arbeitet normalerweise mit dem Adobe-Partner zusammen, um den Wert für den Partnernamen zu ermitteln. Die Abfragezeichenfolgen in der URL sind optional und vom Partner abhängig. Das Integrationsmodul enthält automatisch eine Abfragezeichenfolge mit einer Zufallszahl, um die Zwischenspeicherung im Browser zu verhindern.

### Verzögerung

Adobe arbeitet intern mit Teams zusammen, um diese Methode zu dokumentieren.

### get

Mit der `get`-Methode kann ein Client Partnervariablen importieren und im Partnerobjekt speichern. Sobald sich die Daten im Partnerobjekt befinden, können sie Analytics-Variablen zugewiesen und in einer Bildanforderung gesendet werden. Diese Methode ruft eine URL auf, die auf ein JSON-Objekt verweist, das die gewünschten Daten enthält.

```JavaScript
s.Integrate.<partner_name>.get("<url_to_json_object>?pid=value1&pid2=value2");
```

* **Name des Partners:** Ihr Unternehmen arbeitet normalerweise mit dem Adobe-Partner zusammen, um den Wert für den Partnernamen zu ermitteln.
* **URL zum JSON-Objekt:** Die URL zu einem JSON-Objekt, das die Partnervariablen enthält, die in eine Bildanforderung eingebunden werden sollen.
* **Abfragezeichenfolgenparameter:** Angaben zum Partnerkonto, die Ihre Organisation im System des Partners identifizieren. Der Adobe-Partner verwendet diese Informationen zur Identifizierung Ihres Datensatzes.

Das Integrationsmodul fügt der URL automatisch weitere Abfragezeichenfolgen hinzu. Eine Var-Abfragezeichenfolge gibt den Namen des JSON-Objekts an, das das Modul vom Partner zurückerwartet. Außerdem wird eine Zufallszahl hinzugefügt, um die Zwischenspeicherung im Browser zu verhindern.

### Bereit

Adobe arbeitet intern mit Teams zusammen, um diese Methode zu dokumentieren.

### useVars

Die `useVars`-Methode ermöglicht es dem Client, Variablenwerte mit einem Adobe-Partner zu teilen.

```JavaScript
s.Integrate.<partner_name>.useVars = function (s,p) {
    p.<partner_var1> = s.eVar1;
    p.<partner_var2> = s.eVar2;
}
```

Ihr Unternehmen arbeitet normalerweise mit einem Adobe-Partner zusammen, um die Werte für den Partnernamen und die Variablen zu ermitteln, die der Partner verwendet.

### setVars

Mit der `setVars`-Methode kann der Client Analytics-Variablen mithilfe der abgerufenen Partnerdaten füllen. Partnerdaten können das Ergebnis einer `get`-Methode, einer statischen Zuweisung oder eines anderen Mechanismus sein, der das Partnerobjekt mit Daten füllt.

```JavaScript
s.Integrate.<partner_name>.setVars = function (s,p) {
    s.eVar1 = p.<partner_var1>;
    s.eVar2 = p.<partner_var2>;
}
```

Ihr Unternehmen arbeitet normalerweise mit einem Adobe-Partner zusammen, um die Werte für den Partnernamen und die Variablen zu ermitteln, die der Partner verwendet.

### script

Mit der `script`-Methode kann ein Adobe-Partner zusätzliche JavaScript-Daten von der Partner-Site aus aufrufen, wenn bestimmte Bedingungen erfüllt sind (z. B. wenn die Kampagnenvariable eingestellt ist).

```JavaScript
p.script("<partner_url>/script?qs1=value1&qs2=value2");
```

Ihr Unternehmen arbeitet normalerweise mit dem Adobe-Partner zusammen, um den Wert für den Partnernamen zu ermitteln. Die Abfragezeichenfolgen in der URL sind optional und vom Partner abhängig. Das Integrationsmodul enthält automatisch eine Abfragezeichenfolge mit einer Zufallszahl, um die Zwischenspeicherung im Browser zu verhindern.
