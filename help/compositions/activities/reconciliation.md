---
audience: end-user
title: Verwenden der Aktivität „Abstimmung“
description: Erfahren Sie, wie Sie die Aktivität „Abstimmung“ verwenden.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 933c3cba-9120-4a93-a668-866fb65ee197
source-git-commit: 682695357a9bd8f351b5152becd33088fa16f622
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 91%

---

# Abstimmung {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Aktivität „Abstimmung“"
>abstract="Mit der Aktivität **Abstimmung** können Sie die Verknüpfung zwischen den Daten in der Datenbank und den Daten in einer Arbeitstabelle definieren."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Abstimmung – Feld auswählen"
>abstract="Abstimmung – Feld auswählen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Abstimmung – Bedingung erstellen"
>abstract="Abstimmung – Bedingung erstellen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Abstimmung – Komplement erzeugen"
>abstract="Abstimmung – Komplement erzeugen"

Mit der Aktivität **Abstimmung** können Sie die Verknüpfung zwischen den Daten in der Datenbank und den Daten in einer Arbeitstabelle zu definieren, z. B. Daten, die aus einem externen System geladen werden.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

Sie ermöglicht Ihnen, nicht identifizierte Daten mit bestehenden Ressourcen zu verknüpfen. Der Abstimmungsvorgang setzt voraus, dass die Daten, die Sie zusammenführen, bereits in der Datenbank vorhanden sind. Wenn Sie beispielsweise Bestellinformationen abstimmen möchten, die zeigen, welches Produkt wann von welchem Kunden gekauft wurde, müssen sowohl das Produkt als auch der Kunde bereits in der Datenbank vorhanden sein.

## Konfigurieren der Abstimmungsaktivität {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Wählen Sie das neue Schema aus, das auf die Daten angewendet werden soll. Mit einem Schema, auch bekannt als Zielgruppendimension, können Sie die Zielgruppen definieren: Empfängerinnen und Empfänger, Abonnentinnen und Abonnenten der App, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw.  Standardmäßig ist das aktuelle Schema der Komposition ausgewählt. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Abstimmungsregeln"
>abstract="Wählen Sie die für die Deduplizierung zu verwendenden Abstimmungsregeln aus. Um Attribute zu verwenden, wählen Sie die Option **Einfache Attribute** und dann die Quell- und Zielfelder aus. Um mithilfe des Abfrage-Modelers eine eigene Abstimmbedingung zu erstellen, wählen Sie die Option **Erweiterte Abstimmbedingungen** aus."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Auswählen der Zielgruppendimension"
>abstract="Wählen Sie das Schema, auch bekannt als Zielgruppendimension, für Ihre eingehenden Daten zum Abstimmen aus."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Beibehalten nicht abgestimmter Daten"
>abstract="Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und stehen in der Arbeitstabelle zur späteren Verwendung zur Verfügung. Um nicht abgestimmte Daten zu entfernen, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Abstimmungsattribut"
>abstract="Wählen Sie das Attribut aus, das zur Abstimmung der Daten verwendet werden soll, und bestätigen Sie den Vorgang."

Gehen Sie wie folgt vor, um die Aktivität **Abstimmung** zu konfigurieren:

1. Fügen Sie eine Aktivität **Abstimmung** zu Ihrer Komposition hinzu.

1. Wählen Sie das **neue Schema** aus. Mit einem Schema, auch bekannt als Zielgruppendimension, können Sie die Zielgruppen definieren: Empfängerinnen und Empfänger, Abonnentinnen und Abonnenten der App, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw.

1. Wählen Sie die für Abstimmung zu verwendenden Felder aus. Sie können mehrere Abstimmkriterien verwenden.

   1. Um Attribute zur Abstimmung von Daten zu verwenden, wählen Sie die Option **Einfache Attribute** aus und klicken Sie dann auf die Schaltfläche **Regel hinzufügen**.
   1. Wählen Sie die Felder **Quelle** und **Ziel** für die Abstimmung aus. Das Feld **Quelle** . Das Feld **Ziel** entspricht den Feldern des ausgewählten Schemas.

      Daten werden abgestimmt, wenn Quelle und Ziel gleich sind. Wählen Sie beispielsweise die **E-Mail**-Felder, um Profile anhand ihrer E-Mail-Adresse zu deduplizieren.

      Um weitere Abstimmungskriterien hinzuzufügen, klicken Sie auf die Schaltfläche **Regel hinzufügen**. Wenn mehrere Bedingungen für die Verknüpfung angegeben werden, müssen ALLE erfüllt sein, damit die Relation hergestellt werden kann.

      ![](../assets/reconciliation-rules.png)

   1. Um andere Attribute zur Abstimmung von Daten zu verwenden, wählen Sie die Option **Erweiterte Abstimmbedingungen** und danach die Schaltfläche **Bedingungen erstellen** aus. Sie können dann mit dem Abrfrage-Modeler Ihre eigene Abstimmbedingung erstellen. [Erfahren Sie mehr über die Arbeit mit dem Abfrage-Modeler](../../query/query-modeler-overview.md)

      ![](../assets/reconciliation-advanced.png)

1. Mithilfe der Schaltfläche **Filter erstellen** können Sie Daten zur Abstimmung filtern. Auf diese Weise können Sie mithilfe des Abfrage-Modelers eine benutzerdefinierte Bedingung erstellen.

Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und stehen in der Arbeitstabelle zur zukünftigen Verwendung zur Verfügung. Um nicht abgestimmte Daten zu entfernen, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
