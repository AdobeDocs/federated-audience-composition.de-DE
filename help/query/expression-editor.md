---
audience: end-user
title: Erstellen Ihrer ersten Abfrage mithilfe des Abfrage-Modelers
description: Erfahren Sie, wie Sie Ihre erste Abfrage im Abfrage-Modeler erstellen.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: fdf93fb3554d05057052aa7059e141817a883dcc
workflow-type: tm+mt
source-wordcount: '4107'
ht-degree: 14%

---

# Bearbeiten von Ausdrücken {#expression}

Die Bearbeitung von Ausdrücken erfolgt durch die manuelle Eingabe von Bedingungen, die in ihrer Gesamtheit eine Regel bilden. Dieser Modus bietet erweiterte Funktionen, mit denen Sie die Werte zur Durchführung bestimmter Abfragen ändern können, z. B. Bearbeitung von Daten, Zeichenfolgen, Nummernfeldern, Sortierungen, usw.

## Arbeiten mit dem Ausdruckseditor {#edit}

Der Ausdruckseditor steht bei der Konfiguration einer benutzerdefinierten Bedingung im Abfrage-Modeler unter **[!UICONTROL Ausdruck bearbeiten]** für die Felder **[!UICONTROL Attribut]** und **[!UICONTROL Wert]** zur Verfügung.

| Zugriff über das Feld **[!UICONTROL Attribut]** | Zugriff über das Feld **[!UICONTROL Wert]** |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

Der Ausdruckseditor bietet Folgendes:

* Ein **Eingabefeld (1)**, in dem der Ausdruck definiert wird.
* Die Liste der verfügbaren **Felder (2)**, die im Ausdruck verwendet werden können und dem Schema, auch bekannt als Zielgruppendimension, der Abfrage entsprechen.
* **Hilfsfunktionen (3)**, sortiert nach Kategorie.

Bearbeiten Sie den Ausdruck, indem Sie ihn direkt in das Eingabefeld eingeben. Um ein Feld oder eine Hilfsfunktion hinzuzufügen, gehen Sie mit dem Cursor zu dem Ausdruck, zu dem Sie es/sie hinzufügen möchten, und klicken Sie auf die Schaltfläche „+“.

![](assets/expression-editor.png){zoomable="yes"}

Wenn Ihr Ausdruck fertig ist, klicken Sie auf **[!UICONTROL Bestätigen]**. Der Ausdruck wird im ausgewählten Feld angezeigt. Öffnen Sie zum Bearbeiten den Ausdruckseditor und nehmen Sie die gewünschten Änderungen vor.

Das folgende Beispiel zeigt einen für das Feld **[!UICONTROL Wert]** konfigurierten Ausdruck. Um ihn zu bearbeiten, müssen Sie den Ausdruckseditor über die Schaltfläche **[!UICONTROL Ausdruck bearbeiten]** öffnen.

![](assets/edit-expression-value.png){zoomable="yes"}

## Hilfsfunktionen

Der Abfrageeditor bietet fortgeschrittene Funktionen zur Erstellung komplexer Filter, je nach den gewünschten Ergebnissen und der Art der bearbeiteten Daten. Folgende Funktionen stehen zur Verfügung:

<!-- ### Aggregate

The aggregate functions are used to perform calculations on a set of values.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StdDev** | Returns the standard deviation of the values given. | StdDev(&lt;VALUE&gt;) | StdDev([0,3,5]) | -->

<!-- 

>[!TAB Databricks]

Aggregate functions are not available.

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") |

>[!TAB Redshift]

Aggregate functions are not available. -->

<!-- 

>[!TAB Snowflake]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") | -->

<!-- 
>[!TAB Vertica]

Aggregate functions are not available. -->

<!-- 
>[!ENDTABS] 
-->

### Datum

