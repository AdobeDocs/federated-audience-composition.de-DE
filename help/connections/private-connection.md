---
title: Herstellen einer Verbindung zu einer Komposition föderierter Zielgruppen über eine private Verbindung
description: Erfahren Sie, wie Sie eine Komposition föderierter Zielgruppen über eine private Verbindung einrichten und eine Verbindung herstellen. Das betrifft auch PrivateLink oder ein Site-zu-Site-VPN.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: ht
source-wordcount: '1634'
ht-degree: 100%

---


# Private Verbindung zu einer Komposition föderierter Zielgruppen

Kompositionen föderierter Zielgruppen unterstützen private Verbindungen mit mehreren Datenbanken. Mit privaten Verbindungen können Sie eine Verbindung zu auf Kundenseite gehosteten Data Warehouses herstellen, ohne das öffentliche Internet zu durchlaufen.

## Unterstützte Datenbanken {#supported-databases}

Die folgenden Datenbanken unterstützen private Verbindungen zur Komposition föderierter Zielgruppen:

| Datenbank | Cloud | Typ der privaten Verbindung |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (VPC-Schnittstellenendpunkt) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (privater Endpunkt) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (verwalteter VPC-Endpunkt) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (VPC-Schnittstellenendpunkt) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | Site-zu-Site-VPN |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | Site-zu-Site-VPN |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | Site-zu-Site-VPN |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | Site-zu-Site-VPN |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Um eine private Verbindung mit [!DNL Snowflake] verwenden zu können, **müssen** Sie sich mindestens auf der Stufe „geschäftskritisch“ oder höher auf [!DNL Snowflake] befinden. Weitere Informationen zur privaten Verbindung mit [!DNL Snowflake] finden Sie im [Handbuch zu privaten Verbindungen in der Snowflake-Dokumentation](https://docs.snowflake.com/de/user-guide/private-connectivity-inbound).

Die Verwendung einer privaten Verbindung mit [!DNL Snowflake] hängt davon ab, mit welchem Cloud-Anbieter Sie Ihre [!DNL Snowflake]-Instanz verwenden.

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Bevor Sie fortfahren, müssen Sie Ihre AWS-Konto-ID von der Adobe-Kundenunterstützung erhalten. Sobald Sie Ihre AWS-Konto-ID erhalten haben, wenden Sie sich an den [!DNL Snowflake]-Support, damit [!DNL Snowflake] Ihr AWS-Konto zur Verwendung von PrivateLink autorisieren kann.

Nachdem Ihr AWS-Konto für die Verwendung mit [!DNL Snowflake] autorisiert wurde, müssen Sie zum Erhalten des VPC-Schnittstellenendpunkts Werte wie `privatelink-vpce-id`, `privatelink-account-url` und `privatelink_ocsp-url` abrufen.

Sie können diese Werte abrufen, indem Sie die folgenden Befehle in Ihrem [!DNL Snowflake]-Konto als ACCOUNTADMIN ausführen:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Nachdem Sie diese Befehle ausgeführt haben, können Sie die vollständige SQL-Ausgabe an die Adobe-Kundenunterstützung senden, damit Adobe den VPC-Schnittstellenendpunkt für Sie erstellen kann.

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit AWS finden Sie im [Handbuch zu AWS PrivateLink](https://docs.snowflake.com/de/user-guide/admin-security-privatelink).

Wenn Sie PrivateLink für die Verwendung mit einer internen Staging-Umgebung autorisieren möchten, wenden Sie sich zum Aktivieren der Umgebung an die Adobe-Kundenunterstützung.

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit AWS für interne Staging-Umgebungen finden Sie im Handbuch [AWS-VPC-Schnittstellenendpunkte für interne Staging-Umgebungen](https://docs.snowflake.com/de/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Für Microsoft Azure müssen Sie Werte einschließlich `privatelink-pls-id`, `privatelink-account-url` und `privatelink_ocsp-url` abrufen, um den privaten Azure-Endpunkt zu erstellen.

Sie können diese Werte abrufen, indem Sie die folgenden Befehle in Ihrem Snowflake-Konto ausführen:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Nachdem Sie diese Befehle ausgeführt haben, können Sie die vollständige SQL-Ausgabe an die Adobe-Kundenunterstützung senden, damit Adobe den privaten Azure-Endpunkt für Sie erstellen kann.

Sobald Adobe den privaten Azure-Endpunkt erstellt hat, können Sie die Ressourcen-ID für Ihren privaten Endpunkt abrufen. Nun da Sie über die Ressourcen-ID des privaten Endpunkts verfügen, wenden Sie sich zum Autorisieren Ihres [!DNL Snowflake]-Kontos an den [!DNL Snowflake]-Support und geben Sie die Ressourcen-ID an.

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit Azure finden Sie im [Handbuch zu Azure PrivateLink](https://docs.snowflake.com/de/user-guide/privatelink-azure).

Wenn Sie PrivateLink für die Verwendung mit einer internen Staging-Umgebung autorisieren möchten, führen Sie den folgenden Befehl in [!DNL Snowflake] aus, wobei Sie die interne Staging-Ressourcen-ID angeben, die von der Adobe-Kundenunterstützung bereitgestellt wird:

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Detailliertere Informationen zum Erstellen einer PrivateLink-Verbindung mit Azure für interne Staging-Umgebungen finden Sie im Handbuch [Private Azure-Endpunkte für interne Staging-Umgebungen](https://docs.snowflake.com/de/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Sowohl bereitgestellte Cluster als auch Redshift Serverless unterstützen private Verbindungen mit Kompositionen föderierter Zielgruppen.

>[!IMPORTANT]
>
>Bevor Sie beginnen, wenden Sie sich an die Adobe-Kundenunterstützung, um Ihre Konto-ID für Amazon Web Services (AWS) und Ihre ID für Virtual Private Cloud (VPC) zu erhalten. Sie benötigen **beide** Werte, um kontenübergreifenden Zugriff auf Endpunkte zu erhalten. Ausführlichere Informationen zum Gewähren des Zugriffs auf die VPC finden Sie im [Handbuch zum Gewähren des Zugriffs auf VPC](https://docs.aws.amazon.com/de_de/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Sobald Sie sowohl die AWS- als auch die VPC-ID erhalten haben, wechseln Sie zur AWS Management Console, um kontenübergreifenden Zugriff auf einen verwalteten VPC-Endpunkt zu gewähren.

Beachten Sie bei einem bereitgestellten Cluster sowohl die Werte für **Redshift-Cluster-Kennung** als auch für **Cluster-Inhaber-AWS-Konto-ID**. Bei Redshift Serverless sollten Sie sowohl die Werte für **Arbeitsgruppenname** als auch für **Inhaber-AWS-Konto-ID** beachten.

Nachdem Sie diese Werte erhalten haben, geben Sie diese Details an die Adobe-Kundenunterstützung weiter, damit Adobe den verwalteten VPC-Endpunkt erstellen kann. Adobe gibt dann die folgenden Verbindungsdetails für Sie frei: **Redshift-Endpunkt-URL**, **Redshift-JDBC-URL** und **Redshift-ODBC-URL**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Um eine private Verbindung mit Databricks nutzen zu können, **müssen** Sie über einen Unternehmensplan für Databricks verfügen. Weitere Informationen zur privaten Verbindung mit Databricks finden Sie im [Handbuch zu Konzepten privater Verbindungen](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts).

Die Verwendung einer privaten Verbindung mit Databricks hängt davon ab, mit welchem Cloud-Anbieter Sie Ihre Databricks-Instanz verwenden.

### Amazon Web Services {#databricks-aws}

Wenden Sie sich vor der Konfiguration mit Amazon Web Services an die Kundenunterstützung von Adobe, damit diese einen (eingehenden) Frontend-VPC-Schnittstellenendpunkt erstellen kann, der auf Databricks verweist. Dieser Endpunkt stellt die ODBC-Verbindung der Komposition föderierter Zielgruppen mit Ihrem Databricks-Arbeitsbereich zur Verfügung.

Nachdem Sie Ihre VPC-Endpunkt-ID und die AWS-Region von der Adobe-Kundenunterstützung erhalten haben, müssen Sie Ihren VPC-Endpunkt mit den von Adobe bereitgestellten Informationen registrieren.

Nachdem Sie Ihren VPC-Endpunkt registriert haben, müssen Sie ein PAS-Objekt (Private Access Settings) erstellen. Legen Sie beim Erstellen des Endpunkts die **Ebene für privaten Zugriff** auf eine **Endpunktebene** fest und wählen Sie den zuvor erstellten VPC-Endpunkt aus. Weitere Informationen zum Erstellen von Einstellungen für den privaten Zugriff finden Sie im [Handbuch zum Konfigurieren von eingehendem PrivateLink](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Nachdem Sie Ihre Einstellungen für den privaten Zugriff konfiguriert haben, können Sie den VPC-Endpunkt an Ihren Arbeitsbereich anhängen. Weitere Informationen zum Erstellen Ihres Arbeitsbereichs mit PrivateLink finden Sie im [Handbuch zum Konfigurieren von eingehendem PrivateLink](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Nachdem alle Einstellungen konfiguriert wurden, können Sie der Adobe-Kundenunterstützung Ihre Databricks-Arbeitsbereich-URL mitteilen. Nachdem Sie Ihre Databricks-Arbeitsbereich-URL weitergegeben haben, kann Adobe die zur Weiterleitung von Anfragen an den Arbeitsbereichsendpunkt erforderlichen DNS-Einstellungen konfigurieren.

### Microsoft Azure {#databricks-azure}

Ein Site-zu-Site-VPN wird verwendet, um eine sichere Verbindung von Adobe mit dem Databricks-Arbeitsbereich in Azure herzustellen. Sie müssen ein Azure-VPN-Gateway einrichten, um den VPN-Tunnel herzustellen und Ihre Daten sicher an Adobe zu übertragen.

Nachdem Sie Ihr Azure-VPN-Gateway und Ihren privaten Databricks-Endpunkt eingerichtet haben, geben Sie die folgenden Details an die Adobe-Kundenunterstützung weiter: **Gateway für virtuelles Azure-Netzwerk**, **ID des privaten Databrick-Endpunkts**, **Databricks-Arbeitsbereich-URL** und **Nummer des autonomen Systems (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **öffentlichen und privaten IP-Adressen des VPN-Tunnels**, **vorab freigegebene Schlüssel** sowie eine **Nummer eines autonomen Systems** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Azure-VNet-Gateway konfigurieren. Weitere Informationen finden Sie im Handbuch [Verbinden von AWS und Azure über ein VPN-Gateway](https://learn.microsoft.com/de-de/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Google Cloud Platform {#databricks-gcp}

Ein Site-zu-Site-VPN wird verwendet, um eine sichere Verbindung zwischen Adobe und dem Databricks-Arbeitsbereich in Google Cloud Platform herzustellen. Sie müssen ein Google Cloud Platform-High-Availability-VPN-Gateway und einen Cloud-Router einrichten, um den VPN-Tunnel zu erstellen und Ihre Daten sicher an Adobe zu übertragen.

Sobald Sie Ihr GCP-HA-VPN-Gateway und Ihren Cloud-Router eingerichtet haben, geben Sie die folgenden Informationen an die Adobe-Kundenunterstützung weiter: **GCP-HA-VPN-Gateway**, **Databricks-Arbeitsbereich-URL**, **IP von Private Service Connect (PSC)** und **Nummer des autonomen Systems (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **öffentlichen und privaten IP-Adressen des VPN-Tunnels**, **vorab freigegebene Schlüssel** sowie eine **Nummer eines autonomen Systems** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Google Cloud Platform-Konto konfigurieren. Weitere Informationen finden Sie im [Handbuch zum Herstellen von HA-VPN-Verbindungen](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws?hl=de).

## Azure Synapse Analytics {#azure-synapse}

Um eine Verbindung mit Azure Synapse Analytics herzustellen, müssen Sie zunächst ein Gateway für ein virtuelles Azure-Netzwerk und einen privaten Synapse-Endpunkt erstellen. Mit dem Gateway für das virtuelle Azure-Netzwerk können Sie verschlüsselten Traffic zwischen einem virtuellen Azure-Netzwerk und Synapse senden. Dabei ermöglicht der private Synapse-Endpunkt eine private Verbindung für die sichere Übertragung Ihrer Daten.

Sobald Sie Ihr Gateway für das virtuelle Azure-Netzwerk und Ihren privaten Synapse-Endpunkt eingerichtet haben, geben Sie die folgenden Details an die Adobe-Kundenunterstützung weiter: **Gateway für virtuelles Azure-Netzwerk**, **IP des privaten Synapse-Endpunkts**, **Synapse-Arbeitsbereich-URL** und **Nummer des autonomen Systems (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **VPN-Tunnel-Paarungen**, **vorab freigegebene Schlüssel** sowie eine **Nummer eines autonomen Systems** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Azure-VNet-Gateway konfigurieren. Weitere Informationen finden Sie im Handbuch [Verbinden von AWS und Azure über ein VPN-Gateway](https://learn.microsoft.com/de-de/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google BigQuery {#gbq}

Um eine Verbindung mit Google Big Query herzustellen, müssen Sie zunächst ein Google Cloud Platform-High-Availability-VPN-Gateway und einen Cloud-Router erstellen.

Sobald Sie Ihr GCP-HA-VPN-Gateway und Ihren Cloud-Router eingerichtet haben, geben Sie die folgenden Details an die Adobe-Kundenunterstützung weiter: **GCP-HA-VPN-Gateway**, **IP von Private Service Connect (PSC)**, und die **Nummer des autonomen Systems (ASN)**.

Mit diesen Details kann Adobe die für Ihre Verbindung erforderlichen VPN-Tunnel einrichten. Nach der Einrichtung der VPN-Tunnel stellt Adobe die **öffentlichen und privaten IP-Adressen des VPN-Tunnels**, **vorab freigegebene Schlüssel** sowie eine **Nummer eines autonomen Systems** bereit.

Sie können jetzt Ihre VPN-Tunnel in Ihrem Google Cloud Platform-Konto konfigurieren. Weitere Informationen finden Sie im [Handbuch zum Herstellen von HA-VPN-Verbindungen](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws?hl=de).
