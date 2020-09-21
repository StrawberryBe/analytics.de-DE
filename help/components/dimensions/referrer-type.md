---
title: Referrer-Typ
description: Der Typ des Referrers, je nachdem, woher der Besucher stammt.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '423'
ht-degree: 100%

---


# Referrer-Typ

Die Dimension „Referrer-Typ“ gibt an, durch welche generischen Kanal Besucher geklickt haben, um zu Ihrer Site zu gelangen. Im Gegensatz zu [Marketing-Kanälen](marketing-channel.md), bei denen Ihre Organisation Regeln für jeden Kanal verwaltet, verwaltet Adobe die Regeln für jedes Dimensionselement.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf mehrere interne Suchtabellen von Adobe. Jeder Wert basiert auf dem [Referrer](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/admin/internal-url-filter-admin.md) abhängig ist. Vergewissern Sie sich, dass die Dimension „Referrer“ und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionselemente

Zu den Dimensionselementen gehören die Typen der Referrer des Treffers. Zu den spezifischen Werten gehören die folgenden:

* **Eingegeben/mit Lesezeichen versehen**: Für den Treffer liegen keine Daten zum Referrer vor.
* **Suchmaschinen**: Der Referrer kam von einer anerkannten Suchmaschine, die eine Abfragezeichenfolge mit Suchbegriffen enthält.
* **Soziale Netzwerke**: Die Referrer-Daten gehörten zu einem von Adobe anerkannten sozialen Netzwerk.
* **Andere Websites**: Die Referrer-Daten gehörten nicht zu einer Suchmaschine oder einem sozialen Netzwerk, die/das von Adobe erkannt wird.
* **Festplatte**: Der Referrer stammt von einer lokalen Kopie einer Webseite auf der Festplatte des Besuchers.
* **E-Mail**: Der Referrer stammt aus einer URL mit einem `imap://`- oder `mail://`-Protokoll. Dies umfasst keine Online-E-Mail-Dienste, da diese normalerweise ein `https://`-Protokoll verwenden.

### Soziale Netzwerke

Die folgende Liste verweist auf die von Adobe verwendete Suchtabelle „Soziale Netzwerke“. Adobe stellt diese Liste den Kunden von Adobe Analytics zur Verfügung. Wenn Sie empfehlen möchten, dass Adobe dieser Liste eine Domäne hinzufügt, bitten Sie einen Support-Mitarbeiter in Ihrem Unternehmen, sich an die Kundenunterstützung zu wenden.

>[!NOTE]
>
>Diese Liste unterscheidet sich von der standardmäßigen Liste von sozialen Netzwerken in den [Verarbeitungsregeln für Marketing-Kanäle](../c-marketing-channels/c-rules.md).

