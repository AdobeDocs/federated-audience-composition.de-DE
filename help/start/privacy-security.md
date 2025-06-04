---
title: Datenschutz und Sicherheit in der Federated Audience-Komposition
description: Erfahren Sie, wie die Federated Audience-Komposition mit Datenschutz und Sicherheit für Benutzerdaten umgeht, einschließlich Funktionen wie Data Governance, Durchsetzung von Einverständnissen, Zugriffskontrolle, Datenverschlüsselung und Datenschutzkonformität.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# Datenschutz und Sicherheit in der Federated Audience-Komposition

Die Federated Audience-Komposition erfüllt zahlreiche Sicherheitsverfahren, um Ihre Daten während der Verarbeitung zu schützen.

## Privacy Service {#privacy}

Die Federated Audience-Komposition stellt die Federated Data für Adobe Experience Platform und Adobe Journey Optimizer bereit. Die Federated Audience-Komposition speichert jedoch **keine** der Kundendaten aus einem der Data Warehouses. Daher können Sie Adobe Experience Platform Privacy Service verwenden, um Anfragen von betroffenen Personen und zur Löschung von Daten zu erfüllen.

Wenn Sie beispielsweise eine Zielgruppe mit dem Aktivitätsblock Speichern auf der Arbeitsfläche für die Komposition erstellen, wird die resultierende Zielgruppe im Data Lake in Experience Platform als externe Zielgruppe gespeichert. Diese externe Zielgruppe ist mit ihrem Identitätsfeld und Identity-Namespace gekennzeichnet. Daher können Sie Privacy Service verwenden, um mit einer externen Zielgruppe auf diese Profile zuzugreifen und sie zu entfernen.

Alternativ wird nach dem Erstellen einer Profilanreicherung mithilfe der Aktivität Profil speichern auf der Arbeitsfläche für die Komposition die resultierende Anreicherung in Experience Platform als profilaktiviertes Schema und profilaktivierter Datensatz gespeichert. Diese Anreicherungsdaten werden mit einem Identitätsfeld und einem Identity-Namespace gekennzeichnet. Daher können Sie mit Privacy Service auf diese Profile zugreifen und sie bereinigen.

Weitere Informationen zu Privacy Service finden Sie in der [Übersicht über Privacy Service](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home){target="_blank"}.

### Datenschutzanfragen {#privacy-requests}

In Privacy Service können Sie einzelne Datenschutzanfragen erstellen und verwalten, um auf Kundendaten aus der Federated Audience Composition zuzugreifen und sie zu löschen. Privacy Service bietet sowohl eine [Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de){target="_blank"} als auch eine [RESTful-](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/api/overview){target="_blank"}, mit der Sie Anfragen zu Kundendaten verwalten können.

