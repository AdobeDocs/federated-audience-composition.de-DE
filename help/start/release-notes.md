---
title: Neue Funktionen zur Komposition föderierter Zielgruppen in Experience Platform
description: Neueste Aktualisierungen und Versionshinweise
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 59d7d112421e0ff207ce76122593a111ad9c6cc7
workflow-type: ht
source-wordcount: '1542'
ht-degree: 100%

---

# Versionshinweise {#rn-new}

[!DNL Federated Audience Composition] bietet kontinuierlich neue Funktionen, Verbesserungen vorhandener Funktionen und Fehlerbehebungen. Alle Änderungen sind in diesen Versionshinweisen konsolidiert. [!DNL Federated Audience Composition] setzt nativ auf [!DNL Adobe Experience Platform] auf und profitiert von den neuesten Innovationen und Verbesserungen. Weitere Informationen zu diesen Änderungen finden Sie in den [Versionshinweisen zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=de){target="_blank"}.

## Version Juli 2025 {#fac-25-7}

### Neue Funktionen {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>Neuer Connector – Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der Oracle-Connector ist jetzt für die Verwendung mit der Komposition föderierter Zielgruppen verfügbar.</p>
<p>Sie können den Oracle-Connector für Anwendungsfälle zur Erstellung und Anreicherung von Zielgruppen verwenden.</p>
<p>Weitere Informationen zur Oracle-Verbindung finden Sie unter <a href="../connections/home.md#create">Überblick über Verbindungen</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Warnhinweise zu Kompositionen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sie können jetzt Warnhinweise abonnieren, um mehr über die erfolgreichen und fehlgeschlagenen Ausführungen Ihrer Komposition zu erfahren</p>
<p>Weitere Informationen zum Abonnieren von Benachrichtigungen zu den Ausführungen Ihrer Komposition finden Sie im <a href="../compositions/start-monitor-composition.md#alerts">Handbuch zum Starten und Überwachen Ihrer Komposition</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#fac-25-07-improvements}

Diese Version enthält die folgende Verbesserung:

* **Erhöhte Server-Zeichenlänge**

  Beim Konfigurieren Ihrer föderierten Datenbanken können Sie jetzt bis zu 255 Zeichen anstelle der vorherigen 80 Zeichen verwenden.

## Version Juni 2025 {#fac-25-6}

### Verbesserungen {#fac-25-06-improvements}

Diese Version enthält die folgenden Verbesserungen:

* **Allgemeine Verfügbarkeit für Kundinnen und Kunden von Adobe Healthcare Shield**

  Die Komposition föderierter Zielgruppen steht Kundinnen und Kunden von Adobe Healthcare Shield bis Ende Juni für Anwendungsfälle für die Zielgruppenerstellung, Anreicherung und Profilanreicherung zur Verfügung.

  Weitere Informationen zu Datenschutz und Sicherheit bei der Komposition föderierter Zielgruppen finden Sie im [Handbuch zu Data Governance, Datenschutz und Sicherheit](/help/governance-privacy-security/home.md).

* **Zugriffskontrolle auf Objektebene**

  Die Komposition föderierter Zielgruppen unterstützt jetzt die Zugriffskontrolle auf Objektebene, um Zugriffs-Label auf die angegebenen Kompositionen anzuwenden.

  Weitere Informationen zur Verwendung von Zugriffs-Labels auf Objektebene finden Sie im [Handbuch zu Kompositionen](/help/compositions/gs-compositions.md).

* **Standardrollen**

  Sie können jetzt eine der Standardrollen verwenden, um Benutzerberechtigungen für den Zugriff auf die Komposition föderierter Zielgruppen zu verwalten.

  Weitere Informationen zu den Standardrollen finden Sie im [Handbuch zur Komposition föderierter Zielgruppen](/help/governance-privacy-security/access-control.md).

* **Inkrementelle Aktualisierungen in Anwendungsfällen für die Profilanreicherung**

  Die Aktivität „Profile speichern“ unterstützt jetzt inkrementelle Aktualisierungen. Mit inkrementellen Aktualisierungen können Sie inkrementelle Daten abfragen und aktualisieren und dabei Profile mit Daten aus externen Data Warehouses anreichern.

  Weitere Informationen zur Verwendung der Aktivität „Profile speichern“ finden Sie im [Handbuch zur Aktivität „Profile speichern“](/help/compositions/activities/save-profiles.md).

## Version Mai 2025 {#fac-25-5}

