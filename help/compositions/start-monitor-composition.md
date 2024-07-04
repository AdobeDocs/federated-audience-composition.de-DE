---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 31%

---


# Komposition starten und überwachen {#start-monitor}

Nachdem Sie Ihre Komposition erstellt und die Aufgaben entworfen haben, die auf der Arbeitsfläche ausgeführt werden sollen, können Sie sie starten und überwachen, wie sie ausgeführt wird.

## Komposition starten {#start}

Um eine Komposition zu erstellen, klicken Sie auf die Schaltfläche **[!UICONTROL Starten]** in der oberen rechten Ecke des Bildschirms. Wenn die Komposition ausgeführt wird, wird jede Aktivität auf der Arbeitsfläche in einer sequenziellen Reihenfolge ausgeführt, bis das Ende der Komposition erreicht ist.

Anhand eines visuellen Flusses können Sie den Fortschritt von Zielgruppenprofilen in Echtzeit verfolgen. Auf diese Weise können Sie den Status jeder Aktivität und die Anzahl der Profile, die zwischen ihnen wechseln, schnell identifizieren.

![](assets/composition-visual-flow.png)

## Kompositionsübergänge {#transitions}

In Kompositionen werden Daten, die von einer Aktivität zur anderen über Transitionen übertragen werden, in einer temporären Arbeitstabelle gespeichert. Diese Daten können für jede Transition angezeigt werden. Wählen Sie dazu eine Transition aus, um ihre Eigenschaften auf der rechten Seite des Bildschirms zu öffnen.

* Klicken Sie auf **[!UICONTROL Vorschau für Schema]**, um das Schema der Arbeitstabelle anzuzeigen.
* Klicken Sie auf **[!UICONTROL Ergebnisvorschau]**, um die in der ausgewählten Transition übertragenen Daten zu visualisieren.

![](assets/transition-preview.png)

## Überwachen der Aktivitätsausführung {#activities}

Visuelle Indikatoren in der rechten oberen Ecke eines jeden Aktivitätsfeldes ermöglichen es, die Ausführung zu überprüfen:

| Visueller Indikator | Beschreibung |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | Die Aktivität wird derzeit ausgeführt. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | Die Aktivität erfordert Ihre Aufmerksamkeit. Dies kann die Bestätigung eines Versands oder die Ergreifung einer notwendigen Maßnahme beinhalten. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Bei der Aktivität ist ein Fehler aufgetreten. Um das Problem zu beheben, öffnen Sie die Kompositionsprotokolle , um weitere Informationen zu erhalten. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | Die Aktivität wurde erfolgreich ausgeführt. |

## Überwachen der Protokolle und Aufgaben {#logs-tasks}

Das Überwachen von Kompositionsprotokollen und -aufgaben ist ein wichtiger Schritt, um Ihre Kompositionen zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden. Sie können über die **[!UICONTROL Protokolle]** -Schaltfläche in der Symbolleiste der Aktion und im Eigenschaftenbereich jeder Aktivität verfügbar.

![](assets/logs-button.png)

Die **[!UICONTROL Kompositionsprotokolle und Aufgaben]** zeigt einen Verlauf der Ausführung der Komposition an, in dem alle Benutzeraktionen und aufgetretenen Fehler aufgezeichnet werden.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

Der Verlauf ist in verschiedene Tabs unterteilt, die nachfolgend beschrieben werden:

* Die **[!UICONTROL Protokoll]** enthält den Ausführungsverlauf aller Kompositionsaktivitäten. Er zeigt in chronologischer Abfolge alle Vorgänge und Ausführungsfehler.
* Der **[!UICONTROL Aufgaben]**-Tab liefert Details zur Ausführungsabfolge der Aktivitäten. Die Schaltfläche am Ende jeder Aufgabe ermöglicht die Auflistung der Ereignisvariablen, die durch die Aktivität übergeben werden.
* Die **[!UICONTROL Variablen]** -Tab listet alle in der Komposition übergebenen Variablen auf. Sie ist nur verfügbar, wenn Sie auf die Protokolle und Aufgaben von der Arbeitsfläche der Komposition aus zugreifen. Sie ist jetzt beim Zugriff auf die Protokolle im Eigenschaftenbereich einer Aktivität verfügbar.  <!-- à confirmer-->

![](assets/logs-tasks.png)

In allen Registerkarten können Sie die angezeigten Spalten und ihre Reihenfolge auswählen, Filter anwenden und das Suchfeld verwenden, um die gewünschten Informationen schnell zu finden.

## Ausführungsbefehle von Kompositionen {#execution-commands}

Die Aktionsleiste in der oberen rechten Ecke enthält Befehle, mit denen Sie die Ausführung der Komposition verwalten können.

![](assets/execution-actions.png)

Die verfügbaren Aktionen sind:

* **Starten**: Startet die Ausführung der Komposition, die dann die **Gestartet** -Status. Die Komposition wird gestartet und die ersten Aktivitäten werden aktiviert.

* **[!UICONTROL Fortsetzen]**: Setzt die Ausführung der ausgesetzten Komposition fort. Die Komposition übernimmt die **Gestartet** -Status.

* **[!UICONTROL Anhalten]** die Ausführung der Komposition, die dann die **Angehalten** -Status. Bis zur Wiederaufnahme werden keine neuen Aktivitäten aktiviert, laufende Vorgänge werden jedoch fortgeführt.

* **[!UICONTROL Anhalten]** eine Komposition, die ausgeführt wird, die dann die **Abgeschlossen** -Status. Die laufenden Vorgänge werden nach Möglichkeit unterbrochen. Sie können die Komposition nicht an derselben Stelle wiederaufnehmen, an der sie gestoppt wurde.

* **Neu starten**: Hält die Komposition an und startet sie neu. In den meisten Fällen können Sie so einen schnelleren Neustart durchführen, da das Anhalten eines Workflows eine gewisse Zeit in Anspruch nimmt und die **Starten** -Schaltfläche nur verfügbar, wenn der Stopp effektiv ist.
