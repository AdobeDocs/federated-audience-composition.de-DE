---
audience: end-user
title: Senden von Zielgruppen an die Adobe Federated Audience Komposition
description: Erfahren Sie, wie Sie Adobe Experience Platform-Zielgruppen an Federated Audience Komposition senden.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 1e400d98040cdbcc6f13f84faa00e8efa6cfbd4a
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 8%

---

# Senden von Adobe Experience Platform an die Adobe Federated Audience Komposition {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Erstellen eines Ziels"
>abstract="Geben Sie die Einstellungen für die Verbindung mit der neuen föderierten Datenbank ein. Klicken Sie auf die Schaltfläche **[!UICONTROL Mit Ziel verbinden]**, um Ihre Konfiguration zu validieren."

Mit Adobe Experience Platform können Sie Zielgruppen vom Zielgruppenportal an die Adobe Federated Audience Komposition senden. Auf diese Weise können Sie bereits vorhandene Zielgruppen in Kompositionen nutzen und sie mit Daten aus Ihren externen Datenbanken kombinieren, um neue Zielgruppen zu erstellen oder bestehende zu aktualisieren.

Dazu müssen Sie eine neue Verbindung in Adobe Experience Platform mit dem Ziel der Adobe Federated Audience Komposition einrichten. Sie können eine Planung verwenden, um eine bestimmte Zielgruppe regelmäßig zu senden, und auswählen, welche Felder mit der Zielgruppe gesendet werden sollen, z. B. Kennungen zur Abstimmung der Daten. Wenn Sie Governance- und Datenschutzrichtlinien auf Ihre Zielgruppe angewendet haben, werden diese beibehalten und nach Aktualisierung der Zielgruppe an das Zielgruppenportal zurückgesendet.

Die wichtigsten Schritte zum Senden von Adobe Experience Platform-Zielgruppen an die Adobe Federated Audience Komposition sind:

1. Rufen Sie den Adobe Experience Platform-Zielkatalog auf und wählen Sie das Ziel Zusammengestellte Zielgruppen-Komposition aus.

   Wählen Sie im rechten Bereich **[!UICONTROL Neues Ziel konfigurieren]** aus.

   ![](assets/destination-new.png)

1. Geben Sie einen Namen für die neue Verbindung ein, wählen Sie den zu verwendenden **[!UICONTROL Verbindungstyp]** und die zu verwendende **[!UICONTROL Federated database]** aus und klicken Sie auf **[!UICONTROL Next]**.

   ![](assets/destination-configure.png)

   Im Abschnitt **[!UICONTROL Warnhinweise]** können Sie Warnhinweise aktivieren, mit denen Sie Benachrichtigungen zum Status des Datenflusses an Ihr Ziel erhalten. Weitere Informationen zu Warnhinweisen finden Sie im Handbuch zum [Abonnieren von Zielwarnhinweisen über die Benutzeroberfläche](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts).

1. Im Schritt **[!UICONTROL Governance-Richtlinien und Durchsetzungsaktionen]** können Sie Ihre Data Governance-Richtlinien definieren und sicherstellen, dass die verwendeten Daten beim Senden und Aktivieren von Zielgruppen konform sind.

   Wenn Sie mit der Auswahl der gewünschten Marketing-Aktionen für das Ziel fertig sind, klicken Sie auf **[!UICONTROL Erstellen]**.

1. Die neue Verbindung zum Ziel wird erstellt. Sie können nun Zielgruppen aktivieren, um sie an das Ziel zu senden. Wählen Sie sie dazu aus der Liste aus und klicken Sie auf **[!UICONTROL Weiter]**

   ![](assets/destination-activate.png)

1. Wählen Sie die gewünschten Zielgruppen aus, die Sie senden möchten, und klicken Sie auf **[!UICONTROL Weiter]**.

1. Konfigurieren Sie den Dateinamen und einen Exportzeitplan für die ausgewählten Zielgruppen.

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Detaillierte Informationen zum Konfigurieren des Zeitplans und der Dateinamen finden Sie in der Dokumentation zu Adobe Experience Platform:
   >* [Zielgruppenexport planen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling)
   >* [Dateinamen konfigurieren](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names)

1. Wählen Sie im Schritt **[!UICONTROL Zuordnung]** aus, welche Attribute und Identitätsfelder für Ihre Zielgruppe/n exportiert werden sollen. Weitere Informationen finden Sie im Schritt [Zuordnen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping) in der Adobe Experience Platform-Dokumentation.

   ![](assets/destination-attributes.png)

1. Überprüfen Sie die Zielkonfiguration und die Zielgruppeneinstellungen und klicken Sie dann auf **[!UICONTROL Beenden]**.

   ![](assets/destination-review.png)

Die ausgewählten Zielgruppen werden nun für die neue Verbindung aktiviert. Sie können mit dieser Verbindung weitere Zielgruppen hinzufügen, indem Sie zur Seite **[!UICONTROL Zielgruppen aktivieren]** zurückkehren. Zielgruppen können nicht entfernt werden, nachdem sie aktiviert wurden.