### Neue Funktionen {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>Arbeitsflächenansicht für Datenmodelle – allgemeine Verfügbarkeit</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Datenmodelle mit Arbeitsflächenansicht sind jetzt für alle Kundinnen und Kunden verfügbar!</p>
<p>Die Arbeitsflächenansicht für den Abschnitt „Datenmodelle“ sorgt für ein besseres Erlebnis. Denn sie ermöglicht neben der vorhandenen Tabellenansicht eine Visualisierung von Datenmodellen und deren Verknüpfungen in einem Arbeitsflächen-Layout.  </p>
<p>Weitere Informationen zur Arbeitsflächenansicht finden Sie unter <a href="../data-management/gs-models.md">Überblick über Datenmodelle</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#fac-25-5-improvements}

Diese Version enthält die folgenden Verbesserungen:

* **Rollenbasierte Zugriffskontrolle**

  Ab der Version Mai unterstützt die Funktion [!DNL Federated Audience Composition] neue granulare Berechtigungen zur Zugriffskontrolle. Benutzende können diese Berechtigungen Benutzerrollen zuweisen, um den Zugriff auf die [!DNL Federated Audience Composition] genauer zu steuern.

  Weitere Informationen zu den neuen Berechtigungen finden Sie unter [Zugreifen auf die Komposition föderierter Zielgruppen](/help/governance-privacy-security/access-control.md).

## Version April 2025 {#fac-25-4}

