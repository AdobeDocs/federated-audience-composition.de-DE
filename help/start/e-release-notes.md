---
title: Neue Funktionen zur Komposition föderierter Zielgruppen in Experience Platform
description: Neueste Aktualisierungen und Versionshinweise
hide: true
hidefromtoc: true
exl-id: 23ea1a5d-a0e4-4f47-b0f8-56009bbc0a4a
source-git-commit: a33c3706836e578246c994130d6b46c0cb0e5c1f
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 89%

---

# Versionshinweise {#rn-new}

[!DNL Federated Audience Composition] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen sind in diesen Versionshinweisen konsolidiert. [!DNL Federated Audience Composition] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Juni 2025 {#fac-25-6}

Diese Version umfasst die folgenden Verbesserungen:

* **Allgemeine Verfügbarkeit für Kundinnen und Kunden im Gesundheitswesen**

  Die Federated Audience-Komposition steht Healthcare-Kunden bis Ende Juni für Anwendungsfälle zur Zielgruppenerstellung, -anreicherung und -Profilanreicherung zur Verfügung.

* **Zugriffssteuerung auf Objektebene**

  Die Federated Audience-Komposition unterstützt jetzt die Zugriffssteuerung auf Objektebene, um Zugriffsbeschriftungen auf die angegebenen Kompositionen anzuwenden.

* **Standardrollen**

  Sie können jetzt eine der Standardrollen verwenden, um Benutzerberechtigungen für den Zugriff auf die Federated Audience Composition zu verwalten.

* **Inkrementelle Aktualisierungen in Anwendungsfällen zur Profilanreicherung**

  Die Aktivität Profile speichern unterstützt jetzt inkrementelle Aktualisierungen. Mit inkrementellen Aktualisierungen können Sie inkrementelle Daten abfragen und aktualisieren und dabei Profile mit Daten aus externen Data Warehouses anreichern.

## Version April 2025 {#fac-25-4}

### Verbesserungen {#fac-25-4-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Arbeitsflächenansicht des Datenmodells**

  Die Arbeitsflächenansicht für den Abschnitt „Datenmodelle“ sorgt für ein besseres Erlebnis. Denn sie ermöglicht neben der vorhandenen Tabellenansicht eine Visualisierung von Datenmodellen und deren Links in einem Arbeitsflächen-Layout. [Weitere Informationen](../data-management/gs-models.md)

* **KI-Assistent**

  Der KI-Assistent ist eine Funktion der Benutzeroberfläche, mit der Sie durch Adobe-Konzepte navigieren und diese verstehen sowie betriebliche Erkenntnisse zu Ihrer Umgebung erhalten können. Er ist in verschiedenen Produkten in Adobe Experience Cloud verfügbar, einschließlich der Komposition föderierter Zielgruppen. [Weitere Informationen](../start/audiences.md)

* **Datenmodellname**

  Im Menü „Zielgruppen“ wird auf der Registerkarte **Föderierte Kompositionen** nun der Datenmodellname anstelle der ID angezeigt, was mehr Klarheit bietet und die allgemeine Benutzerfreundlichkeit verbessert.

* **Zielgruppe**

  Im Menü „Zielgruppe“ wird nun der Name oder das Label des ausgewählten Datenmodells angezeigt, wenn Benutzende ein Datenmodell ohne verknüpfte Zielgruppen auswählen.

### Kompatibilität {#fac-25-4-compat}

* **Sichere Snowflake-Verbindung**

  Mit dieser neuen Version unterstützt die Komposition föderierter Zielgruppen sichere Verbindungen über private Links zu Amazon Redshift-Datenbanken, die auf Microsoft Azure gehostet werden. [Weitere Informationen](../connections/federated-db.md#amazon-redshift)

## Version März 2025 {#fac-25-3}

### Verbesserungen {#fac-25-3-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Berechtigungen zur Komposition föderierter Zielgruppen**

  Ab der Version März erzwingt [!DNL Federated Audience Composition] den Zugriff auf die Schnittstellen für **föderiertes Daten-Management** und **föderierte Kompositionen** für Benutzende, denen die Berechtigung **Föderierte Daten verwalten** zugewiesen wurde.

  Wir empfehlen Benutzenden, sich an die Admins zu wenden, damit diese Berechtigung ihrer Rolle hinzugefügt wird, um weiterhin auf die Benutzeroberfläche der [!DNL Federated Audience Composition] zugreifen zu können.

  Wie Sie diese Berechtigung zuweisen, erfahren Sie in der [entsprechenden Dokumentation](feature-access.md).

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. [Learn more](ai-assistant.md)
-->


### Kompatibilität {#fac-25-3-compat}

* **Databricks-Verbindung**

  Mit dieser neuen Version unterstützt die Komposition föderierter Zielgruppen jetzt die Konnektivität privater Links für Verbindungen zu Databricks-Datenbanken.
Dazu gehören sichere Verbindungen zu Databricks-Datenbanken, die auf Amazon Web Services (AWS) über einen privaten Link gehostet werden, und Databricks-Datenbanken, die auf Microsoft Azure über VPN gehostet werden. [Weitere Informationen](../connections/federated-db.md#databricks)

* **Unterstützung für CDP-B2B-Kundschaft**

  Die Komposition föderierter Zielgruppen ist jetzt für B2B-Kundschaft (Business-to-Business) von Customer Data Platform (CDP) für personenbasierte Anwendungsfälle für Zielgruppen verfügbar.

* **Sichere Snowflake-Verbindung**

  Mit dieser neuen Version unterstützt die Komposition föderierter Zielgruppen sichere Verbindungen über private Links zu Snowflake-Datenbanken, die auf Microsoft Azure gehostet werden. [Weitere Informationen](../connections/federated-db.md#snowflake)

## Version Februar 2025 {#fac-25-2}

Diese Version enthält die unten aufgeführten Änderungen.

* **Unterstützung für Microsoft Fabric**

  Sie können nun über die Funktion „Komposition föderierter Zielgruppen“ Verbindungen zu Microsoft Fabric-Datenbanken herstellen. [Weitere Informationen](../connections/federated-db.md)

* **Unterstützung für Amazon Redshift Spectrum**

  Amazon Redshift Spectrum wird jetzt für Amazon Redshift-Datenbankverbindungen unterstützt. [Weitere Informationen](../connections/federated-db.md#amazon-redshift)

* **Verbessertes Erlebnis bei der Schemaerstellung**

  Der Prozess der Schemaerstellung wurde durch eine aktualisierte Benutzeroberfläche verbessert, die intuitiver ist und eine einfachere Navigation bietet. Diese Verbesserungen bieten Datenverantwortlichen eine reibungslosere und effizientere Möglichkeit, Datenmodelle zu entwickeln. [Weitere Informationen](../customer/schemas.md)

* **Unterstützung der Zielgruppenanreicherung für Databricks**

  Sie können jetzt Databricks im Fluss „Zielgruppe lesen“ verwenden, wodurch Aktivitäten für Databricks-Datenbanken aktiviert werden und sie als neues Ziel eingerichtet werden können. [Weitere Informationen](../connections/destinations.md)

## Version November 2024 {#fac-24-11}

### Verbesserungen {#fac-24-11-improvements}

Diese Version enthält die unten aufgeführte Verbesserung.

* **IP-Adressen-Zulassungsliste**

  Beim Hinzufügen einer föderierten Datenbank in der Benutzeroberfläche von Adobe Experience Platform können Sie jetzt die IP-Adressen direkt anzeigen, die mit Ihren Instanzen der Komposition föderierter Zielgruppen verknüpft sind. Auf diese Weise können Sie diese IP-Adressen einfach kopieren und autorisieren, um eine Verbindung mit Ihrer Datenbank herzustellen und so die Sicherheit und Flexibilität zu verbessern. [Weitere Informationen](../connections/connections.md)

## Version Oktober 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Die Komposition föderierter Zielgruppen in Adobe Experience Platform, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen ist (LA), steht jetzt allen Benutzenden zur Verfügung (GA). Diese Funktion wird basierend auf Ihrem Angebot aktiviert und nur mit den zugehörigen Berechtigungen angezeigt. [Weitere Informationen](access-prerequisites.md)
>

### Kompatibilität {#fac-24-10-compat}

Mit dieser neuen Version ist die Komposition föderierter Zielgruppen nun mit den unten aufgeführten Systemen kompatibel.

* **Unterstützung für Databricks**

  Sie können nun über die Funktion „Komposition föderierter Zielgruppen“ Verbindungen zu Databricks-Datenbanken herstellen. [Weitere Informationen](../connections/federated-db.md#databricks)

* **Unterstützung für sicheren Zugriff auf Snowflake über AWS PrivateLink**

  Sicherer Zugriff auf Ihr externes Snowflake-Data-Warehouse über einen privaten Link wird nun unterstützt. Ihr Snowflake-Konto muss auf Amazon Web Services (AWS) gehostet werden und sich in derselben Region wie Ihre Umgebung mit der Funktion „Komposition föderierter Zielgruppen“ befinden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen, um einen sicheren Zugriff auf Ihr Snowflake-Konto einzurichten. [Weitere Informationen](../connections/federated-db.md#snowflake)

* **Unterstützung für Amazon Redshift Serverless**

  Mit dieser neuen Version unterstützt die Funktion „Komposition föderierter Zielgruppen“ [Amazon Redshift Serverless](https://aws.amazon.com/de/redshift/redshift-serverless/){target="_blank"}.

### Verbesserungen {#fac-24-10-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Aktualisieren vorhandener Schemata**

  Wenn eine Spalte in einer föderierten Datenbank erstellt, geändert oder gelöscht wird, können Sie die Änderungen nun erkennen und anwenden, indem Sie im entsprechenden Schema auf die Schaltfläche **[!UICONTROL Schema aktualisieren]** klicken. [Weitere Informationen](../customer/schemas.md#schema-refresh)

* **Verknüpfen eines Datenmodells mit einer neuen Komposition**

  Beim Erstellen einer Komposition können Sie nun das Datenmodell auswählen, das ihr zugeordnet werden soll. Mit dieser neuen Option lassen sich Ihre Aktivitäten einfacher konfigurieren, da nur Tabellen des zugehörigen Datenmodells verfügbar sind. [Weitere Informationen](../compositions/create-composition.md)

## Version Juli 2024 – Komposition föderierter Zielgruppen (LA) {#fac-la}

Die Komposition föderierter Zielgruppen ermöglicht Unternehmen einen flexiblen und erweiterten Zugriff auf Unternehmens-Data-Warehouses, um Zielgruppen unter Verwendung wichtiger Unternehmensdatensätze zu komponieren sowie markeninitiierte und aktuelle Erlebnisse zu ermöglichen. Mit diesem neuen Ansatz können Sie als Benutzerin oder Benutzer von [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/home){target="_blank"} bzw. [Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home){target="_blank"} Zielgruppendaten direkt aus Ihrem vorhandenen Data Warehouse zusammenführen, um die Zielgruppen von Adobe Experience Platform in einem einzigen System anzureichern.

Die Komposition föderierter Zielgruppen richtet sich an die wachsenden Anforderungen des Marktes an Unternehmen, die Flexibilität benötigen, um Zielgruppen mit Warehouse-Datensätzen zu komponieren. Auf diese Weise können Unternehmen die Datenbewegung reduzieren und gleichzeitig Marketing-Teams wichtige Zielgruppendaten zur Verfügung stellen, um die Anforderungen von Anwendungsfällen zu erfüllen und personalisierte Erlebnisse zu ermöglichen.

Weitere Informationen zu den Möglichkeiten der Komposition föderierter Zielgruppen finden Sie auf [dieser Seite](get-started.md) und in den [häufig gestellten Fragen](faq.md).

Ausführliche Informationen zu den Voraussetzungen für den Zugriff auf Kompositionen föderierter Zielgruppen und die aktuellen Leitlinien finden Sie auf [dieser Seite](access-prerequisites.md).
