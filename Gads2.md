##Vorlesung 10(?) 10.1.20

BCC eines ungerichteten zusammenhängenden Graphen G=(V,E)  
- Brücke
- Artikulationspunkt  
- BCC

Partition der Kantenmenge E,  
$e_1$ ~ $e_2$ g.d.w es gibt einfachen Kreis $C_s$, der $e_1$ und $e_2$ enthält, oder $e_1 = e_2$

  BCC := Äquivalenzklassen bzgl. ~

  Zyklus: Teilgraph, jeder Knoten hat geraden Grad  
  Zyklenraum: $\mathbb{Z_2}$-Vektorraum  
  T aufspannender Baum von G.  
  Fundamentalzyklus bzgl. T besteht aus einer Kante $e\in G-T$(e kommt also in dem aufspannenden Baum nicht vor.)  
  und dem einfachen Pfad in T, der die Endknoten von e verbindet.  
  Fundamentalzyklen bzgl. T bilden Basis des Zyklenraums


  Wähle Wurzel in T (beliebig)  
    Elternrelation bzgl. T    
    Für v $\in V$ bezeichne p(v) den Elternknoten, für die Wurzel sei p(v) = NULL.

  Relation R':  
  $e_1 R' e_2$ g.d.w. $e_1 = e_2$ oder es gibt einen Fundamentalzyklus, (bzgl. T), der beide Kanten $e_1,e_2$ enthält.  

  Lemma: $e_1$ ~ $e_2$ g.d.w $e_1(R')^* e_2$

  zu zeigen:

  1. $e_1$ ~ $e_2$ &rarr; $e_1(R')^* e_2$
  2. $e_1(R')^* e_2$ &rarr;  $e_1$ ~ $e_2$  

  - a $e_1 = e_2$  
    -  $e_1$ ~ $e_2$ => $e_1 R' e_2$ => $e_1(R')^* e_2$
  - b $e_1 \ne e_2$ => es gibt einfachen Kreis C, der $e_1$ und $e_2$ enthält.

  Da Fundamentalzyklen Basis sind, gilt $C = C_1 \oplus C_2 \oplus \dots C_k$  
  $C_1, \dots C_k$ Fundamentalzyklen.

  Wir dürfen annehmen, dass $C_L$ so nummeriert sind, dass es für alle $C_i, i\geq 2$ eine $C_j, j < i,$ gibt, so dass $C_i \text{ und } C_j$ eine gemeinsame Kante haben, da G zusammenhängend ist. Sonst würden $C_1, \dots, C_{i-1}$ und $C_i ...C_k$ disjunkte Komponenten (&rarr; BCC) bilden.

  Behauptung:  
  Falls $e_1,e_2 \in C_1 \cup ... \cup C_l, l=1..k$ so gilt $e_1 (R')^* e_2$  

  Induktionsbeweis:  
  l = 1: $e_1,e_2 \in C_1,$ also $e R' e_2$, also $e_1 (R')^* e_2$.  
  Induktionsanfang:  
  Bed. gelte für $1,...l-1$.
  $e_1,e_2 \in C_1 \cup \dots \cup C_{l-1} \cup C_l$  

  $e_1,e_2 \in C' => e_1 (R')^* e_2$.  
  $e_1,e_2 \in C_l => e_1 R' e_2 => e_1 (R')^* e_2$  
  $e_1 \in C', e_2 \in C_l:$  
  es gitb $C_j, j \in \{1,..,l-1\}$, so dass $C_l$ und $C_j$ eine gemeinsame Kante e besitzen.

  $e_1 \in C', e \in C_j \subseteq C'$  
  also nach Induktionsanfang:$e_1 (R')^* e$

  $C_l$ Fundamentalzyklus also $e R' e_2$, also $e (R')^* e_2$  

  => Transitivität von $(R')^* :$ $e_1 (R')^* e_2$  

  $e_2 \in C', e_1 \in C_l$  analog!  

  $e_1 (R')^* e_2$ => $e_1$ ~ $e_2$

  Beobachtung: $e_1 R' e_2$ => $e_1$ ~ $e_2$
  sonst: $e_1 (R')^* e_2 =>$ es gibt Kanten $e^{(0)},e^{(1)},...,e^{(i)}$, so dass $e_1 = e^{(0)} \\e_2 = e^{(i)}$  
  und $e^{(j)} R' e^{(j+1)}, j= 0..i-1$

  Also $e^{(j)}$ ~ $e^{(j+1)}$ für j=0,..,i-1
  und weil ~transitiv ist, auch $e_1 = e^{(0)}$ ~ $e^{(i)} = e_2$  

  ---
  Es "genügt" also, sich Fundamentalzyklen anzuschauen.  

  Wir identifizieren Knoten in G mit ihrer PREORDER-Nummer bzgl. des Wurzelbaums T.  
  Tarjan & Vishkin betrachten weitere Relationen auf Kanten.  
  $R^{(i)}$  
  {v,w} $R^{(i)}$ zu {w,p(w)}  
  falls $\{v,w\} \in G-T$ und v<w  

  $R^{(ii)}$:  
   $\{v,p(v)\} R^{(ii)} \{w,p(w)\}$  
  falls $\{v,w\} \in G-T$  
  und weder w Vorgänger von   
  v in T noch v Vorgänger von w  
  ($p(v) = p(w)$ möglich)  

  $R^{(iii)}$:  
  {u,v} $R^{(iii)}$ {v,w}
  falls v = p(w), u=p(v) und es gibt eine Kante in G-T, die einen Nachfolger von w mit einem Knoten verbindet, der kein Nachfolger von v ist.

$(R^{(i)}\cup R^{(ii)} \cup R^{(iii)})^{* } => R'$

Kantengraphen:  
G' = (E,R')
G'' = (E,$R^{(ii)} \cup R^{(iii)}$)  
Ausdünnen vermeidet quadratisch große Kantenmenge in Kantengraphen.
$|R^{(ii)}\cup R^{(iii)}| = O(E)$  

Äquivalenzklassen von ~ bzw. (R')*  
= Zusammenhangskomponenten von (E,(R')* )
z.z Zusammenhangskomponenten von (E,$R^{(i)}\cup R^{(ii)}\cup R^{(iii)}$)

#Vorlesung 11 17.1.20
Prüfungsgedöns:  
G29-218  
18-19.2  
24.3      
##------
aufspannender Baum T,  
Fundamentalzyklen bzgl. T -> R'    

Sequentieller Algorithmus  

Schritt 1:   
- Bestimme aufspannenden Baum T für G = (V,E) mit Explorationsalgorithmus mit linearer Laufzeit O(V+E)
- Nummeriere Knoten in preorder nach Bestimmung eines Wurzelknotens. Identifiziere Knoten mit preorder-Nummer.  
- Bestimme für jeden Knoten die Anzahl der Knoten im Unterbaum v -> nd(v) //nd = number of descendants

/////  
$nd(v_0) = \sum_{i=1}^k nd(v_i) + 1$
Aufsummieren der nd-Werte im unterbaum von v0  
/////

Schritt 2:
- Berechne für jeden Knoten v den kleinsten (bzgl. PREORDER) Knoten, der von v oder einem Baumnachfolger von v aus durch eine Kante in G-T erreichbar ist, oder Baumnachfolger von v ist.  
Nenne Knoten low(v).  
analog high(v).  
$low(v)= min(\{w|\{v,w\}\in G-T\} \cup \{v\} \cup \{low(u) | p(u) = v\})$
$high(v)= max(\{w|\{v,w\}\in G-T\} \cup \{v\} \cup \{high(u) | p(u) = v\})$  

Schritt 3:
- Konstruiere Graphen G''=(T,$R^{(ii)} \cup R^{(iii)}$)  
Für alle Kanten {w,v} $\in$ G-T mit v + nd(v) ≤ w füge Kante {{p(v),v},{p(w),w}} zu G'' hinzu.  
Für alle Kanten {v,w} aus T mit p(w)= v und v ≠1(V ≠ Wurzel) füge Kante {{v,p(v)},{v,w}} zu G'' hinzu, falls low(w)<v oder high(w) ≥ v + nd(v)

Schritt 4:  
- Bestimme die Zusammenhangskomponenten von G''  
Schritt 5:  
Erweitere CC im Kanten in G-T:
{v,w} $\in$ G-T wird CC von {p(w),w} zugeordnet, falls v<w.

insg.: O(V+E)
