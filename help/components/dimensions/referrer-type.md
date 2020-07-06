---
title: Referrer-Typ
description: Der Typ des Werbers, je nachdem, woher der Besucher stammt.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---


# Referrer-Typ

Die Dimension &quot;Werber-Typ&quot;zeigt an, durch welche generischen Kanal Besucher auf Ihre Site geklickt haben, um zu Ihrer Site zu gelangen. Im Gegensatz zu [Marketing-Kanälen](marketing-channel.md), in denen Ihr Unternehmen Regeln für jeden Kanal unterhält, behält Adobe die Regeln für jeden Dimensionswert bei.

## Diese Dimension mit Daten füllen

Diese Dimension verweist auf mehrere Nachschlagetabellen innerhalb von Adobe. Jeder Wert basiert auf dem [Werber](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/admin/internal-url-filter-admin.md)abhängig ist. Vergewissern Sie sich, dass die Dimension &quot;Werber&quot;und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionswerte

Dimensionswerte beinhalten den Typ des Werbers des Treffers. Zu den spezifischen Werten zählen:

* **Eingegeben/mit Lesezeichen versehen**: Für den Treffer liegen keine Daten zum Werber vor.
* **Suchmaschinen**: Der Werber stammt von einer erkannten Suchmaschine, die eine Abfrage mit Suchbegriffen enthält.
* **Soziale Netzwerke:**: Werber-Daten gehörten zu einem von Adobe anerkannten sozialen Netzwerk.
* **Andere Websites**: Werber-Daten gehörten nicht zu einer Suchmaschine oder einem sozialen Netzwerk, das von Adobe erkannt wurde.
* **Festplatte**: Werber stammen aus einer lokalen Kopie einer Webseite auf der Festplatte des Besuchers.
* **E-Mail**: Werber stammen aus einer URL mit einem Protokoll von `imap://` oder `mail://`. Enthält keine Online-E-Mail-Dienste, da diese normalerweise `https://` Protokoll verwenden.

### Soziale Netzwerke

Die folgende Liste bezieht sich auf die Nachschlagetabelle &quot;Social-Netzwerke&quot;, die von Adobe verwendet wird. Adobe stellt diese Liste für Kunden von Adobe Analytics zur Verfügung. Wenn Sie empfehlen möchten, dass Adobe dieser Liste eine Domäne hinzufügt, bitten Sie einen Supportmitarbeiter in Ihrem Unternehmen, sich an den Kundendienst zu wenden.

>[!NOTE]
>
>Diese Liste unterscheidet sich von der standardmäßigen Liste von sozialen Netzwerken in den Verarbeitungsregeln für [Marketing Kanal](../c-marketing-channels/c-rules.md).

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

### Suchmaschinen im Dimensionswert &quot;Sonstige Websites&quot;

Wenn Sie bestimmte Domänen in der Dimension &quot;Werber-Typ&quot;Ansicht haben, können Domänen, die Sie unter &quot;Suchmaschinen&quot;erwarten würden, stattdessen unter &quot;Andere Websites&quot;aufgeführt werden. Sie können beispielsweise `'google.com'` unter &quot;Andere Websites&quot;sehen.

* **Suchmaschinendomänen im Dimensionswert**&quot;Suchmaschinen&quot;: Der Werber erfüllte alle Kriterien, um von Adobe als Suchmaschine zu klassifizieren. Die verweisende Domäne ist eine gültige Suchmaschine *und* die verweisende URL enthält einen Suchbegriff-Zeichenfolgenparameter.
* **Suchmaschinendomänen im Dimensionswert**&quot;Sonstige Websites&quot;: Die verweisende URL erfüllte nicht alle Kriterien, um als Suchmaschine zu klassifizieren. Häufige Beispiele sind Subdomänen, die neben der Suche anderen Funktionen gewidmet sind. Zum Beispiel `mail.google.com` oder `autos.yahoo.com` sind keine Suchmaschinen, sondern befinden sich in einer Domäne der obersten Ebene, die normalerweise mit der Suche verbunden ist. Diese Subdomänen enthalten keine Suchbegriff-Abfrage-Zeichenfolge. Daher werden sie unter &quot;Sonstige Websites&quot;und nicht unter &quot;Suchmaschinen&quot;aufgeführt.
