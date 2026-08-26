---
title: Herstellen einer Verbindung zur Federated Audience-Komposition über eine private Verbindung
description: Erfahren Sie, wie Sie die Federated Audience-Komposition über eine private Verbindung einrichten und eine Verbindung herstellen. Dazu gehören PrivateLink oder ein Site-zu-Site-VPN.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# Private Konnektivität zur Federated Audience-Komposition

Die Federated Audience-Komposition unterstützt private Verbindungen mit mehreren Datenbanken. Mit privaten Verbindungen können Sie eine Verbindung zu kundengehosteten Data Warehouses herstellen, ohne das öffentliche Internet zu durchlaufen.

## Unterstützte Datenbanken {#supported-databases}

Die folgenden Datenbanken unterstützen die private Konnektivität zur Federated Audience-Komposition:

| Datenbank | Cloud | Privater Verbindungstyp |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (Endpunkt der VPC-Schnittstelle) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (privater Endpunkt) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (Endpunkt von Managed VPC) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (Endpunkt der VPC-Schnittstelle) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | Site-zu-Site-VPN |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | Site-zu-Site-VPN |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | Site-zu-Site-VPN |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | Site-zu-Site-VPN |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Um private Konnektivität mit [!DNL Snowflake] verwenden zu können, **müssen** Sie sich mindestens auf der geschäftskritischen Ebene oder höher auf der [!DNL Snowflake] befinden. Weitere Informationen zur privaten Konnektivität mit [!DNL Snowflake] finden Sie im [Handbuch zur privaten Konnektivität in der Snowflake-Dokumentation](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound).

Die Verwendung der privaten Konnektivität mit [!DNL Snowflake] hängt davon ab, bei welchem Cloud-Anbieter sich Ihre [!DNL Snowflake]-Instanz befindet.

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Bevor Sie fortfahren, stellen Sie sicher, dass Sie Ihre AWS-Konto-ID von der Adobe-Kundenunterstützung erhalten. Sobald Sie Ihre AWS-Konto-ID erhalten haben, wenden Sie sich an [!DNL Snowflake] Support, damit [!DNL Snowflake] Ihr AWS-Konto zur Verwendung von PrivateLink autorisieren können.

Nachdem Ihr AWS-Konto für die Verwendung mit [!DNL Snowflake] autorisiert wurde, müssen Sie Werte einschließlich `privatelink-vpce-id`, `privatelink-account-url` und `privatelink_ocsp-url` abrufen, damit Sie den Endpunkt der VPC-Benutzeroberfläche erhalten.

