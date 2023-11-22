# Hinweise für den Versuch Vierpole und Leitungen

## Aufgabe 2: Drosselkette [2/4]

### Leitungseigenschaften

Aus der Substitution (Gleichung **(6)** [hier](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2.md))
$$
\begin{equation*}
\cosh\gamma\equiv\frac{Z_{\mathrm{L}}}{Z_{\mathrm{C}}}+1;\qquad \sinh\gamma\equiv\frac{Z_{\mathrm{L}}}{Z_{0}}= \sqrt{\frac{2\,Z_{\mathrm{L}}}{Z_{\mathrm{C}}}}
\end{equation*}
$$
 folgt (für kleine Werte von $\gamma$)
$$
\begin{equation*}
\begin{split}
&\sinh\frac{\gamma}{2} = \sqrt{\frac{Z_{\mathrm{L}}}{2\,Z_{\mathrm{C}}}} = \sqrt{-\left(\frac{\omega}{\omega_{0}}\right)^{2}} = i\frac{\omega}{\omega_{0}} \\
&\\
&\text{mit:}\\
&\\
&\frac{Z_{\mathrm{L}}}{2\,Z_{\mathrm{C}}} = -\left(\frac{\omega}{\omega_{0}}\right)^{2}.
\end{split}
\end{equation*}
$$
Andererseits gilt (aus den [Additionstheoremen](https://de.wikipedia.org/wiki/Sinus_hyperbolicus_und_Kosinus_hyperbolicus) des $\sinh(\hspace{0.1cm}\cdot\hspace{0.1cm})$):
$$
\begin{equation*}
\sinh\frac{\gamma}{2} = \sinh\left(\frac{\alpha+i\beta}{2}\right) = \sinh\frac{\alpha}{2}\,\cos\frac{\beta}{2} + i\cosh\frac{\alpha}{2}\,\sin\frac{\beta}{2},
\end{equation*}
$$
die folgenden Gleichungen müssen also gleichzeitig erfüllt sein: 
$$
\begin{equation*}
\begin{split}
&\sinh\frac{\alpha}{2}\,\cos\frac{\beta}{2} = 0, \\
&\\
&\cosh\frac{\alpha}{2}\,\sin\frac{\beta}{2} = \frac{\omega}{\omega_{0}},
\end{split}
\end{equation*}
$$
woraus man die folgenden Lösungen erhält: 
$$
\begin{equation*}
\begin{array}{ccl}
\alpha & \beta & \\
0 & 2\,\arcsin\left(\frac{\omega}{\omega_{0}}\right) & \text{f\"ur }\omega<\omega_{0}\\
2\,\mathrm{arccosh}\left(\frac{\omega}{\omega_{0}}\right) & \pi & \text{f\"ur }\omega>\omega_{0},\\
\end{array}
\end{equation*}
$$
d.h. die (ideale) Drosselkette hat die **Eigenschaft eines Tiefpasses**: Unterhalb der Grenzfrequenz weist sie keine Dämpfung auf, d.h. sie ist als Leitung **verlustfrei**. Oberhalb der Grenzfrequenz steigt die Dämpfung mit $\omega$ steil an. Die Phase des Ausgangssignals ist um $\pi$ zum Eingangssignal verschoben. 

# Navigation

[Zurück](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2.md) | [Main](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen) | [Weiter](https://gitlab.kit.edu/kit/etp-lehre/p1-praktikum/students/-/tree/main/Vierpole_und_Leitungen/doc/Hinweise-Aufgabe-2-b.md)
