---
title: Zugreifen auf die Komposition föderierter Zielgruppen
description: Erfahren Sie mehr über die erforderlichen Berechtigungen für die Komposition föderierter Zielgruppen
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 46%

---

# Zugreifen auf die Komposition föderierter Zielgruppen {#feature-access}

## Verwalten des Zugriffs auf Sandboxes {#access-sandboxes}

Wenn Sie die Komposition föderierter Zielgruppen innerhalb von Adobe Experience Platform erwerben, wird zu diesem Zeitpunkt für jede aktive Sandbox ein Produktprofil erstellt. Dieses Produktprofil wird in der Admin Console unter der Produktkarte **Adobe Experience Platform** erstellt und folgt dieser Namenskonvention: `ACP_FAC - <<SandboxName>> - admin.` Für den Zugriff auf die Komposition föderierter Zielgruppen für eine bestimmte Sandbox müssen Benutzende zum Produktprofil hinzugefügt werden, das für diese Sandbox erstellt wurde.

Wirds beispielsweise eine neue Sandbox mit dem Namen „fac-test“ aktiviert, wird das entsprechende Produktprofil „ACP_FAC – fac-test – admin“ erstellt. Um mit dieser Sandbox auf die Komposition föderierter Zielgruppen zugreifen zu können, müssen Benutzende diesem Produktprofil hinzugefügt werden.

## Verwalten des Zugriffs auf die Komposition föderierter Zielgruppen

Für den Zugriff auf **Federated Audience** Komposition) müssen Sie zunächst sicherstellen, dass Sie die erforderlichen Berechtigungen für den Zugriff auf verschiedene Aspekte der Federated Audience-Komposition zuweisen. Diese Rollen müssen dann Benutzern zugewiesen werden, die Zugriff auf &quot;**Zielgruppenkomposition“**.

Beachten Sie, dass Berechtigungen nur von Admins zugewiesen werden können.

1. Navigieren Sie zum Menü **[!UICONTROL Berechtigungen]**.

1. Wählen Sie im Menü **[!UICONTROL Rollen]** die **[!UICONTROL Rolle]** aus, die Sie aktualisieren möchten.

   ![](assets/access_fda_1.png)

1. Wählen **[!UICONTROL Bearbeiten]** aus, um die Berechtigungen Ihrer Rolle zu ändern.

   ![](assets/access_fda_2.png)

1. Fügen Sie die erforderlichen Berechtigungen für den Benutzer hinzu. Sie können die folgenden Zugriffsberechtigungen für die Federated Audience-Komposition hinzufügen:

   | Berechtigung | Beschreibung |
   | ---------- | ----------- |
   | Verknüpfte Daten verwalten | Verwenden Sie diese Berechtigung, um alle Aspekte der Federated Audience-Komposition zu verwalten. Diese Berechtigung setzt die Verwaltung von Federated Database, Federated Schema und Federated Compositions voraus. |
   | Federated Database verwalten | Verwenden Sie diese Berechtigung, um Verbindungen zu Federated Database hinzuzufügen, anzuzeigen, zu aktualisieren und zu löschen. |
   | Federated Database anzeigen | Verwenden Sie diese Berechtigung, um Ihre Verbindungen zu Federated Database anzuzeigen. |
   | Verknüpftes Schema verwalten | Verwenden Sie diese Berechtigung, um Schemata zu erstellen, anzuzeigen, zu aktualisieren, zu löschen und zu aktualisieren. |
   | Anzeigen von Federated Schema-Daten | Verwenden Sie diese Berechtigung, um die Registerkarte „Daten“ im Schemaabschnitt anzuzeigen. |
   | Verknüpftes Schema anzeigen | Verwenden Sie diese Berechtigung, um die Schematabellen anzuzeigen. |
   | Federated Data Model verwalten | Verwenden Sie diese Berechtigung, um Datenmodelle zu erstellen, anzuzeigen, zu aktualisieren und zu löschen. |
   | Federated Data Model anzeigen | Verwenden Sie diese Berechtigung, um die Datenmodelle anzuzeigen. |
   | Audit-Protokoll des Verbands anzeigen | Verwenden Sie diese Berechtigung, um das Audit-Protokoll für die Federated Audience-Komposition anzuzeigen. |
   | Verknüpfte Kompositionen verwalten | Verwenden Sie diese Berechtigung, um zusammengehörige Kompositionen zu erstellen, anzuzeigen, zu aktualisieren und zu löschen. |
   | Verknüpfte Kompositionen anzeigen | Verwenden Sie diese Berechtigung, um zusammengehörige Kompositionen anzuzeigen. |

   ![](assets/permissions.png)

1. Nachdem Sie die erforderlichen Änderungen vorgenommen haben, klicken Sie auf **[!UICONTROL Speichern]**.

Für alle Benutzenden, die dieser Rolle bereits zugewiesen sind, werden die Berechtigungen automatisch aktualisiert und sie erhalten Zugriff auf die Komposition föderierter Zielgruppen.

So weisen Sie diese Rolle neuen Benutzenden zu:

1. Navigieren Sie zur Registerkarte **[!UICONTROL Benutzer]** in Ihrem Rollen-Dashboard und wählen Sie **[!UICONTROL Benutzer hinzufügen]** aus.

   ![](assets/access_fda_4.png)

1. Geben Sie den Namen oder die E-Mail-Adresse der Person ein oder wählen Sie sie aus der verfügbaren Liste aus. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

Die Person erhält dann eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz. Wenn die Person vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).