Sie können diese Werte abrufen, indem Sie die folgenden Befehle in Ihrem [!DNL Snowflake]-Konto als ACCOUNTADMIN ausführen:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Nachdem Sie diese Befehle ausgeführt haben, können Sie die vollständige SQL-Ausgabe an die Adobe-Kundenunterstützung senden, damit Adobe den Endpunkt der VPC-Benutzeroberfläche für Sie erstellen kann.

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit AWS finden Sie im [Handbuch zu AWS PrivateLink](https://docs.snowflake.com/en/user-guide/admin-security-privatelink).

Wenn Sie den PrivateLink für die Verwendung mit einer internen Staging-Umgebung autorisieren möchten, wenden Sie sich an die Adobe-Kundenunterstützung, um die Umgebung zu aktivieren.

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit AWS für interne Staging-Umgebungen finden Sie im Handbuch [Endpunkte der AWS VPC-Benutzeroberfläche für interne Phasen](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Für Microsoft Azure müssen Sie Werte einschließlich `privatelink-pls-id`, `privatelink-account-url` und `privatelink_ocsp-url` abrufen, um den privaten Azure-Endpunkt zu erstellen.

Sie können diese Werte abrufen, indem Sie die folgenden Befehle in Ihrem Snowflake-Konto ausführen:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Nachdem Sie diese Befehle ausgeführt haben, können Sie die vollständige SQL-Ausgabe an die Adobe-Kundenunterstützung senden, damit Adobe den privaten Azure-Endpunkt für Sie erstellen kann.

Sobald Adobe den privaten Azure-Endpunkt erstellt hat, können Sie Ihre private Endpunkt-Ressourcen-ID abrufen. Nachdem Sie nun über die Ressourcen-ID des privaten Endpunkts verfügen, wenden Sie sich an den [!DNL Snowflake]-Support, um Ihr [!DNL Snowflake]-Konto zu autorisieren, und geben Sie die Ressourcen-ID an.

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit Azure finden Sie im [Handbuch zu Azure PrivateLink](https://docs.snowflake.com/en/user-guide/privatelink-azure).

Wenn Sie PrivateLink für die Verwendung mit einer internen Staging-Umgebung autorisieren möchten, führen Sie den folgenden Befehl in [!DNL Snowflake] aus, wobei Sie die interne Staging-Ressourcen-ID angeben, die von der Adobe-Kundenunterstützung bereitgestellt wird:

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit Azure für interne Staging-Umgebungen finden Sie im Handbuch [Private Endpunkte von Azure für interne Phasen](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Sowohl provisionierte Cluster als auch Redshift ServerLess unterstützen private Verbindungen mit Federated Audience Composition.

>[!IMPORTANT]
>
>Wenden Sie sich vor dem Start an die Adobe-Kundenunterstützung, um Ihre Amazon Web Services (AWS)-Konto-ID und Ihre Virtual Private Cloud (VPC)-ID zu erhalten. Sie benötigen **beide** Werte, um kontenübergreifenden Endpunktzugriff zu erhalten. Ausführlichere Informationen zum Gewähren des Zugriffs auf die VPC finden Sie im [Gewähren des Zugriffs auf eine VPC](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Sobald Sie sowohl die AWS- als auch die VPC-IDs haben, wechseln Sie zur AWS-Verwaltungskonsole , um kontenübergreifenden Zugriff für einen verwalteten VPC-Endpunkt zu gewähren.

Beachten Sie für einen bereitgestellten Cluster sowohl die Werte **Redshift Cluster Identifier** als auch die **Cluster Owner AWS Account ID**. Bei einem Server-losen Redshift-System sollten Sie sowohl die Werte **Arbeitsgruppenname** als auch die **Eigentümer-AWS-Konto-ID** beachten.

Nachdem Sie diese Werte erhalten haben, geben Sie diese Details an die Adobe-Kundenunterstützung weiter, damit Adobe den verwalteten VPC-Endpunkt erstellen kann. Adobe gibt dann die folgenden Verbindungsdetails für Sie frei: **Redshift-Endpunkt**, **Redshift JDBC-** und **Redshift ODBC-URL**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Um private Konnektivität mit Databricks nutzen zu können, **müssen** Sie einen Enterprise-Plan für Databricks haben. Weitere Informationen zur privaten Konnektivität mit Databricks finden Sie im [Handbuch zu privaten Link-Konzepten](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts).

Die Verwendung der privaten Konnektivität mit Databricks hängt davon ab, auf welchem Cloud-Anbieter sich Ihre Databricks-Instanz befindet.

### Amazon Web Services {#databricks-aws}

Wenden Sie sich vor der Konfiguration von mit Amazon Web Services an die Kundenunterstützung von Adobe, damit diese einen Frontend-Endpunkt (eingehende) VPC-Schnittstelle erstellen kann, der auf Databricks verweist. Dieser Endpunkt behandelt die ODBC-Konnektivität der Federated Audience Composition zu Ihrem Databricks-Arbeitsbereich.

Nachdem Sie Ihre VPC-Endpunkt-ID und die AWS-Region von der Adobe-Kundenunterstützung erhalten haben, müssen Sie Ihren VPC-Endpunkt mit den von Adobe bereitgestellten Informationen registrieren.

Nachdem Sie Ihren VPC-Endpunkt registriert haben, müssen Sie ein PAS-Objekt (Private Access Settings) erstellen. Wenn Sie den Endpunkt erstellen, setzen Sie die **private Zugriffsebene** auf eine **Endpunkt**-Ebene und wählen Sie den zuvor erstellten VPC-Endpunkt aus. Weitere Informationen zum Erstellen von Einstellungen für den privaten Zugriff finden Sie im [Handbuch zu eingehenden privaten Links konfigurieren](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Nachdem Sie Ihre privaten Zugriffseinstellungen konfiguriert haben, können Sie den VPC-Endpunkt an Ihren Arbeitsbereich anhängen. Weiterführende Informationen zur Erstellung Ihres Arbeitsbereichs mit PrivateLink finden Sie im [Handbuch zu eingehenden privaten Links konfigurieren](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Nachdem alle Einstellungen konfiguriert wurden, können Sie Ihre Databricks Workspace-URL für die Adobe-Kundenunterstützung freigeben. Nachdem Sie Ihre Databricks Workspace-URL freigegeben haben, kann Adobe die DNS-Einstellungen konfigurieren, die erforderlich sind, um Anfragen an den Workspace-Endpunkt weiterzuleiten.

### Microsoft Azure {#databricks-azure}

Ein Site-zu-Site-VPN wird verwendet, um eine sichere Verbindung von Adobe mit dem Databricks-Arbeitsbereich in Azure herzustellen. Sie müssen ein Azure VPN-Gateway einrichten, um den VPN-Tunnel einzurichten und Ihre Daten sicher an Adobe zu übertragen.

Nachdem Sie Ihr Azure VPN-Gateway und Ihren privaten Databricks-Endpunkt eingerichtet haben, geben Sie die folgenden Details an Ihren Adobe-Kundenbetreuer weiter: **Azure Virtual Network Gateway**, **Databricks Private Endpoint IP**, **Databricks Workspace URL** und **Autonomous System Number (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **öffentlichen und privaten IP-Adressen des VPN**, **vorab freigegebenen Schlüssel** sowie eine **autonome Systemnummer** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Azure VNet-Gateway konfigurieren. Weitere Informationen finden Sie im Handbuch [Verbinden von AWS und Azure über ein VPN-Gateway](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Google Cloud Platform {#databricks-gcp}

Ein Site-zu-Site-VPN wird verwendet, um eine sichere Verbindung zwischen Adobe und dem Datenbricks-Arbeitsbereich in Google Cloud Platform herzustellen. Sie müssen ein Google Cloud Platform High Availability VPN-Gateway und einen Cloud-Router einrichten, um den VPN-Tunnel einzurichten und Ihre Daten sicher an Adobe zu übertragen.

Sobald Sie Ihr GCP HA VPN-Gateway und Ihren Cloud-Router eingerichtet haben, geben Sie die folgenden Informationen an Ihren Adobe-Kundenbetreuer weiter: **GCP HA VPN-Gateway**, **Databricks Workspace URL**, **Private Service Connect (PSC) IP** und **Autonomous System Number (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **öffentlichen und privaten IP-Adressen des VPN**, **vorab freigegebenen Schlüssel** sowie eine **autonome Systemnummer** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Google Cloud Platform-Konto konfigurieren. Weitere Informationen finden Sie im [Handbuch zum Erstellen von HA-VPN-Verbindungen](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).

## Azure Synapse Analytics {#azure-synapse}

Um eine Verbindung mit Azure Synapse Analytics herzustellen, müssen Sie zunächst ein virtuelles Azure-Netzwerkgateway und einen privaten Synapse-Endpunkt erstellen. Mit dem Azure Virtual Network Gateway können Sie verschlüsselten Datenverkehr zwischen einem virtuellen Azure-Netzwerk an Synapse senden, während Sie mit dem privaten Synapse-Endpunkt über eine private Verbindung verfügen, um Ihre Daten sicher zu übertragen.

Sobald Sie Ihr virtuelles Azure-Netzwerkgateway und Ihren privaten Synapse-Endpunkt eingerichtet haben, geben Sie die folgenden Details an Ihren Adobe-Kundenbetreuer weiter: **Azure Virtual Network Gateway**, **Synapse Private Endpoint IP**, **Synapse Workspace URL** und **Autonomous Service Number (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **VPN-Tunnel-Paarungen**, **vorab freigegebene Schlüssel** sowie eine **autonome Systemnummer** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Azure VNet-Gateway konfigurieren. Weitere Informationen finden Sie im Handbuch [Verbinden von AWS und Azure über ein VPN-Gateway](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google BigQuery {#gbq}

Um eine Verbindung mit Google Big Query herzustellen, müssen Sie zunächst ein Google Cloud Platform High Availability VPN-Gateway und einen Cloud-Router erstellen.

Sobald Sie Ihr GCP HA VPN-Gateway und Ihren Cloud-Router eingerichtet haben, teilen Sie die folgenden Details mit Ihrem Adobe-Kundenbetreuer: **GCP HA VPN-Gateway**, **Private Service Connect (PSC)** und die **Autonome Systemnummer (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **öffentlichen und privaten IP-Adressen des VPN**, **vorab freigegebenen Schlüssel** sowie eine **autonome Systemnummer** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Google Cloud Platform-Konto konfigurieren. Weitere Informationen finden Sie im [Handbuch zum Erstellen von HA-VPN-Verbindungen](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).
