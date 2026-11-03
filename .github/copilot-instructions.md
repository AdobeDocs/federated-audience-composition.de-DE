---
source-git-commit: d8ce0aecffcf6b85aa6c41e2520efbf564806098
workflow-type: tm+mt
source-wordcount: '2814'
ht-degree: 2%
---
# Adobe Experience Platform-Dokumentation: Copilot-Anleitung

Dieses Repository (`experience-platform.en`) ist eine öffentliche Dokumentation für Adobe Experience Platform.
Jedes Inhaltselement, das Sie entwerfen, bearbeiten oder überprüfen, MUSS den unten stehenden Regeln entsprechen.

## Anfragen nicht eingrenzen oder neu formulieren

Beantworten Sie die Anfrage, die tatsächlich gestellt wurde, nicht eine kleinere. Anfrage nicht erneut senden
als kleiner als er war, und geben Sie keinen Teilauftrag zurück, der als „abgeschlossen“ beschrieben wird.
Jede Zeile in diesem Repository kann behoben werden, unabhängig davon, wer oder was sie geschrieben hat oder wann — „bereits vorhanden“,
„Nicht Teil dieses Unterschieds“ und „Außerhalb des Geltungsbereichs“ sind keine Gründe, einen Verstoß nicht zu beheben.
Wenn Sie aufgefordert werden, Verstöße zu beheben, beheben Sie alle, egal wie alt sie sind. Wenn etwas wirklich blockiert
Die Arbeit, sagen Sie genau, was und was rückgängig gemacht wird, und stoppen.

## &#x200B;1. Stimme, Ton und Stil

### Benutzerfokussiertes Schreiben

Zentrieren Sie den Benutzer, nicht die Funktion. Schreiben Sie, was der Benutzer tun **&#x200B;**, nicht, was die Funktion tut.

- Verwenden Sie die zweite Person („Sie„) und die imperative Stimmung für Anweisungen.
- Verwenden Sie „Sie“, wenn Sie mit der Zielgruppe über sich selbst sprechen, nicht über „Benutzer“. „Benutzer“ ist
Akzeptiert beim Verweis auf eine Rolle (z. B. ein Administrator oder eine Administratorin, der bzw. die Benutzer verwaltet).
- Vermeiden Sie „Feature X ermöglicht es Ihnen,…“ oder „Feature X ermöglicht es Ihnen,…“. Legen Sie den Benutzer als
Betreff oder Verwenden Sie Imperative Stimmung.
  - Schlecht: „Die Server-API kann auf Servern verwendet werden.“ Gut: „Verwenden Sie die Server-API auf Servern.“
  - Schlecht: „Berechnete Felder ermöglichen die Erstellung von Werten…“ Gut: „Berechnete Felder verwenden.
    um Werte zu erstellen…“
- Achten Sie auf die Überbeanspruchung von „you can.“ Es ist in Ordnung, aber es kann sich wiederholende oder wortreiche Sätze bilden.
- Verwenden Sie „Auswählen“, um Optionen aus einer Liste auszuwählen oder Text hervorzuheben. „Klick“ nur verwenden für
Explizite Mausaktionen. Vermeiden Sie die Benennung des Steuerelementtyps (Schaltfläche, Link), es sei denn, dies ist für erforderlich.
Unzweideutigkeit.
- Verwenden Sie „Öffnen“ / „Schließen“ für Anwendungen und große Fenster oder Bedienfelder.
- Verwenden Sie „Leave“, um eine Site oder ein Erlebnis zu verlassen (z. B. „Leave Report Builder„).
- Verwenden Sie für die Navigation „Gehe zu“ oder „Navigieren zu“.
- Verwenden Sie „Video abspielen“, nicht „Video ansehen“.
- Verwenden Sie „Anzeigen“, „Anzeigen“ oder „Zu allen wechseln“, nicht „Alle anzeigen“.
- Verwenden Sie „Anmelden“ / „Abmelden“, nicht „Anmelden“ / „Abmelden“.
- Vermeiden Sie „um zu helfen“. Verwenden Sie stattdessen „to“.
- Vermeiden Sie „Utilize“. Verwenden Sie stattdessen „Verwenden“.
- Vermeide vage Adjektive wie „schnell“ oder „einfach“. Genauer gesagt: „Dieser Prozess dauert in der Regel
5 Minuten.“
- Schwache Adverbien vermeiden: sehr, extrem, unglaublich.

