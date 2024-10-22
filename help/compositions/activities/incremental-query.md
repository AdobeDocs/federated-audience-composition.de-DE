---
audience: end-user
title: Verwenden der Aktivität „Inkrementelle Abfrage“
description: Erfahren Sie, wie Sie die Aktivität „Inkrementelle Abfrage“ verwenden.
hide: true
hidefromtoc: true
source-git-commit: 34d6fc8f97c491fcb91eebf8e1377018e5020a4a
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 100%

---

# Inkrementelle Abfrage {#incremental-query}

<!-- Warning : contextual help IDs are declared in /start/get-started.md-->

Mit der Aktivität **Inkrementelle Abfrage** können Sie regelmäßige Datenbankabfragen durchführen. Bei jeder neuen Ausführung dieser Aktivität werden die Ergebnisse der vorangehenden Ausführungen ausgeschlossen. Dadurch lassen sich ausschließlich neue Elemente abrufen.

**[!UICONTROL Inkrementelle Abfragen]** kommen in verschiedenen Kontexten zum Einsatz:

* Segmentierung von Einzelpersonen, um beispielsweise Zielgruppen für eine Nachricht zu definieren.
* Export von Daten.  Beispielsweise können Sie die Aktivität verwenden, um regelmäßig neue Protokolle in Dateien zu exportieren. Diese Funktion kann verwendet werden, wenn Sie Ihre Protokolldaten in externen Berichterstellungs- oder Business Intelligence Tools verwenden möchten.

Die bereits bei früheren Ausführungen ausgewählte Population wird in der Komposition gespeichert. Das bedeutet, dass zwei Kompositionen, die aus derselben Vorlage gestartet werden, nicht dasselbe Protokoll verwenden. Zwei Aufgaben, die auf derselben inkrementellen Abfrage in derselben Komposition basieren, verwenden jedoch dasselbe Protokoll.

Wenn das Ergebnis einer inkrementellen Abfrage bei einer ihrer Ausführungen gleich 0 ist, wird die Komposition bis zur nächsten geplanten Ausführung der Abfrage angehalten. Die auf die inkrementelle Abfrage folgenden Transitionen und Aktivitäten werden daher nicht vor der folgenden Ausführung verarbeitet.

## Konfigurieren der Aktivität „Inkrementelle Abfrage“ {#incremental-query-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Inkrementelle Abfrage** zu konfigurieren:

1. Fügen Sie die Aktivität **Inkrementelle Abfrage** in Ihre Komposition ein.

1. Wählen Sie im Abschnitt **[!UICONTROL Zielgruppe]** die **Zielgruppendimension** und klicken Sie dann auf **[!UICONTROL Weiter]**.

   Mit der Zielgruppendimension können Sie die Population definieren, auf welche der Vorgang abzielt: Empfängerinnen und Empfänger, Vertragsbegünstigte, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw. Standardmäßig wird die Zielgruppe aus den Empfängerinnen und Empfängern ausgewählt. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Verwenden Sie den Abfrage-Modeler, um Ihre Abfrage zu definieren, genauso wie Sie eine Zielgruppe beim Entwerfen einer neuen E-Mail erstellen. [Erfahren Sie mehr über die Arbeit mit dem Abfrage-Modeler](../../query/query-modeler-overview.md)

1. Wählen Sie im Abschnitt **[!UICONTROL Verarbeitete Daten]** den zu verwendenden inkrementellen Modus aus:

   * **[!UICONTROL Ergebnisse der vorherigen Ausführung ausschließen]**: Bei jeder neuen Ausführung dieser Aktivität werden die Ergebnisse der vorangehenden Ausführungen ausgeschlossen.

     Die bereits in früheren Ausführungen ausgewählten Einträge können ab dem Tag, an dem sie ausgewählt wurden, bis zu einer Höchstzahl von Tagen protokolliert werden. Verwenden Sie dazu das Feld **[!UICONTROL Verlauf in Tagen]**. Wenn dieser Wert null ist, werden die Empfangenden nie aus dem Protokoll gelöscht.

   * **[!UICONTROL Datumsfeld verwenden]**: Mit dieser Option können Sie Ergebnisse früherer Ausführungen basierend auf einem bestimmten Datumsfeld ausschließen. Wählen Sie dazu das gewünschte Datumsfeld aus der Liste der Attribute aus, die für die ausgewählte Zielgruppendimension verfügbar sind. Bei den nächsten Ausführungen der Komposition werden nur Daten abgerufen, die nach dem Datum der letzten Ausführung geändert oder erstellt wurden.

     Nach der ersten Ausführung der Komposition wird das Feld **[!UICONTROL Letztes Ausführungsdatum]** verfügbar. Es gibt das Datum an, das für die nächste Ausführung verwendet wird, und wird bei jeder Ausführung der Komposition automatisch aktualisiert. Sie können bei Bedarf diesen Wert auch überschreiben, indem Sie einen neuen eingeben.

   >[!NOTE]
   >
   >Der Modus **[!UICONTROL Datumsfeld verwenden]** ermöglicht je nach ausgewähltem Datumsfeld größere Flexibilität. Wenn das angegebene Feld beispielsweise ein Änderungsdatum ist, können Sie mit dem Modus „Datumsfeld“ Daten abrufen, die kürzlich aktualisiert wurden. Dagegen werden im anderen Modus Einträge ausgeschlossen, die schon in einer früheren Ausführung abgerufen worden waren, selbst wenn diese Daten seit der letzten Ausführung der Komposition geändert wurden.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
