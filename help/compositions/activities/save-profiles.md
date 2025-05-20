---
audience: end-user
title: Verwenden der Aktivität „Profile speichern“
description: Erfahren Sie, wie Sie die Aktivität „Profile speichern“ verwenden
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: fae57356b8e9f5358a39d31cad4883171a310fb6
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 100%

---

# Speichern von Profilen {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Speichern von Profilen"
>abstract="Die Aktivität „Profile speichern“ ermöglicht es Ihnen, Experience Platform-Profile anzureichern, indem Sie Daten aus externen Warehouses föderieren, sodass Sie Kundenprofile mit zusätzlichen Attributen erweitern können. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Auswählen eines AEP-Schemas"
>abstract="Wählen Sie das Experience Platform-Schema für die Profile aus."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Auswählen des primären Identifizierungsfelds"
>abstract="Wählen Sie die primäre Identität zur Identifizierung der Zielgruppenprofile in der Datenbank aus."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Auswählen eines AEP-Schemas"
>abstract="Wählen Sie das Experience Platform-Schema für die Profile aus."

Die Aktivität **Profile speichern** ermöglicht es Ihnen, Adobe Experience Platform-Profile mit aus externen Warehouses föderierten Daten anzureichern.

Diese Aktivität wird in der Regel verwendet, um Kundenprofile zu verbessern, indem zusätzliche Attribute und Erkenntnisse eingebracht werden, ohne die Daten physisch in die Plattform zu verschieben oder zu duplizieren

## Konfigurieren der Aktivität „Profile speichern“ {#save-profile-configuration}

Gehen Sie wie folgt vor, um die Aktivität **Profile speichern** zu konfigurieren:

1. Fügen Sie Ihrer Komposition die Aktivität **Profile speichern** hinzu.

   ![](../assets/save-profile.png)

1. Geben Sie das Label der zu erstellenden Profile an.

   >[!IMPORTANT]
   >
   >Das Zielgruppen-Label muss innerhalb der aktuellen Sandbox eindeutig sein. Es darf nicht mit dem Label einer vorhandenen Zielgruppe übereinstimmen.

1. Wählen Sie das Adobe Experience Platform-Schema aus, das verwendet werden soll.

   ![](../assets/save-profile-2.png)

1. Wählen Sie das primäre Identitätsfeld zur Identifizierung von Profilen in der Datenbank.

1. Um weitere Datenattribute abzustimmen, klicken Sie auf **Attribute hinzufügen**.

   Geben Sie dann das Feld **Quelle** (externe Daten) und **Ziel** (Schemafeld) für jedes Attribut an, das zugeordnet werden soll.

   ![](../assets/save-profile-3.png)

1. Klicken Sie nach der Konfiguration auf **Start**.