### Neue Funktionen {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>Arbeitsflächenansicht für Datenmodelle – Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Die Arbeitsflächenansicht für den Abschnitt „Datenmodelle“ sorgt für ein besseres Erlebnis. Denn sie ermöglicht neben der vorhandenen Tabellenansicht eine Visualisierung von Datenmodellen und deren Verknüpfungen in einem Arbeitsflächen-Layout.  </p>
<p>Die Arbeitsflächenansicht für Datenmodelle ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. </p>
<p>Weitere Informationen finden Sie in der <a href="../data-management/gs-models.md">ausführlichen Dokumentation</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>KI-Assistent zum Erwerb von Produktwissen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Der KI-Assistent ist eine Funktion der Benutzeroberfläche, mit der Sie durch Adobe-Konzepte navigieren und diese verstehen sowie betriebliche Erkenntnisse zu Ihrer Umgebung erhalten können. Er ist in verschiedenen Produkten in Adobe Experience Cloud verfügbar, einschließlich der Komposition föderierter Zielgruppen.</p>
<p>Weitere Informationen finden Sie in der <a href="../start/ai-assistant.md">ausführlichen Dokumentation</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktivität „Profile speichern“</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> Die Funktion „Komposition föderierter Zielgruppen“ unterstützt nun die Profilanreicherung als Anwendungsfall, sodass Kundinnen und Kunden bestehende Experience Platform-Profile mit Daten aus ihren externen Data Warehouses erweitern können.
</p>
<p>Weitere Informationen finden Sie in der <a href="../compositions/activities/save-profiles.md">ausführlichen Dokumentation</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Verbesserungen {#fac-25-4-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Datenmodellname**

  Im Menü „Zielgruppen“ wird auf der Registerkarte **Föderierte Kompositionen** nun der Datenmodellname anstelle der ID angezeigt, was mehr Klarheit bietet und die allgemeine Benutzerfreundlichkeit verbessert.

* **Zielgruppe**

  Im Menü „Zielgruppe“ wird nun der Name oder das Label des ausgewählten Datenmodells angezeigt, wenn Benutzende ein Datenmodell ohne verknüpfte Zielgruppen auswählen.

* **Export großer Zielgruppen**

  Die Funktion „Komposition föderierter Zielgruppen“ unterstützt nun den Export großer Zielgruppen mit Dateigrößen von mehr als 1 GB.

* **Aktivität „Zielgruppe speichern“**

  Der Aktivität **Zielgruppe speichern** wurde ein Hinweis hinzugefügt. Dieser erinnert Kundinnen und Kunden daran, mit Daten-Admins zusammenzuarbeiten, um Governance-Label auf neue Schemata und Datensätze anzuwenden, die während der Erstellung und Anreicherung der Zielgruppe erstellt wurden.
  [Weitere Informationen zu Datennutzungs-Labeln](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/labels/user-guide)

### Kompatibilität {#fac-25-4-compat}

* **Sichere Verbindung zu Amazon Redshift**

  Mit dieser neuen Version unterstützt die Funktion „Komposition föderierter Zielgruppen“ sichere Verbindungen über private Links zu Amazon Redshift-Datenbanken. [Weitere Informationen](../connections/home.md#amazon-redshift)

* **Google BigQuery**

  Mit dieser neuen Version unterstützt die Komposition föderierter Zielgruppen sichere VPN-Verbindungen zu Google BigQuery-Datenbanken. [Weitere Informationen](../connections/home.md#google-bigquery)

## Version März 2025 {#fac-25-3}

### Verbesserungen {#fac-25-3-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Berechtigungen zur Komposition föderierter Zielgruppen**

  Ab der Version März erzwingt [!DNL Federated Audience Composition] den Zugriff auf die Schnittstellen für **föderiertes Daten-Management** und **föderierte Kompositionen** für Benutzende, denen die Berechtigung **Föderierte Daten verwalten** zugewiesen wurde.

  Wir empfehlen Benutzenden, sich an die Admins zu wenden, damit diese Berechtigung ihrer Rolle hinzugefügt wird, um weiterhin auf die Benutzeroberfläche der [!DNL Federated Audience Composition] zugreifen zu können.

  Wie Sie diese Berechtigung zuweisen, erfahren Sie in der [entsprechenden Dokumentation](/help/governance-privacy-security/access-control.md).

### Kompatibilität {#fac-25-3-compat}

* **Databricks-Verbindung**

  Mit dieser neuen Version unterstützt die Komposition föderierter Zielgruppen jetzt die Konnektivität privater Links für Verbindungen zu Databricks-Datenbanken.
Dazu gehören sichere Verbindungen zu Databricks-Datenbanken, die auf Amazon Web Services (AWS) über einen privaten Link gehostet werden, und Databricks-Datenbanken, die auf Microsoft Azure über VPN gehostet werden. [Weitere Informationen](../connections/home.md#databricks)

* **Unterstützung für CDP-B2B-Kundschaft**

  Die Komposition föderierter Zielgruppen ist jetzt für B2B-Kundschaft (Business-to-Business) von Customer Data Platform (CDP) für personenbasierte Anwendungsfälle für Zielgruppen verfügbar.

* **Sichere Snowflake-Verbindung**

  Mit dieser neuen Version unterstützt die Komposition föderierter Zielgruppen sichere Verbindungen über private Links zu Snowflake-Datenbanken, die auf Microsoft Azure gehostet werden. [Weitere Informationen](../connections/home.md#snowflake)

## Version Februar 2025 {#fac-25-2}

Diese Version enthält die unten aufgeführten Änderungen.

* **Unterstützung für Microsoft Fabric**

  Sie können nun über die Funktion „Komposition föderierter Zielgruppen“ Verbindungen zu Microsoft Fabric-Datenbanken herstellen. [Weitere Informationen](../connections/home.md)

* **Unterstützung für Amazon Redshift Spectrum**

  Amazon Redshift Spectrum wird jetzt für Amazon Redshift-Datenbankverbindungen unterstützt. [Weitere Informationen](../connections/home.md#amazon-redshift)

* **Verbessertes Erlebnis bei der Schemaerstellung**

  Der Prozess der Schemaerstellung wurde durch eine aktualisierte Benutzeroberfläche verbessert, die intuitiver ist und eine einfachere Navigation bietet. Diese Verbesserungen bieten Datenverantwortlichen eine reibungslosere und effizientere Möglichkeit, Datenmodelle zu entwickeln. [Weitere Informationen](../customer/schemas.md)

* **Unterstützung der Zielgruppenanreicherung für Databricks**

  Sie können jetzt Databricks im Fluss „Zielgruppe lesen“ verwenden, wodurch Aktivitäten für Databricks-Datenbanken aktiviert werden und sie als neues Ziel eingerichtet werden können. [Weitere Informationen](../connections/destinations.md)

## Version November 2024 {#fac-24-11}

### Verbesserungen {#fac-24-11-improvements}

Diese Version enthält die unten aufgeführte Verbesserung.

* **IP-Adressen-Zulassungsliste**

  Beim Hinzufügen einer föderierten Datenbank in der Benutzeroberfläche von Adobe Experience Platform können Sie jetzt die IP-Adressen direkt anzeigen, die mit Ihren Instanzen der Komposition föderierter Zielgruppen verknüpft sind. Auf diese Weise können Sie diese IP-Adressen einfach kopieren und autorisieren, um eine Verbindung mit Ihrer Datenbank herzustellen und so die Sicherheit und Flexibilität zu verbessern. [Weitere Informationen](../connections/home.md)

## Version Oktober 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Die Komposition föderierter Zielgruppen in Adobe Experience Platform, die zuvor nur für eine Reihe von Organisationen verfügbar gewesen ist (LA), steht jetzt allen Benutzenden zur Verfügung (GA). Diese Funktion wird basierend auf Ihrem Angebot aktiviert und nur mit den zugehörigen Berechtigungen angezeigt. [Weitere Informationen](access-prerequisites.md)

### Kompatibilität {#fac-24-10-compat}

Mit dieser neuen Version ist die Komposition föderierter Zielgruppen nun mit den unten aufgeführten Systemen kompatibel.

* **Unterstützung für Databricks**

  Sie können nun über die Funktion „Komposition föderierter Zielgruppen“ Verbindungen zu Databricks-Datenbanken herstellen. [Weitere Informationen](../connections/home.md#databricks)

* **Unterstützung für sicheren Zugriff auf Snowflake über AWS PrivateLink**

  Sicherer Zugriff auf Ihr externes Snowflake-Data-Warehouse über einen privaten Link wird nun unterstützt. Ihr Snowflake-Konto muss auf Amazon Web Services (AWS) gehostet werden und sich in derselben Region wie Ihre Umgebung mit der Funktion „Komposition föderierter Zielgruppen“ befinden. Wenden Sie sich an den Adobe-Support, wenn Sie Hilfe benötigen, um einen sicheren Zugriff auf Ihr Snowflake-Konto einzurichten. [Weitere Informationen](../connections/home.md#snowflake)

* **Unterstützung für Amazon Redshift Serverless**

  Mit dieser neuen Version unterstützt die Funktion „Komposition föderierter Zielgruppen“ [Amazon Redshift Serverless](https://aws.amazon.com/de/redshift/redshift-serverless/){target="_blank"}.

### Verbesserungen {#fac-24-10-improvements}

Diese Version enthält die unten aufgeführten Verbesserungen.

* **Aktualisieren vorhandener Schemata**

  Wenn eine Spalte in einer föderierten Datenbank erstellt, geändert oder gelöscht wird, können Sie die Änderungen nun erkennen und anwenden, indem Sie im entsprechenden Schema auf die Schaltfläche **[!UICONTROL Schema aktualisieren]** klicken. [Weitere Informationen](../customer/schemas.md#schema-refresh)

* **Verknüpfen eines Datenmodells mit einer neuen Komposition**

  Beim Erstellen einer Komposition können Sie nun das Datenmodell auswählen, das ihr zugeordnet werden soll. Mit dieser neuen Option lassen sich Ihre Aktivitäten einfacher konfigurieren, da nur Tabellen des zugehörigen Datenmodells verfügbar sind. [Weitere Informationen](../compositions/create-composition.md)

## Version Juli 2024 – Komposition föderierter Zielgruppen (LA) {#fac-la}

Die Komposition föderierter Zielgruppen ermöglicht Unternehmen einen flexiblen und erweiterten Zugriff auf Unternehmens-Data-Warehouses, um Zielgruppen unter Verwendung wichtiger Unternehmensdatensätze zu komponieren sowie markeninitiierte und aktuelle Erlebnisse zu ermöglichen. Mit diesem neuen Ansatz können Sie als Benutzerin oder Benutzer von [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/home){target="_blank"} bzw. [Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/ajo-home){target="_blank"} Zielgruppendaten direkt aus Ihrem vorhandenen Data Warehouse zusammenführen, um die Zielgruppen von Adobe Experience Platform in einem einzigen System anzureichern.

Die Komposition föderierter Zielgruppen richtet sich an die wachsenden Anforderungen des Marktes an Unternehmen, die Flexibilität benötigen, um Zielgruppen mit Warehouse-Datensätzen zu komponieren. Auf diese Weise können Unternehmen die Datenbewegung reduzieren und gleichzeitig Marketing-Teams wichtige Zielgruppendaten zur Verfügung stellen, um die Anforderungen von Anwendungsfällen zu erfüllen und personalisierte Erlebnisse zu ermöglichen.

Weitere Informationen zu den Möglichkeiten der Komposition föderierter Zielgruppen finden Sie auf [dieser Seite](get-started.md) und in den [häufig gestellten Fragen](faq.md).

Ausführliche Informationen zu den Voraussetzungen für den Zugriff auf Kompositionen föderierter Zielgruppen und die aktuellen Leitlinien finden Sie auf [dieser Seite](access-prerequisites.md).
