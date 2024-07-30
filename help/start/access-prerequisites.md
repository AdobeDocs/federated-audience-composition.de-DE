---
title: Voraussetzungen und Limits für die Komposition von Federated-Zielgruppen
description: Erfahren Sie mehr über Voraussetzungen, Berechtigungen und Limits für die Zusammenstellung von Federated Audience
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: e6858ecd06e97b952e59738f299afc90fddeafb7
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 3%

---

# Voraussetzungen und Leitlinien {#fac-access}

Zusammengestellte Zielgruppenkomposition erfordert Adobe Real-time Customer Data Platform- und/oder Adobe Journey Optimizer- **Prime** - oder **Ultimate** -Packages. Um auf diese Funktion zugreifen zu können, müssen Sie das Add-on Federated Audience Komposition erworben haben.

>[!AVAILABILITY]
>
>Nachdem Sie die Begrüßungs-E-Mail-Benachrichtigung von Adobe erhalten haben, kann es noch einige Stunden dauern, bis die Benutzeroberfläche aktualisiert und Funktionen verfügbar sind.

## Berechtigungen {#permissions}

Wenn Sie das Add-on &quot;Zusammengestellte Zielgruppe&quot;erwerben, wird zu diesem Zeitpunkt für jede aktive Sandbox ein Produktprofil erstellt. Dieses Produktprofil wird in der Admin Console unter der Produktkarte &quot;**Adobe Experience Platform**&quot;erstellt und folgt dieser Namenskonvention: `ACP_FAC - <<SandboxName>> - admin.` Für den Zugriff auf die Zusammenstellung von Federated Audiences für eine bestimmte Sandbox müssen Benutzer zum Produktprofil hinzugefügt werden, das für diese Sandbox erstellt wurde.

Wenn beispielsweise eine neue Sandbox mit dem Namen &quot;fac-test&quot;aktiviert wird, wird das entsprechende Produktprofil &quot;ACP_FAC - fac-test - admin&quot;erstellt. Um mit dieser Sandbox auf Federated Audience-Komposition zugreifen zu können, müssen Benutzer diesem Produktprofil hinzugefügt werden.

## IP-Zulassungsauflistung {#ip}

Wenden Sie sich an Ihren Adobe-Kundenbetreuer, um die IP-Adressen der Federated Audience Komposition-Server zu erhalten, die darauf zugreifen werden, um sicher auf Ihre Datenbanken zugreifen zu können.

Fügen Sie diese IP-Adressen zu Ihrer Zulassungsliste hinzu, um Zugriff für die Zusammenstellung von Federated Audience zu gewähren.

## Schutzmechanismen und Einschränkungen {#fac-guardrails}

* Federated Audience Komposition ist mit dem Privacy &amp; Security Shield kompatibel und kann in allen Vertikalen außer in der Gesundheitsbranche verwendet werden. Derzeit kann die Zusammenstellung von Federated Audience nicht für Kunden lizenziert werden, die Gesundheitsdaten erfassen möchten. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* Berechtigungen, Produktbeschränkungen und Leistungsgarantien, die in der [Adobe Real-time Customer Data Platform-Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} aufgeführt sind, gelten für dieses Add-on.