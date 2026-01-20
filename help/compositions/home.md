---
audience: end-user
title: Erste Schritte mit Kompositionen
description: Erfahren Sie, wie Sie mit Kompositionen beginnen
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e82f1c237927af983a32c848cb9d45d84f9cf3fe
workflow-type: ht
source-wordcount: '646'
ht-degree: 100%

---

# Überblick über Kompositionen

>[!AVAILABILITY]
>
>Um auf Kompositionen zugreifen zu können, benötigen Sie eine der folgenden Berechtigungen:
>
>-**Föderierte Kompositionen verwalten**
>-**Föderierte Kompositionen anzeigen**
>
>Weitere Informationen zu den erforderlichen Berechtigungen finden Sie im [Handbuch zur Zugriffssteuerung](/help/governance-privacy-security/access-control.md).

Mit der Komposition föderierter Zielgruppen können Sie Kompositionen erstellen. Dabei können Sie verschiedene Aktivitäten in einer visuellen Arbeitsfläche nutzen, um Zielgruppen zu erstellen. Die so erstellten Zielgruppen werden in Adobe Experience Platform gespeichert und können in Experience Platform-Zielen und Adobe Journey Optimizer zum Ansprechen von Kundschaft genutzt werden. 

![In der Komposition föderierter Zielgruppen wird ein beispielhafter Kompositions-Workflow angezeigt.](assets/compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Komponenten von Kompositionen {#components}

Eine Komposition innerhalb der Komposition föderierter Zielgruppen besteht aus den folgenden Teilen:

- **[!UICONTROL Aktivitäten]**: Eine Aktivität ist eine Aufgabe, die ausgeführt werden soll. Aktivitäten werden in der Komposition durch Symbole dargestellt.
- **[!UICONTROL Transitionen]**: Transitionen verknüpfen eine Quellaktivität mit einer Zielaktivität und definieren deren Sequenz. Die in den Transitionen enthaltenen Informationen werden in einer Arbeitstabelle gespeichert. Jede Komposition verwendet mehrere Arbeitstabellen. Die in diesen Tabellen enthaltenen Daten können während des gesamten Lebenszyklus der Komposition verwendet werden.

## Zugreifen auf und Verwalten von Kompositionen {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Kompositionen"
>abstract="Auf diesem Bildschirm können Sie auf die vollständige Liste der Kompositionen zugreifen, ihren aktuellen Status sowie das Datum der letzten/nächsten Ausführung überprüfen und eine neue Komposition erstellen."

Der Zugriff auf Kompositionen erfolgt über das Menü **[!UICONTROL Zielgruppen]** in Adobe Experience Platform auf der Registerkarte **[!UICONTROL Föderierte Kompositionen]** im Abschnitt **[!UICONTROL Kundinnen und Kunden]**.

Auf diesem Bildschirm können Sie neue Kompositionen erstellen und auf bestehende Kompositionen zugreifen. Sie können eine bestehende Komposition auch duplizieren oder löschen, indem Sie auf die Schaltfläche mit den ![Auslassungspunkten](/help/assets/icons/more.png) neben ihrem Namen klicken.

Sie können auch Informationen zu den Kompositionen anzeigen, einschließlich Name, Status, Erstellerin bzw. Ersteller und Datum der letzten Änderung.

| Status | Beschreibung |
| ------ | ----------- |
| **[!UICONTROL Entwurf]** | Die Komposition wurde erstellt und gespeichert. |
| **[!UICONTROL In Bearbeitung]** | Die Ausführung der Komposition wurde gestartet und läuft derzeit. |
| **[!UICONTROL Gestoppt]** | Die Ausführung der Komposition ist abgeschlossen und wurde gestoppt. |
| **[!UICONTROL Ausgesetzt]** | Die Ausführung der Komposition wurde angehalten. |
| **[!UICONTROL Fehlerhaft]** | Bei der Ausführung der Komposition ist ein Fehler aufgetreten. Um weitere Informationen zum Fehler anzuzeigen, öffnen Sie die Komposition und greifen Sie auf die Protokolle zu. |

Weitere Informationen zum Starten oder Stoppen einer Komposition finden Sie im [Handbuch zum Erstellen einer Komposition](./create-composition.md#monitor-logs).

![Eine Liste der verfügbaren Kompositionen wird angezeigt.](assets/compositions/compositions-list.png){zoomable="yes"}{width="70%"}

Um die Liste einzugrenzen und die gesuchte Komposition zu finden, können Sie die Liste durchsuchen und Kompositionen nach ihrem Status oder dem letzten Verarbeitungsdatum filtern.

Sie können die Liste auch anpassen, indem Sie Spalten hinzufügen oder entfernen. Wählen Sie dazu die Schaltfläche **[!UICONTROL Spalten konfigurieren]** aus und fügen Sie die gewünschten Ausgabespalten hinzu oder entfernen Sie sie.

![Eine Liste der verfügbaren Spalten wird angezeigt, die Sie der Seite zum Durchsuchen von Kompositionen hinzufügen können.](assets/compositions/compositions-columns.png){zoomable="yes"}{width="70%"}

### Anwenden von Zugriffs-Labels {#access-labels}

Um Zugriffs-Labels auf eine bestimmte Komposition anzuwenden, wählen Sie die Komposition und dann **[!UICONTROL Zugriff verwalten]** aus.

![Die Schaltfläche „Zugriff verwalten“ wird auf der Arbeitsfläche der Komposition hervorgehoben.](assets/compositions/select-manage-access.png){zoomable="yes"}{width="70%"}

Das Popup-Fenster **[!UICONTROL Zugriff verwalten]** wird angezeigt. Auf dieser Seite können Sie die entsprechenden Zugriffs- und Data-Governance-Labels auf Ihre Komposition anwenden.

![Das Popup-Fenster „Zugriff verwalten“ wird angezeigt. Hier wird eine Liste aller verfügbaren Labels angezeigt, die Sie auf die Komposition anwenden können.](assets/compositions/manage-access.png){zoomable="yes"}{width="70%"}

| Label-Typ | Beschreibung |
| ---------- | ----------- |
| Vertrags-Labels | Vertrags-Labels (Contract Labels, C-Labels) dienen der Kategorisierung von Daten, die vertragliche Bestimmungen aufweisen oder mit Data-Governance-Richtlinien Ihrer Organisation in Zusammenhang stehen. |
| Identitäts-Labels | Identitäts-Labels (I-Labels) dienen der Kategorisierung von Daten, mit denen eine bestimmte Person identifiziert oder kontaktiert werden kann. |
| Labels für sensible Daten | Labels für sensible Daten (Sensitive Labels, S-Labels) dienen dazu, Sie und/oder Ihr Unternehmen als sensibel zu kategorisieren. |
| Partner-Ökosystem-Labels | Partner-Ökosystem-Labels dienen der Kategorisierung von Daten aus externen Quellen für Ihr Unternehmen. |

Weitere Informationen zu Zugriff und Data-Governance-Labels finden Sie im [Glossar zu Datennutzungs-Labels](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/labels/reference).

## Erstellen {#create}

Sie können eine Komposition für Adobe Experience Platform mithilfe einer Zielgruppenkomposition erstellen. Weitere Informationen finden Sie im [Handbuch zum Erstellen einer Komposition](./create-composition.md).

## Nächste Schritte

In diesem Handbuch wurde erläutert, wie Sie auf Zugriffs-Labels für Kompositionen zugreifen, diese verwalten und erstellen. Weitere Informationen zum Arbeiten mit Zielgruppen als Ganzes finden Sie im [Handbuch zu Zielgruppen](../start/audiences.md).