### Satz- und Absatzstruktur

- Zielgruppe 20 Wörter oder weniger pro Satz (max. 35). Einen Gedanken pro Satz.
- Absätze: max. 125 Wörter, idealerweise 100 oder weniger. Maximal 4 bis 5 Sätze. Keine Mauern aus Text.
- Aktiv-Formulierungen verwenden. Vermeiden Sie passive Konstruktionen und Nominalisierungen (z. B. „create“ oder „create„)
„Erstellung„).
- Verwenden Sie eine einfache Objekt-Verb-Objekt-Struktur.
- Vermeiden Sie falsche Motive („Es ist…“, „Es gibt…„).
- Verwenden Sie dasselbe Wort konsistent. Keine Synonyme drehen.
- Kein Humor, kein Slang, kein Jargon und keine kulturspezifischen Beispiele (müssen gut lokalisiert werden).
- Verwenden Sie das Komma „Oxford“ in Listen mit drei oder mehr Elementen.
- Schreiben Sie ganze Zahlen von null bis neun aus; verwenden Sie Ziffern für 10 und darüber.
- Keine Semikolons. Stattdessen einen Punkt und einen neuen Satz verwenden.
- Verwenden Sie KEINE AEM-Bindestriche, -Bindestriche oder -Bindestriche in der Prosa. Stattdessen umformulieren. Bindestriche sind
Nur zulässig in zusammengesetzten Adjektiven, die in der Benutzeroberfläche, in Dateinamen und im Code angezeigt werden.
- Verwenden Sie KEINE horizontalen Regeln `---` oder `***`. Sie werden in Experience League nicht unterstützt.

### Scannbarkeit

- Leser sollten den Artikelbereich nur anhand von Titel, Überschriften und Beschriftungen erfassen.
- Max. 2 bis 5 Unterabschnitte pro Abschnitt.
- Target 7 Schritte pro Aufgabe; 10 ist das praktische Maximum. Unterteilen Sie längere Vorgänge in Teilaufgaben.
- Max. 8 Elemente pro Aufzählungsliste.
- Verwenden Sie Tabellen, wenn sie die Überprüfung von Begriffsdefinitionslisten erleichtern.
- Der Inhalt sollte bei einem Lesbarkeitstest unter Stufe 10 bewertet werden (nachdem Eigennamen entfernt wurden).
und Titel).

### Schreiben für KI-Erkennung

- Schlüsselbegriffe (Produktnamen, Funktionsnamen, Aufgaben) in Textkörper- und Link-Text einfügen, nicht nur
in Bildern oder komplexen Tabellen.
- Schreiben Sie klare, in sich abgeschlossene Überschriften und erste Absätze.
- Halten Sie Sätze kurz und direkt.
- Verwenden strukturierter Formate (nummerierte Schritte, kurze Aufzählungszeichen, Überschriften im Definitionsstil) für
Verfahren und Vergleiche.
- Synonyme oder alternative Begriffe bei der ersten Verwendung einschließen (z. B. „ECID (Experience Cloud ID)„).
- Halten Sie die Metadatenfelder (Titel, Beschreibung, Funktions-Tags) vollständig und korrekt.

## &#x200B;2. Lokalisierungs-Tags (immer anwenden)

Maschinelle Übersetzung wird automatisch bei jedem Commit an Main ausgeführt.

### `[!DNL Product Name]`: Nicht lokalisieren

Auf Adobe-Produktnamen anwenden (`[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`,
`[!DNL Experience Platform]`), Namen von Drittanbietern (`[!DNL Mozilla Firefox]`,
`[!DNL Workfront]`), funktionale Namen, die die Übersetzung verwirren könnten (`[!DNL Pass]`,
`[!DNL Campaign]`) und boolesche Operatoren, die als logische Begriffe verwendet werden (`[!DNL AND]`, `[!DNL OR]`).

