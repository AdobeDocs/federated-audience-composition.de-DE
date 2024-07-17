---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 36%

---


# Orchestrieren von Kompositionsaktivitäten {#activities}

Nachdem Sie eine Komposition erstellt haben, können Sie mit der Orchestrierung der verschiedenen Aufgaben beginnen, die sie ausführen wird. Dazu wird eine visuelle Arbeitsfläche bereitgestellt, mit der Sie Ihr Kompositionsdiagramm für Zielgruppen erstellen können. Innerhalb dieses Diagramms können Sie verschiedene Aktivitäten hinzufügen und sie in einer sequentiellen Reihenfolge miteinander verbinden.

## Hinzufügen von Aktivitäten {#add}

In dieser Phase der Konfiguration wird das Diagramm mit einem Startsymbol angezeigt, das den Anfang Ihrer Komposition darstellt. Um Ihre erste Aktivität hinzuzufügen, klicken Sie auf die Schaltfläche **+**, die mit dem Startsymbol verbunden ist.

Es erscheint eine Liste von Aktivitäten, die dem Diagramm hinzugefügt werden können. Die verfügbaren Aktivitäten hängen von Ihrer Position im Kompositionsdiagramm ab. Wenn Sie beispielsweise Ihre erste Aktivität hinzufügen, können Sie Ihre Komposition mit einer Zielgruppe beginnen, den Kompositionspfad aufteilen, eine Planung festlegen, um die Ausführung der Komposition zu verzögern, oder eine **Warten** -Aktivität festlegen, um die Ausführung der Komposition zu verzögern. Nach der Aktivität **Audience erstellen** können Sie Ihre Zielgruppe jedoch durch Zielgruppenbestimmungsaktivitäten verfeinern oder den Kompositionsprozess mit Steuerungsaktivitäten organisieren.

Sobald eine Aktivität zum Diagramm hinzugefügt wurde, erscheint rechts ein Bereich, in dem Sie die neu hinzugefügte Aktivität mit spezifischen Einstellungen konfigurieren können. Detaillierte Informationen über die Konfiguration jeder Aktivität finden Sie in [diesem Abschnitt](activities/about-activities.md).

![](assets/composition-create-add.png)

Wiederholen Sie diesen Vorgang, um je nach den Aufgaben, die Ihre Komposition ausführen soll, beliebig viele Aktivitäten hinzuzufügen. Beachten Sie, dass Sie auch eine neue Aktivität zwischen zwei Aktivitäten einfügen können. Klicken Sie dazu auf die Schaltfläche **+** in der Transition zwischen den Aktivitäten, wählen Sie die gewünschte Aktivität aus und konfigurieren Sie sie im rechten Bereich.

>[!TIP]
>
>Sie haben die Möglichkeit, den Namen der Transitionen zwischen den einzelnen Aktivitäten zu personalisieren. Wählen Sie dazu die Transition aus und ändern Sie die Bezeichnung im rechten Bereich.

## Symbolleiste der Arbeitsfläche {#toolbar}

Die Symbolleiste oben rechts auf der Arbeitsfläche bietet Optionen zum einfachen Bearbeiten der Aktivitäten und Navigieren auf der Arbeitsfläche.

![](assets/canvas-toolbar.png)

Die verfügbaren Aktionen sind:

* **[!UICONTROL Mehrfachauswahl]**: Wählen Sie mehrere Aktivitäten aus, um alle gleichzeitig zu löschen, oder kopieren Sie sie und fügen Sie sie ein. Weitere Informationen finden Sie in [diesem Abschnitt](#copy).
* **[!UICONTROL Drehen]**: Dreht die Arbeitsfläche vertikal.
* **[!UICONTROL An Bildschirm anpassen]**: Passt die Vergrößerung der Arbeitsfläche an Ihren Bildschirm an.
* **[!UICONTROL Verkleinern]**/**[!UICONTROL Vergrößern]**: Verkleinert bzw. vergrößert die Arbeitsfläche.
* **[!UICONTROL Karte anzeigen]**: Öffnet einen Snapshot der Arbeitsfläche, in der Sie sich befinden.

## Verwalten von Aktivitäten {#manage}

Beim Hinzufügen von Aktivitäten sind im Eigenschaftenbereich Aktionsschaltflächen verfügbar, mit denen Sie mehrere Vorgänge ausführen können.

![](assets/activity-actions.png)

Sie haben folgende Möglichkeiten:

* **[!UICONTROL Löschen]** der Aktivität von der Arbeitsfläche aus.
* **[!UICONTROL Deaktivieren]/[!UICONTROL Aktivieren]** Sie die Aktivität. Wenn die Komposition ausgeführt wird, werden deaktivierte Aktivitäten und die folgenden Aktivitäten auf demselben Pfad nicht ausgeführt und die Komposition wird gestoppt.
* **[!UICONTROL Anhalten]/[!UICONTROL Wiederaufnehmen]** der Aktivität. Wenn die Komposition ausgeführt wird, wird sie bei der angehaltenen Aktivität angehalten. Die entsprechende Aufgabe sowie alle auf demselben Pfad folgenden Aufgaben werden nicht ausgeführt.
* **[!UICONTROL Kopieren]** Sie die Aktivität, um sie an einer anderen Stelle in der Komposition einzufügen. Klicken Sie dazu auf die Schaltfläche **+** in einer Transition und wählen Sie die Option **[!UICONTROL Aktivität X einfügen]** <!-- cannot copy multiple activities ? cannot paste in another composition?--> aus.
* Konfigurieren Sie **[!UICONTROL Ausführungsoptionen]** für die ausgewählte Aktivität. Erweitern Sie den folgenden Abschnitt, um mehr über die verfügbaren Optionen zu erfahren.

  ++ Verfügbare Ausführungsoptionen

  Im Abschnitt **[!UICONTROL Eigenschaften]** können Sie allgemeine Einstellungen für die Ausführung der Aktivität konfigurieren:

   * **[!UICONTROL Ausführung]**: Definieren Sie die Aktion, die ausgeführt werden soll, wenn der gestartet wird.
   * **[!UICONTROL Maximale Ausführungsdauer]**: Geben Sie eine Dauer wie &quot;30s&quot;oder &quot;1h&quot;an. Wenn eine Aufgabe die angegebene Dauer überschreitet, wird ein Warnhinweis erzeugt. Dies hat keine Auswirkungen auf die Funktionsweise der Komposition.
   * **[!UICONTROL Zeitzone]**: Wählen Sie die Zeitzone der Aktivität aus. Zusammengestellte Zielgruppenkomposition ermöglicht es Ihnen, die Zeitunterschiede zwischen mehreren Ländern auf derselben Instanz zu verwalten. Die entsprechenden Einstellungen werden bei der Instanzerstellung vorgenommen.
   * **[!UICONTROL Affinität]**: Erzwingt die Ausführung der Kompositionstätigkeit auf einem bestimmten Computer. Hierzu müssen Sie eine oder mehrere Affinitäten für die betreffende Aktivität angeben.
   * **[!UICONTROL Verhalten]**: Definieren Sie das Verfahren, das bei der Verwendung asynchroner Aufgaben ausgeführt werden soll.

  Im Abschnitt **[!UICONTROL Umgang mit Fehlern]** können Sie angeben, welche Aktion ausgeführt werden soll, wenn bei der Aktivität ein Fehler auftritt.

  Im Abschnitt **[!UICONTROL Initialisierungsscript]** können Sie Variablen initialisieren oder Aktivitätseigenschaften ändern. Klicken Sie auf die Schaltfläche **[!UICONTROL Code bearbeiten]** und geben Sie das auszuführende Code-Snippet ein. Das Skript wird aufgerufen, wenn die Aktivität ausgeführt wird.

+++

* Zugreifen auf die **Protokolle und Aufgaben** der Aktivität.
