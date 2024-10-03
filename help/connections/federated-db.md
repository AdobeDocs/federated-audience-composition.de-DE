---
audience: end-user
title: Konfigurieren föderierter Datenbanken
description: Erfahren Sie, wie Sie föderierte Datenbanken konfigurieren
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: b8c0589d-4150-40da-ac79-d53cced236e8
source-git-commit: 47d10997c7701611bbba533dfe7553a7bdc41e02
workflow-type: ht
source-wordcount: '1622'
ht-degree: 100%

---

# Konfigurieren föderierter Datenbanken {#federated-db}

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Föderierte Datenbanken"
>abstract="Bestehende Verbindungen zu föderierten Datenbanken werden auf diesem Bildschirm angezeigt. Um eine neue Verbindung zu erstellen, auf die Schaltfläche **[!UICONTROL Verbund-Datenbank hinzufügen]** klicken."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Eigenschaften der föderierten Datenbank"
>abstract="Den Namen der neuen föderierten Datenbank eingeben und den Typ auswählen."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Details zur föderierten Datenbank"
>abstract="Die Einstellungen für die Verbindung mit der neuen föderierten Datenbank eingeben. Auf die Schaltfläche **[!UICONTROL Verbindung testen]** klicken, um die Konfiguration zu validieren."

Die Komposition föderierter Zielgruppen in Experience Platform ermöglicht es Kundinnen und Kunden, Zielgruppen aus Data Warehouses anderer Drittanbieter zu erstellen und anzureichern und die Zielgruppen in Adobe Experience Platform zu importieren.

Auf [dieser Seite](connections.md) erfahren Sie, wie Sie die Verbindung zu Ihrer externen Datenbank erstellen, konfigurieren, testen und speichern. Unten finden Sie die Liste der unterstützten Datenbanken und die ausführlichen Einstellungen zum Konfigurieren jeder einzelnen Datenbank.

## Unterstützte Datenbanken {#supported-db}

Mit der Komposition föderierter Zielgruppen können Sie eine Verbindung zu den folgenden Datenbanken herstellen. Die Konfiguration der einzelnen Datenbanken wird nachfolgend beschrieben.

