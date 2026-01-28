---
audience: end-user
title: Überblick über Aktivitäten
description: Erfahren Sie mehr über die verschiedenen Aktivitäten und Transitionen, die in Kompositionen föderierter Zielgruppen verfügbar sind.
source-git-commit: 04f4edafd1c687b94bf5617458edf0866bba16fa
workflow-type: tm+mt
source-wordcount: '4662'
ht-degree: 99%

---

# Überblick über Aktivitäten

Sie können der Komposition föderierter Zielgruppen Aktivitäten und Transitionen hinzufügen, mit denen Sie Ihre Zielgruppe definieren können.

## Aktivitäten {#activities}

Mit Aktivitäten können Sie die Komponenten in der Zielgruppe definieren.

Es gibt **zwei** verschiedene Arten von Aktivitäten, die innerhalb einer Komposition föderierter Zielgruppen verwendet werden können: Targeting-Aktivitäten und Aktivitäten zur Flusssteuerung.

### Targeting-Aktivitäten {#targeting}

Mit Targeting-Aktivitäten können Sie definieren, woraus die Zielgruppe für die Komposition besteht.

#### Erstellen einer Zielgruppe

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Zielgruppe"
>abstract="Wählen Sie die Zielgruppe aus."

Mit der Aktivität **Zielgruppe erstellen** können Sie die Zielgruppenpopulation für die Komposition definieren. Sie können entweder eine bestehende Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Zielgruppe erstellen** zur Arbeitsfläche der Komposition hinzugefügt haben, geben Sie Ihrer Zielgruppe einen Namen. Sie können nun angeben, ob Sie eine Zielgruppe erstellen oder eine bestehende Zielgruppe verwenden möchten.

>[!BEGINTABS]

>[!TAB Erstellen einer neuen Zielgruppe]

Wählen Sie nach Auswahl von **Zielgruppe erstellen** das **Schema** für Ihre Zielgruppe aus. Mit dem Schema können Sie die vom Vorgang betroffene Population wie Empfängerinnen und Empfänger, Vertragsbegünstigte, Benutzerinnen und Benutzer oder Abonnierende definieren. Standardmäßig wird das Schema aus den Empfängerinnen und Empfängern ausgewählt. 

![](./assets/activities/build-audience-create.png)

Wählen Sie nach Auswahl eines Schemas **Weiter** aus. Sie können jetzt die Definition Ihrer Zielgruppe im Abfrage-Modeler definieren. Weitere Informationen zur Verwendung des Abfrage-Modelers finden Sie unter [Überblick über den Abfrage-Modeler](../query/home.md).

>[!TAB Verwenden einer bestehenden Zielgruppe]

Wählen Sie nach Auswahl von **Zielgruppe lesen** die Option **Weiter** aus.

![](./assets/activities/build-audience-read.png)

Sie können jetzt auswählen, welche Zielgruppe Sie für Ihre Komposition verwenden möchten.

>[!ENDTABS]

Nachdem Sie Ihre Optionen ausgewählt haben, können Sie **Ausgehende Transition erzeugen** auswählen. Die Auswahl dieser Option ermöglicht es Ihnen, eine ausgehende Transition hinzuzufügen, die am Ende der Aktivitätsausführung aktiviert wird, sofern die Zielgruppenpopulation leer ist.

+++

#### Datenquelle ändern

Mit der Aktivität **Datenquelle ändern** können Sie die von Ihrer Komposition verwendete Datenquelle ändern.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Datenquelle ändern** zur Arbeitsfläche der Komposition hinzugefügt haben, können Sie die Datenquelle definieren, die für die Komposition verwendet werden soll.

![Die Datenquellenoption wird im Arbeitsbereich „Komposition föderierter Zielgruppen“ hervorgehoben.](./assets/activities/configure.png){zoomable="yes"}{width="70%"}

| Quelle | Beschreibung |
| ------ | ----------- |
| Externes FDA-Konto | Eine externe Cloud-Datenbank, die mit der Komposition föderierter Zielgruppen verbunden ist. |

Nach Auswahl des **[!UICONTROL externen FDA-Kontos]** können Sie auswählen, mit welchem externen Konto Sie eine Verbindung herstellen möchten.

![Das Popover mit den Optionen für das externe Konto wird angezeigt.](./assets/activities/fda-external-account.png){zoomable="yes"}{width="70%"}

+++

#### Dimensionsänderung

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **[!UICONTROL Komplement erzeugen]** ein"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Aktivität „Dimensionsänderung“"
>abstract="Mithilfe dieser Aktivität können Sie das Schema, auch bekannt als Zielgruppendimension, beim Erstellen einer Zielgruppe ändern. Die Aktivität verschiebt die Achse je nach Datenvorlage und Eingabeschema.  Beispielsweise können Sie vom Schema „Verträge“ zum Schema „Kundinnen und Kunden“ wechseln."

Mit der Aktivität **Dimensionsänderung** können Sie das Schema (auch als Zielgruppendimension bezeichnet) Ihrer Komposition ändern.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Dimensionsänderung** zur Arbeitsfläche der Komposition hinzugefügt haben, können Sie ein neues Schema definieren, um das vorherige Schema zu ersetzen. Während dieser Schemaänderung werden alle Einträge beibehalten.

![](./assets/activities/change-dimension.png)

Nachdem Sie die Komposition ausgeführt haben, werden Ihre Ergebnisse aktualisiert.

+++

