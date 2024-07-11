---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: be24c32977cdccab0a5fc7e77a033f4d2b746b9f
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 25%

---


# Erstellen und Konfigurieren der Komposition {#create}

Der erste Schritt zum Erstellen einer Komposition besteht darin, ihren Titel zu definieren und bei Bedarf zusätzliche Einstellungen zu konfigurieren.

## Erstellen der Komposition {#create-the-composition}

1. Zugriff auf **[!UICONTROL Zielgruppen]** und wählen Sie **[!UICONTROL Zusammengestellte Kompositionen]** Registerkarte.

1. Klicken Sie auf **[!UICONTROL Komposition erstellen]** Schaltfläche.

   ![](assets/composition-create.png)

1. Im **[!UICONTROL Eigenschaften]** einen Titel für die Komposition angeben und auf **[!UICONTROL Erstellen]**.

1. Die Arbeitsfläche der Komposition wird angezeigt. Sie können Ihre Komposition jetzt konfigurieren, indem Sie so viele Aktivitäten wie nötig hinzufügen, um sie Ihren Anforderungen anzupassen, bevor Sie sie ausführen:

   * [Erfahren Sie, wie Sie Aktivitäten koordinieren](#action-activities)
   * [Erfahren Sie, wie Sie eine Komposition starten und überwachen](#save)

## Einstellungen der Komposition konfigurieren {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Kompositionseigenschaften"
>abstract="Dieser Abschnitt enthält allgemeine Kompositionseigenschaften, auf die auch beim Erstellen der Komposition zugegriffen werden kann."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Kompositionssegmentierung"
>abstract="Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition aufbewahrt. Sie können diese Option aktivieren, um Arbeitstabellen zu Testzwecken beizubehalten. Diese Option darf **nur** in Entwicklungs- oder Staging-Umgebungen verwendet werden. Sie darf niemals in einer Produktionsumgebung aktiviert werden."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Einstellungen für den Umgang mit Fehlern"
>abstract="In diesem Abschnitt können Sie definieren, wie Fehler während der Ausführung behandelt werden sollen. Sie können festlegen, dass der Prozess angehalten werden soll, dass eine bestimmte Anzahl von Fehlern ignoriert werden soll oder dass die Ausführung der Komposition gestoppt werden soll."

Beim Zugriff auf eine Komposition können Sie auf erweiterte Einstellungen zugreifen, mit denen Sie beispielsweise festlegen können, wie sich die Komposition im Falle eines Fehlers verhalten soll.

Um auf zusätzliche Optionen für Ihre Komposition zuzugreifen, klicken Sie auf die **Einstellungen** im oberen Bereich des Bildschirms zur Kompositionserstellung.

![](assets/composition-create-settings.png)

Folgende Einstellungen sind verfügbar:

* **[!UICONTROL Titel]**: Ändern Sie den Titel der Komposition.

* **[!UICONTROL Zwischen zwei Ausführungen die ermittelte Population beibehalten]**: Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition beibehalten. Arbeitstabellen früherer Ausführungen werden durch eine technische Komposition bereinigt, die täglich ausgeführt wird.

  Wenn diese Option aktiviert ist, werden Arbeitstabellen auch nach der Ausführung der Komposition beibehalten. Sie können sie zu Testzwecken verwenden; daher darf sie **nur** in Entwicklungs- oder Staging-Umgebungen genutzt werden. Sie darf nie in einer Produktionseinheit überprüft werden.

* **[!UICONTROL Fehlerverwaltung]**: Mit dieser Option können Sie die Aktionen definieren, die bei einer Kompositionsaktivität mit Fehlern ausgeführt werden sollen. Es gibt drei mögliche Optionen:

   * **[!UICONTROL Prozess aussetzen]**: Die Komposition wird automatisch angehalten und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem gelöst ist, setzen Sie die Komposition mit der **[!UICONTROL Fortsetzen]** Schaltflächen.
   * **[!UICONTROL Ignorieren]**: Der Status der Aufgabe, die den Fehler ausgelöst hat, ändert sich in **[!UICONTROL Fehlgeschlagen]**, aber die Komposition behält die **[!UICONTROL Gestartet]** -Status.
   * **[!UICONTROL Vorgang abbrechen]**: Die Komposition wird automatisch gestoppt und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, starten Sie die Komposition mit dem **[!UICONTROL Starten]** Schaltfläche.

* **[!UICONTROL Folgefehler]**: Geben Sie die Anzahl der Fehler an, die ignoriert werden können, bevor der Prozess angehalten wird. Sobald diese Zahl erreicht ist, ändert sich der Kompositionsstatus in **[!UICONTROL Fehlgeschlagen]**. Wenn der Wert dieses Felds 0 beträgt, wird die Komposition unabhängig von der Anzahl der Fehler nie angehalten.
