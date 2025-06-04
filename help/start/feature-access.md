---
title: Zugreifen auf die Komposition föderierter Zielgruppen
description: Erfahren Sie mehr über die erforderlichen Berechtigungen für die Komposition föderierter Zielgruppen
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 100%

---

# Zugreifen auf die Komposition föderierter Zielgruppen {#feature-access}

## Verwalten des Zugriffs auf Sandboxes {#access-sandboxes}

Wenn Sie die Komposition föderierter Zielgruppen innerhalb von Adobe Experience Platform erwerben, wird zu diesem Zeitpunkt für jede aktive Sandbox ein Produktprofil erstellt. Dieses Produktprofil wird in der Admin Console unter der Produktkarte **Adobe Experience Platform** erstellt und folgt dieser Namenskonvention: `ACP_FAC - <<SandboxName>> - admin.` Für den Zugriff auf die Komposition föderierter Zielgruppen für eine bestimmte Sandbox müssen Benutzende zum Produktprofil hinzugefügt werden, das für diese Sandbox erstellt wurde.

Wirds beispielsweise eine neue Sandbox mit dem Namen „fac-test“ aktiviert, wird das entsprechende Produktprofil „ACP_FAC – fac-test – admin“ erstellt. Um mit dieser Sandbox auf die Komposition föderierter Zielgruppen zugreifen zu können, müssen Benutzende diesem Produktprofil hinzugefügt werden.

## Verwalten des Zugriffs auf die Komposition föderierter Zielgruppen

Um auf die **Komposition föderierter Zielgruppen** zugreifen zu können, müssen Sie zunächst sicherstellen, dass Sie die erforderlichen Berechtigungen für den Zugriff auf verschiedene Aspekte der Komposition föderierter Zielgruppen zuweisen. Diese Rollen müssen dann Benutzenden zugewiesen werden, die Zugriff auf die **Komposition föderierter Zielgruppen** benötigen.

Beachten Sie, dass Berechtigungen nur von Admins zugewiesen werden können.

1. Navigieren Sie zum Menü **[!UICONTROL Berechtigungen]**.

1. Wählen Sie im Menü **[!UICONTROL Rollen]** die **[!UICONTROL Rolle]** aus, die Sie aktualisieren möchten.

   ![](assets/access_fda_1.png)

1. Wählen Sie **[!UICONTROL Bearbeiten]** aus, um die Berechtigungen Ihrer Rolle zu ändern.

   ![](assets/access_fda_2.png)

1. Fügen Sie die erforderlichen Berechtigungen für die Benutzerin bzw. den Benutzer hinzu. Sie können die folgenden Zugriffsberechtigungen für die Komposition föderierter Zielgruppen hinzufügen:

   | Berechtigung | Beschreibung |
   | ---------- | ----------- |
   | Föderierte Daten verwalten | Verwenden Sie diese Berechtigung, um alle Aspekte der Komposition föderierter Zielgruppen zu verwalten. Diese Berechtigung umfasst die Berechtigungen „Föderierte Datenbank verwalten“, „Föderiertes Schema verwalten“, „Föderiertes Datenmodell verwalten“ und „Föderierte Kompositionen verwalten“. |
   | Föderierte Datenbank verwalten | Verwenden Sie diese Berechtigung, um Verbindungen zu föderierten Datenbanken hinzuzufügen, diese anzuzeigen, zu aktualisieren und zu löschen. |
   | Föderierte Datenbank anzeigen | Verwenden Sie diese Berechtigung, um Ihre Verbindungen zu föderierten Datenbanken anzuzeigen. |
   | Föderiertes Schema verwalten | Verwenden Sie diese Berechtigung, um Schemata zu erstellen, anzuzeigen, zu ändern, zu löschen und zu aktualisieren. |
   | Föderierte Schemadaten anzeigen | Verwenden Sie diese Berechtigung, um die Registerkarte „Daten“ im Abschnitt „Schema“ anzuzeigen. |
   | Föderiertes Schema anzeigen | Verwenden Sie diese Berechtigung, um Schematabellen anzuzeigen. |
   | Föderiertes Datenmodell verwalten | Verwenden Sie diese Berechtigung, um Datenmodelle zu erstellen, anzuzeigen, zu aktualisieren und zu löschen. |
   | Föderiertes Datenmodell anzeigen | Verwenden Sie diese Berechtigung, um Datenmodelle anzuzeigen. |
   | Audit-Protokoll der Föderation anzeigen | Verwenden Sie diese Berechtigung, um das Audit-Protokoll für die Komposition föderierter Zielgruppen anzuzeigen. |
   | Föderierte Kompositionen verwalten | Verwenden Sie diese Berechtigung, um föderierte Kompositionen zu erstellen, anzuzeigen, zu aktualisieren und zu löschen. |
   | Föderierte Kompositionen anzeigen | Verwenden Sie diese Berechtigung, um föderierte Kompositionen anzuzeigen. |

   ![](assets/permissions.png)

1. Nachdem Sie die erforderlichen Änderungen vorgenommen haben, wählen Sie **[!UICONTROL Speichern]** aus.

Für alle Benutzenden, die dieser Rolle bereits zugewiesen sind, werden die Berechtigungen automatisch aktualisiert und sie erhalten Zugriff auf die Komposition föderierter Zielgruppen.

So weisen Sie diese Rolle neuen Benutzenden zu:

1. Navigieren Sie im Dashboard für Ihre Rolle zur Registerkarte **[!UICONTROL Benutzer]** und wählen Sie **[!UICONTROL Benutzer hinzufügen]** aus.

   ![](assets/access_fda_4.png)

1. Geben Sie den Namen oder die E-Mail-Adresse der Person ein oder wählen Sie sie aus der verfügbaren Liste aus. Wenn Sie fertig sind, wählen Sie **[!UICONTROL Speichern]** aus.

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

Die Person erhält dann eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz. Wenn die Person vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).
