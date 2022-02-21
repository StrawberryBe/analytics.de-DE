---
description: Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag mit der Bezeichnung „Keine“ gruppiert. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.
title: Nicht klassifizierte Schlüssel
feature: Classifications
exl-id: 37288c2d-f6f6-4343-87a1-3c3a7b56fe32
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 100%

---

# Nicht klassifizierte Schlüssel

Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag mit der Bezeichnung „Keine“ gruppiert. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.

## Nicht klassifizierte Schlüssel {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag mit der Bezeichnung *`None`* gruppiert. Benennen Sie *`None`* in eine aussagekräftigere Bezeichnung um.

Angenommen, Ihre Trackingcodes enthalten Informationen zum Typ der mobilen Kampagne, mit der der Trackingcode verknüpft ist. Mit einer Classification (Mobilkampagnentyp) gruppieren Sie diese Trackingcodes in Kategorien wie „Mobiles Web“, „iOS-Anwendung“, „Android-Anwendung“ usw. Einige Kampagnen sind nicht als Mobilkampagne ausgelegt und werden daher nicht mit einem Mobilkampagnentyp klassifiziert. Alle nicht klassifizierten Trackingcodes werden unter  *`None`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.

## Umbenennen des Classification-Schlüssels „Keine“  {#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

In diesen Schritten wird beschrieben, wie Sie einen nicht klassifizierten Schlüssel, der in den Berichten als *`none`* angezeigt wird, umbenennen.

1. Exportieren Sie mit Hilfe des Importeurs die Classifications in eine lokale Datei.
1. Fügen Sie der Datei eine Zeile hinzu und geben Sie in die Spalte „Schlüssel“ den Wert `~none~` ein.
1. Geben Sie in der hinzugefügten Spalte einen beschreibenden Namen in die entsprechende(n) Classification-Spalte(n) ein.

   Im Beispiel in dieser Dokumentation geben Sie „Nicht-Mobilkampagne“ in die Spalte [!UICONTROL Mobilkampagnentyp] ein.

   Mit diesem Eintrag wird  *`None`* in *`non-mobile campaign`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.

   ![Beispiel eines nicht klassifizierten Schlüssels](/help/components/classifications/importer/assets/non-classified-key.png)

1. [Importieren Sie die Daten](/help/components/classifications/importer/import-file.md) wieder in das System.
