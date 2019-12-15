##Übung 4
###1. Aufgabe:
Erklären Sie, warum eine Aussage der Art  
$$\text{Die Laufzeit von Algorithmus A ist mindestens } O(n^2)$$
wenig Sinn ergibt.

####Antwort:  
Diese Aussage ergibt insofern wenig Sinn, da Die Groß-O-Notation eine Art oberen Grenzwert beschreibt, und zu sagen, es ist mindestens dieser obere Grenzwert ergibt einfach wenig Sinn. Eher sollte man sagen:  
 "$\text{Algorithmus A läuft in } \omega(n^2), \text{da Omega eine untere Grenze beschreibt.}$"  

###2. Aufgabe:
Zeigen Sie, dass
$$\sum^{n-1}_{k=\lfloor{n\over 2}\rfloor} k \leq {3 \over 8}n^2 + {1\over 2}n$$

###3. Aufgabe:
Gegeben seien paarweise verschiedene Zahlen $x_1,...,x_n$ und zugehörige Gewichte w1,...,wn, so dass $\sum w_i = 1$. Der gewichtete Median ist das Element $x_k$, für das gilt:  

(a) Zeigen Sie, wie man den gewichteten Median mit Hilfe eines Sortieralgorithmus in Zeit O(nlogn) bestimmen kann.  
(b) Wie kann man den gewichteten Median in linearer Zeit im schlechtesten Fall bestimmen?
###4. Aufgabe:
Die Elemente einer n-elementigen Liste L seinen rot oder blau gefärbt. Geben Sie einen effizienten
EREW-PRAM-Algorithmus an, der aus L die Liste der roten und die Liste der blauen Elemente extrahiert.
###5. Aufgabe:
Geben Sie einen effizienten EREW-PRAM-Algorithmus an, der für jeden Knoten v eines geordneten
binären Wurzelbaumes seine PREORDER-Nummer bestimmt.
####Antwort:
Ich schlage den Eulertour Algorithmus aus der Vorlesung vor, mit der Abwandlung, dass der C-Prozessor nicht den Wert -1, sondern 0 erhält, so wird jedem Knoten seine PREORDER-Nummer zugewiesen.
###6. Aufgabe:
Geben Sie einen effizienten EREW-PRAM-Algorithmus an, der für jeden Knoten v eines geordneten binären Wurzelbaumes die Anzahl der Elemente im Unterbaum mit Wurzel v bestimmt.
###7. Aufgabe:
Beweisen oder widerlegen Sie: Falls es in einem gerichteten Graphen G eine Kante (u,v) gibt, so ist bei
jeder Tiefensuche auf G die discovery time d[v] von v kleiner als die finishing time f [u] von u.
###8. Aufgabe:
Erklären Sie, ob bzw. wie es sein kann, dass in einem gerichteten Graphen G bei einer Tiefensuche ein DFS-Baum entsteht, der nur aus einem Knoten u besteht, obwohl u sowohl eingehende als auch ausgehende Kanten besitzt.

####Antwort:   
Der Knoten u ist Teil eines Zyklus, bzw. der komplette Graph G ist ein Zyklus.