Weitere Informationen zum Erstellen und Verwalten von Datenschutzanfragen finden Sie unter [Datenschutzaufträge im Handbuch zur Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Durchsetzung von Einverständnisrichtlinien {#consent}

Die Federated Audience-Komposition über Experience Platform bietet Tools, mit denen Sie die Durchsetzung Ihrer Einwilligungen automatisieren können, um sicherzustellen, dass Sie Zielgruppen basierend auf der Einwilligung Ihrer Kunden aktivieren.

Wenn Sie beispielsweise eine Zielgruppe mit dem Aktivitätsblock Speichern auf der Arbeitsfläche für die Komposition erstellen, wird die resultierende Zielgruppe im Data Lake in Experience Platform als externe Zielgruppe gespeichert. Experience Platform unterstützt bei der Aktivierung automatisch die Validierung des Einverständnisses . Weitere Informationen finden Sie unter [Häufig gestellte Fragen zum Segmentierungs-](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Alternativ wird die resultierende Anreicherung, nachdem Sie eine Profilanreicherung mithilfe der Aktivität Profil speichern auf der Arbeitsfläche für die Komposition erstellt haben, in Experience Platform als profilaktiviertes Schema und profilaktivierter Datensatz gespeichert. Bei vorhandenen Profilen werden verfügbare Einverständnisattribute bei der Aktivierung automatisch berücksichtigt. Bei neuen Profilen werden die während der Profilaufnahme bereitgestellten Einverständnisattribute bei der Aktivierung automatisch berücksichtigt. Weiterführende Informationen zur Anwendung von Einverständnissen auf Profile finden Sie im [Handbuch zu Einverständnis- und Voreinstellungsfeldern](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Weiterführende Informationen zur Anwendung von Einverständniserklärungen finden Sie im [Handbuch zur Benutzeroberfläche für die Verwaltung von Richtlinien](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Datenlebenszyklus {#data-lifecycle}

Da die Federated Audience **keine** Kundendaten aus einem der Data Warehouses speichert, können Sie Experience Platform zur Handhabung des Datenlebenszyklus verwenden. Mit Advanced Data Lifecycle Management können Sie Ihren Datenlebenszyklus sowohl auf Datensatz- als auch auf Datensatzebene verwalten.

Wenn Sie beispielsweise eine Zielgruppe mithilfe des Aktivitätsblocks Speichern auf der Arbeitsfläche für die Komposition erstellen, wird die resultierende Zielgruppe im Data Lake in Experience Platform als externe Zielgruppe gespeichert. Da diese Daten **nicht** in der Federated-Audience-Komposition gespeichert werden, werden die Audience-Daten und die entsprechenden Datensätze automatisch gelöscht, wenn die Audience im Audience Portal gelöscht wird.

Alternativ wird die resultierende Anreicherung, nachdem Sie eine Profilanreicherung mithilfe der Aktivität Profil speichern auf der Arbeitsfläche für die Komposition erstellt haben, in Experience Platform als profilaktiviertes Schema und profilaktivierter Datensatz gespeichert. Dadurch können Sie über den Datenlebenszyklus auf die Profile zugreifen und sie bereinigen.

Weitere Informationen zur Verwendung des Datenlebenszyklus finden Sie unter [Übersicht über den Datenlebenszyklus](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Datennutzungskennzeichnungen {#data-usage-labels}

Mit Datennutzungskennzeichnungen können Sie Datensätze und Felder basierend auf den für diese Daten geltenden Governance-Richtlinien kategorisieren. Nachdem Sie eine Zielgruppe mithilfe von Kompositionen erstellt haben, können Sie die entsprechenden Datenbeschriftungen auf das resultierende Schema anwenden, um sicherzustellen, dass es die erforderlichen Nutzungsbeschränkungen einhält.

Weitere Informationen zur Verwendung von Datennutzungskennzeichnungen finden Sie unter [Datennutzungskennzeichnungen - Übersicht](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Verschlüsselung {#encryption}

Die flexible Zielgruppenzusammensetzung bietet Verschlüsselung durch Verschlüsselung statischer Daten, Verschlüsselung von Daten während der Übertragung und kundenverwaltete Schlüssel.

Ruhedaten beziehen sich auf die Kundendaten, die in der Federated Audience-Komposition verwendet werden. Die Daten werden vom Cloud-Service-Anbieter verschlüsselt und in der Federated Audience Composition in ihrer verschlüsselten Form verwendet.

Daten in Übertragung beziehen sich auf die Kundendaten, wenn sie in der Federated Audience Composition von einer Komponente zur anderen verschoben werden. Die Daten werden in allen Komponenten der Federated Audience Composition mit TLS 1.3 über HTTPS verschlüsselt aufbewahrt.

Weitere Informationen zum Umgang von Adobe mit der Datenverschlüsselung finden Sie im Handbuch [Datenverschlüsselung in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Kundenseitig verwaltete Schlüssel {#customer-managed-keys}

Mit kundenverwalteten Schlüsseln haben Sie die Kontrolle über Ihre Daten, indem Sie Ihre eigenen Verschlüsselungsschlüssel zum Verschlüsseln Ihrer Daten verwenden können. Da die Federated Audience **keine** Kundendaten speichert, können kundenverwaltete Schlüssel direkt für die resultierenden Zielgruppen und Anreicherungen verwendet werden, da sie im Data Lake in Experience Platform gespeichert werden.

Weitere Informationen zu kundenverwalteten Schlüsseln finden Sie im Handbuch [Kundenverwaltete Schlüssel](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Auditprotokoll {#audit-log}

Alle Erstellungs-, Lese-, Aktualisierungs- und Löschvorgänge, die in Federated Audience Composition ausgeführt werden, werden im Audit-Protokoll protokolliert. Sie können dieses Auditprotokoll verwenden, um diese Aktionen zu verfolgen, die Verantwortlichkeit durchzusetzen und Compliance-Audits zu unterstützen.

Weitere Informationen finden Sie im Abschnitt [Übersicht über das Audit-Protokoll](/help/admin/audit-trail.md){target="_blank"}.

## Zugangssteuerung {#access-control}

Sie können den Zugriff auf die Federated Audience-Komposition sowohl auf Feld- als auch auf Rollenebene steuern. Sie können diese Zugriffssteuerungen verwenden, um Data-Governance-Richtlinien durchzusetzen, die Offenlegung sensibler Informationen zu begrenzen und den Zugriff auf die Zuständigkeiten der Benutzer abzustimmen.

Weiterführende Informationen zur Zugriffssteuerung in Federated Audience Composition finden Sie im [Handbuch zur Federated Audience Composition](/help/start/feature-access.md){target="_blank"}.

## Datenlokalisierung {#data-localization}

Die Federated Audience-Komposition **keine** Kundendaten. Daher müssen Sie sicherstellen, dass Sie **nur** Ihre externen Datenbanken mit der entsprechenden Sandbox-Region verbinden, um Ihre Daten in derselben Region zu halten. Wenn Sie die Datenbank einer anderen Region mit einer Sandbox verbinden, ist Adobe **nicht** für die Datenlokalisierung verantwortlich.

## Nächste Schritte {#next-steps}

Nach dem Lesen dieses Handbuchs haben Sie ein besseres Verständnis der Datenschutz- und Sicherheitsfunktionen, die für die Federated Audience-Komposition verwendet werden, einschließlich Data Governance, Datenschutzkonformität, Durchsetzung von Einverständnissen, Data Lifecycle Management und Zugriffskontrolle.
