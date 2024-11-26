---
audience: end-user
title: Erstellen und Verwalten von Verbindungen mit föderierten Datenbanken
description: Erfahren Sie, wie Sie Verbindungen mit föderierten Datenbanken erstellen und verwalten.
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: ht
source-wordcount: '226'
ht-degree: 100%

---

# Erstellen von Verbindungen {#connections-fdb}

Die Komposition föderierter Zielgruppen in Experience Platform ermöglicht es Kundinnen und Kunden, Zielgruppen aus Data Warehouses von Drittanbietern zu erstellen und anzureichern und die Zielgruppen in Adobe Experience Platform zu importieren. Die unterstützten Data Warehouses sind in [diesem Abschnitt](../start/access-prerequisites.md#supported-systems) aufgeführt.

Um mit Ihrer föderierten Datenbank und Adobe Experience Platform zu arbeiten, müssen Sie zunächst eine Verbindung herstellen. Diese Verbindung wird in einer dedizierten Benutzeroberfläche eingerichtet, die in der Benutzeroberfläche von Adobe Experience Platform verfügbar ist, wie auf dieser Seite beschrieben.

Gehen Sie wie folgt vor, um eine Verbindung mit Ihrer Datenbank einzurichten:

1. Navigieren Sie in der linken Leiste zum Abschnitt **[!UICONTROL FÖDERIERTE DATEN]**.

1. Klicken Sie unter dem Link **[!UICONTROL Föderierte Datenbanken]** auf die Schaltfläche **[!UICONTROL Föderierte Datenbank hinzufügen]**.

   ![](assets/connections_list.png){zoomable="yes"}

1. Legen Sie die **[!UICONTROL Eigenschaften]** der Verbindung fest und geben Sie dabei den Namen und den Typ Ihrer Datenbank an.

   ![](assets/connections_name.png){zoomable="yes"}

   Wenn Sie den Typ auswählen, haben Sie Zugriff auf andere Eigenschaften, die Sie ausfüllen können. Auf [dieser Seite](federated-db.md) erfahren Sie mehr über die unterstützten Datenbanken.

   ![](assets/connections_details.png){zoomable="yes"}

   Die Konfigurationseinstellungen hängen vom Typ Ihrer Datenbank ab. Durchsuchen Sie die nachfolgenden Links, um auf Details zuzugreifen, die Sie zum Einrichten der Verbindung benötigen:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Databricks](federated-db.md#databricks)
   * [Google BigQuery](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Nachdem Sie die Details eingegeben haben, klicken Sie auf die Schaltfläche **[!UICONTROL Verbindung testen]** und auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]**.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

1. Schließen Sie die Einrichtung Ihrer Verbindung ab, indem Sie auf die Schaltfläche **[!UICONTROL Speichern]** klicken.

   Es ist eine Übersicht über Ihre Verbindung mit der föderierten Datenbank verfügbar, wie unten dargestellt:

   ![](assets/connections_overview.png){zoomable="yes"}
