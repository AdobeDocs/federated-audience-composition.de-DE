---
audience: end-user
title: Erste Schritte mit Federated Databases
description: Erfahren Sie, wie Sie Ihre Federated DataBases erstellen und verwalten.
source-git-commit: 847da9a5eeb28199010f8491f7eebba4a60a83f1
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 25%

---

# Erste Schritte mit Federated Databases {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Vereinigte Datenbanken"
>abstract="Bestehende Verbindungen zu Federated Databases werden auf diesem Bildschirm angezeigt. Um eine neue Verbindung zu erstellen, klicken Sie auf das **Federated-Datenbank hinzufügen** Schaltfläche."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Eigenschaften der verbundenen Datenbank"
>abstract="Geben Sie den Namen der neuen Federated Database ein und wählen Sie den Typ aus."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Federated Database Details"
>abstract="Geben Sie die Einstellungen für die Verbindung mit der neuen Federated Database ein. Verwenden Sie die **Verbindung testen** zur Validierung Ihrer Konfiguration."

Erstellen, konfigurieren, testen und speichern Sie die Verbindung zu einer externen Datenbank.

Unterstützte externe Datenbanken:

* Snowflake
* Google BigQuery
* Azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL Server]**:

* **[!UICONTROL Benutzer]**: Name des Benutzers.

* **[!UICONTROL Passwort]**: Kennwort für Benutzerkonten.

* **[!UICONTROL Datenbank]**:

* **[!UICONTROL Arbeitsschema]**:

* **[!UICONTROL Privater Schlüssel]**: Es werden nur .pem-Dateien akzeptiert.

* **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

