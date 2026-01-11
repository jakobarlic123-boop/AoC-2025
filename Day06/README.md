Program najprej prebere celotno vhodno datoteko in shrani vse vrstice v vektor nizov. Ker imajo lahko vrstice različno dolžino, program najprej poišče največjo širino in vse vrstice razširi na to dolžino z znaki za presledek. Na ta način si zagotovi pravokotno mrežo znakov, ki jo je lažje obdelovati po stolpcih.

V naslednjem koraku program poišče tako imenovane bloke. Blok je zaporedje stolpcev, kjer vsaj v eni vrstici obstaja znak, ki ni presledek. Stolpci, ki so v celoti prazni, služijo kot ločila med bloki. Program gre po stolpcih od leve proti desni in za vsak zaporedni ne-prazen odsek shrani začetni in končni indeks stolpca.

Za vsak najden blok program izvede izračun za prvi in drugi del naloge. Najprej v spodnji vrstici bloka poišče operator, ki je lahko + ali *. Ta operator določa, ali se bodo vrednosti seštevale ali množile.

V prvem delu se blok obdeluje po vrsticah. Iz vsake vrstice nad zadnjo vrstico se izreže del, ki pripada trenutnemu bloku, odstrani se odvečne presledke in, če niz ni prazen, pretvori v število. Ta števila se nato združujejo glede na operator bloka, rezultat pa se prišteje k skupnemu rezultatu prvega dela.

V drugem delu se isti blok obdeluje po stolpcih. Za vsak stolpec v bloku program prebere znake po vrsticah in sestavi število iz zaporednih cifer. Če v stolpcu ni nobene števke, se ta preskoči. Dobljene vrednosti se ponovno združujejo glede na operator in seštejejo v končni rezultat drugega dela.

Na koncu program izpiše skupni rezultat prvega in drugega dela v ločenih vrsticah.