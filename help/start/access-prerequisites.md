---
title: Voraussetzungen und Leitlinien für die Komposition föderierter Zielgruppen
description: Erfahren Sie mehr über die Voraussetzungen, Berechtigungen und Leitlinien für die Komposition föderierter Zielgruppen
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 86%

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
* Microsoft Fabric

Auf dieser Seite erfahren Sie, wie Sie eine Verbindung mit [ Systemen ](../connections/connections.md).

## Sandboxes

Beim Erwerb der Komposition föderierter Zielgruppen haben Sie Anspruch auf zwei Sandboxes. Wenden Sie sich bei Anfragen für die Bereitstellung weiterer Sandboxes an Ihren Kontakt beim Adobe-Support.

Gehen Sie wie folgt vor, um die Liste Ihrer aktiven Sandboxes für die Komposition föderierter Zielgruppen anzuzeigen:

1. Rufen Sie in der Komposition föderierter Zielgruppen das Menü **[!UICONTROL Lizenznutzung]** unter **[!UICONTROL Administration]** auf.

1. Klicken Sie auf das Symbol ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) unter **[!UICONTROL Gesamtvolumen der Datenausgabe]**, um auf Ihre Sandbox-Eigenschaften zuzugreifen.

   ![](assets/sandbox_1.png)

1. Informationen über Ihre Sandbox werden im Popup-Fenster „Eigenschaften“ angezeigt.

   ![](assets/sandbox_2.png)

## Berechtigungen {#permissions}

Um auf die Komposition föderierter Zielgruppen zugreifen zu können, müssen Benutzende dem beim Kauf erstellten Sandbox-spezifischen Produktprofil hinzugefügt werden und ihnen muss die Berechtigung **[!UICONTROL Föderierte Daten verwalten]** zugewiesen werden. [Weitere Informationen](feature-access.md)

## IP-Zulassungsauflistung {#ip}

Damit die Komposition föderierter Zielgruppen sicher auf Ihre Datenbanken zugreifen kann, müssen Sie die IP-Adressen der Server für die Komposition föderierter Zielgruppen autorisieren, die darauf zugreifen werden. Diese IP-Adressen werden angezeigt, wenn in der Benutzeroberfläche von Adobe Experience Platform eine föderierte Datenbank hinzugefügt wird. [Weitere Informationen](../connections/connections.md)

Fügen Sie diese IP-Adressen zu Ihrer Zulassungsliste hinzu, um der Komposition föderierter Zielgruppen Zugriff zu gewähren.

## Leitlinien und Einschränkungen {#fac-guardrails}

* Die Federated Audience-Komposition ist derzeit nicht für Kundinnen und Kunden verfügbar [die Gesundheitsdaten aufnehmen](https://experienceleague.adobe.com/de/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Berechtigungen, Produktbeschränkungen und die Leistung betreffende Leitplanken, die in der Dokumentation zu [Adobe Real-Time Customer Data Platform aufgeführt sind](https://experienceleague.adobe.com/de/docs/experience-platform/profile/guardrails){target="_blank"} gelten für die Federated-Audience-Komposition.

<!--* Federated Audience Composition supports the export of large audiences, with file sizes greater than 1 GB. For optimal performance, the maximum recommended file size is up to 20 GB.
-->

