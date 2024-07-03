---
audience: end-user
title: Erstellen von Kompositionen
description: Erfahren Sie, wie Sie Kompositionen erstellen
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 36%

---


# Wichtige Grundsätze der Kompositionserstellung {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Kompositionseigenschaften"
>abstract="Wählen Sie in diesem Bildschirm die Vorlage aus, die zum Erstellen der Komposition verwendet werden soll, und geben Sie einen Titel an. Erweitern Sie den Abschnitt ADDITIONAL OPTIONS , um weitere Einstellungen wie den internen Namen der Komposition, deren Ordner, die Zeitzone und die Supervisorgruppe zu konfigurieren. Es wird dringend empfohlen, eine Gruppe von Verantwortlichen auszuwählen, damit Benutzerinnen und Benutzer benachrichtigt werden, wenn Fehler auftreten."

Zusammengestellte Datenkomposition bietet eine visuelle Arbeitsfläche, auf der Sie Zielgruppen mithilfe verschiedener Aktivitäten (Aufspaltung, Anreicherung usw.) erstellen können.

## Was ist in einem Aufsatz? {#gs-composition-inside}

Das Kompositionsdiagramm ist eine Darstellung dessen, was passieren soll. Es beschreibt die verschiedenen Aufgaben, die ausgeführt und miteinander verknüpft werden sollen.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Jede Komposition enthält:

* **Aktivitäten**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Die verschiedenen verfügbaren Aktivitäten werden im Diagramm durch Symbole dargestellt. Jede Aktivität verfügt über bestimmte Eigenschaften sowie andere Eigenschaften, die für alle Aktivitäten gelten.

  In einem Kompositionsdiagramm kann eine bestimmte Aktivität mehrere Aufgaben erstellen, insbesondere wenn eine Schleife oder wiederkehrende Aktionen vorhanden sind.

* **Transitionen**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz.

* **Arbeitstabellen**: Die Arbeitstabelle enthält alle von der Transition übermittelten Informationen. Jede Komposition verwendet mehrere Arbeitstabellen. Die in diesen Tabellen übermittelten Daten können während des gesamten Lebenszyklus der Komposition verwendet werden.

## Wichtige Schritte zum Erstellen einer Komposition {#gs-composition-steps}

Die wichtigsten Schritte zum Erstellen einer Komposition sind:

1. [Erstellen der Komposition](#create)
1. [Einstellungen der Komposition konfigurieren](#starting-audience)
1. [Aktivitäten hinzufügen und konfigurieren](#action-activities)
1. [Ausführung der Komposition und Überwachung ihrer Ausführung](#save)
