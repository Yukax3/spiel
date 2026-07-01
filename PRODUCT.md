# Product

## Register

product

## Users
Cozy-/Aufbauspiel-Spieler (Fans von Die Siedler, Anno, ähnlichen Wirtschafts-/Logistiksimulationen), die am Rechner oder Tablet ein entspanntes, aber tiefes Aufbauspiel spielen — im Sitzen, oft über längere Sessions, mit Fokus auf Übersicht über Ressourcen, Bevölkerung und Produktionsketten während sie gleichzeitig die Karte im Blick behalten müssen.

## Product Purpose
Wurzelwerk ist ein browserbasiertes 2D-Aufbau- und Logistikspiel (Hex-Grid, Canvas-Rendering). Kern-Loop: Siedler tragen Güter über ein Wegenetz, Produktionsketten verarbeiten Rohstoffe, eine "Vitalität" pro Biom-Zone belohnt nachhaltiges Wirtschaften. Erfolg bedeutet: Der Spieler kann jederzeit auf einen Blick erfassen, was seine Kolonie gerade braucht (Nahrung, freie Arbeiter, Lagerplatz), ohne dass das HUD selbst zur kognitiven Last wird.

## Brand Personality
**(Update 2026-07-01, überschreibt frühere Einschätzung):** Nutzer will explizit weg vom "Cozy-Kindergame"-Look für das UI-Chrome (HUD/Panels/Buttons) — Ziel: professionell, kompromisslos, "brutal", High-End-Strategiespiel-Niveau ("2030-level"). Referenzpunkt: Anno 1800 / Frostpunk / Civilization-Interfaces — ernsthafte Wirtschaftssimulation für erwachsene Spieler, kein Mobile-Casual-Anstrich. Die illustrierte Canvas-Weltdarstellung (Bäume, Häuser) bleibt wie sie ist; der Kontrast zwischen warmer Spielwelt und scharfem, technischem UI-Overlay ist gewollt.

## Anti-references
Kein Casino-/Idle-Game-UI (grelle Farben, aggressive Badges, verspielte Bounce-Animationen). Kein weiches Glas-Design mit runden Ecken, Pastelltönen oder verspielten Verläufen — das war die alte Richtung und ist jetzt explizit unerwünscht. Kein generisches Bootstrap-Dashboard.

## Design Principles
- Handlungsrelevante Information (Nahrung, freie Arbeiter, Lagerstand) muss auf den ersten Blick erfassbar sein — das sind die Werte, die den nächsten Klick des Spielers bestimmen.
- Gruppierung nach Bedeutung, nicht nach Einfügereihenfolge: Rohstoffe, Bevölkerung/Arbeit, Session-Werkzeuge (Speichern/Laden/Einstellungen) sind drei unterschiedliche mentale Kategorien und sollten sich auch visuell trennen.
- Scharfe Kanten statt runder Ecken, präzise dünne Trennlinien statt weicher Schatten/Glow, ein einziger kräftiger Akzentton (nicht Gold-auf-Grün-Softness) für Daten/States.
- Technische Typografie: enge, klar strukturierte Zahlen-Darstellung (tabular nums), dezente Versalien mit Letter-Spacing für Labels — wirkt wie ein Cockpit/Terminal, nicht wie eine App für Kinder.

## Accessibility & Inclusion
Touch-/DS-taugliche Bedienung wird im GDD explizit gefordert (Kap. 12) — Zielgrößen für Tap-Targets beachten. Keine harten WCAG-Vorgaben vom Nutzer genannt; Kontrast von Text auf dem dunklen Panel-Hintergrund sollte dennoch gut lesbar bleiben (aktuell heller Text auf sehr dunklem Grund, grundsätzlich kontraststark).