Die Datumsfunktionen dienen der Manipulation von Datums- oder Uhrzeitwerten.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Fügt die angegebene Anzahl von Jahren zum angegebenen Datum/zur angegebenen Uhrzeit hinzu. | AddYears(&lt;DATETIME>, &lt;NUMBER>) | AddYears(„2019-12-25 15:30:00“, 3) |
| **AddMonths** | Addiert die angegebene Anzahl von Monaten zum angegebenen Datum/zur angegebenen Uhrzeit-Wert. | AddMonths(&lt;DATETIME>, &lt;NUMBER>) | AddMonths(„2019-12-25 15.:30:&quot;, 6) |
| **AddDays** | Addiert die angegebene Anzahl von Tagen zur angegebenen Datums-/Uhrzeitangabe. | AddDays(&lt;DATETIME>, &lt;NUMBER>) | AddDays(„2019-12-25 15:30:00“, 10) |
| **AddHours** | Fügt die angegebene Anzahl von Stunden zum angegebenen Datum/zur angegebenen Uhrzeit hinzu. | AddHours(&lt;DATETIME>, &lt;NUMBER>) | AddHours(„2019-12-25 15:30:00“, 3) |
| **AddMinutes** | Addiert die angegebene Anzahl von Minuten zur angegebenen Datums-/Uhrzeitangabe. | AddMinutes(&lt;DATETIME>, &lt;NUMBER>) | AddMinutes(„2019-12-25 15:30:00“, 32) |
| **AddSeconds** | Addiert die angegebene Anzahl von Sekunden zur angegebenen Datums-/Uhrzeitangabe. | AddSeconds(&lt;DATETIME>, &lt;NUMBER>) | AddSeconds(„2019-12-25 15:30:00“, 37) |
| **SubYears** | Subtrahiert die angegebene Anzahl von Jahren von der angegebenen Uhrzeit-/Datumsangabe. | SubYears(&lt;DATETIME>, &lt;NUMBER>) | SubYears(„2019-12-25 15.:30:&quot;, 3) |
| **SubMonths** | Subtrahiert die angegebene Anzahl von Monaten von der angegebenen Uhrzeit-/Datumsangabe. | SubMonths(&lt;DATETIME>, &lt;NUMBER>) | SubMonths(„2019-12-25 15.:30:&quot;, 6) |
| **SubDays** | Subtrahiert die angegebene Anzahl von Tagen von der angegebenen Uhrzeit-/Datumsangabe. | SubDays(&lt;DATETIME>, &lt;NUMBER>) | SubDays(„2019-12-25 15:30:00“, 10) |
| **SubHours** | Subtrahiert die angegebene Anzahl von Stunden von der angegebenen Uhrzeit-/Datumsangabe. | SubHours(&lt;DATETIME>, &lt;NUMBER>) | SubHours(„2019-12-25 15.:30:&quot;, 3) |
| **SubMinutes** | Subtrahiert die angegebene Anzahl von Minuten von der angegebenen Datums-/Uhrzeitangabe. | SubMinutes(&lt;DATETIME>, &lt;NUMBER>) | SubMinutes(„2019-12-25 15:30:00“, 32) |
| **SubSeconds** | Subtrahiert die angegebene Anzahl von Sekunden von der angegebenen Datums-/Uhrzeitangabe. | SubSeconds(&lt;DATETIME>, &lt;NUMBER>) | SubSeconds(„2019-12-25 15:30:00“, 37) |
| **Year** | Extrahiert das Jahr aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Month** | Extrahiert den Monat aus dem angegebenen Datetime-Objekt. | MONTH(&lt;DATETIME>) | MONTH(„12.12.2019 15:30:00„) |
| **Day** | Extrahiert den Tag aus dem angegebenen Datetime-Objekt. | DAY(&lt;DATETIME>) | DAY(„12.12.2019 15:30:00„) |
| **DayOfYear** | Extrahiert den Tag des Jahres aus dem angegebenen Datetime-Objekt. Wenn die angegebene Datums-/Uhrzeitangabe beispielsweise der 2. Februar ist, würde sie 33 zurückgeben. | DayOfYear(&lt;DATETIME>) | DayOfYear(„12.12.2019 15:30:00„) |
| **WeekDay** | Extrahiert den Wochentag aus dem angegebenen Datetime-Objekt als eine Zahl von 0 bis 6, wobei 0 Sonntag darstellt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Hour** | Extrahiert den Stundenwert aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Minute** | Extrahiert den Minutenwert aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Second** | Extrahiert den zweiten Wert aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **YearsDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Jahren. | YearsDiff(&lt;DATETIME>, &lt;DATETIME>) | YearsDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **MonthsDiff** | Findet den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Monaten. | monthsDiff(&lt;DATETIME>, &lt;DATETIME>) | MonthsDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **DaysDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Tagen. | DaysDiff(&lt;DATETIME>, &lt;DATETIME>) | DaysDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **HoursDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Stunden. | HoursDiff(&lt;DATETIME>, &lt;DATETIME>) | HoursDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **MinutesDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Minuten. | MinutesDiff(&lt;DATETIME>, &lt;DATETIME>) | MinutesDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **SecondsDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Sekunden. | SecondsDiff(&lt;DATETIME>, &lt;DATETIME>) | SecondsDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **YearsOld** | Sucht den Unterschied zwischen dem angegebenen Datum/der angegebenen Uhrzeit und der Gegenwart mit einer Granularität von Jahren. | YearsOld(&lt;DATETIME>) | YearsOld(„2019-12-25 15:30:00„) |
| **MonthsOld** | Findet den Unterschied zwischen dem angegebenen Datum/Uhrzeit-Wert und der Gegenwart mit einer Granularität von Monaten. | monthsOld(&lt;DATETIME>) | monthsOld(„2019-12-25 15:30:00„) |
| **DaysOld** | Sucht den Unterschied zwischen dem angegebenen Datum/der angegebenen Uhrzeit und der Gegenwart mit einer Granularität von Tagen. | DaysOld(&lt;DATETIME>) | DaysOld(„2019-12-25 15:30:00„) |
| **GetDate** | Das aktuelle Datum des Servers abrufen. | GetDate() | GetDate() |
| **DateOnly** | Kürzt Datum/Uhrzeit auf Jahr, Monat und Tag. | DateOnly(&lt;DATETIME>) | DateOnly(„2019-12-25 15:30:00„) |
| **ToDate** | Konvertiert das Feld in ein Datumsfeld. | ToDate(&lt;DATETIME>) | ToDate(„2019-12-25 15:30:00„) |
| **ToDateTime** | Konvertiert das Feld in ein Datum/Uhrzeit-Feld. | ToDateTime(&lt;DATE>) | ToDateTime(„2019-12-25 15:30:00„) |
| **ToTimestamp** | Konvertiert das Feld in ein Zeitstempelfeld. | ToTimestamp(&lt;DATETIME>) | ToTimestamp(„2019-12-25 15:30:00„) |
| **Oldest** | Gibt das älteste Datum zwischen den beiden angegebenen zurück. | Oldest(&lt;DATETIME>, &lt;DATETIME>) | Oldest(„2015-02-13 11:59:59“, „2016-04-13 19:28:14„) |
| **TruncDate** | Kürzt die Datums-/Uhrzeitangabe auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird er auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3600 ist, wird er auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86400 ist, wird er auf den nächsten Tag gekürzt. Andernfalls wird sie auf die nächste Sekunde gekürzt. | truncDate(&lt;DATETIME>, &lt;NUMBER>) | TruncDate(„2016-04-13 19:28:14“, 3600) |
| **TruncDateTZ** | Kürzt die Datums-/Uhrzeitangabe auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert, und setzt die Datums-/Uhrzeitangabe auf die angegebene Zeitzone. Wenn der numerische Wert gleich 60 ist, wird er auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3600 ist, wird er auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86400 ist, wird er auf den nächsten Tag gekürzt. | truncDateTZ(&lt;DATETIME>, &lt;NUMBER>, &lt;TIMEZONE>) | TruncDateTZ(„2016-04-13 19:28:14“, 3600, „America/Los_Angeles„) |
| **TruncTime** | Setzt den Datum/Uhrzeit-Wert auf den 1. Januar 2000 und rundet den Rest des Datum/Uhrzeit-Werts auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird er auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3600 ist, wird er auf die nächste Stunde gekürzt. | truncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime(„2016-04-13 19:28:14“, 3600) |
| **TruncQuarter** | Kürzt den dateTime-Wert auf das erste Datum im nächsten Quartal. | truncQuarter(&lt;DATETIME>) | TruncQuarter(„2016-04-13 19:28:14„) |
| **TruncYear** | Kürzt den dateTime-Wert auf das erste Datum im nächsten Jahr. | truncYear(&lt;DATETIME>) | TruncYear(„2016-04-13 19:28:14„) |
| **TruncWeek** | Kürzt Datum/Uhrzeit auf den Sonntag der nächsten Woche. | truncWeek(&lt;DATETIME>) | TruncWeek(„2016-04-13 19:28:14„) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- | **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | -->


