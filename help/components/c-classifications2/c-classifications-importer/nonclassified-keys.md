---
description: Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung „Keine“. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.
seo-description: Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung „Keine“. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.
seo-title: Nicht klassifizierte Schlüssel
solution: Analytics
subtopic: Classifications
title: Nicht klassifizierte Schlüssel
topic: Admin Tools
uuid: b 73 a 9161-0 c 6 f -4 c 8 d -900 b -54 ab 2 c 36147 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Nicht klassifizierte Schlüssel

Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung „Keine“. Benennen Sie „Keine“ in eine aussagekräftigere Bezeichnung um.

## Non-classified keys {#concept_233E51DDF3084FF7B7EA89381C73C5FF}

Nicht klassifizierte Schlüssel werden in Classification-Berichten unter einem einzigen Zeileneintrag gruppiert; dieser Zeileneintrag trägt die Bezeichnung *`None`*. It can be useful to rename *`None`* to something more descriptive.

Angenommen, Ihre Trackingcodes enthalten Informationen zum Typ der mobilen Kampagne, mit der der Trackingcode verknüpft ist. Mit einer Classification (Mobilkampagnentyp) gruppieren Sie diese Trackingcodes in Kategorien wie „Mobiles Web“, „iOS-Anwendung“, „Android-Anwendung“ usw. Einige Kampagnen sind nicht als Mobilkampagne ausgelegt und werden daher nicht mit einem Mobilkampagnentyp klassifiziert. Alle nicht klassifizierten Trackingcodes werden unter *`None`* im Bericht [!UICONTROL Mobilkampagnentyp] umbenannt.

## Umbenennen des Classification-Schlüssels „Keine“{#task_8CD595DA82AA44D08CEF002B588C3C30}

<!-- 

t_rename_classification_none.xml

 -->

Steps that describe how to rename a non-classified key that displays as *`none`* in reporting.

1. Exportieren Sie mit Hilfe des Importeurs die Classifications in eine lokale Datei.
1. Add a row to the file, and type [!DNL ~none~] in the Key column.
1. Geben Sie in der hinzugefügten Spalte einen beschreibenden Namen in die entsprechende(n) Classification-Spalte(n) ein. 

   Im Beispiel in dieser Dokumentation geben Sie „Nicht-Mobilkampagne“ in die Spalte [!UICONTROL Mobilkampagnenname] ein.

   Mit diesem Eintrag wird *`None`* im *`non-mobile campaign`*[!UICONTROL Mobilkampagnentyp-] Bericht.
1. [Importieren Sie die Daten](../../../components/c-classifications2/c-classifications-importer/import-file.md#concept_F88785E2BDFD448CB5D1DA3491466B0D) wieder in das System.