* [Amazon Redshift](#amazon-redshift)
* [Azure Synapse Analytics](#azure-synapse)
* [Google BigQuery](#google-big-query)
* [Snowflake](#snowflake)
* [Vertica Analytics](#vertica-analytics)

## Amazon Redshift {#amazon-redshift}

Verwenden Sie föderierte Datenbanken, um in einer externen Datenbank gespeicherte Daten zu verarbeiten. Gehen Sie wie folgt vor, um den Zugriff auf Amazon Redshift zu konfigurieren.

1. Wählen Sie im Menü **[!UICONTROL Föderierte Daten]** die Option **[!UICONTROL Föderierte Datenbanken]** aus.

1. Klicken Sie auf **[!UICONTROL Föderierte Datenbank hinzufügen]**.

   ![](assets/federated_database_1.png)

1. Geben Sie einen **[!UICONTROL Namen]** in Ihre föderierte Datenbank ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option „Amazon Redshift“ aus.

   ![](assets/federated_database_6.png)

1. Konfigurieren Sie die Amazon Redshift-Authentifizierungseinstellungen:

   * **[!UICONTROL Server]**: Fügen Sie den Namen des DNS hinzu.

   * **[!UICONTROL Konto]**: Fügen Sie den Benutzernamen hinzu.

   * **[!UICONTROL Kennwort]**: Fügen Sie das Kontokennwort hinzu.

   * **[!UICONTROL Datenbank]**: Name Ihrer Datenbank, falls nicht im DSN angegeben. Kann leer bleiben, wenn im DSN angegeben

   * **[!UICONTROL Arbeitsschema]**: Name des Datenbankschemas, das für Arbeitstabellen verwendet werden soll. Weitere Informationen finden Sie in der [Dokumentation zu Amazon](https://docs.aws.amazon.com/de_de/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.

     >[!NOTE]
     >
     >Sie können jedes Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen.
     >
     >Beim Verbinden mehrerer Sandboxes mit derselben Datenbank müssen **unterschiedliche Arbeitsschemata** verwendet werden.

1. Wählen Sie die Option **[!UICONTROL Verbindung testen]** aus, um Ihre Konfiguration zu überprüfen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]**, um Funktionen zu erstellen.

1. Nachdem Sie die Konfiguration abgeschlossen haben, klicken Sie auf **[!UICONTROL Hinzufügen]**, um Ihre föderierte Datenbank zu erstellen.

## Azure Synapse Analytics {#azure-synapse}

Verwenden Sie föderierte Datenbanken, um in einer externen Datenbank gespeicherte Daten zu verarbeiten. Führen Sie die folgenden Schritte aus, um den Zugriff auf Azure Synapse Analytics zu konfigurieren.

1. Wählen Sie im Menü **[!UICONTROL Föderierte Daten]** die Option **[!UICONTROL Föderierte Datenbanken]** aus.

1. Klicken Sie auf **[!UICONTROL Föderierte Datenbank hinzufügen]**.

   ![](assets/federated_database_1.png)

1. Geben Sie einen **[!UICONTROL Namen]** in Ihre föderierte Datenbank ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option „Azure Synapse Analytics“ aus.

   ![](assets/federated_database_4.png)

1. Konfigurieren Sie die Authentifizierungseinstellungen für Azure Synapse Analytics:

   * **[!UICONTROL Server]**: Geben Sie die URL des Azure Synapse-Servers ein.

   * **[!UICONTROL Konto]**: Geben Sie den Benutzernamen ein.

   * **[!UICONTROL Kennwort]**: Geben Sie das Kontokennwort ein.

   * **[!UICONTROL Datenbank]** (optional): Geben Sie den Namen Ihrer Datenbank ein, falls nicht im DSN angegeben.

   * **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

1. Wählen Sie die Option **[!UICONTROL Verbindung testen]** aus, um Ihre Konfiguration zu überprüfen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]**, um Funktionen zu erstellen.

1. Nachdem Sie die Konfiguration abgeschlossen haben, klicken Sie auf **[!UICONTROL Hinzufügen]**, um Ihre föderierte Datenbank zu erstellen.

| Option | Beschreibung |
|---|---|
| Authentifizierung | Vom Connector unterstützter Authentifizierungstyp. Aktuell unterstützter Wert: ActiveDirectoryMSI. Weitere Informationen finden Sie in der [Dokumentation zu Microsoft SQL](https://learn.microsoft.com/de-de/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"} (Beispiel für Verbindungszeichenfolgen Nr. 8) |


## Google BigQuery {#google-big-query}

Verwenden Sie föderierte Datenbanken, um in einer externen Datenbank gespeicherte Daten zu verarbeiten. Gehen Sie wie folgt vor, um den Zugriff auf Google BigQuery zu konfigurieren.

1. Wählen Sie im Menü **[!UICONTROL Föderierte Daten]** die Option **[!UICONTROL Föderierte Datenbanken]** aus.

1. Klicken Sie auf **[!UICONTROL Föderierte Datenbank hinzufügen]**.

   ![](assets/federated_database_1.png)

1. Geben Sie einen **[!UICONTROL Namen]** in Ihre föderierte Datenbank ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option „Google BigQuery“ aus.

   ![](assets/federated_database_3.png)

1. Konfigurieren Sie die Authentifizierungseinstellungen für Google BigQuery:

   * **[!UICONTROL Dienstkonto]**: Geben Sie die E-Mail-Adresse Ihres **[!UICONTROL Dienstkontos]** ein. Weiterführende Informationen dazu finden Sie in der [Dokumentation zu Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts){target="_blank"}.

   * **[!UICONTROL Projekt]**: Geben Sie die ID Ihres **[!UICONTROL Projekts]** ein. Weiterführende Informationen dazu finden Sie in der [Dokumentation zu Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}.

   * **[!UICONTROL Datensatz]**: Geben Sie den Namen Ihres **[!UICONTROL Datensatzes]** ein. Weiterführende Informationen dazu finden Sie in der [Dokumentation zu Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}.

   * **[!UICONTROL Pfad der Schlüsseldatei]**: Laden Sie Ihre Schlüsseldatei auf den Server hoch. Es sind nur .json-Dateien zulässig.

   * **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

1. Wählen Sie die Option **[!UICONTROL Verbindung testen]** aus, um Ihre Konfiguration zu überprüfen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]**, um Funktionen zu erstellen.

1. Nachdem Sie die Konfiguration abgeschlossen haben, klicken Sie auf **[!UICONTROL Hinzufügen]**, um Ihre föderierte Datenbank zu erstellen.

| Option | Beschreibung |
|---|---|
| ProxyType | Proxy-Typ, der für die Verbindung mit BigQuery über ODBC- und SDK-Connectoren verwendet wird. </br>Derzeit wird HTTP (Standard), http_no_tunnel, socks4 und socks5 unterstützt. |
| ProxyHost | Host-Name oder IP-Adresse, über die der Proxy erreicht werden kann. |
| ProxyPort | Port-Nummer, auf der der Proxy ausgeführt wird, z. B. 8080 |
| ProxyUid | Für den authentifizierten Proxy verwendeter Benutzername |
| ProxyPwd | ProxyUid-Kennwort |
| bqpath | Beachten Sie, dass dies nur für das Massenlade-Tool (Cloud SDK) gilt. </br> Um die Verwendung der PATH-Variable zu vermeiden oder wenn der Ordner „google-cloud-sdk“ an einen anderen Speicherort verschieben werden muss, können Sie mit dieser Option den genauen Pfad zum Cloud-SDK-Bin-Ordner auf dem Server angeben. |
| GCloudConfigName | Beachten Sie, dass dies ab Version 7.3.4 und nur für das Massenlade-Tool (Cloud SDK) gilt.</br> Das Google Cloud-SDK verwendet Konfigurationen zum Laden von Daten in BigQuery-Tabellen. Die Konfiguration mit dem Namen `accfda` speichert die Parameter zum Laden der Daten. Mit dieser Option können Benutzende jedoch einen anderen Namen für die Konfiguration angeben. |
| GCloudDefaultConfigName | Beachten Sie, dass dies ab Version 7.3.4 und nur für das Massenlade-Tool (Cloud SDK) gilt.</br> Die aktive Google Cloud SDK-Konfiguration kann nicht gelöscht werden, ohne dass das aktive Tag zuerst in eine neue Konfiguration übertragen wird. Diese temporäre Konfiguration ist erforderlich, um die Hauptkonfiguration für das Laden von Daten neu zu erstellen. Der Standardname für die temporäre Konfiguration lautet `default`. Dieser kann bei Bedarf geändert werden. |
| GCloudRecreateConfig | Beachten Sie, dass dies ab Version 7.3.4 und nur für das Massenlade-Tool (Cloud SDK) gilt.</br> Wenn diese Option auf `false` gesetzt ist, versucht der Massenlademechanismus nicht, die Google Cloud SDK-Konfigurationen neu zu erstellen, zu löschen oder zu ändern. Stattdessen wird das Laden der Daten mit der vorhandenen Konfiguration auf dem Computer fortgesetzt. Diese Funktion ist nützlich, wenn andere Vorgänge von Google Cloud SDK-Konfigurationen abhängig sind. </br> Wenn die Benutzerin bzw. der Benutzer diese Engine-Option ohne eine ordnungsgemäße Konfiguration aktiviert, gibt der Massenlademechanismus eine Warnmeldung aus: `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Um weitere Fehler zu vermeiden, wird dann wieder der standardmäßige Massenlademechanismus „ODBC Array Insert“ verwendet. |


## Snowflake {#snowflake}

Verwenden Sie föderierte Datenbanken, um in einer externen Datenbank gespeicherte Daten zu verarbeiten. Gehen Sie wie folgt vor, um den Zugriff auf Snowflake zu konfigurieren.

1. Wählen Sie im Menü **[!UICONTROL Föderierte Daten]** die Option **[!UICONTROL Föderierte Datenbanken]** aus.

1. Klicken Sie auf **[!UICONTROL Föderierte Datenbank hinzufügen]**.

   ![](assets/federated_database_1.png)

1. Geben Sie einen **[!UICONTROL Namen]** in Ihre föderierte Datenbank ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option „Snowflake“ aus.

   ![](assets/federated_database_2.png)

1. Konfigurieren Sie die Authentifizierungseinstellungen für Snowflake:

   * **[!UICONTROL Server]**: Geben Sie Ihren Server-Namen ein.

   * **[!UICONTROL Benutzer]**: Geben Sie Ihren Benutzernamen ein.

   * **[!UICONTROL Kennwort]**: Geben Sie Ihr Kontokennwort ein.

   * **[!UICONTROL Datenbank]** (optional): Geben Sie den Namen Ihrer Datenbank ein, falls nicht im DSN angegeben.

   * **[!UICONTROL Arbeitsschema]** (optional): Geben Sie den Namen des Datenbankschemas ein, das für Arbeitstabellen verwendet werden soll.

     >[!NOTE]
     >
     >Sie können jedes Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen.
     >
     >Beim Verbinden mehrerer Sandboxes mit derselben Datenbank müssen **unterschiedliche Arbeitsschemata** verwendet werden.

   * **[!UICONTROL Privater Schlüssel]**: Klicken Sie auf das Feld **[!UICONTROL Privater Schlüssel]**, um Ihre .pem-Dateien aus Ihrem Gebietsschema-Ordner auszuwählen.

   * **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

1. Wählen Sie die Option **[!UICONTROL Verbindung testen]** aus, um Ihre Konfiguration zu überprüfen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]**, um Funktionen zu erstellen.

1. Nachdem Sie die Konfiguration abgeschlossen haben, klicken Sie auf **[!UICONTROL Hinzufügen]**, um Ihre föderierte Datenbank zu erstellen.

Der Connector unterstützt die folgenden Optionen:

| Option | Beschreibung |
|---|---|
| workschema | Datenbankschema zur Verwendung mit Arbeitstabellen |
| warehouse | Name des zu verwendenden Standard-Warehouse. Dadurch wird die Standardeinstellung des Benutzers außer Kraft gesetzt. |
| TimeZoneName | Standardmäßig leer, d. h. die Systemzeitzone des App-Servers wird verwendet. Mit dieser Option können Sie den Sitzungsparameter „TIMEZONE“ durchsetzen. <br>Weiterführende Informationen hierzu finden Sie auf [dieser Seite](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone){target="_blank"}. |
| WeekStart | Sitzungsparameter WEEK_START. Ist standardmäßig auf 0 gesetzt. <br>Weiterführende Informationen hierzu finden Sie auf [dieser Seite](https://docs.snowflake.com/de/sql-reference/parameters.html#week-start){target="_blank"}. |
| UseCachedResult | Sitzungsparameter USE_CACHED_RESULTS. Standardmäßig ist TRUE festgelegt. Diese Option kann verwendet werden, um zwischengespeicherte Snowflake-Ergebnisse zu deaktivieren. <br>Weiterführende Informationen hierzu finden Sie auf [dieser Seite](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html){target="_blank"}. |
| bulkThreads | Anzahl der Threads, die für den Snowflake-Massenlader verwendet werden sollen. Mehr Threads bedeuten eine bessere Leistung bei größeren Massenladevorgängen. Ist standardmäßig auf 1 gesetzt Die Zahl kann je nach Anzahl der Rechner-Threads angepasst werden. |
| chunkSize | Bestimmt die Dateigröße des Massenladerblocks. Standardmäßig auf 128 MB gesetzt. Kann bei Verwendung mit „bulkThreads“ geändert werden, um eine optimale Leistung zu erreichen. Mehr gleichzeitig aktive Threads bedeuten eine bessere Leistung. <br>Weiterführende Informationen hierzu finden Sie in der [Dokumentation zu Snowflake](https://docs.snowflake.com/de/sql-reference/sql/put){target="_blank"}. |
| StageName | Name des vorab bereitgestellten internen Stages. Er wird beim Massenladen verwendet, anstatt einen neuen temporären Staging-Bereich zu erstellen. |


## Vertica Analytics {#vertica-analytics}

Verwenden Sie föderierte Datenbanken, um in einer externen Datenbank gespeicherte Daten zu verarbeiten. Gehen Sie wie folgt vor, um den Zugriff auf Vertica Analytics zu konfigurieren.

1. Wählen Sie im Menü **[!UICONTROL Föderierte Daten]** die Option **[!UICONTROL Föderierte Datenbanken]** aus.

1. Klicken Sie auf **[!UICONTROL Föderierte Datenbank hinzufügen]**.

   ![](assets/federated_database_1.png)

1. Geben Sie einen **[!UICONTROL Namen]** in Ihre föderierte Datenbank ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Typ]** die Option „Vertica Analytics“ aus.

   ![](assets/federated_database_5.png)

1. Konfigurieren Sie die Vertica Analytics-Authentifizierungseinstellungen:

   * **[!UICONTROL Server]**: Fügen Sie die URL des [!DNL Vertica Analytics]-Servers hinzu.

   * **[!UICONTROL Konto]**: Fügen Sie den Benutzernamen hinzu.

   * **[!UICONTROL Kennwort]**: Fügen Sie das Kontokennwort hinzu.

   * **[!UICONTROL Datenbank]** (optional): Geben Sie den Namen Ihrer Datenbank ein, falls nicht im DSN angegeben.

   * **[!UICONTROL Arbeitsschema]** (optional): Geben Sie den Namen des Datenbankschemas ein, das für Arbeitstabellen verwendet werden soll.

     >[!NOTE]
     >
     >Sie können jedes Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen.
     >
     >Beim Verbinden mehrerer Sandboxes mit derselben Datenbank müssen **unterschiedliche Arbeitsschemata** verwendet werden.

   * **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

1. Wählen Sie die Option **[!UICONTROL Verbindung testen]** aus, um Ihre Konfiguration zu überprüfen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Funktionen bereitstellen]**, um Funktionen zu erstellen.

1. Nachdem Sie die Konfiguration abgeschlossen haben, klicken Sie auf **[!UICONTROL Hinzufügen]**, um Ihre föderierte Datenbank zu erstellen.

Der Connector unterstützt die folgenden Optionen:

| Option | Beschreibung |
|---|---|
| TimeZoneName | Standardmäßig leer, d. h. die Systemzeitzone des App-Servers wird verwendet. Mit dieser Option können Sie den Sitzungsparameter „TIMEZONE“ durchsetzen. |
