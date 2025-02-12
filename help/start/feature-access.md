---
title: Zugreifen auf Federated Audience-Komposition
description: Erfahren Sie mehr über die erforderlichen Berechtigungen für die Federated Audience-Komposition
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
hide: true
hidefromtoc: true
source-git-commit: e9cc50cbcbd076f784c924bd941e4396c14190ce
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 36%

---

# Zugreifen auf Federated Audience-Komposition {#feature-access}

## Zugriff auf Sandboxes verwalten {#access-sandboxes}

Wenn Sie das Add-on „Komposition föderierter Zielgruppen“ erwerben, wird zu diesem Zeitpunkt für jede aktive Sandbox ein Produktprofil erstellt. Dieses Produktprofil wird in der Admin Console unter der Produktkarte **Adobe Experience Platform** erstellt und folgt dieser Namenskonvention: `ACP_FAC - <<SandboxName>> - admin.` Für den Zugriff auf die Komposition föderierter Zielgruppen für eine bestimmte Sandbox müssen Benutzende zum Produktprofil hinzugefügt werden, das für diese Sandbox erstellt wurde.

Wirds beispielsweise eine neue Sandbox mit dem Namen „fac-test“ aktiviert, wird das entsprechende Produktprofil „ACP_FAC – fac-test – admin“ erstellt. Um mit dieser Sandbox auf die Komposition föderierter Zielgruppen zugreifen zu können, müssen Benutzende diesem Produktprofil hinzugefügt werden.

## Zugriff auf Federated Audience Composition verwalten

>[!AVAILABILITY]
>
>Berechtigungen sind als Teil der März-Version verfügbar.

Für den Zugriff **Federated Audience** Komposition) müssen Sie zunächst sicherstellen, dass die Berechtigung **Federated Data verwalten** den entsprechenden Rollen zugewiesen ist. Diese Rollen müssen dann Benutzern zugewiesen werden, die Zugriff auf &quot;**Zielgruppenkomposition“**.

Beachten Sie, dass nur Administratoren Berechtigungen zuweisen können.

1. Navigieren Sie zum Menü **[!UICONTROL Berechtigungen]** .

1. Wählen Sie im Menü **[!UICONTROL Rollen]** die **[!UICONTROL Rolle]** aus, die Sie aktualisieren möchten.

   ![](assets/access_fda_1.png)

1. Klicken Sie **[!UICONTROL Bearbeiten]**, um die Berechtigungen Ihrer Rolle zu ändern.

   ![](assets/access_fda_2.png)

1. Fügen Sie die Ressource **Federated Data** hinzu und wählen Sie dann **[!UICONTROL Federated Data verwalten]** aus dem Dropdown-Menü aus.

   ![](assets/access_fda_3.png)

1. Nachdem Sie die erforderlichen Änderungen vorgenommen haben, klicken Sie auf **[!UICONTROL Speichern]**.

Alle Benutzenden, die dieser Rolle bereits zugewiesen sind, erhalten automatisch aktualisierte Berechtigungen und Zugriff auf die Federated Audience Composition.

So weisen Sie diese Rolle neuen Benutzern zu:

1. Navigieren Sie zur Registerkarte **[!UICONTROL Benutzer]** in Ihrem Rollen-Dashboard und klicken Sie auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](assets/access_fda_4.png)

1. Geben Sie den Namen oder die E-Mail-Adresse des Benutzers ein oder wählen Sie aus der verfügbaren Liste aus. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Der Benutzer erhält dann eine E-Mail mit Anweisungen für den Zugriff auf Ihre Instanz. Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).