#### Kombinieren

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Die Aktivität „Kombinieren“"
>abstract="Die Aktivität **Kombinieren** ermöglicht die Segmentierung der eingehenden Population. Sie können also verschiedene Populationen vereinen, einen Teil daraus ausschließen oder nur die in mehreren Zielgruppen enthaltenen Datensätze verwenden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Optionen für das Zusammenführen von Schnittmengen"
>abstract="Eine **Schnittmenge** dient dazu, nur die Elemente beizubehalten, die den verschiedenen eingehenden Populationen in der Aktivität gemeinsam sind. Aktivieren Sie im Abschnitt **Zusammenzuführende Mengen** alle vorherigen Aktivitäten, die Sie zusammenfügen möchten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Optionen für die Zusammenführung von Ausschlüssen"
>abstract="Mit einem **Ausschluss** können Sie entsprechende Elemente gemäß bestimmten Kriterien aus einer Population ausschließen. Aktivieren Sie im Abschnitt **Zusammenzuführende Mengen** alle vorherigen Aktivitäten, die Sie zusammenfügen möchten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Auswählen des Segmentierungstyps"
>abstract="Wählen Sie aus, wie Zielgruppen kombiniert werden sollen: Vereinigung, Schnittmenge oder Ausschluss."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Abstimmoptionen für Schnittmengen"
>abstract="Wählen Sie den Abstimmtyp aus, um den Umgang mit Duplikaten zu definieren."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Abstimmoptionen"
>abstract="Wählen Sie den **Abstimmtyp** aus, um festzulegen, wie Duplikate behandelt werden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Ausschlussregeln"
>abstract="Bei Bedarf können Sie die eingehenden Tabellen anpassen. Um eine Zielgruppe aus einem anderen Schema, auch bekannt als Zielgruppendimension, auszuschließen, muss diese Zielgruppe tatsächlich auf dasselbe Schema wie die Hauptzielgruppe zurückgesetzt werden. Wählen Sie dazu im Abschnitt **Ausschlussregeln** die Option **Regel hinzufügen** aus und geben Sie die Bedingungen für die Schemaänderung an. Die Datenabstimmung wird entweder über ein Attribut oder über einen Join durchgeführt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Auswählen von Sets, die kombiniert werden sollen"
>abstract="Wählen Sie im Abschnitt **Zusammenzuführende Mengen** die **Hauptmenge** aus den eingehenden Transitionen. Dies ist die Menge, aus der Elemente ausgeschlossen werden. Die anderen Mengen stimmen mit Elementen überein, bevor sie aus der Primärmenge ausgeschlossen werden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Ausschlussregeln"
>abstract="Bei Bedarf können Sie die eingehenden Tabellen anpassen. Um eine Zielgruppe aus einem anderen Schema, auch bekannt als Zielgruppendimension, auszuschließen, muss diese Zielgruppe tatsächlich auf dasselbe Schema wie die Hauptzielgruppe zurückgesetzt werden. Wählen Sie dazu im Abschnitt **Ausschlussregeln** die Option **Regel hinzufügen** aus und geben Sie die Bedingungen für die Schemaänderung an. Die Datenabstimmung wird entweder über ein Attribut oder über einen Join durchgeführt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Kombinieren von „Komplement erzeugen“"
>abstract="Aktivieren Sie die Option **Komplement erzeugen**, um die verbleibende Population in einer zusätzlichen Transition zu verarbeiten."

>[!NOTE]
>
>Die Aktivität **Kombinieren** muss **unbedingt** nach einer anderen Aktivität platziert werden und **kann nicht** am Anfang der Komposition platziert werden.

Mit der Aktivität **Kombinieren** können Sie mehrere Zielgruppen auf unterschiedliche Weise zusammenführen: Vereinigung, Schnittmenge oder Ausschluss.

- **Vereinigung**: Bei einer Vereinigung werden die verschiedenen Zielgruppen zu einer einzigen Zielgruppe kombiniert. Dies entspricht einem ODER-Vorgang.
- **Schnittmenge**: Bei einer Schnittmenge werden die verschiedenen Zielgruppen zu einer einzigen Zielgruppe kombiniert, wobei nur der **gemeinsame** Inhalt beibehalten wird. Dies entspricht einem UND-Vorgang.
- **Ausschluss**: Bei einem Ausschluss werden die verschiedenen Zielgruppen ohne die angegebenen Ausschlussregeln zu einer einzigen Zielgruppe kombiniert. Dies entspricht einem XOR-Vorgang.

+++ Konfigurationsdetails

Fügen Sie nach dem Hinzufügen mehrerer Aktivitäten zum Erstellen von mindestens **zwei** verschiedenen Verzweigungen die Aktivität **Kombinieren** am Ende einer der Verzweigungen hinzu. Sie können jetzt eine der Kombinationsoptionen (Vereinigung, Schnittmenge oder Ausschluss) auswählen.

![](./assets/activities/combine.png)

>[!BEGINTABS]

>[!TAB Vereinigung]

![](./assets/activities/combine-union.png)

Bei Auswahl von **Vereinigung** müssen Sie den **Abstimmtyp** für die Aktivität „Kombinieren“ auswählen. Mit dem Abstimmtyp können Sie definieren, wie doppelte Einträge verarbeitet werden.

- **Nur die Schlüssel**: Wenn Sie **Nur die Schlüssel** auswählen, wird **ein** Element beibehalten, wenn mehrere Elemente denselben Schlüssel haben. Sie können diese Option nur verwenden, wenn die eingehenden Populationen homogen sind.
- **Auswahl an Spalten**: Wenn Sie **Auswahl an Spalten** auswählen, können Sie eine Liste an Spalten definieren, auf die die Datenabstimmung angewendet wird. Sie können den primären Datensatz auswählen, der die Quelldaten enthält, gefolgt von den für den Join zu verwendenden Spalten.

>[!TAB Schnittmenge]

![](./assets/activities/combine-intersection.png)

Bei Auswahl von **Schnittmenge** müssen Sie den **Abstimmtyp** für die Aktivität „Kombinieren“ auswählen. Mit dem Abstimmtyp können Sie definieren, wie doppelte Einträge verarbeitet werden.

