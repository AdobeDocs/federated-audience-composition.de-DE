---
audience: end-user
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie mit Schemata beginnen
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 96508e648b2f97dd9410df617ed3a5fd8b354b52
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 31%

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


## Was ist ein Schema? {#schema-start}

Ein Schema ist ein Objekt in der Anwendung, das definiert, wie die Daten mit Datenbanktabellen verknüpft werden.
Ein Schema verweist auf eine Tabelle.

## Wie erstelle ich ein Schema? {#schema-create}

Wechseln Sie im Abschnitt **[!UICONTROL FEDERATED DATA]** in den Link **[!UICONTROL Modelle]** . Dort finden Sie die Registerkarte **[!UICONTROL Schema]**.
Klicken Sie auf die Schaltfläche **[!UICONTROL Schema erstellen]** .

![](assets/schema_create.png){zoomable="yes"}

Wählen Sie Ihre Quelldatenbank in der Dropdownliste aus und klicken Sie auf die Registerkarte **[!UICONTROL Tabellen hinzufügen]** .

![](assets/schema_tables.png){zoomable="yes"}

Sie haben Zugriff auf alle Tabellen der Datenbank, für die Sie ein Schema erstellen können.

Durch das Hinzufügen der Tabellen haben Sie Zugriff auf die entsprechenden Felder und können so die tatsächlich benötigten Daten speichern.

![](assets/schema_fields.png){zoomable="yes"}

## Wie kann ein Schema bearbeitet werden? {#schema-edit}

Um ein Schema zu bearbeiten, klicken Sie auf den Namen Ihres Schemas im Ordner Schemas . Sie haben Zugriff auf die Seite unten.
Klicken Sie auf die Schaltfläche **[!UICONTROL Bearbeiten]** .

![](assets/schema_edit.png){zoomable="yes"}

## Datenvorschau in einem Schema {#schema-preview}

Um eine Vorschau der Daten in der Tabelle anzuzeigen, die durch Ihr Schema dargestellt wird, gehen Sie zur Registerkarte **[!UICONTROL Daten]** , wie unten dargestellt.

![](assets/schema_data.png){zoomable="yes"}

Sie können die Datenübersicht durch Klicken auf die Schaltfläche **[!UICONTROL Spalten konfigurieren]** ändern.

![](assets/schema_columns.png){zoomable="yes"}

## Wie lösche ich ein Schema? {#schema-delete}

Um ein Schema zu löschen, klicken Sie auf die Schaltfläche **[!UICONTROL Mehr]** und dann auf **[!UICONTROL Löschen]**.

![](assets/schema_delete.png){zoomable="yes"}