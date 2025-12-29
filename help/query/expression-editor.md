---
audience: end-user
title: Erstellen Ihrer ersten Abfrage mithilfe des Abfrage-Modelers
description: Erfahren Sie, wie Sie Ihre erste Abfrage im Abfrage-Modeler erstellen.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: fdf93fb3554d05057052aa7059e141817a883dcc
workflow-type: ht
source-wordcount: '4107'
ht-degree: 100%

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
| **AddYears** | Fügt die angegebene Anzahl von Jahren zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddYears(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | Fügt die angegebene Anzahl von Minuten zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddMonths(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | Fügt die angegebene Anzahl von Tagen zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddDays(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | Fügt die angegebene Anzahl von Stunden zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddHours(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | Fügt die angegebene Anzahl von Minuten zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddMinutes(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | Fügt die angegebene Anzahl von Sekunden zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddSeconds(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | Zieht die angegebene Anzahl von Jahren vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubYears(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | Zieht die angegebene Anzahl von Monaten vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubMonths(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | Zieht die angegebene Anzahl von Tagen vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubDays(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | Zieht die angegebene Anzahl von Stunden vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubHours(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | Zieht die angegebene Anzahl von Minuten vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubMinutes(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | Zieht die angegebene Anzahl von Sekunden vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubSeconds(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | Extrahiert das Jahr aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Month** | Extrahiert den Monat aus dem angegebenen Objekt „Datum/Uhrzeit“. | Month(&lt;DATUM/UHRZEIT>) | Month(&quot;2019-12-15 15:30:00&quot;) |
| **Day** | Extrahiert den Tag aus dem angegebenen Objekt „Datum/Uhrzeit“. | Day(&lt;DATUM/UHRZEIT>) | Day(&quot;2019-12-15 15:30:00&quot;) |
| **DayOfYear** | Extrahiert den Tag des Jahres aus dem angegebenen Objekt „Datum/Uhrzeit“. Wenn der angegebene Wert für „Datum/Uhrzeit“ beispielsweise „2. Februar“ ist, wird „33“ zurückgegeben. | DayOfYear(&lt;DATUM/UHRZEIT>) | DayOfYear(&quot;2019-12-15 15:30:00&quot;) |
| **WeekDay** | Extrahiert den Wochentag aus dem angegebenen Objekt „Datum/Uhrzeit“ als eine Zahl von 0 bis 6, wobei 0 für Sonntag steht. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Hour** | Extrahiert den Stundenwert aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Minute** | Extrahiert den Minutenwert aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Second** | Extrahiert den Sekundenwert aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **YearsDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Jahren an. | YearsDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Monaten an. | MonthsDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Tagen an. | DaysDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Stunden an. | HoursDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Minuten an. | MinutesDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Sekunden an. | SecondsDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **YearsOld** | Gibt den Unterschied zwischen dem angegebenen Datums- und Uhrzeitwert und der aktuellen Zeit mit einer Genauigkeit von Jahren an. | YearsOld(&lt;DATUM/UHRZEIT>) | YearsOld(&quot;2019-12-25 15:30:00&quot;) |
| **MonthsOld** | Gibt den Unterschied zwischen dem angegebenen Datums- und Uhrzeitwert und der aktuellen Zeit mit einer Genauigkeit von Monaten an. | MonthsOld(&lt;DATUM/UHRZEIT>) | MonthsOld(&quot;2019-12-25 15:30:00&quot;) |
| **DaysOld** | Gibt den Unterschied zwischen dem angegebenen Datums- und Uhrzeitwert und der aktuellen Zeit mit einer Genauigkeit von Tagen an. | DaysOld(&lt;DATUM/UHRZEIT>) | DaysOld(&quot;2019-12-25 15:30:00&quot;) |
| **GetDate** | Ruft das aktuelle Datum des Servers ab. | GetDate() | GetDate() |
| **DateOnly** | Kürzt „Datum/Uhrzeit“ auf Jahr, Monat und Tag. | DateOnly(&lt;DATUM/UHRZEIT>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | Konvertiert das Feld in ein Datumsfeld. | ToDate(&lt;DATUM/UHRZEIT>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | Konvertiert das Feld in ein Feld mit Datum und Uhrzeit. | ToDateTime(&lt;DATUM>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | Konvertiert das Feld in ein Zeitstempelfeld. | ToTimestamp(&lt;DATUM/UHRZEIT>) | ToTimestamp(&quot;2019-12-25 15:30:00&quot;) |
| **Oldest** | Gibt das älteste Datum unter den beiden angegebenen zurück. | Oldest(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | Kürzt „Datum/Uhrzeit“ auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3.600 ist, wird auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86.400 ist, wird auf den nächsten Tag gekürzt. Andernfalls wird auf die nächste Sekunde gekürzt. | TruncDate(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | TruncDate(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncDateTZ** | Kürzt „Datum/Uhrzeit“ auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert, und wandelt „Datum/Uhrzeit“ in die angegebene Zeitzone um. Wenn der numerische Wert gleich 60 ist, wird auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3.600 ist, wird auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86.400 ist, wird auf den nächsten Tag gekürzt. | TruncDateTZ(&lt;DATUM/UHRZEIT>, &lt;ZAHL>, &lt;ZEITZONE>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;Amerika/Los_Angeles&quot;) |
| **TruncTime** | Legt „Datum/Uhrzeit“ auf den 1. Januar 2000 fest und rundet den Rest von „Datum/Uhrzeit“ auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3.600 ist, wird auf die nächste Stunde gekürzt. | TruncTime(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | Kürzt „Datum/Uhrzeit“ auf das erste Datum im nächsten Quartal. | TruncQuarter(&lt;DATUM/UHRZEIT>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | Kürzt „Datum/Uhrzeit“ auf das erste Datum im nächsten Jahr. | TruncYear(&lt;DATUM/UHRZEIT>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | Kürzt „Datum/Uhrzeit“ auf den Sonntag der nächsten Woche. | TruncWeek(&lt;DATUM/UHRZEIT>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |

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
| **AddYears** | Fügt die angegebene Anzahl von Jahren zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddYears(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | Fügt die angegebene Anzahl von Minuten zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddMonths(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | Fügt die angegebene Anzahl von Tagen zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddDays(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | Fügt die angegebene Anzahl von Stunden zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddHours(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | Fügt die angegebene Anzahl von Minuten zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddMinutes(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | Fügt die angegebene Anzahl von Sekunden zum angegebenen Datum und zur angegebenen Uhrzeit hinzu. | AddSeconds(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | Zieht die angegebene Anzahl von Jahren vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubYears(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | Zieht die angegebene Anzahl von Monaten vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubMonths(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | Zieht die angegebene Anzahl von Tagen vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubDays(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | Zieht die angegebene Anzahl von Stunden vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubHours(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | Zieht die angegebene Anzahl von Minuten vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubMinutes(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | Zieht die angegebene Anzahl von Sekunden vom angegebenen Datum und der angegebenen Uhrzeit ab. | SubSeconds(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | Extrahiert das Jahr aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Month** | Extrahiert den Monat aus dem angegebenen Objekt „Datum/Uhrzeit“. | Month(&lt;DATUM/UHRZEIT>) | Month(&quot;2019-12-15 15:30:00&quot;) |
| **Day** | Extrahiert den Tag aus dem angegebenen Objekt „Datum/Uhrzeit“. | Day(&lt;DATUM/UHRZEIT>) | Day(&quot;2019-12-15 15:30:00&quot;) |
| **DayOfYear** | Extrahiert den Tag des Jahres aus dem angegebenen Objekt „Datum/Uhrzeit“. Wenn der angegebene Wert für „Datum/Uhrzeit“ beispielsweise „2. Februar“ ist, wird „33“ zurückgegeben. | DayOfYear(&lt;DATUM/UHRZEIT>) | DayOfYear(&quot;2019-12-15 15:30:00&quot;) |
| **WeekDay** | Extrahiert den Wochentag aus dem angegebenen Objekt „Datum/Uhrzeit“ als eine Zahl von 1 bis 7, wobei 1 für Sonntag steht. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Hour** | Extrahiert den Stundenwert aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Minute** | Extrahiert den Minutenwert aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Second** | Extrahiert den Sekundenwert aus dem angegebenen Objekt „Datum/Uhrzeit“. | Year(&lt;DATUM/UHRZEIT>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **YearsDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Jahren an. | YearsDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Monaten an. | MonthsDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Tagen an. | DaysDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Stunden an. | HoursDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Minuten an. | MinutesDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | Gibt den Unterschied zwischen den angegebenen Datums- und Uhrzeitwerten mit einer Genauigkeit von Sekunden an. | SecondsDiff(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsOld** | Gibt den Unterschied zwischen dem angegebenen Datums- und Uhrzeitwert und der aktuellen Zeit mit einer Genauigkeit von Monaten an. | MonthsOld(&lt;DATUM/UHRZEIT>) | MonthsOld(&quot;2019-12-25 15:30:00&quot;) |
| **DaysOld** | Gibt den Unterschied zwischen dem angegebenen Datums- und Uhrzeitwert und der aktuellen Zeit mit einer Genauigkeit von Tagen an. | DaysOld(&lt;DATUM/UHRZEIT>) | DaysOld(&quot;2019-12-25 15:30:00&quot;) |
| **GetDate** | Ruft das aktuelle Datum des Servers ab. | GetDate() | GetDate() |
| **DateOnly** | Kürzt „Datum/Uhrzeit“ auf Jahr, Monat und Tag. | DateOnly(&lt;DATUM/UHRZEIT>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | Konvertiert das Feld in ein Datumsfeld. | ToDate(&lt;DATUM/UHRZEIT>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | Konvertiert das Feld in ein Feld mit Datum und Uhrzeit. | ToDateTime(&lt;DATUM>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | Konvertiert das Feld in ein Zeitstempelfeld. | ToTimestamp(&lt;DATUM/UHRZEIT>) | ToTimestamp(&quot;2019-12-25 15:30:00&quot;) |
| **Oldest** | Gibt das älteste Datum unter den beiden angegebenen zurück. | Oldest(&lt;DATUM/UHRZEIT>, &lt;DATUM/UHRZEIT>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | Kürzt „Datum/Uhrzeit“ auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3.600 ist, wird auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86.400 ist, wird auf den nächsten Tag gekürzt. Andernfalls wird auf die nächste Sekunde gekürzt. | TruncDate(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | TruncDate(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncDateTZ** | Kürzt „Datum/Uhrzeit“ auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert, und wandelt „Datum/Uhrzeit“ in die angegebene Zeitzone um. Wenn der numerische Wert gleich 60 ist, wird auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3.600 ist, wird auf die nächste Stunde gekürzt. Wenn der numerische Wert gleich 86.400 ist, wird auf den nächsten Tag gekürzt. | TruncDateTZ(&lt;DATUM/UHRZEIT>, &lt;ZAHL>, &lt;ZEITZONE>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;Amerika/Los_Angeles&quot;) |
| **TruncTime** | Legt „Datum/Uhrzeit“ auf den 1. Januar 2000 fest und rundet den Rest von „Datum/Uhrzeit“ auf die nächste Einheit, basierend auf dem angegebenen numerischen Wert. Wenn der numerische Wert gleich 60 ist, wird auf die nächste Minute gekürzt. Wenn der numerische Wert gleich 3.600 ist, wird auf die nächste Stunde gekürzt. | TruncTime(&lt;DATUM/UHRZEIT>, &lt;ZAHL>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | Kürzt „Datum/Uhrzeit“ auf das erste Datum im nächsten Quartal. | TruncQuarter(&lt;DATUM/UHRZEIT>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | Kürzt „Datum/Uhrzeit“ auf das erste Datum im nächsten Jahr. | TruncYear(&lt;DATUM/UHRZEIT>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | Kürzt „Datum/Uhrzeit“ auf den Sonntag der nächsten Woche. | TruncWeek(&lt;DATUM/UHRZEIT>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |
| **ConvertNTZ** | Konvertiert einen Zeitstempel ohne Zeitzone in einen Zeitstempel mit Zeitzone. Die angehängte Zeitzone ist die Zeitzone des externen Kontos. | ConvertNTZ(&lt;DATUM/UHRZEIT>) | ConvertNTZ(&quot;2024-06-24 14:43:49&quot;) |

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
>Beachten Sie, dass die Funktion **Dateonly** nicht die Zeitzone der nutzenden Person, sondern des Servers verwendet.

### Geomarketing

Die Geomarketing-Funktionen dienen der Manipulation von geografischen Werten.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Beschreibung | Syntax | Beispiel |
| ---- | ----------- | ------ | ------- |
| **Distance** | Gibt die Entfernung zwischen zwei durch Längen- und Breitengrad definierten Punkten in Grad zurück (als Doppel). | Distance(&lt;ZAHL>, &lt;ZAHL>, &lt;ZAHL>, &lt;ZAHL>) | Distance(40.345, 39.2345, -35.5834, 34.599) |

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
| **Distance** | Gibt die Entfernung zwischen zwei durch Längen- und Breitengrad definierten Punkten in Grad zurück (als Doppel). | Distance(&lt;ZAHL>, &lt;ZAHL>, &lt;ZAHL>, &lt;ZAHL>) | Distance(40.345, 39.2345, -35.5834, 34.599) |

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
| **Mod** | Gibt den Rest der ersten Zahl dividiert durch die zweite Zahl zurück. | Mod(&lt;ZAHL>, &lt;ZAHL>) | Mod(3, 2) |
| **Percent** | Berechnet den Prozentsatz der ersten Zahl von der zweiten Zahl. | Percent(&lt;ZAHL>, &lt;ZAHL>) | Prozent(1, 2) |
| **Random** | Gibt eine zufällige Zahl zwischen 0 (inklusive) und 1 (exklusive) zurück. | Random() | Random() |
| **Round** | Gibt die angegebene Zahl gerundet auf die nächste angeforderte Dezimalstelle zurück. | Round(&lt;ZAHL>, &lt;ZAHL>) | Round(4.5394, 2) |
| **ToDouble** | Konvertiert die angegebene Zahl in ein Doppel. | ToDouble(&lt;ZAHL>) | ToDouble(5) |
| **ToInteger** | Konvertiert die angegebene Zahl in eine Ganzzahl. | ToInteger(&lt;ZAHL>) | ToInteger(45) |
| **ToInt64** | Konvertiert die angegebene Zahl in eine 64-Bit-Ganzzahl. | ToInt64(&lt;ZAHL>) | ToInt64(493) |
| **Trunc** | Kürzt die angegebene Zahl auf die angeforderte Anzahl an Dezimalstellen. | Trunc(&lt;ZAHL>, &lt;ZAHL>) | Trunc(36.9348934, 3) |

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
| **Mod** | Gibt den Rest der ersten Zahl dividiert durch die zweite Zahl zurück. | Mod(&lt;ZAHL>, &lt;ZAHL>) | Mod(3, 2) |
| **Percent** | Berechnet den Prozentsatz der ersten Zahl von der zweiten Zahl. | Percent(&lt;ZAHL>, &lt;ZAHL>) | Prozent(1, 2) |
| **Random** | Gibt eine zufällige Zahl zwischen 0 (inklusive) und 1 (exklusive) zurück. | Random() | Random() |
| **ToDouble** | Konvertiert die angegebene Zahl in ein Doppel. | ToDouble(&lt;ZAHL>) | ToDouble(5) |
| **ToInteger** | Konvertiert die angegebene Zahl in eine Ganzzahl. | ToInteger(&lt;ZAHL>) | ToInteger(45) |
| **ToInt64** | Konvertiert die angegebene Zahl in eine 64-Bit-Ganzzahl. | ToInt64(&lt;ZAHL>) | ToInt64(493) |
| **Trunc** | Kürzt die angegebene Zahl auf die angeforderte Anzahl an Dezimalstellen. | Trunc(&lt;ZAHL>, &lt;ZAHL>) | Trunc(36.9348934, 3) |

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
| **Case** | Gibt ersten Wert zurück, wenn der Ausdruck wahr ist. Andernfalls wird der zweite Wert zurückgegeben. | Case(When(&lt;AUSDRUCK> &lt;WERT>), Else(&lt;WERT>)) | Case(When(a > b, &quot;ja&quot;), Else(&quot;nein&quot;)) |
| **When** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um den Ausdruck in der Case-Funktion zu überprüfen. | When(&lt;AUSDRUCK> &lt;WERT>) | When(a > b, &quot;ja&quot;) |
| **Else** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um die andere Option auszuwählen, wenn der When-Ausdruck falsch ist. | Else(&lt;VALUE>) | Else (&quot;nein&quot;) |
| **Coalesce** | Gibt den ersten Nicht-Null-Wert zurück. | Coalesce(&lt;WERT>, &lt;WERT>) | Coalesce (&quot;&quot;, &quot;String&quot;) |
| **Decode** | Gibt die erste Option zurück, wenn die Werte gleich sind. Gibt die zweite Option zurück, wenn die Werte nicht gleich sind. | Decode(&lt;WERT>, &lt;WERT>, &lt;WERT>, &lt;WERT>) | Decode(1, 2, &quot;wahr&quot;, &quot;falsch&quot;) |
| **GetEmailDomain** | Extrahiert die Domain der angegebenen E-Mail-Adresse. | GetEmailDomain(&lt;STRING>) | GetEmailDomain(&quot;beispiel@beispiel.com&quot;) |
| **Iif** | Gibt die erste Option zurück, wenn die Bedingung wahr ist, und gibt die zweite Option zurück, wenn die Bedingung falsch ist. | Iif(&lt;BEDINGUNG>, &lt;WERT>, &lt;WERT>) | Iif(10 &lt; 20, &quot;wahr&quot;, &quot;falsch&quot;) |
| **IsEmptyString** | Gibt die erste Option zurück, wenn der String leer ist. Andernfalls wird die zweite Option zurückgegeben. | IsEmptyString( &lt;STRING> ,&lt;WERT>, &lt;WERT>) | IsEmptyString(&quot;String&quot;, &quot;ja&quot;, &quot;nein&quot;) |
| **NewUUID** | Generiert eine neue eindeutige UUID. | NewUUID() | NewUUID() |
| **NoNull** | Gibt den angegebenen String zurück, wenn er nicht leer ist, und gibt einen leeren String zurück, wenn der angegebene String leer ist. | NoNull(&lt;STRING>) | NoNull(&quot;Test&quot;) |
| **IsBitSet** | Führt ein bitweises Und (&amp;) für die angegebenen Zahlen durch. Auf diese Weise können Sie überprüfen, ob das Bit innerhalb des ersten Parameters auf die Position festgelegt ist, die im zweiten Parameter angegeben ist. | IsBitSet(&lt;ZAHL>, &lt;ZAHL>) | IsBitSet(5, 3) |
| **ClearBit** | Dadurch können Sie das Bit innerhalb des ersten Parameters an der Position löschen, die im zweiten Parameter angegeben ist. | ClearBit(&lt;ZAHL>, &lt;ZAHL>) | |
| **SetBit** | Führt ein bitweises Oder (\|) für die angegebenen Zahlen durch. Dadurch können Sie das Bit innerhalb des ersten Parameters für die Position festlegen, die im zweiten Parameter angegeben ist. | SetBit(&lt;ZAHL>, &lt;ZAHL>) | SetBit(5, 3) |
| **RowId** | Gibt die Zeilennummer zurück. | RowId() | RowId() |
| **ToBoolean** | Konvertiert den Wert in einen booleschen Wert. | ToBoolean(&lt;WERT>) | ToBoolean(a=b) |

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
| **Case** | Gibt ersten Wert zurück, wenn der Ausdruck wahr ist. Andernfalls wird der zweite Wert zurückgegeben. | Case(When(&lt;AUSDRUCK> &lt;WERT>), Else(&lt;WERT>)) | Case(When(a > b, &quot;ja&quot;), Else(&quot;nein&quot;)) |
| **When** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um den Ausdruck in der Case-Funktion zu überprüfen. | When(&lt;AUSDRUCK> &lt;WERT>) | When(a > b, &quot;ja&quot;) |
| **Else** | Wird als Teil der Case-Funktion verwendet. Wird verwendet, um die andere Option auszuwählen, wenn der When-Ausdruck falsch ist. | Else(&lt;VALUE>) | Else (&quot;nein&quot;) |
| **GetEmailDomain** | Extrahiert die Domain der angegebenen E-Mail-Adresse. | GetEmailDomain(&lt;STRING>) | GetEmailDomain(&quot;beispiel@beispiel.com&quot;) |
| **Iif** | Gibt die erste Option zurück, wenn die Bedingung wahr ist, und gibt die zweite Option zurück, wenn die Bedingung falsch ist. | Iif(&lt;BEDINGUNG>, &lt;WERT>, &lt;WERT>) | Iif(10 &lt; 20, &quot;wahr&quot;, &quot;falsch&quot;) |
| **IsEmptyString** | Gibt die erste Option zurück, wenn der String leer ist. Andernfalls wird die zweite Option zurückgegeben. | IsEmptyString( &lt;STRING> ,&lt;WERT>, &lt;WERT>) | IsEmptyString(&quot;String&quot;, &quot;ja&quot;, &quot;nein&quot;) |
| **ToBoolean** | Gibt „1“ zurück, wenn der Wert wahr ist. Gibt „0“ zurück, wenn der Wert falsch ist. | ToBoolean(&lt;WERT>) | ToBoolean(a=b) |
| **ToBooleanType** | Konvertiert den Wert in einen booleschen Wert. | ToBooleanType(&lt;WERT>) | ToBooleanType(a=b) |
| **IsBitSet** | Führt ein bitweises Und (&amp;) für die angegebenen Zahlen durch. Auf diese Weise können Sie überprüfen, ob das Bit innerhalb des ersten Parameters auf die Position festgelegt ist, die im zweiten Parameter angegeben ist. | IsBitSet(&lt;ZAHL>, &lt;ZAHL>) | IsBitSet(5, 3) |
| **ClearBit** | Dadurch können Sie das Bit innerhalb des ersten Parameters an der Position löschen, die im zweiten Parameter angegeben ist. | ClearBit(&lt;ZAHL>, &lt;ZAHL>) | |
| **SetBit** | Führt ein bitweises Oder (\|) für die angegebenen Zahlen durch. Dadurch können Sie das Bit innerhalb des ersten Parameters für die Position festlegen, die im zweiten Parameter angegeben ist. | SetBit(&lt;ZAHL>, &lt;ZAHL>) | SetBit(5, 3) |
| **RowId** | Gibt die Zeilennummer zurück. | RowId() | RowId() |
| **NewUUID** | Generiert eine neue eindeutige UUID. | NewUUID() | NewUUID() |
| **NoNull** | Gibt den angegebenen String zurück, wenn er nicht leer ist, und gibt einen leeren String zurück, wenn der angegebene String leer ist. | NoNull(&lt;STRING>) | NoNull(&quot;Test&quot;) |
| **AESEncrypt** | Verschlüsselt den angegebenen String mit dem AES-Verschlüsselungstyp. | AESEncrypt() | AESEncrypt(&quot;hallo&quot;) |
| **ObjectConstruct** | Erstellt ein Objekt basierend auf den angegebenen Schlüssel/Wert-Paaren. | ObjectConstruct(&lt;STRING>, &lt;STRING>) | ObjectConstruct(&quot;Schlüssel&quot;, &quot;Wert&quot;) |

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
| **AllNonNull2** | Nimmt zwei Strings und überprüft, ob alle nicht null und nicht leer sind. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(&quot;&quot;, &quot;String2&quot;) |
| **AllNonNull3** | Nimmt drei Strings und überprüft, ob alle nicht null und nicht leer sind | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(&quot;&quot;, &quot;eins&quot;, &quot;drei&quot;) |
| **Ascii** | Nimmt einen String und gibt das Ergebnis zurück. | Ascii(&lt;STRING>) | Ascii (&quot;foo&quot;) |
| **Char** | Nimmt ein Array von Unicode-Code-Punkten und gibt den resultierenden String zurück. | Char(&lt;ARRAY>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Gibt das erste Vorkommen der angegebenen Unterzeichenfolge innerhalb der Hauptzeichenfolge an. | Charindex(&lt;STRING>, &lt;SUBSTRING>) | Charindex(&quot;bar@beispiel.com&quot;, &quot;@&quot;) |
| **dataLength** | Gibt die Anzahl der Byte im String zurück. | dataLength(&lt;STRING>) | dataLength(&quot;Mein String&quot;) |
| **GetLine** | Gibt die angeforderte Zeile des angegebenen Strings zurück. | GetLine(&lt;STRING>, &lt;ZAHL>) | GetLine(multilinestring, 5) |
| **IfEquals** | Nimmt vier Strings und gibt den dritten String zurück, wenn die ersten beiden Strings gleich sind, und gibt den vierten String zurück, wenn die ersten beiden Strings nicht gleich sind. | IfEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;ja&quot;, &quot;nein&quot;) |
| **IsMemoNull** | Gibt „1“ zurück, wenn der String null ist. Andernfalls wird „0“ zurückgegeben. | IsMemoNull(&lt;STRING>) | IsMemoNull(&quot;hallo&quot;) |
| **JuxtWords** | Nimmt zwei Strings und kombiniert sie zu einem einzigen String. Leerzeichen zwischen den Strings werden bei Bedarf hinzugefügt. | JuxtWords(&lt;STRING>, &lt;STRING>) | JuxtWords(&quot;Hallo&quot;, &quot;Welt&quot;) |
| **JuxtWords3** | Nimmt drei Strings und kombiniert sie zu einem einzigen String. Leerzeichen zwischen den Strings werden bei Bedarf hinzugefügt. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JuxtWords3(&quot;Hallo&quot;, &quot;Neue&quot;, &quot;Welt&quot;) |
| **Left** | Nimmt einen String und gibt das Zeichen ganz links zurück, wie angegeben. | Left(&lt;STRING>, &lt;ZAHL>) | Left(&quot;Unterzeichenfolge&quot;, 3) |
| **Length** | Gibt die Länge des Strings zurück. | Length(&lt;STRING>) | Length(&quot;Mein String&quot;) |
| **Md5Digest** | Konvertiert den MD5-Hash-String in seine hexadezimale Darstellung. | Md5Digest(&lt;STRING>) | Md5Digest(&quot;String&quot;) |
| **MemoContains** | Prüft, ob der String die angegebene Unterzeichenfolge enthält. | MemoContains(&lt;STRING>, &lt;STRING>) | MemoContains(&quot;String&quot;, &quot;str&quot;) |
| **Right** | Nimmt einen String und gibt das Zeichen ganz rechts zurück, wie angegeben. | Right(&lt;STRING>, &lt;NUMBER>) | Right(&quot;Unterzeichenfolge&quot;, 3) |
| **Smart** | Gibt jedes Wort des Strings beginnend mit einem Großbuchstaben zurück. | Smart(&lt;STRING>) | Smart(&quot;hallo welt&quot;) |
| **Substring** | Nimmt einen String und gibt einen Teil des angegebenen Strings zurück, basierend auf den angegebenen Positionen. | Substring(&lt;STRING>, &lt;LINKE_ZAHL>,&lt;RECHTE_ZAHL>) | Substring(&quot;Unterzeichenfolge&quot;, 3, 5) |
| **Sha256Digest** | Konvertiert den SHA256-Hash-String in seine hexadezimale Darstellung. | Sha256Digest(&lt;STRING>) | Sha256Digest(&quot;String&quot;) |
| **Sha512Digest** | Konvertiert den SHA512-Hash-String in seine hexadezimale Darstellung. | Sha512Digest(&lt;STRING>) | Sha512Digest(&quot;String&quot;) |
| **ToString** | Gibt den Wert als String zurück. | ToString(&lt;WERT>) | ToString(123) |

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
| **AllNonNull2** | Nimmt zwei Strings und überprüft, ob alle nicht null und nicht leer sind. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(&quot;&quot;, &quot;String2&quot;) |
| **AllNonNull3** | Nimmt drei Strings und überprüft, ob alle nicht null und nicht leer sind | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(&quot;&quot;, &quot;eins&quot;, &quot;drei&quot;) |
| **Char** | Nimmt ein Array von Unicode-Code-Punkten und gibt den resultierenden String zurück. | Char(&lt;ARRAY>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Gibt das erste Vorkommen der angegebenen Unterzeichenfolge innerhalb der Hauptzeichenfolge an. | Charindex(&lt;STRING>, &lt;SUBSTRING>) | Charindex(&quot;bar@beispiel.com&quot;, &quot;@&quot;) |
| **dataLength** | Gibt die Anzahl der Byte im String zurück. | dataLength(&lt;STRING>) | dataLength(&quot;Mein String&quot;) |
| **GetLine** | Gibt die angeforderte Zeile des angegebenen Strings zurück. | GetLine(&lt;STRING>, &lt;ZAHL>) | GetLine(multilinestring, 5) |
| **IfEquals** | Nimmt vier Strings und gibt den dritten String zurück, wenn die ersten beiden Strings gleich sind, und gibt den vierten String zurück, wenn die ersten beiden Strings nicht gleich sind. | IfEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;ja&quot;, &quot;nein&quot;) |
| **IsMemoNull** | Gibt „1“ zurück, wenn der String null ist. Andernfalls wird „0“ zurückgegeben. | IsMemoNull(&lt;STRING>) | IsMemoNull(&quot;hallo&quot;) |
| **JuxtWords** | Nimmt zwei Strings und kombiniert sie zu einem einzigen String. Leerzeichen zwischen den Strings werden bei Bedarf hinzugefügt. | JuxtWords(&lt;STRING>, &lt;STRING>) | JuxtWords(&quot;Hallo&quot;, &quot;Welt&quot;) |
| **JuxtWords3** | Nimmt drei Strings und kombiniert sie zu einem einzigen String. Leerzeichen zwischen den Strings werden bei Bedarf hinzugefügt. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JuxtWords3(&quot;Hallo&quot;, &quot;Neue&quot;, &quot;Welt&quot;) |
| **Left** | Nimmt einen String und gibt das Zeichen ganz links zurück, wie angegeben. | Left(&lt;STRING>, &lt;ZAHL>) | Left(&quot;Unterzeichenfolge&quot;, 3) |
| **Length** | Gibt die Länge des Strings zurück. | Length(&lt;STRING>) | Length(&quot;Mein String&quot;) |
| **Line** | Gibt die angegebene nummerierte Zeile aus dem String zurück. | Line(&lt;STRING>, &lt;ZAHL>) | Line(multilinestring, 5) |
| **Md5Digest** | Konvertiert den MD5-Hash-String in seine hexadezimale Darstellung. | Md5Digest(&lt;STRING>) | Md5Digest(&quot;String&quot;) |
| **Replace** | Nimmt einen String und ersetzt alle Instanzen der Unterzeichenfolge mit einer Ersatzunterzeichenfolge. | Replace(&lt;STRING>, &lt;STRING&amp;gt, &lt;STRING&amp;gt) | Replace(&quot;Kapitän Steve&quot;, &quot;Kapitän&quot;, &quot;Ingenieur&quot;) |
| **Right** | Nimmt einen String und gibt das Zeichen ganz rechts zurück, wie angegeben. | Right(&lt;STRING>, &lt;NUMBER>) | Right(&quot;Unterzeichenfolge&quot;, 3) |
| **Sha256Digest** | Konvertiert den SHA256-Hash-String in seine hexadezimale Darstellung. | Sha256Digest(&lt;STRING>) | Sha256Digest(&quot;String&quot;) |
| **Sha512Digest** | Konvertiert den SHA512-Hash-String in seine hexadezimale Darstellung. | Sha512Digest(&lt;STRING>) | Sha512Digest(&quot;String&quot;) |
| **Smart** | Gibt jedes Wort des Strings beginnend mit einem Großbuchstaben zurück. | Smart(&lt;STRING>) | Smart(&quot;hallo welt&quot;) |
| **ToString** | Gibt den Wert als String zurück. | ToString(&lt;WERT>) | ToString(123) |

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
| **RowNum** | Gibt eine Reihenfolge von Zeilen basierend auf der Tabellenpartition und der Sortierreihenfolge zurück. | RowNum(PartitionBy(&lt;AUSDRUCK>), OrderBy(&lt;AUSDRUCK>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Trennt die Eingabezeilen in verschiedene Teile, basierend auf dem angegebenen Ausdruck. | PartitionBy(&lt;AUSDRUCK>) | PartitionBy(division) |
| **OrderBy** | Sortiert das Ergebnis innerhalb der Partition. | OrderBy(&lt;AUSDRUCK>) | OrderBy(age) |
| **Desc** | Sortiert „OrderBy“ in absteigender Reihenfolge anstatt in aufsteigender Reihenfolge. | Desc(OrderBy(&lt;AUSDRUCK>)) | Desc(OrderBy(age)) |

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
| **RowNum** | Gibt eine Reihenfolge von Zeilen basierend auf der Tabellenpartition und der Sortierreihenfolge zurück. | RowNum(PartitionBy(&lt;AUSDRUCK>), OrderBy(&lt;AUSDRUCK>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Trennt die Eingabezeilen in verschiedene Teile, basierend auf dem angegebenen Ausdruck. | PartitionBy(&lt;AUSDRUCK>) | PartitionBy(division) |
| **OrderBy** | Sortiert das Ergebnis innerhalb der Partition. | OrderBy(&lt;AUSDRUCK>) | OrderBy(age) |
| **Desc** | Sortiert „OrderBy“ in absteigender Reihenfolge anstatt in aufsteigender Reihenfolge. | Desc(OrderBy(&lt;AUSDRUCK>)) | Desc(OrderBy(age)) |

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