- **Nur die Schlüssel**: Wenn Sie **Nur die Schlüssel** auswählen, wird **ein** Element beibehalten, wenn mehrere Elemente denselben Schlüssel haben. Sie können diese Option nur verwenden, wenn die eingehenden Populationen homogen sind.
- **Auswahl an Spalten**: Wenn Sie **Auswahl an Spalten** auswählen, können Sie eine Liste an Spalten definieren, auf die die Datenabstimmung angewendet wird.

Nach der Konfiguration des Abstimmtyps können Sie auch die Option **Komplement erzeugen** auswählen. Beim Erzeugen eines Komplements wird die verbleibende Population verarbeitet. Die Daten, die **nicht** Teil der Schnittmenge sind, sind dabei enthalten. Der Aktivität wird eine zusätzliche ausgehende Transition hinzugefügt.

>[!TAB Ausschluss]

![](./assets/activities/combine-exclusion.png)

Bei Auswahl von **Ausschluss** müssen Sie die **Hauptmenge** aus den eingehenden Transitionen auswählen. Dies entspricht den Mengen, aus denen die Elemente ausgeschlossen werden.

Nachdem Sie die Hauptmenge ausgewählt haben, können Sie Ihre **Ausschlussregeln** einrichten. Sie können entweder **Übereinstimmung mit Attribut** oder **Join** auswählen.

Nachdem Sie Ihre Ausschlussregeln konfiguriert haben, können Sie auch die Option **Komplement erzeugen** auswählen. Beim Erzeugen eines Komplements wird die verbleibende Population verarbeitet. Die Daten, die **nicht** Teil des Ausschlusses sind, sind dabei enthalten. Der Aktivität wird eine zusätzliche ausgehende Transition hinzugefügt.

+++

#### Deduplizierung

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Felder zum Identifizieren von Duplikaten"
>abstract="Wählen Sie im Abschnitt **[!UICONTROL Felder zum Identifizieren von Duplikaten]** die Schaltfläche **[!UICONTROL Attribut hinzufügen]** aus, um die Felder anzugeben, für die die Identifizierung von Duplikaten aufgrund identischer Werte ermöglicht werden soll, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Aktivität „Deduplizierung“"
>abstract="Mithilfe der Aktivität **Deduplizierung** lassen sich Duplikate in Ergebnissen aus eingehenden Aktivitäten löschen. Sie wird hauptsächlich im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendaten zulassen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **[!UICONTROL Komplement erzeugen]** ein"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Deduplizierungseinstellungen"
>abstract="Um Duplikate in den eingehenden Daten zu löschen, definieren Sie die Deduplizierungsmethode in den folgenden Feldern. Standardmäßig wird nur ein Eintrag beibehalten. Sie sollten außerdem die Deduplizierungsmethode anhand eines Ausdrucks oder Attributs auswählen. Standardmäßig wird der Eintrag, der von den Duplikaten ausgenommen sein soll, zufällig ausgewählt."

Die Aktivität **Deduplizierung** entfernt alle doppelten Ergebnisse innerhalb der Zielgruppe.

+++ Konfigurationsdetails

>[!NOTE]
>
>Wenn Sie über mehrere eingehende Transitionen verfügen, müssen Sie zunächst die **Hauptmenge** aus der Dropdown-Liste auswählen.

Nach Hinzufügen einer Aktivität des Typs **Deduplizierung** können Sie die Felder zum Identifizieren von Duplikaten auswählen. Wählen Sie **Attribut hinzufügen** aus, um die Felder zu identifizieren, in denen Duplikate auftreten können.

![](./assets/activities/deduplication.png)

Nachdem Sie die Felder identifiziert haben, können Sie Ihre Deduplizierungseinstellungen konfigurieren.

| Einstellung | Beschreibung |
| ------- | ----------- |
| Beizubehaltende Duplikate | Die Anzahl der doppelten Einträge, die beibehalten werden sollen. Wenn der Wert auf 0 festgelegt ist, werden **alle** doppelten Einträge beibehalten. |
| Deduplizierungsmethode | Die Methode zum Entfernen der doppelten Einträge. <ul><li>**Zufällige Auswahl**: Der entfernte Eintrag wird zufällig ausgewählt.</li><li>**Von einem Ausdruck ausgehend**: Der entfernte Eintrag basiert auf dem übermittelten Ausdruck. Sie können abhängig von den zu entfernenden Werten entweder in aufsteigender oder absteigender Reihenfolge sortieren.</li><li>**Wert nicht leer**: Der entfernte Eintrag basiert auf dem übermittelten Ausdruck. Es werden die Einträge entfernt, für die der Ausdruck keinen Wert hat.</li><li>**Gemäß einer Werteliste**: Der entfernte Eintrag basiert auf dem übermittelten Feld oder Ausdruck. Sie können die verbleibenden Werte zufällig, in aufsteigender oder absteigender Reihenfolge sortieren.</li></ul> |

Darüber hinaus können Sie die Option **Komplement erzeugen** auswählen. Beim Erzeugen eines Komplements wird die verbleibende Population verarbeitet. Die Daten, die **nicht** Teil der Deduplizierung sind, sind dabei enthalten. Der Aktivität wird eine zusätzliche ausgehende Transition hinzugefügt.

+++

