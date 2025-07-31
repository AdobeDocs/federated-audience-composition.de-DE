---
audience: end-user
title: Erstellen und Verwalten von Verbindungen mit föderierten Datenbanken
description: Erfahren Sie, wie Sie Verbindungen mit föderierten Datenbanken erstellen und verwalten.
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 59d7d112421e0ff207ce76122593a111ad9c6cc7
workflow-type: tm+mt
source-wordcount: '1942'
ht-degree: 13%

---

# Erstellen von Verbindungen {#connections-fdb}

>[!AVAILABILITY]
>
>Um auf Verbindungen zugreifen zu können, benötigen Sie eine der folgenden Berechtigungen:
>
>-**Föderierte Datenbank verwalten**
>>-**Föderierte Datenbank anzeigen**
>
>Weitere Informationen zu den erforderlichen Berechtigungen finden Sie im [Handbuch zur Zugriffssteuerung](/help/governance-privacy-security/access-control.md).

Mit der Federated Audience-Komposition von Experience Platform können Sie Zielgruppen aus Data Warehouses von Drittanbietern erstellen und anreichern sowie die Zielgruppen in Adobe Experience Platform importieren.

## Unterstützte Datenbanken {#supported-databases}

Um mit Ihrer Federated Database und Adobe Experience Platform zu arbeiten, müssen Sie zunächst eine Verbindung zwischen den beiden Quellen herstellen. Mit Federated Audience Composition können Sie eine Verbindung zu den folgenden Datenbanken herstellen.

* Amazon Redshift
* Azure Synapse Analytics
* Databricks
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

## Verbindung erstellen {#create}

Um eine Verbindung zu erstellen, wählen Sie **[!UICONTROL Federated Database]** im Abschnitt Federated Data aus.

