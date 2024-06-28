---
audience: end-user
title: Verwenden der Aktivität Audience-Speicherung
description: Erfahren Sie, wie Sie die Aktivität Verzweigung verwenden
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 67%

---

# Zielgruppe speichern {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Speichern einer Zielgruppe"
>abstract="Verwenden Sie diese Aktivität, um eine existierende Audience zu aktualisieren oder eine neue Audience aus der zuvor in der Komposition berechneten Population zu erstellen. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste hinzugefügt und sind über das Menü **Zielgruppen** zugänglich."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Ausgehende Transition generieren"
>abstract="Verwenden Sie diese Option, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Feld „Primäre Identität“"
>abstract="Wählen Sie die primäre Identität für Profile aus."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Weitere Informationen finden Sie in der Experience Platform-Dokumentation ."


>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Identity-Namespace"
>abstract="Wählen Sie den Namespace aus, der für Profile verwendet werden soll."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces" text="Weitere Informationen finden Sie in der Experience Platform-Dokumentation ."



Die **Audience-Speicherung** ermöglicht die Aktualisierung einer existierenden Audience oder die Erstellung einer neuen Audience aus der zuvor erstellten Population. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste in Adobe Campaign hinzugefügt und sind über das Menü **Zielgruppen** zugänglich.

Diese Aktivität dient im Wesentlichen dazu, innerhalb derselben Komposition berechnete Populationen in wiederverwendbare Zielgruppen umzuwandeln. Verbinden Sie sie mit anderen Zielgruppenbestimmungsaktivitäten, wie etwa den Aktivitäten **Zielgruppe aufbauen** oder **Kombinieren**.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe aufbauen** zu konfigurieren:

1. Hinzufügen einer **Audience-Speicherung** Aktivität zu Ihrer Komposition hinzufügen.

1. Wählen Sie im Dropdown-Menü **Modus** die Aktion aus, die Sie ausführen möchten:

   * **Erstellen oder Aktualisieren einer vorhandenen Zielgruppe**: Definieren Sie eine **Zielgruppenbezeichnung**. Wenn die Zielgruppe bereits existiert, wird sie aktualisiert, andernfalls wird eine neue Zielgruppe erstellt.

   * **Vorhandene Zielgruppe aktualisieren**: Wählen Sie die **Zielgruppe**, die Sie aktualisieren möchten, in der Liste der vorhandenen Zielgruppen aus.

1. Wählen Sie den **Aktualisierungsmodus** aus, der für vorhandene Zielgruppen gelten soll:

   * **Zielgruppeninhalt durch neue Daten ersetzen**: Der gesamte Inhalt der Zielgruppe wird ersetzt. Die zuvor enthaltenen Daten gehen dabei verloren. Nur die in der eingehenden Transition der Aktivität „Zielgruppe speichern“ übermittelten Daten werden beibehalten. Bei dieser Option werden Zielgruppendimension und -typ der aktualisierten Zielgruppe gelöscht.

   * **Zielgruppeninhalt mit den neuen Daten ergänzen**: Der alte Zielgruppeninhalt wird beibehalten und die Daten der eingehenden Transition der Aktivität „Zielgruppe speichern“ wird hinzugefügt.

1. Markieren Sie die Option **Ausgehende Transition erzeugen**, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten.

Der Inhalt der gespeicherten Zielgruppe ist anschließend in der Detailansicht der Zielgruppe verfügbar, auf die Sie im Menü **Zielgruppen** zugreifen können. Die in dieser Ansicht verfügbaren Spalten entsprechen den Spalten der eingehenden Transition der **Audience-Speicherung** -Aktivität.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
