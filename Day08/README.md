Program najprej prebere vhodno datoteko, kjer je vsaka vrstica zapisana kot trojica koordinat v prostoru (x, y, z). Te točke shrani v vektor struktur Point. Če v vhodu ni nobene točke, program izpiše ničelna rezultata in se zaključi.

Nato program ustvari vse možne povezave med pari točk. Za vsak par izračuna kvadrat evklidske razdalje in jo shrani skupaj z indeksoma točk v strukturo Edge. Kvadrat razdalje zadostuje, saj za primerjavo razdalj ni potrebno računati korena. Vse povezave se nato uredijo po naraščajoči razdalji.

Za nadaljnjo obdelavo program uporabi strukturo disjunktnih množic (Union-Find). Vsaka točka je na začetku v svoji komponenti. Obdelava povezav poteka po vrstnem redu naraščajočih razdalj in za vsako povezavo program preveri, ali povezuje dve različni komponenti. Če ju povezuje, se komponenti združita, število komponent pa se zmanjša.

V prvem delu se po obdelavi prvih 1000 povezav določi velikost vseh trenutno obstoječih komponent. Te velikosti se uredijo po padajočem vrstnem redu, nato pa se izračuna produkt treh največjih komponent. Ta vrednost predstavlja rezultat prvega dela.

Drugi del se zaključi v trenutku, ko so vse točke združene v eno samo komponento. Takrat program vzame točki, ki sta bili povezani z zadnjo uporabljeno povezavo, in kot rezultat drugega dela izračuna produkt njunih koordinat x.

Če se zgodi, da prvi del ni bil izračunan znotraj glavne zanke, se velikosti komponent izračunajo še enkrat po koncu obdelave povezav. Na koncu program izpiše rezultat prvega in drugega dela v ločenih vrsticah.