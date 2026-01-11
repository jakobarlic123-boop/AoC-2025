Program najprej prebere vhodno datoteko, kjer je vsaka vrstica zapisana kot par koordinat (x, y). Te točke shrani v vektor. Če je v vhodu manj kot dve točki, program nima kaj računati in izpiše ničelna rezultata.

V prvem delu program poišče največjo možno pravokotno površino, ki jo lahko določimo z dvema točkama. Za vsak par točk izračuna širino in višino pravokotnika kot absolutno razliko koordinat, povečano za ena, nato pa izračuna površino. Med vsemi pari se shrani največja najdena vrednost.

Drugi del je bistveno zahtevnejši. Ker so koordinate lahko velike, program najprej izvede koordinatno kompresijo. Vse različne x in y koordinate shrani v ločena seznama, ju uredi in odstrani podvojitve. Nato vsako originalno koordinato preslika v njen indeks v kompresiranem sistemu. S tem dobi manjšo mrežo, ki ohranja relativne položaje točk.

Na tej kompresirani mreži program nariše rob poligona, ki je določen z zaporedjem vhodnih točk. Robovi so ortogonalni, zato se rišejo bodisi navpično bodisi vodoravno. Tako nastane mreža, kjer so celice, ki ležijo na robu, posebej označene.

Sledi poplavno iskanje (flood-fill), s katerim program označi vse celice, ki pripadajo zunanjosti poligona. Začne se na robu mreže in se širi v vse smeri, razen čez rob poligona. Vse neoznačene celice, ki po tem postopku ostanejo, predstavljajo notranjost poligona.

Na podlagi tega program ustvari mrežo dovoljenih celic, kamor spadajo tako rob poligona kot njegova notranjost. Nad to mrežo izračuna 2D prefix vsote, kar omogoča hitro preverjanje, ali je določen pravokotnik v celoti znotraj dovoljenega območja.

V zadnjem koraku program ponovno pregleda vse pare točk. Za vsak par v kompresiranem koordinatnem sistemu preveri, ali je celoten pravokotnik med njima v celoti znotraj dovoljenega območja. Če je pogoj izpolnjen, izračuna dejansko površino pravokotnika v originalnih koordinatah in posodobi največjo vrednost.

Na koncu program izpiše rezultat prvega in drugega dela v ločenih vrsticah.