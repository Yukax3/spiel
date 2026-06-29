# Wurzelwerk — Game Design Dokument (v0.1)

> **Genre:** Friedliches 2D-Aufbau- & Logistikspiel
> **Inspiration:** *Die Siedler* (Nintendo DS) für Logistik & Siedler-Wuseln, *Anno* für Produktionsketten & Bevölkerungsstufen
> **Kern-Twist:** Symbiose mit einer lebenden Welt — **kein Krieg, keine Feinde**. Die einzige „Gegnerin" ist das ökologische Gleichgewicht.
> **Plattform-Idee:** PC/Web (2D, Top-Down), Steuerung bewusst DS-/Touch-freundlich

---

## 1. Vision in einem Satz

Du gründest keine Kolonie *gegen* die Natur, sondern *mit* ihr: Ein verschlungenes Netz aus Pfaden, Trägern und Produktionsketten wächst wie ein Wurzelwerk durch eine lebende Welt — und gedeiht nur, solange du ihr genauso viel zurückgibst, wie du nimmst.

## 2. Der Pitch (Elevator)

In *Wurzelwerk* baust du eine kleine Kolonie in einem riesigen, lebendigen Hain. Jeder Siedler ist ein echtes Wesen, das Güter Schritt für Schritt über dein Wegenetz trägt — genau wie in *Die Siedler*. Aber jedes Stück Holz, jede Frucht, jeder Stein wird der Welt **entnommen**. Die Welt hat eine **Vitalität**. Nimmst du zu viel, welkt das Biom: Erträge sinken, Tiere wandern ab, Böden verdorren. Gibst du zurück (Aufforsten, Kompostieren, Tiere ansiedeln, Brachen ruhen lassen), blüht die Welt auf und schenkt dir **neue, bessere Ressourcen**, die in toter Erde nie entstünden.

Es gibt nichts zu erobern. Der Reiz ist: eine immer komplexere, schöne, *gesunde* Wirtschaft zu weben, ohne den Ast abzusägen, auf dem alles wächst.

## 3. Designsäulen

1. **Sichtbare Wirtschaft (Siedler-DNA).** Keine abstrakte Logistik. Jedes Gut wird von einem sichtbaren Träger über Pfade getragen. Engpässe sieht man als Stau.
2. **Lebende, reaktive Welt (Symbiose-Kern).** Die Karte ist kein statisches Brett. Biome haben Gesundheit, gedeihen oder welken sichtbar und verändern, was möglich ist.
3. **Frieden als Haltung.** Spannung entsteht durch Knappheit, Timing und Balance — niemals durch Gewalt. Kein Militär, keine Gegner, kein „Game Over durch Angriff".
4. **Verschachtelte Ketten (Anno-DNA).** Tiefe durch Produktionsketten & Bevölkerungsstufen, nicht durch Kampf.
5. **Lesbarkeit vor Realismus.** Klare 2D-Top-Down-Optik, alles auf einen Blick verständlich (DS-tauglich).

---

## 4. Kern-System: Die lebende Welt (Symbiose)

### 4.1 Vitalität (das zentrale Maß)
Die Karte ist in **Hexfelder** unterteilt (organischer für Natur & Biome), gruppiert zu **Biom-Zonen** (Hain, Aue, Felsgrund, Sumpf, Lichtung …). Jede Zone hat einen Wert **Vitalität 0–100**.

- **Entnahme senkt Vitalität.** Bäume fällen, Erz schürfen, Felder ernten, Tiere jagen.
- **Pflege hebt Vitalität.** Aufforsten, Kompost ausbringen, Brache, Bienen/Bestäuber, Teiche anlegen, Tiere ansiedeln.
- **Natürliche Regeneration.** Jede Zone erholt sich langsam von selbst — je höher die Vitalität, desto schneller (gesunde Böden heilen besser). Die Regenerationsrate wird zusätzlich von der **Jahreszeit** moduliert (Frühling/Sommer schnell, Winter stark gebremst — siehe Kap. 6).

