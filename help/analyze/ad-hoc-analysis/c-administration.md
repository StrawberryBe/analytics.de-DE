---
description: Konfigurieren Sie Benutzer und erfahren Sie mehr über das Sampling von Daten.
title: Administration
uuid: 12f90223-139f-4a8d-bfd3-5cd9af7489d2
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Administration

Konfigurieren Sie Benutzer und erfahren Sie mehr über das Sampling von Daten.

Hilfe hinsichtlich der [!DNL Admin Console] erhalten Sie in der [Analysereferenz](https://docs.adobe.com/content/help/de-DE/analytics/landing/home.html).

## Anwenderlizenzen {#concept_C1440741C77C471EB38A243B013EA620}

Vor der Anmeldung muss der Benutzer eine Anwenderlizenz erhalten. Anwenderlizenzen lassen eine gleichzeitige Nutzung des Programms zu. Die Anwenderlizenzen können von mehreren Benutzern gemeinsam verwendet werden. Die Anzahl der gleichzeitigen Benutzer ist jedoch auf die Anzahl der erworbenen Lizenzen beschränkt.

<!-- 

c_user_license.html

 -->

Übersteigt die Anzahl der angemeldeten Benutzer die Anzahl der verfügbaren Lizenzen, wird der Benutzer durch ein Dialogfeld darauf hingewiesen, dass alle verfügbaren Lizenzen bereits in Gebrauch sind. Weiterhin werden sein Platz in der Warteschlange und ein Link zur erneuten Überprüfung des Warteschlangenplatzes angezeigt. Wenn eine Lizenz frei wird, wird der Benutzer per E-Mail benachrichtigt und es erscheint ein Popup-Dialogfeld, das die Verfügbarkeit von Ad Hoc Analysis anzeigt. Er hat dann 15 Minuten Zeit, um zu antworten, bevor er seinen Platz in der Warteschlange verliert.

## Anwenderlizenzen erteilen {#task_22AE669703EC48BA9685414538D8B1FA}

Schritte, die beschreiben, wie lokale Administratoren von „Reports and Analytics“ Anwenderlizenzen über das Zugriffsberechtigungssystem erteilen können.

<!-- 

t_user_licenses.xml

 -->

1. Melden Sie sich bei [!DNL Experience Cloud] an.
1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL User Management]**.
1. Klicken Sie auf **[!UICONTROL Edit Groups]**.

   Wenn Ihre Firma Anwenderlizenzen erworben hat, wird die [!UICONTROL Ad Hoc Analysis License Users] Gruppe in der [!UICONTROL Group Name] Spalte angezeigt. Die Anzahl der verfügbaren Lizenzen für die Benutzeranmeldung wird ebenfalls angezeigt.

1. Klicken Sie auf **[!UICONTROL Edit]**.
1. Under [!UICONTROL Assign User Logins], select the users you want to add to the group, then click **[!UICONTROL Add.]**
1. Klicken Sie auf **[!UICONTROL Save Group]**.

   Die Anzahl der Benutzer, die zu einer Gruppe hinzugefügt werden, wird vom Lizenzierungssystem nicht begrenzt. Die gleichzeitige Nutzung ist auf die Anzahl der erworbenen Anwenderlizenzen eingeschränkt.

## Benutzersitzungen verwalten {#task_868C3DD9CB3F45D19B98EEF60F5E0B32}

Schritte, die beschreiben, wie ein Administrator eine Benutzersitzung beenden kann. Mit dieser Funktion kann allerdings nicht verhindert werden, dass sich der betroffene Benutzer wieder anmeldet.

<!-- 

t_managing_users.xml

 -->

1. Klicken Sie auf **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User Management]** und dann auf **[!UICONTROL Manage Users]**.
1. Locate the user, then click **[!UICONTROL Terminate.]**

   On the [!UICONTROL Active Ad Hoc Analysis Sessions] page, the user who has been idle the longest displays at the top of list.

## Zugriffsberechtigung {#concept_A7F2A7600BFF47C38D7C980E08D395B8}

<!-- 

c_permissions.xml

 -->

Sie können den Zugriff auf Report Suites in der [!DNL Administration Console] einstellen. Sie können Berechtigungen auf der Report Suite-Ebene konfigurieren. Wenn Sie beispielsweise mehrere Report Suites aktiviert haben, aber nicht allen Benutzern Zugriff auf alle Report Suites gewähren möchten, können Sie Gruppen mit spezifischen Report Suites erstellen und die Benutzer dann der entsprechenden Gruppe zuweisen.

## Einen Benutzer zur Gruppe mit Zugriff auf alle Berichte hinzufügen {#task_E821BF3B4FDB434D844A98AAB15487A9}

Schritte, die das Gewähren des Zugriffs auf alle Report Suites für Benutzer ohne Admin-Berechtigung beschreiben.

