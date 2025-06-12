---
title: Datenschutz und Sicherheit bei der Komposition föderierter Zielgruppen
description: Erfahren Sie, wie die Komposition föderierter Zielgruppen mit Datenschutz und Sicherheit für Benutzerdaten umgeht, einschließlich Funktionen wie Data Governance, Durchsetzung des Einverständnisses, Zugriffskontrolle, Datenverschlüsselung und Einhaltung von Datenschutzbestimmungen.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 8076a7851d0cd5cd84a7c48c6f1783b452864903
workflow-type: ht
source-wordcount: '1085'
ht-degree: 100%

---

# Datenschutz und Sicherheit bei der Komposition föderierter Zielgruppen

Die Komposition föderierter Zielgruppen erfüllt zahlreiche Sicherheitsfunktionen, um Ihre Daten während der Verarbeitung zu schützen.

## Privacy Service {#privacy}

Die Komposition föderierter Zielgruppen stellt die föderierten Daten für die Verwendung durch Adobe Experience Platform und Adobe Journey Optimizer bereit. Die Komposition föderierter Zielgruppen speichert jedoch **keine** der Kundendaten aus einem der Data Warehouses. Daher können Sie Adobe Experience Platform Privacy Service verwenden, um Anfragen von betroffenen Personen und zur Löschung von Daten zu erfüllen.

Wenn Sie beispielsweise eine Zielgruppe mit dem Aktivitätsblock „Speichern“ auf der Arbeitsfläche für die Komposition erstellen, wird die resultierende Zielgruppe im Data Lake in Experience Platform als externe Zielgruppe gespeichert. Diese externe Zielgruppe ist mit ihrem Identitätsfeld und Identity-Namespace gekennzeichnet. Daher können Sie Privacy Service verwenden, um mit einer externen Zielgruppe auf diese Profile zuzugreifen und sie zu entfernen.

Alternativ wird nach dem Erstellen einer Profilanreicherung mithilfe der Aktivität „Profil speichern“ auf der Arbeitsfläche für die Komposition die resultierende Anreicherung in Experience Platform als profilaktiviertes Schema und profilaktivierter Datensatz gespeichert. Diese Anreicherungsdaten werden mit einem Identitätsfeld und einem Identity-Namespace gekennzeichnet. Daher können Sie mit Privacy Service auf diese Profile zugreifen und sie bereinigen.

Weiterführende Informationen zu Privacy Service finden Sie in der [Übersicht zu Privacy Service](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/home){target="_blank"}.

### Datenschutzanfragen {#privacy-requests}

In Privacy Service können Sie individuelle Datenschutzanfragen für den Zugriff auf und die Löschung von Kundendaten aus der Komposition föderierter Zielgruppen von Adobe erstellen und verwalten. Privacy Service bietet sowohl eine [Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de){target="_blank"} als auch ein [RESTful-API](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/api/overview){target="_blank"}, die Sie bei der Verwaltung von Kundendatenanfragen unterstützen.

