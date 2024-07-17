---
audience: end-user
title: Arbeiten mit Aktivitäten
description: Erfahren Sie, wie Sie mit Aktivitäten arbeiten.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 39%

---


# Arbeiten mit Aktivitäten {#activities}

In Federated Audience Komposition können Sie Kompositionen mit zwei Arten von Aktivitäten erstellen:

* Mit **Zielgruppenbestimmungsaktivitäten** können Sie eine oder mehrere Zielgruppen erstellen, indem Sie eine Zielgruppe definieren und diese Zielgruppen mithilfe von Schnittmengen-, Vereinigungs- oder Ausschlussvorgängen teilen oder kombinieren.
* **Steuerungsaktivitäten** sind spezifisch für das Organisieren und Ausführen von Kompositionen. Sie ermöglichen die Koordinierung der anderen Aktivitäten.

## Zielgruppenbestimmungs-Aktivitäten

* [Aktivität Audience erstellen](build-audience.md): Definieren Sie Ihre Zielpopulation. Sie können entweder eine vorhandene Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.
* [Dimensionsänderung](change-dimension.md): Ändern Sie beim Erstellen Ihrer Komposition das Schema, auch als Zielgruppendimension bezeichnet.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Dubletten in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten zur Verarbeitung in Ihrer Komposition. Mit dieser Aktivität können Sie die eingehende Transition nutzen und entsprechend der Konfiguration der Aktivität die ausgehende Transition mit Zusatzdaten ergänzen.
* [Abstimmung](reconciliation.md): Definieren Sie die Verknüpfung zwischen den Daten in der Datenbank und den Daten in einer Arbeitstabelle, z. B. aus einer externen Datei geladene Daten.
* [Audience-Speicherung](save-audience.md): Aktualisieren Sie eine vorhandene Audience oder erstellen Sie eine neue Audience aus der zuvor in einer Komposition berechneten Population.
* [Aufteilen](split.md): Mit dieser Aktivität unterteilen Sie die eingehende Population in mehrere Teilmengen.

## Aktivitäten zur Flusskontrolle

* [AND-join](and-join.md): Synchronisieren Sie mehrere Ausführungszweige einer Komposition.
* **Ende** : Grafische Markierung des Endes einer Komposition. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
* [Verzweigung](fork.md): Mit dieser Aktivität erzeugen Sie ausgehende Transitionen, um parallel mehrere Aktivitäten zu starten.
* [Planer](scheduler.md): Planen Sie den Beginn der Komposition ein.
* [Warten](wait.md): Halten Sie die Ausführung eines Teils einer Komposition vorübergehend an.
