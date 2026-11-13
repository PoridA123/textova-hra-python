Projekt Python Text Based Hra

Textová hra v Pythonu, kterou hraješ přímo v terminálu. Probouzíš se v podzemí a tvým cílem je dostat se na povrch. Cestou bojuješ s nepřáteli, sbíráš zbraně i výbavu a rozhoduješ se, kudy půjdeš dál.

Obsah
O hře
Jak hru spustit
Ovládání
Předměty
Tipy
Autor
O hře
Hraješ za hrdinu, který uvízl v podzemí.
Pohybuješ se po místnostech pomocí kláves W, A, S, D.
Bojuješ s nepřáteli, kteří ti mohou v boji také ublížit.
Sbíráš předměty (zbraně, štít, brnění, lektvar) a vybíráš si, co použiješ.
Hra končí výhrou, nebo prohrou (například když ti klesne zdraví na 0).
Jak hru spustit
Nainstaluj Python 3 – stáhneš ho na python.org.
Stáhni projekt (nebo ho naklonuj):
bash
   git clone https://github.com/PoridA123/textova-hra-python.git
Přejdi do složky projektu:
bash
   cd textova-hra-python
Spusť hru:
bash
   python projekt.txt

Na některých systémech místo python použij python3.

Hru spouštěj v terminálu, ne v Jupyter Notebooku (hra používá exit(0)).

Ovládání

Vše zadáváš psaním do terminálu a potvrzuješ klávesou Enter.

Situace	Co zadáš
Začátek hry	své jméno
Pohyb po místnostech	W, A, S, D
V boji	F – útok pěstí, I – otevřít inventář
V inventáři	název předmětu (např. mec), nebo zpet
Otázky ano/ne	ano nebo ne
Výběr odměny v místnosti	mec nebo shield
Předměty
Předmět	Účinek
nuz	útok se 20 damage
mec	útok s 25 damage
shield	snižuje damage, který dostaneš
armor	snižuje damage, který dostaneš
potion	obnoví zdraví na 100
Tipy
Zbraň (nuz, mec) musíš v inventáři používat při každém útoku znovu a při jejím použití dostaneš také damage.
armor stačí použít jednou, platí do konce hry.
potion se dá použít jen jednou.
V jedné z místností si můžeš vzít jen jednu věc, rozmysli se dobře.
Ne každá cesta vede k cíli, a ne každá je bezpečná.
Autor

PoridA123 – github.com/PoridA123
