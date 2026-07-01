# Product

## Register

product

## Users
Cozy-/Aufbauspiel-Spieler (Fans von Die Siedler, Anno, ähnlichen Wirtschafts-/Logistiksimulationen), die am Rechner oder Tablet ein entspanntes, aber tiefes Aufbauspiel spielen — im Sitzen, oft über längere Sessions, mit Fokus auf Übersicht über Ressourcen, Bevölkerung und Produktionsketten während sie gleichzeitig die Karte im Blick behalten müssen.

## Product Purpose
Wurzelwerk ist ein browserbasiertes 2D-Aufbau- und Logistikspiel (Hex-Grid, Canvas-Rendering). Kern-Loop: Siedler tragen Güter über ein Wegenetz, Produktionsketten verarbeiten Rohstoffe, eine "Vitalität" pro Biom-Zone belohnt nachhaltiges Wirtschaften. Erfolg bedeutet: Der Spieler kann jederzeit auf einen Blick erfassen, was seine Kolonie gerade braucht (Nahrung, freie Arbeiter, Lagerplatz), ohne dass das HUD selbst zur kognitiven Last wird.

## Brand Personality
Ruhig, warm, kontemplativ — "Cozy-Aufbauspiel mit Tiefe" (Originalzitat aus dem Game Design Dokument). Kein Stress, keine grelle Dringlichkeit; Informationsdichte soll organisiert und lesbar sein, nicht hektisch.

## Anti-references
Kein hartes Casino-/Idle-Game-UI (grelle Farben, aggressive Benachrichtigungs-Badges, Kauf-Dialoge). Kein steriles Enterprise-Dashboard-Look. Das HUD soll sich in die warme, illustrative Hain-Ästhetik einfügen, nicht wie ein technisches Overlay wirken.

## Design Principles
- Handlungsrelevante Information (Nahrung, freie Arbeiter, Lagerstand) muss auf den ersten Blick erfassbar sein — das sind die Werte, die den nächsten Klick des Spielers bestimmen.
- Gruppierung nach Bedeutung, nicht nach Einfügereihenfolge: Rohstoffe, Bevölkerung/Arbeit, Session-Werkzeuge (Speichern/Laden/Einstellungen) sind drei unterschiedliche mentale Kategorien und sollten sich auch visuell trennen.
- Ruhige Dichte statt Reizüberflutung: viele Datenpunkte sind ok, solange klare visuelle Hierarchie (Größe, Kontrast, Gruppierung) sie ordnet.
- Bestehende Ästhetik respektieren (dunkles, warmes Glas-Panel-Design mit Gold-Akzenten) statt neu zu erfinden.

## Accessibility & Inclusion
Touch-/DS-taugliche Bedienung wird im GDD explizit gefordert (Kap. 12) — Zielgrößen für Tap-Targets beachten. Keine harten WCAG-Vorgaben vom Nutzer genannt; Kontrast von Text auf dem dunklen Panel-Hintergrund sollte dennoch gut lesbar bleiben (aktuell heller Text auf sehr dunklem Grund, grundsätzlich kontraststark).
