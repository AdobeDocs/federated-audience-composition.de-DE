---
audience: end-user
title: Aktivität "Deduplizierung"
description: Erfahren Sie, wie Sie die Aktivität Deduplizierung verwenden.
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 92%

---

# Deduplizierung {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Felder zum Identifizieren von Dubletten"
>abstract="Klicken Sie im Abschnitt **Felder zum Identifizieren von Dubletten** auf die Schaltfläche **Attribut hinzufügen**, um die Felder anzugeben, für die die Identifizierung von Dubletten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Aktivität „Deduplizierung“"
>abstract="Mithilfe der Aktivität **Deduplizierung** lassen sich Dubletten in Ergebnissen aus eingehenden Aktivitäten löschen. Sie wird hauptsächlich im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendaten zulassen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Deduplizierungseinstellungen"
>abstract="Um Dubletten in den eingehenden Daten zu löschen, definieren Sie die Deduplizierungsmethode in den folgenden Feldern. Standardmäßig wird nur ein Eintrag beibehalten. Sie sollten außerdem die Deduplizierungsmethode anhand eines Ausdrucks oder Attributs auswählen. Standardmäßig wird der Eintrag, der von den Dubletten ausgenommen sein soll, zufällig ausgewählt."

Die **Deduplizierung** Mithilfe der Aktivität lassen sich Dubletten in Ergebnissen aus eingehenden Aktivitäten löschen, z. B. duplizierte Profile aus der Empfängerliste. Die **Deduplizierungsaktivität** wird im Allgemeinen im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendatum zulassen.

## Konfigurieren der Deduplizierungsaktivität{#deduplication-configuration}

Gehen Sie folgendermaßen vor, um die **Deduplizierungsaktivität** zu konfigurieren:

1. Hinzufügen einer **Deduplizierung** Aktivität zu Ihrer Komposition hinzufügen.

1. Klicken Sie im Abschnitt **Felder zum Identifizieren von Dubletten** auf die Schaltfläche **Attribut hinzufügen**, um die Felder anzugeben, für die die Identifizierung von Dubletten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen.

1. Wählen Sie im Abschnitt **Deduplizierungseinstellungen** die Anzahl der eindeutigen **beizubehaltenden Dubletten** aus. Der Standardwert dieses Felds ist 1. Mittels des Werts 0 lassen sich alle Dubletten beibehalten.

   Nehmen wir z. B. den Fall, dass die Datensätze A und B wie Dubletten des Datensatzes Y und ein Datensatz C wie eine Dublette des Datensatzes Z angesehen werden:

   * Wenn der Wert des Felds 1 ist: nur die Datensätze Y und Z werden beibehalten.
   * Wenn der Wert des Felds 0 ist: alle Datensätze werden beibehalten.
   * Wenn der Wert des Felds 2 ist: Die Datensätze C und Z werden beibehalten und von den Datensätzen A, B und Y werden zwei entweder nach dem Zufallsprinzip oder in Abhängigkeit von der im Anschluss ausgewählten Deduplizierungsmethode beibehalten.

1. Wählen Sie die **Deduplizierungsmethode** aus, die verwendet werden soll:

   * **Automatische Auswahl**: Wählt nach dem Zufallsprinzip unter den Dubletten den Eintrag aus, der beibehalten werden soll.
   * **Von einem Ausdruck ausgehend**: hiermit lassen sich Einträge beibehalten, für die der angegebene Ausdruck den kleinsten oder größten Wert aufweist.
   * **Gemäß einer Werteliste**: ermöglicht die Bestimmung einer Reihenfolge nach Priorität von Werten für ein oder mehrere Felder. Klicken Sie zur Bestimmung dieser Werte auf **Attribute**, um ein Feld auszuwählen, oder erstellen Sie einen Ausdruck und fügen Sie dann den oder die Werte der entsprechenden Tabelle hinzu. Verwenden Sie die Schaltfläche „Hinzufügen“ oberhalb der Werteliste, um ein neues Feld zu definieren.

1. Markieren Sie die Option **Komplement erzeugen**, wenn Sie auch die restliche Population im weiteren Verlauf des Workflows verwenden möchten. Das Komplement enthält in diesem Fall alle Dubletten, und es wird dann eine zusätzliche Transition zur Aktivität hinzugefügt.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