<!-- 
>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncDateTZ** | Truncates the datetime to the nearest unit, based on the numerical value given, and sets the datetime to the specified timezone. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. | TruncDateTZ(&lt;DATETIME&gt;, &lt;NUMBER&gt;, &lt;TIMEZONE&gt;) | TruncDateTZ("2016-04-13 19:28:14", 3600, "America/Los_Angeles") |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |

>[!TAB Redshift]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **ConvertTimezone** | Converts the datetime from its timezone to the timezone of the external account. | ConvertTimezone(&lt;DATETIME&gt;) | ConvertTimezone("2019-12-25 15:30:00") |

 -->

>[!TAB Snowflake]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Fügt die angegebene Anzahl von Jahren zum angegebenen Datum/zur angegebenen Uhrzeit hinzu. | AddYears(&lt;DATETIME>, &lt;NUMBER>) | AddYears(„2019-12-25 15:30:00“, 3) |
| **AddMonths** | Addiert die angegebene Anzahl von Monaten zum angegebenen Datum/zur angegebenen Uhrzeit-Wert. | AddMonths(&lt;DATETIME>, &lt;NUMBER>) | AddMonths(„2019-12-25 15.:30:&quot;, 6) |
| **AddDays** | Addiert die angegebene Anzahl von Tagen zur angegebenen Datums-/Uhrzeitangabe. | AddDays(&lt;DATETIME>, &lt;NUMBER>) | AddDays(„2019-12-25 15:30:00“, 10) |
| **AddHours** | Fügt die angegebene Anzahl von Stunden zum angegebenen Datum/zur angegebenen Uhrzeit hinzu. | AddHours(&lt;DATETIME>, &lt;NUMBER>) | AddHours(„2019-12-25 15:30:00“, 3) |
| **AddMinutes** | Addiert die angegebene Anzahl von Minuten zur angegebenen Datums-/Uhrzeitangabe. | AddMinutes(&lt;DATETIME>, &lt;NUMBER>) | AddMinutes(„2019-12-25 15:30:00“, 32) |
| **AddSeconds** | Addiert die angegebene Anzahl von Sekunden zur angegebenen Datums-/Uhrzeitangabe. | AddSeconds(&lt;DATETIME>, &lt;NUMBER>) | AddSeconds(„2019-12-25 15:30:00“, 37) |
| **SubYears** | Subtrahiert die angegebene Anzahl von Jahren von der angegebenen Uhrzeit-/Datumsangabe. | SubYears(&lt;DATETIME>, &lt;NUMBER>) | SubYears(„2019-12-25 15.:30:&quot;, 3) |
| **SubMonths** | Subtrahiert die angegebene Anzahl von Monaten von der angegebenen Uhrzeit-/Datumsangabe. | SubMonths(&lt;DATETIME>, &lt;NUMBER>) | SubMonths(„2019-12-25 15.:30:&quot;, 6) |
| **SubDays** | Subtrahiert die angegebene Anzahl von Tagen von der angegebenen Uhrzeit-/Datumsangabe. | SubDays(&lt;DATETIME>, &lt;NUMBER>) | SubDays(„2019-12-25 15:30:00“, 10) |
| **SubHours** | Subtrahiert die angegebene Anzahl von Stunden von der angegebenen Uhrzeit-/Datumsangabe. | SubHours(&lt;DATETIME>, &lt;NUMBER>) | SubHours(„2019-12-25 15.:30:&quot;, 3) |
| **SubMinutes** | Subtrahiert die angegebene Anzahl von Minuten von der angegebenen Datums-/Uhrzeitangabe. | SubMinutes(&lt;DATETIME>, &lt;NUMBER>) | SubMinutes(„2019-12-25 15:30:00“, 32) |
| **SubSeconds** | AdSubtrahiert die angegebene Anzahl von Sekunden von der angegebenen Datums-/Uhrzeitangabe. | SubSeconds(&lt;DATETIME>, &lt;NUMBER>) | SubSeconds(„2019-12-25 15:30:00“, 37) |
| **Year** | Extrahiert das Jahr aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Month** | Extrahiert den Monat aus dem angegebenen Datetime-Objekt. | MONTH(&lt;DATETIME>) | MONTH(„12.12.2019 15:30:00„) |
| **Day** | Extrahiert den Tag aus dem angegebenen Datetime-Objekt. | DAY(&lt;DATETIME>) | DAY(„12.12.2019 15:30:00„) |
| **DayOfYear** | Extrahiert den Tag des Jahres aus dem angegebenen Datetime-Objekt. Wenn die angegebene Datums-/Uhrzeitangabe beispielsweise der 2. Februar ist, würde sie 33 zurückgeben. | DayOfYear(&lt;DATETIME>) | DayOfYear(„12.12.2019 15:30:00„) |
| **WeekDay** | Extrahiert den Wochentag aus dem angegebenen Datetime-Objekt als eine Zahl von 1 bis 7, wobei 1 Sonntag darstellt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Hour** | Extrahiert den Stundenwert aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Minute** | Extrahiert den Minutenwert aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **Second** | Extrahiert den zweiten Wert aus dem angegebenen Datetime-Objekt. | YEAR(&lt;DATETIME>) | YEAR(„12.12.2019 15:30:00„) |
| **YearsDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Jahren. | YearsDiff(&lt;DATETIME>, &lt;DATETIME>) | YearsDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **MonthsDiff** | Findet den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Monaten. | monthsDiff(&lt;DATETIME>, &lt;DATETIME>) | MonthsDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **DaysDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Tagen. | DaysDiff(&lt;DATETIME>, &lt;DATETIME>) | DaysDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **HoursDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Stunden. | HoursDiff(&lt;DATETIME>, &lt;DATETIME>) | HoursDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **MinutesDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Minuten. | MinutesDiff(&lt;DATETIME>, &lt;DATETIME>) | MinutesDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **SecondsDiff** | Sucht den Unterschied zwischen den angegebenen Datums- und Uhrzeitangaben mit einer Granularität von Sekunden. | SecondsDiff(&lt;DATETIME>, &lt;DATETIME>) | SecondsDiff(„2019-12-25 15:30:00“, „2018-10-14 18:35:27„) |
| **MonthsOld** | Findet den Unterschied zwischen dem angegebenen Datum/Uhrzeit-Wert und der Gegenwart mit einer Granularität von Monaten. | monthsOld(&lt;DATETIME>) | monthsOld(„2019-12-25 15:30:00„) |
| **DaysOld** | Sucht den Unterschied zwischen dem angegebenen Datum/der angegebenen Uhrzeit und der Gegenwart mit einer Granularität von Tagen. | DaysOld(&lt;DATETIME>) | DaysOld(„2019-12-25 15:30:00„) |
| **GetDate** | Das aktuelle Datum des Servers abrufen. | GetDate() | GetDate() |
| **DateOnly** | Kürzt Datum/Uhrzeit auf Jahr, Monat und Tag. | DateOnly(&lt;DATETIME>) | DateOnly(„2019-12-25 15:30:00„) |
| **ToDate** | Konvertiert das Feld in ein Datumsfeld. | ToDate(&lt;DATETIME>) | ToDate(„2019-12-25 15:30:00„) |
| **ToDateTime** | Konvertiert das Feld in ein Datum/Uhrzeit-Feld. | ToDateTime(&lt;DATE>) | ToDateTime(„2019-12-25 15:30:00„) |
| **ToTimestamp** | Konvertiert das Feld in ein Zeitstempelfeld. | ToTimestamp(&lt;DATETIME>) | ToTimestamp(„2019-12-25 15:30:00„) |
| **Oldest** | Gibt das älteste Datum zwischen den beiden angegebenen zurück. | Oldest(&lt;DATETIME>, &lt;DATETIME>) | Oldest(„2015-02-13 11:59:59“, „2016-04-13 19:28:14„) |
| **TruncDate** | Kürzt die Datums-/Uhrzeitangabe auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird er auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3600 ist, wird er auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86400 ist, wird er auf den nächsten Tag gekürzt. Andernfalls wird sie auf die nächste Sekunde gekürzt. | truncDate(&lt;DATETIME>, &lt;NUMBER>) | TruncDate(„2016-04-13 19:28:14“, 3600) |
| **TruncDateTZ** | Kürzt die Datums-/Uhrzeitangabe auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert, und setzt die Datums-/Uhrzeitangabe auf die angegebene Zeitzone. Wenn der numerische Wert gleich 60 ist, wird er auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3600 ist, wird er auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86400 ist, wird er auf den nächsten Tag gekürzt. | truncDateTZ(&lt;DATETIME>, &lt;NUMBER>, &lt;TIMEZONE>) | TruncDateTZ(„2016-04-13 19:28:14“, 3600, „America/Los_Angeles„) |
| **TruncTime** | Setzt den Datum/Uhrzeit-Wert auf den 1. Januar 2000 und rundet den Rest des Datum/Uhrzeit-Werts auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird er auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3600 ist, wird er auf die nächste Stunde gekürzt. | truncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime(„2016-04-13 19:28:14“, 3600) |
| **TruncQuarter** | Kürzt den dateTime-Wert auf das erste Datum im nächsten Quartal. | truncQuarter(&lt;DATETIME>) | TruncQuarter(„2016-04-13 19:28:14„) |
| **TruncYear** | Kürzt den dateTime-Wert auf das erste Datum im nächsten Jahr. | truncYear(&lt;DATETIME>) | TruncYear(„2016-04-13 19:28:14„) |
| **TruncWeek** | Kürzt Datum/Uhrzeit auf den Sonntag der nächsten Woche. | truncWeek(&lt;DATETIME>) | TruncWeek(„2016-04-13 19:28:14„) |
| **ConvertNTZ** | Konvertiert einen Zeitstempel ohne Zeitzone in einen Zeitstempel mit einer Zeitzone. Die angehängte Zeitzone ist die Zeitzone des externen Kontos. | ConvertNTZ(&lt;DATETIME>) | ConvertNTZ(„2024-06-24 14:43:49„) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- 
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | 
-->

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") |
-->