| Option | Beschreibung |
|---|---|
| workschema | Datenbankschema zur Verwendung mit Arbeitstabellen |
| warehouse | Name des zu verwendenden Standard-Warehouse. Dadurch wird die Standardeinstellung des Benutzers außer Kraft gesetzt. |
| TimeZoneName | Standardmäßig leer, d. h. die Systemzeitzone des Campaign Classic-App-Servers wird verwendet. Mit dieser Option können Sie den Sitzungsparameter TIMEZONE erzwingen. <br>Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | Sitzungsparameter WEEK_START. Standardmäßig auf 0 gesetzt <br>Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://docs.snowflake.com/de/sql-reference/parameters.html#week-start). |
| UseCachedResult | Sitzungsparameter USE_CACHED_RESULTS. Standardmäßig ist TRUE festgelegt. Diese Option kann verwendet werden, um zwischengespeicherte Ergebnisse im Snowflake zu deaktivieren. <br>Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThreads | Anzahl der Threads, die für Snowflake-Bulk-Loader verwendet werden sollen, mehr Threads bedeuten eine bessere Leistung bei größeren Bulk-Ladungen. Standardmäßig auf 1 gesetzt Die Zahl kann je nach Anzahl der Maschinenthread angepasst werden. |
| chunkSize | Bestimmt die Dateigröße des Stapels für Ladegeräte. Standardmäßig auf 128 MB eingestellt. Kann für eine optimale Leistung geändert werden, wenn BulkThreads verwendet werden. Gleichzeitigere aktive Threads bedeuten eine bessere Leistung. <br>Weitere Informationen hierzu finden Sie unter [Snowflake-Dokumentation](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| StageName | Name des vorab bereitgestellten internen Schritts. Sie wird bei Bulk Load verwendet, anstatt eine neue temporäre Phase zu erstellen. |

## Google BigQuery {#google-big-query}

* **[!UICONTROL Dienstkonto]**: E-Mail Ihrer **[!UICONTROL Dienstkonto]**. Weitere Informationen hierzu finden Sie unter [Dokumentation zu Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL Projekt]**: Name Ihres **[!UICONTROL Projekt]**. Weitere Informationen hierzu finden Sie unter [Dokumentation zu Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL Datensatz]**: Name Ihres **[!UICONTROL Datensatz]**. Weitere Informationen hierzu finden Sie unter [Dokumentation zu Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL Pfad der Schlüsseldatei]**: Laden Sie Ihre Schlüsseldatei auf den Server hoch. Es werden nur .json-Dateien akzeptiert.

* **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

| Option | Beschreibung |
|:-:|:-:|
| ProxyType | Typ des Proxys, der für die Verbindung mit BigQuery über ODBC- und SDK-Connectoren verwendet wird. </br>HTTP (Standard), http_no_tunnel, socks4 und socks5 werden derzeit unterstützt. |
| ProxyHost | Hostname oder IP-Adresse, an der der Proxy erreicht werden kann. |
| ProxyPort | Anschlussnummer, auf der der Proxy ausgeführt wird, z. B. 8080 |
| ProxyUid | Benutzername für den authentifizierten Proxy |
| ProxyPwd | ProxyUid-Kennwort |
| bqpath | Beachten Sie, dass dies nur für Tools mit Massenladevorgang (Cloud SDK) gilt. </br> Um die Verwendung der PATH-Variablen zu vermeiden oder den Ordner google-cloud-sdk an einen anderen Speicherort zu verschieben, können Sie mit dieser Option den genauen Pfad zum Ordner &quot;cloud sdk bin&quot;auf dem Server angeben. |
| GCloudConfigName | Beachten Sie, dass dies ab Version 7.3.4 und nur für Tools mit Massenladevorgang (Cloud SDK) gilt.</br> Das Google Cloud SDK verwendet Konfigurationen zum Laden von Daten in BigQuery-Tabellen. Die Konfiguration namens `accfda` speichert die Parameter zum Laden der Daten. Mit dieser Option können Benutzer jedoch einen anderen Namen für die Konfiguration angeben. |
| GCloudDefaultConfigName | Beachten Sie, dass dies ab Version 7.3.4 und nur für Tools mit Massenladevorgang (Cloud SDK) gilt.</br> Die aktive Google Cloud SDK-Konfiguration kann nicht gelöscht werden, ohne dass das aktive Tag zuerst in eine neue Konfiguration übertragen wird. Diese temporäre Konfiguration ist erforderlich, um die Hauptkonfiguration für das Laden von Daten neu zu erstellen. Der Standardname für die temporäre Konfiguration lautet `default`, kann dies bei Bedarf geändert werden. |
| GCloudRecreateConfig | Beachten Sie, dass dies ab Version 7.3.4 und nur für Tools mit Massenladevorgang (Cloud SDK) gilt.</br> Wenn festgelegt auf `false`, verhindert der Massenlademechanismus den Versuch, die Google Cloud SDK-Konfigurationen neu zu erstellen, zu löschen oder zu ändern. Stattdessen wird das Laden der Daten mit der vorhandenen Konfiguration auf dem Computer fortgesetzt. Diese Funktion ist nützlich, wenn andere Vorgänge von Google Cloud SDK-Konfigurationen abhängig sind. </br> Wenn der Benutzer diese Engine-Option ohne ordnungsgemäße Konfiguration aktiviert, gibt der Massenlademechanismus eine Warnmeldung aus: `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Um weitere Fehler zu vermeiden, wird dann der standardmäßige ODBC-Array-Einfügemechanismus für Massen-Ladevorgänge verwendet. |

## Azure synapse Redshift {#azure-synapse-redshift}

* **[!UICONTROL Server]**: URL des Azure Synapse-Servers

* **[!UICONTROL Konto]**: Name des Benutzers

* **[!UICONTROL Passwort]**: Passwort des Benutzerkontos

* **[!UICONTROL Datenbank]**: Name der Datenbank

* **[!UICONTROL Optionen]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL Server]**: URL des [!DNL Vertica Analytics]-Servers

* **[!UICONTROL Konto]**: Name des Benutzers

* **[!UICONTROL Passwort]**: Passwort des Benutzerkontos

* **[!UICONTROL Datenbank]**: Name der Datenbank

* **[!UICONTROL Arbeitsschema]**: Name Ihres Arbeitsschemas.

* **[!UICONTROL Optionen]**: Der Connector unterstützt die in der folgenden Tabelle aufgeführten Optionen.

Der Connector unterstützt die folgenden Optionen:

| Option | Beschreibung |
|---|---|
| TimeZoneName | Standardmäßig leer, d. h. die Systemzeitzone des Campaign Classic-App-Servers wird verwendet. Die Option kann verwendet werden, um den Sitzungsparameter TIMEZONE zu erzwingen. |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL Server]**: Name des DNS

* **[!UICONTROL Konto]**: Name des Benutzers

* **[!UICONTROL Passwort]**: Passwort des Benutzerkontos

* **[!UICONTROL Datenbank]**: Name Ihrer Datenbank, falls nicht im DSN angegeben. Kann leer bleiben, wenn im DSN angegeben

* **[!UICONTROL Arbeitsschema]**: Name Ihres Arbeitsschemas. [Weitere Informationen](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