#### Anreicherung

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Aktivität „Anreicherung“"
>abstract="Die Aktivität **Anreicherung** ermöglicht es Ihnen, die Zielgruppendaten um zusätzliche Informationen aus der Datenbank zu erweitern. Sie wird in einer Komposition häufig nach den Segmentierungsaktivitäten verwendet."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Aktivität „Anreicherung“"
>abstract="Nachdem Anreicherungsdaten zur Komposition hinzugefügt wurden, können sie in den Aktivitäten verwendet werden, die nach der Aktivität **Anreicherung** hinzugefügt wurden, um Profile basierend auf ihren Verhaltensweisen, Voreinstellungen und Auswahlmöglichkeiten in separate Gruppen zu segmentieren."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Verknüpfungsdefinition"
>abstract="Erstellen Sie eine Verknüpfung zwischen den Arbeitstabellendaten und der föderierten Datenbank."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Abstimmung der Anreicherung"
>abstract="Legen Sie die Abstimmparameter fest."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Anreicherungsdaten"
>abstract="Wählen Sie die zur Anreicherung Ihrer Komposition zu verwendenden Daten aus. Sie können zwei Arten von Anreicherungsdaten auswählen: ein einzelnes Anreicherungsattribut aus dem Schema, auch bekannt als Zielgruppendimension, oder eine Sammlungsrelation, bei der es sich um eine Verknüpfung mit einer 1:n-Kardinalität zwischen Tabellen handelt."

Mit der Aktivität **Anreicherung** können Sie Ihre Komposition durch Hinzufügen zusätzlicher Daten aus der föderierten Datenbank erweitern.

Wenn Sie eine Verbindung zum Ziel „Komposition föderierter Zielgruppen“ konfiguriert haben, können Sie mit der Aktivität „Anreicherung“ Daten aus Adobe Experience Platform mit Attributen aus Ihrer externen Datenbank anreichern. [Erfahren Sie, wie Sie Adobe Experience Platform-Zielgruppen mit externen Daten anreichern](../connections/destinations.md)

+++ Konfigurationsdetails

>[!NOTE]
>
>Wenn Sie über mehrere eingehende Transitionen verfügen, müssen Sie zunächst die **Hauptmenge** aus der Dropdown-Liste auswählen.

Nachdem Sie die Aktivität **Anreicherung** zu Ihrer Komposition hinzugefügt haben, können Sie **Anreicherungsdaten hinzufügen** auswählen, um das Attribut auszuwählen, das Sie zur Anreicherung Ihrer Komposition verwenden möchten. Sie können **Ausdruck bearbeiten** auswählen, um einen erweiterten Ausdruck zur Auswahl des Attributs zu erstellen.

![](./assets/activities/enrichment.png)

+++

#### Abstimmung

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Aktivität „Abstimmung“"
>abstract="Mit der Aktivität **Abstimmung** können Sie die Verknüpfung zwischen den Daten in der Datenbank und den Daten in einer Arbeitstabelle definieren."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Abstimmung – Feld auswählen"
>abstract="Abstimmung – Feld auswählen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Abstimmung – Bedingung erstellen"
>abstract="Abstimmung – Bedingung erstellen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Abstimmung – Komplement erzeugen"
>abstract="Abstimmung – Komplement erzeugen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Wählen Sie das neue Schema aus, das auf die Daten angewendet werden soll. Mit einem Schema, auch bekannt als Zielgruppendimension, können Sie die Zielpopulation definieren: Empfängerinnen und Empfänger, Abonnentinnen und Abonnenten der App, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw. Standardmäßig ist das aktuelle Schema der Komposition ausgewählt. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Abstimmungsregeln"
>abstract="Wählen Sie die für die Deduplizierung zu verwendenden Abstimmungsregeln aus. Um Attribute zu verwenden, wählen Sie die Option **Einfache Attribute** und dann die Quell- und Zielfelder aus. Um mithilfe des Abfrage-Modelers eine eigene Abstimmbedingung zu erstellen, wählen Sie die Option **Erweiterte Abstimmbedingungen** aus."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Auswählen der Zielgruppendimension"
>abstract="Wählen Sie das Schema, auch bekannt als Zielgruppendimension, für Ihre eingehenden Daten zum Abstimmen aus."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Beibehalten nicht abgestimmter Daten"
>abstract="Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und stehen in der Arbeitstabelle zur späteren Verwendung zur Verfügung. Um nicht abgestimmte Daten zu entfernen, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Abstimmattribut"
>abstract="Wählen Sie das Attribut aus, das zur Abstimmung der Daten verwendet werden soll, und bestätigen Sie den Vorgang."

>[!NOTE]
>
>Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und sind in der Arbeitstabelle zur zukünftigen Verwendung verfügbar. Wenn Sie **nicht** möchten, dass abgestimmte Daten verwendet werden, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**.

Mit der Aktivität **Abstimmung** können Sie die Verknüpfung zwischen den Daten in der föderierten Datenbank und den Daten in einer Arbeitstabelle definieren.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Abstimmung** zu Ihrer Komposition hinzugefügt haben, können das Schema auswählen, das für die Abstimmung verwendet werden soll.

Nachdem Sie das Schema ausgewählt haben, müssen Sie Ihre Abstimmregeln einrichten. Sie können zwischen **Einfache Attribute** oder **Erweiterte Abstimmbedingungen** auswählen.

>[!BEGINTABS]

>[!TAB Einfache Attribute]

Wählen Sie nach Auswahl von **Einfache Attribute** die Option **Regel hinzufügen** aus. Sie können jetzt die Abstimmung einrichten, indem Sie die Felder **Quelle** und **Ziel** hinzufügen. Das Feld **Ziel** entspricht den Feldern des ausgewählten Schemas.

![](./assets/activities/reconciliation-rules.png)

Daten werden abgestimmt, wenn Quelle und Ziel gleich sind. Sie können weitere Abstimmkriterien hinzufügen, indem Sie **Regel hinzufügen** auswählen. Wenn mehrere Join-Bedingungen angegeben sind, müssen **alle** überprüft werden, damit die Daten miteinander verknüpft werden können.

>[!TAB Erweiterte Abstimmbedingungen]

Wählen Sie nach Auswahl von **Erweiterte Abstimmbedingungen** die Option **Bedingungen erstellen** aus. Sie können nun mithilfe des Abfrage-Modelers eine eigene Abstimmbedingung erstellen. Weitere Informationen zur Verwendung des Abfrage-Modelers finden Sie unter [Überblick über den Abfrage-Modeler](../query/home.md).

![](./assets/activities/reconciliation-advanced.png)

>[!ENDTABS]

Sie können die abgestimmten Daten auch filtern. Wählen Sie **Filter erstellen** aus, um mithilfe des Abfrage-Modelers eine benutzerdefinierte Bedingung zu erstellen. Weitere Informationen zur Verwendung des Abfrage-Modelers finden Sie unter [Überblick über den Abfrage-Modeler](../query/home.md).

+++

#### Speichern einer Zielgruppe

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Speichern einer Zielgruppe"
>abstract="Mit dieser Aktivität können Sie eine neue Zielgruppe aus der Population erstellen, die im Vorfeld der Komposition ermittelt wurde. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste hinzugefügt und sind über das Menü **Zielgruppen** zugänglich."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Ausgehende Transition generieren"
>abstract="Verwenden Sie diese Option, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Feld „Primäre Identität“"
>abstract="Wählen Sie die primäre Identität aus, die für Profile verwendet werden soll."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Identity-Namespace"
>abstract="Wählen Sie den Namespace aus, der für Profile verwendet werden soll."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/identity/features/namespaces" text="Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Platform"

>[!IMPORTANT]
>
>Wenn Ihre Sandbox eine Zusammenführungsrichtlinie mit **Datensatzpriorität** verwendet, wenden Sie sich an die Adobe-Kundenunterstützung, um den Datensatz `Halos UPS` zu Ihrer Zusammenführungsrichtlinie hinzuzufügen.
>
>Weitere Informationen zu Zusammenführungsrichtlinien finden Sie im [Überblick über Zusammenführungsrichtlinien](https://experienceleague.adobe.com/de/docs/experience-platform/profile/merge-policies/overview).

Mit der Aktivität **Zielgruppe speichern** können Sie eine Zielgruppe basierend auf der Komposition erstellen. Nachdem die Zielgruppe erstellt wurde, können Sie sie im Zielgruppenportal in Adobe Experience Platform verwenden. Weitere Informationen zum Verwenden von Zielgruppen mit der Komposition föderierter Zielgruppen finden Sie unter [Überblick über Zielgruppen](../start/audiences.md). Weitere Informationen zu Zielgruppen in Experience Platform finden Sie unter [Überblick über das Zielgruppenportal](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

+++ Konfigurationsdetails

>[!IMPORTANT]
>
>Der Name der Zielgruppe **muss** innerhalb der aktuellen Sandbox eindeutig sein und darf nicht derselbe Name wie der einer vorhandenen Zielgruppe sein.

Nachdem Sie die Aktivität **Zielgruppe speichern** zu Ihrer Komposition hinzugefügt haben, können Sie den Namen der neu erstellten Zielgruppe angeben.

![](./assets/activities/save-audience.png)

Jetzt können Sie die Zuordnungen angeben, um auszuwählen, welche Felder Sie an die neu erstellte Zielgruppe übertragen möchten. Wählen Sie **Zielgruppenzuordnung hinzufügen** und anschließend das Quellzielgruppenfeld und das Zielgruppenfeld aus. Wiederholen Sie dies so oft wie nötig.

Nachdem Sie die Zuordnungen hinzugefügt haben, können Sie die primäre Identität und den Namespace auswählen, um die Zielgruppenprofile in der Datenbank zu identifizieren. Das Feld für die primäre Identität wird zur Identifizierung der Profile verwendet, während der Identity-Namespace als Schlüssel zur Identifikation der Identität dient.

Darüber hinaus können Sie den Datenablauf für die Zielgruppe festlegen. Der Ablauf von Daten bestimmt die Anzahl der Tage, nach denen die Zielgruppenzugehörigkeit abläuft. Der Ablauf der Daten kann 1 bis 90 Tage betragen. Standardmäßig ist dieser Wert auf 30 festgelegt.

+++

#### Aufspaltung

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Aktivität „Aufspaltung“"
>abstract="Mit der Aktivität **Aufspaltung** können eingehende Populationen basierend auf unterschiedlichen Auswahlkriterien in mehrere Teilmengen segmentiert werden, z. B. Filterregeln oder Populationsgröße."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segmente für die Aktivität „Aufspaltung“"
>abstract="Es können beliebig viele Teilmengen hinzugefügt werden, um die eingehende Population zu segmentieren.<br/></br>Bei Ausführung der Aktivität **Aufspaltung** wird die Population sukzessive in unterschiedliche Teilmengen segmentiert, und zwar in der Reihenfolge, in der diese zur Aktivität hinzugefügt werden. Man sollte sich vor dem Start Ihrer Komposition vergewissern, dass die Teilmengen mithilfe der Pfeilschaltflächen in der passenden Reihenfolge angeordnet wurde."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Filter für die Aufspaltungsaktivität"
>abstract="Wählen Sie zum Anwenden einer Filterbedingung auf eine Teilmenge **[!UICONTROL Filter erstellen]** aus und konfigurieren Sie die gewünschte Filterregel mithilfe des Abfrage-Modelers. Es können beispielsweise alle Profile aus der eingehenden Population eingeschlossen werden, deren E-Mail-Adresse in der Datenbank vorhanden ist."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Begrenzung der Aufspaltungsaktivität"
>abstract="Um die Anzahl der von der Teilmenge ausgewählten Profile zu begrenzen, muss **[!UICONTROL Grenzwert aktivieren]** aktiviert und die Anzahl oder der Prozentsatz der einzuschließenden Population angegeben werden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Sortierung der Aufspaltungsaktivität"
>abstract="Beim Festlegen einer Populationsbegrenzung für eine Teilmenge können die ausgewählten Profile anhand eines bestimmten Profilattributs in auf- oder absteigender Reihenfolge sortiert werden. Dazu die Option **Sortierung aktivieren** einschalten. Teilmengen können z. B. so eingeschränkt werden, dass nur die 50 Top-Profile mit dem höchsten Einkaufsbetrag einbezogen werden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Aufspaltung – Komplement erzeugen"
>abstract="Nachdem Sie alle Teilmengen konfiguriert haben, kann die verbleibende Population ausgewählt werden, die keiner der Teilmengen entspricht, und in eine zusätzliche ausgehende Transition eingeschlossen werden. Schalten Sie dazu die Option **Komplement erzeugen** ein."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Alle Teilmengen in derselben Tabelle erzeugen"
>abstract="Diese Option aktivieren, um alle Teilmengen in einer Ausgabetransition zusammenzufassen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Leere Transition überspringen"
>abstract="Die Option **[!UICONTROL Leere Transition überspringen]** aktivieren, um die ausgehende Transition für diese Teilmenge zu deaktivieren, wenn die Eingangspopulation leer ist."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Überschneidung der Ausgabepopulationen zulassen"
>abstract="Die Option **[!UICONTROL Überschneidung der Ausgabepopulationen zulassen]** ermöglicht den Umgang mit Profilen, die in mehreren Teilmengen enthalten sind. Wenn das Kästchen nicht aktiviert ist, stellt die Aufspaltungsaktivität sicher, dass eine Empfängerin oder ein Empfänger nicht in mehreren Ausgangstransitionen vorhanden sein kann, selbst wenn sie bzw. er die Kriterien mehrerer Teilmengen erfüllt. Sie bzw. er befindet sich in der Zielgruppe der ersten Registerkarte mit entsprechenden Kriterien. Wenn das Kästchen aktiviert ist, können die Empfangenden in mehreren Teilmengen gefunden werden, falls sie ihren Filterkriterien entsprechen. "

Die Aktivität **Aufspaltung** unterteilt die eingehende Population je nach den angegebenen Kriterien in mehrere Teile.

+++ Konfigurationsdetails

>[!IMPORTANT]
>
>Bei Ausführung der Aktivität **Aufspaltung** wird die Population auf die verschiedenen Teilmengen aufgeteilt, und zwar in der **Reihenfolge, in der diese hinzugefügt wurden**. Wenn beispielsweise 70 % der Anfangspopulation auf die erste Teilmenge aufgespaltet werden, werden die Auswahlkriterien der nächsten Teilmenge nur auf die restlichen 30 % angewendet.
>
>Stellen Sie vor dem Ausführen der Komposition sicher, dass Sie die Teilmengen in der Reihenfolge sortiert haben, in der die Aufspaltung ausgeführt werden soll.

Nachdem Sie die Aktivität **Aufspaltung** zu Ihrer Komposition hinzugefügt haben, können Sie nun die Teilmengen Ihrer Zielgruppe bestimmen. Wählen Sie **Segment hinzufügen** aus, um die verschiedenen Verzweigungspfade zu erstellen.

Sie können jetzt Details für jeden dieser Teilpfade angeben. Sie können dem Teilpfad einen Namen sowie Filterbedingungen geben. Wählen Sie zum Erstellen einer Filterbedingung **Filter erstellen** aus und konfigurieren Sie die Filterregel mithilfe des Abfrage-Modelers. Weitere Informationen zur Verwendung des Abfrage-Modelers finden Sie unter [Überblick über den Abfrage-Modeler](../query/home.md).

Nachdem Sie Ihre Filterbedingung erstellt haben, können Sie die folgenden zusätzlichen Regeln anwenden:

- **Grenzwert aktivieren**: Begrenzt die Anzahl der Profile, die in die Teilmenge aufgespaltet werden dürfen. Sie können dies als eine Zahl oder einen Prozentsatz der Population festlegen.
   - Wenn Sie einen Grenzwert aktivieren, können Sie die ausgewählten Profile auch nach einem bestimmten Profilattribut ordnen. Aktivieren Sie **Sortierung aktivieren**, um die Attribute in aufsteigender oder absteigender Reihenfolge zu sortieren.
- **Leere Transition überspringen**: Deaktiviert die Transition, wenn die eingehende Population leer ist.

Nach der Konfiguration der Teilmengen können Sie einige weitere Optionen festlegen.

| Optionen | Beschreibung |
| ------- | ----------- |
| **Komplement erzeugen** | Erstellt eine ausgehende Transition, die die verbleibende Population enthält. |
| **Überschneidung der Ausgabepopulationen zulassen** | Wenn diese Option aktiviert ist, kann die Empfängerin bzw. der Empfänger **nicht** in mehreren ausgehenden Transitionen enthalten sein, sondern ist **nur** in der ersten ausgehenden Transition enthalten. Wenn diese Option deaktiviert ist, **kann** die Empfängerin bzw. der Empfänger in mehreren ausgehenden Transitionen enthalten sein. |
| **Alle Teilmengen in derselben Tabelle erzeugen** | Gruppiert alle Teilmengen in einer einzigen ausgehenden Transition. |

+++

### Aktivitäten zur Flusssteuerung {#flow-control}

Mit Aktivitäten zur Flusssteuerung können Sie die Organisation und Koordinierung Ihrer Komposition definieren.

#### Und-Verknüpfung

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Aktivität „UND-Verknüpfung“"
>abstract="Die Aktivität **Und-Verknüpfung** ermöglicht es, die Ausführung verschiedener Kompositionsverzweigungen zu synchronisieren. Sie wird ausgelöst, sobald alle vorangehenden Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten abgeschlossen sind, bevor Sie mit der Ausführung der Komposition fortfahren."

Mit der Aktivität **UND-Verknüpfung** können Sie mehrere Verzweigungen einer Komposition miteinander kombinieren. Diese Aktivität wird erst ausgelöst, wenn **alle** eingehenden Transitionen aktiviert sind.

+++ Konfigurationsdetails

Nachdem Sie mehrere Aktivitäten zum Erstellen von mindestens zwei verschiedenen Verzweigungen hinzugefügt haben, können Sie die Aktivität **UND-Verknüpfung** am Ende einer der Verzweigungen hinzufügen.

![](./assets/activities/and-join.png)

Im Abschnitt **Zusammenführungsoptionen** können Sie alle Aktivitäten auswählen, die Sie synchronisieren möchten. Darüber hinaus können Sie in der Dropdown-Liste **Hauptmenge** auswählen, welche eingehende Transition beibehalten werden soll.

+++

#### Ende

Die Aktivität **Ende** kennzeichnet das Ende der Komposition grafisch und hat keine funktionalen Auswirkungen.

#### Verzweigung

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork"
>title="Aktivität „Verzweigung“"
>abstract="Die Aktivität **Verzweigung** ermöglicht es Ihnen, ausgehende Transitionen zu erstellen, um mehrere Aktivitäten parallel zu starten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork_transitions"
>title="Transitionen von Verzweigungsaktivitäten"
>abstract="Standardmäßig werden zwei Transitionen mit einer **Verzweigungsaktivität** erstellt. Wählen Sie die Schaltfläche **Transition hinzufügen** aus, um eine zusätzliche ausgehende Transition zu definieren, und geben Sie deren Label ein."

Mit der Aktivität **Verzweigung** können Sie mehrere ausgehende Transitionen erstellen, die gleichzeitig mehrere Aktivitäten starten.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Verzweigung** zu Ihrer Komposition hinzugefügt haben, werden automatisch zwei ausgehende Transitionen generiert. Sie können diesen ausgehenden Transitionen einen Namen geben. Darüber hinaus können Sie **Transition hinzufügen** auswählen, um eine weitere ausgehende Transition hinzuzufügen.

![](./assets/activities/fork.png)

+++

#### Planung

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Aktivität „Planung“"
>abstract="Mit der Aktivität **Planung** können Sie planen, wann die Zielgruppenkomposition gestartet werden soll. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität einer Komposition verwendet werden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Gültigkeit der Planung"
>abstract="Sie können einen Gültigkeitszeitraum für die Planung definieren. Er kann dauerhaft sein (Standard) oder bis zu einem bestimmten Datum gültig sein."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Planungsoptionen"
>abstract="Definieren Sie die Häufigkeit der Planung. Er kann zu einem bestimmten Zeitpunkt, einmal oder mehrmals pro Tag, Woche oder Monat, ausgeführt werden."

Mit der Aktivität **Planung** können Sie planen, wann die Ausführung der Komposition starten soll. Sie **müssen** diese als erste Aktivität der Komposition verwenden.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Planung** zu Ihrer Komposition hinzugefügt haben, können Sie die **Ausführungshäufigkeit** für die Komposition festlegen. Die Optionen sind **Einmal**, **Täglich**, **Mehrmals täglich**, **Wöchentlich** und **Monatlich**.

>[!BEGINTABS]

>[!TAB Einmal]

>[!NOTE]
>
>Die Zeit ist auf „UTC“ festgelegt.

Wenn Sie **Einmal** auswählen, wird die Komposition nur einmal ausgeführt. Sie können das Datum und die Uhrzeit der Ausführung der Komposition auswählen.

>[!TAB Täglich]

Wenn Sie **Täglich** auswählen, wird die Komposition einmal täglich ausgeführt. Sie können im Abschnitt **Tag des Monats** jedoch auswählen, an welchem Tag des Monats die Komposition ausgeführt wird. Mögliche Werte sind **Jeden Tag**, **An Wochentagen**, **Über einen ausgewählten Zeitraum** und **Ausgewählte Wochentage**.

| Tag des Monats | Beschreibung |
| ---------------- | ----------- |
| Jeden Tag | Die Komposition wird jeden Tag ausgeführt. |
| An Wochentagen | Die Komposition wird an jedem Wochentag ausgeführt. |
| Über einen ausgewählten Zeitraum | Die Komposition wird während des ausgewählten Zeitraums jeden Tag ausgeführt. Sie können die Länge des Wiederholungszeitraums sowie das Datum festlegen, an dem der Zeitraum beginnt. |
| Ausgewählte Wochentage | Die Komposition wird an jedem ausgewählten Wochentag ausgeführt. |

Nachdem Sie ausgewählt haben, an welchem Tag des Monats der Zeitplan ausgeführt wird, können Sie **Startzeiten in der Vorschau** auswählen, um den Zeitplan der nächsten zehn Ausführungen Ihrer Komposition zu überprüfen.

>[!TAB Mehrmals täglich]

Wenn Sie **Mehrmals täglich** auswählen, wird die Komposition mehrmals am Tag ausgeführt. Sie können auswählen, ob die Komposition zu bestimmten Zeiten am Tag oder regelmäßig in festgelegten Zeitabständen ausgeführt wird.

Wenn Sie **Ausgewählte Stunden** auswählen, können Sie die bestimmten Zeiten für die Ausführung der Komposition auswählen. Wenn Sie **Periodisch** auswählen, können Sie festlegen, wie oft die Komposition in Stunden oder Minuten und innerhalb welcher Zeiten sie ausgeführt wird. Alle Zeiten sind in der Zeitzone „UTC“ angegeben.

Nachdem Sie die Stunden ausgewählt haben, können Sie im Abschnitt **Tag des Monats** auswählen, wie oft die Ausführung stattfindet.

| Tag des Monats | Beschreibung |
| ---------------- | ----------- |
| Jeder Wochentag | Die Komposition wird jeden Tag ausgeführt. |
| An bestimmten Wochentagen | Die Komposition wird an jedem ausgewählten Wochentag ausgeführt. |

Nachdem Sie ausgewählt haben, an welchem Tag des Monats der Zeitplan ausgeführt wird, können Sie **Startzeiten in der Vorschau** auswählen, um den Zeitplan der nächsten zehn Ausführungen Ihrer Komposition zu überprüfen.

>[!TAB Wöchentlich]

Wenn Sie **Wöchentlich** auswählen, wird die Komposition mit der festgelegten wöchentlichen Häufigkeit ausgeführt. Wenn Sie die wöchentliche Häufigkeit als eine Zahl größer als 1 festlegen, können Sie auch das Datum auswählen, ab dem die Ausführung beginnt.

Nachdem Sie die Auswertungshäufigkeit ausgewählt haben, können Sie im Abschnitt **Tag des Monats** auswählen, wie oft die Ausführung stattfindet.

| Tag des Monats | Beschreibung |
| ---------------- | ----------- |
| Jeder Wochentag | Die Komposition wird jeden Tag ausgeführt. |
| An bestimmten Wochentagen | Die Komposition wird an jedem ausgewählten Wochentag ausgeführt. |

Nachdem Sie ausgewählt haben, an welchem Tag des Monats der Zeitplan ausgeführt wird, können Sie **Startzeiten in der Vorschau** auswählen, um den Zeitplan der nächsten zehn Ausführungen Ihrer Komposition zu überprüfen.

>[!TAB Monatlich]

Wenn Sie **Monatlich** auswählen, wird die Komposition mit der festgelegten monatlichen Häufigkeit ausgeführt. Sie können sie entweder auf jeden Monat oder auf bestimmte Monate festlegen.

Nachdem Sie die monatliche Häufigkeit ausgewählt haben, können Sie den **Tag des Monats** auswählen, an dem die Ausführung stattfindet.

| Tag des Monats | Beschreibung |
| ---------------- | ----------- |
| Jeden Tag | Die Komposition wird jeden Tag ausgeführt. |
| An Wochentagen | Die Komposition wird an jedem Wochentag ausgeführt. |
| Über einen ausgewählten Zeitraum | Die Komposition wird während des ausgewählten Zeitraums jeden Tag ausgeführt. Sie können die Länge des Wiederholungszeitraums sowie das Datum festlegen, an dem der Zeitraum beginnt. |
| Ausgewählte Wochentage | Die Komposition wird an jedem ausgewählten Wochentag ausgeführt. |

Nachdem Sie den **Tag des Monats** festgelegt haben, können Sie die Startzeit auswählen. Alle Zeiten sind in der Zeitzone „UTC“ angegeben.

>[!ENDTABS]

Nach Auswahl der Ausführungshäufigkeit können Sie den **Gültigkeitszeitraum** des Zeitplans auswählen.

| Gültigkeitszeitraum | Beschreibung |
| --------------- | ----------- |
| **Dauerhaft (läuft nie ab)** | Die Komposition läuft nie ab. |
| **Gültigkeitszeitraum** | Die Komposition wird im angegebenen Datumsbereich ausgeführt. |

+++

#### Warten

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Aktivität „Warten“"
>abstract="Die Aktivität **Warten** wird verwendet, um die Transition von einer Aktivität zu einer anderen zu verzögern."

Die Aktivität **Warten** hält die Ausführung der Komposition für die angegebene Zeitdauer an.

+++ Konfigurationsdetails

Nachdem Sie die Aktivität **Warten** zu Ihrer Komposition hinzugefügt haben, können Sie die Wartezeit entweder als **Dauer** oder bis zu einem **festen Zeitpunkt** festlegen.

![](./assets/activities/wait.png)

Wenn Sie eine Dauer auswählen, können Sie den Zeitraum für die Wartezeit festlegen. Dieser Zeitraum kann in Sekunden, Minuten, Stunden oder Tagen angegeben werden.

Wenn Sie einen festen Zeitpunkt auswählen, können Sie festlegen, dass die Komposition bis zum angegebenen Datum und zur angegebenen Uhrzeit wartet. Die Uhrzeit wird in Ihrer **lokalen Zeitzone** angegeben.

+++

## Transitionen {#transitions}

Transitionen zeigen in Kompositionen, wie Daten von einer Aktivität zu einer anderen übertragen werden. Die Transitionen speichern die Daten in einer temporären Arbeitstabelle. Wenn Sie die Transition auswählen, können Sie folgende Informationen anzeigen:

- **Vorschau des Schemas**: Sie können diese Option auswählen, um das Schema für die Arbeitstabelle anzuzeigen.
- **Vorschau der Ergebnisse**: Sie können diese Option auswählen, um die Daten zu visualisieren, die in der ausgewählten Transition übertragen werden. Diese Option ist nur verfügbar, wenn die Option **Zwischen zwei Ausführungen die ermittelte Population festhalten** aktiviert ist. 

![](assets/transition-preview.png)

## Nächste Schritte {#next-steps}

Nach dem Lesen dieses Handbuchs verfügen Sie über umfangreichere Kenntnisse im Hinblick auf Aktivitäten und Transitionen, die Sie in einer Komposition verwenden können. Weitere Informationen zu Kompositionen im Allgemeinen finden Sie unter [Überblick über Kompositionen](./create-composition.md).