>[!ENDTABS]

>[!NOTE]
>
>Beachten Sie, dass die Funktion **Dateonly** nicht die Zeitzone des Benutzers, sondern des Servers verwendet.

### Geomarketing

Die Geomarketing-Funktionen dienen der Manipulation von geografischen Werten.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Distance** | Gibt den Abstand zwischen zwei Punkten zurück, die durch ihren Längen- und Breitengrad in Grad definiert sind, als doppelt. | Distance(&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Entfernung (40,345, 39,2345, -35,5834, 34,599) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Redshift]

Geomarketing functions are not available.

-->

>[!TAB Snowflake]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Distance** | Gibt den Abstand zwischen zwei Punkten zurück, die durch ihren Längen- und Breitengrad in Grad definiert sind, als doppelt. | Distance(&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Entfernung (40,345, 39,2345, -35,5834, 34,599) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

-->

>[!ENDTABS]

### Numerisch

Die numerischen Funktionen dienen der Konversion von Text in Zahlen.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Mod** | Gibt den Rest der ersten Zahl dividiert durch die zweite Zahl zurück. | mod(&lt;NUMBER>, &lt;NUMBER>) | Mod (3, 2) |
| **Percent** | Berechnet den Prozentsatz der ersten Zahl der zweiten Zahl. | Percent(&lt;NUMBER>, &lt;NUMBER>) | Prozent(1, 2) |
| **Random** | Gibt eine zufällige Zahl zwischen 0 (einschließlich) und 1 (ausschließlich) zurück. | random() | Zufällig () |
| **Round** | Gibt die angegebene Zahl auf die nächste angeforderte Dezimalstelle zurück. | ROUND(&lt;NUMBER>, &lt;NUMBER>) | ROUND(4,5394, 2) |
| **ToDouble** | Konvertiert die angegebene Zahl in eine Dublette. | ToDouble(&lt;NUMBER>) | ToDouble(5) |
| **ToInteger** | Konvertiert die angegebene Zahl in eine Ganzzahl. | ToInteger(&lt;NUMBER>) | ToInteger(45) |
| **ToInt64** | Konvertiert die angegebene Zahl in eine 64-Bit-Ganzzahl. | ToInt64(&lt;NUMBER>) | ToInt64(493) |
| **Trunc** | Kürzt die angegebene Zahl auf die angeforderte Anzahl von Dezimalstellen. | TRUNC(&lt;NUMBER>, &lt;NUMBER>) | TRUNC(36.9348934, 3) |

<!-- 
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Floor** | Rounds down the provided number to the nearest integer. For example, if the provided number is 3.8, it will return 3. | Floor(&lt;NUMBER&gt;) | Floor(3.8) |
| **Greatest** | Returns the larger number between the two provided numbers. | Greatest(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Greatest(1, 2) |
| **Least** | Returns the smaller number between the two provided numbers. | Least(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Least (1,2) |
 -->

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Redshift]

Numeric functions are not available.

--->

>[!TAB Snowflake]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Mod** | Gibt den Rest der ersten Zahl dividiert durch die zweite Zahl zurück. | mod(&lt;NUMBER>, &lt;NUMBER>) | Mod (3, 2) |
| **Percent** | Berechnet den Prozentsatz der ersten Zahl der zweiten Zahl. | Percent(&lt;NUMBER>, &lt;NUMBER>) | Prozent(1, 2) |
| **Random** | Gibt eine zufällige Zahl zwischen 0 (einschließlich) und 1 (ausschließlich) zurück. | random() | Zufällig () |
| **ToDouble** | Konvertiert die angegebene Zahl in eine Dublette. | ToDouble(&lt;NUMBER>) | ToDouble(5) |
| **ToInteger** | Konvertiert die angegebene Zahl in eine Ganzzahl. | ToInteger(&lt;NUMBER>) | ToInteger(45) |
| **ToInt64** | Konvertiert die angegebene Zahl in eine 64-Bit-Ganzzahl. | ToInt64(&lt;NUMBER>) | ToInt64(493) |
| **Trunc** | Kürzt die angegebene Zahl auf die angeforderte Anzahl von Dezimalstellen. | TRUNC(&lt;NUMBER>, &lt;NUMBER>) | TRUNC(36.9348934, 3) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

--->

>[!ENDTABS]

### Sonstige

In dieser Tabelle sind die restlichen verfügbaren Funktionen enthalten.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Case** | Gibt den ersten Wert zurück, wenn der Ausdruck wahr ist. Andernfalls wird der zweite Wert zurückgegeben. | case(when(&lt;EXPRESSION> &lt;VALUE>), else(&lt;VALUE>)) | case(Wenn(a > b, „ja„), Sonst(„nein„)) |
| **When** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um den Ausdruck in der Groß-/Kleinschreibung zu überprüfen. | WHEN(&lt;AUSDRUCK> &lt;WERT>) | Wenn(a > b, „ja„) |
| **Else** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um die andere Option auszuwählen, wenn der Wenn-Ausdruck „false“ ist. | else(&lt;VALUE>) | Sonst („nein„) |
| **Coalesce** | Gibt den ersten Wert ungleich null zurück. | coalesce(&lt;VALUE>, &lt;VALUE>) | Zusammenführen (“&quot;, „Zeichenfolge„) |
| **Decode** | Gibt die erste Option zurück, wenn die Werte gleich sind. Gibt die zweite Option zurück, wenn die Werte nicht gleich sind. | DECODE(&lt;VALUE>, &lt;VALUE>, &lt;VALUE>, &lt;VALUE>) | Decode(1, 2, „true“, „false„) |
| **GetEmailDomain** | Extrahiert die Domain aus der angegebenen E-Mail-Adresse. | GetEmailDomain(&lt;STRING>) | GetEmailDomain(“sample@example.com„) |
| **Iif** | Gibt die erste Option zurück, wenn die Bedingung wahr ist, und gibt die zweite Option zurück, wenn die Bedingung falsch ist. | IF(&lt;CONDITION>, &lt;VALUE>, &lt;VALUE>) | Iif(10 &lt; 20, „true“, „false„) |
| **IsEmptyString** | Gibt die erste Option zurück, wenn die Zeichenfolge leer ist. Andernfalls wird die zweite Option zurückgegeben. | IsEmptyString( &lt;STRING> ,&lt;VALUE>, &lt;VALUE>) | IsEmptyString(„string“, „yes“, „no„) |
| **NewUUID** | Erzeugt eine neue eindeutige UUID. | NewUUID() | NewUUID() |
| **NoNull** | Gibt die angegebene Zeichenfolge zurück, wenn sie nicht leer ist, und gibt eine leere Zeichenfolge zurück, wenn die angegebene Zeichenfolge leer ist. | NoNull(&lt;STRING>) | NoNull(„test„) |
| **IsBitSet** | Führt ein bitweises AND-Zeichen (&amp;) für die angegebenen Zahlen aus. Auf diese Weise können Sie überprüfen, ob das Bit innerhalb des ersten Parameters an der Position gesetzt ist, die im zweiten Parameter angegeben ist. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Dadurch können Sie das Bit innerhalb des ersten Parameters an der Position löschen, die im zweiten Parameter angegeben ist. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Führt ein bitweises OR (\|) für die angegebenen Zahlen durch. Auf diese Weise können Sie das Bit innerhalb des ersten Parameters wird an der Position gesetzt, die im zweiten Parameter bereitgestellt wird. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Gibt die Zeilennummer zurück. | RowId() | RowId() |
| **ToBoolean** | Konvertiert den Wert in einen booleschen Wert. | toBoolean(&lt;VALUE>) | ToBoolean(a=b) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBool(&lt;VALUE&gt;) | ToBool(a=b) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |

>[!TAB Redshift]

Other functions are not available.

--->

>[!TAB Snowflake]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Case** | Gibt den ersten Wert zurück, wenn der Ausdruck wahr ist. Andernfalls wird der zweite Wert zurückgegeben. | case(when(&lt;EXPRESSION> &lt;VALUE>), else(&lt;VALUE>)) | case(Wenn(a > b, „ja„), Sonst(„nein„)) |
| **When** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um den Ausdruck in der Groß-/Kleinschreibung zu überprüfen. | WHEN(&lt;AUSDRUCK> &lt;WERT>) | Wenn(a > b, „ja„) |
| **Else** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um die andere Option auszuwählen, wenn der Wenn-Ausdruck „false“ ist. | else(&lt;VALUE>) | Sonst („nein„) |
| **GetEmailDomain** | Extrahiert die Domain aus der angegebenen E-Mail-Adresse. | GetEmailDomain(&lt;STRING>) | GetEmailDomain(“sample@example.com„) |
| **Iif** | Gibt die erste Option zurück, wenn die Bedingung wahr ist, und gibt die zweite Option zurück, wenn die Bedingung falsch ist. | IF(&lt;CONDITION>, &lt;VALUE>, &lt;VALUE>) | Iif(10 &lt; 20, „true“, „false„) |
| **IsEmptyString** | Gibt die erste Option zurück, wenn die Zeichenfolge leer ist. Andernfalls wird die zweite Option zurückgegeben. | IsEmptyString( &lt;STRING> ,&lt;VALUE>, &lt;VALUE>) | IsEmptyString(„string“, „yes“, „no„) |
| **ToBoolean** | Gibt 1 zurück, wenn der Wert „true“ ist. Gibt 0 zurück, wenn der Wert „false“ ist. | toBoolean(&lt;VALUE>) | ToBoolean(a=b) |
| **ToBooleanType** | Konvertiert den Wert in einen booleschen Wert. | ToBooleanType(&lt;VALUE>) | ToBooleanType(a=b) |
| **IsBitSet** | Führt ein bitweises AND-Zeichen (&amp;) für die angegebenen Zahlen aus. Auf diese Weise können Sie überprüfen, ob das Bit innerhalb des ersten Parameters an der Position gesetzt ist, die im zweiten Parameter angegeben ist. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Dadurch können Sie das Bit innerhalb des ersten Parameters an der Position löschen, die im zweiten Parameter angegeben ist. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Führt ein bitweises OR (\|) für die angegebenen Zahlen durch. Auf diese Weise können Sie das Bit innerhalb des ersten Parameters wird an der Position gesetzt, die im zweiten Parameter bereitgestellt wird. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Gibt die Zeilennummer zurück. | RowId() | RowId() |
| **NewUUID** | Erzeugt eine neue eindeutige UUID. | NewUUID() | NewUUID() |
| **NoNull** | Gibt die angegebene Zeichenfolge zurück, wenn sie nicht leer ist, und gibt eine leere Zeichenfolge zurück, wenn die angegebene Zeichenfolge leer ist. | NoNull(&lt;STRING>) | NoNull(„test„) |
| **AESEncrypt** | Verschlüsselt die bereitgestellte Zeichenfolge mit dem AES-Verschlüsselungstyp. | AESEncrypt() | AESEncrypt(„hello„) |
| **ObjectConstruct** | Erstellt ein -Objekt basierend auf den bereitgestellten Schlüssel/Wert-Paaren. | ObjectConstruct(&lt;STRING>, &lt;STRING>) | ObjectConstruct(„key“, „value„) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **Coalesce** | Returns the first non-null value. | Coalesce(&lt;VALUE&gt;, &lt;VALUE&gt;) | Coalesce ("", "string") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBoolean(&lt;VALUE&gt;) | ToBoolean(a=b) |

-->

>[!ENDTABS]

### String

Die String-Funktionen dienen der Manipulation einer Reihe von Strings.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Nimmt zwei Zeichenfolgen und prüft, ob alle nicht null und nicht leer sind. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(“&quot;, „string2„) |
| **AllNonNull3** | Nimmt drei Zeichenfolgen und prüft, ob alle nicht null und nicht leer sind | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(“&quot;, „one“, „three„) |
| **Ascii** | Nimmt eine Zeichenfolge und gibt das resultierende zurück. | ASCII(&lt;STRING>) | ASCII („foo„) |
| **Char** | Nimmt ein Array von Unicode-Codepunkten und gibt die resultierende Zeichenfolge zurück. | char(&lt;ARRAY>) | CHAR([65, 68, 79, 66, 69]) |
| **Charindex** | Sucht das erste Vorkommen der angegebenen Unterzeichenfolge innerhalb der Hauptzeichenfolge. | charIndex(&lt;STRING>, &lt;SUBSTRING>) | charIndex (“bar@example.com&quot;, &quot;@„) |
| **dataLength** | Gibt die Anzahl der Bytes in der Zeichenfolge zurück. | dataLength(&lt;STRING>) | dataLength(„My string„) |
| **GetLine** | Gibt die angeforderte Zeile der angegebenen Zeichenfolge zurück. | GetLine(&lt;STRING>, &lt;NUMBER>) | GetLine(multilineString, 5) |
| **IfEquals** | Nimmt vier Zeichenfolgen und gibt die dritte Zeichenfolge zurück, wenn die ersten beiden Zeichenfolgen gleich sind, und gibt die vierte Zeichenfolge zurück, wenn die ersten beiden Zeichenfolgen nicht gleich sind. | ifEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(„a“, „a“, „yes“, „no„) |
| **IsMemoNull** | Gibt 1 zurück, wenn die Zeichenfolge null ist, andernfalls gibt sie 0 zurück. | IsMemoNull(&lt;STRING>) | IsMemoNull(„Hallo„) |
| **JuxtWords** | Nimmt zwei Zeichenfolgen und kombiniert sie zu einer einzigen Zeichenfolge. Leerzeichen zwischen den Zeichenfolgen werden bei Bedarf hinzugefügt. | JustWords(&lt;STRING>, &lt;STRING>) | JustWords(„Hallo“, „Welt„) |
| **JuxtWords3** | Nimmt drei Zeichenfolgen und kombiniert sie zu einer einzigen Zeichenfolge. Leerzeichen zwischen den Zeichenfolgen werden bei Bedarf hinzugefügt. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JustWords3(„Hallo“, „Neu“, „Welt„) |
| **Left** | Nimmt eine Zeichenfolge und gibt die am weitesten links liegenden Zeichen wie angegeben zurück | LEFT(&lt;STRING>, &lt;NUMBER>) | LEFT(„Teilzeichenfolge“, 3) |
| **Length** | Gibt die Länge der Zeichenfolge zurück. | length(&lt;STRING>) | Length(„MyString„) |
| **Md5Digest** | Konvertiert den MD5-Hash-String in seine hexadezimale Darstellung. | md5Digest(&lt;STRING>) | md5Digest(„String„) |
| **MemoContains** | Prüft, ob die Zeichenfolge die bereitgestellte Unterzeichenfolge enthält. | memoContains(&lt;STRING>, &lt;STRING>) | MemoContains(„string“, „str„) |
| **Right** | Nimmt eine Zeichenfolge und gibt die am weitesten rechts liegenden Zeichen wie angegeben zurück. | RIGHT(&lt;STRING>, &lt;NUMBER>) | RIGHT („Teilzeichenfolge“, 3) |
| **Smart** | Gibt die Zeichenfolge zurück, bei der der erste Buchstabe eines jeden Wortes großgeschrieben wird. | Smart(&lt;STRING>) | Smart(„Hallo Welt„) |
| **Substring** | Nehmen Sie eine Zeichenfolge und gibt einen Teil der angegebenen Zeichenfolge zurück, basierend auf den angegebenen Positionen. | Teilzeichenfolge(&lt;STRING>, &lt;LEFT_NUMBER>, RIGHT_NUMBER>) | SUBSTRING(„Teilzeichenfolge“, 3, 5) |
| **Sha256Digest** | Konvertiert die SHA256-gehashte Zeichenfolge in ihre hexadezimale Darstellung. | SHA256Digest(&lt;STRING>) | SHA256Digest(„string„) |
| **Sha512Digest** | Konvertiert die SHA512-gehashte Zeichenfolge in ihre hexadezimale Darstellung. | SHA512Digest(&lt;STRING>) | SHA512Digest(„string„) |
| **ToString** | Gibt den Wert als Zeichenfolge zurück. | ToString(&lt;VALUE>) | ToString(123) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **IsMemoNull** |  Returns 1 if the string is null, otherwise it returns 0. | IsMemoNull(&lt;STRING&gt;) | IsMemoNull("hello") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Redshift]

String functions are not available.

-->

>[!TAB Snowflake]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Nimmt zwei Zeichenfolgen und prüft, ob alle nicht null und nicht leer sind. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(“&quot;, „string2„) |
| **AllNonNull3** | Nimmt drei Zeichenfolgen und prüft, ob alle nicht null und nicht leer sind | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(“&quot;, „one“, „three„) |
| **Char** | Nimmt ein Array von Unicode-Codepunkten und gibt die resultierende Zeichenfolge zurück. | char(&lt;ARRAY>) | CHAR([65, 68, 79, 66, 69]) |
| **Charindex** | Sucht das erste Vorkommen der angegebenen Unterzeichenfolge innerhalb der Hauptzeichenfolge. | charIndex(&lt;STRING>, &lt;SUBSTRING>) | charIndex (“bar@example.com&quot;, &quot;@„) |
| **dataLength** | Gibt die Anzahl der Bytes in der Zeichenfolge zurück. | dataLength(&lt;STRING>) | dataLength(„My string„) |
| **GetLine** | Gibt die angeforderte Zeile der angegebenen Zeichenfolge zurück. | GetLine(&lt;STRING>, &lt;NUMBER>) | GetLine(multilineString, 5) |
| **IfEquals** | Nimmt vier Zeichenfolgen und gibt die dritte Zeichenfolge zurück, wenn die ersten beiden Zeichenfolgen gleich sind, und gibt die vierte Zeichenfolge zurück, wenn die ersten beiden Zeichenfolgen nicht gleich sind. | ifEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(„a“, „a“, „yes“, „no„) |
| **IsMemoNull** | Gibt 1 zurück, wenn die Zeichenfolge null ist, andernfalls gibt sie 0 zurück. | IsMemoNull(&lt;STRING>) | IsMemoNull(„Hallo„) |
| **JuxtWords** | Nimmt zwei Zeichenfolgen und kombiniert sie zu einer einzigen Zeichenfolge. Leerzeichen zwischen den Zeichenfolgen werden bei Bedarf hinzugefügt. | JustWords(&lt;STRING>, &lt;STRING>) | JustWords(„Hallo“, „Welt„) |
| **JuxtWords3** | Nimmt drei Zeichenfolgen und kombiniert sie zu einer einzigen Zeichenfolge. Leerzeichen zwischen den Zeichenfolgen werden bei Bedarf hinzugefügt. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JustWords3(„Hallo“, „Neu“, „Welt„) |
| **Left** | Nimmt eine Zeichenfolge und gibt die am weitesten links liegenden Zeichen wie angegeben zurück | LEFT(&lt;STRING>, &lt;NUMBER>) | LEFT(„Teilzeichenfolge“, 3) |
| **Length** | Gibt die Länge der Zeichenfolge zurück. | length(&lt;STRING>) | Length(„MyString„) |
| **Line** | Gibt die angegebene nummerierte Zeile aus der Zeichenfolge zurück. | LINE(&lt;STRING>, &lt;NUMBER>) | LINE(multiLineString, 5) |
| **Md5Digest** | Konvertiert den MD5-Hash-String in seine hexadezimale Darstellung. | md5Digest(&lt;STRING>) | md5Digest(„String„) |
| **Replace** | Nimmt eine Zeichenfolge und ersetzt alle Instanzen der Teilzeichenfolge durch eine Ersatzteilzeichenfolge. | REPLACE(&lt;STRING>, &lt;STRING&amp;gt, &lt;STRING&amp;gt) | replace(„Captain Steve“, „Captain“, „Engineer„) |
| **Right** | Nimmt eine Zeichenfolge und gibt die am weitesten rechts liegenden Zeichen wie angegeben zurück. | RIGHT(&lt;STRING>, &lt;NUMBER>) | RIGHT („Teilzeichenfolge“, 3) |
| **Sha256Digest** | Konvertiert die SHA256-gehashte Zeichenfolge in ihre hexadezimale Darstellung. | SHA256Digest(&lt;STRING>) | SHA256Digest(„string„) |
| **Sha512Digest** | Konvertiert die SHA512-gehashte Zeichenfolge in ihre hexadezimale Darstellung. | SHA512Digest(&lt;STRING>) | SHA512Digest(„string„) |
| **Smart** | Gibt die Zeichenfolge zurück, bei der der erste Buchstabe eines jeden Wortes großgeschrieben wird. | Smart(&lt;STRING>) | Smart(„Hallo Welt„) |
| **ToString** | Gibt den Wert als Zeichenfolge zurück. | ToString(&lt;VALUE>) | ToString(123) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |

-->

>[!ENDTABS]

### Fenster

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Gibt eine Folge von Zeilen basierend auf der Tabellenpartition und der Sortierreihenfolge zurück. | RowNum(partitionBy(&lt;EXPRESSION>), orderBy(&lt;EXPRESSION>)) | RowNum(partitionBy(division), orderBy(time)) |
| **PartitionBy** | Trennt die Eingabezeilen in verschiedene Partitionen, basierend auf dem gegebenen Ausdruck. | partitionBy(&lt;EXPRESSION>) | partitionBy(division) |
| **OrderBy** | Sortiert das Ergebnis der Partition. | orderBy(&lt;EXPRESSION>) | ORDERBY(Seite) |
| **Desc** | Sortiert OrderBy in absteigender Reihenfolge anstatt in aufsteigender Reihenfolge. | DESC(orderBy(&lt;EXPRESSION>)) | DESC(orderBy(page)) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Redshift]

Window functions are not available.

--->

>[!TAB Snowflake]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Gibt eine Folge von Zeilen basierend auf der Tabellenpartition und der Sortierreihenfolge zurück. | RowNum(partitionBy(&lt;EXPRESSION>), orderBy(&lt;EXPRESSION>)) | RowNum(partitionBy(division), orderBy(time)) |
| **PartitionBy** | Trennt die Eingabezeilen in verschiedene Partitionen, basierend auf dem gegebenen Ausdruck. | partitionBy(&lt;EXPRESSION>) | partitionBy(division) |
| **OrderBy** | Sortiert das Ergebnis der Partition. | orderBy(&lt;EXPRESSION>) | ORDERBY(Seite) |
| **Desc** | Sortiert OrderBy in absteigender Reihenfolge anstatt in aufsteigender Reihenfolge. | DESC(orderBy(&lt;EXPRESSION>)) | DESC(orderBy(page)) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

-->

>[!ENDTABS]
