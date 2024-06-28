---
audience: end-user
title: Verwenden der Aktivität Dimensionsänderung
description: Erfahren Sie, wie Sie die Aktivität der Dimensionsänderung verwenden
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 56%

---

# Ändern der Dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Aktivität „Dimensionsänderung“"
>abstract="Mithilfe dieser Aktivität können Sie die Zielgruppendimension beim Erstellen einer Zielgruppe ändern. Diese Aktivität verschiebt die Achse je nach Datenvorlage und der Eingabedimension. Beispielsweise können Sie von der Dimension „Verträge“ zur Dimension „Kundinnen und Kunden“ wechseln."

Die **Dimensionsänderung** ermöglicht es Ihnen, die Zielgruppendimension während der Erstellung Ihrer Audience zu ändern. Die Achse wird entsprechend der Datenvorlage und der Eingabedimension verschoben. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->


## Konfigurieren der Aktivität „Dimensionsänderung“ {#configure}

Gehen Sie folgendermaßen vor, um die Aktivität **Dimensionsänderung** zu konfigurieren:

1. Hinzufügen einer **Dimensionsänderung** Aktivität zu Ihrer Komposition hinzufügen.

1. Definieren Sie die **neue Zielgruppendimension**. Bei Dimensionsänderung werden alle Datensätze beibehalten.

1. Führen Sie die Komposition aus, um das Ergebnis anzuzeigen. Vergleichen Sie die Daten in den Tabellen vor und nach der Aktivität Dimensionsänderung und vergleichen Sie die Struktur der Kompositionstabellen.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->
