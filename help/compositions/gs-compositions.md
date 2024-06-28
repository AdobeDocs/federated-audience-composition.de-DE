---
audience: end-user
title: Erste Schritte mit Kompositionen
description: Erfahren Sie, wie Sie mit Kompositionen beginnen
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 16%

---

# Erste Schritte mit Kompositionen {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Kompositionseigenschaften"
>abstract="In diesem Abschnitt finden Sie allgemeine Kompositionseigenschaften, auf die auch beim Erstellen der Komposition zugegriffen werden kann."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Kompositionssegmentierung"
>abstract="Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition beibehalten. Sie können diese Option aktivieren, um Arbeitstabellen zu Testzwecken beizubehalten. Es muss verwendet werden **only** in Entwicklungs- oder Staging-Umgebungen. Sie darf nie in einer Produktionsumgebung überprüft werden."




## Was ist ein Aufsatz? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Kompositionen"
>abstract="In diesem Bildschirm können Sie die vollständige Liste der Kompositionen aufrufen, ihren aktuellen Status, das letzte/nächste Ausführungsdatum überprüfen und eine neue Komposition erstellen."


## Einstellungen für den Umgang mit Fehlern  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Einstellungen für den Umgang mit Fehlern"
>abstract="In diesem Abschnitt können Sie definieren, wie Fehler während der Ausführung verwaltet werden. Sie können den Vorgang anhalten, eine bestimmte Anzahl von Fehlern ignorieren oder die Ausführung der Komposition stoppen."

* **[!UICONTROL Fehlerverwaltung]**: In diesem Feld können Sie festlegen, welche Aktionen im Fall von Fehlern bei einer Kompositionsaktivität durchgeführt werden sollen.
Es gibt drei mögliche Optionen:

   * **[!UICONTROL Prozess aussetzen]**: Die Komposition wird automatisch angehalten und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem gelöst ist, setzen Sie die Komposition mit der **[!UICONTROL Fortsetzen]** Schaltflächen.
   * **[!UICONTROL Ignorieren]**: Der Status der Aufgabe, die den Fehler ausgelöst hat, ändert sich in **[!UICONTROL Fehlgeschlagen]**, aber die Komposition behält die **[!UICONTROL Gestartet]** -Status.
   * **[!UICONTROL Vorgang abbrechen]**: Die Komposition wird automatisch gestoppt und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, starten Sie die Komposition mit dem **[!UICONTROL Starten]** Schaltfläche.

* **[!UICONTROL Aufeinanderfolgende Fehler]**: Dieses Feld wird verfügbar, wenn im Feld **[!UICONTROL Im Fehlerfall]** der Wert **[!UICONTROL Ignorieren]** ausgewählt wurde. Sie können die Anzahl der Fehler angeben, die ignoriert werden können, bevor der Prozess angehalten wird. Sobald diese Zahl erreicht ist, ändert sich der Kompositionsstatus in **[!UICONTROL Fehlgeschlagen]**. Wenn der Wert dieses Felds 0 beträgt, wird die Komposition unabhängig von der Anzahl der Fehler nie angehalten.
