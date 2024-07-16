---
title: Erste Schritte mit Federated Audience-Komposition
description: Erfahren Sie, was unter Adobe Federated Audience Komposition zu verstehen ist und wie Sie sie in Adobe Experience Platform verwenden.
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# Erste Schritte mit Federated Audience-Komposition {#gs-fac}

Die Adobe Federated Audience Komposition hilft Adobe Experience Platform-Anwendern beim Zugriff auf ihre in ihrem Enterprise Data Warehouse gespeicherten Kundendaten. Kundendaten können in mehreren Data Warehouse gespeichert werden und sollten sofort ohne Replikation verfügbar sein.

Adobe Experience Platform Federated Audience Komposition bietet eine einfache und leistungsstarke Lösung, um Ihr Enterprise Data Warehouse direkt in Adobe Real-time Customer Data Platform zu verbinden und Abfragen über die Tabellen in Ihrem Data Warehouse durchzuführen.

## Die wichtigsten Schritte {#gs-steps}

Mit der Adobe Federated Audience Komposition können Sie Adobe Experience Platform-Zielgruppen direkt aus Ihrer Datenbank erstellen und aktualisieren, ohne dass ein Aufnahmevorgang erforderlich ist.

![Diagramm](assets/FAC-diagram.png)

Wichtigste Schritte:

* **Konfiguration**

   1. Verbinden Sie Adobe Experience Platform und Ihr Enterprise Data Warehouse.
Folgende Datenbanken werden unterstützt: Snowflake, Google Big Query, Azure synapse, Redshift.
Weiterführende Informationen finden Sie auf [dieser Seite](../connections/federated-db.md)
   1. Erstellen Sie Schemata, um festzulegen, auf welche Daten über die Benutzeroberfläche zugegriffen werden soll.
Weiterführende Informationen finden Sie auf [dieser Seite](../customer/schemas.md)
   1. Erstellen Sie Links für Ihr Datenmodell.
Weiterführende Informationen finden Sie auf [dieser Seite](../data-management/gs-models.md)

* **Erstellen von Zielgruppen**

   1. Erstellen Sie Kompositionen und führen Sie sie aus, um Audiences zu erstellen.
Weiterführende Informationen finden Sie auf [dieser Seite](../compositions/gs-compositions.md)
   1. Vorhandene Zielgruppen über das Adobe Experience Platform Audience Portal und die Ziele aktualisieren oder wiederverwenden.
Weiterführende Informationen finden Sie auf [dieser Seite](../connections/destinations.md)

## Weitere Informationen {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Ausführungseinstellungen"
>abstract="In diesem Abschnitt können Sie Einstellungen für die Ausführung des Workflows konfigurieren, z. B. für wie viele Tage der Workflow-Verlauf gespeichert wird."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktivität nicht bearbeitbar"
>abstract="Wenn eine **Abfrage** oder **Anreicherung** mit zusätzlichen Daten in der Konsole konfiguriert wird, werden die Anreicherungsdaten berücksichtigt und an die ausgehende Transition übergeben. Sie können jedoch nicht bearbeitet werden."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Erstellen eines Links"
>abstract="Definieren Sie die Link-Einstellungen."