### 4.2 Was Vitalität bewirkt (das Feedback)
| Vitalität | Zustand | Folgen |
|-----------|---------|--------|
| 80–100 | **Blühend** | Höchste Erträge, seltene Ressourcen erscheinen, Tiere siedeln sich an, Bonus-Wachstum |
| 50–79 | **Gesund** | Normale Erträge, stabile Regeneration |
| 25–49 | **Erschöpft** | Erträge −40 %, langsamere Nachwuchsraten, erste Verödung sichtbar |
| 0–24 | **Verödet** | Kaum Erträge, Tiere fliehen, Boden kippt ins nächsttiefere Biom (Hain → Heide → Ödland) |

**Wichtig (kein Krieg-Ersatz durch Frust):** Verödung ist **immer umkehrbar**. Es gibt kein Fail-State, nur Rückschritt. Ödland kann über viele Spielstunden zurück zum Hain gepflegt werden — das ist sogar ein eigenes Spätspiel-Ziel.

### 4.3 Symbiose-Boni (der Belohnungsmotor)
Gesunde Welt schenkt dir Dinge, die du nicht „bauen" kannst:
- **Blühend → Sonderressourcen:** Heilkräuter, Edelharz, Wildhonig, Singvogel-Federn, Tiefenpilze.
- **Tier-Symbiosen:** Bestäuber (+Ertrag Felder), Biber (bauen dir Teiche/Stauwerke gratis), Maulwürfe (legen Erzadern frei), Vögel (verbreiten Saatgut → kostenlose Aufforstung).
- **Lebende Infrastruktur:** Brücken aus verwachsenen Wurzeln, Pilznetz-Lager (verlustfreie Lagerung), die nur in blühenden Zonen wachsen.

### 4.4 Raubbau-Balance (bewusste Versuchung)
Raubbau ist eine **echte, reizvolle Option** — nicht nur eine Falle.

- **Kurzfristig spürbar schneller.** Wer eine Zone leerräumt, bekommt sofort einen Mengen-/Tempo-Schub (Design-Zielwert: ~2× Output über die ersten Spielminuten einer Zone gegenüber dem nachhaltigen Pfad). Das soll sich gut anfühlen.
- **Legitimer Krisen-Notnagel.** In Engpässen (z. B. harter Winter, eingebrochene Nahrungskette) ist es richtig und erlaubt, kurz eine Zone anzuzapfen, um die Kolonie über die Runden zu bringen.
- **Langfristig klar unterlegen.** Verödete Zonen liefern kaum noch etwas, kippen ins nächsttiefere Biom und schneiden dich von den **Symbiose-Sonderwaren** (Kap. 4.3) ab — die der einzige Weg zu den höheren Bevölkerungsstufen sind. Wer dauerhaft raubbaut, deckelt sich selbst.
- **Korrektur statt Strafe.** Es gibt kein Strafsystem und kein Fail-State — nur die Welt, die auf dein Handeln reagiert. Jede Verödung ist umkehrbar (Kap. 4.2).

> **Designkern:** Du wirst nie *gezwungen*, nachhaltig zu sein. Raubbau ist der schnelle, verführerische Sprint und der Rettungsanker in Not — Nachhaltigkeit ist der überlegene Marathon. Die Spannung lebt von dieser Wahl.

---

## 5. Kern-System: Siedler & Logistik (Die-Siedler-DNA)

