---
audience: end-user
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie mit Schemata beginnen.
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 98%

---

# Überblick über Schemata {#schemas}

>[!AVAILABILITY]
>
>Um auf Schemata zugreifen zu können, benötigen Sie eine der folgenden Berechtigungen:
>
>-**Föderiertes Schema verwalten**
>-**Föderiertes Schema anzeigen**
>
>Weitere Informationen zu den erforderlichen Berechtigungen finden Sie im [Handbuch zur Zugriffssteuerung](/help/governance-privacy-security/access-control.md).

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
>abstract="Die Beschreibung des Schemas listet Spalten, Typen und Bezeichnungen auf. Man kann auch den Abstimmschlüssel für das Schema überprüfen. Um die Schemadefinition zu aktualisieren, klicken Sie auf das Stiftsymbol."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Quelldatenbank zum Filtern auswählen"
>abstract="Sie können die Schemata nach ihrer Quelle filtern. Wählen Sie eine oder mehrere föderierte Datenbanken aus, um deren Schemata anzuzeigen."

Ein Schema ist eine Darstellung einer Tabelle Ihrer Datenbank. Es ist ein Objekt innerhalb der Anwendung, das definiert, wie die Daten mit Datenbanktabellen verknüpft werden.

Durch Erstellung eines Schemas können Sie eine Darstellung Ihrer Tabelle in der Komposition föderierter Zielgruppen in Experience Platform definieren:

* Geben Sie einen Anzeigenamen und eine gute Beschreibung ein, um das Verständnis für Benutzende zu erleichtern
* Bestimmen Sie die Sichtbarkeit der einzelnen Felder entsprechend ihrer tatsächlichen Verwendung.
* Wählen Sie den Primärschlüssel, um die Schemata untereinander zu verknüpfen, wie es im [Datenmodell](../data-modelling/models.md#data-model-start) erforderlich ist.

>[!CAUTION]
>
>Wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden, müssen Sie unterschiedliche Arbeitsschemata verwenden.

## Erstellen eines Schemas {#schema-create}

Um in Komposition föderierter Zielgruppen ein Schema zu erstellen, wählen Sie im Abschnitt **[!UICONTROL Föderierte Daten]** die Option **[!UICONTROL Modelle]** aus. Wählen Sie auf der Registerkarte **[!UICONTROL Schema]** die Option **[!UICONTROL Schema erstellen]** aus.

![Die Schaltfläche „Schema erstellen“ ist im Schemaabschnitt „Komposition föderierter Zielgruppen“ hervorgehoben.](assets/schemas/schema_create.png){zoomable="yes"}

Das Popup-Fenster **[!UICONTROL Föderierte Datenbank auswählen]** erscheint. In diesem Popup-Fenster können Sie die [Quelldatenbank](/help/connections/home.md) auswählen, gefolgt von **[!UICONTROL Weiter]**.


![](assets/schemas/schema_tables.png){zoomable="yes"}

Das Popup-Fenster **Tabelle auswählen** erscheint. In diesem Popup-Fenster können Sie die Tabellen auswählen, die Sie zum Erstellen des Schemas verwenden möchten.

![Das Popup-Fenster „Tabelle auswählen“ wird angezeigt.](assets/schemas/select-table.png){zoomable="yes"}

Jede ausgewählte Tabelle generiert ein Schema mit den ausgewählten Spalten. Für jede Tabelle können Sie das Label des Schemas ändern, eine Beschreibung hinzufügen, den Feldtitel umbenennen, die Sichtbarkeit des Feldtitels festlegen und den Primärschlüssel für das Schema auswählen.

![](assets/schemas/schema-fields.png){zoomable="yes"}

>[!NOTE]
>
>Wenn Sie **[!UICONTROL Zusammengesetzten Schlüssel verwenden]** aktivieren, aber nur einen zu verwendenden Schlüssel auswählen, wird der Schlüssel wie der Primärschlüssel eines Standardschemas behandelt.

Darüber hinaus können Sie einen Schlüssel erstellen, der aus mehreren Schemaspalten besteht. Aktivieren Sie **[!UICONTROL Zusammengesetzten Schlüssel verwenden]** und markieren Sie die Schlüssel, die Sie als zusammengesetzten Schlüssel verwenden möchten.

![](assets/schemas/composite-key.png){zoomable="yes"}

Wählen Sie nach Abschluss der Konfiguration **[!UICONTROL Fertig]** aus, um die Erstellung Ihres Schemas abzuschließen.

## Bearbeiten eines Schemas {#schema-edit}

Wählen Sie zum Bearbeiten eines Schemas das zuvor erstellte Schema auf der Seite **Schemata** aus.

Die Seite mit den Schemadetails wird angezeigt. Klicken Sie auf das ![Stiftsymbol](/help/assets/icons/edit.png), um das Schema zu bearbeiten.

![](assets/schemas/schema_edit.png){zoomable="yes"}

Im Fenster **[!UICONTROL Schema bearbeiten]** können Sie die gleichen Optionen aufrufen und konfigurieren wie beim [Erstellen eines Schemas](#schema-create).

![](assets/schemas/schema_edit_orders.png){zoomable="yes"}

## Vorschau von Daten in einem Schema {#schema-preview}

Um eine Vorschau der Daten in der Tabelle anzuzeigen, die durch Ihr Schema dargestellt wird, gehen Sie zur Registerkarte **[!UICONTROL Daten]**, wie unten dargestellt.

Wählen Sie den Link **[!UICONTROL Berechnen]** aus, um eine Vorschau der Gesamtzahl der Aufzeichnungen anzuzeigen.

![](assets/schemas/schema_data.png){zoomable="yes"}

Wählen Sie die Schaltfläche **[!UICONTROL Spalten konfigurieren]** aus, um die Datenanzeige zu ändern.

![](assets/schemas/schema_columns.png){zoomable="yes"}

## Aktualisieren eines Schemas {#schema-refresh}

Tabellen in einer föderierten Datenbank können aktualisiert, hinzugefügt oder entfernt werden. Sie müssen dann das Schema in Adobe Experience Platform aktualisieren, um es an die neuesten Änderungen anzupassen. Wählen Sie dazu das ![Symbol mit den drei Punkten](/help/assets/icons/more.png) neben dem Namen des Schemas und dann die Option **[!UICONTROL Schema aktualisieren]** aus.

Sie können die Schemadefinition auch bei der Bearbeitung aktualisieren.

![](assets/schemas/schema_refresh.png){zoomable="yes"}

## Löschen eines Schemas {#schema-delete}

Um ein Schema zu löschen, wählen Sie das ![Symbol mit den drei Punkten](/help/assets/icons/more.png) und dann die Option **[!UICONTROL Löschen]** aus.

![](assets/schemas/schema_delete.png){zoomable="yes"}
