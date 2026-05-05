---
title: Berechtigungen für den Zugriff auf externe Datenbanken
description: Erfahren Sie, welche Berechtigungen Sie für den Zugriff auf jede Datenbank-Engine sowie das Durchführen von Aufgaben auf diesen benötigen
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
TQID: https://experienceleague.adobe.com/LI7H7b6iM3TAsPy00wDwNj3-D0Z7mIrH9MKW8g9QDsk
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 5cbe8da3f51b33b14f5c86648b3523ce6464b944
workflow-type: tm+mt
source-wordcount: 447
ht-degree: 93%

---

# Berechtigungsmatrix für Federated Data Access (FDA) {#fda-rights}

In der folgenden Tabelle sind die erforderlichen Datenbankberechtigungen für jedes System aufgeführt, mit denen Sie über Federated Data Access (FDA) Vorgänge für externe Datenbanken durchführen können.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | `USAGE ON WAREHOUSE`-, `USAGE ON DATABASE`- und `USAGE ON SCHEMA`-Berechtigungen | Erstellen von mit dem AWS-Konto verknüpften Benutzenden | Erstellen eines Dienstkontos und Gewähren von Hauptzugriff auf das Projekt | `USE CATALOG`-Berechtigung für Katalog und `CAN_USE`-Berechtigung für SQL Warehouse |
| **Erstellen von Tabellen** | `CREATE TABLE ON SCHEMA`-Berechtigung | `CREATE`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`- und `bigquery.tables.create`-Berechtigung | `USE SCHEMA`- und `CREATE TABLE`-Berechtigung |
| **Erstellen von Indizes** | K. A. | `CREATE`-Berechtigung | BigQuery unterstützt nur Suchindizes. Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`-, `bigquery.tables.getData`- und `bigquery.tables.createIndex`-Berechtigung | K. A. |
| **Erstellen von Funktionen** | `CREATE FUNCTION ON SCHEMA`-Berechtigung | `USAGE ON LANGUAGE plpythonu`-Berechtigung zum Aufrufen externer Python-Skripte | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`- und `bigquery.routines.create`-Berechtigung | `CREATE FUNCTION`-Berechtigung |
| **Erstellen von Verfahren** | K. A. | `USAGE ON LANGUAGE plpythonu`-Berechtigung zum Aufrufen externer Python-Skripte | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`- und `bigquery.routines.create`-Berechtigung |  K. A. |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | Eigentümer des Objekts | Eigentümer des Objekts oder Superuser | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`-, `bigquery.routines.delete`-, `bigquery.tables.delete`- und `bigquery.tables.deleteIndex`-Berechtigung | K. A. |
| **Monitoring von Ausführungen** | `MONITOR`-Berechtigung für das erforderliche Objekt | Keine Berechtigung erforderlich für die Verwendung des `EXPLAIN`-Befehls | `monitoring.viewer`-Rolle | `CAN_VIEW`-Berechtigung |
| **Schreiben von Daten** | `INSERT`- und/oder `UPDATE`-Berechtigung (abhängig vom Schreibvorgang) | `INSERT`- und `UPDATE`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.updateData` | `MODIFY`-Berechtigung |
| **Laden von Daten in Tabellen** | `CREATE STAGE ON SCHEMA`, `Create file FORMATGRANT CREATE FILE FORMAT ON SCHEMA <SCHEMA> to ROLE <ROLE>` `SELECT` und `INSERT` für die Zieltabellen-Berechtigungen | `SELECT`- und `INSERT`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`, `bigquery.tables.getData` und `bigquery.tables.updateData` | `SELECT`- und `MODIFY`-Berechtigung |
| **Zugreifen auf Client-Daten** | `SELECT on (FUTURE) TABLE(S)`- oder `VIEW(S)`-Berechtigung | `SELECT`-Berechtigung | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.getData` für Tabellen oder die `bigquery.dataViewer`-Rolle | `SELECT`-Berechtigung |
| **Zugreifen auf Metadaten** | `SELECT on INFORMATION_SCHEMA SCHEMA`-Berechtigung | `SELECT`-Berechtigung | `bigquery.metadataViewer`-Rolle |  `SELECT on INFORMATION_SCHEMA SCHEMA`-Berechtigung |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica | Teradata |
|:-:|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Leseberechtigung (Standard) | `CONNECT`-Berechtigung | Keine Berechtigung erforderlich | `CONNECT`-Berechtigung |
| **Erstellen von Tabellen** | `CREATE TABLE ON DATABASE` (Warehouse) und `ALTER ON SCHEMA` | `CREATE TABLE`-Berechtigung | `CREATE ON SCHEMA`-Berechtigung | `CREATE TABLE` oder `TABLE` Keyword |
| **Erstellen von Indizes** | K. A. | `ALTER`-Berechtigung | K. A. | `CREATE INDEX` oder `INDEX` Keyword |
| **Erstellen von Funktionen** | K. A. | `CREATE FUNCTION`-Berechtigung | `CREATE ON SCHEMA`-Berechtigung | `CREATE FUNCTION` oder `FUNCTION` Keyword |
| **Erstellen von Verfahren** | `CREATE PROCEDURE ON DATABASE` (Warehouse) und `ALTER ON SCHEMA` | `CREATE PROCEDURE`-Berechtigung | `CREATE ON SCHEMA`-Berechtigung | `CREATE PROCEDURE` oder `PROCEDURE` Keyword |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | `ALTER ON SCHEMA` | `ALTER`-Berechtigung | Besitz des Objekts oder der `DROP`-Berechtigung für Objekt | `DROP` nach Objekttyp oder verwandtem Schlüsselwort |
| **Monitoring von Ausführungen** | Workspace-Mitwirkende bzw. -Mitwirkender oder höhere Berechtigungen (`queryinsights.exec_requests_history`) | `CONTROL`-Berechtigung | Keine Berechtigung erforderlich zur Verwendung von `EXPLAIN`-Anweisung | Keine zusätzliche Berechtigung erforderlich, um `EXPLAIN` zu verwenden |
| **Schreiben von Daten** | `INSERT` und/oder `UPDATE ON OBJECT` | `INSERT`- und `UPDATE`-Berechtigung | `INSERT`- und `UPDATE`-Berechtigung | `INSERT`- und `UPDATE`-Berechtigung |
| **Laden von Daten in Tabellen** | `SELECT ON OBJECT` und `INSERT ON OBJECT` | `CREATE TABLE`-, `EXECUTE`-, `SELECT`-, `INSERT`-, `UPDATE`- und `ALTER`-Berechtigung | `INSERT`-Berechtigung für Tabelle, `USAGE`-Berechtigung für Schema | `SELECT` und `INSERT` (zum Beispiel `COPY TO`/`COPY FROM`) |
| **Zugreifen auf Client-Daten** | `SELECT ON OBJECT` | `SELECT`-Berechtigung | `SELECT`-Berechtigung | `SELECT`-Berechtigung |
| **Zugreifen auf Metadaten** | `SELECT ON INFORMATION_SCHEMA` | Keine Berechtigung zum Beschreiben der Tabelle erforderlich | `USAGE ON SCHEMA`, `SELECT on TABLE` und auch Berechtigungen für Tabellen `v_catalog.columns` und `v_catalog.view_columns` | `SHOW`-Berechtigung |
