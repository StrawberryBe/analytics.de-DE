---
title: manageVars
description: Ändern Sie die Werte mehrerer Analytics-Variablen gleichzeitig.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 100%

---


# Adobe-Plug-in: manageVars

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Mit dem `manageVars`-Plug-in können Sie die Werte mehrerer Analytics-Variablen gleichzeitig bearbeiten. Sie können Werte auch auf Kleinbuchstaben setzen oder unnötige Zeichen gleichzeitig aus mehreren Variablenwerten entfernen. Adobe empfiehlt die Verwendung dieses Plug-ins, wenn Sie den Wert mehrerer Variablen gleichzeitig bereinigen möchten.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: manageVars initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

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

## Verwenden des Plug-ins

Die `manageVars`-Methode verwendet die folgenden Argumente:

* **`cb`** (erforderlich, Zeichenfolge): Der Name einer Callback-Funktion, mit der das Plug-in die Analytics-Variablen bearbeiten kann. Sie können eine Adobe-Funktion wie `cleanStr` oder Ihre eigene benutzerdefinierte Funktion verwenden.
* **`l`** (optional, Zeichenfolge): Eine kommagetrennte Liste der Analytics-Variablen, die Sie bearbeiten möchten. Wenn nicht festgelegt, werden standardmäßig ALLE Adobe Analytics-Variablen bearbeiten. Dazu gehören:
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
   * Alle Listenvariablen
   * Alle Kontextdatenvariablen
* **`Il`** (optional, boolesch): Setzen Sie den Wert auf `false`, wenn Sie die Liste der im `l`-Argument deklarierten Variablen *ausschließen* möchten, anstatt sie einzubeziehen. Die Standardeinstellung ist `true`.

Der Aufruf dieser Methode gibt nichts zurück. Stattdessen werden die Werte der Analytics-Variablen basierend auf der gewünschten Callback-Funktion geändert.

## Beispielaufrufe

### Beispiel 1

Der folgende Code ...

```js
s.manageVars("lowerCaseVars");
```

... ändert die Werte aller oben beschriebenen Variablen in kleingeschriebene Versionen.  Die einzige Ausnahme hiervon ist die Ereignisvariable, da einige der Ereignisse (z. B. scAdd, scCheckout usw.) die Groß-/Kleinschreibung beachten und nicht klein geschrieben werden sollten

### Beispiel 2

Der folgende Code ...

```js
s.manageVars("lowerCaseVars", "events", false);
```

... liefert im Wesentlichen genau dasselbe Ergebnis wie das erste Beispiel, da die Ereignisvariable standardmäßig nicht in Kleinbuchstaben geschrieben wird.

### Beispiel 3

Der folgende Code ...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2");
```

... ändert nur die Werte von eVar1, eVar2, eVar3 und list2 (z. B. in Kleinbuchstaben)

### Beispiel 4

Der folgende Code ...

```js
s.manageVars("lowerCaseVars", "eVar1,eVar2,eVar3,list2", false);
```

... ändert die Werte aller oben beschriebenen Variablen (z. B. in Kleinbuchstaben) AUSSER für eVar1, eVar2, eVar3 und list2

### Beispiel 5

Der folgende Code ...

```js
s.manageVars("cleanStr");
```

... ändert die Werte aller oben beschriebenen Variablen, einschließlich der Ereignisvariablen.  Die cleanStr-Callback-Funktion führt für jeden Variablenwert Folgendes aus:

* Entfernt die HTML-Codierung
* Entfernt Leerzeichen am Anfang und Ende des Werts
* Ersetzt linke/rechte einfache Anführungszeichen (z. B. ‘) mit einem geraden einfachen Anführungszeichen (&#39;)
* Ersetzt Tabulatorzeichen, Zeilenumbruchzeichen und Zeilenumschalterzeichen durch Leerzeichen
* Ersetzt alle doppelten (oder dreifachen usw.) Leerzeichen mit einem Leerzeichen

## Versionsverlauf

### 2.1 (14. Januar 2019)

* Fehlerbehebung für Internet Explorer 11-Browser.
* Änderungen für `s.cleanStr`, es wird jetzt die standardmäßige `cleanStr`-Funktion verwendet.

### 2.0 (7. Mai 2018)

* Zwischenversion (einschließlich einer vollständigen Neuanalyse/Umformulierung des Plug-ins)
* Callback-Funktion `cleanStr` hinzugefügt
