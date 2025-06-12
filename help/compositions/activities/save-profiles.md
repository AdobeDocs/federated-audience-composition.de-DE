---
audience: end-user
title: Verwenden der Aktivität „Profile speichern“
description: Erfahren Sie, wie Sie die Aktivität „Profile speichern“ verwenden
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: ca975be136155f69bc84362fde8c283b1c4edffe
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 55%

---

# Speichern von Profilen {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Speichern von Profilen"
>abstract="Die Aktivität „Profile speichern“ ermöglicht es, Experience Platform-Profile anzureichern, indem Daten aus externen Warehouses föderiert werden, sodass Kundenprofile mit zusätzlichen Attributen erweitert werden können. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Experience Platform-Schema auswählen"
>abstract="Auswahl des Experience Platform-Schema für die Profile."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Auswählen des primären Identifizierungsfelds"
>abstract="Auswahl der primären Identität zur Identifizierung der Zielgruppenprofile in der Datenbank."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Experience Platform-Schema auswählen"
>abstract="Auswahl des Experience Platform-Schema für die Profile."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="Aktualisierungsmodus für Profil speichern"
>abstract="Die verfügbaren Aktualisierungsmodi für die Aktivität Profil speichern umfassen eine vollständige Aktualisierung und eine inkrementelle Aktualisierung."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Vollständige Aktualisierung"
>abstract="Der Modus Vollständige Aktualisierung aktualisiert den vollständigen Satz an Profilen für die Anreicherung."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Inkrementelle Aktualisierung"
>abstract="Der Modus für inkrementelle Aktualisierungen aktualisiert die Profile, die seit der letzten Anreicherung geändert wurden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Feld „Primärer Identitätswert“"
>abstract="Das Feld Primäre Identität gibt die Datenquelle an, die beim Zusammenführen von Profilen für die Anreicherung verwendet wird."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Erforderliche Felder und Kriterien"
>abstract="Ein erforderliches Feld ist ein Attribut, das beim Exportieren von Daten für jedes Profil oder jeden Datensatz ausgefüllt werden muss. Wenn ein erforderliches Feld fehlt, ist der Export weder vollständig noch gültig."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Kriterien für Primäre Identitätsfelder"
>abstract="Die eindeutige Kennung für jedes Profil oder jeden Datensatz. Dadurch wird sichergestellt, dass jeder Datensatz eindeutig erkannt und abgeglichen werden kann, was eine Duplizierung der Daten verhindert."

Die Aktivität **Profile speichern** ermöglicht es Ihnen, Adobe Experience Platform-Profile mit aus externen Warehouses föderierten Daten anzureichern.

Diese Aktivität wird in der Regel verwendet, um Kundenprofile zu verbessern, indem zusätzliche Attribute und Einblicke eingebracht werden, ohne die Daten physisch in die Plattform zu verschieben oder zu duplizieren.

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
