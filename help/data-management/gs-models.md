---
audience: end-user
title: Erste Schritte mit Datenmodellen
description: Erfahren Sie, wie Sie mit der Arbeit mit Datenmodellen beginnen.
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: d8fd926a445e65b6c7310d2ceac5a83ba9fece3f
workflow-type: ht
source-wordcount: '751'
ht-degree: 100%

---


# Erste Schritte mit Datenmodellen {#data-model-beta}

>[!AVAILABILITY]
>
>Um auf Datenmodelle zugreifen zu können, benötigen Sie eine der folgenden Berechtigungen:
>
>-**Föderiertes Datenmodell verwalten**
>>-**Föderiertes Datenmodell anzeigen**
>
>Weitere Informationen zu den erforderlichen Berechtigungen finden Sie im [Handbuch zur Zugriffssteuerung](/help/governance-privacy-security/access-control.md).

## Was ist ein Datenmodell? {#data-model-start}

Ein Datenmodell ist ein Satz von Schemata, Zielgruppen und den Verknüpfungen zwischen ihnen. Es wird verwendet, um Zielgruppen mit Daten aus Datenbanken zu verbinden.

Bei der Komposition föderierter Zielgruppen können Sie Datenmodelle direkt in der Arbeitsflächenansicht erstellen und verwalten. Dazu gehört das Hinzufügen von Schemata und Zielgruppen sowie das Definieren der Verknüpfungen zwischen ihnen auf Grundlage Ihres Anwendungsfalls.

Weitere Informationen zu [Schemata](../customer/schemas.md#schema-start) und [Zielgruppen](../start/audiences.md).

Unten sehen Sie beispielsweise die Darstellung eines Datenmodells: die Tabellen mit ihrem Namen und die Verknüpfungen zwischen ihnen.

![](assets/datamodel.png){zoomable="yes"}

## Erstellen eines Datenmodells {#data-model-create}

Gehen Sie wie folgt vor, um ein Datenmodell zu erstellen:

1. Greifen Sie im Abschnitt **[!UICONTROL Föderierte Daten]** auf das Menü **[!UICONTROL Modelle]** zu und gehen Sie zur Registerkarte **[!UICONTROL Datenmodell]**.

   Wählen Sie die Schaltfläche **[!UICONTROL Datenmodell erstellen]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

2. Definieren Sie den Namen Ihres Datenmodells und wählen Sie die Schaltfläche **[!UICONTROL Erstellen]** aus.

3. Wählen Sie im Dashboard Ihres Datenmodells **[!UICONTROL Schemata hinzufügen]** aus, um das mit Ihrem Datenmodell verknüpfte Schema auszuwählen.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

4. Außerdem können Sie Zielgruppen zu Ihrem Datenmodell hinzufügen. Wählen Sie **[!UICONTROL Zielgruppen hinzufügen]** aus, um Ihre Zielgruppen zu definieren.

   ![](assets/datamodel-audiences.png){zoomable="yes"}

5. Stellen Sie Verbindungen zwischen Tabellen in Ihrem Datenmodell her, um genaue Datenbeziehungen sicherzustellen. Weiterführende Informationen finden Sie im Abschnitt [Erstellen von Links](#data-model-links).

6. Wählen Sie nach Abschluss der Konfiguration **[!UICONTROL Speichern]** aus, um Ihre Änderungen anzuwenden.

## Erstellen von Links {#data-model-links}

>[!NOTE]
>
>Wenn Sie einen Link mit mehreren Joins erstellen, können Sie dieselbe Kombination aus Quell- und Zielschemata nur einmal verwenden.

>[!BEGINTABS]

>[!TAB Tabellenansicht]

Gehen Sie wie folgt vor, um über die Registerkarte „Tabellenansicht“ Links zwischen Tabellen Ihres Datenmodells zu erstellen:

1. Wählen Sie das ![Symbol mit den drei Punkten](/help/assets/icons/more.png) gefolgt von **[!UICONTROL Link erstellen]** neben einer der Tabellen oder **[!UICONTROL Links erstellen]** im Abschnitt **[!UICONTROL Links]** aus:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

2. Füllen Sie das angegebene Formular aus, um den Link zu definieren:

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Kardinalität**

   * **1:N**: Eine Entität in der Quelltabelle kann mit mehreren Entitäten in der Zieltabelle in Beziehung stehen, aber eine Entität in der Zieltabelle kann nur maximal mit einer Entität in der Quelltabelle in Beziehung stehen.

   * **N:1**: Eine Entität in der Zieltabelle kann mit mehreren Entitäten in der Quelltabelle in Beziehung stehen, aber eine Entität in der Quelltabelle kann nur maximal mit einer Entität in der Zieltabelle in Beziehung stehen.

   * **1:1**: Eine Entität in der Quelltabelle kann maximal mit einer Entität in der Zieltabelle in Beziehung stehen.

   Um einen Link mit mehreren Joins zu erstellen, wählen Sie das Plussymbol. Sie können jetzt mehrere Joins zwischen den Schemafeldern erstellen.

   ![Die Schaltfläche mit dem Plussymbol wird hervorgehoben, sodass Sie einen Link mit mehreren Joins für das Modell erstellen können.](assets/multi-join.png){zoomable="yes"}

Alle für Ihr Datenmodell definierten Links werden wie folgt aufgeführt:

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB Arbeitsflächenansicht]

Gehen Sie wie folgt vor, um über die Registerkarte „Arbeitsflächenansicht“ Links zwischen Tabellen Ihres Datenmodells zu erstellen:

1. Rufen Sie die Arbeitsflächenansicht Ihres Datenmodells auf und wählen Sie die beiden Tabellen aus, die Sie verknüpfen möchten.

2. Wählen Sie die Schaltfläche ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) neben dem Quellen-Join aus und ziehen Sie den Pfeil in Richtung Ziel-Join, um die Verbindung herzustellen.

   ![](assets/datamodel.gif){zoomable="yes"}

