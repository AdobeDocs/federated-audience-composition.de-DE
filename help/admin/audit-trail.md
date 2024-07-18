---
audience: end-user
title: Erste Schritte mit dem Audit-Protokoll
description: Erfahren Sie, wie Sie Ihre Datenbanken mit dem Audit-Protokoll überwachen.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: bdef7049ee78c512857adcf7d587066eaf80046e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 69%

---

# Erste Schritte mit dem Audit-Protokoll {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="Audit-Protokoll"
>abstract="Die Funktion „Audit-Protokoll“ bietet eine detaillierte und chronologische Übersicht aller Aktionen und Ereignisse, die in Echtzeit an Ihrer Umgebung durchgeführt wurden."

Die Funktion &quot;Audit&quot; bietet eine detaillierte und chronologische Aufzeichnung aller Aktionen und Ereignisse, die in Echtzeit an Ihrer Umgebung vorgenommen wurden

Die Funktion **[!UICONTROL Audit trail]** zeichnet ständig ein detailliertes Protokoll von Aktionen und Ereignissen auf, die in der Adobe-Datenkompositionsinstanz in Echtzeit stattfinden. Dies bietet eine einfache Methode, um auf einen chronologischen Dateneintrag mit Abfragen zuzugreifen, wie zum Status von Workflows, den Personen, die diese geändert haben oder den Aktivitäten, die von Benutzerinnen und Benutzern innerhalb der Instanz ausgeführt wurden.

+++ Weitere Informationen über die verfügbaren Entitäten im Audit-Protokoll

* Mit dem **Source-Schema-Audit-Protokoll** können Sie Aktivitäten und aktuelle Änderungen an Ihren Schemas in der Adobe-Datenkompositionsinstanz überwachen.

  Detaillierte Informationen zu Schemata finden Sie auf dieser [Seite](../customer/schemas.md).

* Das **Workflow-Audit-Protokoll** ermöglicht es Ihnen, Aktivitäten und aktuelle Änderungen an Workflows zu verfolgen, einschließlich der aktuellen Status wie:

   * Starten
   * Aussetzen
   * Stoppen
   * Neu starten
   * Bereinigen, was der Aktion „Verlauf bereinigen“ entspricht
   * Simulieren, was der Aktion „Starten“ im Simulationsmodus entspricht
   * Wecken, was der Aktion „Vorgezogene Ausführung der ausstehenden Aufgaben“ entspricht
   * Unbedingter Stopp

  Weiterführende Informationen zu Workflows finden Sie auf [dieser Seite](../compositions/gs-compositions.md).

* Mit **Externes Konto** können Sie Änderungen an externen Konten in der Adobe-Datenkompositionsinstanz überprüfen.

  Weiterführende Informationen zu „Externes Konto“ finden Sie auf [dieser Seite](../connections/federated-db.md).

+++

## Zugriff auf das Audit-Protokoll {#accessing-audit-trail}

So greifen auf das **[!UICONTROL Audit-Protokoll]** Ihrer Instanz zu:

1. Wählen Sie im Menü **[!UICONTROL Federated data]** die Option **[!UICONTROL Audit-Protokoll]** aus.

1. Das Fenster **[!UICONTROL Audit-Protokoll]** wird mit der Liste Ihrer Entitäten geöffnet. Die Adobe Campaign Web-Benutzeroberfläche protokolliert die Aktionen zum Erstellen, Bearbeiten und Löschen von Workflows, Optionen, Sendungen oder Schemata.

   ![](assets/audit_trail.png)

1. Im Fenster **[!UICONTROL Audit-Entität]** erhalten Sie detailliertere Informationen zu der ausgewählten Entität, z. B.:

   * **[!UICONTROL Typ]**: Workflow, Optionen, Sendungen oder Schemata.
   * **[!UICONTROL Entität]**: Interner Name Ihrer Aktivitäten.
   * **[!UICONTROL Geändert von]**: Benutzername der Person, die diese Entität zuletzt geändert hat.
   * **[!UICONTROL Aktion]**: Letzte Aktion, die für diese Entität ausgeführt wurde, entweder „Erstellt“, „Geändert“ oder „Gelöscht“.
   * **[!UICONTROL Änderungsdatum]**: Datum der letzten Aktion, die an dieser Entität durchgeführt wurde.
