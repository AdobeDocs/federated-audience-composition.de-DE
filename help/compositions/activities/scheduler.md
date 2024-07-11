---
audience: end-user
title: Planungsaktivität verwenden
description: Erfahren Sie, wie Sie die Aktivität Planung verwenden
source-git-commit: 4dca96ae81d1f70c8f20509fdbd9ec31e05c01dc
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 47%

---


# Planung {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Planungsaktivität"
>abstract="Mit der Aktivität **Planung** können Sie planen, wann der Workflow gestartet werden soll. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität des Workflows verwendet werden."

Die Aktivität **Planung** ist eine Aktivität zur **Flusssteuerung**. Damit können Sie planen, wann die Komposition beginnt. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität der Komposition verwendet werden.

## Konfigurieren der Aktivität „Planung“ {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Gültigkeit der Planung"
>abstract="Sie können einen Gültigkeitszeitraum für die Planung definieren. Er kann dauerhaft sein (Standard) oder bis zu einem bestimmten Datum gültig sein."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Planungsoptionen"
>abstract="Definieren Sie die Häufigkeit der Planung. Er kann zu einem bestimmten Zeitpunkt, einmal oder mehrmals pro Tag, Woche oder Monat, ausgeführt werden."

Gehen Sie folgendermaßen vor, um die Aktivität **Planung** zu konfigurieren:

1. Fügen Sie eine **Planungsaktivität** zu Ihrem Workflow hinzu.

1. Konfigurieren Sie die **Ausführungshäufigkeit**:

   * **Einmal**: Die Komposition wird ein einziges Mal ausgeführt.

   * **Täglich**: Die Komposition wird einmal täglich zu einem bestimmten Zeitpunkt ausgeführt.

   * **Mehrmals am Tag:** die Komposition wird regelmäßig mehrmals am Tag ausgeführt. Sie können Ausführungen zu bestimmten Zeiten oder in regelmäßigen Abständen einrichten.

     >[!NOTE]
     >
     >Planen Sie nicht, dass eine Komposition mehr als alle 15 Minuten ausgeführt wird, da dies die Gesamtleistung des Systems beeinträchtigen und Blöcke in der Datenbank erstellen kann.

   * **Wöchentlich**: Die Komposition wird wiederholt zu bestimmten Zeiten in der Woche ausgeführt.

   * **Monatlich**: Die Komposition wird wiederholt zu bestimmten Zeiten im Monat ausgeführt. Sie können Monate auswählen, in denen die Komposition ausgeführt werden soll. Sie können für die Ausführung von Workflows auch bestimmte Wochentage des Monats auswählen, z. B. am zweiten Dienstag des Monats.

1. Definieren Sie die Ausführungsdetails. Je nach gewählter Frequenz sind verschiedene Parameter (Uhrzeit, Ausführungsintervall, bestimmte Tage etc.) zu konfigurieren.

1. Klicks **Vorschau der Startzeiten anzeigen** um den Zeitplan der nächsten zehn Ausführungen Ihres Aufsatzes zu überprüfen.

1. Definieren Sie den Gültigkeitszeitraum der Planung:

   * **Dauerhaft (nie abläuft)**: Die Komposition wird in der angegebenen Häufigkeit ausgeführt, ohne dass der Zeitrahmen oder die Anzahl der Iterationen begrenzt werden.

   * **Gültigkeitszeitraum**: Die Komposition wird in der angegebenen Häufigkeit bis zu einem bestimmten Datum ausgeführt. Sie müssen Start- und Enddaten angeben.

>[!NOTE]
>
>Wenn Sie die Komposition sofort starten möchten, können Sie auf die **Ausstehende Aufgabe ausführen** in der oberen Symbolleiste der Planung. Diese Schaltfläche ist nur verfügbar, wenn Sie mit der Komposition begonnen haben.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->

