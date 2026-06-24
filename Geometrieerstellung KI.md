# Berechnung der dynamischen Stoßkraft (Gwen Stacy)

Um die reale Belastung in **PrePoMax** simulieren zu können, muss der dynamische freie Fall in eine äquivalente statische Maximalkraft (F_max) umgerechnet werden. Diese Kraft repräsentiert den exakten Moment der höchsten Spannung, wenn der Faden maximal gedehnt ist und Gwen Stacy abrupt zum Stillstand kommt.

## 1. Gegebene Parameter und Variablen
Bevor die Kraft in PrePoMax eingetragen wird, müssen die Werte aus der quantitativen Filmanalyse definiert werden:

* [cite_start]**m (Masse):** 70 kg (Angenommenes Gewicht für Gwen Stacy [cite: 100]).
* **g (Erdbeschleunigung):** 9,81 m/s^2.
* **h (Fallhöhe):** Die Distanz des freien Falls vor dem Straffen des Fadens (muss aus der Filmszene rekonstruiert werden).
* **s (Dehnungsweg/Bremsweg):** Die Strecke, um die sich der Spinnenfaden elastisch dehnt, bis die Zielperson zum Stillstand kommt.

## 2. Physikalische Herleitung (Energieerhaltung)
Beim Auffangen wird die gesamte (kinetische und potenzielle) Energie des Falls in die elastische Spannenergie des Fadens umgewandelt.

**Die Gesamtenergie beim tiefsten Punkt (Stillstand):**
Die Person fällt nicht nur die Höhe (h), sondern auch den zusätzlichen Dehnungsweg (s) des Fadens nach unten. Die gesamte potenzielle Energie, die abgebaut werden muss, ist daher:
E_pot = m * g * (h + s)

**Die aufgenommene Spannenergie des Fadens:**
Unter der Annahme, dass das Hookesche Gesetz (lineare Elastizität) gilt, berechnet sich die im Faden gespeicherte Arbeit durch:
W_spann = 1/2 * F_max * s

**Gleichsetzen der Energien:**
m * g * (h + s) = 1/2 * F_max * s

## 3. Formel für die Maximalkraft (F_max)
Wenn wir die obige Gleichung nach der gesuchten Kraft F_max auflösen, erhalten wir den Wert, der in das CAD/FEA-Programm eingegeben werden muss:

> [!info] Endformel für PrePoMax
> **F_max = (2 * m * g * (h + s)) / s**

*Anmerkung für die Auswertung:* Diese Formel verdeutlicht das physikalische Kernproblem der Filmszene. Je kürzer der Dehnungsweg (s) des Spinnenfadens ist (abruptes Abbremsen), desto gewaltiger wird die Kraftspitze (F_max), die sowohl auf den Faden als auch auf den Körper von Gwen Stacy wirkt.

## 4. Anwendung im PrePoMax-Workflow
1.  Berechne den exakten Wert für **F_max** in Newton (N) mit den ermittelten Werten aus dem Film.
2.  Öffne das vorbereitete PrePoMax-Modell.
3.  Wechsle zu `FE Model` -> `Loads`.
4.  Erstelle eine `Surface Traction` auf der Unterseite des Fadens.
5.  Trage den berechneten Wert (z. B. 15000 N) auf der entsprechenden Achse (z.B. Z-Achse) ein. Achte dabei auf das korrekte Vorzeichen (meistens negativ, da es ein Zug nach unten ist).