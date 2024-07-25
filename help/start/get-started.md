---
title: Erste Schritte mit Federated Audience-Komposition
description: Erfahren Sie, was unter Adobe Federated Audience Komposition zu verstehen ist und wie Sie sie in Adobe Experience Platform verwenden.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 3b4f5284cd65cd5cd30c4223fe2df3ffff7c0905
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 11%

---

# Erste Schritte mit Federated Audience-Komposition {#gs-fac}

Zusammengestellte Zielgruppenkomposition ist ein Add-on für Adobe Real-time Customer Data Platform und Adobe Journey Optimizer, mit dem Sie Zielgruppen aus Ihren Drittanbieter-Data Warehouse erstellen und anreichern und die Zielgruppen in Adobe Experience Platform importieren können. Federated Audience Komposition bietet eine einfache und leistungsstarke Lösung, um Ihr Enterprise Data Warehouse direkt in Adobe Real-time Customer Data Platform und/oder Adobe Journey Optimizer zu verbinden und Abfragen über die Tabellen in Ihrem Data Warehouse durchzuführen.

Mit der Adobe Federated Audience Komposition können Anwender von Adobe Experience Platform-Apps auf ihre Kundendaten zugreifen, die in ihren Data Warehouse und Cloud-Speicherplattformen wie Amazon Redshift, Azure synapse Analytics und mehr gespeichert sind. Kundendaten können in mehreren Data Warehouse gespeichert werden und sind jetzt ohne Replikation sofort verfügbar. Die unterstützten Plattformen werden auf [dieser Seite](../connections/federated-db.md#supported-db) aufgeführt.

## Anwendungsfälle {#rn-uc}

Erstellen Sie über eine marketingfreundliche Benutzeroberfläche Segmentregeln, die in Ihrem Data Warehouse eine Liste von Benutzern abfragen, die sich für ein bestimmtes Segment qualifizieren, das für Marketing-Kampagnen benötigt wird, greifen Sie zur Aktivierung auf vorhandene Zielgruppen in Data Warehouse zu oder ergänzen Sie Adobe Experience Platform-Zielgruppen mit zusätzlichen Datenpunkten, die in Warehouse vorhanden sind.

In dieser Version sind zwei Anwendungsfälle verfügbar: Zielgruppenerstellung und Zielgruppenanreicherung.

![Diagramm](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Die wichtigsten Schritte {#gs-steps}

Mit der Adobe Federated Audience Komposition können Sie Adobe Experience Platform-Zielgruppen direkt aus Ihrer Datenbank erstellen und aktualisieren, ohne dass ein Aufnahmevorgang erforderlich ist.

![Diagramm](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

Wichtigste Schritte:

1. **Datenintegration**: Zusammenführen von Daten aus verschiedenen Quellen und Zusammenführen dieser Daten zu einem einheitlichen Datensatz. Informationen zum Verbinden von Adobe Experience Platform-Apps mit Ihrem Enterprise Data Warehouse, unterstützten Datenbanken und deren Konfiguration finden Sie in [diesem Abschnitt](../connections/federated-db.md).

2. **Datenmodellierung**: Entwerfen und erstellen Sie Datenmodelle und -schemas, die die Struktur, die Beziehungen und Einschränkungen der Daten definieren. Weitere Informationen zu Schemata finden Sie auf [dieser Seite](../customer/schemas.md). Erfahren Sie auf [dieser Seite](../data-management/gs-models.md), wie Sie Links für Ihr Datenmodell erstellen.

3. **Datenumwandlung**: Wenden Sie Datenbearbeitungsmethoden an, um das Format, die Struktur oder die Werte von Datenelementen zu ändern, damit sie kompatibel oder für bestimmte Analysen oder Anwendungen geeignet sind.

4. **Datenverwendung**: Erstellen, orchestrieren und erstellen Sie Zielgruppen. Erfahren Sie, wie Sie in [dieser Seite](../compositions/gs-compositions.md) Zielgruppen erstellen. Sie können vorhandene Zielgruppen auch über das Adobe Experience Platform Audience Portal und die Ziele aktualisieren oder wiederverwenden. Weiterführende Informationen finden Sie auf [dieser Seite](../connections/destinations.md)


>[!NOTE]
>
>Nach der Ausführung der Komposition wird die resultierende Zielgruppe in Adobe Experience Platform als externe Zielgruppe gespeichert und in der Echtzeit-Kundendatenplattform von Adobe und/oder Adobe Journey Optimizer verfügbar gemacht. Sie ist im Menü **Zielgruppen** verfügbar. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



## Weitere Informationen {#learn}

<!-- Workflow + Workflow activities-->

Siehe Häufig gestellte Fragen in [dieser Seite](faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Ausführungseinstellungen"
>abstract="In diesem Abschnitt können Sie Einstellungen für die Ausführung des Workflows konfigurieren, z. B. die Anzahl der Tage, in denen der Kompositionsverlauf beibehalten wird."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktivität nicht bearbeitbar"
>abstract="Wenn eine **Abfrage** oder **Anreicherung** mit zusätzlichen Daten in der Konsole konfiguriert wird, werden die Anreicherungsdaten berücksichtigt und an die ausgehende Transition übergeben. Sie können jedoch nicht bearbeitet werden."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Erstellen eines Links"
>abstract="Definieren Sie die Link-Einstellungen."
