---
audience: end-user
title: Erstellen und Verwalten von Verbindungen mit Federated Data Datenbanken
description: Erfahren Sie, wie Sie Verbindungen mit Federated Databases erstellen und verwalten.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# Verbindungen erstellen {#connections-fdb}

Das direkte Arbeiten mit einer Federated-Datenbank in AEP setzt voraus, dass eine Verbindung mit ihr hergestellt wird.

Um eine Verbindung mit Ihrer Datenbank einzurichten, wechseln Sie zum Abschnitt **[!UICONTROL FEDERATED DATA]** und klicken Sie im Link **[!UICONTROL Federated DataBases]** auf die Schaltfläche **[!UICONTROL Federated Database hinzufügen]** .

![](assets/connections_list.png){zoomable="yes"}

Sie greifen auf das Fenster für die Verbindung **[!UICONTROL Eigenschaften]** zu, das den Namen und den Typ Ihrer Datenbank enthält.

![](assets/connections_name.png){zoomable="yes"}

Wenn Sie den Typ auswählen, haben Sie Zugriff auf andere Eigenschaften, die ausgefüllt werden sollen. [Erfahren Sie hier mehr über die unterstützten Datenbanken](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

Je nach Typ Ihrer Datenbank finden Sie in den Links unter den Informationen, die Sie zum Einrichten der Verbindung benötigen:

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google BigQuery](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Nachdem Sie die Details ausgefüllt haben, klicken Sie auf die Schaltfläche **[!UICONTROL Verbindung testen]** und auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]** .
Schließen Sie die Erstellung Ihrer Verbindung ab, indem Sie auf die Schaltfläche **[!UICONTROL Speichern]** klicken.

![](assets/connections_testdeploy.png){zoomable="yes"}

Sie erhalten einen Überblick über Ihre Federated Database-Verbindung wie folgt:

![](assets/connections_overview.png){zoomable="yes"}
