---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 6cfd3bd85d7811e00e716042502c7d7b23fa4ad9
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 3%

---


# Häufig gestellte Fragen {#faq}

Im Folgenden finden Sie eine Liste häufig gestellter Fragen zur Zusammenstellung von Federated Audience. Globale FAQs sind auch für den Adobe Experience Platform Segmentation Service auf [dieser Seite](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"} verfügbar.


++ Welche Berechtigungen sind für den Zugriff auf Federated Audience Komposition erforderlich?

Es gibt keine spezifischen Berechtigungen für die Zusammenstellung von Federated Audience. Die einzige Voraussetzung für den Zugriff auf diese Funktion ist der Kauf des Add-ons &quot;Federated Audience Komposition&quot;.

+++

++ Welche Cloud-Warehouse werden unterstützt?

Für diese Version ist die Zusammenstellung von Federated Audience mit folgenden Versionen kompatibel:

* Amazon Redshift
* Azure synapse
* Google BigQuery
* Snowflake
* Vertica Analytics

+++


+++ Können mehrere Data Warehouse-Abfragen in derselben Komposition durchgeführt werden?

Ja, mehrere Lagerhäuser können in derselben Zusammensetzung abgefragt werden und Daten aus mehreren Quellen kombinieren.  In der Regel wird jede [Kompositionsaktivität](../compositions/orchestrate-activities.md) (Abfrage, Anreicherung, Aufspaltung usw.) führt je nach Aktivitätskonfiguration, Zieldatenbanken (es kann mehrere Fälle von Federated Data Access geben) eine oder mehrere SQL-Anweisungen aus und gibt eine oder mehrere Arbeitstabellen mit dem Ergebnis der Ausführung aus. Diese Arbeitstabellen werden als Eingabe für aufeinander folgende Aktivitäten verwendet.

+++

+++ Kann ich mit Federated Audience Komposition auf meine gesamte Datenbank zugreifen?

Nein, es liegt an Ihnen, den Zugriff auf eine dedizierte oder freigegebene Datenbank/ein dediziertes Schema zu konfigurieren. Es wird empfohlen, ein dediziertes Schema für die Zusammenstellung von Federated Audience zu erstellen und nur Geschäftsfalldatensätze zu kopieren/freizugeben.
+++



+++ Habe ich Zugriff auf alle Tabellen im dedizierten Schema?

Ja, nach der Verbindung können Sie die Zusammenstellung von Federated Audience verwenden, um alle Tabellen basierend auf den definierten anfänglichen Berechtigungen zu ermitteln. Anschließend können Sie den visuellen Schema-Editor verwenden, um:

* Spalten und Primärschlüssel aus Ihren Tabellen
* Benutzerfreundliche Beschriftungen für diese Tabellen erstellen
* Anzeigenamen für jede Spalte erstellen
* Ausblenden unnötiger Spalten
* Diese Tabellenbeschreibung speichern
+++


++ Gibt es temporären Speicher in der Zusammenstellung von Federated Audience?

Nein, Zusammengestellte Zielgruppenkomposition speichert nur Metadaten (Schemabeschreibungen). Es werden keine Kundendaten übermittelt. Der Zielgruppenexport erfolgt direkt aus Adobe Experience Platform Audience Portal (über [Ziel](../connections/destinations.md)) zur Kundendatenbank. Der Erstellungs- und Aktualisierungsfluss erfolgt direkt von Ihrer Data Warehouse-Datenbank zu Adobe Experience Platform Audience Portal.

+++

+ + + Speichert Federated Audience Komposition eine physische Kopie dieser Personenliste, die an nachgelagerte Systeme gesendet werden soll?

Zusammengestellte Zielgruppen Komposition verwaltet keine physische Kopie der Daten. Die Häufigkeit wird in der Komposition konfiguriert, um festzulegen, wie häufig diese Daten aktualisiert werden. Die resultierenden Zielgruppendaten werden von Adobe Experience Platform nicht länger gespeichert, als es für die Anwendungsfälle oder die Aktion des Kunden erforderlich ist.

Beispiel:

* Im Fall einer Zielgruppensegmentierung wird die Zielgruppe in Ihrem Warehouse erstellt. Sie können die Federated Audience-Komposition für zusätzliche Kompositionsaufgaben und Datenmanipulationen verwenden, bevor Sie die resultierende Zielgruppe und die zugehörigen Attribute über Adobe Experience Platform Audience Portal veröffentlichen. Die Zielgruppendefinition und die zugehörigen Attribute werden an Adobe Experience Platform übergeben.
Beachten Sie, dass die aktuelle Datengültigkeit für extern generierte Zielgruppen 30 Tage beträgt. Diese Datengültigkeit reduziert die Menge an überschüssigen Daten, die in einer Organisation gespeichert sind. Nach Ablauf des Datenablaufzeitraums ist der verknüpfte Datensatz weiterhin im Datensatzbestand sichtbar, Sie können die Zielgruppe jedoch nicht aktivieren, und die Profilanzahl wird als null angezeigt. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* Bei einer Zielgruppen-Anreicherung ist der Ausgangspunkt eine bestehende Adobe Experience Platform-Zielgruppe. Hier können Sie zwei Szenarien betrachten:
   1. Fügen Sie zusätzliche Zielgruppen-Payload-Attribute aus dem Federated Data Warehouse hinzu: In diesem Fall werden die zusätzlichen Attribute, die hinzugefügt werden, als Teil dieser Zielgruppendefinition übernommen. Der Datenablauf für extern generierte Zielgruppen entspricht dem oben beschriebenen 30 Tage.
   1. Optimieren Sie die vorhandene Adobe Experience Platform-Zielgruppe auf der Grundlage zusätzlicher Attribute, die in Ihrem Data Warehouse vorhanden sind. Sie haben beispielsweise eine Zielgruppe von Kunden, die in den letzten zwei Monaten Interesse an einem bestimmten Produkt auf der Website gezeigt haben. Sie möchten diese Zielgruppe nun mithilfe der Federated Audience-Komposition weiter segmentieren und nur Kunden mit einem hohen Bonitätswert einbeziehen. Der Kreditwert wird als vertraulich betrachtet und einzelne Kreditwürdigkeit-Datenpunkte werden nicht aus dem Data Warehouse kopiert.
+++

+++ Wenn die Anwendungsfälle für Zielgruppensegmentierung und Zielgruppeneranreicherung nicht persistiert werden, wie werden sie dann vorübergehend gespeichert?

Die resultierenden Zielgruppendaten bleiben nicht unbegrenzt in Adobe Experience Platform oder in der Zusammenstellung von Federated Audience erhalten. Er wird nicht länger aufbewahrt als für Ihren Anwendungsfall erforderlich. Die Zielgruppenattribute, die als Teil der Zielgruppen-Payload übermittelt werden, bleiben nur als Teil der Zielgruppendefinition erhalten. Die Dauer der Persistenz basiert für jede Zielgruppe auf TTL. Die Standardeinstellung ist 30 Tage.

+++

+++ Kann ich eine benutzerdefiniert hochgeladene Zielgruppe löschen?

Sie können Zielgruppen, die nicht in der nachgelagerten Aktivierung verwendet werden, direkt in Audience Portal löschen, indem Sie einfach im Aktionsmenü die Option Löschen auswählen. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.

+++

+++ Wenn ich Daten aus mehreren Quellen kombiniere, wie werden die Daten zusammengeführt? Verwenden wir den Identity-Dienst?

Nein, Identity Service wird während einer Komposition nicht genutzt. Die Daten zwischen den verschiedenen in der Komposition verwendeten Quellen werden durch eine benutzerdefinierte Logik verbunden (wie im zugrunde liegenden Modell ausgedrückt), z. B. CRM-ID, Benutzerkontonummer usw. Sie müssen die Identität auswählen, die als Kennung in der Zielgruppe zur Auswahl in Ihrem Data Warehouse verwendet wird. Bei einer resultierenden Zielgruppe aus Federated Audience Komposition müssen Sie den Identitäts-Namespace für die Identität im resultierenden Datensatz identifizieren.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->