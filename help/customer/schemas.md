---
audience: end-user
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie mit Schemata beginnen
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 75d539eef7b36b721c0df52b2fe9115728cf14d3
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 20%

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

Ein Schema ist eine Darstellung einer Tabelle Ihrer Datenbank. Es ist ein Objekt innerhalb der Anwendung, das definiert, wie die Daten mit Datenbanktabellen verknüpft werden.

Durch Erstellung eines Schemas haben Sie die Möglichkeit, Ihre Tabelle in FAC zu bearbeiten:
- Geben Sie ihm einen Anzeigenamen und eine Beschreibung, um das Verständnis für den Benutzer zu vereinfachen
- die Sichtbarkeit der einzelnen Felder entsprechend ihrer tatsächlichen Nutzung bestimmen;
- Wählen Sie den Primärschlüssel aus, um Schemas wie im [Datenmodell](../data-management/gs-models.md#data-model-start) benötigt zwischen ihnen zu verknüpfen.

## Erstellen eines Schemas {#schema-create}

Gehen Sie wie folgt vor, um Schemas in FAC zu erstellen:
Wechseln Sie im Abschnitt **[!UICONTROL FEDERATED DATA]** in den Link **[!UICONTROL Modelle]** . Dort finden Sie die Registerkarte **[!UICONTROL Schema]**.
Klicken Sie auf die Schaltfläche **[!UICONTROL Schema erstellen]** .

![](assets/schema_create.png){zoomable="yes"}

Sie haben Zugriff auf eine neue Benutzeroberfläche mit einer Dropdown-Liste, in der Sie
alle Datenbanken, die mit Ihrer Anwendung verbunden sind. Erfahren Sie mehr über die [Datenbankverbindung](../connections/connections.md#connections-fdb).
Wählen Sie Ihre Quelldatenbank in der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Tabellen hinzufügen]** .

![](assets/schema_tables.png){zoomable="yes"}

Sie haben Zugriff auf die Liste aller Tabellen in der Datenbank.

Durch Hinzufügen der Tabellen, für die Sie das Schema erstellen möchten, haben Sie Zugriff auf die entsprechenden Felder wie unten dargestellt.

![](assets/schema_fields.png){zoomable="yes"}

Für jede Tabelle haben Sie folgende Möglichkeiten:
- Benennen Sie die angegebene Schemakennung um.
- Beschreibung hinzufügen
- benennen Sie alle Felder um und legen Sie deren Sichtbarkeit fest.
- Primärschlüssel des Schemas auswählen

Beispielsweise wird hier eine Tabelle importiert, direkt nach dem Hinzufügen :

![](assets/schema_lumaorder.png){zoomable="yes"}

Das Schema kann wie folgt definiert werden:

![](assets/schema_lumaorders.png){zoomable="yes"}

## Schema bearbeiten {#schema-edit}

Um ein Schema zu bearbeiten, klicken Sie auf den Namen Ihres Schemas im Ordner Schemas . Sie haben Zugriff auf die Seite unten.
Klicken Sie auf die Schaltfläche **[!UICONTROL Bearbeiten]** .

![](assets/schema_edit.png){zoomable="yes"}

Sie haben Zugriff auf die gleiche Möglichkeit wie beim Erstellen des Schemas :
- Benennen Sie die angegebene Schemakennung um.
- Beschreibung hinzufügen
- benennen Sie alle Felder um und legen Sie deren Sichtbarkeit fest.
- Primärschlüssel des Schemas auswählen

![](assets/schema_edit_orders.png){zoomable="yes"}

## Datenvorschau in einem Schema {#schema-preview}

Um eine Vorschau der Daten in der Tabelle anzuzeigen, die durch Ihr Schema dargestellt wird, gehen Sie zur Registerkarte **[!UICONTROL Daten]** , wie unten dargestellt.
Sie können die Gesamtzahl der Aufzeichnungen anzeigen, indem Sie auf den Link **[!UICONTROL Berechnen]** klicken.

![](assets/schema_data.png){zoomable="yes"}

Sie können die Datenübersicht durch Klicken auf die Schaltfläche **[!UICONTROL Spalten konfigurieren]** ändern.

![](assets/schema_columns.png){zoomable="yes"}

## Löschen eines Schemas {#schema-delete}

Um ein Schema zu löschen, klicken Sie auf die Schaltfläche **[!UICONTROL Mehr]** und dann auf **[!UICONTROL Löschen]**.

![](assets/schema_delete.png){zoomable="yes"}