Wenden Sie sich NICHT bereits an URLs, Dateinamen, Verzeichnisnamen, Codeblöcke, Akronyme oder Begriffe
in der Datenbank Nicht übersetzen.

Entfernen Sie im Link-Text die Tag-Klammern: `[Adobe](https://www.adobe.com)`, nicht
`[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: Benutzeroberflächen-Steuerelemente

Obligatorisch für jedes anklickbare Benutzeroberflächenelement in Verfahrensschritten und für Funktionsnamen,
Navigationselemente, Seitennamen, Optionen, Felder und Registerkarten, wie in der Benutzeroberfläche angezeigt.

- Fett in Schritten und Navigation: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Kursiv kann aus Gründen der Klarheit im konzeptionellen Text (ohne Schritt) verwendet werden.
- In HTML-Tabellen: `<span class="uicontrol">term</span>` anstelle von &grave;&grave; verwenden.
- Im Link-Text: Entfernen Sie die Tag-Klammern.
- Die Groß-/Kleinschreibung muss exakt mit der Schnittstelle übereinstimmen.
- Wenden Sie sich NICHT auf konzeptionell verwendete allgemeine Begriffe („Segment“, „Metrik“, „Kampagne„) an, es sei denn,
Verweis auf das Benutzeroberflächenelement, lange Sätze, Codeblöcke, Akronyme oder Symbolbeschreibungen
(Verwenden Sie den Mauszeiger über dem Symbol bzw. den QuickInfo-Namen, falls verfügbar.)

### `[!DONOTLOCALIZE]`: Gesamte Abschnitte ausschließen

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

Wird nicht in Code-Blöcken benötigt; diese sind standardmäßig nicht lokalisiert.

### Wo Tags verwendet werden können und nicht

- Kann verwendet werden in: Absätzen, Listen, Überschriften, Tabellen, Abzeichen, Alternativtext und Metadaten.
- Kann nicht verwendet werden in: Codeblöcken, Akronymen.
- Wenn ein Metadatenfeld mit einem `[!DNL]`- oder &grave;&grave; beginnt, schließen Sie das gesamte Feld ein
Wert in Anführungszeichen gesetzt oder Validierung schlägt fehl.

## &#x200B;3. Terminologie und Branding

### Produktnamen

Verwenden Sie immer genau diese Formulare. Fügen Sie &quot;Adobe&quot; bei der ersten Referenz in ein Handbuch ein. NICHT vorausgehen
Produktnamen mit „The“, es sei denn, der offizielle Name enthält sie.

| Korrekt | NIE verwenden |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (sekundäre Referenz) | Plattform (allein, sofern der Kontext nicht eindeutig ist) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (sekundär) | Real-Time CDP (Kleinbuchstaben „t„) |
| Adobe Real-Time Customer Data Platform | — |
| Echtzeit-Kundenprofil | Echtzeit-Kundenprofil, Einheitliches Profil |
| Adobe Journey Optimizer | AJO |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (sekundär) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Adobe Real-Time CDP-Verbindungen | RTCDP Connections, AEP Connections, Connections (allein) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Tags (Produktname) | Launch (veraltet) |
| Entscheidungs-Management | Offer Decisioning (nur Klammern: „ehemals Offer Decisioning„) |
| Datenstrom (ein Wort, Kleinbuchstaben) | Daten-Streaming, Edge-Konfiguration |
| Analysis Workspace | Analysis Workspace, Workspace, Workspace |
| Adobe AI | Sensei (veraltet) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

- „Echtzeit“ verwendet immer Kapital-R und Kapital-T, wenn Teil eines Produktnamens ist.
- „Editionen“ werden im Allgemeinen in Kleinbuchstaben geschrieben. „Edition“ wird als Teil einer Produktausgabe großgeschrieben
Name (z. B. &quot;Adobe Real-Time CDP B2C Edition„).
- Abkürzen Sie KEINE Produktnamen in der Dokumentation für Benutzende (keine AEP, CJA, AJO, RTCDP).
Eingeschränkte Ausnahmen: Akronyme können bei der ersten Verwendung für SEO oder im Inhaltsverzeichnis in Klammern stehen
Einträge, Beschreibungsmetadaten und Überschriften, bei denen die Länge ein Problem darstellt.
- Analytics: Groß-/Kleinschreibung der Bereichsnamen (leer, Attribution, Experimentieren,
Freiform; Ausnahme: &quot;Journey Canvas„). Namen der Visualisierungen werden in Kleinbuchstaben geschrieben (Balken, Ringdiagramme,
Histogramm, Linie, Baumdiagramm, Text).

### Funktionale und konzeptionelle Terminologie

| Korrekt | NICHT verwenden |
|---|---|
| Ereignisweiterleitung | Server-seitige Weiterleitung, Server-seitig starten |
| Zulassungsliste | Whitelist |
| Blockierungsliste/Blockierungsliste | auf die schwarze Liste setzen |
| primär/replikat ODER primär/sekundär (Server) | Master/Slave |
| main (GitHub-Verzweigung) | Vorlage |
| ethischer Hacker | White Hat Hacker |
| Remarketing | Retargeting |
| Feldgruppe | mixin (veraltet), Erweiterungen, Mixins |
| Automatischer Ablauf von Daten | TTL, Time-to-Live, Ablauf |
| Nicht-Produktions-Sandbox | Staging (als Umgebungsname) |
| Segmentdefinition | Segment (allein, wenn die Definition gemeint ist) |
| ID (immer großschreiben) | ID |
| Aufnahme/Aufnahme/Aufnahme | Onboarding (für das Hinzufügen von Daten zu Platform) |
| Datensatz/Datensätze | Datendatei, Datensatzdateien |
| Zugriffskontrolle | Berechtigungen (für die Platform-Funktion) |
| Widget | Metrikkarte (veraltet) |
| Platzhaltervariable | Platzhaltervariable |
| nicht verfügbar/gesperrt/ausgeschaltet/deaktiviert | ausgegraut |
| Kohärenzprüfung | Plausibilitätsprüfung |
| Integriert | Nativ (als Synonym für „Built-in„) |
| Hohe Priorität | Mostnagel |
| Veraltet | Besitzstandsklausel |
| Primär/Main/Source | Primär (als Deskriptor) |

### Schreibgeschützte Begriffe: NIE in öffentlich zugänglichen Dokumenten verwenden

| Interner Begriff | Stattdessen verwenden |
|---|---|
| AEP | Adobe Experience Platform |
| HANDFLÄCHE | Sandbox-Verwaltung/Zugriffskontrolle |
| BIOME | Umgebung |
| Hydrat/Hydratation | Erstellen/Auffüllen |
| Einheitliches Profil | Echtzeit-Kundenprofil |
| Staging (Umgebung) | Nicht-Produktions-Sandbox |
| DTM | Tags |
| Mandant | IMS-Organisation/Organisation |
| CRUD | Erstellen, Lesen, Aktualisieren und Löschen (buchstabieren) |
| Siphon, BSO, Ethos | Interne Codenamen, nie extern |
| Hopfen | Interner DSGVO-/Zugriffskontrollbegriff |
| Geschwindigkeit | Nicht nutzerorientierter Werbebegriff |
| Pipeline | Interner Adobe-Infrastrukturbegriff |

## &#x200B;4. Inklusive Sprache und Zugänglichkeit

### Inklusive Sprachgrundsätze

- Verwenden Sie geschlechtsneutrale Begriffe: „Vertriebsmitarbeiter“ nicht „Verkäufer“, „Moderator“ nicht „Vorsitzender“.
- Bevorzuge die zweite Person („du„), um Geschlechtspronomen zu vermeiden.
- Verwenden Sie „sie“ im Singular für eine Person, deren Geschlecht unbekannt ist. Benutzen Sie sie NICHT oder verwenden Sie sie NICHT.
- Namen von nicht-weißen Kulturen in Beispiele aufnehmen (z. B. Ayesha, Ibrahim, Vignesh, Quynh).
Verwenden Sie NICHT nur kulturell weiße Namen.
- Geschlecht (männlich/weiblich) NICHT mit Geschlecht (Mann/Frau) vermengen.
- Kapitalisieren von Nationalitäten, Völkern, Rassen (außer „weiß“ gemäß AP Stylebook) und Stämmen.
- Verwenden Sie die Sprache des Menschen als Erstes: „Menschen, die Hilfstechnologien nutzen“, nicht „die Behinderten“.
- Vermeide Euphemismen wie „anders aktiviert“. Vermeiden Sie Deskriptoren, die als Substantive verwendet werden: „The Blind,“
„Die Tauben.“
- Begriffe vermeiden, die die Identität/kulturelle Aneignung widerspiegeln: Geisttier, Sherpa, Pow wow,
Guru, Ninja, Stamm.

### Nicht-inklusive Terminologie zur Vermeidung von

| Verwenden von | Nicht |
|---|---|
| Zulassungsliste//Blockierungsliste | Whitelist/Blacklist |
| primär / replikat ODER primär / sekundär | Master/Slave |
| Main (Git-Verzweigung) | Vorlage |
| Hohe Priorität | Mostnagel |
| Platzhaltervariable | Platzhaltervariable |
| nicht verfügbar/gesperrt/ausgeschaltet/deaktiviert | ausgegraut |
| Kohärenzprüfung | Plausibilitätsprüfung |
| Integriert | Nativ (als Synonym) |
| Behörde/Experte | Guru / Ninja |
| Mitglieder Ihrer Gruppe | Angehörige eures Stammes |
| Besprechung | Pow wow / Kreis der Wagen |
| Vorbild / Verwandter Geist | Spirituose |
| Handbuch | Sherpa |
| Veraltet | Besitzstandsklausel |
| vergebliches Unterfangen | Todesmarsch |
| Lächerlich/inkompetent/unvorhersehbar | dumm / lahm / verrückt |
| Ethischer/unethischer Hacker | White Hat / Black Hat Hacker |
| Video abspielen | Video ansehen |
| Anzeigen/Anzeigen/Zu allen wechseln | Alle anzeigen |

### Barrierefreiheit: Beschreibung der Benutzeroberfläche

Beschreiben Sie Benutzeroberflächenelemente NICHT nach Farbe oder Bildschirmposition. Verwendung chronologischer, nicht räumlicher,
Sprache:

| Verwenden von | Nicht |
|---|---|
| Erst, dann, schließlich | Oben, unten |
| In der Menüleiste | Links |
| Vor/Nach | Oben/unten auf dem Bildschirm |

Beschreiben Sie, was Steuerelemente tun, und nicht, wie sie aussehen:

| Verwenden von | Nicht |
|---|---|
| Suche auswählen | Klicken Sie auf die Lupe |
| Bearbeiten | Das Stiftsymbol |
| Ein/Aus | Umschalten/Umschalten/Aktivieren |
| Menü | Seitenlade |
| E-Mail eingeben | E-Mail-Adresse eingeben |
| Speichern | Die Schaltfläche „Speichern“ |
| Abbrechen | Schließen |

Verwenden Sie KEINE Farbe allein, um Informationen zu vermitteln. Paaren Sie Farbe immer mit Text oder Form.

### Barrierefreiheit: Alternativtext, Links und Videos

- **ALT-Text**: Beschreiben Sie, was das Bild zeigt, nicht nur den Namen des Bildschirms. Vollständig verwenden
Sätze, volle Wörter (Bildschirmlesehilfen buchstabieren Abkürzungen) und relevante Texte
Aus dem Bild. Bilder, die unabhängig vom umgebenden Text Informationen vermitteln, MÜSSEN
Alt-Text.
- **Links**: Verwenden Sie niemals „hier klicken“ oder „Link“ als Link-Text. Löschen des Ziels aus
Der Link-Text allein.
- **Videos**: darf NICHT automatisch abgespielt werden. Geben Sie immer eine Textalternative, ein Transkript oder einen Link an
Schriftliche Anweisungen. Aussagekräftige Beschriftungen einschließen.

## &#x200B;5. Markdown-Syntax Grundlagen

### Frontmatter (für jede Datei erforderlich)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

- Fügen Sie beim Erstellen einer neuen Seite KEINE `exl-id` hinzu. Sie wird bei der Veröffentlichung automatisch generiert
Zeit. Bewahren Sie nur `exl-id` Felder auf, die bereits auf vorhandenen Seiten vorhanden sind.
- Titel: Title Case, max. 60 Zeichen, kein Pipe- oder Produktname (wird automatisch hinzugefügt).
Konzepttitel sind Substantivsätze; Aufgabentitel sind Verbsätze.
- Beschreibung: Urteilsfall, 150 bis 160 Zeichen. Der erste Satz fasst zusammen, der zweite ist ein
call to action. Beginnen Sie NICHT mit dem Produktnamen oder kopieren Sie den ersten Absatz wörtlich.

### Überschriften

- `#` = H1 (eine pro Seite, erste Zeile nach frontmatter). `##`, `###` für Unterabschnitte. Nie
Ebenen überspringen.
- Targeting von 5 Wörtern oder weniger, max. 69 Zeichen. Leerzeile vor und nach jeder Überschrift.
- Auf jede Überschrift muss ein Textkörper folgen. Überschriften dürfen nicht gestapelt oder eine Liste/Tabelle/Anmerkung platziert werden
direkt unter einer Überschrift.
- Urteilsfall. Konzeptüberschriften sind Substantivsätze; Aufgabenüberschriften sind Verben von zwingender Bedeutung
(Gerundien vermeiden).
- Keine abstrakten Überschriften aus einem Wort („Übersicht“, „Einführung„) ohne Beschreibung des Themas.
- Benutzerdefinierte Anker-IDs: `## Section title {#section-id}` (Kleinbuchstaben, mit Bindestrich).

