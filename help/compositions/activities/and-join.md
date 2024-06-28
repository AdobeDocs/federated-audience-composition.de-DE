---
audience: end-user
title: Verwenden der Und-Verknüpfung
description: Erfahren Sie, wie Sie die Und-Verknüpfung verwenden.
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 66%

---

# Und-Verknüpfung {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Aktivität &quot;Und-Verknüpfung&quot;"
>abstract="Die **Und-Verknüpfung** -Aktivität können Sie mehrere Ausführungszweige einer Komposition synchronisieren. Sie wird ausgelöst, sobald alle vorangehenden Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten beendet sind, bevor Sie mit der Ausführung der Komposition fortfahren."

Die **Und-Verknüpfung** -Aktivität können Sie mehrere Ausführungszweige einer Komposition synchronisieren.

Bei dieser Aktivität wird die ausgehende Transition erst aktiviert, wenn alle eingehenden Transitionen aktiviert wurden, d. h. wenn alle vorangehenden Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten abgeschlossen sind, bevor Sie mit der Ausführung der Komposition fortfahren.

## Konfigurieren der Aktivität „Und-Verknüpfung“ {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Konfigurieren der Aktivität „Und-Verknüpfung“"
>abstract="Wählen Sie die Aktivitäten aus, die Sie verknüpfen möchten. Wählen Sie in der Dropdown-Liste **Hauptmenge** die Population der eingehenden Transition aus, die Sie beibehalten möchten."

Führen Sie die folgenden Schritte aus, um die Aktivität **Und-Verknüpfung** zu konfigurieren:

1. Fügen Sie mehrere Aktivitäten wie z. B. Kanalaktivitäten hinzu, um mindestens zwei verschiedene Ausführungsverzweigungen zu bilden.
1. Fügen Sie die Aktivität **Und-Verknüpfung** zu einer der Verzweigungen hinzu.
1. Aktivieren Sie im Abschnitt **Zusammenführungsoptionen** alle vorherigen Aktivitäten, denen Sie beitreten möchten.
1. Wählen Sie in der Dropdown-Liste **Hauptmenge** die Population der eingehenden Transition aus, die Sie beibehalten möchten. Die ausgehende Transition darf nur eine der Populationen der eingehenden Transition enthalten.

