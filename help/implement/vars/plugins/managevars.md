---
title: 'manageVars  '
description: Ändern Sie die Werte mehrerer Analytics-Variablen gleichzeitig.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Adobe-Plug-in: manageVars

> [!IMPORTANT] Dieses Plug-in wird von Adobe Consulting bereitgestellt, um Ihnen zu helfen, aus Adobe Analytics mehr Nutzen zu ziehen. Der Adobe-Kundendienst bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe zu diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater für Hilfe arrangieren.

Mit dem `manageVars` Plug-in können Sie die Werte mehrerer Analytics-Variablen gleichzeitig bearbeiten. Sie können Werte auch in Kleinbuchstaben festlegen oder unnötige Zeichen gleichzeitig aus mehreren Variablenwerten entfernen. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie den Wert mehrerer Variablen gleichzeitig bereinigen möchten.

## Installieren Sie das Plug-In mit der Adobe Experience Platform Launch-Erweiterung

Adobe Angebots ist eine Erweiterung, mit der Sie am häufigsten verwendete Plug-ins verwenden können.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Catalog] Schaltfläche
1. Installieren und Veröffentlichen der [!UICONTROL Common Analytics Plugins] Erweiterung
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung &quot;Plug-ins initialisieren&quot;mit der folgenden Konfiguration:
   * Bedingung: Keines
   * Ereignis: Core - Bibliothek geladen (Seitenanfang)
1. Hinzufügen Sie eine Aktion mit der folgenden Konfiguration auf die oben stehende Regel:
   * Erweiterung: Allgemeine Analytics-Plugins
   * Aktionstyp: Initialisieren von manageVars
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-Ins mit dem Editor für benutzerdefinierten Code starten

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerspezifischen Code verwenden.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Wechseln Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter der Adobe Analytics-Erweiterung.
1. Erweitern Sie das [!UICONTROL Configure tracking using custom code] Akkordeon, das die [!UICONTROL Open Editor] Schaltfläche einblendet.
1. Öffnen Sie den benutzerdefinierten Code-Editor und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen in der Analytics-Erweiterung.

## Plug-In mit AppMeasurement installieren

