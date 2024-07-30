---
audience: end-user
title: Arbeiten mit Zielgruppen
description: Erfahren Sie, wie Sie mit Zielgruppen arbeiten
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 27%

---

# Arbeiten mit Zielgruppen {#gs-audiences}

Mit der Experience Platform Federated Audience Komposition können Sie [Kompositionen erstellen](../compositions/gs-compositions.md), wo Sie verschiedene Aktivitäten in einer visuellen Arbeitsfläche nutzen können, um Zielgruppen zu erstellen und in Adobe Experience Platform Audience Portal zu speichern.

Sie können diese Zielgruppe dann in Journey Optimizer als Ziel auswählen oder für ein beliebiges von Adobe Experience Platform unterstütztes Ziel aktivieren.

## Zielgruppenerstellung mit Kompositionen {#creation}

Um Zielgruppen mithilfe der Komposition &quot;Federated Audience&quot;zu erstellen, müssen Sie eine Komposition mit der Aktivität **[!UICONTROL Audience-Speicherung]** erstellen. Mit dieser Aktivität können Sie die Zielgruppe in Audience Portal speichern und Felder aus Ihren externen Datenbanken auswählen, die in die Zielgruppe aufgenommen werden sollen. [Erfahren Sie, wie Sie eine Aktivität „Zielgruppe speichern“ konfigurieren können](../compositions/activities/save-audience.md)

Die mit der Adobe Federated Data Komposition erstellte Zielgruppe umfasst alle in der Aktivität **[!UICONTROL Audience-Speicherung]** ausgewählten Felder und wird in Audience Portal neben allen Adobe Experience Platform-Zielgruppen gespeichert.

Nach der Ausführung der Komposition wird die resultierende Zielgruppe in Adobe Experience Platform als externe Zielgruppe gespeichert und in der Echtzeit-Kundendatenplattform von Adobe und/oder Adobe Journey Optimizer verfügbar gemacht.

Sie können diese Zielgruppen für jedes von Adobe Experience Platform unterstützte Ziel aktivieren. Erfahren Sie, wie Sie mit Zielen in [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"} arbeiten.

>[!NOTE]
>
>Zielgruppen, die mithilfe der Komposition föderierter Zielgruppen erstellt wurden, können nicht bearbeitet werden. Um Änderungen an einer dieser Zielgruppen vorzunehmen, müssen Sie mithilfe einer Komposition eine neue Zielgruppe erstellen.

## Auf Ihre Zielgruppe in Adobe Experience Platform zugreifen {#access-audience}

Mit Federated Audience Komposition erstellte Zielgruppen werden in Audience Portal zugänglich gemacht, auf das über das Menü **Zielgruppen** zugegriffen werden kann.

Auf der Registerkarte **[!UICONTROL Durchsuchen]** werden alle in Adobe Experience Platform gespeicherten Zielgruppen aufgelistet. Sie können die Zielgruppen der Komposition föderierter Zielgruppen in der Liste mithilfe der Spalte **[!UICONTROL Herkunft]** oder der im linken Bereich verfügbaren Filter identifizieren.

![](assets/audiences-list.png)

Weitere Informationen zum Arbeiten mit Zielgruppen in Adobe Experience Platform finden Sie in der [Audience Portal-Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"} .

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->