### 5.1 Träger statt Trucks
- Güter werden **nicht** abstrakt teleportiert. Jeder Transport ist ein **sichtbarer Siedler**, der ein Gut von A nach B trägt.
- **Pfadnetz mit Knoten (Flaggen).** Wege verlaufen über die **Hex-Nachbarschaft**: Flaggen sitzen auf Hex-Ecken/Feldern, Wegsegmente folgen den 6 Nachbarrichtungen. Zwischen zwei Flaggen pendelt jeweils ein Träger und reicht Güter weiter (Eimerkette). Das macht Engpässe sichtbar und planbar. (Die 6er-Nachbarschaft gibt natürlichere, weniger schachbrettartige Netze als ein Quadratraster.)
- **Stau = Feedback.** Türmt sich Ware an einer Flagge, brauchst du mehr Träger, einen kürzeren Weg oder eine Esels-/Karren-Strecke.

### 5.2 Wege-Tiers
1. **Trampelpfad** — gratis, langsam, trampelt aber Vitalität nieder, wenn stark genutzt.
2. **Befestigter Weg** — schneller, neutral für die Natur.
3. **Lebende Wurzelstraße** — nur in gesunden Zonen baubar, am schnellsten, **hebt** sogar leicht die Vitalität (wächst mit dem Hain).
4. **Wasserwege** — Flöße/Kähne auf Flüssen & Biber-Teichen, hoher Durchsatz für Massengüter.

### 5.3 Bevölkerung
- Siedler wohnen in **Wohnstätten** und übernehmen automatisch freie Jobs (Siedler-typisch: kein Mikromanagement einzelner Personen).
- Bedürfnisse je Stufe (Anno-typisch) steuern Zufriedenheit & Zuzug.

---

## 6. Jahreszeiten & Zeit

Ein Spieljahr hat **vier Jahreszeiten**, die als **milder Rhythmus** wirken — sie verändern Erträge & Regeneration spürbar, **blockieren aber nichts hart**. Vorratsdenken wird belohnt, nicht erzwungen.

| Jahreszeit | Ertrag (Felder/Sammeln) | Regeneration | Stimmung |
|------------|-------------------------|--------------|----------|
| **Frühling** | +20 % (Saat/Blüte) | hoch | Aufbruch, Bestäuber aktiv |
| **Sommer** | normal/hoch | hoch | Hauptproduktionszeit |
| **Herbst** | +10 % Ernte, dann Abklingen | mittel | Vorräte anlegen |
| **Winter** | Felder ruhen (−70 %), Wald/Stein normal | stark gebremst | Zehrungsphase |

**Designprinzip:**
- Kein hartes Sperren — Felder *ruhen* im Winter (stark reduziert), produzieren aber nicht null; Holz-, Stein-, Erzgewinnung läuft ganzjährig weiter.
- **Winter erzeugt Rhythmus statt Frust:** Wer im Herbst Brot/Vorräte eingelagert hat, kommt entspannt durch. Wer nicht, gerät in einen Engpass — genau die Situation, in der **Raubbau zum legitimen Notnagel** wird (Kap. 4.4).
- **Jahreszeit × Vitalität:** Eine blühende Zone übersteht den Winter besser (Restregeneration), eine erschöpfte fällt schneller. Das koppelt Zeit und Symbiose.
- Optional/Settings: Jahreszeitenlänge & -härte einstellbar für Cozy- vs. Planungs-Spieler.

## 7. Bevölkerungs-/Kolonie-Stufen

| Stufe | Name | Schaltet frei | Hauptbedürfnisse |
|-------|------|---------------|------------------|
| 1 | **Sammler** | Holz, Beeren, Wasser, einfache Hütten | Nahrung, Wasser, Wärme |
| 2 | **Pflanzer** | Felder, Mühle, Brot, Lehm, Werkstätten | + Brot, Kleidung, ein Treffpunkt |
| 3 | **Handwerker** | Erz, Schmelze, Werkzeug, Keramik, Imkerei | + Werkzeug, Töpferware, Honig |
| 4 | **Hüter** | Heilkräuter, Papier/Schule, lebende Infrastruktur, Sonderwaren | + Bildung, Heilmittel, Kultur |
| 5 | **Hainmeister** (Endspiel) | Symbiose-Großbauten, Renaturierung von Ödland | + Festtage, seltene Symbiose-Luxusgüter |

