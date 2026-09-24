---
audience: end-user
title: Erstellen und Verwalten von Verbindungen mit Federated Database in der Experience Platform-Benutzeroberfläche
description: Erfahren Sie, wie Sie in der Experience Platform-Benutzeroberfläche Verbindungen mit Federated Database erstellen und verwalten.
TQID: https://experienceleague.adobe.com/6-pzawt2ndn2MKLyYLXPMy-ec1SIOsQI5frTt9IqOX0
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '4385'
ht-degree: 78%
---
# Erstellen von Verbindungen in der Experience Platform-Benutzeroberfläche

>[!AVAILABILITY]
>
>Die neue einheitliche Verbindungserfahrung steht nur ausgewählten Kunden zur Verfügung. Weitere Informationen erhalten Sie bei der Adobe-Kundenunterstützung.
>
>Wenn Sie keinen Zugriff auf das neue Verbindungserlebnis haben, lesen Sie „Verbindungen - [Übersicht](./home.md).
>
>Um auf Verbindungen zugreifen zu können, benötigen Sie eine der folgenden Berechtigungen:
>
>-**Föderierte Datenbank verwalten**
>-**Föderierte Datenbank anzeigen**
>
>Weitere Informationen zu den erforderlichen Berechtigungen finden Sie im [Handbuch zur Zugriffssteuerung](/help/governance-privacy-security/access-control.md).

Die Komposition föderierter Zielgruppen in Experience Platform ermöglicht es Ihnen, Zielgruppen in Data Warehouses von Drittanbietern zu erstellen und anzureichern und die Zielgruppen in Adobe Experience Platform zu importieren.

## Unterstützte Datenbanken {#supported-databases}

>[!CONTEXTUALHELP]
>id="platform_sources_snowflake_privatekey"
>title="Privater Schlüssel"
>abstract="Temporärer leerer Inhalt."

>[!CONTEXTUALHELP]
>id="platform_sources_snowflake_keyfilepath"
>title="Schlüsseldateipfad"
>abstract="Temporärer leerer Inhalt."

Um mit Ihrer föderierten Datenbank und Adobe Experience Platform zu arbeiten, müssen Sie zunächst eine Verbindung zwischen den beiden Quellen herstellen. Mit der Komposition föderierter Zielgruppen können Sie eine Verbindung zu den folgenden Datenbanken herstellen.

- Amazon Redshift
- Azure Synapse Analytics
- DataBricks
- Google BigQuery
- Microsoft Fabric
- Oracle
- Snowflake
- Teradata
- Vertica Analytics

## Erstellen einer Verbindung {#create}

>[!CONTEXTUALHELP]
>id="platform_sources_serverip"
>title="Server-IP"
>abstract="Die IP-Adressen, die für die Verbindung mit der Datenbank auf die Zulassungsliste gesetzt werden müssen."

Um eine Verbindung zu erstellen, wählen Sie **[!UICONTROL Quellen]** im Abschnitt **[!UICONTROL Verbindungen]** aus.

Der Quellkatalog wird angezeigt. Wählen Sie **[!UICONTROL Federated Data]** aus, um die Liste der für Ihre Organisation verfügbaren Federated-Datenbanken anzuzeigen.

![Der Abschnitt „Federated Data“ im Quellkatalog ist hervorgehoben.](/help/connections/assets/integrated/federated-data-sources.png)

Nachdem Sie den Federated Database-Typ ausgewählt haben, wählen Sie **[!UICONTROL Einrichten]**, wenn Sie eine neue Verbindung herstellen, oder **[!UICONTROL Daten hinzufügen]** wenn Sie eine vorhandene Verbindung verwenden.

Die Seite Konto verbinden wird angezeigt. Sie können entweder ein **vorhandenes** Konto verwenden oder ein **neues** Konto erstellen.

### Vorhandenes Konto {#existing-account}

Wenn Sie **[!UICONTROL Vorhandenes Konto]** auswählen, können Sie eine der zuvor erstellten Quellverbindungen auswählen.

![Ein Beispiel für den Abschnitt „Vorhandene Konten“ wird angezeigt.](/help/connections/assets/integrated/existing-account.png)

>[!NOTE]
>
>Um eine sichere Konnektivität über einen privaten Link oder ein VPN anzufordern, **müssen** entweder Privacy and Security Shield oder Healthcare Shield lizenziert haben.

### Neues Konto {#new-account}

Wenn Sie **[!UICONTROL Neues Konto]** auswählen, wird die Seite mit den Verbindungsdetails angezeigt. Auf dieser Seite können Sie Details zu Ihrer Verbindung festlegen, einschließlich Kontoname, Beschreibung und Details zur Kontoauthentifizierung. Der Abschnitt zur Kontoauthentifizierung unterscheidet sich je nach dem zuvor ausgewählten Datenbanktyp.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Es werden nur Amazon Redshift AWS, Amazon Redshift Spectrum und Amazon Redshift Serverless unterstützt.
>
>Darüber hinaus wird der sichere Zugriff auf Ihr externes Amazon Redshift-Data-Warehouse über einen privaten Link unterstützt.