3. Füllen Sie das angegebene Formular aus, um den Link zu definieren, und wählen Sie nach der Konfiguration **[!UICONTROL Anwenden]** aus.

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **Kardinalität**

   * **1:N**: Eine Entität in der Quelltabelle kann mit mehreren Entitäten in der Zieltabelle in Beziehung stehen, aber eine Entität in der Zieltabelle kann nur maximal mit einer Entität in der Quelltabelle in Beziehung stehen.

   * **N:1**: Eine Entität in der Zieltabelle kann mit mehreren Entitäten in der Quelltabelle in Beziehung stehen, aber eine Entität in der Quelltabelle kann nur maximal mit einer Entität in der Zieltabelle in Beziehung stehen.

   * **1:1**: Eine Entität in der Quelltabelle kann maximal mit einer Entität in der Zieltabelle in Beziehung stehen.

4. Alle in Ihrem Datenmodell definierten Links werden in der Arbeitsflächenansicht als Pfeile dargestellt. Wählen Sie einen Pfeil zwischen zwei Tabellen aus, um je nach Bedarf Details anzuzeigen, Änderungen vorzunehmen oder den Link zu entfernen.

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

5. Verwenden Sie die Symbolleiste, um die Arbeitsfläche anzupassen.

   ![](assets/datamodel-canvas-3.png)

   * **[!UICONTROL Vergrößern]**: Vergrößert die Arbeitsfläche, um Details zu Ihrem Datenmodell deutlicher zu sehen.
   * **[!UICONTROL Verkleinern]**: Verkleinert die Arbeitsfläche, um eine erweiterte Ansicht Ihres Datenmodells zu erhalten.
   * **[!UICONTROL Ansicht anpassen]**: Passt den Zoom so an, dass alle Schemata und/oder Zielgruppen in den sichtbaren Bereich passen.
   * **[!UICONTROL Interaktivität ein/ausschalten]**: Aktiviert oder deaktiviert die Benutzerinteraktion mit der Arbeitsfläche.
   * **[!UICONTROL Filter]**: Wählen Sie aus, welches Schema auf der Arbeitsfläche angezeigt werden soll.
   * **[!UICONTROL Automatisches Layout erzwingen]**: Lassen Sie Schemata und/oder Zielgruppen zur besseren Organisation automatisch anordnen.

>[!ENDTABS]

## Anleitungsvideo {#data-model-video}

In diesem Video erfahren Sie, wie Sie ein Datenmodell erstellen:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
