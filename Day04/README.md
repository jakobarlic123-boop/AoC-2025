Program najprej prebere celotno vhodno datoteko in jo shrani v dvodimenzionalno mrežo znakov. Vsaka vrstica predstavlja eno vrstico mreže, pri čemer znak @ označuje aktiven element, znak . pa prazno polje. Če je mreža prazna, program izpiše ničelna rezultata in se zaključi.

Za obdelavo sosednjih polj program uporabi tabeli dx in dy, ki opisujeta vseh osem možnih smeri okoli posamezne celice. Na ta način lahko enostavno preveri tudi diagonalne sosede.

V prvem delu program pregleda vsa polja mreže. Za vsako polje, ki vsebuje znak @, prešteje, koliko sosednjih polj v okolici prav tako vsebuje znak @. Če je takih sosedov manj kot štiri, se to polje upošteva pri rezultatu prvega dela.

V drugem delu program simulira postopno odstranjevanje elementov iz mreže. Najprej se izdela kopija začetne mreže, nato pa se v zanki ponavlja postopek: v vsakem koraku se poiščejo vsa polja z znakom @, ki imajo manj kot štiri sosednje @. Ta polja se zabeležijo in nato hkrati odstranijo iz mreže. Število odstranjenih polj v posameznem koraku se prišteje k rezultatu drugega dela.

Postopek se ponavlja, dokler v enem koraku ni več nobenega polja, ki bi izpolnjevalo pogoj za odstranitev. Takrat se simulacija zaključi. Končni rezultat drugega dela predstavlja skupno število vseh odstranjenih elementov skozi celoten proces.

Na koncu program izpiše rezultat prvega in drugega dela v ločenih vrsticah.