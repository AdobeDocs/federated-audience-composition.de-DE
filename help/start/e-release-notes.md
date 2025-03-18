---
title: Neue Funktionen zur Komposition föderierter Zielgruppen in Experience Platform
description: Neueste Aktualisierungen und Versionshinweise
hide: true
hidefromtoc: true
source-git-commit: 016623ed6aa6e3b2c4dafa5733fd6d1a00109271
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 66%

---

# Versionshinweise {#rn-new}

[!DNL Federated Audience Composition] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen sind in diesen Versionshinweisen konsolidiert. [!DNL Federated Audience Composition] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen von Platform. Weitere Informationen zu diesen Änderungen finden Sie unter [Versionshinweise zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version vom 25. März {#fac-25-3}

### Verbesserungen {#fac-25-3-improvements}

Diese Version enthält die folgenden Verbesserungen.

* **Berechtigungen für zusammengeführte Zielgruppenkomposition**

  Ab März erzwingen [!DNL Federated Audience Composition] den Zugriff auf die Schnittstellen **Federated Data Management** und **Federated Compositions** für Benutzende, denen die Berechtigung **Federated Data verwalten** wurde.

  Wir empfehlen Benutzern, sich an die Administratoren zu wenden, damit diese Berechtigung ihrer Rolle hinzugefügt wird, um weiterhin auf die [!DNL Federated Audience Composition] Benutzeroberfläche zugreifen zu können.

  Informationen zum Zuweisen dieser Berechtigung finden Sie in der [ Dokumentation](feature-access.md).

* **Arbeitsfläche des Datenmodells**

  Die Arbeitsflächen-Ansicht für den Abschnitt Datenmodelle verbessert das Erlebnis, indem sie die Visualisierung von Datenmodellen und deren Links in einem Arbeitsflächen-Layout neben der vorhandenen Tabellenansicht ermöglicht. [Weitere Informationen](../data-management/gs-models.md)

* **Zielgruppenexport**

  Die Federated Audience-Komposition unterstützt jetzt den Export großer Zielgruppen und verarbeitet Dateigrößen von bis zu 20 GB.

* **KI-Assistent**

  Der KI-Assistent ist eine Funktion der Benutzeroberfläche, die Ihnen hilft, Adobe-Konzepte zu navigieren und zu verstehen und operative Einblicke für Ihre spezifische Umgebung zu erhalten. Es ist in verschiedenen Produkten in Adobe Experience Cloud verfügbar, einschließlich Federated Audience Composition.

### Kompatibilität {#fac-25-3-compat}

* **Datenbricks-Verbindung**

  Mit dieser neuen Version unterstützt die Federated Audience-Komposition jetzt die Konnektivität privater Links für Datenbankverbindungen von Databricks.
Es ermöglicht auch sichere Verbindungen zu Datenbanken von Databricks, die auf Amazon Web Services (AWS) und Azure gehostet werden. [Weitere Informationen](../connections/federated-db.md#databricks)

* **Support für B2B CDP-Kunden**

  Federated Audience Composition ist jetzt für B2B-Kunden (Business-to-Business) von Customer Data Platform (CDP) für personenbasierte Anwendungsfälle von Zielgruppen verfügbar.

* **Sichere Snowflake-Verbindung**

  Mit dieser neuen Version unterstützt Federated Audience Composition sichere private Link-Verbindungen zu Snowflake-Datenbanken, die auf Azure gehostet werden. [Weitere Informationen](../connections/federated-db.md#snowflake)

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
>Die Komposition föderierter Zielgruppen in Adobe Experience Platform, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen ist (LA), steht jetzt allen Benutzenden zur Verfügung (GA). Diese Funktion wird basierend auf Ihrem Angebot aktiviert und ist nur mit den zugehörigen Berechtigungen sichtbar. [Weitere Informationen](access-prerequisites.md)
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

Die Federated Audience-Komposition bietet Unternehmen einen flexiblen und erweiterten Zugriff auf Unternehmens-Data Warehouses, um Zielgruppen mithilfe kritischer Unternehmensdatensätze zu erstellen und markeninitiierte und aktuelle Erlebnisse zu ermöglichen. Mit diesem neuen Ansatz können Sie als Benutzer oder Benutzer von [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/home){target="_blank"} bzw. [Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home){target="_blank"} Zielgruppendaten direkt aus ihrem vorhandenen Data Warehouse zusammenführen, um die Zielgruppen von Adobe Experience Platform in einem einzigen System anzureichern.

Die Federated Audience-Komposition erfüllt wachsende Marktanforderungen für Unternehmen, die die Flexibilität benötigen, Zielgruppen mit Warehouse-Datensätzen zu erstellen. Auf diese Weise können Unternehmen die Datenbewegung reduzieren und gleichzeitig Marketing-Teams wichtige Zielgruppendaten zur Verfügung stellen, um die Anforderungen von Anwendungsfällen zu erfüllen und personalisierte Erlebnisse zu ermöglichen.

Weitere Informationen zu den Möglichkeiten der Komposition föderierter Zielgruppen finden Sie auf [dieser Seite](get-started.md) und in den [häufig gestellten Fragen](faq.md).

Ausführliche Informationen zu den Voraussetzungen für den Zugriff auf Kompositionen föderierter Zielgruppen und die aktuellen Leitlinien finden Sie auf [dieser Seite](access-prerequisites.md).


