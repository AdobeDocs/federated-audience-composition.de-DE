---
audience: end-user
title: Zielgruppenbestimmung für mehrere Entitäten mit Zielgruppen aus der Komposition föderierter Zielgruppen in Adobe Journey Optimizer
description: Erfahren Sie, wie Sie die Zielgruppenbestimmung für Profile aus Zielgruppen der Komposition föderierter Zielgruppen in Adobe Journey Optimizer-Journeys vornehmen.
source-git-commit: 79f05c5a1b025b522a1b88615973d9fe383e3720
workflow-type: ht
source-wordcount: '496'
ht-degree: 100%

---


# Zielgruppenbestimmung für mehrere Entitäten mit Zielgruppen aus der Komposition föderierter Zielgruppen in Adobe Journey Optimizer

Mit der Zielgruppenbestimmung für mehrere Entitäten können Sie Zielgruppenattribute aus der Komposition föderierter Zielgruppen als ergänzende Kennungen in Adobe Journey Optimizer-Journeys verwenden. Diese Attribute ermöglichen Ihnen die Aktivierung von Zielgruppen auf der Ebene mehrerer Entitäten, wie z. B. von Konten oder Abonnements.

## Erstellen Sie Ihre Zielgruppe in der Komposition föderierter Zielgruppen {#create}

Um mit der Zielgruppenbestimmung für mehrere Entitäten zu beginnen, müssen Sie zunächst Ihre Zielgruppe in der Komposition föderierter Zielgruppen erstellen und speichern.

Fügen Sie auf der Benutzeroberfläche für die Zielgruppenkomposition die Aktivität **Zielgruppe erstellen** hinzu, um die Zielgruppe auf der Arbeitsfläche für die föderierte Komposition zu erstellen, und fügen Sie die Aktivität **Zielgruppe speichern** hinzu, um die Zuordnungen, die primäre Identität und den Datenablauf der Zielgruppe zu konfigurieren.

![Die Benutzeroberfläche der Komposition föderierter Zielgruppen wird angezeigt, in der die Zielgruppe dargestellt ist.](/help/connections/assets/multi-entity-targeting/build-activity.png)

Sobald Sie die Konfigurationen Ihrer Zielgruppe abgeschlossen haben, wählen Sie **Starten** aus, um die Ausführung der Komposition zu starten. Diese Zielgruppe und der entsprechende Datensatz stehen zur Verwendung in Experience Platform zur Verfügung.

Weitere Informationen zum Erstellen einer Komposition in der Komposition föderierter Zielgruppen finden Sie im [Handbuch zum Erstellen einer Komposition](/help/compositions/create-composition.md).

## Aktivieren von Zielgruppen in Adobe Journey Optimizer {#activate}

Nachdem die Ausführung Ihrer Komposition abgeschlossen ist, können Sie die Zielgruppe in Journey Optimizer aktivieren. Wählen Sie im Abschnitt **Journey-Management** von Adobe Journey Optimizer die Option **Journeys** aus und anschließend **Journey erstellen**, um die Journey-Benutzeroberfläche zu öffnen.

![Die Schaltfläche „Journey erstellen“ in Adobe Journey Optimizer ist hervorgehoben.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

Fügen Sie in der Journey-Benutzeroberfläche den Knoten **Zielgruppe lesen** hinzu. Sie können diesen Knoten konfigurieren, indem Sie ein Label angeben und die zuvor erstellte Zielgruppe auswählen.

![Der Knoten „Zielgruppe lesen“ wird in der Journey Optimizer-Benutzeroberfläche angezeigt.](/help/connections/assets/multi-entity-targeting/read-journey.png)

Aktivieren Sie nach Auswahl der zuvor erstellten Zielgruppe die Option **Zusätzliche Kennung verwenden**.

![Das Kontrollkästchen „Zusätzliche Kennung verwenden“ ist hervorgehoben.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

Sie können nun eine zusätzliche Kennung auswählen. Wählen Sie im Auswahlbildschirm die Option **Erweiterter Modus** aus und navigieren Sie zu **Experience Platform**. Wählen Sie auf dieser Seite den Namen der zuvor erstellten Zielgruppe aus und bestimmen Sie die zusätzliche Kennung, die Sie für die Zielgruppe verwenden möchten.

![Der Ausdruckseditor wird angezeigt.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## Konfigurieren von Journey-Bedingungen {#configure-journey}

Nachdem Sie nun Ihre Zielgruppeneinstellungen aktiviert und konfiguriert haben, können Sie mit der Konfiguration der restlichen Journey-Bedingungen fortfahren. Für diesen Anwendungsfall fügen Sie nach dem Knoten **Zielgruppe lesen** einen Knoten vom Typ **Optimizer** und danach einen Knoten vom Typ **Aktion** hinzu.

Wählen Sie nach dem Konfigurieren der restlichen Knoten **Veröffentlichen** aus, um die Erstellung der Journey abzuschließen.

![Die Schaltfläche „Veröffentlichen“ ist hervorgehoben.](/help/connections/assets/multi-entity-targeting/select-publish.png)

Ihre Journey spricht nun die Zielgruppenprofile auf Basis der **zusätzlichen Kennung** anstelle der primären Kennung an. Mithilfe dieser Funktion können Sie nun mehrere Entitäten wie die Abonnement-ID, die Konto-ID oder die Bestellungs-ID ansprechen und für Ihren gewünschten Kanal aktivieren.

## Nächste Schritte {#next-steps}

Nach dem Lesen dieses Handbuchs wissen Sie nun, wie Sie zusätzliche Kennungen aus Ihren Zielgruppen der Komposition föderierter Zielgruppen in Journey Optimizer-Journeys verwenden. Weitere Informationen zur Verwendung zusätzlicher Journeys finden Sie im [Handbuch zum Verwenden zusätzlicher Kennungen in Journeys](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

