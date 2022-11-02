# Zusammenfassung

---

## Beschreibung der Signale in der Nachrichtentechnik

Es werden nur periodische Signale behandelt

### Sinus

![Hier sollte Bild sein](Bilder/sinus.png)

Signalform: $\text{sinusförmig}$
Amplitude: $U_{ss},\hat u_{max},\hat u_{min}, \text{Offset} \ U_{DC}$
Periodendauer: $T$
Delay, Phasenverschiebung: $t_D, \text{Phasenwinkel} \ \varphi $
Frequenz: $f=\frac{1}{T}$

![Hier sollte Bild sein](Bilder/rechteck.png)

Signalform: $\text{rechteckförmig}$
Amplitude: $(\hat u_{max},\hat u_{min}),u_{max},u_{min} \text{Offset} \ U_{DC}$
Periodendauer: $T,t_i = \text{Impulsdauer}, t_p = \text{Pausendauer},\text{Tastverhältnis}=\frac{t_i}{t_p}$
Delay, Verzögerung: $t_D$
Frequenz: $T = t_i+t_p, f=\frac{1}{T}$

#### Gleichspannungsanteil $U_{DC}$

$U_{DC}=\frac{\hat u_i \cdot t_i + \hat u_p\cdot t_p}{T}$

#### Allgemeine Gleichung einer Rechteckschwingung

$w_0=2\pi f_0=Kreisfrequenz \ der \ Grundwelle$

#####

$a_n,b_n=Fourierkoeffizienten$

#####

$u(t)=a_{DC}+\sum_{n=1}^{\infty} [a_n \cdot cos(n\cdot w_0\cdot t)+b_n\cdot sin(n\cdot w_0 \cdot t)]$

#####

$a_{DC}=\frac{1}{T}\cdot \int_{0}^{T} u(t) \,dt$

#####

$a_n= \frac{2}{T}\cdot \int_{0}^{T} u(t)\cdot cos(n\cdot w_0 \cdot t) \,dt$

#####

$b_n= \frac{2}{T}\cdot \int_{0}^{T} u(t)\cdot sin(n\cdot w_0 \cdot t) \,dt$

---

## Spektraldichtefunktion

Berechnung von symetrischen Signalen, d.h. f(t) = f(-t)
![Hier sollte Bild sein](Bilder/rechtspeck.png)
![Hier sollte Bild sein](Bilder/spektral.png)

Die Berechnung der Amplitudenwerte des Spektrums mit der Spektraldichtefunktion resultiert aus Analogien und einer Betrachtung der Energieverteilung im Spektrum. Da keine negativen Frequenzen auftreten, wird der negative (rote) Bereich auf den positiven (grünen) Bereich geklappt => die roten werden zu den grünen Linien addiert, d.h. der Betrag verdoppelt sich.

### Amplitudenwerte

$A_n=u(n\cdot f_0)=2 \cdot \frac{U_{ss}\cdot t_i}{T} \cdot \frac{sin(\pi \cdot n \cdot f_0 \cdot t_i)}{\pi \cdot n \cdot f_0 \cdot t_i}=\frac{2\cdot U_{ss}}{\pi \cdot n}\cdot sin(\pi \cdot n \cdot f_0 \cdot t_i)$

#### Nullstellen für

$sin(\pi \cdot n \cdot f_0 \cdot t_i)=0=sin(\pi \cdot n \cdot \frac{t_i}{T})$
=> $n\cdot f_0 \cdot t_i = m (ganze \ Zahl)$
$n \cdot f_0=m \cdot \frac{1}{t_i} (Nullstellen \ im \ Spektrum \ bei \ \ m \cdot f_0)$

### Bandbreite(Definition)
vereinfacht: $B=\frac{1}{t_i}\ \ \ \text{für} \ t_i=t_p\ \text{folgt}\ \ B=\frac{2}{T}=2\cdot f_0$

---

## Frequenzsynthese

![Hier sollte Bild sein](Bilder/schaltung.png)

Bei der Frequenzsynthese werden die Momentanwerte der Einzelsignal zur Gesamtamplitude addiert und ergeben den zeitlichen Verlauf des Gesamtsignals $U_a$. Die einzelnen Frequenzen bleiben bei der Überlagerung erhalten und tauchen als Linien im Spektrum auf.

![Hier sollte Bild sein](Bilder/fourier1.png)

### Erkenntnisse

- Mit höheren Frequenzen nimmt die Amplitude ab, d.h. die Linie bei der Grundwelle hat die höchste Amplitude.
- Bei ti = tp treten nur bei ungeraden Vielfachen der Grundwelle Linien auf.
- Bei ti ungleich tp treten bei allen Vielfachen der Grundwelle Linien auf.
- Es gibt nur bei Vielfachen der Grundwelle Linien.
- Im Spektrum sieht man keine Phasenverschiebung des Signals
- Eine Veränderung des Offsets ändert nur die Linie bei 0 Hz
- Es gibt unendlich viele Spektrallinien
- Die Grundwelle hat die niedrigste Frequenz (>0 Hz)

---

## Leitungen

![Hier sollte Bild sein](Bilder/leitung.png)

Hin und Rückleitung zusammengefasst ergibt $R' = 2 \cdot \frac {R'}{2},L' = 2 \cdot \frac {L'}{2}$
Leitungsbelag = Kennwert bezogen auf die Längeneinheit 
z.B. $R'=\frac{2 \Omega}{100m}$

![Hier sollte Bild sein](Bilder/leitung1.png)

### Vereifachungen (praxisnäher)

- kurzes Leitungsstück => R' ≈ 0 $\Omega$
- hoher Isolationswiderstand => G' ≈ 0S
- hohe Frequenzen 
$X_L'=\omega \cdot L' \rightarrow \infty \Omega $
$X_c'=\frac{1}{\omega \cdot C'}\rightarrow 0\Omega$

Daraus fogt R' und G' können vernachlässigt werden
![Hier sollte Bild sein](Bilder/esb.png)