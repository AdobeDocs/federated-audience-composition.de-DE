---
title: Berechtigungen für den Zugriff auf eine externe Datenbank
description: Erfahren Sie mehr über die spezifischen Berechtigungen der einzelnen Datenbank-Engines
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 46%

---

# FDA-Rechtematrix {#fda-rights}

In der folgenden Tabelle sind die erforderlichen Datenbankberechtigungen für jedes System aufgeführt, sodass Benutzer über FDA Vorgänge für externe Datenbanken ausführen können.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Berechtigungen USAGE ON WAREHOUSE, USAGE ON DATABASE und USAGE ON SCHEMA | Erstellen eines mit dem AWS-Konto verknüpften Benutzers | Erstellen eines Service-Kontos und Gewähren des Prinzipalzugriffs auf das Projekt | USE CATALOG privileges on Catalog und CAN_USE privileges on SQL Warehouse |
| **Erstellen von Tabellen** | Berechtigung CREATE TABLE ON SCHEMA | Berechtigung CREATE | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.tables.create-Berechtigungen | SCHEMA-Berechtigung und CREATE TABLE-Berechtigung verwenden |
| **Erstellen von Indizes** | K. A. | Berechtigung CREATE | BigQuery unterstützt nur Suchindizes. Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create, bigquery.tables.getData und bigquery.tables.createIndex-Berechtigungen | K. A. |
| **Erstellen von Funktionen** | Berechtigung CREATE FUNCTION ON SCHEMA | Berechtigung USAGE ON LANGUAGE plpythonu, um externe Python-Skripte aufrufen zu können | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.routines.create-Berechtigungen | Berechtigung CREATE FUNCTION |
| **Erstellen von Verfahren** | K. A. | Berechtigung USAGE ON LANGUAGE plpythonu, um externe Python-Skripte aufrufen zu können | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.routines.create-Berechtigungen |  Nicht zutreffend |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | Eigentümer des Objekts | Eigentümer des Objekts oder Superuser | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete und bigquery.tables.deleteIndex-Berechtigungen |
| **Überwachen von Ausführungen** | Berechtigung MONITOR für das erforderliche Objekt | Keine Berechtigung erforderlich, um den Befehl EXPLAIN zu verwenden | monitoring.viewer.role | CAN_VIEW-Berechtigung |
| **Schreiben von Daten** | Berechtigungen INSERT und/oder UPDATE (je nach Schreibvorgang) | Berechtigungen INSERT und UPDATE | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.tables.updateData |  BERECHTIGUNG ÄNDERN |
| **Laden von Daten in Tabellen** | Berechtigungen CREATE STAGE ON SCHEMA, SELECT und INSERT für die Zieltabelle | Berechtigungen SELECT und INSERT | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create, bigquery.tables.getData und bigquery.tables.updateData | SELECT and MODIFY privileges |
| **Zugreifen auf Client-Daten** | Berechtigungen SELECT für (FUTURE) TABLE(S) oder VIEW(S) | Berechtigung SELECT | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.tables.getData für Tabellen oder bigquery.dataViewer-Rolle |  Berechtigung AUSWÄHLEN |
| **Zugreifen auf Metadaten** | Berechtigung SELECT für INFORMATION_SCHEMA SCHEMA | Berechtigung SELECT | bigquery.metadataViewer-Rolle |  SELECT on INFORMATION_SCHEMA privilege |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Leseberechtigung (Standard) | Berechtigung CONNECT | Keine Berechtigung erforderlich |
| **Erstellen von Tabellen** | TABELLE IN DATENBANK (Warehouse) ERSTELLEN UND SCHEMA ÄNDERN | Berechtigung CREATE TABLE | Berechtigung ERSTELLEN BEI SCHEMA |
| **Erstellen von Indizes** | K. A. | Berechtigung ALTER | K. A. |
| **Erstellen von Funktionen** | K. A. | Berechtigung CREATE FUNCTION | Berechtigung ERSTELLEN BEI SCHEMA |
| **Erstellen von Verfahren** | ERSTELLEN EINES VORGANGS IN EINER DATENBANK (Warehouse) UND ÄNDERN EINES SCHEMAS | Berechtigung CREATE PROCEDURE | Berechtigung ERSTELLEN BEI SCHEMA |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | SCHEMA ÄNDERN | Berechtigung ALTER | Besitz des Objekts oder der DROP-Berechtigung für ein Objekt |
| **Überwachen von Ausführungen** | Mitwirkende an Workspace oder höhere Berechtigungen (queryinsights.exec_requests_history)  | BERECHTIGUNG ZUR KONTROLLE | Zur Verwendung der EXPLAIN-Anweisung ist keine Berechtigung erforderlich |
| **Schreiben von Daten** | EINFÜGEN UND/ODER AKTUALISIEREN EINES OBJEKTS | Berechtigungen INSERT und UPDATE | Berechtigungen INSERT und UPDATE |
| **Laden von Daten in Tabellen** | SELECT ON OBJECT und INSERT ON OBJECT | ERSTELLEN EINER TABELLE, AUSFÜHREN, AUSWÄHLEN, EINFÜGEN, AKTUALISIEREN, ÄNDERN VON BERECHTIGUNGEN | INSERT-Berechtigung für Tabelle, USAGE-Berechtigung für Schema |
| **Zugreifen auf Client-Daten** | OBJEKT AUSWÄHLEN | Berechtigung SELECT | Berechtigung SELECT |
| **Zugreifen auf Metadaten** | WÄHLEN SIE EIN INFORMATIONS-SCHEMA AUS | Keine Berechtigung zur Beschreibung der Tabelle erforderlich | VERWENDUNG IM SCHEMA, SELECT ON TABLE und auch Berechtigungen für die Tabellen v_catalog.columns und v_catalog.view_columns |
