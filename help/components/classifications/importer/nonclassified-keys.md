---
description: Nicht klassifizierte Schlüssel werden in Classification-Berichten als einzelner Zeileneintrag mit der Bezeichnung "Keine"gruppiert. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.
subtopic: Classifications
title: Nicht klassifizierte Schlüssel
feature: Admin Tools
uuid: b73a9161-0c6f-4c8d-900b-54ab2c36147c
exl-id: 37288c2d-f6f6-4343-87a1-3c3a7b56fe32
translation-type: tm+mt
source-git-commit: f52baf97efe20b209f51108995a0620b6c19bec0
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 61%

---

# Nicht klassifizierte Schlüssel

Nicht klassifizierte Schlüssel werden in Classification-Berichten als einzelner Zeileneintrag mit der Bezeichnung &quot;Keine&quot;gruppiert. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.

## Nicht klassifizierte Schlüssel {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Nicht klassifizierte Schlüssel werden in Classification-Berichten als einzelner Zeileneintrag mit der Bezeichnung *`None`* gruppiert. Benennen Sie *`None`* in eine aussagekräftigere Bezeichnung um.

Angenommen, Ihre Rückverfolgungscodes enthalten Informationen, die den Typ der mobilen Kampagne, mit der der Rückverfolgungscode verknüpft ist, kennzeichnen. Mit einer Classification (Mobilkampagnentyp) gruppieren Sie diese Trackingcodes in Kategorien wie „Mobiles Web“, „iOS-Anwendung“, „Android-Anwendung“ usw. Einige Kampagnen sind nicht als Mobilkampagne ausgelegt und werden daher nicht mit einem Mobilkampagnentyp klassifiziert. Alle nicht klassifizierten Trackingcodes werden unter   *`None`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.

## Umbenennen des Classification-Schlüssels „Keine“ {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

In diesen Schritten wird beschrieben, wie Sie einen nicht klassifizierten Schlüssel, der in den Berichten als *`none`* angezeigt wird, umbenennen.

1. Exportieren Sie mit Hilfe des Importeurs die Classifications in eine lokale Datei.
1. hinzufügen Sie der Datei eine Zeile und geben Sie `~none~` in die Spalte &quot;Schlüssel&quot;ein.
1. Geben Sie in der hinzugefügten Spalte einen beschreibenden Namen in die entsprechende(n) Classification-Spalte(n) ein.

   Um dem Beispiel in dieser Dokumentation zu folgen, können Sie &quot;Nicht-Mobilgeräte-Kampagne&quot;in eine Spalte mit dem Namen [!UICONTROL Mobilgerätetyp] eingeben.

   Mit diesem Eintrag wird   *`None`* in *`non-mobile campaign`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.

   ![Beispiel eines nicht klassifizierten Schlüssels](/help/components/classifications/importer/assets/non-classified-key.png)

1. [Importieren Sie die Daten](/help/components/classifications/importer/import-file.md) wieder in das System.
