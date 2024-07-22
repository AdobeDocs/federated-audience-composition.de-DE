---
audience: end-user
title: Verwenden der Aktivität Audience-Speicherung
description: Erfahren Sie, wie Sie die Aktivität Audience-Speicherung verwenden
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 6e04c42bf4b83448673851b97227faf953638d1e
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 42%

---


# Zielgruppe speichern {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Speichern einer Zielgruppe"
>abstract="Mit dieser Aktivität können Sie eine vorhandene Zielgruppe aktualisieren oder eine neue Zielgruppe aus der Population erstellen, die im Vorfeld der Komposition ermittelt wurde. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste hinzugefügt und sind über das Menü **Zielgruppen** zugänglich."

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

Mit der Aktivität **Audience-Speicherung** können Sie eine vorhandene Audience aktualisieren oder eine neue Audience aus der zuvor in einer Komposition berechneten Population erstellen. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste in Adobe Campaign hinzugefügt und sind über das Menü **Zielgruppen** zugänglich.

Diese Aktivität dient im Wesentlichen dazu, innerhalb derselben Komposition berechnete Populationen in wiederverwendbare Zielgruppen umzuwandeln. Verbinden Sie sie mit anderen Zielgruppenbestimmungsaktivitäten, wie etwa den Aktivitäten **Zielgruppe aufbauen** oder **Kombinieren**.

## Konfigurieren der Aktivität „Zielgruppe speichern“ {#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe aufbauen** zu konfigurieren:

1. Fügen Sie Ihrer Komposition die Aktivität **Audience-Speicherung** hinzu.

   ![](../assets/save-audience.png)

1. Geben Sie den Titel der zu erstellenden Audience an.

   >[!IMPORTANT]
   >
   >Die Zielgruppenbeschriftung muss innerhalb der aktuellen Sandbox eindeutig sein. Sie darf nicht mit der einer existierenden Zielgruppe übereinstimmen.

1. Klicken Sie auf **Zielgruppenzuordnung hinzufügen** und wählen Sie dann die Quell- und Zielgruppenfelder aus:

   * **Source Audience Field**:
   * **Zielgruppenfeld der Zielgruppe auswählen**:

   Wiederholen Sie den Vorgang, um beliebig viele Zielgruppen-Mappings hinzuzufügen.

1. Wählen Sie die primäre Identität und den Namespace aus, die zur Identifizierung der Zielprofile in der Datenbank verwendet werden sollen:

   * **Primäres Identitätsfeld**: Wählen Sie das Feld aus, das zur Identifizierung der Profile verwendet werden soll. Beispielsweise die E-Mail-Adresse oder Telefonnummer.
   * **Identitäts-Namespace**: Wählen Sie den Namespace aus, der zur Identifizierung der Profile verwendet werden soll, d. h. den Datentyp, der als Identifizierungsschlüssel verwendet werden soll. Wenn beispielsweise die E-Mail-Adresse als primäres Identitätsfeld ausgewählt wurde, sollte der Identitäts-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

Nach dem Ausführen der Komposition wird die resultierende Zielgruppe in Adobe Experience Platform <!-- to check--> gespeichert und im Menü **Zielgruppen** zugänglich gemacht.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
