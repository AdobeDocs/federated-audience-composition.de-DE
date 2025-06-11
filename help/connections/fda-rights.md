---
title: Berechtigungen für den Zugriff auf externe Datenbanken
description: Erfahren Sie, auf welche Berechtigungen Sie zugreifen und Aufgaben für jede Datenbank-Engine ausführen müssen
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: 530a8709a67fabec1a36e1661b922f3e9a9e6996
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 35%

---

# Berechtigungsmatrix für Federated Data Access (FDA) {#fda-rights}

In der folgenden Tabelle sind die erforderlichen Datenbankberechtigungen für jedes System aufgeführt, sodass Sie über Federated Data Access (FDA) Vorgänge für externe Datenbanken durchführen können.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Berechtigungen für `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` und `USAGE ON SCHEMA` | Erstellen eines mit dem AWS-Konto verknüpften Benutzers | Erstellen eines Dienstkontos und Gewähren von Hauptzugriff auf das Projekt | `USE CATALOG` für Katalog und `CAN_USE` für SQL Warehouse |
| **Erstellen von Tabellen** | `CREATE TABLE ON SCHEMA` | Berechtigung `CREATE` | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.create` Berechtigungen | Berechtigungen für `USE SCHEMA` und `CREATE TABLE` |
| **Erstellen von Indizes** | K. A. | Berechtigung `CREATE` | BigQuery unterstützt nur Suchindizes. Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`, `bigquery.tables.getData` und `bigquery.tables.createIndex` | K. A. |
| **Erstellen von Funktionen** | `CREATE FUNCTION ON SCHEMA` | Berechtigung zum Aufrufen externer Python-Skripte `USAGE ON LANGUAGE plpythonu` | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.routines.create` Berechtigungen | Berechtigung `CREATE FUNCTION` |
| **Erstellen von Verfahren** | K. A. | Berechtigung zum Aufrufen externer Python-Skripte `USAGE ON LANGUAGE plpythonu` | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.routines.create` Berechtigungen |  K. A. |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | Eigentümer des Objekts | Eigentümer des Objekts oder Superuser | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` und `bigquery.tables.deleteIndex` | K. A. |
| **Überwachen von Ausführungen** | Berechtigung für das erforderliche Objekt `MONITOR` | Keine Berechtigungen erforderlich, um den `EXPLAIN`-Befehl zu verwenden | Rolle `monitoring.viewer` | Berechtigung `CAN_VIEW` |
| **Schreiben von Daten** | `INSERT`- und/oder `UPDATE` Berechtigungen (abhängig vom Schreibvorgang) | Berechtigungen für `INSERT` und `UPDATE` | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.updateData` | Berechtigung `MODIFY` |
| **Laden von Daten in Tabellen** | Berechtigungen für `CREATE STAGE ON SCHEMA`, `SELECT` und `INSERT` in der Zieltabelle | Berechtigungen für `SELECT` und `INSERT` | Die dem Service-Konto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create`, `bigquery.tables.getData` und `bigquery.tables.updateData` | Berechtigungen für `SELECT` und `MODIFY` |
| **Zugreifen auf Client-Daten** | `SELECT on (FUTURE) TABLE(S)` oder `VIEW(S)` Berechtigung(en) | Berechtigung `SELECT` | Die dem Dienstkonto zugewiesene Rolle muss Folgendes enthalten: `bigquery.jobs.create` und `bigquery.tables.getData` für Tabellen oder die `bigquery.dataViewer` Rolle | Berechtigung `SELECT` |
| **Zugreifen auf Metadaten** | `SELECT on INFORMATION_SCHEMA SCHEMA` | Berechtigung `SELECT` | Rolle `bigquery.metadataViewer` |  Berechtigung `SELECT on INFORMATION_SCHEMA SCHEMA` |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Herstellen einer Verbindung zu einer Remote-Datenbank** | Leseberechtigung (Standard) | Berechtigung `CONNECT` | Keine Berechtigung erforderlich |
| **Erstellen von Tabellen** | `CREATE TABLE ON DATABASE` (Warehouse) und `ALTER ON SCHEMA` | Berechtigung `CREATE TABLE` | `CREATE ON SCHEMA` |
| **Erstellen von Indizes** | K. A. | Berechtigung `ALTER` | K. A. |
| **Erstellen von Funktionen** | K. A. | Berechtigung `CREATE FUNCTION` | `CREATE ON SCHEMA` |
| **Erstellen von Verfahren** | `CREATE PROCEDURE ON DATABASE` (Warehouse) und `ALTER ON SCHEMA` | Berechtigung `CREATE PROCEDURE` | `CREATE ON SCHEMA` |
| **Entfernen von Objekten (Tabellen, Indizes, Funktionen, Verfahren)** | `ALTER ON SCHEMA` | Berechtigung `ALTER` | Eigentümerschaft des Objekts oder der Berechtigung `DROP` für ein Objekt |
| **Überwachen von Ausführungen** | Mitwirkende an Workspace oder höhere Berechtigungen (`queryinsights.exec_requests_history`) | Berechtigung `CONTROL` | Keine Berechtigung erforderlich, um `EXPLAIN` Anweisung zu verwenden |
| **Schreiben von Daten** | `INSERT` und/oder `UPDATE ON OBJECT` | Berechtigungen für `INSERT` und `UPDATE` | `INSERT` und `UPDATE` Berechtigungen |
| **Laden von Daten in Tabellen** | `SELECT ON OBJECT` und `INSERT ON OBJECT` | Berechtigungen für `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` und `ALTER` | Berechtigung für Tabelle `INSERT`, Berechtigung für Schema `USAGE` |
| **Zugreifen auf Client-Daten** | `SELECT ON OBJECT` | Berechtigung `SELECT` | `SELECT` |
| **Zugreifen auf Metadaten** | `SELECT ON INFORMATION_SCHEMA` | Keine Berechtigung zum Beschreiben der Tabelle erforderlich | `USAGE ON SCHEMA`, `SELECT on TABLE` und auch Berechtigungen für Tabellen `v_catalog.columns` und `v_catalog.view_columns` |
