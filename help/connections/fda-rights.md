---
title: Berechtigungen für den Zugriff auf externe Datenbanken
description: Erfahren Sie, welche Berechtigungen Sie für den Zugriff auf jede Datenbank-Engine sowie das Durchführen von Aufgaben auf diesen benötigen
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# Berechtigungsmatrix für Federated Data Access (FDA) {#fda-rights}

In der folgenden Tabelle sind die erforderlichen Datenbankberechtigungen für jedes System aufgeführt, mit denen Sie über Federated Data Access (FDA) Vorgänge für externe Datenbanken durchführen können.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | `USAGE ON WAREHOUSE`-, `USAGE ON DATABASE`- und `USAGE ON SCHEMA`-Berechtigungen | Erstellen von mit dem AWS-Konto verknüpften Benutzenden | Erstellen eines Dienstkontos und Gewähren von Hauptzugriff auf das Projekt | `USE CATALOG`-Berechtigung für Katalog und `CAN_USE`-Berechtigung für SQL Warehouse |
| **Erstellen von Tabellen** | `CREATE TABLE ON SCHEMA`-Berechtigung | `CREATE`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`- und `bigquery.tables.create`-Berechtigung | `USE SCHEMA`- und `CREATE TABLE`-Berechtigung |
| **Erstellen von Indizes** | k. A. | `CREATE`-Berechtigung | BigQuery unterstützt nur Suchindizes. Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`-, `bigquery.tables.getData`- und `bigquery.tables.createIndex`-Berechtigung | k. A. |
| **Erstellen von Funktionen** | `CREATE FUNCTION ON SCHEMA`-Berechtigung | `USAGE ON LANGUAGE plpythonu`-Berechtigung zum Aufrufen externer Python-Skripte | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`- und `bigquery.routines.create`-Berechtigung | `CREATE FUNCTION`-Berechtigung |
| **Erstellen von Verfahren** | k. A. | `USAGE ON LANGUAGE plpythonu`-Berechtigung zum Aufrufen externer Python-Skripte | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`- und `bigquery.routines.create`-Berechtigung |  K. A. |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | Eigentümer des Objekts | Eigentümer des Objekts oder Superuser | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`-, `bigquery.routines.delete`-, `bigquery.tables.delete`- und `bigquery.tables.deleteIndex`-Berechtigung | k. A. |
| **Überwachen von Ausführungen** | `MONITOR`-Berechtigung für das erforderliche Objekt | Keine Berechtigung erforderlich für die Verwendung des `EXPLAIN`-Befehls | `monitoring.viewer`-Rolle | `CAN_VIEW`-Berechtigung |
| **Schreiben von Daten** | `INSERT`- und/oder `UPDATE`-Berechtigung (abhängig vom Schreibvorgang) | `INSERT`- und `UPDATE`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.updateData` | `MODIFY`-Berechtigung |
| **Laden von Daten in Tabellen** | `CREATE STAGE ON SCHEMA`-, `SELECT`- und `INSERT`-Berechtigung in der Zieltabelle | `SELECT`- und `INSERT`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`, `bigquery.tables.getData` und `bigquery.tables.updateData` | `SELECT`- und `MODIFY`-Berechtigung |
| **Zugreifen auf Client-Daten** | `SELECT on (FUTURE) TABLE(S)`- oder `VIEW(S)`-Berechtigung | `SELECT`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.getData` für Tabellen oder die `bigquery.dataViewer`-Rolle | `SELECT`-Berechtigung |
| **Zugreifen auf Metadaten** | `SELECT on INFORMATION_SCHEMA SCHEMA`-Berechtigung | `SELECT`-Berechtigung | `bigquery.metadataViewer`-Rolle |  `SELECT on INFORMATION_SCHEMA SCHEMA`-Berechtigung |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Leseberechtigung (Standard) | `CONNECT`-Berechtigung | Keine Berechtigung erforderlich |
| **Erstellen von Tabellen** | `CREATE TABLE ON DATABASE` (Warehouse) und `ALTER ON SCHEMA` | `CREATE TABLE`-Berechtigung | `CREATE ON SCHEMA`-Berechtigung |
| **Erstellen von Indizes** | k. A. | `ALTER`-Berechtigung | k. A. |
| **Erstellen von Funktionen** | k. A. | `CREATE FUNCTION`-Berechtigung | `CREATE ON SCHEMA`-Berechtigung |
| **Erstellen von Verfahren** | `CREATE PROCEDURE ON DATABASE` (Warehouse) und `ALTER ON SCHEMA` | `CREATE PROCEDURE`-Berechtigung | `CREATE ON SCHEMA`-Berechtigung |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | `ALTER ON SCHEMA` | `ALTER`-Berechtigung | Besitz des Objekts oder der `DROP`-Berechtigung für Objekt |
| **Überwachen von Ausführungen** | Workspace-Mitwirkende bzw. -Mitwirkender oder höhere Berechtigungen (`queryinsights.exec_requests_history`) | `CONTROL`-Berechtigung | Keine Berechtigung erforderlich zur Verwendung von `EXPLAIN`-Anweisung |
| **Schreiben von Daten** | `INSERT` und/oder `UPDATE ON OBJECT` | `INSERT`- und `UPDATE`-Berechtigung | `INSERT`- und `UPDATE`-Berechtigung |
| **Laden von Daten in Tabellen** | `SELECT ON OBJECT` und `INSERT ON OBJECT` | `CREATE TABLE`-, `EXECUTE`-, `SELECT`-, `INSERT`-, `UPDATE`- und `ALTER`-Berechtigung | `INSERT`-Berechtigung für Tabelle, `USAGE`-Berechtigung für Schema |
| **Zugreifen auf Client-Daten** | `SELECT ON OBJECT` | `SELECT`-Berechtigung | `SELECT`-Berechtigung |
| **Zugreifen auf Metadaten** | `SELECT ON INFORMATION_SCHEMA` | Keine Berechtigung zum Beschreiben der Tabelle erforderlich | `USAGE ON SCHEMA`, `SELECT on TABLE` und auch Berechtigungen für Tabellen `v_catalog.columns` und `v_catalog.view_columns` |
