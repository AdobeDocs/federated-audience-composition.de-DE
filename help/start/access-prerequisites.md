---
title: Voraussetzungen und Leitlinien für die Komposition föderierter Zielgruppen
description: Erfahren Sie mehr über die Voraussetzungen, Berechtigungen und Leitlinien für die Komposition föderierter Zielgruppen
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: ht
source-wordcount: '305'
ht-degree: 100%

---

# Voraussetzungen und Leitlinien {#fac-access}

Die Komposition föderierter Zielgruppen erfordert Adobe Real-Time Customer Data Platform und/oder die Pakete **Prime** oder **Ultimate** von Adobe Journey Optimizer. Um auf diese Funktion zugreifen zu können, müssen Sie das Add-on „Komposition föderierter Zielgruppen“ gekauft haben.

>[!AVAILABILITY]
>
>Nachdem Sie die Begrüßungs-E-Mail von Adobe erhalten haben, kann es noch einige Stunden dauern, bis die Benutzeroberfläche aktualisiert ist und Ihnen die Funktionen zur Verfügung stehen.

## Unterstützte Systeme {#supported-systems}

Die Komposition föderierter Zielgruppen unterstützt die folgenden Cloud-Warehouses:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google BigQuery
* Snowflake
* Vertica Analytics

Auf [dieser Seite](../connections/connections.md) erfahren Sie, wie Sie eine Verbindung mit diesen Systemen herstellen.

## Berechtigungen {#permissions}

Wenn Sie das Add-on „Komposition föderierter Zielgruppen“ erwerben, wird zu diesem Zeitpunkt für jede aktive Sandbox ein Produktprofil erstellt. Dieses Produktprofil wird in der Admin Console unter der Produktkarte **Adobe Experience Platform** erstellt und folgt dieser Namenskonvention: `ACP_FAC - <<SandboxName>> - admin.` Für den Zugriff auf die Komposition föderierter Zielgruppen für eine bestimmte Sandbox müssen Benutzende zum Produktprofil hinzugefügt werden, das für diese Sandbox erstellt wurde.

Wirds beispielsweise eine neue Sandbox mit dem Namen „fac-test“ aktiviert, wird das entsprechende Produktprofil „ACP_FAC – fac-test – admin“ erstellt. Um mit dieser Sandbox auf die Komposition föderierter Zielgruppen zugreifen zu können, müssen Benutzende diesem Produktprofil hinzugefügt werden.

## IP-Zulassungsauflistung {#ip}

Damit die Komposition föderierter Zielgruppen sicher auf Ihre Datenbanken zugreifen kann, wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um die IP-Adressen des Servers der Komposition föderierter Zielgruppen zu erhalten, der darauf zugreifen wird.

Fügen Sie diese IP-Adressen zu Ihrer Zulassungsliste hinzu, um der Komposition föderierter Zielgruppen Zugriff zu gewähren.

## Leitlinien und Einschränkungen {#fac-guardrails}

* Die Komposition föderierter Zielgruppen ist derzeit nicht für Kundinnen und Kunden verfügbar, die [Gesundheitsdaten aufnehmen](https://experienceleague.adobe.com/de/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}, sowie für Kundinnen und Kunden von Adobe Journey Optimizer und Privacy and Security Shield. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Für dieses Add-on gelten die Berechtigungen, Produktbeschränkungen und Leistungsleitlinien, die in der [Dokumentation zu Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/de/docs/experience-platform/profile/guardrails) {target="_blank"} aufgeführt sind.
