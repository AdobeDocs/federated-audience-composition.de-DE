---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 7%

---


# Einstellungen der Komposition konfigurieren {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Kompositionseigenschaften"
>abstract="In diesem Abschnitt finden Sie allgemeine Kompositionseigenschaften, auf die auch beim Erstellen der Komposition zugegriffen werden kann."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Kompositionssegmentierung"
>abstract="Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition beibehalten. Sie können diese Option aktivieren, um Arbeitstabellen zu Testzwecken beizubehalten. Es muss verwendet werden **only** in Entwicklungs- oder Staging-Umgebungen. Sie darf nie in einer Produktionsumgebung überprüft werden."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Einstellungen für den Umgang mit Fehlern"
>abstract="In diesem Abschnitt können Sie definieren, wie Fehler während der Ausführung verwaltet werden. Sie können den Vorgang anhalten, eine bestimmte Anzahl von Fehlern ignorieren oder die Ausführung der Komposition stoppen."

Beim Zugriff auf eine Komposition können Sie auf erweiterte Einstellungen zugreifen, mit denen Sie beispielsweise festlegen können, wie sich die Komposition im Falle eines Fehlers verhalten soll, oder die Verzögerung verwalten, nach der der Kompositionsverlauf bereinigt werden soll.

Um auf zusätzliche Optionen für Ihre Komposition zuzugreifen, klicken Sie auf die **Einstellungen** oberhalb der Arbeitsfläche.

![](assets/composition-create-settings.png)

Folgende Einstellungen sind verfügbar:

* **[!UICONTROL Titel]**: Ändern Sie den Titel der Komposition.

* **[!UICONTROL Zwischen zwei Ausführungen die ermittelte Population beibehalten]**: Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition beibehalten. Arbeitstabellen früherer Ausführungen werden durch eine technische Komposition bereinigt, die täglich ausgeführt wird.

  Wenn diese Option aktiviert ist, werden Arbeitstabellen auch nach der Ausführung der Komposition beibehalten. Sie können sie zu Testzwecken verwenden; daher darf sie **nur** in Entwicklungs- oder Staging-Umgebungen genutzt werden. Sie darf nie in einer Produktionseinheit überprüft werden.

* **[!UICONTROL Fehlerverwaltung]**: In diesem Abschnitt können Sie festlegen, welche Aktionen im Fall von Fehlern bei einer Kompositionsaktivität durchgeführt werden sollen. Es gibt drei mögliche Optionen:

   * **[!UICONTROL Prozess aussetzen]**: Die Komposition wird automatisch angehalten und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem gelöst ist, setzen Sie die Komposition mit der **[!UICONTROL Fortsetzen]** Schaltflächen.
   * **[!UICONTROL Ignorieren]**: Der Status der Aufgabe, die den Fehler ausgelöst hat, ändert sich in **[!UICONTROL Fehlgeschlagen]**, aber die Komposition behält die **[!UICONTROL Gestartet]** -Status.
   * **[!UICONTROL Vorgang abbrechen]**: Die Komposition wird automatisch gestoppt und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, starten Sie die Komposition mit dem **[!UICONTROL Starten]** Schaltfläche.

* **[!UICONTROL Folgefehler]**: Geben Sie die Anzahl der Fehler an, die ignoriert werden können, bevor der Prozess angehalten wird. Sobald diese Zahl erreicht ist, ändert sich der Kompositionsstatus in **[!UICONTROL Fehlgeschlagen]**. Wenn der Wert dieses Felds 0 beträgt, wird die Komposition unabhängig von der Anzahl der Fehler nie angehalten.
