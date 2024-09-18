---
title: Erste Schritte mit der Komposition föderierter Zielgruppen in Experience Platform
description: Erfahren Sie, was die Komposition föderierter Zielgruppen ist und wie Sie diese in Adobe Experience Platform verwenden.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 8b67aa9258b05a6ca239dd54ebb10273826ea550
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 97%

---

# Erste Schritte mit der Komposition föderierter Zielgruppen {#gs-fac}

Die Komposition föderierter Zielgruppen ist eine Add-on-Funktion für [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/home){target="_blank"} und [Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home){target="_blank"}, mit der Sie Zielgruppen aus Data Warehouses von Drittanbietern erstellen und anreichern sowie die Zielgruppen in Adobe Experience Platform importieren können. Die Komposition föderierter Zielgruppen bietet eine einfache und leistungsstarke Lösung, um Ihr Unternehmens-Data Warehouse direkt in Adobe Real-Time Customer Data Platform und/oder Adobe Journey Optimizer zu verbinden und Abfragen über die Tabellen in Ihrem Data Warehouse durchzuführen.

Mit der Komposition föderierter Zielgruppen von Adobe können Benutzerinnen und Benutzer von Adobe Experience Platform-Apps auf ihre Kundendaten zugreifen, die in ihren Data Warehouses und auf Cloud-Speicherplattformen wie Amazon Redshift, Azure Synapse Analytics usw. gespeichert sind. Kundendaten können in mehreren Data Warehouses gespeichert werden und sind jetzt ohne Replikation sofort verfügbar. Welche Plattformen unterstützt werden, erfahren Sie auf [dieser Seite](../connections/federated-db.md#supported-db).

## Funktionen {#rn-capabilities}

Die Komposition föderierter Zielgruppen steigert den Wert von Real-Time CDP und Adobe Journey Optimizer mit einem umfassenden Ansatz für die Kuration und Aktivierung von Zielgruppen:

* Erweitern Sie den Zugriff auf kritische Warehouse-basierte Datensätze, um hochwertige Zielgruppen zu erstellen: Nutzen Sie vorhandene Data Warehouses als Hauptaufzeichnungssystem und nutzen Sie gleichzeitig marktführende Anwendungen, um großartige Kundenerlebnisse zu erzielen.

* Umfassende Unterstützung für Anwendungsfälle zur Interaktion: Die Komposition föderierter Zielgruppen in Verbindung mit Real-Time CDP oder Journey Optimizer unterstützt markeninitiierte, personalisierte Erlebnisse mit föderierten Zielgruppen und bietet durch Echtzeitereignisse ausgelöste Ad-hoc-Erlebnisse, in Kombination mit Attributen zu Personen, um die Anforderungen an Anwendungsfälle über alle Teams hinweg zu erfüllen.

* Minimieren der Datenbewegung und -duplizierung: Erstellen Sie Zielgruppen aus Datensätzen, die in einem Unternehmens-Data Warehouse gespeichert sind, ohne die zugrunde liegenden Daten zu kopieren, um umsetzbare Marketing-Profile und -Zielgruppen zu verwalten.

* Verwenden Sie ein einziges System für erlebnisgesteuerte Workflows: Kuratieren Sie aufgenommene und föderierte Zielgruppen in Adobe Experience Platform und koordinieren Sie ausgehende Erlebnisse über alle Kanäle hinweg.

## Anwendungsfälle {#rn-uc}

Erstellen Sie über eine Marketing-freundliche Benutzeroberfläche Segmentregeln, mit denen in Ihrem Data Warehouse eine Liste der Benutzenden abgefragt wird, die für ein bestimmtes, für Marketing-Kampagnen benötigtes Segment infrage kommen. Greifen Sie zur Aktivierung auf vorhandene Zielgruppen im Warehouse zu oder reichern Sie Adobe Experience Platform-Zielgruppen mit zusätzlichen Datenpunkten aus dem Warehouse an.

In dieser Version sind zwei Anwendungsfälle verfügbar:

1. Zielgruppenerstellung: Erstellen Sie neue Zielgruppen aus Unternehmenskatalogen, ohne die zugrunde liegenden Daten zu kopieren, und aktivieren Sie diese Zielgruppen mit vordefinierten Zielen.

1. Zielgruppenanreicherung: Reichern Sie vorhandene Zielgruppen in Adobe Experience Platform an, indem Sie zusammengestellte Zielgruppendaten verwenden, die mit dem Unternehmens-Data Warehouse föderiert wurden. Diese Daten werden nicht in Adobe Experience Platform-Kundenprofilen beibehalten.

![Diagramm](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Die wichtigsten Schritte {#gs-steps}

Mit der Komposition föderierter Zielgruppen von Adobe können Sie Adobe Experience Platform-Zielgruppen direkt aus Ihrer Datenbank erstellen und aktualisieren, ohne dass ein Aufnahmevorgang erforderlich ist.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

Die wichtigsten Schritte:

1. **Datenintegration**: Führen Sie Daten aus verschiedenen Quellen zu einem einheitlichen Datensatz zusammen. Informationen zum Verbinden von Adobe Experience Platform-Apps mit Ihrem Unternehmens-Data Warehouse, den unterstützten Datenbanken und deren Konfiguration finden Sie in [diesem Abschnitt](../connections/federated-db.md).

1. **Datenmodellierung**: Entwerfen und erstellen Sie Datenmodelle und -schemata, welche die Struktur, die Beziehungen und Einschränkungen der Daten definieren. Weitere Informationen zu Schemata finden Sie auf [dieser Seite](../customer/schemas.md). Wie Sie Links für Ihr Datenmodell erstellen, erfahren Sie auf [dieser Seite](../data-management/gs-models.md).

1. **Datenumwandlung**: Wenden Sie Datenbearbeitungsmethoden an, um das Format, die Struktur oder die Werte von Datenelementen zu ändern, damit sie kompatibel oder für bestimmte Analysen oder Anwendungen geeignet sind.

1. **Datennutzung**: Erstellen, orchestrieren und bauen Sie Zielgruppen auf. Wie Sie Zielgruppen erstellen, erfahren Sie auf [dieser Seite](../compositions/gs-compositions.md). Sie können vorhandene Zielgruppen auch über das Zielgruppenportal und die Ziele von Adobe Experience Platform aktualisieren oder wiederverwenden. Weiterführende Informationen finden Sie auf [dieser Seite](../connections/destinations.md)

>[!NOTE]
>
>Nach der Ausführung der Komposition wird die resultierende Zielgruppe in Adobe Experience Platform als externe Zielgruppe gespeichert und in Adobe Real-Time Customer Data Platform und/oder Adobe Journey Optimizer zur Verfügung gestellt. Sie wird im Menü **Zielgruppen** zur Verfügung gestellt. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Weitere Informationen {#learn}

<!-- Workflow + Workflow activities-->


Erfahren Sie auf [dieser Seite](access-prerequisites.md), wie Sie auf Komposition föderierter Zielgruppen, Leitlinien und Einschränkungen zugreifen können.

Sehen Sie sich auch die häufig gestellten Fragen auf [dieser Seite](faq.md) an.


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Ausführungseinstellungen"
>abstract="In diesem Abschnitt können Sie Einstellungen für die Ausführung der Komposition konfigurieren, beispielsweise für wie viele Tage der Kompositionsverlauf gespeichert wird."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktivität nicht bearbeitbar"
>abstract="Wenn eine **Abfrage** oder **Anreicherung** mit zusätzlichen Daten in der Konsole konfiguriert wird, werden die Anreicherungsdaten berücksichtigt und an die ausgehende Transition übergeben. Sie können jedoch nicht bearbeitet werden."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Erstellen eines Links"
>abstract="Die Link-Einstellungen definieren."
