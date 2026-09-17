## Das „Web-Swinging“ / Pendeln zwischen Wolkenkratzern (Teil 1 & 2)
### A. Szenenanalyse & physikalischer Kontext
Peter Parker schwingt an einem Faden durch die Häuserschluchten. Physikalisch lässt sich diese Bewegung als **Kreispendel (physikalisches Pendel)** modellieren.
### B. Physikalische Formeln & Herleitung
1. **Energieerhaltung beim Pendeln (Geschwindigkeit am tiefsten Punkt):**
    $$E_{\text{pot, max}} = E_{\text{kin, max}} \implies m \cdot g \cdot h = \frac{1}{2} m \cdot v_{\text{max}}^2$$
    $$v_{\text{max}} = \sqrt{2 \cdot g \cdot h} = \sqrt{2 \cdot g \cdot L \cdot (1 - \cos\theta_0)}$$
    - $L$: Seillänge / Radius der Kreisbahn
    - $\theta_0$: Auslenkwinkel beim Start (z. B. $60^\circ$)
2. **Zentripetalbeschleunigung & Zentripetalkraft am tiefsten Punkt:**
    $$a_c = \frac{v^2}{L}$$
    $$F_c = m \cdot \frac{v^2}{L}$$
3. **Gesamte Zugkraft im Faden & Scheingewicht am tiefsten Punkt:**
    $$F_{\text{ges}} = F_g + F_c = m \cdot g + m \cdot \frac{v^2}{L} = m \cdot \left(g + \frac{v^2}{L}\right)$$
    Setzt man $v_{\text{max}}^2 = 2gL(1 - \cos\theta_0)$ ein, ergibt sich die Gesamtbeschleunigung $a_{\text{ges}}$ am tiefsten Punkt:
    $$a_{\text{ges}} = g \cdot (3 - 2 \cos\theta_0)$$

### C. Konkrete Beispielrechnung & Werte
- **Masse Peter Parker:** $m = 75\,\text{kg}$
- **Seillänge:** $L = 30\,\text{m}$
- **Startwinkel:** $\theta_0 = 60^\circ$ ($\cos(60^\circ) = 0{,}5$)
- **Geschwindigkeit am tiefsten Punkt:**
    $$v_{\text{max}} = \sqrt{2 \cdot 9{,}81 \cdot 30 \cdot (1 - 0{,}5)} = \sqrt{294{,}3} \approx 17{,}16\,\text{m/s} \quad (\approx 61{,}8\,\text{km/h})$$
- **Gesamtbeschleunigung am tiefsten Punkt:**
    $$a_{\text{ges}} = 9{,}81 \cdot (3 - 2 \cdot 0{,}5) = 9{,}81 \cdot 2 = 19{,}62\,\text{m/s}^2 = 2\,g$$
    _(Hätte Spider-Man Anlauf genommen oder startet waagerecht bei $\theta_0 = 90^\circ$, steigt $a_{\text{ges}}$ auf $3\,g \approx 29{,}4\,\text{m/s}^2$)._
- **Gesamtkraft auf Peter Parker:** $F_{\text{ges}} = 75\,\text{kg} \cdot 19{,}62\,\text{m/s}^2 = 1.471{,}5\,\text{N}$
### D. Physikalische Bewertung („Amazing or Hallucinating?“)
- **Ergebnis:** **Realistisch („Amazing“)**. Belastungen von $2\,g$ bis $4\,g$ sind für trainierte Menschen und Kampfpiloten problemlos aushaltbar. Die mechanische Belastung auf den Faden ist moderat.
Experiment:
[[2026-09-17_Web-Swinging_Experiment|View]]