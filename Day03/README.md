Program najprej odpre vhodno datoteko in jo bere po vrsticah. Vsaka vrstica predstavlja zaporedje števk, iz katerega je potrebno izbrati določeno število števk tako, da dobljeno število postane čim večje. V prvem delu se iz vsake vrstice izbereta 2 števki, v drugem delu pa 12 števk. Pomembno je, da se ohrani vrstni red števk, izbira pa je dovoljena kjerkoli znotraj zapisa.

Glavna logika izbire je implementirana v funkciji bestKDigits. Funkcija prejme niz števk in število k, ki pove, koliko števk mora izbrati. Če je k večji ali enak dolžini niza, funkcija preprosto pretvori celoten niz v število in ga vrne.

V splošnem primeru funkcija uporablja požrešen pristop. Števke izbira postopoma, eno po eno. Pri vsakem koraku pregleda del niza, kjer je še dovolj preostalih znakov, da lahko izbere vseh k števk. Med temi znaki poišče največjo možno števko in jo doda v rezultat. Nato nadaljuje iskanje za naslednjo števko za mestom, kjer je bila izbrana prejšnja. Na ta način funkcija zagotovi, da je končno število čim večje, hkrati pa ohrani vrstni red števk.

Ko so vse izbrane števke zbrane v niz, se ta pretvori v število tipa long long in vrne kot rezultat funkcije.

V funkciji main se vsaka prebrana vrstica obdela dvakrat: enkrat za prvi del z izbiro dveh števk in enkrat za drugi del z izbiro dvanajstih števk. Dobljeni rezultati se sproti seštevajo v ločenih spremenljivkah. Na koncu program izpiše obe vsoti, vsako v svoji vrstici.