---
audience: end-user
title: Verwenden der Aktivität Audience-Speicherung
description: Erfahren Sie, wie Sie die Aktivität Audience-Speicherung verwenden
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: 3b891232a3a671f8ec12e06b19086f12ef849f1e
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 28%

---

# Zielgruppe speichern {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Speichern einer Zielgruppe"
>abstract="Verwenden Sie diese Aktivität, um eine neue Audience aus der zuvor in der Komposition berechneten Population zu erstellen. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste hinzugefügt und sind über das Menü **Zielgruppen** zugänglich."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Ausgehende Transition generieren"
>abstract="Verwenden Sie diese Option, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Feld „Primärer Identitätswert“"
>abstract="Wählen Sie die primäre Identität aus, die für Profile verwendet werden soll."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Identity-Namespace"
>abstract="Wählen Sie den Namespace aus, der für Profile verwendet werden soll."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces" text="Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Platform"

Mit der Aktivität **Audience-Speicherung** können Sie eine neue Audience aus der zuvor in einer Komposition berechneten Population erstellen. Die erstellten Audiences werden der Adobe Experience Platform-Zielgruppenliste hinzugefügt und über das Menü **Audiences** verfügbar gemacht. [Erfahren Sie, wie Sie mit Zielgruppen arbeiten können](../../start/audiences.md)

Diese Aktivität dient im Wesentlichen dazu, innerhalb derselben Komposition berechnete Populationen in wiederverwendbare Zielgruppen umzuwandeln. Verbinden Sie sie mit anderen Zielgruppenbestimmungsaktivitäten, wie etwa den Aktivitäten **Zielgruppe aufbauen** oder **Kombinieren**.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe aufbauen** zu konfigurieren:

1. Fügen Sie Ihrer Komposition die Aktivität **Audience-Speicherung** hinzu.

   ![](../assets/save-audience.png)

1. Geben Sie den Titel der zu erstellenden Audience an.

   >[!IMPORTANT]
   >
   >Die Zielgruppenbeschriftung muss innerhalb der aktuellen Sandbox eindeutig sein. Sie darf nicht mit der einer existierenden Zielgruppe übereinstimmen.

1. Wählen Sie im Abschnitt Zielgruppenzuordnungen die Felder aus, die Sie mit der neu erstellten Zielgruppe übernehmen möchten. Klicken Sie dazu auf **Zielgruppenzuordnung hinzufügen** und wählen Sie dann die Quell- und Zielgruppenfelder aus.

   Wiederholen Sie den Vorgang, um beliebig viele Zielgruppen-Mappings hinzuzufügen.

1. Wählen Sie die primäre Identität und den Namespace aus, die zur Identifizierung der Zielprofile in der Datenbank verwendet werden sollen:

   * **Primäres Identitätsfeld**: Wählen Sie das Feld aus, das zur Identifizierung der Profile verwendet werden soll. Beispielsweise die E-Mail-Adresse oder Telefonnummer.
   * **Identitäts-Namespace**: Wählen Sie den Namespace aus, der zur Identifizierung der Profile verwendet werden soll, d. h. den Datentyp, der als Identifizierungsschlüssel verwendet werden soll. Wenn beispielsweise die E-Mail-Adresse als primäres Identitätsfeld ausgewählt wurde, sollte der Identitäts-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

## Auf Ihre Zielgruppe in Adobe Experience Platform zugreifen {#access-audience}

Nach der Ausführung der Komposition wird die resultierende Zielgruppe in Adobe Experience Platform als externe Zielgruppe gespeichert und in der Echtzeit-Kundendatenplattform von Adobe und/oder Adobe Journey Optimizer verfügbar gemacht. Sie ist im Menü **Zielgruppen** verfügbar. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

Die erstellte Zielgruppe enthält alle Felder, die im Abschnitt Zielgruppenzuordnungen ausgewählt wurden. Sie können diese Zielgruppe in Journey Optimizer auswählen oder für ein beliebiges Ziel aktivieren, das von Adobe Experience Platform unterstützt wird.

[Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
