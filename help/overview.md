---
title: Übersicht über die zusammengeführte Zielgruppenkomposition
description: Erfahren Sie mehr über die Adobe Federated Audience-Komposition und deren Verwendung in nachgelagerten Services wie Adobe Experience Platform und Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# Übersicht über die zusammengeführte Zielgruppenkomposition

Mit der Federated Audience-Komposition können Sie Zielgruppen aus Data Warehouses von Drittanbietern erstellen und anreichern sowie die Zielgruppen in Adobe Experience Platform importieren. Dies bietet eine einfache und leistungsstarke Lösung, um Ihr Unternehmens-Data Warehouse direkt mit nachgelagerten Services wie Adobe Real-Time Customer Data Platform oder Adobe Journey Optimizer zu verbinden und Abfragen für die Tabellen Ihres Data Warehouse durchzuführen. Auf diese Weise können Sie auf Kundendaten zugreifen, die in Data Warehouses und Cloud-Speicherplattformen wie Amazon Redshift und Azure Synapse Analytics gespeichert sind.

## Funktionen {#rn-capabilities}

Die Komposition föderierter Zielgruppen steigert den Wert von Real-Time CDP und Adobe Journey Optimizer mit einem umfassenden Ansatz für die Kuration und Aktivierung von Zielgruppen:

* **Erweitern Sie den Zugriff auf wichtige Warehouse-basierte Datensätze, um hochwertige Zielgruppen zu erstellen**: Sie können vorhandene Data Warehouses als Hauptsystem für Aufzeichnungen verwenden und gleichzeitig branchenführende Anwendungen nutzen, um herausragende Kundenerlebnisse zu schaffen.

* **Umfassende Unterstützung für Anwendungsfälle zur Förderung von Interaktionen**: Die Federated Audience Composition in Kombination mit Real-Time CDP oder Journey Optimizer unterstützt markeninitiierte, personalisierte Erlebnisse mit verbundenen Zielgruppen und liefert sofort einsetzbare Erlebnisse, die durch Echtzeit-Ereignisse ausgelöst werden. Diese Erlebnisse werden mit Personenattributen kombiniert, um Anwendungsfallanforderungen in allen Teams zu erfüllen.

* **Minimieren von Datenverschiebung und Duplizierung**: Sie können Zielgruppen aus Datensätzen erstellen, die sich in Data Warehouses eines Unternehmens befinden, ohne die zugrunde liegenden Daten zu kopieren, um verwertbare Marketing-Profile und Zielgruppen zu verwalten.

* **Nutzen eines einzigen Systems für erlebnisgesteuerte Workflows**: Sie können sowohl aufgenommene als auch zusammengeführte Zielgruppen in Adobe Experience Platform kuratieren und ausgehende Erlebnisse kanalübergreifend koordinieren.

* **Unterstützung mehrerer Editionen**: B2C- und B2B-CDP-Kunden können Federated Audience Composition nutzen, um personenbasierte Zielgruppen zu erstellen, indem sie Daten aus unterstützten Unternehmens-Data Warehouses integrieren. Darüber hinaus können sie bestehende, personenbasierte Zielgruppen von Experience Platform anreichern, indem sie relevante Attribute, die im Enterprise Data Warehouse verfügbar sind, integrieren und so ihre Zielgruppenprofile verbessern, um eine personalisiertere und zielgerichtetere Interaktion zu ermöglichen.

## Anwendungsfälle {#use-cases}

Die Komposition föderierter Zielgruppen unterstützt **drei** Kategorien von Anwendungsfällen: Zielgruppenerstellung, Zielgruppenanreicherung und Kundenprofilanreicherung.

* **Zielgruppenerstellung**: Sie können Zielgruppen aus einem Data Warehouse erstellen und diese Zielgruppen zur Verwendung in Real-Time CDP oder Journey Optimizer über eine marketerfreundliche Drag-and-Drop-Benutzeroberfläche in Experience Platform zusammenführen. Infolgedessen können Sie Ihre Data Warehouses abfragen, ohne vertrauliche zugrunde liegende Daten zu kopieren oder vorhandene Daten zu duplizieren.
   * **Beispiel:** Erstellen Sie eine Zielgruppe mit Personen, die in der Vergangenheit zu hohen Beträgen eingekauft haben, indem Sie historische Transaktionsdaten im Warehouse verwenden, ohne diese Transaktionen nach Experience Platform zu kopieren.

