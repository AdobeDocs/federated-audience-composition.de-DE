---
audience: end-user
title: Überblick über Schemata
description: Erfahren Sie, wie Sie in der Adobe Experience Platform-Benutzeroberfläche Schemas für die Federated Audience-Komposition erstellen und verwenden.
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 35%
---
# Überblick über Schemata {#schemas}

>[!AVAILABILITY]
>
>Das neue Schema-Erlebnis steht nur ausgewählten Kunden zur Verfügung. Weitere Informationen erhalten Sie bei der Adobe-Kundenunterstützung.
>
>Wenn Sie keinen Zugriff auf das neue Schemaerlebnis haben, lesen Sie den Abschnitt [Schemas - Übersicht](./schemas.md).
>
>Um auf Schemata zugreifen zu können, benötigen Sie eine der folgenden Berechtigungen:
>
>-**Verknüpftes Schema verwalten**
>-**Föderiertes Schema anzeigen**
>
>Weitere Informationen zu den erforderlichen Berechtigungen finden Sie im [Handbuch zur Zugriffssteuerung](/help/governance-privacy-security/access-control.md).

Ein Schema ist eine Darstellung einer Tabelle Ihrer Datenbank. Es ist ein Objekt innerhalb der Anwendung, das definiert, wie die Daten mit Datenbanktabellen verknüpft werden.

Durch Erstellung eines Schemas können Sie eine Darstellung Ihrer Tabelle in der Komposition föderierter Zielgruppen in Experience Platform definieren:

* Geben Sie einen Anzeigenamen und eine gute Beschreibung ein, um das Verständnis für Benutzende zu erleichtern
* Bestimmen Sie die Sichtbarkeit der einzelnen Felder entsprechend ihrer tatsächlichen Verwendung.
* Wählen Sie den Primärschlüssel, um die Schemata untereinander zu verknüpfen, wie es im [Datenmodell](../data-modelling/models.md#data-model-start) erforderlich ist.

>[!CAUTION]
>
>Wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden, müssen Sie unterschiedliche Arbeitsschemata verwenden.

## Erstellen eines Schemas {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="Konfiguration verwalten"
>abstract="Temporärer leerer Inhalt."

Um ein Schema in Federated Audience Composition zu erstellen, wählen Sie **[!UICONTROL Schemata]** im Abschnitt **[!UICONTROL Daten-Management]** der Benutzeroberfläche von Experience Platform aus. Wählen Sie in der Benutzeroberfläche „Schemata“ **[!UICONTROL Schema erstellen]**.

![Die Schaltflächen Schemata und Schema erstellen sind beide in der Benutzeroberfläche Schemata hervorgehoben.](/help/data-modelling/assets/integrated/select-create-schema.png)

Sobald das Popup „Schema erstellen“ angezeigt wird, wählen Sie **[!UICONTROL Relational]**, gefolgt von **[!UICONTROL Discover schemas]** und **[!UICONTROL Weiter]** aus, um ein Schema für die Federated Audience-Komposition zu erstellen.

![Die Schaltfläche „Schemata erkennen“ ist im Pop-up „Relationales Schema erstellen“ hervorgehoben.](/help/data-modelling/assets/integrated/select-discover-schemas.png)

Das Popup-Fenster **[!UICONTROL Föderierte Datenbank auswählen]** erscheint. In diesem Popup-Fenster können Sie die [Quelldatenbank](/help/connections/home.md) auswählen, gefolgt von **[!UICONTROL Weiter]**.

![Das Popover „Federated Database auswählen“ wird angezeigt.](/help/data-modelling/assets/integrated/select-federated-database.png)

## Schema definieren {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="Zusammengesetzter Schlüssel"
>abstract="Ein Schemaschlüssel, der aus mehreren Schemaspalten besteht. Markieren Sie die Spalten, die Sie als zusammengesetzten Schlüssel verwenden möchten."

Nachdem Sie die Federated Database ausgewählt haben, können Sie jetzt Ihr Schema definieren. Der **[!UICONTROL „Daten hinzufügen]** wird angezeigt. Auf dieser Seite können Sie auf **[!UICONTROL Tabelle hinzufügen]** klicken, um die Tabellen auszuwählen, die Sie zum Schema hinzufügen möchten.

![Die Schaltfläche „Tabelle hinzufügen“ ist im Bildschirm „Daten hinzufügen“ hervorgehoben.](/help/data-modelling/assets/integrated/select-add-table.png)

Das Popup-Fenster **[!UICONTROL Tabelle auswählen]** erscheint. In diesem Popup-Fenster können Sie die Tabellen auswählen, die Sie zum Erstellen des Schemas verwenden möchten.

![Das Popup-Fenster „Tabelle auswählen“ wird angezeigt.](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

Jede ausgewählte Tabelle generiert ein Schema mit den ausgewählten Spalten. Für jede Tabelle können Sie das Label des Schemas ändern, eine Beschreibung hinzufügen, den Feldtitel umbenennen, die Sichtbarkeit des Feldtitels festlegen und den Primärschlüssel für das Schema auswählen.

![Die ausgewählten Tabellen werden auf der Seite Daten hinzufügen angezeigt.](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>Wenn Sie **[!UICONTROL Zusammengesetzter Schlüssel]** auswählen, aber nur einen zu verwendenden Schlüssel, wird der Schlüssel wie ein standardmäßiger Schema-Primärschlüssel behandelt.

Darüber hinaus können Sie einen Schlüssel erstellen, der aus mehreren Schemaspalten besteht. Wählen Sie **[!UICONTROL Zusammengesetzter Schlüssel]** aus und markieren Sie die Schlüssel, die Sie als zusammengesetzten Schlüssel verwenden möchten.

![Sowohl der Umschalter Zusammengesetzter Schlüssel als auch die Schemata sind ausgewählt.](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

Wählen Sie nach Abschluss der Konfiguration **[!UICONTROL Fertig]** aus, um die Erstellung Ihres Schemas abzuschließen.

## Bearbeiten eines Schemas {#schema-edit}

Um ein Schema zu bearbeiten, klicken Sie auf das ![Auslassungssymbol](/help/assets/icons/more.png) neben Ihrem zuvor erstellten Schema auf der Seite **Schemata** und klicken Sie dann auf **[!UICONTROL Bearbeiten]**.

![Die Schaltfläche „Schema bearbeiten“ ist hervorgehoben.](/help/data-modelling/assets/integrated/edit-schema.png)

Im Fenster **[!UICONTROL Schema bearbeiten]** wird der Schema-Editor angezeigt. Weitere Informationen zur Verwendung des Schema-Editors finden Sie im [Handbuch zur Schema-Benutzeroberfläche](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/resources/schemas#customize-schema).

![Der Schema-Editor wird angezeigt.](/help/data-modelling/assets/integrated/schema-editor.png)

### Bearbeiten von Beziehungen {#relationship-edit}

Um die Beziehungen für ein Schema zu bearbeiten, wählen Sie **[!UICONTROL Entitätsdiagramm anzeigen]** im Schema-Editor aus.

![Die Schaltfläche „Entitätsdiagramm anzeigen“ ist hervorgehoben.](/help/data-modelling/assets/integrated/view-entity-diagram.png)

Die Seite mit dem Entitätsdiagramm wird angezeigt. Auf dieser Seite können Sie Links erstellen, um Beziehungen zwischen Ihren Schemata herzustellen.

![Das Entitätsdiagramm wird angezeigt.](/help/data-modelling/assets/integrated/entity-diagram.png)

Weiterführende Informationen zum Erstellen von Links finden Sie in der Registerkarte „Arbeitsflächen-Ansicht“ der [Datenmodelle - Übersicht](/help/data-modelling/models.md#data-model-links).

## Vorschau von Daten in einem Schema {#schema-preview}

Um eine Vorschau der Daten in der Tabelle anzuzeigen, die durch Ihr Schema dargestellt wird, gehen Sie zum Abschnitt **[!UICONTROL Datensätze]** und wählen Sie dann **[!UICONTROL Durchsuchen]** aus.

![Die Schaltflächen Datensätze und Durchsuchen sind hervorgehoben.](/help/data-modelling/assets/integrated/datasets-browse.png)

Wählen Sie die ![drei Punkte](/help/assets/icons/more.png) gefolgt von **[!UICONTROL Vorschau des Datensatzes]** aus, um eine Vorschau der Daten im Schema anzuzeigen.

![Die Schaltfläche „Datensatz in der Vorschau anzeigen“ ist hervorgehoben.](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## Aktualisieren eines Schemas {#schema-refresh}

Tabellen in einer föderierten Datenbank können aktualisiert, hinzugefügt oder entfernt werden. Sie müssen dann das Schema in Adobe Experience Platform aktualisieren, um es an die neuesten Änderungen anzupassen. Um das Schema zu aktualisieren, wählen Sie die Schaltfläche **[!UICONTROL Mehr]** und dann **[!UICONTROL Konfiguration verwalten]** aus.

![Die Schaltfläche „Konfiguration verwalten“ ist hervorgehoben.](/help/data-modelling/assets/integrated/manage-configuration.png)

Das **[!UICONTROL Konfiguration bearbeiten]** wird angezeigt. Wählen Sie **[!UICONTROL Aktualisieren]** aus, um das Schema zu aktualisieren.

![Die Schaltfläche „Schema aktualisieren“ ist hervorgehoben.](/help/data-modelling/assets/integrated/refresh-schema.png)

## Löschen eines Schemas {#schema-delete}

Um ein Schema im Schema-Editor zu löschen, wählen Sie **[!UICONTROL Mehr]** und dann **[!UICONTROL Löschen]** aus.

![Die Schaltfläche „Schema löschen“ ist hervorgehoben.](/help/data-modelling/assets/integrated/delete-schema.png)
