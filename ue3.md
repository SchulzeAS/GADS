
Übung 3
1. Aufgabe:  
Zeigen Sie, dass man n ganze Zahlen aus dem Bereich $[0..n^2 −1]$ in Zeit O(n) sortieren kann.

- Basis b
- Anzahl Ziffern = O($log_ba$)

      linSort(A)
        b <- benutzte Zahlenbasis   O(1)
        Basiswechsel(A,n)           O(n)
        Countingsort(A,1)           O(n)
        Countingsort(A,2)           O(n)
        Basiswechsel(A,b)           O(n)
        return A                    O(1)



2. Aufgabe:  
Geben Sie asymptotische obere Schranken für T(n) an, wenn T(n) durch die folgenden Rekursionsgleichungen gegeben ist. Für n ≤ 10 gelte T(n) = Θ(1). Geben Sie möglichst scharfe Schranken an und begründen Sie ihre Antworten.

(a) T(n) = T(n−2)+2logn  
  Mit jeder Rekursion werden es 2 weniger, daher sind es $n-10\over 2$ Schritte bis n ≤ 10, da in jedem Schritt logarithmischer Aufwand ist, ist es in O(n*log n)

(b) T(n) = T($\sqrt{n}$)+$\Theta$(loglog n)  
Irgendwie kommt man auf T(n) = O((loglog $n)^2$ )

(c) T(n) =  $\sqrt{n}$ T($\sqrt{n}$)+100n


3. Aufgabe:
Geben Sie asymptotische obere Schranken für T(n) an, wenn T(n) durch die folgenden Rekursionsgleichungen gegeben ist. Für n ≤ 4 sei jeweils T(n) = Θ(1). Geben Sie möglichst scharfe Schranken an und
begründen Sie ihre Antworten.  
(a) T(n) = 2T(${n\over 4} + \sqrt{n}$)  
(b) T(n) = T(n−1)+n  
(c) T(n) = 2T(n−1)  
(d) T(n) = $T({n\over2})+T({n\over4})+T({n\over8})+n$


4. Aufgabe:
Nehmen Sie an, Sie hätten einen Black-Box Algorithmus, der den Median deterministisch in linearer Zeit
im schlechtesten Fall bestimmt. Geben Sie darauf basierend einen Algorithmus an, der das k-t kleinste
Element bestimmt, und analysieren Sie den Algorithmus.


5. Aufgabe:
Eine Erdölfirma möchte eine Ost-West-Pipeline verlegen,
die ihre Bohrplattformen miteinander verbindet. Dabei sollen die n Plattformen, deren x,y-Koordinaten bekannt sind,
vertikal mit der horizontalen Ost-West-Pipeline verbunden
werden. Gesucht ist die Position der horizontalen Ost-WestPipeline, bei der die Summe der Längen der Abschlusspipelines von den Plattformen zur Ost-West-Pipeline minimiert
wird. Geben Sie einen O(n) Algorithmus zur Bestimmung
der Position der Ost-West-Pipeline an. Quelle: [Cormen, Leiserson, Rivest, Stein; Introduction to Algorithms]


6. Aufgabe:
Sei S eine Menge von n Elementen, die paarweise verschieden sind. Sei k ≤ n. Geben Sie einen O(n)
Algorithmus an, der die k Elemente aus S bestimmt, die am nächsten am Median liegen.