![Die Schaltfläche „Federated Database“ ist im linken Navigationsbereich hervorgehoben.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

Der Abschnitt Federated Database wird angezeigt. Wählen **[!UICONTROL Federated Database hinzufügen]**, um eine Verbindung zu erstellen.

![Die Schaltfläche „Federated Database hinzufügen“ ist auf der Seite „Federated Database-Anzeige“ hervorgehoben.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

Das Popup-Fenster „Verbindungseigenschaften“ wird angezeigt. Sie können Ihre Verbindung benennen und auswählen, welchen Datenbanktyp Sie erstellen möchten.

![Die zusammengeführten Datenbanktypen werden angezeigt.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

Nach Auswahl eines Typs wird der Abschnitt **[!UICONTROL Details]** angezeigt. Dieser Abschnitt unterscheidet sich je nach dem zuvor ausgewählten Datenbanktyp.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Nur Amazon Redshift AWS, Amazon Redshift Spectrum und Amazon Redshift ServerLess werden unterstützt.

Nach Auswahl von Amazon Redshift können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name der Datenquelle. |
| Konto | Der Benutzername des Kontos. |
| Kennwort | Das Passwort des Kontos. |
| Datenbank | Der Name der Datenbank. Wenn dies im Servernamen angegeben ist, kann dieses Feld leer gelassen werden. |
| Arbeitsschema | Der Name des für Arbeitstabellen zu verwendenden Datenbankschemas. Weitere Informationen zu dieser Funktion finden Sie in der Dokumentation zu [Amazon-Schemata](https://docs.aws.amazon.com/de_de/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.<br/><br/>**Hinweis:** Sie können jedes Schema aus der Datenbank verwenden, einschließlich der Schemata für die temporäre Datenverarbeitung, sofern Sie über die erforderlichen Berechtigungen verfügen, um eine Verbindung zu diesem Schema herzustellen. Sie **müssen** unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |

>[!TAB Azure Synapse Analytics]

Nach Auswahl von Azure Synapse Analytics können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL des Azure Synapse-Servers |
| Konto | Der Benutzername für das Azure Synapse-Konto. |
| Kennwort | Das Kennwort für das Azure Synapse-Konto. |
| Datenbank | Der Name der Datenbank. Wenn dies im Servernamen angegeben ist, kann dieses Feld leer gelassen werden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Für Azure Synapse Analytics können Sie den Authentifizierungstyp angeben, der vom Connector unterstützt wird. Derzeit unterstützt die Federated-Audience-Komposition `ActiveDirectoryMSI`. Weitere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt [Beispiel-Verbindungszeichenfolgen in der Dokumentation von Microsoft](https://learn.microsoft.com/de-de/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"} . |

>[!TAB Datenblöcke]

>[!NOTE]
>
>Sicherer Zugriff auf Ihr externes Databricks-Data-Warehouse über einen privaten Link wird unterstützt. Dazu gehören sichere Verbindungen zu Databricks-Datenbanken, die auf Amazon Web Services (AWS) über einen privaten Link gehostet werden, und Databricks-Datenbanken, die auf Microsoft Azure über VPN gehostet werden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen, um sicheren Zugriff einzurichten.

Nach Auswahl von Datenblöcken können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des DataBricks-Servers. |
| HTTP-Pfad | Der Pfad zu Ihrem Cluster oder Warehouse. Weitere Informationen zum Pfad finden Sie in der [Databricks-Dokumentation zu Verbindungsdetails](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Kennwort | Das Zugriffstoken für den Databricks-Server. Weitere Informationen zu diesem Wert finden Sie in der [Databricks-Dokumentation zu persönlichen Zugriffstoken](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |
| Catalog | Der Name des Databricks-Katalogs. Weitere Informationen zu Katalogen in Databricks finden Sie in der [Databricks-Dokumentation zu Katalogen](https://docs.databricks.com/aws/en/catalogs/){target="_blank"} |
| Arbeitsschema | Der Name des für die Arbeitstabellen zu verwendenden Datenbankschemas. <br/><br/>**Hinweis:** Sie können **Beliebiges** Schema aus der Datenbank verwenden, einschließlich Schemata für die temporäre Datenverarbeitung, sofern Sie über die erforderlichen Berechtigungen verfügen, um eine Verbindung zu diesem Schema herzustellen. Sie **müssen** unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Databricks können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| TimeZoneName | Der Name der zu verwendenden Zeitzone. Dieser Wert stellt den `TIMEZONE` Sitzungsparameter dar. Weitere Informationen zu Zeitzonen finden Sie in der [Databricks-Dokumentation zu Zeitzonen](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}. |

>[!TAB Google BigQuery]

Nach Auswahl von Google BigQuery können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Service-Konto | Die E-Mail-Adresse Ihres Service-Kontos. Weitere Informationen finden Sie in der Dokumentation zum [Google Cloud Service-Konto](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |
| Projekt | Die ID Ihres Projekts. Weitere Informationen finden Sie in der Dokumentation zum [Google Cloud-Projekt](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Datensatz | Der Name des Datensatzes. Weitere Informationen finden Sie in der [Dokumentation zu Google Cloud-Datensätzen](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Pfad der Schlüsseldatei | Die Schlüsseldatei zum Server. Es werden nur `json` Dateien unterstützt. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Google BigQuery können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| ProxyType | Der Proxy-Typ, mit dem die Verbindung zu BigQuery hergestellt wird. Zu den unterstützten Werten gehören `HTTP`, `http_no_tunnel`, `socks4` und `socks5`. |
| ProxyHost | Der Hostname oder die IP-Adresse, unter der der Proxy erreicht werden kann. |
| ProxyUid | Die Port-Nummer, auf der der Proxy ausgeführt wird. |
| ProxyPwd | Das Kennwort für den Proxy. |
| bgpath | **Hinweis:** Dies gilt nur für das Tool **Massenladen** (Cloud SDK). <br/><br/> Der Pfad zum Ordner „bin“ von Cloud SDK auf dem Server. Sie müssen dies nur festlegen, wenn Sie das `google-cloud-sdk` an einen anderen Speicherort verschoben haben oder wenn Sie die Variable PATH vermeiden möchten. |
| GCloudConfigName | **Hinweis:** Dies gilt nur für das Tool **Bulk-Load** (Cloud SDK) über Version 7.3.4. <br/><br/> Der Name der Konfiguration, die die Parameter zum Laden der Daten speichert. Standardmäßig ist dieser Wert `accfda`. |
| GCloudDefaultConfigName | **Hinweis:** Dies gilt nur für das Tool **Bulk-Load** (Cloud SDK) über Version 7.3.4. <br/><br/> Der Name der temporären Konfiguration, um die Hauptkonfiguration zum Laden von Daten neu zu erstellen. Standardmäßig ist dieser Wert `default`. |
| GCloudRecreateConfig | **Hinweis:** Dies gilt nur für das Tool **Bulk-Load** (Cloud SDK) über Version 7.3.4. <br/><br/> Ein boolescher Wert, mit dem Sie entscheiden können, ob der Massenlademechanismus die Google Cloud SDK-Konfigurationen automatisch neu erstellen, löschen oder ändern soll. Wenn dieser Wert auf `false` festgelegt ist, lädt der Massenlademechanismus Daten mit einer vorhandenen Konfiguration auf dem Computer. Wenn dieser Wert auf `true` festgelegt ist, stellen Sie sicher, dass Ihre Konfiguration ordnungsgemäß eingerichtet ist. Andernfalls wird der `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` angezeigt und der Lademechanismus wird auf den standardmäßigen Lademechanismus zurückgesetzt. |

>[!TAB Microsoft-Fabric]

Nach Auswahl von Microsoft Fabric können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL für den Microsoft Fabric-Server. |
| Anwendungs-ID | Die Anwendungs-ID für Microsoft Fabric. Weitere Informationen zur Anwendungs-ID finden Sie in der Dokumentation zu [Microsoft Fabric beim Einrichten der Anwendung](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Client-Geheimnis | Das Client-Geheimnis für die Anwendung. Weitere Informationen zum Client-Geheimnis finden Sie in der [Microsoft Fabric-Dokumentation unter Anwendungseinrichtung](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Microsoft Fabric können Sie die folgenden zusätzlichen Optionen festlegen:

| Option | Beschreibung |
| ------ | ----------- |
| Authentifizierung | Der vom Connector verwendete Authentifizierungstyp. Folgende Werte werden unterstützt: `ActiveDirectoryMSI`. Weitere Informationen finden Sie in der [Microsoft-Dokumentation zu Warehouse-Konnektivität](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB Oracle]

>[!IMPORTANT]
>
>Der Oracle-Datenbank-Connector kann derzeit **nur** für Anwendungsfälle zur Erstellung und Anreicherung von Zielgruppen verwendet werden.
>
>Wenden Sie sich vor der Einrichtung Ihrer Oracle-Datenbank an Ihren Adobe-Kundenbetreuer.

Nach Auswahl von Oracle können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL für den Oracle-Server. |
| Konto | Der Benutzername des Kontos. |
| Kennwort | Das Passwort des Kontos. |

>[!TAB Snowflake]

>[!NOTE]
>
>Sicherer Zugriff auf Ihr externes Snowflake-Data-Warehouse über einen privaten Link wird unterstützt. Ihr Snowflake-Konto muss auf Amazon Web Services (AWS) oder Azure gehostet werden und sich in derselben Region wie Ihre Umgebung mit der Funktion „Komposition föderierter Zielgruppen“ befinden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen, um einen sicheren Zugriff auf Ihr Snowflake-Konto einzurichten.

Nach Auswahl von Snowflake können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des Servers. |
| Benutzer | Der Benutzername für das Konto. |
| Kennwort | Das Kennwort für das Konto. |
| Datenbank | Der Name der Datenbank. Wenn dies im Servernamen angegeben ist, kann dieses Feld leer gelassen werden. |
| Arbeitsschema | Der Name des für die Arbeitstabellen zu verwendenden Datenbankschemas. <br/><br/>**Hinweis:** Sie können **Beliebiges** Schema aus der Datenbank verwenden, einschließlich Schemata für die temporäre Datenverarbeitung, sofern Sie über die erforderlichen Berechtigungen verfügen, um eine Verbindung zu diesem Schema herzustellen. Sie **müssen** unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |
| Privater Schlüssel | Der private Schlüssel für Ihre Datenbankverbindung. Sie können eine `.pem`-Datei von Ihrem lokalen System hochladen. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Snowflake können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| workschema | Der Name des für Arbeitstabellen zu verwendenden Datenbankschemas. |
| TimeZoneName | Der Name der zu verwendenden Zeitzone. Dieser Wert stellt den `TIMEZONE` Sitzungsparameter dar. Standardmäßig wird die Systemzeitzone verwendet. Weitere Informationen zu Zeitzonen finden Sie in der [Snowflake-Dokumentation zu Zeitzonen](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | Der Tag, an dem die Woche beginnen soll. Dieser Wert stellt den `WEEK_START` Sitzungsparameter dar. Weitere Informationen zum Wochenstart finden Sie in der [Snowflake-Dokumentation zum Parameter „Week Start“](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"} |
| UseCachedResult | Ein boolescher Wert, der bestimmt, ob die zwischengespeicherten Ergebnisse von Snowflake verwendet werden. Dieser Wert stellt den `USE_CACHED_RESULTS` Sitzungsparameter dar. Standardmäßig ist dieser Wert auf „true“ festgelegt. Weitere Informationen zu diesem Parameter finden Sie in der [Snowflake-Dokumentation zu persistenten Ergebnissen](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | Die Anzahl der Threads, die für den Bulk Loader von Snowflake verwendet werden sollen. Je mehr Threads hinzugefügt werden, desto besser ist die Leistung bei größeren Massenladevorgängen. Standardmäßig ist dieser Wert auf 1 festgelegt. |
| chunkSize | Die Dateigröße des Blocks jedes Bulk-Loaders. Bei gleichzeitiger Verwendung mit mehr Threads können Sie die Leistung Ihrer Massenladevorgänge verbessern. Standardmäßig ist dieser Wert auf 128 MB festgelegt. Weitere Informationen zu Blockgrößen finden Sie in der [Snowflake-Dokumentation unter Vorbereiten von Datendateien](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | Der Name einer vorab bereitgestellten internen Staging-Umgebung. Dies kann in Massenladevorgängen verwendet werden, anstatt einen neuen temporären Schritt zu erstellen. |

>[!TAB Vertica Analytics]

Nach Auswahl von Vertica Analytics können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL des Vertica Analytics-Servers |
| Konto | Der Benutzername des Kontos. |
| Kennwort | Das Passwort des Kontos. |
| Datenbank | Der Name der Datenbank. Wenn dies im Servernamen angegeben ist, kann dieses Feld leer gelassen werden. |
| Arbeitsschema | Der Name des für die Arbeitstabellen zu verwendenden Datenbankschemas. <br/><br/>**Hinweis:** Sie können **Beliebiges** Schema aus der Datenbank verwenden, einschließlich Schemata für die temporäre Datenverarbeitung, sofern Sie über die erforderlichen Berechtigungen verfügen, um eine Verbindung zu diesem Schema herzustellen. Sie **müssen** unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Vertica Analytics können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| TimeZoneName | Der Name der zu verwendenden Zeitzone. Dieser Wert stellt den `TIMEZONE` Sitzungsparameter dar. Weitere Informationen zu Zeitzonen finden Sie in der [Vertica Analytics-Dokumentation zu Zeitzonen](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"} |

>[!ENDTABS]

Nachdem Sie die Details der Verbindung hinzugefügt haben, beachten Sie die folgenden zusätzlichen Einstellungen:

>[!NOTE]
>
>Um die Federated Audience-Komposition für eine bestimmte Datenbank zu verwenden, müssen **alle** IP-Adressen, die mit dieser Datenbank verknüpft sind, Zulassungsliste werden.

| Einstellungen | Details |
| -------- | ------- |
| Verbindung aktivieren | Ein boolescher Umschalter, der bestimmt, ob die Verbindung automatisch aktiviert wird. |
| Server-IPs | Ein Popup, das anzeigt, welche IP-Adressen für die Verbindung mit der Datenbank auf die Zulassungsliste gesetzt werden müssen. |
| Testen der Verbindung | Ermöglicht die Überprüfung Ihrer Konfigurationsdetails. |

Sie können jetzt **[!UICONTROL Funktionen bereitstellen]** und anschließend **[!UICONTROL Hinzufügen]** auswählen, um die Verbindung zwischen der Federated-Datenbank und Experience Platform abzuschließen.
