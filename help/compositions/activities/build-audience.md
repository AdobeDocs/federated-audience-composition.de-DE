---
audience: end-user
title: Verwenden der Aktivität Audience erstellen
description: Erfahren Sie, wie Sie die Aktivität Audience erstellen verwenden
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 54%

---


# Zielgruppe erstellen {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Aktivität „Zielgruppe erstellen“"
>abstract="Die Aktivität **Zielgruppe erstellen** ermöglicht Ihnen das Definieren der Zielgruppe, die in der Komposition aufgenommen wird."

Die Aktivität **Zielgruppe erstellen** ermöglicht Ihnen das Definieren der Zielgruppe, die in der Komposition aufgenommen wird.

Zur Definition der Zielgruppenpopulation haben Sie folgende Möglichkeiten:

<!--* Select an existing audience, created as a list in the client console.-->
* Wählen Sie eine Adobe Experience Platform-Zielgruppe aus.
* Erstellen Sie mit dem Abfrage-Modeler eine neue Zielgruppe, indem Sie Filterkriterien definieren und kombinieren.

Die Aktivität **Audience erstellen** kann am Anfang der Komposition oder nach jeder anderen Aktivität platziert werden. Jede Aktivität kann nach der **Build-Zielgruppe** platziert werden.

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
1. Klicken Sie auf **Weiter**.
1. Definieren Sie Ihre Abfrage mithilfe des Abfragemodells. [Erfahren sie mehr über die Arbeit mit dem Abfrage-Modeler](../../query/query-modeler-overview.md)

>[!TAB Zielgruppe lesen]

Gehen Sie wie folgt vor, um eine vorhandene Zielgruppe auszuwählen:

1. Wählen Sie **Zielgruppe lesen** aus.
1. Klicken Sie auf **Weiter**.
1. Wählen Sie Ihre Zielgruppe aus.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