Nach Auswahl von Amazon Redshift können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name der Datenquelle. |
| Konto | Der Benutzername des Kontos. |
| Passwort | Das Passwort des Kontos. |
| Datenbank | Der Name der Datenbank. Wenn dies im Server-Namen angegeben ist, kann dieses Feld leer gelassen werden. |
| Arbeitsschema | Name des Datenbankschemas, das für Arbeitstabellen verwendet werden soll. Weitere Informationen zu dieser Funktion finden Sie in der [Dokumentation zu Amazon-Schemata](https://docs.aws.amazon.com/de_de/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.<br/><br/>**Hinweis:** Sie können jedes Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen. Sie **müssen** jedoch unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |

>[!TAB Azure Synapse Analytics]

>[!NOTE]
>
>Wenn Sie eine sichere Verbindung mit Azure Synapse Analytics einrichten möchten, wenden Sie sich an die Adobe-Kundenunterstützung.

Nach Auswahl von Azure Synapse Analytics können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL des Azure Synapse-Servers. |
| Konto | Die Anwendungs-ID (**Client-ID**) der Registrierung der Azure-App. |
| Passwort | Der **Client-Geheimnis**-Wert der Azure-App. |
| Datenbank | Der Name der Datenbank. Wenn dies im Server-Namen angegeben ist, kann dieses Feld leer gelassen werden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Für Azure Synapse Analytics können Sie den Authentifizierungstyp angeben, der vom Connector unterstützt wird. Derzeit unterstützt die Komposition föderierter Zielgruppen `ActiveDirectoryMSI`. Weitere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zu [Beispiel-Verbindungszeichenfolgen in der Dokumentation von Microsoft](https://learn.microsoft.com/de-de/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}. |

Alternativ können Sie Ihre Azure Synapse Analytics-Verbindung sicher konfigurieren, indem Sie die Service-Prinzipal-Authentifizierung verwenden. Sie sollten die Service-Prinzipal-Authentifizierung sowohl für produktionsfähige Integrationen als auch für Automatisierungsszenarien nutzen.

+++ Voraussetzungen

Beachten Sie vor dem Einrichten der Service-Prinzipal-Authentifizierung die folgenden Voraussetzungen:

- Azure-Abonnement mit Zugriff auf Microsoft Entra ID
- Azure Synapse-Arbeitsbereich und -Datenbank
- Berechtigung zum Erstellen der App-Registrierung
- Berechtigung zum Verwalten von Azure Synapse-Datenbankrollen
- Berechtigung zum Aktualisieren von Konfigurationen föderierter Datenbanken

+++

Im Azure-Portal müssen Sie zunächst eine neue App-Registrierung erstellen. Wählen Sie **Registrieren** aus, nachdem Sie der Anwendung einen eindeutigen Namen gegeben haben. Die Seite **Überblick** wird angezeigt. Notieren Sie sich die Werte **Application (Client) ID** (Anwendungs-(Client-)ID) und **Directory (Tenant) ID** (Verzeichnis-(Mandanten-)ID).

![Die Anwendungs-(Client-)ID auf der Überblicksseite ist hervorgehoben.](/help/connections/assets/home/azure-client-id.png)

Wählen Sie in der neu registrierten Anwendung **Zertifikate und Geheimnisse** aus. Wählen Sie von hier aus **Neues Client-Geheimnis** im Abschnitt **Client-Geheimnisse** aus, um ein neues Client-Geheimnis zu erstellen. Nachdem Sie eine Beschreibung und eine Gültigkeit angegeben haben, wählen Sie **Hinzufügen** aus, um das Client-Geheimnis zu generieren.

>[!IMPORTANT]
>
>Kopieren Sie nach dem Generieren Ihres Client-Geheimnisses den **Wert des Client-Geheimnisses** und speichern Sie ihn sicher. Dieser Wert wird **nicht** wieder angezeigt.

Nachdem Sie Ihr Client-Geheimnis generiert haben, müssen Sie prüfen, ob Sie der Ressource die Identität **Service-Prinzipal** gewährt haben.

Weitere Informationen zum Zuweisen von Identitäten zu Ressourcen finden Sie im [Handbuch zu verwalteten Identitäten für Azure Synapse Analytics](https://learn.microsoft.com/de-de/azure/synapse-analytics/synapse-service-identity).

Da Sie nun alle Azure-seitigen Konfigurationen abgeschlossen haben, können Sie jetzt Ihre Konfigurationen für die Komposition föderierter Zielgruppen einrichten.

Legen Sie innerhalb Ihrer Azure Synapse-Verbindung die folgenden Konfigurationsdetails fest:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL des Azure Synapse-Servers. |
| Konto | Die Anwendungs-ID (**Client-ID**) der Registrierung der Azure-App. |
| Passwort | Der **Client-Geheimnis**-Wert der Azure-App. |
| Datenbank | Der Name der Datenbank. Wenn dies im Server-Namen angegeben ist, kann dieses Feld leer gelassen werden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Um die Service-Prinzipal-Authentifizierung verwenden zu können, müssen Sie `Authentication="ActiveDirectoryServicePrincipal"` festlegen. |

>[!TAB DataBricks]

>[!NOTE]
>
>Der sichere Zugriff auf Ihr externes Data Warehouse von Data Bricks über einen privaten Link wird unterstützt. Dazu gehören sichere Verbindungen zu DataBricks-Datenbanken, die auf Amazon Web Services (AWS) über einen privaten Link gehostet werden, und DataBricks-Datenbanken, die auf Microsoft Azure über VPN gehostet werden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen, um sicheren Zugriff einzurichten.

Nach Auswahl von DataBricks können Sie mit der Authentifizierungsmethode auswählen, die Sie beim Herstellen einer Verbindung mit Federated Audience Composition verwenden möchten.

Wenn Sie **[!UICONTROL Standardauthentifizierung]** auswählen, können Sie die folgenden Anmeldedetails hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des DataBricks-Servers. |
| Passwort | Das Zugriffstoken für den DataBricks-Server. Weitere Informationen zu diesem Wert finden Sie in der [DataBricks-Dokumentation zu persönlichen Zugriffstoken](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |

Wenn Sie **[!UICONTROL OAuth2-Authentifizierungs-Code]** auswählen, können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des DataBricks-Servers. |
| Client-ID | Die Client-ID von Ihrem DataBricks-Server. Dieses Feld wird verwendet, um die Anwendung bei der OAuth 2.0-Authentifizierung zu identifizieren, und dient als Benutzername für Ihr Projekt. |
| Client-Geheimnis | Das Client-Geheimnis aus Ihrem DataBricks-Server. Diese vertraulichen Anmeldedaten werden mit der Client-ID ausgestellt und dienen als Passwort für Ihr Projekt. |
| Zugriffsumfang | Vorausgefüllte Informationen, die die Bereiche auflisten, für die Ihr OAuth-Token auf Ihrem DataBricks-Server autorisiert ist. |

Wenn Sie **[!UICONTROL Service-Prinzipal-Authentifizierung]** auswählen, können Sie die folgenden Informationen hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des DataBricks-Servers. |
| Client-ID | Die Client-ID von Ihrem DataBricks-Server. Dieses Feld dient als Benutzername für Ihr Projekt. |
| Client-Geheimnis | Das Client-Geheimnis aus Ihrem DataBricks-Server. Dieses Feld dient als Passwort für Ihr Projekt. |

Nach der Eingabe Ihrer Anmeldeinformationen können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| HTTP-Pfad | Der Pfad zu Ihrem Cluster oder Warehouse. Weitere Informationen zum Pfad finden Sie in der [Dokumentation zu DataBricks unter Verbindungsdetails](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Catalog | Der Name des DataBricks-Katalogs. Weitere Informationen zu Katalogen in DataBricks finden Sie in der [DataBricks-Dokumentation zu Katalogen](https://docs.databricks.com/aws/en/catalogs/){target="_blank"} |
| Arbeitsschema | Der Name des Datenbankschemas, das für Arbeitstabellen verwendet werden soll. <br/><br/>**Hinweis**: Sie können **jedes** Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen. Sie **müssen** jedoch unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für DataBricks können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| TimeZoneName | Der Name der zu verwendenden Zeitzone. Dieser Wert stellt den Sitzungsparameter `TIMEZONE` dar. Weitere Informationen zu Zeitzonen finden Sie in der [DataBricks-Dokumentation zu Zeitzonen](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}. |

>[!TAB Google BigQuery]

>[!NOTE]
>
>Der sichere Zugriff auf Ihr externes Google BigQuery-Data-Warehouse über VPN wird unterstützt.

Nach der Auswahl von Google BigQuery können Sie festlegen, welche Authentifizierungsmethode Sie beim Herstellen einer Verbindung mit der Komposition föderierter Zielgruppen verwenden möchten.

Wenn Sie **[!UICONTROL Standardauthentifizierung]** auswählen, können Sie die folgenden Anmeldeinformationen hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Service-Konto | Die E-Mail-Adresse Ihres Service-Kontos. Weitere Informationen finden Sie unter [Dokumentation zu Google Cloud-Service-Konten](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |

Wenn Sie **[!UICONTROL OAuth2-Autorisierungs]** Code auswählen, können Sie die folgenden Anmeldeinformationen hinzufügen:

>[!NOTE]
>
>Bevor Sie eine Verbindung zu Google BigQuery mit OAuth 2.0 herstellen, müssen Sie Ihre Umleitungs-URL in Ihrem Google Cloud-Projekt konfigurieren. Fügen Sie die Umleitungs-URL `https://fac-oauth.adobe.io/oauth` unter Ihrer OAuth 2.0-Client-ID-Konfiguration zu Ihrem Google Cloud-Projekt hinzu.

| Feld | Beschreibung |
| ----- | ----------- |
| Client-ID | Die Client-ID aus Ihrem Google BigQuery-Projekt. Dieses Feld dient als Benutzername für Ihr Projekt. |
| Client-Geheimnis | Das Client-Geheimnis aus Ihrem Google BigQuery-Projekt. Dieses Feld dient als Passwort für Ihr Projekt. |
| Zugriffsumfang | Vorausgefüllte Informationen, die die Bereiche auflisten, für die Ihr OAuth-Token in Ihren Google Cloud-Ressourcen autorisiert ist. |

Wählen Sie **[!UICONTROL Anmelden]** aus, um Ihre Authentifizierung zu beenden.

Wenn Sie **[!UICONTROL WIF]** auswählen, müssen Sie **keine** Anmeldeinformationen hinzufügen. Sie **müssen** die Client-Bibliothekskonfiguration jedoch als &quot;**[!UICONTROL -Dateipfad“]**. Weitere Informationen zur Konfiguration der Client-Bibliothek finden Sie im [Abschnitt zur Konfiguration für Google BigQuery (Workload Identity Federation)](#wif-configuration).

Nach der Eingabe Ihrer Anmeldeinformationen können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Projekt | Die ID Ihres Projekts. Weitere Informationen finden Sie unter [Dokumentation zu Google Cloud-Projekten](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Datensatz | Der Name des Datensatzes. Weitere Informationen finden Sie unter [Dokumentation zu Google Cloud-Datensätzen](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Pfad der Konfigurationsdatei | Die Konfigurationsdatei auf dem Server. Es werden nur `json`-Dateien unterstützt. |
| Speicherort für den Google-Bucket | Der Speicherort Ihres Google Buckets. Sie müssen dieses Feld nur hinzufügen, wenn Sie die Aktivität **Dimension ändern** in Ihrer Komposition verwenden. Weitere Informationen finden Sie in der [Dokumentation zu den Google Cloud-Bucket-Speicherorten](https://docs.cloud.google.com/storage/docs/locations){target="_blank"}. |
| REST-API-Connector verwenden | Ein Schalter, mit dem der REST-API-Connector verwendet werden kann. Diese Option ist **nur** verfügbar, wenn Sie die Standardauthentifizierung verwenden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Google BigQuery können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| ProxyType | Der Proxy-Typ, mit dem die Verbindung zu BigQuery hergestellt wird. Zu den unterstützten Werten gehören `HTTP`, `http_no_tunnel`, `socks4` und `socks5`. |
| ProxyHost | Der Host-Name oder die IP-Adresse, um den Proxy zu erreichen. |
| ProxyUid | Die Port-Nummer, auf der der Proxy ausgeführt wird. |
| ProxyPwd | Das Passwort für den Proxy. |
| bgpath | **Hinweis**: Dies gilt nur für das **Tool für Massenladung** (Cloud SDK). <br/><br/> Der Pfad zum Cloud SDK-Klassenverzeichnis am Server. Sie müssen dies nur festlegen, wenn Sie das Verzeichnis `google-cloud-sdk` an einen anderen Speicherort verschoben haben oder wenn Sie die Verwendung der Variable „PATH“ vermeiden möchten. |
| GCloudConfigName | **Hinweis**: Dies gilt nur für das **Tool für Massenladung** (Cloud SDK), Version 7.3.4 oder höher. <br/><br/> Der Name der Konfiguration, die die Parameter zum Laden der Daten speichert. Standardmäßig ist dieser Wert `accfda`. |
| GCloudDefaultConfigName | **Hinweis**: Dies gilt nur für das **Tool für Massenladung** (Cloud SDK), Version 7.3.4 und höher. <br/><br/> Der Name der temporären Konfiguration, um die Hauptkonfiguration zum Laden von Daten neu zu erstellen. Standardmäßig ist dieser Wert `default`. |
| GCloudRecreateConfig | **Hinweis**: Dies gilt nur für das **Tool für Massenladung** (Cloud SDK), Version 7.3.4 und höher. <br/><br/> Ein boolescher Wert, mit dem Sie festlegen können, ob der Massenlademechanismus die Google Cloud SDK-Konfigurationen automatisch neu erstellen, löschen oder ändern soll. Wenn dieser Wert auf `false` festgelegt ist, lädt der Massenlademechanismus Daten mit einer vorhandenen Konfiguration am Computer. Wenn dieser Wert auf `true` festgelegt ist, stellen Sie sicher, dass Ihre Konfiguration ordnungsgemäß eingerichtet ist. Andernfalls wird der Fehler `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` angezeigt und der Lademechanismus wird auf den standardmäßigen Lademechanismus zurückgesetzt. |
| **restEndpoint** | Der Endpunkt für Ihren Apigee-Proxy. Sie müssen diesen Endpunkt nur verwenden, wenn Sie den REST-API-Connector mit dem Apigee-Proxy nutzen. Wenn Sie den Apigee-Proxy verwenden, aktivieren Sie die Einstellung **REST-API-Connector verwenden**. Weitere Informationen zum Setup finden Sie im Abschnitt [Unterstützung für das Google BigQuery Apigee-Gateway](#apigee). |

>[!TAB Microsoft Fabric]

Nach Auswahl von Microsoft Fabric können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL für den Microsoft Fabric-Server. |
| Anwendungs-ID | Die Anwendungs-ID für Microsoft Fabric. Weitere Informationen zur Anwendungs-ID finden Sie in der [Microsoft Fabric-Dokumentation zum Einrichten der Anwendung](https://learn.microsoft.com/de-de/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Client-Geheimnis | Das Client-Geheimnis für die Anwendung. Weitere Informationen zum Client-Geheimnis finden Sie in der [Microsoft Fabric-Dokumentation zum Einrichten der Anwendung](https://learn.microsoft.com/de-de/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Microsoft Fabric können die folgenden zusätzlichen Optionen festlegen:

| Option | Beschreibung |
| ------ | ----------- |
| Authentifizierung | Vom Connector verwendeter Authentifizierungstyp. Zu den unterstützten Werten gehört `ActiveDirectoryMSI`. Weitere Informationen finden Sie in der [Microsoft-Dokumentation zu Warehouse-Konnektivität](https://learn.microsoft.com/de-de/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB Oracle]

>[!NOTE]
>
>Die Komposition föderierter Zielgruppen unterstützt die Einrichtung von föderierten Verbindungen mit Oracle-Datenbanken der Version 11g oder höher, die auf AWS, Azure, Exadata oder einer privaten Cloud gehostet werden (sofern Zugriff über ein externes Netzwerk besteht). Wenn Sie weitere Fragen zur Oracle-Datenbankeinrichtung haben oder eine sichere Verbindung mit Oracle herstellen müssen, wenden Sie sich bitte an die Adobe-Kundenunterstützung.

Nach Auswahl von Oracle können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL für den Oracle-Server. |
| Konto | Der Benutzername des Kontos. |
| Passwort | Das Passwort des Kontos. |

>[!TAB Snowflake]

>[!NOTE]
>
>Sicherer Zugriff auf Ihr externes Snowflake-Data-Warehouse über einen privaten Link wird unterstützt. Ihr Snowflake-Konto muss auf Amazon Web Services (AWS) oder Azure gehostet werden und sich in derselben Region wie Ihre Umgebung mit der Funktion „Komposition föderierter Zielgruppen“ befinden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen, um sicheren Zugriff auf Ihr Snowflake-Konto einzurichten.

Nach der Auswahl von Snowflake können Sie festlegen, welche Authentifizierungsmethode Sie beim Herstellen einer Verbindung mit der Komposition föderierter Zielgruppen verwenden möchten.

Wenn Sie **[!UICONTROL Standardauthentifizierung]** auswählen, können Sie die folgenden Anmeldeinformationen hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des Servers. |
| Benutzerin bzw. Benutzer | Der Benutzername für das Konto. |
| Passwort | Das Passwort für das Konto. |

Wenn Sie **[!UICONTROL Schlüsselpaar-Authentifizierung]** auswählen, können Sie die folgenden Anmeldeinformationen hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des Servers. |
| Benutzerin bzw. Benutzer | Der Benutzername für das Konto. |
| Privater Schlüssel | Der private Schlüssel für das Konto. Es werden nur `.pem`-Dateien unterstützt. |
| Passwort | (Optional) Das Passwort für das Konto. |

Wenn Sie **[!UICONTROL OAuth2-Autorisierungs]** Code auswählen, können Sie die folgenden Anmeldeinformationen hinzufügen:

>[!NOTE]
>
>Bevor Sie eine Verbindung zu Snowflake mit OAuth 2.0 herstellen, müssen Sie Ihre Umleitungs-URL in Ihrem Snowflake OAuth-Integrationsobjekt konfigurieren. Fügen Sie die Umleitungs-URL `https://fac-oauth.adobe.io/oauth` zu Ihrer Snowflake OAuth-Integrationskonfiguration hinzu.

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Der Name des Servers. |
| Client-ID | Die Client-ID aus Ihrem Snowflake-Projekt. Dieses Feld dient als Benutzername für Ihr Projekt. |
| Client-Geheimnis | Das Client-Geheimnis aus Ihrem Snowflake-Projekt. Dieses Feld dient als Passwort für Ihr Projekt. |

Wählen Sie **[!UICONTROL Anmelden]** aus, um Ihre Authentifizierung zu beenden.

Nach der Eingabe Ihrer Anmeldeinformationen können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Datenbank | Der Name der Datenbank. Wenn dies im Server-Namen angegeben ist, kann dieses Feld leer gelassen werden. |
| Arbeitsschema | Der Name des Datenbankschemas, das für Arbeitstabellen verwendet werden soll. <br/><br/>**Hinweis**: Sie können **jedes** Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen. Sie **müssen** jedoch unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |
| Privater Schlüssel | Der Base64-kodierte private Schlüssel Ihres Snowflake-Kontos. Sie können entweder verschlüsselte oder unverschlüsselte private Schlüssel generieren. Wenn Sie einen verschlüsselten privaten Schlüssel verwenden, müssen Sie auch eine Passphrase für den privaten Schlüssel angeben, wenn Sie sich bei Experience Platform authentifizieren. Weitere Informationen finden Sie im Handbuch unter [Abrufen des privaten Snowflake](https://experienceleague.adobe.com/de/docs/experience-platform/sources/connectors/databases/snowflake)Schlüssels). |
| Passphrase für privaten Schlüssel | Die Passphrase für den privaten Schlüssel ist eine zusätzliche Sicherheitsebene, die Sie bei der Authentifizierung mit einem verschlüsselten privaten Schlüssel verwenden müssen. Sie müssen die Passphrase nicht angeben, wenn Sie einen unverschlüsselten privaten Schlüssel verwenden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Snowflake können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| workschema | Name des Datenbankschemas, das für Arbeitstabellen verwendet werden soll. |
| TimeZoneName | Der Name der zu verwendenden Zeitzone. Dieser Wert stellt den Sitzungsparameter `TIMEZONE` dar. Standardmäßig wird die Zeitzone des Systems verwendet. Weitere Informationen zu Zeitzonen finden Sie in der [Snowflake-Dokumentation zu Zeitzonen](https://docs.snowflake.com/de/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | Der Tag, an dem die Woche beginnen soll. Dieser Wert stellt den Sitzungsparameter `WEEK_START` dar. Weitere Informationen zum Wochenstart finden Sie in der [Snowflake-Dokumentation zum Wochenstartparameter](https://docs.snowflake.com/de/sql-reference/parameters#week-start){target="_blank"} |
| UseCachedResult | Ein boolescher Wert, der bestimmt, ob die zwischengespeicherten Ergebnisse von Snowflake verwendet werden. Dieser Wert stellt den Sitzungsparameter `USE_CACHED_RESULTS` dar. Standardmäßig ist dieser Wert auf „wahr“ festgelegt. Weitere Informationen zu diesem Parameter finden Sie in der [Snowflake-Dokumentation zu gespeicherten Ergebnissen](https://docs.snowflake.com/de/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | Die Anzahl der Threads, die für den Massenlader von Snowflake verwendet werden sollen. Je mehr Threads hinzugefügt werden, desto besser ist die Leistung bei größeren Massenladevorgängen. Standardmäßig ist dieser Wert auf 1 festgelegt. |
| chunkSize | Die Dateigröße jedes Blocks des Massenladers. Bei gleichzeitiger Verwendung mit mehreren Threads können Sie die Leistung Ihrer Massenladevorgänge verbessern. Standardmäßig ist dieser Wert auf 128 MB festgelegt. Weitere Informationen zu Blockgrößen finden Sie in der [Snowflake-Dokumentation zum Vorbereiten von Datendateien](https://docs.snowflake.com/de/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | Der Name einer vorab bereitgestellten internen Staging-Umgebung. Dieser kann bei Massenladevorgängen verwendet werden, anstatt einen neuen temporären Staging-Bereich zu erstellen. |

>[!TAB Teradata]

>[!NOTE]
>
>Um eine Verbindung mit Teradata herzustellen, **müssen** verschiedene Voraussetzungen erfüllt sein, einschließlich der Installation von Datenbanktreibern. Bitte wenden Sie sich an die Adobe-Kundenunterstützung, um weitere Informationen zu erhalten.

Nach Auswahl von Teradata können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL des Teradata-Servers. |
| Konto | Der Benutzername, den die Datenbank für die Open Database Connectivity-Sitzung (ODBC) verwendet. |
| Passwort | Das Passwort, mit dem Sie eine Verbindung zur ODBC-Sitzung herstellen. |
| Datenbank | Der Name der Datenbank. |
| Optionen | Zusätzliche Optionen für die Verbindung. Für Teradata ist das Hinzufügen beider aufgelisteter Optionen **zwingend erforderlich**. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Teradata können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| `workTableSchema` | Der Name des Schemas für Arbeitstabellen. |
| `ODBCLib` | Der Speicherort der ODBC-Bibliothek des Systems, den Sie verwenden können, wenn Sie Teradata mit einer anderen ODBC-Verbindung kombinieren. |

>[!TAB Vertica Analytics]

Nach Auswahl von Vertica Analytics können Sie die folgenden Details hinzufügen:

| Feld | Beschreibung |
| ----- | ----------- |
| Server | Die URL des Vertica Analytics-Servers. |
| Konto | Der Benutzername des Kontos. |
| Passwort | Das Passwort des Kontos. |
| Datenbank | Der Name der Datenbank. Wenn dies im Server-Namen angegeben ist, kann dieses Feld leer gelassen werden. |
| Arbeitsschema | Der Name des Datenbankschemas, das für Arbeitstabellen verwendet werden soll. <br/><br/>**Hinweis**: Sie können **jedes** Schema aus der Datenbank verwenden, einschließlich Schemata, die für die temporäre Datenverarbeitung verwendet werden, sofern Sie über die erforderliche Berechtigung zum Herstellen einer Verbindung mit diesem Schema verfügen. Sie **müssen** jedoch unterschiedliche Arbeitsschemata verwenden, wenn Sie mehrere Sandboxes mit derselben Datenbank verbinden. |
| Optionen | Zusätzliche Optionen für die Verbindung. Die verfügbaren Optionen sind in der folgenden Tabelle aufgeführt. |

Für Vertica Analytics können Sie die folgenden zusätzlichen Optionen festlegen:

| Optionen | Beschreibung |
| ------- | ----------- |
| TimeZoneName | Der Name der zu verwendenden Zeitzone. Dieser Wert stellt den Sitzungsparameter `TIMEZONE` dar. Weitere Informationen zu Zeitzonen finden Sie in der [Vertica Analytics-Dokumentation zu Zeitzonen](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"}. |

>[!ENDTABS]

Nachdem Sie die Details der Verbindung hinzugefügt haben, beachten Sie die folgenden zusätzlichen Einstellungen:

>[!NOTE]
>
>Zum Verwenden der Komposition föderierter Zielgruppen für eine bestimmte Datenbank müssen Sie **alle** mit dieser Datenbank verknüpften IP-Adressen in die Zulassungsliste aufnehmen.

| Einstellungen | Details |
| -------- | ------- |
| Verbindung aktivieren | Ein boolescher Umschalter, der bestimmt, ob die Verbindung automatisch aktiviert wird. |
| Server-IPs | Ein Popup-Fenster, das anzeigt, welche IP-Adressen für die Verbindung mit der Datenbank auf die Zulassungsliste gesetzt werden müssen. |
| Testen der Verbindung | Ermöglicht die Überprüfung Ihrer Konfigurationsdetails. |

Sie können jetzt auf **[!UICONTROL Mit Quelle verbinden]** klicken, um die Schemadetails für die Datenbankverbindung einzurichten.

## Schemaauswahl {#schema-selection}

Die **[!UICONTROL Schemaauswahl]** wird angezeigt. Auf dieser Seite können Sie das Schema für Ihre Federated Database-Verbindung definieren.

![Die Schaltfläche „Tabelle hinzufügen“ ist im Bildschirm „Daten hinzufügen“ hervorgehoben.](/help/data-modelling/assets/integrated/select-add-table.png)

Weitere Informationen zum Einrichten von Schemadetails finden Sie im [Schemahandbuch](/help/data-modelling/schemas-integrated.md).

Nachdem Sie Ihre Schemata ausgewählt haben, wählen Sie **[!UICONTROL Weiter]**, um fortzufahren.

## Überprüfung {#review}

Die **[!UICONTROL &quot;]**&quot; wird angezeigt. Auf dieser Seite können Sie die Details Ihrer Federated Database Connection überprüfen. Wenn die Details korrekt aussehen, wählen Sie **[!UICONTROL Beenden]** aus, um die Verbindung zu erstellen.

![Die Überprüfungsseite wird angezeigt. Auf dieser Seite werden die Verbindungsdetails und Schemainformationen angezeigt.](/help/connections/assets/integrated/review.png)

Die Verbindung wird erstellt. Es wird ein Popup angezeigt, in dem Sie aufgefordert werden, entweder **[!UICONTROL Schema anzeigen]** oder **[!UICONTROL Beziehungen erstellen]**. Wenn Sie **[!UICONTROL Schema anzeigen]** auswählen, wird die Seite [Schema durchsuchen](/help/data-modelling/schemas-integrated.md#edit-a-schema) angezeigt. Wenn Sie **[!UICONTROL Beziehungen erstellen]** auswählen, wird die Seite [Entitätsdiagramm](/help/data-modelling/schemas-integrated.md#edit-relationships) angezeigt.

## Verbindung bearbeiten {#edit-connection}

Wenn Sie die Anmeldedetails für die Quellverbindung bearbeiten müssen, wählen Sie **[!UICONTROL Quellen]** gefolgt von **[!UICONTROL Konten]** aus.

![Die Schaltfläche Konten ist hervorgehoben und zeigt die Seite zum Durchsuchen der Quellkonten an.](/help/connections/assets/integrated/select-accounts.png)

Die Seite zum Durchsuchen der Quell-Connectoren wird angezeigt. Suchen Sie den Quell-Connector, den Sie aktualisieren möchten, und wählen Sie ![die drei Punkte](/help/assets/icons/more.png) gefolgt von **[!UICONTROL Details bearbeiten]** aus.

![Die Schaltfläche „Details bearbeiten“ ist hervorgehoben.](/help/connections/assets/integrated/select-edit-details.png)

Das **[!UICONTROL Kontodetails bearbeiten]** wird angezeigt. In diesem Popover können Sie die Details der Federated Database Source-Verbindung aktualisieren.

![Das Pop-up Kontodetails bearbeiten wird angezeigt.](/help/connections/assets/integrated/edit-account-details.png)

## Anhang {#appendix}

Im folgenden Anhang wird beschrieben, wie Sie die Verbindungen aufseiten des externen Kontos einrichten.

### Konfiguration von Google BigQuery (Workload Identity Federation) {#wif-configuration}

Bevor Sie die Google Cloud Platform-Einrichtung konfigurieren, benötigen Sie die folgenden Werte:

- AWS-Konto-ID
  - Wenden Sie sich an die Adobe-Kundenunterstützung, um diesen Wert zu erhalten.
- AWS IAM-Rollenname
  - Der Name der AWS IAM-Rolle folgt dem folgenden Format: `arn:aws:iam::<ADOBE_AWS_ACCOUNT_ID>:role/fac-<CUSTOMER_IMS_ORG_ID>`

Erstellen Sie in der Google Cloud Console einen **Workload Identity-Pool** im **Abschnitt für IAM und Administration**. Auf diese Weise können Sie externe Identitäten organisieren und verwalten.

Wählen Sie **Anbieter hinzufügen** aus, um einen Identitätsanbieter zu erstellen. Hierdurch wird ein einseitiges Vertrauensverhältnis zwischen dem Identitätsanbieter in Google Cloud und dem Workload Identity-Pool konfiguriert, indem die relevanten Metadaten über den Anbieter bereitgestellt werden.

![Die Schaltfläche „Anbieter hinzufügen“ ist in Google Cloud hervorgehoben.](/help/connections/assets/home/select-add-provider.png)

Wenn Sie einen Anbieter erstellen, müssen Sie die folgenden Informationen angeben:

| Feld | Beschreibung |
| ----- | ----------- |
| Name | Der Name des Anbieters für den Workload Identity-Pool. |
| ID | Die ID für den Anbieter wird automatisch generiert. |
| AWS-Konto-ID | Die zuvor angegebene AWS-Konto-ID. |
| Aktivierter Anbieter | Ein boolescher Wert, der bestimmt, ob der Anbieter aktiviert oder deaktiviert ist. |
| Attributzuordnung | Die Zuordnungen, die mit den Rollen übereinstimmen müssen. Diese Informationen sind bereits vorhanden. |

Nachdem Sie den Anbieter erstellt haben, müssen Sie eine IAM-Richtlinie erstellen, damit die Identitäten des Workload Identity-Pools die Identität des Dienstkontos annehmen können. Wählen Sie **Zugriff gewähren** aus, um das Dialogfeld „Zugriff auf Dienstkonto gewähren“ zu öffnen.

Wählen Sie im Dialogfeld die Option für **Zugriff über Dienstkontosimulation gewähren** aus. Im Abschnitt **Prinzipale auswählen** müssen Sie Ihre Attributzuordnungen erstellen.

Wählen Sie **aws_role** aus und fügen Sie `arn:aws:sts::AWSAccountID:assumed-role/AWSRoleName` als Wert hinzu, wobei Sie `AWSAccountID` und `AWSRoleName` durch die zuvor bereitgestellten Werte ersetzen.

![Das Dialogfeld „Zugriff gewähren“ wird angezeigt.](/help/connections/assets/home/aws-role.png)

Laden Sie nach der Gewährung des Zugriffs auf das Dienstkonto die Konfiguration der Client-Bibliothek herunter.

![Der Speicherort für das Herunterladen der Bibliothekskonfiguration wird angezeigt.](/help/connections/assets/home/download-config.png)

Nach dem Herunterladen der Konfiguration der Client-Bibliothek können Sie nun eine WIF-Verbindung mit der Konfiguration föderierter Zielgruppen einrichten.

### Unterstützung für das Google BigQuery [!DNL Apigee]-Gateway {#apigee}

Sie können [!DNL Apigee] verwenden, die native API-Verwaltungsplattform von Google Cloud, um API-Aufrufe an Google BigQuery weiterzuleiten.

Zunächst müssen Sie einen Proxy in der [!DNL Apigee]-Benutzeroberfläche erstellen. Navigieren Sie in Google Cloud zu **Apigee** und wählen Sie **Proxy-Entwicklung**, **API-Proxys** und **Erstellen** aus, um das Panel **Proxy erstellen** aufzurufen. Im Panel können Sie die folgenden Details eingeben:

![Der Bildschirm für die Erstellung des Apigee-Proxys wird angezeigt.](/help/connections/assets/home/create-proxy-apigee.png)

| Details | Beschreibung |
| ------- | ----------- |
| Proxy-Vorlage | Der Typ des Proxys, den Sie erstellen möchten. In diesem Anwendungsfall sollten Sie **Reverse Proxy (Am häufigsten)** auswählen. |
| Proxy-Name | Der Name Ihres Proxys. Dieser Wert darf **nur** alphanumerische Zeichen, Bindestriche (`-`) oder Unterstriche (`_`) enthalten. |
| Basispfad | Das URI-Fragment, das die Host-Adresse für Ihren API-Proxy anzeigt. Dieser Basispfad basiert auf dem Proxy-Namen und **muss** eindeutig sein. |
| Beschreibung | Eine optionale Beschreibung für den API-Proxy. |
| Ziel | Die URL (die entweder HTTP oder HTTPS enthält) des Backend-Dienstes, den der API-Proxy aufruft. |

Erstellen Sie zur Komposition föderierter Zielgruppen eine Proxy-Endpunktregel für **jeden** Endpunkt, den der Google BigQuery-Connector verwendet, wie unten aufgeführt:

| Basispfad | Ziel-Endpunkt | Beschreibung |
| --------- | --------------- | ----------- |
| `/bigquery` | `https://bigquery.googleapis.com/bigquery` | Der Hauptendpunkt für Google BigQuery. Dieser Endpunkt wird verwendet, um Daten wie Abfragen und Tabellenlisten abzurufen. |
| `/token` | `https://oauth2.googleapis.com/token` | Dieser Endpunkt wird für die Authentifizierung von Dienstkonten verwendet. |
| `/storage` | `https://storage.googleapis.com/storage` | Dieser Speicherendpunkt dient zum Löschen temporärer Massenladedateien. |
| `/upload` | `https://storage.googleapis.com/upload` | Dieser Speicherendpunkt wird zum Massenladen von Dateien verwendet. |
| `/v1/token` | `https://sts.googleapis.com/v1/token` | Dieser Endpunkt wird für den Fluss „Workload Identity Federation“ (WIF) zum Abrufen des Tokens verwendet. |
| `/v1/projects` | `https://iamcredentials.googleapis.com/v1/projects` | Dieser Endpunkt wird verwendet, um die Identität als Dienstkonto im Fluss „Workload Identity Federation“ (WIF) anzunehmen. |

Sobald Sie Ihren Proxy erstellt haben, können Sie ihn für die Verbindung mit der Komposition föderierter Zielgruppen verwenden. Nachdem Sie den Proxy bereitgestellt haben, finden Sie die vollständige URL für Ihren Proxy unter **Host-Namen**, wenn Sie im Abschnitt **Admin** erst **Umgebungen** und dann **Gruppen** auswählen.
