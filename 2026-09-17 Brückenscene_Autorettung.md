## 1. Die Brückenszene / Autorettung (_The Amazing Spider-Man 1_)
### A. Szenenanalyse & physikalischer Kontext
Spider-Man hält ein abstürzendes Auto (Mittelklassewagen inkl. Insasse, Masse $M \approx 1500\,\text{kg}$) an einem einzelnen, dünnen Spinnenfaden unter der [[2026-09-17 Brückenscene_Autorettung_Williamsburg Bridge|Williamsburg Bridge]]. Das Auto hängt schwingend in der Luft und wird statisch gehalten.
### B. Physikalische Formeln & Herleitung
1. **Gewichtskraft (Statische Grundlast):**
    $$F_g = M \cdot g$$
    - $M$: Gesamtmasse ($1500\,\text{kg}$)
    - $g$: Erdbeschleunigung ($9{,}81\,\text{m/s}^2$)
2. **Mechanische Zugspannung im Faden:**
    $$\sigma = \frac{F}{A} = \frac{F}{\pi \cdot r^2}$$
    - $\sigma$: Mechanische Spannung (in $\text{N/m}^2$ bzw. $\text{Pa}$
    - $A$: Querschnittsfläche des zylindrischen Fadens ($\pi \cdot r^2$)
    - $r$: Radius des Spinnenfadens
3. **Elastische Dehnung (Hookesches Gesetz):**
    $$\sigma = E \cdot \varepsilon \quad \Longleftrightarrow \quad \frac{F}{A} = E \cdot \frac{\Delta L}{L_0}$$
    - $E$: Elastizitätsmodul (Young-Modul in $\text{GPa}$)
    - $\varepsilon = \frac{\Delta L}{L_0}$: Relative Dehnung
### C. Konkrete Beispielrechnung & Werte
- **Masse des Autos:** $M = 1500\,\text{kg}$
- **Gewichtskraft:** $F_g = 1500\,\text{kg} \cdot 9{,}81\,\text{m/s}^2 = 14.715\,\text{N} \approx 14{,}7\,\text{kN}$
- **Radius des Netzfadens:** $r = 2\,\text{mm} = 0{,}002\,\text{m}$ (Querschnitt $A = \pi \cdot (0{,}002\,\text{m})^2 \approx 1{,}26 \times 10^{-5}\,\text{m}^2$)
- **Berechnung der Zugspannung:**
    $$\sigma = \frac{14.715\,\text{N}}{1{,}26 \times 10^{-5}\,\text{m}^2} \approx 1{,}17 \times 10^9\,\text{N/m}^2 = 1{,}17\,\text{GPa}$$
### D. Physikalische Bewertung („Amazing or Hallucinating?“)

- Realer Spinnenfaden (Dragline-Seide von _Nephila clavipes_) besitzt eine Reißfestigkeit von $\sigma_{\text{max}} \approx 1{,}1 \text{ bis } 1{,}4\,\text{GPa}$.
    
- **Ergebnis:** **Möglich („Amazing“)**. Ein Spinnenfaden von nur $4\,\text{mm}$ Durchmesser könnte das Auto statisch tragen, da die erforderliche Zugspannung ($1{,}17\,\text{GPa}$) knapp unter der Reißfestigkeit echter Spinnenseide liegt. Dynamische Zusatzbelastungen durch Schwingungen würden den Faden allerdings zum Reißen bringen.