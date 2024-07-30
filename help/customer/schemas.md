---
audience: end-user
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie mit Schemata beginnen
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 43e43d2600edc9e8c2aeb5713fba50ff4da8e2eb
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 22%

---

# Erste Schritte mit Schemata {#schemas}

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Tabellen auswählen"
>abstract="Wählen Sie die Tabellen aus, die für das Datenmodell hinzugefügt werden sollen."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Schlüssel"
>abstract="Wählen Sie einen Schlüssel für die Datenabstimmung aus."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Name des Schemas"
>abstract="Geben Sie den Namen des Schemas ein."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Beschreibung des Schemas"
>abstract="Die Beschreibung des Schemas listet Spalten, Typen und Bezeichnungen auf. Sie können auch den Abstimmschlüssel für das Schema überprüfen. Um die Definition des Schemas zu aktualisieren, klicken Sie auf das Stiftsymbol."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Quelldatenbank zum Filtern auswählen"
>abstract="Sie können die Schemata nach ihrer Quelle filtern. Wählen Sie eine oder mehrere föderierte Datenbanken aus, um deren Schemata anzuzeigen."

## Was ist ein Schema {#schema-start}

Ein Schema ist eine Darstellung einer Tabelle Ihrer Datenbank. Es ist ein Objekt innerhalb der Anwendung, das definiert, wie die Daten mit Datenbanktabellen verknüpft werden.

Durch Erstellung eines Schemas können Sie eine Darstellung Ihrer Tabelle in der Experience Platform Federated Audience Komposition definieren:

* Geben Sie ihm einen Anzeigenamen und eine Beschreibung, um das Verständnis für den Benutzer zu vereinfachen
* Definieren Sie die Sichtbarkeit jedes Felds entsprechend seiner tatsächlichen Nutzung.
* Wählen Sie den Primärschlüssel aus, um Schemas wie im [Datenmodell](../data-management/gs-models.md#data-model-start) benötigt zwischen ihnen zu verknüpfen.

>[!IMPORTANT]
>
>Es wird empfohlen, für jede Sandbox unterschiedliche Federated-Datenbankschemata zu verwenden.

## Erstellen eines Schemas {#schema-create}

Gehen Sie wie folgt vor, um Schemas in Federated Audience Komposition zu erstellen:

1. Wechseln Sie im Abschnitt **[!UICONTROL FEDERATED DATA]** in den Link **[!UICONTROL Modelle]** . Navigieren Sie zur Registerkarte **[!UICONTROL Schema]** und klicken Sie auf die Schaltfläche **[!UICONTROL Schema erstellen]** .

   ![](assets/schema_create.png){zoomable="yes"}

   In diesem Schritt können Sie auf einen neuen Bildschirm mit einer Dropdown-Liste zugreifen, in der Sie die mit Ihrer Umgebung verbundenen Datenbanken finden. Weitere Informationen zur Datenbankverbindung finden Sie in [diesem Abschnitt](../connections/connections.md#connections-fdb).

1. Wählen Sie Ihre Quelldatenbank in der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Tabellen hinzufügen]** .

   ![](assets/schema_tables.png){zoomable="yes"}

   Daraufhin wird die Liste aller Tabellen in der Datenbank angezeigt.

1. Durch Hinzufügen der Tabellen, für die Sie das Schema erstellen möchten, haben Sie Zugriff auf die entsprechenden Felder wie folgt:

   ![](assets/schema_fields.png){zoomable="yes"}

   Für jede Tabelle haben Sie folgende Möglichkeiten:

   * den Titel des Schemas ändern
   * Beschreibung hinzufügen
   * benennen Sie alle Felder um und legen Sie deren Sichtbarkeit fest.
   * Primärschlüssel des Schemas auswählen

   Beispielsweise wurde für die folgende Tabelle importiert:

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   Das Schema kann wie folgt definiert werden:

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## Schema bearbeiten {#schema-edit}

So bearbeiten Sie ein Schema:

1. Klicken Sie auf den Namen Ihres Schemas im Ordner Schemas .

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Bearbeiten]** .

   ![](assets/schema_edit.png){zoomable="yes"}

   Sie können auf dieselben Optionen zugreifen wie beim Erstellen eines Schemas ](#schema-create).[

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Datenvorschau in einem Schema {#schema-preview}

Um eine Vorschau der Daten in der Tabelle anzuzeigen, die durch Ihr Schema dargestellt wird, gehen Sie zur Registerkarte **[!UICONTROL Daten]** , wie unten dargestellt.

Klicken Sie auf den Link **[!UICONTROL Berechnen]** , um eine Vorschau der Gesamtzahl der Aufzeichnungen anzuzeigen.

![](assets/schema_data.png){zoomable="yes"}

Klicken Sie auf die Schaltfläche **[!UICONTROL Spalten konfigurieren]** , um die Datenanzeige zu ändern.

![](assets/schema_columns.png){zoomable="yes"}

## Löschen eines Schemas {#schema-delete}

Um ein Schema zu löschen, klicken Sie auf die Schaltfläche **[!UICONTROL Mehr]** und wählen Sie dann **[!UICONTROL Löschen]** aus.

![](assets/schema_delete.png){zoomable="yes"}
