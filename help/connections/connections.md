---
audience: end-user
title: Erstellen und Verwalten von Verbindungen mit föderierten Datenbanken
description: Erfahren Sie, wie Sie Verbindungen mit föderierten Datenbanken erstellen und verwalten
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 19%

---

# Erstellen von Verbindungen {#connections-fdb}

Mit der Experience Platform Federated Audience Komposition können Kunden Audiences aus Drittanbieter-Data Warehouse erstellen und anreichern und die Zielgruppen in Adobe Experience Platform importieren.

Um mit Ihrer verbundenen Datenbank und Adobe Experience Platform zu arbeiten, müssen Sie zunächst eine Verbindung herstellen. Diese Verbindung wird in einer dedizierten Benutzeroberfläche eingerichtet, die in der Benutzeroberfläche von Adobe Experience Platform verfügbar ist, wie auf dieser Seite beschrieben.

Gehen Sie wie folgt vor, um eine Verbindung mit Ihrer Datenbank einzurichten:

1. Navigieren Sie in der linken Leiste zum Abschnitt **[!UICONTROL FEDERATED DATA]** .

1. Klicken Sie im Link **[!UICONTROL Federated DataBases]** auf die Schaltfläche **[!UICONTROL Federated Database hinzufügen]** .

   ![](assets/connections_list.png){zoomable="yes"}

1. Legen Sie die Verbindung **[!UICONTROL Eigenschaften]** mit dem Namen und dem Typ Ihrer Datenbank fest.

   ![](assets/connections_name.png){zoomable="yes"}

   Wenn Sie den Typ auswählen, haben Sie Zugriff auf andere Eigenschaften, die ausgefüllt werden sollen. Weitere Informationen zu den unterstützten Datenbanken finden Sie auf [dieser Seite](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   Die Konfigurationseinstellungen hängen vom Typ Ihrer Datenbank ab. Klicken Sie auf die folgenden Links, um auf Details zuzugreifen, die Sie zum Einrichten der Verbindung benötigen:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Google BigQuery](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Nachdem Sie die Details ausgefüllt haben, klicken Sie auf die Schaltfläche **[!UICONTROL Verbindung testen]** und auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]** .

1. Schließen Sie die Einrichtung Ihrer Verbindung ab, indem Sie auf die Schaltfläche **[!UICONTROL Speichern]** klicken.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   Eine Übersicht über Ihre Federated Database-Verbindung finden Sie im Folgenden:

   ![](assets/connections_overview.png){zoomable="yes"}
