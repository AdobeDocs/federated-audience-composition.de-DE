---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 23%

---


# Erstellen und Ausführen einer Komposition {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="Workflow-Eigenschaften"
>abstract="Wählen Sie in diesem Bildschirm die Vorlage aus, die zum Erstellen des Workflows verwendet werden soll, und geben Sie einen Titel an. Erweitern Sie den Abschnitt ZUSÄTZLICHE OPTIONEN, um weitere Einstellungen wie den internen Namen des Workflows, seine Ordner, die Zeitzone und die Gruppe der Verantwortlichen zu konfigurieren. Es wird dringend empfohlen, eine Gruppe von Verantwortlichen auszuwählen, damit Benutzerinnen und Benutzer benachrichtigt werden, wenn Fehler auftreten."

## Erstellen der Komposition {#create}

Gehen Sie wie folgt vor, um eine Komposition zu erstellen:

1. Zugriff auf **[!UICONTROL Zielgruppen]** und wählen Sie **[!UICONTROL Zusammengestellte Kompositionen]** Registerkarte.

1. Klicken Sie auf **[!UICONTROL Komposition erstellen]** Schaltfläche.

1. Im **[!UICONTROL Eigenschaften]** einen Titel für die Komposition angeben und auf **[!UICONTROL Erstellen]**.

1. Die Arbeitsfläche der Komposition wird angezeigt. Sie können Ihre Komposition jetzt konfigurieren, indem Sie so viele Aktivitäten hinzufügen, wie Sie benötigen, um sie vor der Ausführung Ihren Anforderungen anzupassen. Sie können auch zusätzliche Einstellungen wie den Titel der Komposition oder Optionen bezüglich der Fehlerverwaltung bei der Ausführung der Komposition konfigurieren.

Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Einstellungen der Komposition konfigurieren](#starting-audience)
* [Hinzufügen von Aktivitäten](#action-activities)
* [Ausführung der Komposition und Überwachung ihrer Ausführung](#save)

## Einstellungen der Komposition konfigurieren {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Kompositionseigenschaften"
>abstract="In diesem Abschnitt finden Sie allgemeine Kompositionseigenschaften, auf die auch beim Erstellen der Komposition zugegriffen werden kann."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Kompositionssegmentierung"
>abstract="Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition beibehalten. Sie können diese Option aktivieren, um Arbeitstabellen zu Testzwecken beizubehalten. Es muss verwendet werden **only** in Entwicklungs- oder Staging-Umgebungen. Sie darf nie in einer Produktionsumgebung überprüft werden."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Einstellungen für den Umgang mit Fehlern"
>abstract="In diesem Abschnitt können Sie definieren, wie Fehler während der Ausführung verwaltet werden. Sie können den Vorgang anhalten, eine bestimmte Anzahl von Fehlern ignorieren oder die Ausführung der Komposition stoppen."

Klicken Sie auf **Einstellungen** -Schaltfläche, um auf zusätzliche Optionen für die Komposition zuzugreifen:

* **[!UICONTROL Titel]**: Ändern Sie den Titel der Komposition.

* **[!UICONTROL Zwischen zwei Ausführungen die ermittelte Population beibehalten]**: Standardmäßig werden nur die Arbeitstabellen der letzten Ausführung der Komposition beibehalten. Arbeitstabellen früherer Ausführungen werden durch einen technischen Workflow bereinigt, der täglich ausgeführt wird.

  Wenn diese Option aktiviert ist, werden Arbeitstabellen auch nach der Ausführung der Komposition beibehalten. Sie können sie zu Testzwecken verwenden; daher darf sie **nur** in Entwicklungs- oder Staging-Umgebungen genutzt werden. Sie darf niemals in einem Produktions-Workflow aktiviert sein.

* **[!UICONTROL Fehlerverwaltung]**: In diesem Abschnitt können Sie festlegen, welche Aktionen im Fall von Fehlern bei einer Kompositionsaktivität durchgeführt werden sollen. Es gibt drei mögliche Optionen:

   * **[!UICONTROL Prozess aussetzen]**: Die Komposition wird automatisch angehalten und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem gelöst ist, setzen Sie die Komposition mit der **[!UICONTROL Fortsetzen]** Schaltflächen.
   * **[!UICONTROL Ignorieren]**: Der Status der Aufgabe, die den Fehler ausgelöst hat, ändert sich in **[!UICONTROL Fehlgeschlagen]**, aber die Komposition behält die **[!UICONTROL Gestartet]** -Status.
   * **[!UICONTROL Vorgang abbrechen]**: Die Komposition wird automatisch gestoppt und ihr Status ändert sich in **[!UICONTROL Fehlgeschlagen]**. Sobald das Problem behoben ist, starten Sie die Komposition mit dem **[!UICONTROL Starten]** Schaltfläche.

* **[!UICONTROL Folgefehler]**: Geben Sie die Anzahl der Fehler an, die ignoriert werden können, bevor der Prozess angehalten wird. Sobald diese Zahl erreicht ist, ändert sich der Kompositionsstatus in **[!UICONTROL Fehlgeschlagen]**. Wenn der Wert dieses Felds 0 beträgt, wird die Komposition unabhängig von der Anzahl der Fehler nie angehalten.

## Hinzufügen von Aktivitäten {#activities}

Auf der Arbeitsfläche für Kompositionen können Sie konfigurieren, dass beliebig viele Aktivitäten in der Komposition hinzugefügt werden.

Klicken Sie dazu auf die Schaltfläche + im Kompositionspfad und fügen Sie dann die gewünschte Aktivität hinzu. Der rechte Bereich wird geöffnet, in dem Sie die neu hinzugefügte Aktivität konfigurieren können. [Erfahren Sie mehr über die Aktivitäten in Kompositionen und deren Konfiguration](../compositions/activities/about-activities.md)

Um eine Aktivität aus der Arbeitsfläche zu entfernen, wählen Sie sie aus und klicken Sie im rechten Bereich auf die Schaltfläche Löschen . Wenn die zu löschende Aktivität eine übergeordnete Aktivität in der Komposition ist, wird eine Nachricht angezeigt, in der Sie angeben können, ob Sie nur die ausgewählte Aktivität oder alle ihre untergeordneten Aktivitäten löschen möchten.

## Komposition ausführen {#execute}

Sobald Ihre Komposition fertig ist, klicken Sie auf die **[!UICONTROL Starten]** -Schaltfläche, um sie auszuführen und die resultierenden Zielgruppen in Adobe Experience Platform zu speichern. &quot;Sie können die Ausführung des Workflows mithilfe des **Protokolle** Schaltfläche. Es stehen drei Tabs zur Verfügung, mit denen Sie die Ausführung überwachen können:

* **[!UICONTROL Protokolle]**:
* **[!UICONTROL Aufgaben]**:
* **[!UICONTROL Variablen]**:
