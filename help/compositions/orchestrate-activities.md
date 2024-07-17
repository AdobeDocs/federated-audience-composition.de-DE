---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 45%

---


# Orchestrieren von Kompositionsaktivitäten {#activities}

Nachdem Sie eine Komposition erstellt haben, können Sie mit der Orchestrierung der verschiedenen Aufgaben beginnen, die sie ausführen wird. Dazu wird eine visuelle Arbeitsfläche bereitgestellt, mit der Sie Ihr Kompositionsdiagramm erstellen können. Innerhalb dieses Diagramms können Sie verschiedene Aktivitäten hinzufügen und sie in einer sequentiellen Reihenfolge miteinander verbinden.

## Hinzufügen von Aktivitäten {#add}

In diesem Schritt der Konfiguration wird das Diagramm mit einem Startsymbol angezeigt, das den Anfang Ihres Workflows darstellt. Um Ihre erste Aktivität hinzuzufügen, klicken Sie auf die Schaltfläche **+**, die mit dem Startsymbol verbunden ist.

Es erscheint eine Liste von Aktivitäten, die dem Diagramm hinzugefügt werden können. Die verfügbaren Aktivitäten hängen von Ihrer Position im Kompositionsdiagramm ab. Wenn Sie beispielsweise Ihre erste Aktivität hinzufügen, können Sie Ihre Komposition mit einer Audience beginnen, den Workflow-Pfad aufteilen, eine Planung festlegen, um die Ausführung des Workflows zu verzögern, oder eine **Warten** -Aktivität festlegen, um die Ausführung des Workflows zu verzögern. Nach der Aktivität **Audience erstellen** können Sie Ihre Zielgruppe jedoch durch Zielgruppenbestimmungsaktivitäten verfeinern oder den Kompositionsprozess mit Steuerungsaktivitäten organisieren.

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

* **Mehrfachauswahl**: Wählen Sie mehrere Aktivitäten aus, um alle gleichzeitig zu löschen, oder kopieren Sie sie und fügen Sie sie ein. Weitere Informationen finden Sie in [diesem Abschnitt](#copy).
* **Drehen**: Dreht die Arbeitsfläche vertikal.
* **An Bildschirm anpassen**: Passt die Vergrößerung der Arbeitsfläche an Ihren Bildschirm an.
* **Verkleinern**/**Vergrößern**: Verkleinert bzw. vergrößert die Arbeitsfläche.
* **Karte anzeigen**: Öffnet einen Snapshot der Arbeitsfläche, in der Sie sich befinden.

## Verwalten von Aktivitäten {#manage}

Beim Hinzufügen von Aktivitäten sind im Eigenschaftenbereich Aktionsschaltflächen verfügbar, mit denen Sie mehrere Vorgänge ausführen können.

![](assets/activity-actions.png)

Sie haben folgende Möglichkeiten:

* **Löschen** der Aktivität von der Arbeitsfläche aus.
* **Deaktivieren/Aktivieren** der Aktivität. Wenn der Workflow ausgeführt wird, werden deaktivierte Aktivitäten und auf demselben Pfad folgende Aktivitäten nicht ausgeführt und der Workflow wird angehalten.
* **Anhalten/Fortsetzen** der Aktivität. Wenn der Workflow ausgeführt wird, wird er mit bei der angehaltenen Aktivität angehalten. Die entsprechende Aufgabe sowie alle auf demselben Pfad folgenden Aufgaben werden nicht ausgeführt.
* **Kopieren** Sie die Aktivität, um sie an einer anderen Stelle in der Komposition einzufügen. Klicken Sie dazu auf die Schaltfläche **+** in einer Transition und wählen Sie &quot;Aktivität &quot;X einfügen&quot;. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Konfigurieren Sie **Ausführungsoptionen** für die ausgewählte Aktivität. Erweitern Sie den folgenden Abschnitt, um mehr über die verfügbaren Optionen zu erfahren.

  ++ Verfügbare Ausführungsoptionen

  Im Abschnitt **Eigenschaften** können Sie allgemeine Einstellungen für die Ausführung der Aktivität konfigurieren:

   * **Ausführung**: Definieren Sie die Aktion, die ausgeführt werden soll, wenn der gestartet wird.
   * **Maximale Ausführungsdauer**: Geben Sie eine Dauer wie &quot;30s&quot;oder &quot;1h&quot;an. Wenn eine Aufgabe die angegebene Dauer überschreitet, wird ein Warnhinweis erzeugt. Die Workflow-Ausführung wird hiervon jedoch nicht beeinflusst.
   * **Zeitzone**: Wählen Sie die Zeitzone der Aktivität aus. Zusammengestellte Zielgruppenkomposition ermöglicht es Ihnen, die Zeitunterschiede zwischen mehreren Ländern auf derselben Instanz zu verwalten. Die entsprechenden Einstellungen werden bei der Instanzerstellung vorgenommen.
   * **Affinität**: Erzwingt die Ausführung der Kompositionstätigkeit auf einem bestimmten Computer. Hierzu müssen Sie eine oder mehrere Affinitäten für die betreffende Aktivität angeben.
   * **Verhalten**: Definieren Sie das Verfahren, das bei der Verwendung asynchroner Aufgaben ausgeführt werden soll.

  Im Abschnitt **Umgang mit Fehlern** können Sie angeben, welche Aktion ausgeführt werden soll, wenn bei der Aktivität ein Fehler auftritt.

  Im Abschnitt **Initialisierungsscript** können Sie Variablen initialisieren oder Aktivitätseigenschaften ändern. Klicken Sie auf die Schaltfläche **Code bearbeiten** und geben Sie das auszuführende Code-Snippet ein. Das Skript wird aufgerufen, wenn die Aktivität ausgeführt wird.

+++

* Zugreifen auf die **Protokolle und Aufgaben** der Aktivität.
