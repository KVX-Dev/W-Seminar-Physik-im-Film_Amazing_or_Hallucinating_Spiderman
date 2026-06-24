## 1. Mechanik: Grundlagen der Bewegung und Kraft
### 1.1 Kraft ($F$)
Eine Kraft ist eine Einwirkung, die einen Körper beschleunigen oder verformen kann. Nach dem Newtonschen Grundgesetz gilt:

$$F = m \cdot a$$

wobei $m$ die Masse und $a$ die Beschleunigung ist. Beim Auffangen von Gwen Stacy wirkt die **Stoßkraft**, die den Körper innerhalb eines sehr kurzen Zeitraums $\Delta t$ abbremst.

### 1.2 Impuls ($p$)
Der Impuls ist das Produkt aus Masse und Geschwindigkeit:

$$p = m \cdot v$$

Die Änderung des Impulses entspricht dem Kraftstoß:

$$\Delta p = F \cdot \Delta t = m \cdot \Delta v$$

> [!important] Relevanz für die Analyse
> Je kürzer der Bremsweg (und damit die Zeit $\Delta t$), desto größer ist die wirkende Kraft $F$. Das ist der entscheidende Faktor bei einem abrupten Stopp.

### 1.3 Energieerhaltung
Bei einem freien Fall wird potentielle Energie ($E_{\text{pot}}$) in kinetische Energie ($E_{\text{kin}}$) umgewandelt:

$$E_{\text{pot}} = m \cdot g \cdot h = \frac{1}{2} m \cdot v^2 = E_{\text{kin}}$$

Beim abrupten Stopp muss die Spinnenseide die gesamte kinetische Energie aufnehmen, meist durch Verformungsarbeit (Dehnung).

### 1.4 Elastizität
Ein Körper ist elastisch, wenn er nach einer Verformung in seine Ausgangsform zurückkehrt. Die Rückstellkraft $F_R$ ist bei idealen Federn proportional zur Auslenkung $s$ (Hookesches Gesetz für Federn):

$$F_R = -D \cdot s$$

*(mit $D$ = Federkonstante)*

---

## 2. Materialwissenschaft: Eigenschaften der Spinnenseide

### 2.1 Hookesches Gesetz (Materialspannung)
Im elastischen Bereich gilt für die mechanische Spannung $\sigma$ und die Dehnung $\varepsilon$:

$$\sigma = E \cdot \varepsilon$$

Hierbei ist $E$ der **Elastizitätsmodul** (E-Modul), ein Maß für die Steifigkeit des Materials.

### 2.2 Elastizitätsmodul ($E$)
Der E-Modul beschreibt das Verhältnis von Spannung zu Dehnung im Detail:

$$E = \frac{\sigma}{\varepsilon} = \frac{F \cdot L_0}{A \cdot \Delta L}$$

* **$L_0$:** Ausgangslänge des Fadens
* **$A$:** Querschnittsfläche ($A = \pi \cdot r^2$)
* **$\Delta L$:** Längenänderung (Dehnung)

### 2.3 Reißlänge
Die Reißlänge $L_{\text{Reiß}}$ ist die theoretische Länge eines Fadens, bei der dieser unter seinem eigenen Gewicht gerade noch nicht reißt. Sie ist ein Maß für die spezifische Festigkeit:

$$L_{\text{Reiß}} = \frac{R_m}{\rho \cdot g}$$

* **$R_m$:** Zugfestigkeit (maximale Spannung vor dem Reißen: $R_m = \frac{F_{\text{max}}}{A}$)
* **$\rho$:** Dichte des Materials
* **$g$:** Erdbeschleunigung ($\approx 9{,}81 \, \text{m/s}^2$)

---

## 3. Anwendung auf die „Gwen Stacy“-Szene

Um die physikalische Plausibilität der Filmszene zu prüfen, musst du die **maximale Stoßkraft** berechnen. Wenn Spider-Man Gwen mit einem Faden abfängt, wirkt eine negative Beschleunigung (Verzögerung) $a$. 

Die wirkende Gesamtkraft $F_{\text{ges}}$ setzt sich aus der Gewichtskraft und der Bremskraft zusammen:

$$F_{\text{ges}} = m \cdot (g + a)$$

