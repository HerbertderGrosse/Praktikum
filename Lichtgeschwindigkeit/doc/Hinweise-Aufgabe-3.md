# Hinweise für den Versuch Lichtgeschwindigkeit

## Aufgabe 3: Bestimmung des Brechungsindex $n$ von Wasser oder Plexiglas

In optisch dichten Medien ist $c$ niedriger, als im Vakuum (oder Luft). Das Maß in dem $c$ abnimmt wird durch den [Brechungsindex](https://de.wikipedia.org/wiki/Brechungsindex) $n$ (auch optische Dichte genannt) quantifiziert. Wir bestimmen den Brechungsindex durch die erhöhte Laufzeit des Lichtes im optisch dichteren Medium. Dazu bringen wir in einen Teil des Laufwegs $\ell$ des Lichtstrahls ein Behältnis der Länge $d<\ell$ mit dem optisch dichteren Medium ein. Damit gilt für die Laufzeit:

$$
\begin{equation}
\begin{split}
&\Delta t = \frac{\ell-d}{c}+\frac{n\,d}{c}; \\
&\\
& n = \frac{c\,\Delta t-\ell}{d}+1. \\
\end{split}
\end{equation}
$$
 Für Aufgabe 3.1 wird $\Delta t$ analog zu Aufgabe 2 bestimmt, die Abmessungen $\ell$ und $d$ sind gegeben. 

Der Laserentfernungsmesser gibt die Entfernung zu einer reflektierenden Oberfläche (Reflektor) basierend auf einer Laufzeitmessung des ausgesandten Laserlichts unter Annahme von $c$ (in Luft!) an: 

$$
\begin{equation}
\Delta t = \frac{2 \ell}{c}
\end{equation}
$$
Wird ein Teil $d$ des Wegs $\ell$ zum Reflektor durch ein Medium der optischen Dichte $n$ ersetzt ändert (verfälscht) dies die Längenmessung, woraus sich $n$ bestimmen lässt: 

$$
\begin{equation}
\begin{split}
\Delta t' &= 2\frac{\ell-d}{c} + 2\frac{d\,n}{c}; \\
&\\
\ell' &= \frac{c}{2}\Delta t' = \ell-d+d\,n; \\
&\\
&n = \frac{\ell'-\ell}{d}+1. \\
\end{split}
\end{equation}
$$
Dabei ist $\ell$ die unverfälschte Anzeige ohne und $\ell'$ die verfälschte Anzeige mit optisch dichterem Medium.

### Hinweise zur Durchführung

- Führen Sie die Messung für Aufgabe 3.2 mindestens viermal durch, indem Sie den Laserstrahl einmal quer und einmal längs durch die Küvette laufen lassen und jeweils noch einmal $\ell$ variieren. 

- Bestimmen Sie jeweils ein Ergebnis für $n_{i}$ mit entsprechender Unsicherheit $\Delta n_{i}$. 

- Das Ergebnis Ihrer Messung ist dann das gewichtete Mittel $\overline{n}$ der Einzelmessungen:

  ```math
  \begin{equation}
  \begin{split}
  &\overline{n} = \frac{\sum w_{i}n_{i}}{\sum w_{i}}\qquad \text{mit:}\qquad w_{i}=\frac{1}{\Delta n_{i}}; \\
  &\\
  &\mathrm{var}[\overline{n}] = \frac{N}{N-1}\frac{\sum w_{i}\left(n_{i}-\overline{n}\right)^{2}}{\sum w_{i}}; \qquad \sigma_{\overline{n}} = \sqrt{\mathrm{var}[\overline{n}]}, \\
  \end{split}
  \end{equation}
  ```

  wenn $N$ die Länge Ihrer Stichprobe ist.

# Navigation

[Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Lichtgeschwindigkeit)