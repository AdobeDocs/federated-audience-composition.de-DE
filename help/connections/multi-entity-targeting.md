---
audience: end-user
title: Zielgruppenbestimmung durch mehrere Entitäten mit Zielgruppenkomposition in Adobe Journey Optimizer
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Journey Profile aus Zielgruppen mit zusammengeführter Zielgruppenkomposition ansprechen.
source-git-commit: 297a1d5019737c35ee07967a6d7330d3ad0bac1d
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# Zielgruppenbestimmung durch mehrere Entitäten mit Zielgruppenkomposition in Adobe Journey Optimizer

Beim Targeting mit mehreren Entitäten können Sie Zielgruppenattribute für die Federated Audience Composition als zusätzliche Kennungen in Adobe Journey Optimizer Journey verwenden. Mit diesen Attributen können Sie Zielgruppen auf mehreren Entitäten aktivieren, z. B. auf Konto- oder Abonnementebene.

## Erstellen Sie Ihre Zielgruppe in Federated Audience Composition {#create}

Um mit dem Targeting für mehrere Entitäten zu beginnen, müssen Sie zunächst Ihre Audience in Federated Audience Composition erstellen und speichern.

Fügen Sie in der Benutzeroberfläche für die Zielgruppenkomposition die Aktivität **Zielgruppe aufbauen** hinzu, um die Zielgruppe auf der Arbeitsfläche für die Federated Composition zu erstellen, und fügen Sie die Aktivität **Zielgruppe speichern** hinzu, um die Zuordnungen der Zielgruppe, ihre primäre Identität und ihren Datenablauf zu konfigurieren.

![Die Benutzeroberfläche „Federated Audience Composition“ wird angezeigt und zeigt die Zielgruppe an.](/help/connections/assets/multi-entity-targeting/build-activity.png)

Nachdem Sie die Konfigurationen Ihrer Audience abgeschlossen haben, wählen Sie **Starten** aus, um die Ausführung der Komposition zu starten. Diese Zielgruppe und der zugehörige Datensatz stehen in Experience Platform zur Verwendung zur Verfügung.

Weitere Informationen zum Erstellen einer Komposition in der Federated-Audience-Komposition finden Sie im [Handbuch zum Erstellen einer Komposition](/help/compositions/create-composition.md).

## Zielgruppe in Adobe Journey Optimizer aktivieren {#activate}

Nachdem die Ausführung Ihrer Komposition abgeschlossen ist, können Sie die Audience in Journey Optimizer aktivieren. Wählen Sie im Abschnitt **Journey-** von Adobe Journey Optimizer **Journey** gefolgt von **Journey erstellen** aus, um die Journey-Benutzeroberfläche zu öffnen.

![Die Schaltfläche &quot;Journey erstellen“ in Adobe Journey Optimizer ist hervorgehoben.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

Fügen Sie in der Journey-Oberfläche den Knoten **Zielgruppe lesen** hinzu. Sie können diesen Knoten konfigurieren, indem Sie eine Bezeichnung angeben und die zuvor erstellte Zielgruppe auswählen.

![Der Knoten Zielgruppe lesen wird in der Journey Optimizer-Benutzeroberfläche angezeigt.](/help/connections/assets/multi-entity-targeting/read-journey.png)

Nachdem Sie die zuvor erstellte Zielgruppe ausgewählt haben, aktivieren Sie **Zusätzliche Kennung verwenden**.

![Das Kontrollkästchen „Zusätzliche Kennung verwenden“ ist hervorgehoben.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

Sie können jetzt eine zusätzliche Kennung auswählen. Wählen Sie im Auswahlbildschirm die Option **Erweiterter Modus** aus und navigieren Sie zu **Experience Platform**. Klicken Sie auf dieser Seite auf den Namen der zuvor erstellten Zielgruppe und wählen Sie die zusätzliche Kennung aus, die Sie für die Zielgruppe verwenden möchten.

![Der Ausdruckseditor wird angezeigt.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## Konfigurieren von Journey-Bedingungen {#configure-journey}

Nachdem Sie nun Ihre Zielgruppeneinstellungen aktiviert und konfiguriert haben, können Sie mit der Konfiguration der übrigen Bedingungen auf Ihrer Journey fortfahren. Für diesen Anwendungsfall sollten Sie nach dem Knoten **Zielgruppe lesen** **&#x200B;**&#x200B;einen Knoten **Optimizer** hinzufügen.

Wählen Sie nach dem Konfigurieren der verbleibenden Knoten **Veröffentlichen** aus, um die Erstellung der Journey abzuschließen.

![Die Schaltfläche „Veröffentlichen“ ist hervorgehoben.](/help/connections/assets/multi-entity-targeting/select-publish.png)

Ihr Journey richtet sich nun bei den Zielgruppenprofilen nach der **zusätzlichen Kennung** und nicht nach der primären Kennung. Mit dieser Funktion können Sie jetzt mehrere Entitäten wie Abonnement-ID, Konto-ID oder Auftrags-ID auswählen und für Ihren gewünschten Kanal aktivieren.

## Nächste Schritte {#next-steps}

Nach dem Lesen dieses Handbuchs wissen Sie jetzt, wie Sie zusätzliche Kennungen aus Ihren Zielgruppen mit Federated-Audience-Komposition in Journey Optimizer Journey verwenden können. Weitere Informationen zur Verwendung zusätzlicher Journey finden Sie im Handbuch [Verwendung zusätzlicher IDs in Journey](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).