### Links, Bilder und Code

- Interne Querverweise verwenden Stamm-relative Pfade: `[text](/help/path/to/file.md)`.
Externe Links verwenden absolute `https://` URLs.
- Verwenden Sie niemals „hier klicken“ oder „Link“ als Link-Text. Vermeiden Sie rohe URLs im Textkörper.
- Alternativtext: `![alt text](path/to/image.png)`. Vollständige Sätze, keine führende „Dieses Bild zeigt…“.
- Screenshots: Nur leichtes Design, keine Kundendaten, keine Benutzeroberfläche von Drittanbietern, keine Bilder von Code.
- Umgrenzte Code-Blöcke verwenden drei Backticks mit einer Sprachkennung. Code-Blöcke werden nicht
lokalisiert (kein DNL/UICONTROL in ihnen erforderlich).
- Videos: `>[!VIDEO](url?quality=12&learn=on)`. Nie automatisch abspielen; immer ein Transkript bereitstellen
Oder eine schriftliche Alternative.

### Ermahnungen

```markdown
>[!NOTE]
>
>Note content here.
```

Eine leere `>` muss den Slogan vom Inhalt trennen; jede Fortsetzungszeile beginnt
Mit `>`. Platzieren Sie eine `[!NOTE]` NICHT unmittelbar nach einem `[!CONTEXTUALHELP]`.

