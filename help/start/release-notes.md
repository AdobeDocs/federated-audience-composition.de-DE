---
title: Neue Funktionen zur Komposition föderierter Zielgruppen in Experience Platform
description: Neueste Aktualisierungen und Versionshinweise
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 61a70f9de0a6cf171a2ff1128b57ae6206be842c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 53%

---

# Versionshinweise {#rn-new}

[!DNL Federated Audience Composition] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen sind in diesen Versionshinweisen konsolidiert. [!DNL Federated Audience Composition] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Oktober 24 {#fac-24-10}

### Kompatibilität {#fac-24-10-compat}

Mit dieser neuen Version ist die Zusammenstellung von Federated Audience nun mit den unten aufgeführten Systemen kompatibel.

* **Unterstützung von Databricks**

  Sie können jetzt über Federated Audience Komposition Verbindungen zu Datenbanken von Databricks herstellen. [Weitere Informationen](../connections/federated-db.md#databricks)

* **Unterstützung für sicheren Zugriff auf Snowflake über AWS PrivateLink**

  Der sichere Zugriff auf Ihr externes Snowflake Data Warehouse über einen privaten Link wird jetzt unterstützt. Beachten Sie, dass Ihr Snowflake-Konto auf Amazon Web Services (AWS) gehostet werden muss und sich in derselben Region wie Ihre Federated Audience Komposition-Umgebung befindet. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, wenn Sie Hilfe beim Einrichten eines sicheren Zugriffs auf Ihr Snowflake-Konto benötigen. [Weitere Informationen](../connections/federated-db.md#snowflake)

* **Amazon Redshift Server-lose Unterstützung**

  Mit dieser neuen Version unterstützt die Zusammenstellung von Federated Audience [Amazon Redshift Server-los](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Verbesserungen {#fac-24-10-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Vorhandene Schemas aktualisieren**

  Wenn eine Spalte in einer verbundenen Datenbank erstellt, geändert oder gelöscht wird, können Sie die Änderungen nun erkennen und anwenden, indem Sie im entsprechenden Schema auf die Schaltfläche **[!UICONTROL Schema aktualisieren]** klicken. [Weitere Informationen](../customer/schemas.md#schema-refresh)

* **Verknüpfen eines Datenmodells mit einer neuen Komposition**

  Beim Erstellen einer Komposition können Sie jetzt das Datenmodell auswählen, das ihr zugeordnet werden soll. Mit dieser neuen Option ist die Konfiguration Ihrer Aktivitäten einfacher, da nur Tabellen des zugehörigen Datenmodells verfügbar sind. [Weitere Informationen](../compositions/create-composition.md)

## Version vom 24. Juli - Zusammengestellte Zielgruppen-Komposition (LA) {#fac-la}

>[!AVAILABILITY]
>
>Die Komposition föderierter Zielgruppen in Experience Platform ist derzeit nur für eine Gruppe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). 
>

Bei der Komposition föderierter Zielgruppen handelt es sich um eine Add-on-Funktion, die Unternehmen einen flexiblen und erweiterten Zugriff auf Unternehmens-Data Warehouses ermöglicht, um Zielgruppen unter Verwendung wichtiger Unternehmensdatensätze zu komponieren sowie markeninitiierte und aktuelle Erlebnisse zu ermöglichen. Mit diesem neuen Ansatz können Sie als Benutzer oder Benutzer von [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/home){target="_blank"} bzw. [Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home){target="_blank"} Zielgruppendaten direkt aus ihrem vorhandenen Data Warehouse zusammenführen, um die Zielgruppen von Adobe Experience Platform in einem einzigen System anzureichern.

Die Komposition föderierter Zielgruppen richtet sich an die wachsenden Anforderungen des Marktes an Unternehmen, die Flexibilität benötigen, um Zielgruppen mit Warehouse-Datensätzen zusammenzustellen. Auf diese Weise können Unternehmen die Datenbewegung reduzieren und gleichzeitig Marketing-Teams wichtige Zielgruppendaten zur Verfügung stellen, um die Anforderungen von Anwendungsfällen zu erfüllen und personalisierte Erlebnisse zu ermöglichen. 

Weitere Informationen zu den Möglichkeiten der Komposition föderierter Zielgruppen finden Sie auf [dieser Seite](get-started.md) und in den [häufig gestellten Fragen](faq.md).

Ausführliche Informationen zu den Voraussetzungen für den Zugriff auf Kompositionen föderierter Zielgruppen und die aktuellen Leitlinien finden Sie auf [dieser Seite](access-prerequisites.md).

