---
title: KI-Assistent - Übersicht
description: Erfahren Sie, wie Sie den KI-Assistenten verwenden, einschließlich Produktkenntnissen, betrieblicher Einblicke und der Erstellung von zusammengeführten Zielgruppenkompositionen.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: 226679a38d0ad17726fd743f5df3b74879a2dd32
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# Überblick über den KI-Assistenten {#ai-assistant}

Der KI-Assistent ist eine Funktion der Benutzeroberfläche, mit der Sie durch Adobe-Konzepte navigieren und diese verstehen können. Sie können den KI-Assistenten verwenden, um Anwendungsfälle mit Produktkenntnissen in verschiedenen Produkten in Adobe Experience Cloud besser zu verstehen, einschließlich der Federated Audience-Komposition.

>[!CAUTION]
>
>Bevor Sie den KI-Assistenten verwenden können, müssen Sie den Benutzerrichtlinien für generative KI in Adobe Experience Cloud zustimmen. Weitere Informationen zur Vereinbarung finden Sie in der [Übersicht zum KI-Assistenten (frühere Version](https://experienceleague.adobe.com/de/docs/experience-platform/ai-assistant/home){target="_blank"}.

Bei der Komposition föderierter Zielgruppen können Sie auf Produktwissen zugreifen, um mehr über Adobe-Konzepte im Zusammenhang mit verschiedenen Prozessaspekten zu erfahren. Der KI-Assistent unterstützt vier Arten von Anwendungsfällen: **Offene Erkennung** (Erkunden von Produktkonzepten basierend auf der Experience League-Dokumentation), **Targeted Learning und Fehlerbehebung** (Stellen Sie Fragen zu bestimmten Funktionen), **Operative Einblicke** (Stellen Sie Fragen zu Ihren Objekten innerhalb der Federated-Audience-Komposition) und **Erstellen von Federated-Audience-Kompositionen**.

## Zugriff {#access}

Um auf den KI-Assistenten zuzugreifen![&#x200B; wählen Sie in der oberen Leiste &#x200B;](/help/start/assets/ai-assistant/icon.png)das Symbol KI-Assistent“ aus. Der KI-Assistent wird rechts am Bildschirm angezeigt. Sie können ![ALT-Text für das Tauchbild](assets/do-not-localize/Smock_FullScreen_18_N.svg "Symbol „Erweitern“ "), um das Fenster des KI-Assistenten zu erweitern.

![Das Symbol für den KI-Assistenten ist hervorgehoben und zeigt an, wie auf den KI-Assistenten zugegriffen werden kann.](/help/start/assets/ai-assistant/access.png)

## Verwenden des KI-Assistenten {#using}

Nachdem Sie den KI-Assistenten geöffnet haben, geben Sie Ihre Frage in das Feld am unteren Bildschirmrand ein und drücken Sie die Eingabetaste. Die Antwort auf Ihre Frage wird jetzt angezeigt. Sie können Daumen hoch oder Daumen runter verwenden, um Ihre Antwort zu bewerten.

![Im KI-Assistenten wird eine Beispielfrage und -antwort angezeigt.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Beispielfragen {#sample-questions}

Die folgenden Abfragen zeigen die verfügbaren Fragetypen an, die Sie dem KI-Assistenten stellen können:

| Abfragetyp | Beispielfrage |
| ---------- | --------------- |
| Erkennung öffnen | <ul><li>Was ist die Komposition föderierter Zielgruppen?</li></ul> |
| Gezieltes Lernen | <ul><li>Wie kann ich ein Snowflake Federated Database-Konto konfigurieren?</li><li>Wie kann ich eine föderierte Komposition erstellen?</li></ul> |
| Betriebliche Erkenntnisse | <ul><li>Wie viele Verbunddatenbanken habe ich in meiner Sandbox?</li><li>Wie viele Schemata habe ich in den letzten 30 Tagen erstellt?</li></ul> |
| Erstellen einer Federated-Audience-Komposition | <ul><li>Erstellen Sie eine verbundene Zielgruppe von Kunden, die in Großbritannien leben.</li></ul> |

Darüber hinaus können Sie den KI-Assistenten verwenden, um autonom eine Federated-Audience-Komposition zu erstellen.

## Erstellen einer Zielgruppe {#create-audience}

Sie können den KI-Assistenten verwenden, um mithilfe von Eingabeaufforderungen in natürlicher Sprache eine Federated-Audience-Komposition zu erstellen. Wenn Sie mit dem KI-Assistenten eine Zielgruppe erstellen, erstellt der KI-Assistent einen auf Ihrer Eingabeaufforderung basierenden Plan und führt ihn in Ihrem Browser mithilfe der KI-gestützten Automatisierung aus.

Wenn Sie beispielsweise den KI-Assistenten bitten, „mithilfe des Schemas CUSTOMERS_Table eine verbundene Zielgruppe von Kunden mit Wohnsitz in Großbritannien zu erstellen“, legt der KI-Assistent den Plan für die Erstellung der Zielgruppe dar, einschließlich Schritten wie Navigieren zur Seite „Federated Compositions“, wie der Agent die Komposition erstellt und Speichern der Zielgruppe, sobald sie abgeschlossen ist.

![Es werden Beispielfragen und -antworten angezeigt.](/help/start/assets/ai-assistant/ask-create.png)

Wenn der Plan korrekt aussieht, können Sie **[!UICONTROL Ausführen]** wählen, damit der Agent seine Automatisierung durchlaufen kann. Der Agent führt im Browser selbstständig die Schritte zur Erstellung Ihrer angeforderten Komposition in der Benutzeroberfläche für die Federated Audience-Komposition durch. Wenn Sie die Automatisierung zu einem beliebigen Zeitpunkt stoppen möchten, wählen Sie **[!UICONTROL Stoppen]**.

![Der Plan wurde ausgeführt und der Agent führt den Plan autonom aus.](/help/start/assets/ai-assistant/execute-plan.png)

Derzeit unterstützt die Fähigkeit zur Zielgruppenerstellung die folgenden zusätzlichen Funktionen:

- Planung
   - Sie können Verbundkompositionen erstellen, die nach einem wiederkehrenden Zeitplan ausgeführt werden. Unterstützte Werte sind **Einmal** und **Täglich**.
- Deduplizierung
   - Sie können die zusammengeführten Datensätze während der Datenabstimmung deduplizieren

## Nächste Schritte

Weitere Informationen zum KI-Assistenten, einschließlich Beispielzielen, die Sie mit dem KI-Assistenten erreichen können, und Informationen zur Funktionsweise des KI-Assistenten finden Sie unter [KI-Assistent - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/ai-assistant/home){target="_blank"}.

Eine vollständige Liste der Fragen zur operativen Insight-Komposition, die Sie bei der Federated Audience-Komposition stellen können, finden Sie im [Abschnitt zu operativen Einblicken](https://experienceleague.adobe.com/de/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