<!-- 

t_permissions.xml

 -->

1. Melden Sie sich bei **[!UICONTROL Experience Cloud]** an.
1. Klicken Sie auf **[!UICONTROL Adobe Analytics > Admin]** > **[!UICONTROL User Management]** > **[!UICONTROL Edit Groups]**.
1. Klicken Sie auf **[!UICONTROL All Report Access]**.
1. Wählen [!UICONTROL Available Users]Sie den Benutzer aus und klicken Sie auf **[!UICONTROL Add.]**
1. Klicken Sie auf **[!UICONTROL Save Group]**.

## Berechtigungsgruppen erstellen {#task_65A4C2E58B13475B9B2606CEB93B7CBD}

Erstellen Sie Berechtigungsgruppen, um Benutzern ohne Admin-Berechtigungen Zugriff auf bestimmte Report Suites zu gewähren.

<!-- 

t_permission_groups.xml

 -->

1. Melden Sie sich bei **[!UICONTROL Experience Cloud]** an.
1. Klicken Sie auf **[!UICONTROL Adobe Analytics > Admin]** > **[!UICONTROL User Management]** > **[!UICONTROL Edit Groups]**.
1. Erstellen Sie eine Berechtigungsgruppe für Benutzer ohne Admin-Berechtigungen, in denen die für Ad Hoc Analysis aktivierten Report Suites enthalten sind, die Sie für Benutzer zugänglich machen möchten.

   Die dem Benutzer zur Verfügung stehenden Report Suites werden im Menü [!UICONTROL Report Cloud] angezeigt, wenn Sie ein neues Projekt erstellen.

## Proxy-Richtlinien in Java einrichten {#task_3B03F58519544025B55CF54FACF8F4F5}

Schritte, die das Einrichten von Proxy-Richtlinien bei einem Serververbindungsfehler beschreiben.

<!-- 

t_proxy_policies.xml

 -->

Ad Hoc Analysis nutzen HTTP zur Serverkommunikation. Es gelten dieselben Proxy-Richtlinien wie für anderen HTTP-Datenverkehr.

1. Starten Sie im [!DNL Windows Control Panel]Fenster die [!UICONTROL Java Control Panel].
1. Klicken Sie auf der **[!UICONTROL General]** Registerkarte auf **[!UICONTROL Network Settings]**.
1. Wählen Sie die Proxy-Einstellungen aus **[!UICONTROL Use browser settings]** oder konfigurieren Sie sie manuell.
1. Klicken Sie auf **[!UICONTROL OK]** und dann auf **[!UICONTROL OK]** die [!UICONTROL Java Control Panel].

## Ziehen von Stichproben von Daten {#concept_8433CFD38E0243849E92DF4F1E743AC3}

Es werden Stichproben von Besucherdaten gezogen, um aussagekräftige und präzise Berichte zu erzeugen. Der Datumsbereich wird als Datenausschnitt für ein geladenes Projekt verwendet. Ein Ausschnitt stellt in der Regel den aktuellen Monat sowie die vorhergehenden zwei Monate dar.

<!-- 

c_overview_data_sampling.xml

 -->

Zur optimalen Verarbeitung verwendet Ad Hoc Analysis in etwa 750 Mio. als die maximale Anzahl von Treffern pro Ausschnitt. (Treffer = Seitenansichten + Ereignisse.) 

Um die projizierte Stichprobenrate zu erhalten, werden die voraussichtlichen Treffer pro Datensatz errechnet und diese dann durch 750 Mio. dividiert, wie hier dargestellt:

* (Durchschnittl. Treffer pro Tag × Anzahl der Tage im Ausschnitt) ÷ 750 Mio.

Wenn Sie beispielsweise 10 Mio. Treffer pro Tag verzeichnen und einen Datenausschnitt von 90 Tagen verwenden:

* (10.000.000 × 90) ÷ 750.000.000 = 1,2

Um die Anzahl der Treffer in den 90 Tagen demnach unter 750.000.000 zu halten, könnte eine Stichprobe der Daten im Verhältnis 1,2 zu 1 erfolgen, aber da nur Stichproben aus Ganzzahlen gezogen werden, beträgt die Stichprobenrate 2 zu 1.

Wenn Sie als weiteres Beispiel 10 Mio. Treffer pro Tag verzeichnen und einen Datenausschnitt von 365 Tagen verwenden:

* (10.000.000 × 365) ÷ 750.000.000 = 4.8

Um die Anzahl der Treffer in den 365 Tagen demnach unter 750.000.000 zu halten, könnte eine Stichprobe der Daten im Verhältnis 4,8 zu 1 erfolgen, aber da Discover nur Stichproben aus Ganzzahlen zieht, beträgt die Stichprobenrate 5 zu 1.