* **Zielgruppenanreicherung**: Sie können Ihren bestehenden Zielgruppen in Experience Platform weitere Details hinzufügen, indem Sie zusätzliche Datensätze aus Ihren Data Warehouses verwenden und Ihre Zielgruppen mit diesen Informationen überlagern - und das alles, ohne die zugrunde liegenden Daten in Experience Platform zu kopieren. Über die Zielgruppenanreicherung können Sie mit der angereicherten Zielgruppe verbesserte Personalisierung bereitstellen.
   * **Beispiel:** Eine Experience Platform-Zielgruppe mit Personen mit abgebrochenem Warenkorb können Sie mit der Zielgruppe aus der Komposition föderierter Zielgruppen mit Personen anreichern, die in der Vergangenheit zu hohen Beträgen eingekauft haben, um ein zielgerichtetes Angebot zu unterbreiten.

* **Profilanreicherung**: Sie können einzelne Kundenattribute aus Ihrem Data Warehouse auswählen, um Experience Platform-Profile zu verbessern. Durch das Hinzufügen von föderierten Daten zu diesen Profilen können Sie aktuelle Erlebnisse optimieren, die durch eingehende Kundensignale ausgelöst werden.
   * **Beispiel:** Reichern Sie ein Experience Platform-Profil mit Informationen aus der föderierten Zielgruppe an. Sie können jetzt Site-Besuchende anwerben, die zu der Zielgruppe mit Personen gehören, die in der Vergangenheit zu hohen Beträgen einkauft haben. Sie können diesen ein zielgerichtetes Angebot unterbreiten, das durch ihr Verhalten auf der Site ausgelöst wird.

