---
audience: end-user
title: Verwenden der Aktivität Dimensionsänderung
description: Erfahren Sie, wie Sie die Aktivität der Dimensionsänderung verwenden
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 29%

---


# Ändern der Dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Aktivität „Dimensionsänderung“"
>abstract="Diese Aktivität ermöglicht es Ihnen, das Schema, die Zielgruppendimension, während der Erstellung einer Audience zu ändern. Die Achse wird je nach Datenvorlage und Eingabeschema verschoben. Sie können beispielsweise vom Schema &quot;Verträge&quot;zum Schema &quot;Kunden&quot;wechseln."

Die **Dimensionsänderung** Aktivität ermöglicht Ihnen, das Schema, die Zielgruppendimension, während der Erstellung Ihrer Audience zu ändern. Die Achse wird je nach Datenvorlage und Eingabeschema verschoben.

## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **Dimensionsänderung** zu konfigurieren:

1. Hinzufügen einer **Dimensionsänderung** Aktivität zu Ihrer Komposition hinzufügen.

   ![](../assets/change-dimension.png)

1. Definieren Sie die **Neues Schema**. Während der Schemaänderung werden alle Datensätze beibehalten.

1. Führen Sie die Komposition aus, um das Ergebnis anzuzeigen. Vergleichen Sie die Daten in den Tabellen vor und nach dem **Dimensionsänderung** und die Struktur der Kompositionstabellen vergleichen.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->