* `12seconds.tv`
* `t.163.com`
* `4travel.jp`
* `advogato.org`
* `ameba.jp`
* `anobii.com`
* `asmallworld.net`
* `avforums.com`
* `backtype.com`
* `badoo.com`
* `bebo.com`
* `bigadda.com`
* `bigtent.com`
* `biip.no`
* `blackplanet.com`
* `blogspot.com`
* `blogster.com`
* `blomotion.jp`
* `bolt.com`
* `brightkite.com`
* `buzznet.com`
* `cafemom.com`
* `care2.com`
* `classmates.com`
* `cloob.com`
* `collegeblender.com`
* `cyworld.co.kr`
* `cyworld.com.cn`
* `dailymotion.com`
* `yozm.daum.net`
* `delicious.com`
* `deviantart.com`
* `digg.com`
* `diigo.com`
* `disqus.com`
* `draugiem.lv`
* `facebook.com`
* `faceparty.com`
* `fc2.com`
* `flickr.com`
* `flixster.com`
* `fotolog.com`
* `foursquare.com`
* `friendfeed.com`
* `friendsreunited.com`
* `friendsreunited.co.uk`
* `friendster.com`
* `fubar.com`
* `gaiaonline.com`
* `geni.com`
* `goodreads.com`
* `plus.google.com`
* `plus.url.google.com`
* `grono.net`
* `habbo.com`
* `hatena.ne.jp`
* `t.hexun.com`
* `hi5.com`
* `hyves.nl`
* `ibibo.com`
* `identi.ca`
* `t.ifeng.com`
* `imeem.com`
* `hotnews.infoseek.co.jp`
* `instagram.com`
* `intensedebate.com`
* `irc-galleria.net`
* `iwiw.hu`
* `jaiku.com`
* `kaixin001.com`
* `kaixin002.com`
* `kakaku.com`
* `kanshin.com`
* `kozocom.com`
* `last.fm`
* `linkedin.com`
* `livejournal.com`
* `lnkd.in`
* `me2day.net`
* `meetup.com`
* `mister-wong.com`
* `mixi.jp`
* `mixx.com`
* `mouthshut.com`
* `multiply.com`
* `mumsnet.com`
* `myheritage.com`
* `mylife.com`
* `myspace.com`
* `myyearbook.com`
* `nasza-klasa.pl`
* `matome.naver.jp`
* `netlog.com`
* `nettby.no`
* `netvibes.com`
* `nextdoor.com`
* `nicovideo.jp`
* `ning.com`
* `odnoklassniki.ru`
* `ok.ru`
* `orkut.com`
* `pakila.jp`
* `t.people.com.cn`
* `photobucket.com`
* `pinterest.com (and all international domains)`
* `plaxo.com`
* `plurk.com`
* `po.st`
* `t.qq.com`
* `mp.weixin.qq.com`
* `boards.qwant.com`
* `reddit.com`
* `renren.com`
* `blog.seesaa.jp`
* `t.sina.com.cn`
* `skyrock.com`
* `slideshare.net`
* `smcb.jp`
* `smugmug.com`
* `t.sohu.com`
* `sonico.com`
* `studivz.net`
* `stumbleupon.com`
* `t.co`
* `tabelog.com`
* `tagged.com`
* `taringa.net`
* `thefancy.com`
* `toutiao.com`
* `tripit.com`
* `trombi.com`
* `trytrend.jp`
* `tuenti.com`
* `tumblr.com`
* `twine.com`
* `twitter.com`
* `uhuru.jp`
* `viadeo.com`
* `vimeo.com`
* `vk.com`
* `wayn.com`
* `weibo.com`
* `weourfamily.com`
* `wer-kennt-wen.de`
* `wordpress.com`
* `xanga.com`
* `xing.com`
* `answers.yahoo.com`
* `yammer.com`
* `yaplog.jp`
* `yelp.com`
* `yelp.co.uk`
* `youku.com`
* `youtube.com`
* `yuku.com`
* `zooomr.com`
* `zhihu.com`

### Suchmaschinen im Dimensionselement „Andere Websites“

Wenn Sie bestimmte Domänen in der Dimension „Referrer-Typ“ anzeigen, kann es vorkommen, dass Domänen, die Sie unter „Suchmaschinen“ erwarten würden, stattdessen unter „Andere Websites“ aufgeführt sind. Beispielsweise sehen Sie möglicherweise `'google.com'` unter „Andere Websites“.

* **Suchmaschinendomänen im Dimensionselement „Suchmaschinen“**: Der Referrer erfüllte alle Kriterien, um von Adobe als Suchmaschine klassifiziert zu werden. Die Referrer-Domäne ist eine gültige Suchmaschine *und* die Referrer-URL enthält einen Abfragezeichenfolgenparameter für Suchbegriffe.
* **Suchmaschinendomänen im Dimensionselement „Andere Websites“**: Die Referrer-URL erfüllte nicht alle Kriterien, um als Suchmaschine klassifiziert zu werden. Häufige Beispiele sind Unterdomänen, die neben der Suche anderen Funktionen gewidmet sind. Zum Beispiel sind `mail.google.com` und `autos.yahoo.com` keine Suchmaschinen, sondern befinden sich in einer Domäne auf oberster Ebene, die normalerweise mit der Suche verbunden ist. Diese Unterdomänen enthalten keine Abfragezeichenfolge für Suchbegriffe. Daher werden sie unter „Andere Websites“ und nicht unter „Suchmaschinen“ aufgeführt.
