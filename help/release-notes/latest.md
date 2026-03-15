---
title: Versionshinweise zur Federated Audience-Komposition
description: Aktuelle Updates und Versionshinweise für Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 7d12773b36cb963f3d4251a9b88486864056a0fb
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 11%

---


# Versionshinweise

[!DNL Federated Audience Composition] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen werden in diesen Versionshinweisen zusammengefasst. [!DNL Federated Audience Composition] basiert nativ auf [!DNL Adobe Experience Platform] und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Februar &#39;26 {#fac-26-02}

Die Februarversion für Federated Audience Komposition unterstützt die folgenden Funktionen:

### Neue Funktionen {#fac-26-02-feature}

| Unterstützung für Feldanreicherung |
| --- |
| Sie können jetzt die Feldaktivität Speichern in Ihren Kompositionen verwenden. Die Aktivität Feld speichern ermöglicht es Ihnen, Experience Platform-Schemata anzureichern, indem Sie Daten aus externen Warehouses zusammenführen, wodurch Sie Experience Platform-Schemata mit zusätzlichen Attributen erweitern können. Die Aktivität Feld speichern unterstützt sowohl B2B- als auch B2C-Schemata. Weiterführende Informationen zur Verwendung dieser Aktivität finden Sie in der [Aktivitätsübersicht](../compositions/activities.md#save-fields). |

| Erweiterte Authentifizierungsunterstützung für Databricks |
| --- |
| Sie können jetzt mithilfe der Service-Prinzipalauthentifizierung oder mit OAuth 2.0 eine Verbindung zu Federated Audience Composition mit Databricks herstellen. Weiterführende Informationen zum Erstellen einer Verbindung finden Sie in der [Verbindungen - Übersicht](../connections/home.md#create). |

## Version Januar &#39;26 {#fac-26-01}

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
