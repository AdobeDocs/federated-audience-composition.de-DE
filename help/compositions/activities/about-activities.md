---
audience: end-user
title: Arbeiten mit Aktivitäten
description: Erfahren Sie, wie Sie mit Aktivitäten arbeiten.
source-git-commit: 13e7e75fe1dc175fce9464fa58c7a50b5e6107d4
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 45%

---


# Arbeiten mit Aktivitäten {#activities}

In Federated Audience Komposition können Sie Kompositionen mit zwei Arten von Aktivitäten erstellen:

* **Zielgruppenbestimmungsaktivitäten** Sie können eine oder mehrere Zielgruppen erstellen, indem Sie eine Zielgruppe definieren und diese mithilfe von Schnittmengen-, Vereinigungs- oder Ausschlussvorgängen teilen oder kombinieren.
* **Flusssteuerung** -Aktivitäten dienen der Organisation und Ausführung von Kompositionen. Sie ermöglichen die Koordinierung der anderen Aktivitäten.

## Zielgruppenbestimmungs-Aktivitäten

* [Erstellen der Zielgruppenaktivität](build-audience.md): Definieren Sie Ihre Zielpopulation. Sie können entweder eine vorhandene Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.
* [Dimensionsänderung](change-dimension.md): Ändern Sie die Zielgruppendimension beim Erstellen der Komposition.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Dubletten in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten zur Verarbeitung in Ihrer Komposition. Mit dieser Aktivität können Sie die eingehende Transition nutzen und entsprechend der Konfiguration der Aktivität die ausgehende Transition mit Zusatzdaten ergänzen.
* [Abstimmung](reconciliation.md): Definieren Sie die Relation zwischen den Daten in der Datenbank und den Daten in einer Arbeitstabelle, z. B. aus einer externen Datei geladenen Daten.
* [Audience-Speicherung](save-audience.md): Aktualisieren Sie eine existierende Audience oder erstellen Sie eine neue Audience aus der zuvor in einer Komposition berechneten Population.
* [Aufteilen](split.md): Mit dieser Aktivität unterteilen Sie die eingehende Population in mehrere Teilmengen.

## Aktivitäten zur Flusskontrolle

* [Und-Verknüpfung](and-join.md): Synchronisieren Sie mehrere Ausführungszweige eines Workflows.
* **Ende** : Markieren Sie grafisch das Ende eines Workflows. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
* [Verzweigung](fork.md): Mit dieser Aktivität erzeugen Sie ausgehende Transitionen, um parallel mehrere Aktivitäten zu starten.
* [Planung](scheduler.md): Mit dieser Aktivität planen Sie, wann der Workflow gestartet werden soll.
* [Warten](wait.md): Mit dieser Aktivität halten Sie die Ausführung eines Teils eines Workflows vorübergehend an.
