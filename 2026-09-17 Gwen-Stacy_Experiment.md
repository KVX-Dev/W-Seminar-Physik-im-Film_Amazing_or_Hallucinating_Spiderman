#### **Versuchsziel**
Quantifizierung der auftretenden Stoßkraftspitze $F_{\text{Stoß}}$ und der maximalen Verzögerung $a_{\text{max}}$ beim abrupten Stoppen einer Fallmasse an unterschiedlich elastischen Ersatzfasern.
#### **Versuchsaufbau & Material**
- **Masse-Objekt:** Smartphone (in stark gepolsterter Schutzhülle, Gesamtmasse $m_{\text{ges}}$ wiegen, z. B. $0{,}25\,\text{kg}$)
- **Mess-Software:** App **phyphox** (Modul: _„Beschleunigung (ohne g)“_ oder _„Einfache Beschleunigung“_)
- **Testfasern (Länge jeweils $L_0 = 1{,}00\,\text{m}$):**
    1. Starre Schnur (z. B. Nähseide / dünne Hanfschnur)
    2. Elastischere Faser (z. B. Nylon-Angelschnur)
    3. Hochelastisches Gummi/Expanderband
- **Halterung:** Reißfest verankertes Stativ oder Deckenhaken
```
             [ Feste Deckenhalterung ]
                         |
                         |  Testfaser (Länge L_0 = 1,00 m)
                         |
                 [ Smartphone in Hülle ] (Masse m)
                 (phyphox: Beschleunigung)
                         |
                         v (Freier Fall aus Höhe h = L_0)
```
#### **Durchführung**
1. Die Faser der Länge $L_0 = 1{,}00\,\text{m}$ wird an der Halterung und an der Smartphone-Hülle fixiert.
2. Das Smartphone wird auf Höhe der Aufhängung gehalten (Seil ist schlaff, Fallhöhe $h = L_0 = 1{,}00\,\text{m}$).
3. In **phyphox** wird die Aufzeichnung gestartet.
4. Das Smartphone wird losgelassen. Es fällt im freien Fall, bis die Faser gestrafft wird und den Fall stoppt.
5. Aus den phyphox-Daten wird der maximale Beschleunigungssensor-Peak $a_{\text{max}}$ (in $\text{m/s}^2$) ausgelesen.
6. Wiederholung der Messreihe für alle drei Testmaterialien.
#### **Auswertung & Ausbeute für die Seminararbeit**
- **Berechnung der maximalen Stoßkraft:**
    $$F_{\text{Stoß}} = m \cdot (g + a_{\text{max}})$$
- **Vergleich der Materialien:**
    - Starre Schnüre erzeugen extrem kurze Bremswege $\Delta x$ und riesige Beschleunigungsspitzen $a_{\text{max}}$ ($> 150\,\text{m/s}^2$).
    - Elastische Schnüre dehnen sich, vergrößern $\Delta x$ und flachen den Peak $a_{\text{max}}$ deutlich ab.
- **Bezug zur Gwen-Stacy-Szene:** Mit diesem Experiment zeigst du experimentell, dass Spider-Mans Netz ohne ausreichende Dehnbarkeit (Elastizitätsmodul) wie ein Stahlseil wirkt und das Abfangen tödlich macht.