Aufstieg einer Wohnstätte braucht erfüllte Bedürfnisse **und** eine Mindest-Vitalität der Umgebung → Wachstum und Naturpflege sind systemisch gekoppelt.

---

## 8. Produktionsketten (Beispiele)

**Brot (Grundkette)**
Feld (Korn) → Mühle (Mehl) → Backhaus (Brot) → Wohnstätte

**Werkzeug (verzweigt)**
Köhlerei (Holz→Kohle) + Erzgrube (Erz) → Schmelze (Barren) → Schmiede (Werkzeug)
*Werkzeug ist für höhere Gebäude nötig → klassischer Anno-Gate.*

**Symbiose-Kette (Belohnungspfad)**
Blühende Zone → Imkerei (Wildhonig) + Kräutergarten (Heilkräuter) → Sudhaus (Heiltrank) → Hüter-Wohnstätten
*Diese Kette existiert nur, wenn du die Welt gesund hältst.*

**Renaturierung (Pflege als „Produktion")**
Kompostwerk (Bioabfall → Humus) → Förster/Saatgut → ausgebrachter Humus + Saat **hebt Vitalität** einer Zone
*Pflege läuft über dieselbe Logistik wie Güter — Humus ist eine „Ware", die Träger zur Zone bringen.*

---

## 9. Gebäude (Auswahl)

**Gewinnung:** Holzfäller, Förster (pflanzt nach!), Beerensammler, Brunnen, Lehmgrube, Steinbruch, Erzgrube, Fischerhütte
**Verarbeitung:** Mühle, Backhaus, Weberei, Köhlerei, Schmelze, Schmiede, Töpferei, Sudhaus
**Natur/Symbiose:** Kompostwerk, Imkerei, Kräutergarten, Teichbau, Wildgehege (ansiedeln, nicht jagen), Hain-Schrein (Renatur-Boost im Umkreis)
**Bevölkerung/Sozial:** Wohnstätten (4 Stufen), Marktplatz (Verteilzentrum), Schule, Festplatz, Heilstube
**Logistik:** Flagge, Lager, Eselstation, Anleger/Floßbau, Pilznetz-Lager (lebend)

---

## 10. Spiel-Loop

**Frühphase (Sammler/Pflanzer):** Erste Hütten, Holz & Nahrung, Wegenetz spannen, erstes Gefühl für Entnahme vs. Regeneration.

**Mittelphase (Handwerker):** Werkzeugkette, Erzabbau — der erste echte Vitalitäts-Druck. Du musst aktiv pflegen (Förster, Kompost), sonst veröden deine Erzregionen drumherum. Logistik wird komplex (Flaggen-Staus, Eselsrouten).

**Spätphase (Hüter/Hainmeister):** Symbiose-Ökonomie. Du orchestrierst blühende Zonen für Sonderwaren, baust lebende Infrastruktur, und nimmst dir das große Projekt vor: **ein totes Ödland-Areal über die Zeit zurück zum blühenden Hain pflegen.**

## 11. Ziele & Endgame (reine Sandbox)

Das Spiel ist eine **offene Sandbox** — keine Kampagne, keine Story-Missionen, keine Eroberung. Stattdessen setzt du dir selbst **wählbare Bestrebungen** (optionale Langzeitziele, die du an-/abschalten kannst), die Fortschritt und Stolz geben, ohne Druck zu erzeugen:

- **Der große Hain:** Bring X Zonen gleichzeitig auf „Blühend".
- **Renaturierer:** Verwandle ein Ödland-Gebiet zurück in Hain.
- **Die wuselnde Stadt:** Erreiche eine große, voll versorgte Hüter-/Hainmeister-Bevölkerung.
- **Symbiose-Meisterin:** Habe alle Tier-Symbiosen gleichzeitig aktiv.
- **Vier Jahreszeiten lang autark:** Übersteh ein volles Jahr ohne Raubbau und ohne Nahrungs-Engpass.
- **Freier Modus:** Kein Ziel, nur bauen & gärtnern.

Bestrebungen sind reine Selbstverpflichtungen mit Belohnung (Statistik/Abzeichen, evtl. kosmetische Freischaltungen) — nie ein Fail-State. Der Reiz ist die eigene, immer schönere und gesündere Wirtschaft.

---

## 12. Steuerung & UI (DS-/Touch-tauglich)

- **Top-Down 2D**, weiche, lesbare Illustrations-Optik; Vitalität farblich über einen umschaltbaren **„Lebens-Layer"** (sattes Grün → fahles Braun).
- Bauen per Klick/Tap aus einer Radial- oder Leistenpalette.
- Wege ziehen per Drag (Flagge-zu-Flagge).
- **Ein-Blick-Diagnose:** Heatmap-Layer für Vitalität, Warenfluss, Stau, Zufriedenheit.
- Bewusst **wenig Mikromanagement**: Siedler suchen sich Jobs selbst, Pflege ist als reguläre Kette automatisierbar.

## 13. Look & Feel / Ton

Ruhig, warm, kontemplativ — ein „Cozy-Aufbauspiel" mit Tiefe. Tag/Nacht & Jahreszeiten als Stimmung (und milder Ertragsmodifikator). Sound: Vogelgezwitscher in blühenden, Wind in verödeten Zonen — die Welt klingt nach ihrer Gesundheit.

---

## 14. Technik-Vorschlag (für späteren Prototyp)

- **Web/2D:** TypeScript + Canvas oder ein leichtes Engine-Setup (PixiJS für Performance beim Wuseln, oder Phaser für Schnellstart).
- **Datengetrieben:** Gebäude, Ketten, Biome als JSON/Config → leicht balancierbar.
- **Simulationskern getrennt von Rendering** (Tick-basiert): Vitalität, Warenfluss und Träger-Pathfinding laufen im Modell, das Rendering zeichnet nur den Zustand.
- **Prototyp-Scope (MVP):**
  1. **Hex-Karte** mit 2 Biomen + Vitalitätswert pro Zone (Hex-Grid + Achsen-Koordinaten, z. B. axial q/r)
  2. 3 Gebäude (Holzfäller, Förster, Wohnstätte) + 1 Kette
  3. Flaggen-Wege über Hex-Nachbarschaft + sichtbare Träger
  4. Vitalität sinkt bei Entnahme, steigt durch Förster → sichtbarer Lebens-Layer
  Das allein beweist schon den Kern-Loop „nehmen vs. zurückgeben".

---

## 15. Decisions-Log (getroffene Grundsatzentscheidungen)

| # | Frage | Entscheidung |
|---|-------|--------------|
| 1 | Kartenraster | **Hexfelder** — organischer für Biome; Wegenetz über 6er-Nachbarschaft (Kap. 4, 5). |
| 2 | Raubbau-Balance | **Starke Versuchung + Krisen-Notnagel** — kurzfristig spürbar schneller, in Engpässen legitim, langfristig klar unterlegen; Korrektur statt Strafe (Kap. 4.4). |
| 3 | Jahreszeiten | **Mild-mechanisch** — beeinflussen Ertrag & Regeneration spürbar, blockieren nichts hart; Winter = Vorratsrhythmus (Kap. 6). |
| 4 | Spielmodus | **Nur Sandbox** mit wählbaren Bestrebungen, keine Kampagne (Kap. 11). |

### Noch offen für später
- Genauer Balancing-Kurvenverlauf von Vitalität ↔ Ertrag ↔ Regeneration.
- Anzahl & Identität der Tier-Symbiosen im Detail.
- Tag/Nacht zusätzlich zu Jahreszeiten — ja/nein?