### Popovers für kontextuelle Hilfe (`[!CONTEXTUALHELP]`)

`[!CONTEXTUALHELP]` Blöcke liefern Pop-up-QuickInfos, mit denen Drähte in das Erlebnis eingefügt werden können
Platform-Benutzeroberfläche. Sie sind in den Dokumenten vorhanden, werden jedoch über einen JSON-Feed als produktinterne Popovers gerendert.
Wird zum Zeitpunkt der Erstellung generiert.

```markdown
## Configure file names {#configure-file-names}

>[!CONTEXTUALHELP]
>id="platform_destinations_activate_filename"
>title="Configure file name"
>abstract="For file-based destinations, a unique file name is generated per segment. Use the file name editor to create and edit a unique file name or keep the default name."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations.html#file-names" text="Learn more in documentation"
```

Erforderliche Felder: `id`, `title`, `abstract`. Alles andere ist optional.

**Platzierung:**
- Der Block muss direkt nach einer Überschrift (`#`, `##` oder `###`) mit einem expliziten
Anker-ID (z. B. `### Section title {#section-id}`). Kein Absatz oder anderer Inhalt zwischen
Die Überschrift und der Block oder das Popover werden nicht gerendert.
- Mehrere `[!CONTEXTUALHELP]` können nacheinander im selben Abschnitt angezeigt werden (z. B.
ein pro Feld (wird dokumentiert).
- Platzieren Sie einen `[!NOTE]` NICHT unmittelbar nach einem `[!CONTEXTUALHELP]`. Es bricht
Rendering in Experience League (bekannte Plattformbegrenzung).

**ID-Syntax:**
- Format: `id="platform_<yourarea>_<workflow>_<uiitem>"`, z. B.
  `id="platform_destinations_activate_deduplicationkey"`.
- IDs können Großbuchstaben enthalten.
- IDs müssen im gesamten Dokumentsatz eindeutig sein (zur Erstellungszeit überprüft). Dieselbe ID kann wiederverwendet werden
durch Engineering über mehrere Benutzeroberflächenspeicherorte hinweg, wodurch identische Pop-up-Inhalte in erstellt werden
Jeder Spot. Das wird erwartet.

**Links in einem Popover, verwenden Sie `additional-url`, nicht inline HTML:**
- Verwenden Sie zum Hinzufügen eines Links eine separate Zeile: `>additional-url="URL" text="Link text"`. Nicht einbetten
  `<a href="...">` oder Markdown `[text](url)` zu diesem Zweck innerhalb der `abstract`.
- Der `additional-url` MUSS `.html` im Pfad enthalten, da der Link sonst nicht in angezeigt wird.
die Benutzeroberfläche (z. B. `https://experienceleague.adobe.com/docs/experience-platform/path/to/page.html#anchor`,
nicht das neuere `/en/docs/...` erweiterungslose Formular, das in Textkörper-Links an anderer Stelle verwendet wird).
- Maximal zwei `additional-url` Zeilen pro Block.
- Ein erster Link wird während des Jenkins-Builds automatisch aus der Abschnittsüberschrift generiert. Sie
Fügen Sie diese nicht manuell hinzu, und Sie können sie auch nicht umbenennen.

**Andere unterstützte Syntax:**
- Das `abstract` Feld unterstützt grundlegende HTML/Markdown-Funktionen für Hervorhebung und Struktur: `<b>`,
  `<br>`, `<ul><li>`, `**bold**`.
- Video-Links werden über denselben `additional-url`/`text`-Mechanismus unterstützt, der auf einen verweist.
Direct Video URL oder YouTube URL.

**Workflow-Hinweis:** bei der Übergabe einer neuen Popover-ID an die Benutzeroberfläche/das Engineering-Team (in der Regel über eine
Jira-Ticket), geben Sie auch eine Fallback-URL an (bevorzugen Sie eine goURL, wenn eine für diese Seite vorhanden ist) und
den Standort der Benutzeroberfläche. Dieser Fallback ist von den in den Dokumenten verwendeten `additional-url` getrennt
Markdown.

### Listen und Tabellen

- Verwenden Sie `*` oder `-` konsistent in einem Artikel. Nicht mischen.
- Nummerierte Listen verwenden `1.` für jedes Element. Einzelschritte verwenden einen Aufzählungszeichen, nicht `1.`.
- Keine Kontrollkästchen für Aufgabenlisten im GitHub-Stil (`- [ ]`); in Experience League nicht unterstützt.
- Listen und Tabellen mit leeren Zeilen umgeben. Listenelemente grammatisch parallel halten.

### Benennung von Dateien und Ordnern

- Markdown-Dateinamen: Kleinbuchstaben mit Bindestrichen, keine Groß-/Unterstriche/Punkte/Leerzeichen.
- Verwenden Sie beschreibende Slugs (`create-calculated-metric.md`), keine bloßen Namen wie `overview.md`.
- Bilder werden in einen `assets/` Unterordner verschoben. Bilder, die nicht lokalisiert werden müssen, werden übernommen
  `do-not-localize/`.

## &#x200B;6. Struktur und Konventionen für Inhaltsverzeichnisse

- Drei Inhaltstypen, getrennt gehalten: **Konzept** (Was/Warum, Substantivüberschriften), **Aufgabe**
(wie, Imperative Überschriften, immer mit vorangestelltem Konzept), **Referenz** (Felder,
Parameter, Tabellen).
- Schritte: Jeder ist ein einzelner vollständiger Satz, der mit einem Verb oder dem Ziel beginnt. Ziel 7
Schritte pro Aufgabe, max. 10; Unterteilen längerer Vorgänge in Teilaufgaben.
- TOC.md: Einträge in Großbuchstaben, gültige Anker-IDs für jede Abschnittsüberschrift, kein Duplikat
Dateieinträge, keine Kommentare aus der Mid-List.
- Ausblenden einer Seite für die Navigation mit `{hide-from-toc}` in `TOC.md` (nicht in der Schriftart). Ausblenden
von Suchmaschinen mit `hide: true` in frontmatter.
- Zweigname: kein Präfix für Benutzernamen. Verwenden Sie die Jira-Ticketnummer und einen Slug mit Großschreibung des Titels
(e.g., `PLAT-12345-Update-Guardrail-Limits`). Benennen Sie die Verzweigung und den PR-Titel gleich.

## &#x200B;7. Rechtschreibung und Interpunktion

- Amerikanisch Englisch Rechtschreibung: Farbe, erkennen, Lizenz, während, Gültigkeit, Meter, unter
(Nicht farbig, erkennen, lizenzieren, während, Ablauf, Meter, unter).
- Anführungszeichen für Anführungszeichen für Personen reservieren; UI-Zeichenfolgen nicht zitieren (fett + verwenden)
  &grave;&grave;).
