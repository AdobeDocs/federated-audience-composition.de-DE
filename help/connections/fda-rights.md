---
title: Berechtigungen für den Zugriff auf externe Datenbanken
description: Erfahren Sie mehr über die spezifischen Rechte für die einzelnen Datenbank-Engines
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: f778f3367c5e19a3052e1055005b6c84f3a55a57
workflow-type: ht
source-wordcount: '560'
ht-degree: 100%

---

# Matrix der FDA-Berechtigungen {#fda-rights}

In der folgenden Tabelle sind die erforderlichen Datenbankberechtigungen für jedes System aufgeführt, sodass Benutzende über FDA Vorgänge für externe Datenbanken ausführen können.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Berechtigungen USAGE ON WAREHOUSE, USAGE ON DATABASE und USAGE ON SCHEMA | Erstellen eines mit dem AWS-Konto verknüpften Benutzers | Erstellen eines Dienstkontos und Gewähren von Hauptzugriff auf das Projekt | Berechtigung USE CATALOG für Katalog und Berechtigung CAN_USE für SQL-Warehouse |
| **Erstellen von Tabellen** | Berechtigung CREATE TABLE ON SCHEMA | Berechtigung CREATE | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create- und bigquery.tables.create-Berechtigungen | Berechtigungen USE SCHEMA und CREATE TABLE |
| **Erstellen von Indizes** | K. A. | Berechtigung CREATE | BigQuery unterstützt nur Suchindizes. Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create-, bigquery.tables.getData- und bigquery.tables.createIndex-Berechtigungen | K. A. |
| **Erstellen von Funktionen** | Berechtigung CREATE FUNCTION ON SCHEMA | Berechtigung USAGE ON LANGUAGE plpythonu, um externe Python-Skripte aufrufen zu können | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create- und bigquery.routines.create-Berechtigungen | Berechtigung CREATE FUNCTION |
| **Erstellen von Verfahren** | K. A. | Berechtigung USAGE ON LANGUAGE plpythonu, um externe Python-Skripte aufrufen zu können | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create- und bigquery.routines.create-Berechtigungen |  K. A. |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | Eigentümer des Objekts | Eigentümer des Objekts oder Superuser | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create-, bigquery.routines.delete-, bigquery.tables.delete- und bigquery.tables.deleteIndex-Berechtigungen |
| **Überwachen von Ausführungen** | Berechtigung MONITOR für das erforderliche Objekt | Keine Berechtigung erforderlich, um den Befehl EXPLAIN zu verwenden | monitoring.viewer-Rolle | Berechtigung CAN_VIEW |
| **Schreiben von Daten** | Berechtigungen INSERT und/oder UPDATE (je nach Schreibvorgang) | Berechtigungen INSERT und UPDATE | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.tables.updateData |  Berechtigung MODIFY |
| **Laden von Daten in Tabellen** | Berechtigungen CREATE STAGE ON SCHEMA, SELECT und INSERT für die Zieltabelle | Berechtigungen SELECT und INSERT | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create, bigquery.tables.getData und bigquery.tables.updateData | Berechtigungen SELECT und MODIFY |
| **Zugreifen auf Client-Daten** | Berechtigungen SELECT für (FUTURE) TABLE(S) oder VIEW(S) | Berechtigung SELECT | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: bigquery.jobs.create und bigquery.tables.getData für Tabellen oder bigquery.dataViewer-Rolle |  Berechtigung SELECT |
| **Zugreifen auf Metadaten** | Berechtigung SELECT für INFORMATION_SCHEMA SCHEMA | Berechtigung SELECT | bigquery.metadataViewer-Rolle |  Berechtigung SELECT für INFORMATION_SCHEMA SCHEMA |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Leseberechtigung (Standard) | Berechtigung CONNECT | Keine Berechtigung erforderlich |
| **Erstellen von Tabellen** | CREATE TABLE ON DATABASE (Warehouse) und ALTER ON SCHEMA | Berechtigung CREATE TABLE | Berechtigung CREATE ON SCHEMA |
| **Erstellen von Indizes** | K. A. | Berechtigung ALTER | K. A. |
| **Erstellen von Funktionen** | K. A. | Berechtigung CREATE FUNCTION | Berechtigung CREATE ON SCHEMA |
| **Erstellen von Verfahren** | CREATE PROCEDURE ON DATABASE (Warehouse) und ALTER ON SCHEMA | Berechtigung CREATE PROCEDURE | Berechtigung CREATE ON SCHEMA |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | ALTER ON SCHEMA | Berechtigung ALTER | Besitz des Objekts oder der Berechtigung DROP für ein Objekt |
| **Überwachen von Ausführungen** | Workspace Contributor oder höhere Berechtigungen (queryinsights.exec_requests_history)  | Berechtigung CONTROL | Zur Verwendung der EXPLAIN-Anweisung ist keine Berechtigung erforderlich |
| **Schreiben von Daten** | INSERT und/oder UPDATE ON OBJECT | Berechtigungen INSERT und UPDATE | Berechtigungen INSERT und UPDATE |
| **Laden von Daten in Tabellen** | SELECT ON OBJECT und INSERT ON OBJECT | Berechtigungen CREATE TABLE, EXECUTE, SELECT, INSERT, UPDATE, ALTER | Berechtigung INSERT für Tabelle, Berechtigung USAGE für Schema |
| **Zugreifen auf Client-Daten** | SELECT ON OBJECT | Berechtigung SELECT | Berechtigung SELECT |
| **Zugreifen auf Metadaten** | SELECT ON INFORMATION_SCHEMA | Keine Berechtigung zum Beschreiben der Tabelle erforderlich | USAGE ON SCHEMA, SELECT on TABLE und zudem Berechtigungen für die Tabellen v_catalog.columns und v_catalog.view_columns |