![Diagramm](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Weitere Informationen zu Anwendungsfällen für die Komposition föderierter Zielgruppen finden Sie im [Whitepaper zur Komposition föderierter Zielgruppen](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Die wichtigsten Schritte {#gs-steps}

Mit der Komposition föderierter Zielgruppen von Adobe können Sie Adobe Experience Platform-Zielgruppen direkt aus Ihrer Datenbank erstellen und aktualisieren, ohne dass ein Aufnahmevorgang erforderlich ist.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **Verbindung erstellen**: Daten aus verschiedenen Quellen zusammenführen und zu einem einheitlichen Datensatz zusammenführen. Weitere Informationen zum Verbinden von Adobe Experience Platform-Apps mit Ihrem Unternehmens-Data Warehouse, zu unterstützten Datenbanken und zum Konfigurieren Ihrer Verbindung finden Sie im Abschnitt [Verbindungen - Übersicht](./connections/home.md).

2. **Daten modellieren**: Entwerfen und erstellen Sie Schemata und Datenmodelle, die die Struktur, Beziehungen und Einschränkungen der Daten definieren. Weitere Informationen zu Schemata finden Sie unter [Schemaübersicht](./data-modelling/schemas.md). Weitere Informationen zu Datenmodellen finden Sie unter [Datenmodellübersicht](./data-modelling/models.md).

3. **Daten transformieren**: Wenden Sie Datenmanipulationstechniken an, um das Format, die Struktur oder die Werte von Datenelementen zu ändern, damit sie kompatibel oder für bestimmte Analysen oder Anwendungen geeignet sind.

4. **Zielgruppe erstellen**: Erstellen, orchestrieren und erstellen Sie Zielgruppen. Weitere Informationen zum Erstellen von Zielgruppen finden Sie im Abschnitt [Übersicht über die Komposition](./compositions/home.md). Sie können vorhandene Zielgruppen auch über das Zielgruppenportal und die Ziele von Adobe Experience Platform aktualisieren oder wiederverwenden. Weitere Informationen finden Sie auf [dieser Seite](./connections/destinations.md).

>[!NOTE]
>
>Nach der Ausführung der Komposition wird die resultierende Zielgruppe in Adobe Experience Platform als externe Zielgruppe gespeichert und in Adobe Real-Time Customer Data Platform und/oder Adobe Journey Optimizer zur Verfügung gestellt. Sie wird im Menü **Zielgruppen** zur Verfügung gestellt. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Verwaltung, Datenschutz und Sicherheit {#governance-privacy-security}

### Datenschutzanfragen {#gov-privacy-requests}

Nachdem Sie eine Komposition erstellt haben, werden die resultierenden Zielgruppen in Adobe Experience Platform gespeichert.

Anschließend können Sie Datenschutzanfragen stellen, um auf Profildaten, die diesen Zielgruppen entsprechen, zuzugreifen und/oder sie zu löschen. Verwenden Sie dazu Adobe Experience Platform **Privacy Service**, das eine [Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de){target="_blank"} und ein [RESTful-API](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/api/overview){target="_blank"} bereitstellt, um Sie bei der Verwaltung von Kundendatenanfragen zu unterstützen.

>[!NOTE]
>
>Weitere Informationen zu Privacy Service finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de){target="_blank"}.

Sie können individuelle Anfragen für den Zugriff auf und die Löschung von Kundendaten aus der Komposition föderierter Zielgruppen von Adobe erstellen und verwalten. Die Schritte zum Senden von **Zugriffsanfragen** und **Löschanfragen** werden in der [Dokumentation zum Echtzeit-Kundenprofil](https://experienceleague.adobe.com/de/docs/experience-platform/profile/privacy){target="_blank"} beschrieben.

### Audit-Protokoll {#gov-audit-trail}

Die Funktion „Audit-Protokoll“ bietet eine detaillierte und chronologische Aufzeichnung aller Aktionen und Ereignisse, die in Echtzeit in Ihrer Umgebung durchgeführt wurden. Weitere Informationen zum Audit-Protokoll finden Sie im Abschnitt [Audit-Protokoll - Übersicht](./admin/audit-trail.md).

## Weitere Informationen {#learn}

<!-- Workflow + Workflow activities-->

Auf [dieser Seite](./start/access-prerequisites.md) erfahren Sie, wie Sie auf die Funktion „Komposition föderierter Zielgruppen“, Leitlinien und Einschränkungen zugreifen können.

Antworten auf häufig gestellte Fragen finden Sie unter [Häufig gestellte Fragen zur Federated Audience &#x200B;](./faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Ausführungseinstellungen"
>abstract="In diesem Abschnitt können Sie Einstellungen für die Ausführung des Workflows konfigurieren, z. B. die Anzahl der Tage, die der Kompositionsverlauf gespeichert wird."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Aktivität nicht bearbeitbar"
>abstract="Wenn eine **Abfrage** oder **Anreicherung** mit zusätzlichen Daten in der Konsole konfiguriert wird, werden die Anreicherungsdaten berücksichtigt und an die ausgehende Transition übergeben. Sie können jedoch nicht bearbeitet werden."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Link erstellen"
>abstract="Die Link-Einstellungen definieren."


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Inkrementelle Abfrage"
>abstract="Mit der Aktivität **Inkrementelle Abfrage** können Sie die Datenbank mithilfe des Abfrage-Modelers abfragen. Bei jeder neuen Ausführung dieser Aktivität werden die Ergebnisse der vorangehenden Ausführungen ausgeschlossen. Dadurch lassen sich ausschließlich neue Elemente abrufen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Inkrementeller Abfrageverlauf"
>abstract="Inkrementeller Abfrageverlauf"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Inkrementelle Abfrage – Verarbeitete Daten"
>abstract="Inkrementelle Abfrage – Verarbeitete Daten"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="Modus „Inkrementelle Abfrage“"
>abstract="Die inkrementelle Abfrage ermöglicht es Ihnen, dieselbe Abfrage mehrmals auszuführen, indem die Ergebnisse früherer Ausführungen für jede neue Ausführung ausgeschlossen werden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Modus „Inkrementelle Abfrage“"
>abstract="Die inkrementelle Abfrage ermöglicht es Ihnen, dieselbe Abfrage mehrmals auszuführen, indem nur die Ergebnisse berücksichtigt werden, bei denen das Datum im Datumsfeld nach oder an dem Datum der letzten Ausführung der inkrementellen Abfrage liegt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Auswählen der Zielgruppendimension"
>abstract="Die Zielgruppendimension ermöglicht die Bestimmung der vom Vorgang betroffenen Population: Empfängerinnen und Empfänger, Vertragsbegünstigte, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw. Standardmäßig wird die Zielgruppe für E-Mails und SMS in der integrierten Tabelle der Empfängerinnen und Empfänger ausgewählt. Bei Push-Benachrichtigungen ist die Standard-Zielgruppendimension „Abonnierte Anwendungen“."