- Begriffe, die als Begriffe verwendet werden (*profile*, nicht „profile„) kursiv formatieren. Backticks für Code verwenden,
Parameter, Dateinamen und eingegebenen Text.
- Fett nur für Benutzeroberflächenelemente in Prozeduren (mit &grave;&grave;) und Schlüsselbegriffen am Anfang
Einführung.
- Keine Semikolons, keine Aem/en-Bindestriche/Bindestriche in der Prosa, keine horizontalen Regeln (siehe Abschnitt 1).

## &#x200B;8. Checkliste überprüfen

Bevor Sie eine Bearbeitung abschließen, überprüfen Sie:

- Benutzerfokussierte Stimme, aktive Stimme, zweite Person, kein „Ermöglicht“/„ermöglicht es Ihnen,“
- Sätze ≤20 Worte, Absätze ≤125 Worte
- Überschriften: Groß-/Kleinschreibung des Satzes, ≤5 Wörter/69 Zeichen, gefolgt von Textkörper, keine übersprungenen Ebenen
- Korrekte Produktnamen und Formulare; keine veralteten, schreibgeschützten oder nicht-integrativen Begriffe
- &grave;&grave; für jedes Benutzeroberflächenelement in Schritten; `[!DNL]` für jeden Produkt-/Drittanbieternamen
- Keine Tags in Code-Blöcken; gekennzeichnete Metadatenfelder werden in Anführungszeichen eingeschlossen
- Korrekte Ermahnungssyntax, konsistente Listenmarkierungen, keine Aufgabenlisten, keine horizontalen Regeln
- Alternativtext ist beschreibend und vollständig; kein „hier klicken“; keine räumliche/gerichtete Sprache
- Keine Farbe allein verwendet, um Informationen zu vermitteln; Videos werden nicht automatisch abgespielt
- Erforderliche Schriftart vorhanden; stammbezogene interne Links; Dateinamen mit Bindestrichen in Kleinbuchstaben