Kopieren Sie den folgenden Code an einer beliebigen Stelle in der AppMeasurement-Datei, nachdem das Analytics-Verfolgungsobjekt instanziiert wurde (unter Verwendung [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: manageVars v2.1 (Requires pt plug-in and other necessary callback plug-ins) */
s.manageVars=function(cb,l,il){var s=this;if(!s[cb])return!1;l=l||"";il=il||!0;var a,d="pageName,purchaseID,channel,server, pageType,campaign,state,zip,events,products,transactionID";for(a=1;76>a;a++)d+=",prop"+a;for(a=1;251>a;a++)d+=",eVar"+a;for(a=1;6>a;a++)d+=",hier"+a;for(a=1;4>a;a++)d+=",list"+a;for(a in s.contextData)d+=",contextData."+a;if(l){if(1==il)d=l.replace("['", ".").replace("']","");else if(0==il){l=l.split(",");il=d.split(",");d="";for(x in l)for(y in-1<l[x].indexOf("contextData")&& (l[x]="contextData."+l[x].split("'")[1]),il)l[x]===il[y]&&(il[y]="");for(y in il)d+=il[y]?","+il[y]:""}s.pt(d,",",cb,0);return!0} return""===l&&il?(s.pt(d,",",cb,0),!0):!1};

/* Adobe Consulting Plugin: lowerCaseVars for manageVars (Requires manageVars plug-in) */
s.lowerCaseVars=function(v){var s=this;s[v]&&("events"!==v&&-1===v.indexOf("contextData")?(s[v]=s[v].toString(),0!== s[v].indexOf("D=")&&(s[v]=s[v].toLowerCase())):-1<v.indexOf("contextData")&&(v=v.substring(v.indexOf(".")+1),s.contextData[v]&& (s.contextData[v]=s.contextData[v].toString().toLowerCase())))};

/* Adobe Consulting Plugin: cleanStr for manageVars (Requires manageVars and cleanStr plug-ins) */
s.cleanStr=function(v){var s=this;s[v]&&"function"!==typeof cleanStr&&(0>v.indexOf("contextData")?s[v]=cleanStr(s[v]): (v=v.substring(v.indexOf(".")+1),s.contextData[v]&&(s.contextData[v]=cleanStr(s.contextData[v].toString()))))};

/* Adobe Consulting Plugin: cleanStr v1.0 */
function cleanStr(str){if("string"===typeof str){str=str.replace(/<\/?[^>]+(>|$)/g,"").trim().replace(/[\u2018\u2019\u201A]/g, "'").replace(/\t+/g,"").replace(/[\n\r]/g," ");for(;-1<str.indexOf("  ");)str=str.replace(/\s\s/g," ");return str}return""};

/* Adobe Consulting Plugin: pt v2.01 */
s.pt=function(l,de,cf,fa){if(l&&this[cf]){l=l.split(de||",");de=l.length;for(var e,c=0;c<de;c++)if(e=this[cf](l[c],fa))return e}};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Plug-In verwenden

Die `manageVars` Methode verwendet die folgenden Argumente:

* **`cb`** (erforderlich, Zeichenfolge): Der Name einer Rückruffunktion, mit der das Plug-In die Analytics-Variablen bearbeiten kann. Sie können eine Adobe-Funktion wie `cleanStr` oder Ihre eigene benutzerdefinierte Funktion verwenden.
* **`l`** (optional, Zeichenfolge): Eine kommagetrennte Liste von Analytics-Variablen, die Sie bearbeiten möchten. Standardmäßig werden ALLE Adobe Analytics-Variablen verwendet, wenn sie nicht festgelegt sind. Dazu gehören:
   * `pageName`
   * `purchaseID`
   * `channel`
   * `server`
   * `pageType`
   * `campaign`
   * `state`
   * `zip`
   * `events`
   * `products`
   * `transactionID`
   * Alle Props
   * Alle eVars
   * Alle Hierarchievariablen
   * Alle Listen
   * Alle Kontextdatenvariablen
* **`Il`** (optional, boolean): Auf `false` , wenn Sie die Liste der im *Argument deklarierten Variablen* ausschließen `l` möchten, anstatt sie einzubeziehen. Die Standardeinstellung ist `true`.

Der Aufruf dieser Methode gibt nichts zurück. Stattdessen werden die Werte der Analytics-Variablen basierend auf der gewünschten Rückruffunktion geändert.

## Beispielaufrufe

### Beispiel 1

Der folgende Code...

```js
s.manageVars("lowerCaseVars");
```

...ändert die Werte aller oben beschriebenen Variablen in kleinere Versionen.  Die einzige Ausnahme hiervon ist die Variable &quot;Ereignisses&quot;, wie einige der Ereignis (z. B. scAdd, scCheckout usw.) die Groß-/Kleinschreibung beachten und nicht herabgesetzt werden sollten

### Beispiel 2

Der folgende Code...

```js
s.manageVars("lowerCaseVars", "events", false);
```

...führt im Wesentlichen zum exakt gleichen Ergebnis wie im ersten Beispiel, da die Variable &quot;Ereignisses&quot;nicht standardmäßig verringert wird.

### Beispiel 3

Der folgende Code...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2");
```

...ändert sich (z. B. in Kleinbuchstaben) nur die Werte von eVar1, eVar2, eVar3 und Liste2

### Beispiel 4

Der folgende Code...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2", false);
```

...ändert (z. B. in Kleinbuchstaben) die Werte aller oben beschriebenen Variablen außer für eVar1, eVar2, eVar3 und Liste2

### Beispiel 5

Der folgende Code...

```js
s.manageVars("cleanStr");
```

...ändert die Werte aller oben beschriebenen Variablen, einschließlich der Ereignis-Variablen.  Die cleanStr-Rückruffunktion führt für jeden Variablenwert Folgendes aus:

* Entfernt die HTML-Kodierung
* Entfernt Leerzeichen am Anfang und Ende des Werts
* Ersetzt linke/rechte einfache Anführungszeichen (z. B. &quot;) mit einem einfachen einfachen einfachen Anführungszeichen (&quot;)
* Ersetzt TabTabZeichen, Zeilenumbruch- und Wagenrücklaufzeichen durch Leerzeichen
* Ersetzt alle Dubletten (oder Dreifache usw.) Leerzeichen mit Leerzeichen

## Versionsverlauf

### 2.1 (14. Januar 2019)

* Fehlerbehebung für Internet Explorer 11-Browser.
* Änderungen für `s.cleanStr`, die jetzt die normale `cleanStr` Funktion verwenden.

### 2.0 (7. Mai 2018)

* Point Release (einschließlich vollständiger Neuanalyse/Umschreiben des Plugins)
* Rückruffunktion `cleanStr` hinzugefügt
