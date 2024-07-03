---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: b946f8821d965fb00f79f6f5557adcfff1ee2387
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 47%

---


# Komposition starten und überwachen {#start-monitor}

Nachdem Sie Ihre Komposition erstellt und die Aufgaben entworfen haben, die auf der Arbeitsfläche ausgeführt werden sollen, können Sie sie starten und überwachen, wie sie ausgeführt wird.

## Komposition starten {#start}

Um die Komposition zu starten, navigieren Sie zum **[!UICONTROL Kompositionen]** oder der zugehörigen Kampagne und klicken Sie auf **[!UICONTROL Starten]** in der oberen rechten Ecke der Arbeitsfläche.

Sobald die Komposition ausgeführt wird, wird jede Aktivität auf der Arbeitsfläche in einer sequenziellen Reihenfolge ausgeführt, bis das Ende der Komposition erreicht ist.

Anhand eines visuellen Flusses können Sie den Fortschritt von Zielgruppenprofilen in Echtzeit verfolgen. Auf diese Weise können Sie den Status jeder Aktivität und die Anzahl der Profile, die zwischen ihnen wechseln, schnell identifizieren.

## Kompositionsübergänge {#transitions}

In Kompositionen werden Daten, die von einer Aktivität zur anderen über Transitionen übertragen werden, in einer temporären Arbeitstabelle gespeichert. Diese Daten können für jede Transition angezeigt werden. Wählen Sie dazu eine Transition aus, um ihre Eigenschaften auf der rechten Seite des Bildschirms zu öffnen.

* Klicken Sie auf **[!UICONTROL Vorschau für Schema]**, um das Schema der Arbeitstabelle anzuzeigen.
* Klicken Sie auf **[!UICONTROL Ergebnisvorschau]**, um die in der ausgewählten Transition übertragenen Daten zu visualisieren.

## Überwachen der Aktivitätsausführung {#activities}

Visuelle Indikatoren in der rechten oberen Ecke eines jeden Aktivitätsfeldes ermöglichen es, die Ausführung zu überprüfen:

| Visueller Indikator | Beschreibung |
|-----|------------|
|  | Die Aktivität wird derzeit ausgeführt. |
|  | Die Aktivität erfordert Ihre Aufmerksamkeit. Dies kann die Bestätigung eines Versands oder die Ergreifung einer notwendigen Maßnahme beinhalten. |
|  | Bei der Aktivität ist ein Fehler aufgetreten. Um das Problem zu beheben, öffnen Sie die Kompositionsprotokolle , um weitere Informationen zu erhalten. |
|  | Die Aktivität wurde erfolgreich ausgeführt. |

## Überwachen der Protokolle und Aufgaben {#logs-tasks}

Das Überwachen von Kompositionsprotokollen und -aufgaben ist ein wichtiger Schritt, um Ihre Kompositionen zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden. Sie können über das Symbol **[!UICONTROL Protokolle]** in der Aktionssymbolleiste und im Eigenschaftenbereich jeder Aktivität aufgerufen werden.

Die **[!UICONTROL Protokolle und Aufgaben]** zeigt einen Verlauf der Ausführung der Komposition an und zeichnet alle Benutzeraktionen und aufgetretenen Fehler auf. Dieser Verlauf wird für die in der Komposition angegebene Dauer gespeichert. [Ausführungsoptionen](composition-settings.md). Während dieser Dauer werden alle Nachrichten gespeichert, auch nach einem Neustart der Komposition. Wenn Sie die Nachrichten einer früheren Ausführung nicht speichern möchten, klicken Sie auf die Schaltfläche **[!UICONTROL Verlauf bereinigen]**.

Es stehen zwei Arten von Informationen zur Verfügung:

* Die **[!UICONTROL Protokoll]** enthält den Ausführungsverlauf aller Kompositionsaktivitäten. Sie zeigt in chronologischer Abfolge alle Vorgänge und Ausführungsfehler.
* Die Registerkarte **[!UICONTROL Aufgaben]** liefert Details zur Ausführungsabfolge der Aktivitäten.

In beiden Registerkarten können Sie die angezeigten Spalten und ihre Reihenfolge auswählen, Filter anwenden und das Suchfeld verwenden, um die gewünschten Informationen schnell zu finden.

## Ausführungsbefehle von Kompositionen {#execution-commands}

Die Aktionsleiste in der oberen rechten Ecke enthält Befehle, mit denen Sie die Ausführung der Komposition verwalten können. Sie haben folgende Möglichkeiten:

* **[!UICONTROL Starten]** / **[!UICONTROL Fortsetzen]** die Ausführung der Komposition, die dann den Status Gestartet annimmt. Wenn die Komposition angehalten wurde, wird sie fortgesetzt. Andernfalls wird sie gestartet und die ersten Aktivitäten werden aktiviert.

* **[!UICONTROL Anhalten]** die Ausführung der Komposition, die dann den Status Ausgesetzt annimmt. Bis zur Wiederaufnahme werden keine neuen Aktivitäten aktiviert, laufende Vorgänge werden jedoch fortgeführt.

* **[!UICONTROL Anhalten]** eine Komposition, die ausgeführt wird und dann den Status Abgeschlossen annimmt. Die laufenden Vorgänge werden nach Möglichkeit unterbrochen. Sie können die Komposition nicht an derselben Stelle wiederaufnehmen, an der sie gestoppt wurde.
