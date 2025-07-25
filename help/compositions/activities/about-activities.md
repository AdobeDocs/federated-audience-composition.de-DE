---
audience: end-user
title: Arbeiten mit Aktivitäten
description: Erfahren Sie, wie Sie mit Aktivitäten arbeiten
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: ht
source-wordcount: '289'
ht-degree: 100%

---

# Arbeiten mit Aktivitäten {#activities}

In der Komposition föderierter Zielgruppen können Sie Kompositionen mit zwei Arten von Aktivitäten erstellen:

* Mit **Aktivitäten zur Zielgruppenbestimmung** können Sie ein oder mehrere Ziele erstellen, indem Sie eine Zielgruppe definieren und diese Zielgruppen mithilfe von Vorgängen wie Schnittmenge, Vereinigung oder Ausschluss aufteilen oder kombinieren.
* Die Aktivitäten zur **Flusssteuerung** sind speziell auf die Organisation und Ausführung von Kompositionen ausgerichtet. Ihre Hauptaufgabe besteht darin, die anderen Aktivitäten zu koordinieren.

## Aktivitäten zur Zielgruppenbestimmung

* [Aktivität „Zielgruppe erstellen“](build-audience.md): Definieren Sie Ihre Zielpopulation. Sie können entweder eine bestehende Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.
* [Datenquelle ändern](./change-data-source.md): Ändern Sie die von Ihrer Komposition verwendete Datenquelle.
* [Dimensionsänderung](change-dimension.md): Ändern Sie das Schema, auch bekannt als Zielgruppendimension, während Sie Ihre Komposition erstellen.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Dubletten in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten, die in Ihrer Komposition verarbeitet werden sollen. Mit dieser Aktivität können Sie die eingehende Transition nutzen und die Aktivität so konfigurieren, dass sie die ausgehende Transition mit zusätzlichen Daten ergänzt.
* [Abstimmung](reconciliation.md): Definieren Sie die Verknüpfung zwischen den Daten in der Datenbank und den Daten in einer Arbeitstabelle, z. B. Daten, die aus einer externen Datei geladen wurden.
* [Zielgruppe speichern](save-audience.md): Aktualisieren Sie eine bestehende Zielgruppe oder erstellen Sie eine neue Zielgruppe aus der im Vorfeld einer Komposition berechneten Population.
* [Aufspaltung](split.md): Segmentieren Sie die eingehende Population in mehrere Teilmengen.

## Aktivitäten zur Flusssteuerung

* [Und-Verknüpfung](and-join.md): Synchronisieren Sie mehrere Ausführungszweige einer Komposition.
* **Ende**: Markieren Sie grafisch das Ende einer Komposition. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
* [Verzweigung](fork.md): Erstellen Sie ausgehende Transitionen, um mehrere Aktivitäten gleichzeitig zu starten.
* [Planung](scheduler.md): Planen Sie, wann die Komposition gestartet wird.
* [Warten](wait.md): Hält die Ausführung eines Teils einer Komposition kurzzeitig an.
