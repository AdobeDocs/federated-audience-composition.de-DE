---
audience: end-user
title: Verwenden der Aktivität Audience erstellen
description: Erfahren Sie, wie Sie die Aktivität Audience erstellen verwenden
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 53%

---


# Zielgruppe erstellen {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Aktivität „Zielgruppe erstellen“"
>abstract="Die **Audience erstellen** -Aktivität können Sie die Audience definieren, die in die Komposition eintreten soll."

Die **Audience erstellen** -Aktivität können Sie die Audience definieren, die in die Komposition eintreten soll.

Zur Definition der Zielgruppenpopulation haben Sie folgende Möglichkeiten:

<!--* Select an existing audience, created as a list in the client console.-->
* Wählen Sie eine Adobe Experience Platform-Zielgruppe aus.
* Erstellen Sie mit dem Abfrage-Modeler eine neue Zielgruppe, indem Sie Filterkriterien definieren und kombinieren.

Die **Audience erstellen** -Aktivitäten können am Anfang der Komposition oder nach jeder anderen Aktivität platziert werden. Jede Aktivität kann nach der **Audience erstellen**.

## Konfigurieren der Aktivität „Zielgruppe erstellen“ {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Zielgruppe"
>abstract="Wählen Sie Ihre Zielgruppe aus."

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe erstellen** zu konfigurieren:

1. Fügen Sie die Aktivität **Zielgruppe erstellen** hinzu.
1. Definieren Sie einen Titel.
1. Definieren Sie die Art der Zielgruppe: **Eigene erstellen** oder **Zielgruppe lesen**.
1. Konfigurieren Sie Ihre Zielgruppe anhand der Schritte in den unten stehenden Registerkarten.

>[!BEGINTABS]

>[!TAB Eigene erstellen (Abfrage)]

Gehen Sie wie folgt vor, um Ihre eigene Abfrage zu erstellen:

1. Wählen Sie **Eigene erstellen (Abfrage)** aus.
1. Wählen Sie die **Zielgruppendimension**. Die Zielgruppendimension ermöglicht die Bestimmung der vom Vorgang betroffenen Population: Empfängerinnen und Empfänger, Vertragsbegünstigte, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw. Standardmäßig wird die Zielgruppe aus den Empfängern ausgewählt.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Klicken Sie auf **Weiter**.
1. Verwenden Sie das Abfragemodell, um Ihre Abfrage zu definieren. Dies entspricht der Erstellung einer Audience bei der Erstellung einer neuen E-Mail. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Zielgruppe lesen]

Gehen Sie wie folgt vor, um eine vorhandene Zielgruppe auszuwählen:

1. Wählen Sie **Zielgruppe lesen** aus.
1. Klicken Sie auf **Weiter**.
1. Wählen Sie Ihre Audience auf die gleiche Weise aus wie eine Audience bei der Konzeption eines neuen Versands. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