Weiterführende Informationen zum Erstellen und Verwalten von Datenschutzanfragen finden Sie unter [„Datenschutzaufträge“ im Handbuch zur Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Durchsetzung der Einverständnisrichtlinie {#consent}

Die Komposition föderierter Zielgruppen bietet über Experience Platform Tools, mit denen Sie die Durchsetzung des Einverständnisses automatisieren können, um sicherzustellen, dass Sie Zielgruppen basierend auf dem Einverständnis Ihrer Kundinnen und Kunden aktivieren.

Wenn Sie beispielsweise eine Zielgruppe mit dem Aktivitätsblock „Speichern“ auf der Arbeitsfläche für die Komposition erstellen, wird die resultierende Zielgruppe im Data Lake in Experience Platform als externe Zielgruppe gespeichert. Experience Platform unterstützt bei der Aktivierung automatisch die Validierung des Einverständnisses. Weiterführende Informationen finden Sie unter [Häufig gestellte Fragen zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Alternativ wird die resultierende Anreicherung, nachdem Sie eine Profilanreicherung erstellt haben, mithilfe der Aktivität „Profil speichern“ auf der Arbeitsfläche für die Komposition in Experience Platform als profilaktiviertes Schema und profilaktivierter Datensatz gespeichert. Bei vorhandenen Profilen werden verfügbare Einverständnisattribute bei der Aktivierung automatisch berücksichtigt. Bei neuen Profilen werden die während der Profilaufnahme bereitgestellten Einverständnisattribute bei der Aktivierung automatisch berücksichtigt. Weiterführende Informationen zur Anwendung von Einverständnissen auf Profile finden Sie im [Handbuch zu den Einverständnis- und Voreinstellungsfeldergruppen](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Weiterführende Informationen zur Anwendung von Einverständnissen finden Sie im [UI-Handbuch zur Verwaltung von Einverständnissen](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Datenlebenszyklus {#data-lifecycle}

Da die Komposition föderierter Zielgruppen **keine** Kundendaten aus einem der Data Warehouses speichert, können Sie Experience Platform zur Handhabung des Datenlebenszyklus verwenden. Mit Advanced Data Lifecycle Management können Sie Ihren Datenlebenszyklus sowohl auf Datensatz- als auch auf Eintragsebene verwalten.

Wenn Sie beispielsweise eine Zielgruppe mit dem Aktivitätsblock „Speichern“ auf der Arbeitsfläche für die Komposition erstellen, wird die resultierende Zielgruppe im Data Lake in Experience Platform als externe Zielgruppe gespeichert. Da diese Daten **nicht** in der Komposition föderierter Zielgruppen gespeichert werden, werden die Zielgruppendaten und die entsprechenden Datensätze automatisch gelöscht, wenn die Zielgruppe im Zielgruppenportal gelöscht wird.

Alternativ wird die resultierende Anreicherung, nachdem Sie eine Profilanreicherung erstellt haben, mithilfe der Aktivität „Profil speichern“ auf der Arbeitsfläche für die Komposition in Experience Platform als profilaktiviertes Schema und profilaktivierter Datensatz gespeichert. Dadurch können Sie über den Datenlebenszyklus auf die Profile zugreifen und sie bereinigen.

Weiterführende Informationen zur Verwendung des Datenlebenszyklus finden Sie im [Überblick über den Datenlebenszyklus](https://experienceleague.adobe.com/de/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Datennutzungs-Labels {#data-usage-labels}

Mit Datennutzungs-Labels können Sie Datensätze und Felder basierend auf der für diese Daten geltenden Governance-Richtlinien kategorisieren. Nachdem Sie mithilfe von Kompositionen eine Zielgruppe erstellt haben, können Sie die entsprechenden Daten-Labels auf das resultierende Schema anwenden, um sicherzustellen, dass es die erforderlichen Nutzungseinschränkungen einhält.

Weitere Informationen zur Verwendung von Daten-Labels finden Sie im [Überblick über Datennutzungs-Labels](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Verschlüsselung {#encryption}

Die flexible Zielgruppenkomposition bietet Verschlüsselungen durch die Verschlüsselung von Daten im Ruhezustand, die Verschlüsselung von Daten während der Übertragung und kundenseitig verwaltete Schlüssel.

„Daten im Ruhezustand“ bezieht sich auf die Kundendaten, die in der Komposition föderierter Zielgruppen verwendet werden. Die Daten werden vom Cloud-Dienst-Anbieter verschlüsselt und in der Komposition föderierter Zielgruppen in ihrer verschlüsselten Form verwendet.

„Daten während der Übertragung“ bezieht sich auf die Kundendaten, die in der Komposition föderierter Zielgruppen von einer Komponente zu einer anderen Komponente verschoben werden. Die Daten werden in allen Komponenten der Komposition föderierter Zielgruppen mit TLS 1.3 über HTTPS verschlüsselt aufbewahrt.

Weiterführende Informationen dazu, wie Adobe die Datenverschlüsselung handhabt, finden Sie im Handbuch zur [Datenverschlüsselung in Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Kundenseitig verwaltete Schlüssel {#customer-managed-keys}

Mit kundenseitig verwalteten Schlüsseln haben Sie die Kontrolle über Ihre Daten, indem Sie Ihre eigenen Verschlüsselungsschlüssel zum Verschlüsseln Ihrer Daten verwenden können. Da die Komposition föderierter Zielgruppen **keine** der Kundendaten speichert, können Sie kundenseitig verwaltete Schlüssel direkt für die resultierenden Zielgruppen und Anreicherungen verwenden, da diese im Data Lake in Experience Platform gespeichert werden.

Weiterführende Informationen zu kundenseitig verwalteten Schlüsseln finden Sie im [Handbuch zu kundenseitig verwalteten Schlüsseln](https://experienceleague.adobe.com/de/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Auditprotokoll {#audit-log}

Alle Erstellungs-, Lese-, Aktualisierungs- und Löschvorgänge, die in der Komposition föderierter Zielgruppen ausgeführt werden, werden im Audit-Protokoll protokolliert. Sie können dieses Audit-Protokoll verwenden, um diese Aktionen zu verfolgen, die Verantwortlichkeit durchzusetzen und Compliance-Audits zu unterstützen.

Weiterführende Informationen finden Sie im [Überblick über das Audit-Protokoll](/help/admin/audit-trail.md){target="_blank"}.

## Zugangssteuerung {#access-control}

Sie können den Zugriff auf die Komposition föderierter Zielgruppen sowohl auf einer feld- als auch auf einer rollenbasierten Ebene steuern. Sie können diese Zugriffskontrollen verwenden, um Data-Governance-Richtlinien durchzusetzen, die Offenlegung vertraulicher Daten zu begrenzen und den Zugriff auf die Zuständigkeiten der Benutzenden abzustimmen.

Weiterführende Informationen zur Zugriffskontrolle in der Komposition föderierter Zielgruppen finden Sie im [Handbuch für den Zugriff auf die Komposition föderierter Zielgruppen](/help/start/feature-access.md){target="_blank"}.

## Datenlokalisierung {#data-localization}

Die Komposition föderierter Zielgruppen speichert **keine** Kundendaten. Daher müssen Sie sicherstellen, dass Sie **nur** Ihre externen Datenbanken mit der entsprechenden Sandbox-Region verbinden, damit Ihre Daten in derselben Region bleiben. Wenn Sie die Datenbank einer anderen Region mit einer Sandbox verbinden, ist Adobe **nicht** für die Datenlokalisierung verantwortlich.

## Nächste Schritte {#next-steps}

Nach dem Lesen dieses Handbuchs haben Sie ein besseres Verständnis über die Datenschutz- und Sicherheitsfunktionen, die für die Komposition föderierter Zielgruppen verwendet werden, einschließlich Data Governance, Datenschutzkonformität, der Durchsetzung von Einverständnissen, Verwaltung des Datenlebenszyklus und der Zugriffskontrolle.
