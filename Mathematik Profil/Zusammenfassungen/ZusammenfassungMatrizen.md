# Matrizen

## Was ist eine Matrix

Eine $m * n$ Matrix hat $m$ Zeilen und $n$ Spalten. Somit hat sie $m * n$ Zahlen.
Der Name einer Matrix ist meistens ein Grossbuchstabe. Um eine Zahl in der Matrix aufzuzeigen, benutzt man den entsprechenden Kleinbuchstaben.
Um ein Feld zu lokalisieren, wird zuerst die Zeile gelesen, dann die Spalte.


$$A = \begin{pmatrix}
1 & 2 \\
3 & 4 \end{pmatrix}$$

$$a_{11} = 1; 
a_{12} = 2; 
a_{21} = 3; 
a_{22} = 4$$


## Spezielle Matrizen

**Vektor:**  
Wenn $n = 1$ ist es ein Spaltenvektor.  
Wenn $m = 1$ ist es ein Zeilenvektor.  
Für Vektoren schreibt man $\vec{a} = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ oder $\vec{b} = \begin{pmatrix} 1, 2 \end{pmatrix}$  
*(Bei einem Zeilenvektor werden die Elemente mit "," abgetrennt)*

**Quadratische Matrix:**  
Eine Matrix wird quadratisch genannt, wenn $n = m$.

**Nullmatrix:**  
Eine Matrix N wird Nullmatrix genannt, wenn sie nur aus Nullen besteht.

**Einheitsmatrix:**  
Die Einheitsmatrix E ist eine Quadratische Nullmatrix, welche so abgeändert wird, dass alle Elemente in der Haupdiagonale ($e_{ii}$) eine Eins werden.
Die Einheitsmatrix ist das neutrale Element, wenn Matrizen multipliziert werden.

**Inverse Matrix:**  
Eine Matrix $A^{-1}$ ist invers zu einer anderen Matrix $A$, wenn $A * A^{-1} = E$


## Operationen

**Die Resultatsmatrix heisst R:**

* Man kann zwei Matrizen $A$ und $B$ Addieren, wenn beide gleich gross sind:  
$r_{ij} = a_{ij} + b_{ij}$
* Man kann eine Zahl $x$ immer mit einer Matrix $A$ multiplizieren:  
$r_{ij} = a_{ij} * x$
* Man kann zwei Matrizen $A$ und $B$ Multiplizieren, wenn $A$ gleich viele Spalten wie $B$ Zeilen hat (diese Zahl wird $l$ genannt):  
$r_{ij} = \sum_{p=1}^{l} a_{ip} * b_{pj}$


\newpage


## Rechengesetzte

Folgende Gesetze gelten:

* Assoziativgesetz: $(A*B)*C = A*(B*C)$
* Distributivgesetz: $A*(B+C) = A*B + A*C$
* Es gibt Nullteiler.  D.h, dass das Produkt von zwei Matrizen $\neq N$ die Nullmatrix $N$ sein kann.

Folgende Gesetze gelten **nicht**:

* Kommutativgesetz: $A*B \neq B*A$ mit Ausnahmen:
    * Matrix mit Einheitsmatrix multiplizieren: $A*E = E*A$
    * Matrix mit Inverser Matrix multiplizieren: $A*A^{-1} = A^{-1}*A$


## Inverse Matrix berechnen

Für eine $2*2$ Matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ kann zuerst die Determinante bestimmt werden:

$$det(A) = det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = a*d - b*c$$

Dann gilt $A^{-1} = \frac{1}{det(A)} * \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$


Mit der Inversen Matrix kann man eine Gleichung lösen:

$$A * X = B$$
$$A^{-1} * B = X$$

*oder*

$$X * A = B$$
$$B * A^{-1} = X$$


Eine solche Gleichung kann auch als einfaches Gleichungssystem dargestellt werden:

$$
\begin{pmatrix} a & b \\ c & d \end{pmatrix} * \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} e \\ f \end{pmatrix}
$$

$$\begin{cases}
a*x + b*y = e \\
c*x + d*y = f
\end{cases}$$
