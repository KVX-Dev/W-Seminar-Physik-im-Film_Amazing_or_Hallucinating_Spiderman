Diese Anleitung beschreibt den kompletten Workflow in PrePoMax (CalculiX), um den in der Seminararbeit thematisierten Stoßbelastungs-Fallversuch digital nachzubilden. Da die dynamische Phase des Abbremsens extrem schnell abläuft, ist die Simulation eine essenzielle Brücke zwischen der Theorie und dem geplanten phyphox-Experiment.

> [!info] Konzept der äquivalenten statischen Last PrePoMax kann zwar dynamische Analysen durchführen, für den Einstieg (und um die Hookesche Elastizitätslehre sauber anzuwenden) empfiehlt es sich jedoch, den freien Fall in eine **äquivalente statische Maximalkraft** ($F_{max}$) umzurechnen und diese statisch auf das Modell wirken zu lassen.

## Phase 1: Geometrie-Import (Die Spinnenseide)

PrePoMax benötigt eine fertige 3D-Geometrie, da es primär ein reines Berechnungsnetzwerk aufbaut.

1. **Erstellung im CAD:** Konstruiere in einem CAD-Programm (z. B. FreeCAD, Fusion360) einen langen, dünnen Zylinder.
    - _Tipp für die Maße:_ Nimm für einen ersten Testlauf eine realistische Länge (z. B. $L = 10 \text{ m}$) und einen winzigen Radius (z. B. $r = 1.5 \text{ mm}$).
2. **Export:** Speichere die Datei zwingend als **.step** oder **.iges** ab.
3. **Import in PrePoMax:** - Öffne PrePoMax.
    - Wähle `File` $\rightarrow$ `New`. Wähle das Einheitensystem `mm, ton, s, N, MPa` (Standard im Maschinenbau).
    - Wähle `File` $\rightarrow$ `Import` und lade deine STEP-Datei.
## Phase 2: Materialdefinition (Materialwissenschaft)
Hier verknüpfen wir deine Literaturrecherche mit der Simulation. Wir benötigen den Elastizitätsmodul.
1. **Material erstellen:**
    - Navigiere im linken Strukturbaum zum Reiter **FE Model**.
    - Rechtsklick auf `Materials` $\rightarrow$ `Create`.
    - Benenne es z. B. "Nylonfaden" oder "Spinnenseide".
2. **Elastizität hinzufügen:**
    - Wähle im neuen Fenster `Elasticity` $\rightarrow$ `Elastic`.
    - **Young's Modulus ($E$):** Trage den E-Modul ein. (Beispiel für starkes Nylon: ca. 3000 MPa; Spinnenseide kann zwischen 1000 und 10000 MPa variieren).
    - **Poisson's Ratio ($\nu$):** Die Querkontraktionszahl. Für Polymere/Nylon liegt diese oft bei **0.4**.
3. **Sektion zuweisen:**
    - Rechtsklick auf `Sections` $\rightarrow$ `Create` $\rightarrow$ `Solid Section`.
    - Wähle bei _Material_ dein erstelltes Material aus.
    - Klicke im 3D-Fenster auf deinen Zylinder, um die Auswahl zu bestätigen (er wird markiert). Bestätige mit `OK`.
## Phase 3: Vernetzung (Meshing)
Das Bauteil muss für die Finite-Elemente-Methode in ein Gitter (Mesh) zerlegt werden. Da ein Faden ein extremes Längen-zu-Durchmesser-Verhältnis hat, erfordert dies Präzision.
1. Wechsel in den Reiter **Mesh** (links oben).
2. Doppelklick auf `Meshing Parameters`.
3. **Elementgröße anpassen:**
    - _Max element size:_ Darf nicht größer sein als der halbe Durchmesser deines Fadens, sonst besteht das Modell aus zu wenigen Schichten, um Biegung oder Dehnung korrekt zu berechnen. Setze ihn testweise auf **0.5 mm**.
4. Rechtsklick auf dein Modell im Strukturbaum $\rightarrow$ `Create Mesh`.    

> [!warning] Rechenleistung Bei einem 10 Meter langen Faden und 0.5 mm Elementgröße generiert der PC zehntausende Elemente. Falls das Programm abstürzt, verkürze für den Testlauf die Länge des Fadens im CAD-Programm (z.B. auf 1 Meter) und rechne die Dehnung später analytisch hoch.
## Phase 4: Randbedingungen und Lasten (Die Gwen Stacy Szene)
Nun simulieren wir den Moment des Straffens der Leine. Wir gehen von Gwen Stacys Gewicht von 70 kg aus.
### Berechnung der Maximalkraft
Um die Last ($F_{max}$) zu definieren, musst du aus der Fallhöhe ($h$) über die Energieerhaltung die Kraftspitze berechnen, die beim abrupten Stoppen entsteht. Die kinetische Energie wird in elastische Verformungsenergie umgewandelt:

$$E_{kin} = E_{spann}$$

$$m \cdot g \cdot h = \frac{1}{2} \cdot D \cdot s^2$$

_(Mit $D$ als Federkonstante und $s$ als Dehnungsweg)._
Sobald du über diese Formel die maximale Kraft $F_{max}$ ermittelt hast, überträgst du sie in PrePoMax:
### Setup in PrePoMax
1. Wechsel zurück zum Reiter **FE Model**.
2. **Step erstellen:** Rechtsklick auf `Steps` $\rightarrow$ `Create`. Wähle `Static Step`. Bestätige mit `OK`.
3. **Aufhängung (Wolkenkratzer) fixieren:**
    - Rechtsklick auf `BCs` (Boundary Conditions) $\rightarrow$ `Create` $\rightarrow$ `Fixed`.
    - Rotiere die Kamera zur oberen Kreisfläche des Zylinders, klicke sie an und bestätige. Die Fläche ist nun unbeweglich.
4. **Kraft (Gwen Stacy) applizieren:**
    - Rechtsklick auf `Loads` $\rightarrow$ `Create` $\rightarrow$ `Surface Traction`.
    - Klicke auf die untere Kreisfläche des Zylinders.
    - Trage bei **Force (N)** deinen berechneten Wert für $F_{max}$ ein (Achtung: Achte auf die Richtung. Wenn der Faden auf der Z-Achse liegt, trage z. B. `-15000` bei Z ein).
## Phase 5: Simulation & Auswertung (Die Analyse)
1. **Job starten:**
    - Rechtsklick auf `Analysis` $\rightarrow$ `Create`.
    - Rechtsklick auf die neu erstellte Analyse $\rightarrow$ `Run`.
    - Warte, bis der Status auf _Finished_ springt.
2. **Ergebnisse interpretieren:**
    - Rechtsklick auf die Analyse $\rightarrow$ `Results`. PrePoMax wechselt nun in die Post-Processing-Ansicht.
    - **Von-Mises-Spannung prüfen:** Wähle links oben `Stress` $\rightarrow$ `von Mises`. Vergleiche den Maximalwert (in MPa) mit der theoretischen Reißfestigkeit (Zugfestigkeit) deines Materials. Ist der Wert im Programm höher als die Reißfestigkeit deines realen Fadens, würde er reißen – Gwen Stacy wäre nicht gerettet. 
    - **Dehnung prüfen:** Wähle `Displacement` $\rightarrow$ `Total`. Hier siehst du in Millimetern, wie lang sich der Faden wie ein Gummiband dehnen würde.
        
#### Modellierung mit Free CAD (Geometrieerstellung)
[[Geometrieerstellung KI]]