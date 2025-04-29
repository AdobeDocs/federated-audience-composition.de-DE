---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zur Komposition föderierter Zielgruppen in Adobe Experience Platform
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: ht
source-wordcount: '897'
ht-degree: 100%

---

# Häufig gestellte Fragen {#faq}

Im Folgenden finden Sie eine Liste häufig gestellter Fragen zur Komposition föderierter Zielgruppen in Adobe Experience Platform. Außerdem finden Sie global häufig gestellte Fragen für den Segmentierungs-Service von Adobe Experience Platform auf [dieser Seite](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Welche Berechtigungen sind für den Zugriff auf die Komposition föderierter Zielgruppen erforderlich?

Die Komposition föderierter Zielgruppen erfordert Adobe Real-Time Customer Data Platform und/oder die Pakete „Prime“ oder „Ultimate“ von Adobe Journey Optimizer. Sie müssen außerdem die Komposition föderierter Zielgruppen erworben haben.

Um die Komposition föderierter Zielgruppen verwenden zu können, muss jede Benutzerin und jeder Benutzer einem spezifischen Profil hinzugefügt werden, das für jede Sandbox erstellt wurde. Weitere Informationen finden Sie auf der Seite [Zugriff auf die Komposition föderierter Zielgruppen](access-prerequisites.md).

+++

+++Welche Cloud-Warehouses werden unterstützt?

Die Liste der für die Komposition föderierter Zielgruppen unterstützten Systeme finden Sie auf [dieser Seite](../start/access-prerequisites.md#supported-systems).

+++


+++Können mehrere Data Warehouses in derselben Komposition abgefragt werden?

Ja, es können mehrere Warehouses in derselben Komposition abgefragt und Daten aus mehreren Quellen kombiniert werden. In der Regel führt jede [Kompositionsaktivität](../compositions/orchestrate-activities.md) (Abfrage, Anreicherung, Aufspaltung usw.) eine oder mehrere SQL-Anweisungen je nach Konfiguration der Aktivität und je nach Zieldatenbanken aus (es kann mehrere Fälle von föderiertem Datenzugriff geben) und gibt eine oder mehrere Arbeitstabellen mit dem Ergebnis der Ausführung aus. Diese Arbeitstabellen werden als Eingabe für aufeinander folgende Aktivitäten verwendet.

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

+++Kann ich eine Zielgruppe löschen?

Nein, in der aktuellen Version können Sie keine Zielgruppen der Komposition föderierter Zielgruppen löschen.

+++

+++Wie werden Daten zusammengeführt, wenn ich die Daten aus mehreren Quellen kombiniere? Wird Identity Service dafür verwendet?

Nein, Identity Service wird während einer Komposition nicht genutzt. Die Daten zwischen den verschiedenen in der Komposition verwendeten Quellen werden durch eine benutzerdefinierte Logik verbunden (wie im zugrunde liegenden Modell ausgedrückt), z. B. CRM-ID, Benutzerkontonummer usw. Sie müssen die Identität, die als Kennung in der Zielgruppe verwendet wird, für die Auswahl in Ihrem Data Warehouse auswählen. Bei einer aus der Komposition föderierter Zielgruppen resultierenden Zielgruppe müssen Sie den Identity-Namespace für die Identität im resultierenden Datensatz identifizieren.

+++

+++Wie erstelle und verwalte ich Datenschutzanfragen mit der Komposition föderierter Zielgruppen?

Sie können individuelle Anfragen zum Zugriff auf und Löschen von Verbraucherdaten aus der Komposition föderierter Zielgruppen von Adobe auf zwei Arten senden:

* Über die **Privacy Service-Benutzeroberfläche** von Adobe Experience Platform. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de){target="_blank"}
* Über das **Privacy Service-API** von Adobe Experience Platform. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/api/overview){target="_blank"}

Alle Schritte zum Erstellen und Verwalten von **Zugriffs**- und **Löschanfragen** werden in der [Dokumentation zum Echtzeit-Kundenprofil](https://experienceleague.adobe.com/de/docs/experience-platform/profile/privacy){target="_blank"} beschrieben.

+++

<!--
+++How are customer consent preferences honored for externally generated audiences that are imported into Federated Audience Composition?

As customer data is captured from multiple channels, identity stitching and merge policies allow this data to be consolidated in a single Real-Time Customer Profile. Information on the customers' consent preferences are stored and evaluated at the profile level.

Downstream Real-Time CDP and Journey Optimizer destinations check each profile for consent preferences prior to activation. Each profile's consent information is compared against consent requirements for a particular destination. If the profile does not satisfy the requirements, that profile is not sent to a destination.

When an external audience is ingested into Federated Audience Composition, it is reconciliated with existing profiles using a primary ID such as email or ECID. As a result, the existing consent policies will remain in force throughout activation.

>[!NOTE]
>
>Since the payload variables are not stored in the profile but in the data lake, you should not include consent information in externally generated audiences. Instead, use other Adobe Experience Platform ingestion channels where profile data is imported.

+++
-->
