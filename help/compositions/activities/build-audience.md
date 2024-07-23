---
audience: end-user
title: Verwenden der Aktivität Audience erstellen
description: Erfahren Sie, wie Sie die Aktivität Audience erstellen verwenden
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 71936c3fb6946ce9d4928499c96da39aaef49231
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 38%

---


# Zielgruppe erstellen {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Aktivität „Zielgruppe erstellen“"
>abstract="Die Aktivität **Zielgruppe erstellen** ermöglicht Ihnen das Definieren der Zielgruppe, die in der Komposition aufgenommen wird."

Mit der Aktivität **Audience erstellen** können Sie die Audience definieren, die in die Komposition eintreten soll. Zur Definition der Zielgruppenpopulation haben Sie folgende Möglichkeiten:

* Wählen Sie eine vorhandene Adobe Experience Platform-Zielgruppe aus.
* Erstellen Sie mit dem Abfragemodell eine neue Zielgruppe, indem Sie Filterkriterien definieren und kombinieren.

## Konfigurieren der Aktivität „Zielgruppe erstellen“ {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Zielgruppe"
>abstract="Wählen Sie Ihre Zielgruppe aus."

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe erstellen** zu konfigurieren:

1. Fügen Sie die Aktivität **Zielgruppe erstellen** hinzu.
1. Definieren Sie einen Titel.
1. Geben Sie an, ob Sie eine Audience erstellen oder eine existierende auswählen möchten.
1. Konfigurieren Sie Ihre Zielgruppe anhand der Schritte in den unten stehenden Registerkarten.

>[!BEGINTABS]

>[!TAB Erstellen einer Audience]

Gehen Sie wie folgt vor, um eine eigene Zielgruppe zu erstellen:

1. Wählen Sie **Zielgruppe erstellen** aus.
1. Wählen Sie das **Schema**, auch als Zielgruppendimension bezeichnet. Im Schema wird die durch den Vorgang ermittelte Population bestimmt: Empfänger, Empfänger, Benutzer, Abonnenten etc. Standardmäßig wird das Schema von den Empfängern ausgewählt.

   ![](../assets/build-audience-create.png)

1. Klicken Sie auf **Weiter**.
1. Definieren Sie mithilfe des Abfragemodells Ihre Abfrage und bestätigen Sie sie. [Erfahren sie mehr über die Arbeit mit dem Abfrage-Modeler](../../query/query-modeler-overview.md)

>[!TAB Zielgruppe lesen]

Gehen Sie wie folgt vor, um eine vorhandene Zielgruppe auszuwählen:

1. Wählen Sie **Zielgruppe lesen** aus.
1. Klicken Sie auf **Weiter**.

   ![](../assets/build-audience-read.png)

1. Wählen Sie Ihre Zielgruppe aus.

>[!ENDTABS]

>[!NOTE]
>
>Mit der Option **Ausgehende Transition erzeugen** können Sie eine ausgehende Transition hinzufügen, die am Ende der Ausführung der Aktivität aktiviert wird, wenn die Zielgruppe leer ist.

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
