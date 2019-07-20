---
description: Das getTimeParting-Plug-in füllt benutzerdefinierte Variablen mit Werten für Stunde, Tag der Woche und Wochenende oder Wochentag auf. Analysis Workspace bietet vordefinierte Zeitunterteilungsdimensionen. Das Plug-in sollte verwendet werden, wenn Zeitunterteilungsdimensionen in anderen Analytics-Lösungen außerhalb von Analysis Workspace benötigt werden.
keywords: Analytics-Implementierung
seo-description: Das getTimeParting-Plug-in füllt benutzerdefinierte Variablen mit Werten für Stunde, Tag der Woche und Wochenende oder Wochentag auf. Analysis Workspace bietet vordefinierte Zeitunterteilungsdimensionen. Das Plug-in sollte verwendet werden, wenn Zeitunterteilungsdimensionen in anderen Analytics-Lösungen außerhalb von Analysis Workspace benötigt werden.
seo-title: getTimeParting
solution: Analytics
subtopic: Plug-ins
title: getTimeParting
topic: Entwickler und Implementierung
uuid: 74 f 696 a 3-7169-4560-89 b 2-478 b 3 d 385 e 1
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# getTimeParting

Das getTimeParting-Plug-in füllt benutzerdefinierte Variablen mit Werten für Stunde, Tag der Woche und Wochenende oder Wochentag auf. Analysis Workspace bietet vordefinierte Zeitunterteilungsdimensionen. The plug-in should be used if time parting dimensions are needed in other Analytics solutions, outside of [!UICONTROL Analysis Workspace].

Mit diesem Plug-in werden die Datums- und Uhrzeitinformationen aus den Webbrowsern der Benutzer erfasst. Hierzu werden die Stunde des Tages und der Tag der Woche abgerufen. Anschließend werden diese Daten in die von Ihnen ausgewählte Zeitzone umgewandelt. Dabei wird auch die Sommerzeit berücksichtigt.

>[!NOTE]
>
>Die folgenden Anweisungen erfordern, dass Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Plug-in-Code {#section_1390D6FA53BE4C40B748B0C0AE09C4FA}

**Config Section**

Fügen Sie den folgenden Code in der Datei [!DNL s_code.js] im Abschnitt [!UICONTROL CONFIG SECTION] ein und nehmen Sie die unten beschriebenen erforderlichen Änderungen vor.

`s._tpDST` - ein Array von DST-Werten. The array is structured in the following format: `YYYY:'MM/DD,MM/DD'`

```js
//time parting configuration 
//Australia 
s._tpDST = { 
2012:'4/1,10/7', 
2013:'4/7,10/6', 
2014:'4/6,10/5', 
2015:'4/5,10/4', 
2016:'4/3,10/2', 
2017:'4/2,10/1', 
2018:'4/1,10/7', 
2019:'4/7,10/6'} 
  
//US 
s._tpDST = { 
2012:'3/11,11/4', 
2013:'3/10,11/3', 
2014:'3/9,11/2', 
2015:'3/8,11/1', 
2016:'3/13,11/6', 
2017:'3/12,11/5', 
2018:'3/11,11/4', 
2019:'3/10,11/3'} 
  
//Europe 
s._tpDST = { 
2012:'3/25,10/28', 
2013:'3/31,10/27', 
2014:'3/30,10/26', 
2015:'3/29,10/25', 
2016:'3/27,10/30', 
2017:'3/26,10/29', 
2018:'3/25,10/28', 
2019:'3/31,10/27'}
```

Hinweis für Clients in der nördlichen Halbkugel: Die DST-Werte im Array sind DST-Start, DST-Ende.

Hinweis für Clients in der südlichen Halbkugel: Die DST-Werte im Array sind DST-Ende, DST-Start.

**Parameter**

```js
var tp = s.getTimeParting(h,z);
```

* h = (erforderlich) Halbkugel – Geben Sie an, in welche Halbkugel die Zeit umgerechnet werden soll. Der Wert lautet 'n' oder 's'. Damit wird bestimmt, wie das übergebene DST-Array verwendet wird. Wenn Sie 'n' übergeben, verwendet das Plug-in die Daten, wenn DST aktiviert ist. Wenn Sie 's' übergeben, verwendet das Plug-in die Daten, wenn DST deaktiviert ist.
* z = (optional) Zeitzone – Wenn die Daten auf einem bestimmten Zeitraum basieren sollen, muss dieser Zeitraum als Stundendifferenz zu GMT hier angegeben werden. Beachten Sie, dass dies GMT bei deaktiviertem DST sein sollte. Wenn Sie keinen Wert angeben, wird standardmäßig GMT (also '-5' für US-Ostküstenzeit) verwendet.

**Rückgabe**

Gibt einen verketteten Zeitwert auf Minutenebene mit Wochentag zurück. Beispiel:

```
8:03 AM|Monday
```

Dann können Sie [Classifications](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html) verwenden, um Besuche in Zeiträumen zu gruppieren. Beispiel: Sie können eine Regel im Classification Rule Builder einrichten, um Besuche zwischen 09:00 Uhr und 09:59 Uhr im Zeitraum „09:00–10:00 Uhr“ zu erfassen. Als Alternative zu Classifications könnten Sie zusätzliche clientseitige Logik bereitstellen, um Besuche in JavaScript in Zeiträume einzuteilen.

**Beispielaufruf**

```js
var tp = s.getTimeParting('n','-7'); 
s.prop1 = tp;
```

**Plug-ins SECTION**

Fügen Sie im Abschnitt [!UICONTROL Plug-ins SECTION] in der Datei [!DNL s_code.js] den folgenden Code hinzu.

```js
/* 
 * Plugin: getTimeParting 3.4 
 */ 
s.getTimeParting=new Function("h","z","" 
+"var s=this,od;od=new Date('1/1/2000');if(od.getDay()!=6||od.getMont" 
+"h()!=0){return'Data Not Available';}else{var H,M,D,U,ds,de,tm,da=['" 
+"Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturda" 
+"y'],d=new Date();z=z?z:0;z=parseFloat(z);if(s._tpDST){var dso=s._tp" 
+"DST[d.getFullYear()].split(/,/);ds=new Date(dso[0]+'/'+d.getFullYea" 
+"r());de=new Date(dso[1]+'/'+d.getFullYear());if(h=='n'&&d>ds&&d<de)" 
+"{z=z+1;}else if(h=='s'&&(d>de||d<ds)){z=z+1;}}d=d.getTime()+(d.getT" 
+"imezoneOffset()*60000);d=new Date(d+(3600000*z));H=d.getHours();M=d" 
+".getMinutes();M=(M<10)?'0'+M:M;D=d.getDay();U=' AM';if(H>=12){U=' P" 
+"M';H=H-12;}if(H==0){H=12;}D=da[D];tm=H+':'+M+U;return(tm+'|'+D);}");
```

**Hinweise**

* Testen Sie stets die Installation von Plug-ins, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie sie in die Produktionsumgebung übernehmen.
* Es müssen Konfigurationsvariablen festgelegt werden, damit das Plug-In ordnungsgemäß funktioniert.

