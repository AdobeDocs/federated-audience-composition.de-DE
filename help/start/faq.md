---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zur Komposition föderierter Zielgruppen in Adobe Experience Platform
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: dd19c6a8170a87c10fd8534bf2aa63adcf360529
workflow-type: ht
source-wordcount: '834'
ht-degree: 100%

---

# Häufig gestellte Fragen {#faq}

Im Folgenden finden Sie eine Liste häufig gestellter Fragen zur Komposition föderierter Zielgruppen in Adobe Experience Platform. Außerdem finden Sie global häufig gestellte Fragen für den Segmentierungs-Service von Adobe Experience Platform auf [dieser Seite](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Welche Berechtigungen sind für den Zugriff auf die Komposition föderierter Zielgruppen erforderlich?

Die Komposition föderierter Zielgruppen erfordert Adobe Real-Time Customer Data Platform und/oder die Pakete „Prime“ oder „Ultimate“ von Adobe Journey Optimizer. Sie müssen außerdem das Add-on „Komposition föderierter Zielgruppen“ erworben haben.

Um die Komposition föderierter Zielgruppen verwenden zu können, muss jede Benutzerin und jeder Benutzer einem spezifischen Profil hinzugefügt werden, das für jede Sandbox erstellt wurde. Weitere Informationen finden Sie auf der Seite [Zugriff auf die Komposition föderierter Zielgruppen](access-prerequisites.md).

+++

+++Welche Cloud-Warehouses werden unterstützt?

In dieser Version ist die Komposition föderierter Zielgruppen kompatibel mit:

* Amazon Redshift
* Azure Synapse
* Google BigQuery
* Snowflake
* Vertica Analytics

+++


+++Können mehrere Data Warehouses in derselben Komposition abgefragt werden?

Ja, es können mehrere Warehouses in derselben Komposition abgefragt und Daten aus mehreren Quellen kombiniert werden. In der Regel führt jede [Kompositionsaktivität](../compositions/orchestrate-activities.md) (Abfrage, Anreicherung, Aufspaltung) je nach Konfiguration der Aktivität eine oder mehrere SQL-Anweisungen aus (es kann mehrere Fälle von föderiertem Datenzugriff geben) und gibt eine oder mehrere Arbeitstabellen mit dem Ergebnis der Ausführung aus. Diese Arbeitstabellen werden als Eingabe für aufeinander folgende Aktivitäten verwendet.

+++

+++ Kann ich mit der Komposition föderierter Zielgruppen auf meine gesamte Datenbank zugreifen?

Nein, es liegt an Ihnen, den Zugriff auf eine dedizierte oder freigegebene Datenbank oder ein dediziertes Schema zu konfigurieren. Es wird empfohlen, ein dediziertes Schema für die Komposition föderierter Zielgruppen zu erstellen und nur Business-Case-Datensätze zu kopieren/freizugeben.
+++



+++Habe ich Zugriff auf alle Tabellen im dedizierten Schema?

Ja. Nach der Verbindung können Sie die Komposition föderierter Zielgruppen verwenden, um alle Tabellen basierend auf den anfänglich definierten Berechtigungen zu ermitteln. Anschließend können Sie den visuellen Schema-Editor für Folgendes verwenden:

* Ermitteln von Spalten und Primärschlüssel aus Ihren Tabellen
* Erstellen benutzerfreundlicher Bezeichnungen für diese Tabellen
* Erstellen benutzerfreundlicher Anzeigenamen für jede Spalte
* Ausblenden unnötiger Spalten
* Speichern dieser Tabellenbeschreibung
+++


+++Gibt in der Komposition föderierter Zielgruppen eine temporäre Speicherung?

Nein. Die Komposition föderierter Zielgruppen speichert nur Metadaten (Schemabeschreibungen). Es werden keine Kundendaten übermittelt. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++Speichert die Komposition föderierter Zielgruppen eine physische Kopie dieser Liste von Personen, um sie an nachgelagerte Systeme zu senden?

Bei der Komposition föderierter Zielgruppen wird keine physische Kopie der Daten gespeichert. In der Komposition wird festgelegt, wie häufig diese Daten aktualisiert werden. Die daraus resultierenden Daten der Zielgruppe werden von Adobe Experience Platform nicht länger gespeichert, als es für die Anwendungsfälle oder die Aktion des Kunden erforderlich ist.

Zum Beispiel:

* Im Fall einer Zielgruppenerstellung wird die Zielgruppe in Ihrem Warehouse erstellt. Sie können die Komposition föderierter Zielgruppen für zusätzliche Kompositionsaufgaben und Datenmanipulationen verwenden, bevor Sie die resultierende Zielgruppe und die zugehörigen Attribute über das Zielgruppenportal von Adobe Experience Platform veröffentlichen. Die Zielgruppendefinition und die zugehörigen Attribute werden an Adobe Experience Platform übergeben.
Beachten Sie, dass die Gültigkeit der Daten für extern generierte Zielgruppen derzeit 30 Tage beträgt. Dadurch wird die Menge an überschüssigen Daten, die in einer Organisation gespeichert werden, reduziert. Nach Ablauf der Gültigkeitsdauer der Daten ist der zugehörige Datensatz weiterhin im Datensatzbestand sichtbar, Sie können die Zielgruppe jedoch nicht aktivieren und die Profilanzahl wird als null angezeigt. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* Der Ausgangspunkt einer Zielgruppenanreicherung ist eine vorhandene Adobe Experience Platform-Zielgruppe. Hier sind zwei Szenarien denkbar:
   1. Fügen Sie zusätzliche Zielgruppen-Payload-Attribute aus dem föderierten Data Warehouse hinzu: In diesem Fall werden die zusätzlichen hinzugefügten Attribute als Teil dieser Zielgruppendefinition übernommen. Die Gültigkeit der Daten für extern generierte Zielgruppen ist dieselbe wie oben beschrieben, nämlich 30 Tage.
   1. Verfeinern Sie die bestehende Adobe Experience Platform-Zielgruppe anhand zusätzlicher Attribute, die in Ihrem Data Warehouse vorhanden sind. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Wie werden die Daten der Anwendungsfälle für Zielgruppenerstellung und Zielgruppenanreicherung zwischengespeichert, wenn sie nicht persistiert werden?

Die resultierenden Zielgruppendaten werden nicht unbegrenzt in Adobe Experience Platform oder in der Komposition föderierter Zielgruppen persistiert. Sie werden nicht länger aufbewahrt als für Ihren Anwendungsfall erforderlich. Als Teil der Zielgruppen-Payload hinzugefügte Zielgruppenattribute werden nur als Teil der Zielgruppendefinition persistiert. Die Dauer der Persistenz hängt von der Gültigkeitsdauer für jede Zielgruppe ab, die Standardeinstellung beträgt 30 Tage.

+++

+++Kann ich eine hochgeladene benutzerdefinierte Zielgruppe löschen?

Nein, in der aktuellen Version können Sie hochgeladene benutzerdefinierte Zielgruppen nicht löschen. <!--that are not used in downstream activation directly in Audience Portal by simply selecting delete from the actions menu. Learn more in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.-->

+++

+++Wie werden Daten zusammengeführt, wenn ich die Daten aus mehreren Quellen kombiniere? Wird Identity Service dafür verwendet?

Nein, Identity Service wird während einer Komposition nicht genutzt. Die Daten zwischen den verschiedenen in der Komposition verwendeten Quellen werden durch eine benutzerdefinierte Logik verbunden (wie im zugrunde liegenden Modell ausgedrückt), z. B. CRM-ID, Benutzerkontonummer usw. Sie müssen die Identität, die als Kennung in der Zielgruppe verwendet wird, für die Auswahl in Ihrem Data Warehouse auswählen. Bei einer aus der Komposition föderierter Zielgruppen resultierenden Zielgruppe müssen Sie den Identity-Namespace für die Identität im resultierenden Datensatz identifizieren.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
