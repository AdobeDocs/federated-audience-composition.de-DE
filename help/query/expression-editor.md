---
audience: end-user
title: Erstellen Ihrer ersten Abfrage mithilfe des Abfrage-Modelers
description: Erfahren Sie, wie Sie Ihre erste Abfrage im Abfrage-Modeler erstellen.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: ht
source-wordcount: '2066'
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

### Aggregat

Die Aggregatfunktionen dienen der Durchführung von Berechnungen zu einer Reihe von Werten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Avg</strong><br /> </td> 
   <td> Gibt den Durchschnittswert einer Spalte vom Typ Zahl aus<br /> </td> 
   <td> Avg(&lt;Wert&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Count</strong><br /> </td> 
   <td> Zählt die Werte ungleich null einer Spalte<br /> </td> 
   <td> Count(&lt;Wert&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>CountAll</strong><br /> </td> 
   <td> Zählt die ausgegebenen Werte (alle Felder)<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Countdistinct</strong><br /> </td> 
   <td> Zählt die unterschiedlichen Werte ungleich null einer Spalte<br /> </td> 
   <td> Countdistinct(&lt;Wert&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Max</strong><br /> </td> 
   <td> Gibt den Höchstwert einer Spalte vom Typ Zahl, String oder Datum aus<br /> </td> 
   <td> Max(&lt;Wert&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Min</strong><br /> </td> 
   <td> Gibt den Mindestwert einer Spalte vom Typ Zahl, String oder Datum aus<br /> </td> 
   <td> Min(&lt;Wert&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>StdDev</strong><br /> </td> 
   <td> Gibt die Standardabweichung einer Zahl, Zeichenfolge oder Datumsspalte aus<br /> </td> 
   <td> StdDev(&lt;Wert&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>StringAgg</strong><br /> </td> 
   <td> Gibt die Verkettung der Werte einer Spalte vom Typ „String“ zurück, getrennt durch das Zeichen im zweiten Argument<br /> </td> 
   <td> StringAgg(&lt;Wert&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Sum</strong><br /> </td> 
   <td> Gibt die Summe der Werte einer Spalte vom Typ Zahl, String oder Datum aus<br /> </td> 
   <td> Sum(&lt;Wert&gt;)<br /></td> 
  </tr> 
 </tbody> 
</table>

### Datum

Die Datumsfunktionen dienen der Manipulation von Datums- oder Uhrzeitwerten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Tagen hinzu<br /> </td> 
   <td> AddDays(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Stunden hinzu<br /> </td> 
   <td> AddHours(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Minuten hinzu<br /> </td> 
   <td> AddMinutes(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Monaten hinzu<br /> </td> 
   <td> AddMonths(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Sekunden hinzu<br /> </td> 
   <td> AddSeconds(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Jahren hinzu<br /> </td> 
   <td> AddYears(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>ConvertNTZ</strong><br /> </td> 
   <td> Konvertiert NTZ-Zeitstempel (Zeitstempel ohne Zeitzone) in TZ (Zeitstempel mit Zeitzone) unter Anwendung der definierten Sitzungs-Zeitzone<br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;)<br /> </td>  
  </tr>
  <tr> 
   <!--<td> <strong>ConvertTimezone</strong><br /> </td> 
   <td> <br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;)<br /> </td>  
  </tr>-->
  <tr> 
   <td> <strong>DateCmp</strong><br /> </td> 
   <td> Vergleicht zwei Daten<br/> </td> 
   <td> DateCmp(&lt;Datum&gt;,&lt;Datum&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> Gibt nur das Datum aus (mit Uhrzeit = 00:00 Uhr)*<br /> </td> 
   <td> DateOnly(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> Gibt die Zahl aus, die dem Tag des Datums entspricht<br /> </td> 
   <td> Day(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> Gibt die Zahl des Tages im Jahr des angegebenen Datums aus<br /> </td> 
   <td> DayOfYear(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> Gibt das Datum aus, das dem aktuellen Datum abzüglich n Tage entspricht<br /> </td> 
   <td> DaysAgo(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> Gibt das Datum (Integer JJJJMMTT) aus, das dem aktuellen Datum abzüglich n Tage entspricht<br /> </td> 
   <td> DaysAgoInt(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> Anzahl von Tagen zwischen zwei Daten<br /> </td> 
   <td> DaysDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> Gibt das Alter in Tagen in Bezug auf ein Datum aus<br /> </td> 
   <td> DaysOld(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> Gibt das aktuelle Systemdatum des Servers aus<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> Gibt die Stunde der im Datum angegebenen Uhrzeit aus<br /> </td> 
   <td> Hour(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Stunden zwischen zwei Daten aus<br /> </td> 
   <td> HoursDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> Gibt die Minuten der im Datum angegebenen Uhrzeit aus<br /> </td> 
   <td> Minute(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Minuten zwischen zwei Daten aus<br /> </td> 
   <td> MinutesDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> Gibt die Zahl aus, die dem Monat des Datums entspricht<br /> </td> 
   <td> Month(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> Gibt das Datum aus, das dem aktuellen Datum abzüglich n Monate entspricht<br /> </td> 
   <td> MonthsAgo(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Monaten zwischen zwei Daten aus<br /> </td> 
   <td> MonthsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> Gibt das Alter in Monaten in Bezug auf ein Datum aus<br /> </td> 
   <td> MonthsOld(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> Gibt das älteste Datum in einem Bereich zurück<br /> </td> 
   <td> Oldest(&lt;Datum, Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> Gibt die Sekunden der im Datum angegebenen Uhrzeit aus<br /> </td> 
   <td> Second(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Sekunden zwischen zwei Daten aus<br /> </td> 
   <td> SecondsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Tagen vom Datum ab<br /> </td> 
   <td> SubDays(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Stunden vom Datum ab<br /> </td> 
   <td> SubHours(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Minuten vom Datum ab<br /> </td> 
   <td> SubMinutes(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Monaten vom Datum ab<br /> </td> 
   <td> SubMonths(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Sekunden vom Datum ab<br /> </td> 
   <td> SubSeconds(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Jahren vom Datum ab<br /> </td> 
   <td> SubYears(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> Konvertiert eine Angabe Datum+Uhrzeit in Datum alleine<br /> </td> 
   <td> ToDate(&lt;Datum + Uhrzeit&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> Konvertiert einen String in Datum+Uhrzeit<br /> </td> 
   <td> ToDateTime(&lt;String&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToTimestamp</strong><br /> </td> 
   <td> Konvertiert einen String in einen Zeitstempel<br /> </td> 
   <td> ToTimestamp(&lt;String&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToTimeZone</strong><br /> </td> 
   <td> Konvertiert Datum + Uhrzeit in eine Zeitzone<br /> </td> 
   <td> ToTimeZone(&lt;Datum&gt;,&lt;time zone&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> Kürzt die Angabe Datum+Uhrzeit auf Sekunden<br /> </td> 
   <td> TruncDate(@lastModified, &lt;Anzahl Sekunden&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> Kürzt die Angabe Datum+Uhrzeit auf Sekunden<br /> </td> 
   <td> TruncDateTZ(&lt;Datum&gt;, &lt;Anzahl Sekunden&gt;, &lt;Zeitzone&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> Kürzt die Angabe des Datums auf den ersten Tag des Quartals<br /> </td> 
   <td> TruncQuarter(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> Kürzt die Uhrzeitangabe auf Sekunden<br /> </td> 
   <td> TruncTime(&lt;Datum&gt;, &lt;Anzahl Sekunden&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> Kürzt ein Datum auf die Woche<br /> </td> 
   <td> TruncWeek(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> Kürzt die Angabe Datum+Uhrzeit auf den ersten Januar des Jahres<br /> </td> 
   <td> TruncYear(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> Gibt die Zahl des Wochentages in Bezug auf das Datum aus (0=Montag, 6=Sonntag)<br /> </td> 
   <td> WeekDay(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> Gibt die Zahl aus, die dem Jahr des Datums entspricht<br /> </td> 
   <td> Year(&lt;Datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearAndMonth</strong><br /> </td> 
   <td> Gibt Jahr und Monat eines Datums aus<br /> </td> 
   <td> YearAndMonth(&lt;Datum&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>YearsAgo</strong><br /> </td> 
   <td> Gibt die Anzahl von Jahren zwischen einem bestimmten Datum und dem aktuellen Datum wieder<br /> </td> 
   <td> YearsAgo(&lt;date&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Jahren zwischen zwei Daten aus<br /> </td> 
   <td> YearsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> Gibt das Alter in Jahren in Bezug auf ein Datum aus<br /> </td> 
   <td> YearsOld(&lt;Datum&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Beachten Sie, dass die Funktion **Dateonly** nicht die Zeitzone des Benutzers, sondern des Servers verwendet.

### Geomarketing

Die Geomarketing-Funktionen dienen der Manipulation von geografischen Werten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Gibt die Entfernung zwischen zwei durch Längen- und Breitengrad bezeichneten Punkten aus (in Grad).<br /> </td> 
   <td> Distance(&lt;Längengrad A&gt;, &lt;Breitengrad A&gt;, &lt;Längengrad B&gt;, &lt;Breitengrad B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numerisch

Die numerischen Funktionen dienen der Konversion von Text in Zahlen.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Gibt den absoluten Wert einer Zahl aus<br /> </td> 
   <td> Abs(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Gibt die kleinste ganze Zahl aus, die größer oder gleich der angegebenen Zahl ist<br /> </td> 
   <td> Ceil(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Gibt die größte ganze Zahl aus, die kleiner oder gleich der angegebenen Zahl ist<br /> </td> 
   <td> Floor(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Gibt die größere von zwei Zahlen aus<br /> </td> 
   <td> Greatest(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Gibt die kleinere von zwei Zahlen aus<br /> </td> 
   <td> Least(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Gibt den Rest der ganzzahligen Division von n1 durch n2 aus<br /> </td> 
   <td> Mod(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Gibt das Verhältnis zwischen zwei Werten in Prozent aus<br /> </td> 
   <td> Percent(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Gibt einen Zufallswert aus<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Rundet eine Zahl auf n Dezimalstellen<br /> </td> 
   <td> Round(&lt;Zahl&gt;, &lt;Anzahl Dezimalstellen&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Gibt das Vorzeichen einer Zahl aus<br /> </td> 
   <td> Sign(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Konvertiert einen Integer in einen Real<br /> </td> 
   <td> ToDouble(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Konvertiert einen Real in einen 64-Bit-Integer<br /> </td> 
   <td> ToInt64(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Konvertiert einen Real in einen Integer<br /> </td> 
   <td> ToInteger(&lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Kürzt n1 auf n2 Dezimalstellen<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Sonstige

In dieser Tabelle sind die restlichen verfügbaren Funktionen enthalten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> Verschlüsselt den im Argument angegebenen String<br /> </td> 
   <td> AESEncrypt(&lt;Wert&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Gibt Wert 1 zurück, wenn die Bedingung zutrifft. Wenn nicht, wird Wert 2 zurückgegeben.<br /> </td> 
   <td> Case(When(&lt;Bedingung&gt;, &lt;Wert 1&gt;), Else(&lt;Wert 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Löscht das Flag aus dem Wert<br /> </td> 
   <td> ClearBit(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Gibt den Wert 2 aus, wenn der Wert 1 gleich null oder leer ist, sonst den Wert 1<br /> </td> 
   <td> Coalesce(&lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Gibt Wert 3 zurück, wenn Wert 1 = Wert 2 ist. Wenn nicht, wird Wert 4 zurückgegeben.<br /> </td> 
   <td> Decode(&lt;Wert 1&gt;, &lt;Wert 2&gt;, &lt;Wert 3&gt;, &lt;Wert 4&gt;)<br /> </td>  
  </tr> 
  <!--<tr> 
   <td> <strong>DefaultFolder</strong><br /> </td> 
   <td> Returns value 3 if value 1 = value 2. If not returns value 4.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td>  
  </tr> -->
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Gibt den Wert 1 aus (kann nur als Parameter der 'Case'-Funktion verwendet werden)<br /> </td> 
   <td> Else(&lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extrahiert die Domain einer E-Mail-Adresse<br /> </td> 
   <td> GetEmailDomain(&lt;Wert&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Ruft die URL des Mirrorseiten-Servers ab<br /> </td> 
   <td> GetMirrorURL(&lt;Wert&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Gibt Wert 1 aus, wenn die Bedingung zutrifft. Wenn nicht, wird Wert 2 zurückgegeben<br /> </td> 
   <td> Iif(&lt;Bedingung&gt;, &lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Gibt an, ob das Flag im Wert vorkommt<br /> </td> 
   <td> IsBitSet(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Gibt den Wert 2 aus, wenn der String 1 leer ist, sonst den Wert 3<br /> </td> 
   <td> IsEmptyString(&lt;Wert 1&gt;, &lt;Wert 2&gt;, &lt;Wert 3&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> Gibt eine eindeutige ID zurück<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Gibt einen Leerstring aus, wenn das Argument gleich null ist<br /> </td> 
   <td> NoNull(&lt;Wert&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Gibt die Zeilennummer aus<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Setzt das Flag im Wert<br /> </td> 
   <td> SetBit(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen booleschen Wert<br /> </td> 
   <td> ToBoolean(&lt;Zahl&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Gibt Wert 1 aus, wenn die Bedingung zutrifft. Falls nicht, wird Wert 2 zurückgegeben (kann nur als Parameter der Case-Funktion verwendet werden)<br /> </td> 
   <td> When(&lt;Bedingung&gt;, &lt;Wert 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### String

Die String-Funktionen dienen der Manipulation einer Reihe von Strings.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Gibt an, ob alle Parameter ungleich null und nicht leer sind<br /> </td> 
   <td> AllNonNull2(&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Gibt an, ob alle Parameter ungleich null und nicht leer sind<br /> </td> 
   <td> AllNonNull3(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Gibt den ASCII-Wert des ersten Zeichens des Strings aus.<br /> </td> 
   <td> Ascii(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Gibt das ASCII-Code-Zeichen 'n' aus<br /> </td> 
   <td> Char(&lt;Zahl&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Gibt die Position von Zeichenfolge 2 in Zeichenfolge 1 zurück.<br /> </td> 
   <td> Charindex(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> Gibt die Größe der Zeichenfolge in Bytes zurück<br /> </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Gibt die n-te Zeile (beginnend bei 1) des Strings aus<br /> </td> 
   <td> GetLine(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Gibt den dritten Parameter zurück, wenn die ersten beiden Parameter identisch sind. Wenn nicht, wird der letzte Parameter zurückgegeben<br /> </td> 
   <td> IfEquals(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Gibt an, ob das als Parameter ausgegebene Memo gleich null ist<br /> </td> 
   <td> IsMemoNull(&lt;Memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Verkettet die zwei als Parameter übergebenen Zeichenfolgen. Fügt bei Bedarf Leerzeichen zwischen den Zeichenfolgen hinzu.<br /> </td> 
   <td> JuxtWords(&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Verkettet die zwei als Parameter übergebenen Zeichenfolgen. Fügt bei Bedarf Leerzeichen zwischen den Zeichenfolgen hinzu<br /> </td> 
   <td> JuxtWords3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Gibt die n ersten Zeichen des Strings aus<br /> </td> 
   <td> Left(&lt;String&gt;, &lt;Zahl&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Gibt die Länge des Strings aus<br /> </td> 
   <td> Length(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Zeile</strong><br /> </td> 
   <td> Extrahiert Zeile n aus dem String<br /> </td> 
   <td> Line(&lt;String&gt;,&lt;Zahl&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Gibt den String in Kleinbuchstaben aus<br /> </td> 
   <td> Lower(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Gibt den String linksseitig aufgefüllt aus<br /> </td> 
   <td> LPad (&lt;String&gt;, &lt;Number&gt;, &lt;Char&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Löscht die Leerstellen links vom String<br /> </td> 
   <td> Ltrim(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Gibt eine hexadezimale Darstellung des MD5-Schlüssels eines Strings aus<br /> </td> 
   <td> Md5Digest(&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Gibt an, ob das Memo den als Parameter übergebenen String enthält<br /> </td> 
   <td> MemoContains(&lt;Memo&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> Extrahiert den Wert eines XML-Felds aus seinem XPath und den Felddaten<br /> </td> 
   <td> NodeValue (&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Ersetzt alle Vorkommen eines angegebenen String-Werts durch einen anderen String-Wert.<br /> </td> 
   <td> Replace(&lt;String&gt;,&lt;String&gt;,&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Gibt die n letzten Zeichen des Strings aus<br /> </td> 
   <td> Right(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Gibt den String rechtsseitig aufgefüllt aus<br /> </td> 
   <td> RPad(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zeichen&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Löscht die Leerstellen rechts vom String<br /> </td> 
   <td> Rtrim(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Hexadezimale Darstellung des SHA256-Schlüssels einer Zeichenfolge.<br /> </td> 
   <td> Sha256Digest (&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Hexadezimale Darstellung des SHA512-Schlüssels einer Zeichenfolge.<br /> </td> 
   <td> Sha512Digest (&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Gibt jedes Wort des Strings beginnend mit einem Großbuchstaben aus<br /> </td> 
   <td> Smart(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extrahiert aus dem String den Teilstring, der mit dem Zeichen n1 beginnt und die Länge n2 aufweist<br /> </td> 
   <td> Substring(&lt;String&gt;, &lt;Start&gt;, &lt;Länge&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen String<br /> </td> 
   <td> ToString(&lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Gibt den String in Großbuchstaben aus<br /> </td> 
   <td> Upper(&lt;String&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Gibt den Fremdschlüssel einer als erster Parameter übergebenen Relation aus, wenn die beiden anderen Parameter identisch sind<br /> </td> 
   <td> VirtualLink(&lt;Zahl&gt;, &lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Gibt den Fremdschlüssel (Text) einer als erster Parameter übergebenen Relation aus, wenn die beiden anderen Parameter identisch sind<br /> </td> 
   <td> VirtualLinkStr(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Fenster

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Ruft die als ersten Parameter eingegebene SQL-Funktion über die als zweiten Parameter eingegebenen Felder „Partition“ oder „Anordnen nach“ aus<br /> </td> 
   <td> _Over_ (&lt;Value&gt;, &lt;Value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Absteigende Sortierung<br /> </td> 
   <td> Desc(&lt;Wert 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Sortiert das Ergebnis innerhalb der Partition<br /> </td> 
   <td> OrderBy(&lt;Wert 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partitioniert das Ergebnis einer Abfrage<br /> </td> 
   <td> PartitionBy(&lt;Wert 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Erzeugt eine Zeilennummer in Abhängigkeit von der Tabellenpartition und der Sortierreihenfolge<br /> </td> 
   <td> RowNum(PartitionBy(&lt;Wert 1&gt;), OrderBy(&lt;Wert 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
