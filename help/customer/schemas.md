---
audience: end-user
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie mit Schemata beginnen.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 25a60847484aae0cb0dc8441e5dcc7968f8c1615
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 84%

---

# Erste Schritte mit Schemata {#schemas}

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Tabellen auswählen"
>abstract="Die Tabellen auswählen, die für das Datenmodell hinzugefügt werden sollen."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Schlüssel"
>abstract="Einen Schlüssel für die Datenabstimmung auswählen."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Name des Schemas"
>abstract="Den Namen des Schemas eingeben."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Beschreibung des Schemas"
>abstract="Die Beschreibung des Schemas listet Spalten, Typen und Bezeichnungen auf. Man kann auch den Abstimmschlüssel für das Schema überprüfen. Um die Definition des Schemas zu aktualisieren, auf das Stiftsymbol klicken."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Quelldatenbank zum Filtern auswählen"
>abstract="Sie können die Schemata nach ihrer Quelle filtern. Wählen Sie eine oder mehrere föderierte Datenbanken aus, um deren Schemata anzuzeigen."

## Was ist ein Schema {#schema-start}

Ein Schema ist eine Darstellung einer Tabelle Ihrer Datenbank. Es ist ein Objekt innerhalb der Anwendung, das definiert, wie die Daten mit Datenbanktabellen verknüpft werden.

Durch Erstellung eines Schemas können Sie eine Darstellung Ihrer Tabelle in der Komposition föderierter Zielgruppen in Experience Platform definieren:

* Geben Sie einen Anzeigenamen und eine gute Beschreibung ein, um das Verständnis für Benutzende zu erleichtern
* Bestimmen Sie die Sichtbarkeit der einzelnen Felder entsprechend ihrer tatsächlichen Verwendung.
* Wählen Sie den Primärschlüssel, um die Schemata untereinander zu verknüpfen, wie es im [Datenmodell](../data-management/gs-models.md#data-model-start) erforderlich ist.

>[!CAUTION]
>
>Wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden, müssen Sie unterschiedliche Arbeitsschemata verwenden.
>

## Erstellen eines Schemas {#schema-create}

Gehen Sie wie folgt vor, um Schemata in der Komposition föderierter Zielgruppen zu erstellen:

1. Navigieren Sie im Abschnitt **[!UICONTROL FÖDERIERTE DATEN]** zum Link **[!UICONTROL Modelle]**. Navigieren Sie zur Registerkarte **[!UICONTROL Schema]** und klicken Sie auf die Schaltfläche **[!UICONTROL Schema erstellen]**.

   ![](assets/schema_create.png){zoomable="yes"}

   Mit diesem Schritt erhalten Sie Zugang zu einem neuen Bildschirm mit einer Dropdown-Liste, in der Sie die mit Ihrer Umgebung verbundene(n) Datenbank(en) finden. Weiterführende Informationen zur Verbindung von Datenbanken finden Sie in [diesem Abschnitt](../connections/connections.md#connections-fdb)

1. Wählen Sie Ihre Quelldatenbank in der Liste aus und klicken Sie auf die Registerkarte **[!UICONTROL Tabellen hinzufügen]**.

   ![](assets/schema_tables.png){zoomable="yes"}

   Anschließend sehen Sie die Liste aller Tabellen in der Datenbank.

1. Indem Sie die Tabellen hinzufügen, für die das Schema erstellt werden soll, haben Sie Zugriff auf die entsprechenden Felder (siehe unten).

   ![](assets/schema_fields.png){zoomable="yes"}

   Für jede Tabelle können Sie folgende Vorgänge durchführen:

   * Ändern des Schema-Labels
   * Hinzufügen einer Beschreibung
   * Umbenennen aller Felder und Festlegen ihrer Sichtbarkeit
   * Auswählen des Primärschlüssels des Schemas

   Beispielsweise für die folgenden importierte Tabelle:

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   Das Schema kann wie folgt definiert werden:

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## Bearbeiten eines Schemas {#schema-edit}

Gehen Sie wie folgt vor, um ein Schema zu bearbeiten:

1. Klicken Sie in der Liste auf den Namen Ihres Schemas.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Bearbeiten]**.

   ![](assets/schema_edit.png){zoomable="yes"}

   Sie können auf dieselben Optionen zugreifen wie beim [Erstellen eines Schemas](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}


## Vorschau von Daten in einem Schema {#schema-preview}

Um eine Vorschau der Daten in der Tabelle anzuzeigen, die durch Ihr Schema dargestellt wird, gehen Sie zur Registerkarte **[!UICONTROL Daten]**, wie unten dargestellt.

Klicken Sie auf den Link **[!UICONTROL Berechnen]**, um eine Vorschau der Gesamtzahl der Aufzeichnungen anzuzeigen.

![](assets/schema_data.png){zoomable="yes"}

Klicken Sie auf die Schaltfläche **[!UICONTROL Spalten konfigurieren]**, um die Datenanzeige zu ändern.

![](assets/schema_columns.png){zoomable="yes"}


## Schema aktualisieren {#schema-refresh}

Tabellen in einer verbundenen Datenbank können aktualisiert, hinzugefügt oder entfernt werden. In diesem Fall müssen Sie das Schema in Adobe Experience Platform aktualisieren, um es an die neuesten Änderungen anzupassen. Klicken Sie dazu auf die drei Punkte neben dem Namen des zu aktualisierenden Schemas und wählen Sie **Schema aktualisieren** aus.

Sie können die Schemadefinition auch bei der Bearbeitung aktualisieren.

![](assets/schema_refresh.png){zoomable="yes"}


## Löschen eines Schemas {#schema-delete}

Klicken Sie zum Löschen eines Schemas auf die Schaltfläche **[!UICONTROL Mehr]** und dann auf **[!UICONTROL Löschen]**.

![](assets/schema_delete.png){zoomable="yes"}
