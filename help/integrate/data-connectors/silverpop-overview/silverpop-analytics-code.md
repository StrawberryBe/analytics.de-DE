---
description: 'Wenn Sie die javascript-Plug-In-Datenerfassungsmethode ausgewählt haben, kopieren Sie die folgenden Codezeilen und fügen Sie sie dem Analytics-Code auf Ihren Seiten hinzu. '
seo-description: 'Wenn Sie die javascript-Plug-In-Datenerfassungsmethode ausgewählt haben, kopieren Sie die folgenden Codezeilen und fügen Sie sie dem Analytics-Code auf Ihren Seiten hinzu. '
seo-title: Analytics-Plug-In-Code
title: Analytics-Plug-In-Code
uuid: 534874 bd -49 d 9-4 b 15-8019-b 503 dfcf 3182
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Analytics Plug-In Code{#analytics-plug-in-code}

Wenn Sie die javascript-Plug-In-Datenerfassungsmethode ausgewählt haben, kopieren Sie die folgenden Codezeilen und fügen Sie sie dem Analytics-Code auf Ihren Seiten hinzu:

`/*`

`* Plugin: getQueryParam 2.3`

`*/ s.getQueryParam=new Function("p","d","u","" +"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" +"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" +".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" +"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" +"=p.length?i:i+1)}return v"); s.p_gpv=new Function("k","u","" +"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" +"=s.pt(q,'&','p_gvf',k)}return v"); s.p_gvf=new Function("t","k","" +"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" +"rue':t.substring(i+1);if(p.toLowerCase()==k. oLowerCase())return s." +"epa(v)}return ''");`

`/*in the s_doPlugins function`

`s.campaign=s.getQueryParam("ET_CID"); //places query param value from cid in campaign variable s.eVar2=s.getQueryParam("ET_RID"); //places query param value from rid in eVar2 variable`

>[!NOTE]
>
>Das oben stehende Plug-plugin geht davon aus, dass bestimmte Custom Commerce-Variablen (evars) verfügbar sind. Wenn die im oben genannten Plug-plugin angegebenen Variablen nicht in Ihrer Analytics-Bereitstellung verfügbar sind, ersetzen Sie sie einfach durch die verfügbaren.

