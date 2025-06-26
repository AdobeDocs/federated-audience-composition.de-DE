---
title: Zugriffssteuerung bei der Komposition einer zusammengeführten Zielgruppe
description: Erfahren Sie, wie Sie den Datenzugriff für Benutzende in Federated Audience Composition verwalten.
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: a26e5a2b106426113764d3f2f668ddfbbff85b01
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 80%

---

# Zugriffssteuerung bei der Komposition einer zusammengeführten Zielgruppe

Sie können die Zugriffssteuerung verwenden, um rollenbasierten Zugriff auf Sandboxes und die Federated Audience-Komposition bereitzustellen.

## Verwalten des Zugriffs auf Sandboxes {#access-sandboxes}

Wenn Sie die Komposition föderierter Zielgruppen innerhalb von Adobe Experience Platform erwerben, wird zu diesem Zeitpunkt für jede aktive Sandbox ein Produktprofil erstellt. Dieses Produktprofil wird in der Admin Console unter der Produktkarte **Adobe Experience Platform** erstellt und folgt dieser Namenskonvention: `ACP_FAC - <<SandboxName>> - admin.` Für den Zugriff auf die Komposition föderierter Zielgruppen für eine bestimmte Sandbox müssen Benutzende zum Produktprofil hinzugefügt werden, das für diese Sandbox erstellt wurde.

Wirds beispielsweise eine neue Sandbox mit dem Namen „fac-test“ aktiviert, wird das entsprechende Produktprofil „ACP_FAC – fac-test – admin“ erstellt. Um mit dieser Sandbox auf die Komposition föderierter Zielgruppen zugreifen zu können, müssen Benutzende diesem Produktprofil hinzugefügt werden.

## Verwalten des Zugriffs auf die Komposition föderierter Zielgruppen

Sie können den Zugriff verwalten, indem Sie die erforderlichen Berechtigungen für den Zugriff auf verschiedene Aspekte der Federated Audience Composition zuweisen. Diese Berechtigungen werden über Rollen Benutzern zugewiesen, die Zugriff auf **Federated Audience Composition** benötigen.

>[!NOTE]
>
>Nur Administratoren können anderen Benutzern Berechtigungen zuweisen.

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

Sie können den Benutzenden auch abhängig von den jeweils benötigten Berechtigungen eine der bereits vorhandenen Rollen zuweisen. Weitere Informationen zum Zuweisen bereits vorhandener Rollen zu Benutzenden finden Sie im [Handbuch zur Benutzerverwaltung für ein Produktprofil](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

| Rollenname | Berechtigungen |
| --------- | ----------- |
| Komposition föderierter Zielgruppen – Daten-Managerinnen und -Manager | <ul><li>Föderierte Kompositionen verwalten</li><li>Föderierte Datenbanken anzeigen</li><li>Föderierte Schemata anzeigen</li><li>Föderierte Schemadaten anzeigen</li><li>Föderierte Datenmodelle anzeigen</li></ul> |
| Komposition föderierter Zielgruppen – Kompositions-Managerinnen und -Manager | <ul><li>Föderierte Kompositionen verwalten</li></ul> |
| Komposition föderierter Zielgruppen – Administratorinnen und Administratoren | <ul><li>Föderierte Daten verwalten</li></ul> |

Die Person erhält dann eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz. Wenn die Person vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).

## Zugriff auf bestimmte Kompositionen verwalten

Sie können den Zugriff auf eine bestimmte Komposition verwalten, indem Sie Zugriffsbeschriftungen anwenden.

Weiterführende Informationen zum Anwenden von Zugriffsbeschriftungen auf eine Komposition finden Sie im Abschnitt [Anwenden von Zugriffsbeschriftungen](/help/compositions/gs-compositions.md#access-labels) des Kompositionshandbuchs.
