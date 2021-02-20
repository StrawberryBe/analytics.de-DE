---
description: Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung „Keine“. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.
subtopic: Classifications
title: Nicht klassifizierte Schlüssel
topic: Admin tools
uuid: b73a9161-0c6f-4c8d-900b-54ab2c36147c
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 100%

---


# Nicht klassifizierte Schlüssel

Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung „Keine“. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.

## Nicht klassifizierte Schlüssel {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung *`None`*. Benennen Sie *`None`* in eine aussagekräftigere Bezeichnung um.

Angenommen, Ihre Trackingcodes enthalten Informationen zum Typ der mobilen Kampagne, mit der der Trackingcode verknüpft ist. Mit einer Classification (Mobilkampagnentyp) gruppieren Sie diese Trackingcodes in Kategorien wie „Mobiles Web“, „iOS-Anwendung“, „Android-Anwendung“ usw. Einige Kampagnen sind nicht als Mobilkampagne ausgelegt und werden daher nicht mit einem Mobilkampagnentyp klassifiziert. Alle nicht klassifizierten Trackingcodes werden unter   *`None`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.

## Umbenennen des Classification-Schlüssels „Keine“ {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

In diesen Schritten wird beschrieben, wie Sie einen nicht klassifizierten Schlüssel, der in den Berichten als *`none`* angezeigt wird, umbenennen.

1. Exportieren Sie mit Hilfe des Importeurs die Classifications in eine lokale Datei.
1. Fügen Sie eine Zeile zur Datei hinzu und geben Sie in die Spalte „Schlüssel“ den Wert [!DNL ~keine~] ein.
1. Geben Sie in der hinzugefügten Spalte einen beschreibenden Namen in die entsprechende(n) Classification-Spalte(n) ein.

   Im Beispiel in dieser Dokumentation geben Sie „Nicht-Mobilkampagne“ in die Spalte [!UICONTROL Mobilkampagnenname] ein.

   Mit diesem Eintrag wird   *`None`* in *`non-mobile campaign`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.
1. [Importieren Sie die Daten](/help/components/classifications/importer/import-file.md) wieder in das System.
