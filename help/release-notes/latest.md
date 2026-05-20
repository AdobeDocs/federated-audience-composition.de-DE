---
title: Versionshinweise zur Federated Audience-Komposition
description: Aktuelle Updates und Versionshinweise für Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
TQID: https://experienceleague.adobe.com/AqtqibUr1TNXwQ9lrtVoQ3CBNwyjSMS64e4s8y4iTSc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
source-git-commit: 02d8690a6e20c22ddd67afc4899830ccd2f03da9
workflow-type: tm+mt
source-wordcount: 671
ht-degree: 12%

---

# Versionshinweise

[!DNL Federated Audience Composition] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen sind in diesen Versionshinweisen konsolidiert. [!DNL Federated Audience Composition] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Mai &#39;26 {#fac-26-05}

Die Version vom Mai für Federated Audience Composition unterstützt die folgenden Funktionen:

| Authentifizierung des Workload Identity Federation (WIF) für Google Big Query |
| --- |
| Sie können jetzt mit Google Big Query über die WIF-Authentifizierung verbinden. Weitere Informationen zur Verbindung mit der WIF-Authentifizierung finden Sie unter [Verbindungen - Übersicht](/help/connections/home.md#wif-configuration). |

### Verbesserungen {#fac-26-05-improvements}

Diese Version umfasst die folgende Verbesserung.

- **Targeting mehrerer Entitäten mit Zielgruppenkomposition „Federated Audience“ in Adobe Journey Optimizer - Journey lesen**

  Sie können jetzt FAC-Zielgruppenattribute als zusätzliche Kennungen in Journey Optimizer-Journey lesen. Auf diese Weise können Sie die Zielgruppen auf mehreren Entitäten aktivieren, z. B. auf Konto- oder Abonnementebene.

  Weitere Informationen finden Sie im Handbuch [Verwendung zusätzlicher Kennungen in Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

## Version April &#39;26 {#fac-26-04}

Die April-Version für Federated Audience Komposition unterstützt die folgenden Funktionen und Verbesserungen:

### Neue Funktionen {#fac=26-04-feature}

| Neuer Connector - Teradata |
| --- |
| Der Teradata-Connector ist jetzt für die Verwendung mit der Federated Audience-Komposition verfügbar. Sie können den Teradata-Connector für Anwendungsfälle zur Erstellung und Anreicherung von Zielgruppen verwenden. Weitere Informationen zum Teradata-Connector finden Sie unter [Verbindungen - Übersicht](/help/connections/home.md). |

### Verbesserungen {#fac-26-04-improvements}

Diese Version umfasst die folgende Verbesserung.

- **Unterstützung von unverschlüsselten Schlüsseln für Snowflake**

  Sie können jetzt unverschlüsselte Schlüssel verwenden, wenn Sie die Schlüsselpaar-Authentifizierung verwenden, um eine Verbindung mit Snowflake Data Warehouses herzustellen.

  Um mehr über die Verwendung unverschlüsselter Schlüssel mit Snowflake zu erfahren, lesen Sie bitte die [Verbindungen - Übersicht](/help/connections/home.md).

## Version März 2026 {#fac-26-03}

Die März-Version für Federated Audience Komposition unterstützt die folgenden Funktionen:

### Neue Funktionen {#fac-26-03-feature}

| KI-gestützte Segmentierung |
| --- |
| Sie können jetzt im KI-Assistenten eigenständig zusammengeführte Zielgruppenkompositionen erstellen. Wenn Sie die Zielgruppe mit dem KI-Assistenten erstellen, generiert der KI-Assistent einen Plan, der nach der Genehmigung in Ihrem Browser ausgeführt wird. Weitere Informationen zur Verwendung des KI-Assistenten zum Erstellen von Zielgruppen finden Sie im Abschnitt [Übersicht über den KI-Assistenten](/help/start/ai-assistant.md). |

| KI-Assistent für operative Erkenntnisse |
| --- |
| Sie können jetzt dem KI-Assistenten Fragen zu operativen Einblicken in die Federated Audience-Komposition stellen. Zu den unterstützten Bereichen gehören Verbindungen, Schemata und Datenmodelle. Verknüpfte Kompositionen werden **dieser Version** unterstützt. Weitere Informationen zum KI-Assistenten in der Federated-Audience-Komposition finden Sie in der [Übersicht zum KI-Assistenten](/help/start/ai-assistant.md). |

## Version Februar 2026 {#fac-26-02}

Die Februarversion für Federated Audience Komposition unterstützt die folgenden Funktionen:

### Neue Funktionen {#fac-26-02-feature}

| Unterstützung für Feldanreicherung |
| --- |
| Sie können jetzt die Feldaktivität Speichern in Ihren Kompositionen verwenden. Die Aktivität Feld speichern ermöglicht es Ihnen, Experience Platform-Schemata anzureichern, indem Sie Daten aus externen Warehouses zusammenführen, wodurch Sie Experience Platform-Schemata mit zusätzlichen Attributen erweitern können. Die Aktivität Feld speichern unterstützt sowohl B2B- als auch B2C-Schemata. Weiterführende Informationen zur Verwendung dieser Aktivität finden Sie in der [Aktivitätsübersicht](../compositions/activities.md#save-fields). |

| Erweiterte Authentifizierungsunterstützung für Databricks |
| --- |
| Sie können jetzt mithilfe der Service-Prinzipalauthentifizierung oder mit OAuth 2.0 eine Verbindung zu Federated Audience Composition mit Databricks herstellen. Weiterführende Informationen zum Erstellen einer Verbindung finden Sie in der [Verbindungen - Übersicht](../connections/home.md#create). |

## Version Januar 2026 {#fac-26-01}

Die Version vom Januar für Federated Audience Composition unterstützt die folgenden neuen Funktionen und Verbesserungen:

### Neue Funktionen {#fac-26-01-feature}

| Unterstützung der Azure Synapse-Service-Prinzipalauthentifizierung |
| --- |
| Sie können jetzt mit Azure Synapse über einen Service-Prinzipal eine Verbindung zur Federated Audience-Komposition herstellen. Weiterführende Informationen zum Erstellen einer Verbindung finden Sie in der [Verbindungen - Übersicht](../connections/home.md#create). |

| Verfügbarkeit für Adobe Experience Platform-Kunden in Amazon Web Services (AWS) |
| --- |
| Sie können jetzt die Federated Audience-Komposition verwenden, wenn sich Ihre Experience Platform-Instanz in AWS befindet. Weitere Informationen zu Experience Platform in AWS finden Sie unter [Übersicht über Multi-Cloud](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud). |

### Verbesserungen {#fac-26-01-improvements}

Diese Version umfasst die folgende Verbesserung.

- **Konfiguration des Datenablaufs für Zielgruppen**

  Sie können jetzt eine Datengültigkeit festlegen, wenn Sie die Aktivität **Zielgruppe speichern** in einer Komposition verwenden.

  Weitere Informationen zur Datengültigkeit in der Federated-Audience-Komposition finden Sie im [Aktivitätshandbuch](../compositions/activities.md#save-audience).
