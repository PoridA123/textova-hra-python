Dungeon – textová RPG hra

Jednoduchá textová hra pro terminál napsaná v Pythonu. Jsi hrdina uvězněný v podzemí a musíš se dostat nahoru. Cestou bojuješ s nepřáteli, sbíráš předměty a nakonec čelíš obrovské potvoře.

Požadavky
Python 3.6+
Žádné externí knihovny (používá se jen random)
Spuštění
bash
python hra.py

Hru spouštěj v normálním terminálu (ne v Jupyter Notebooku), protože se ukončuje pomocí exit(0).

Ovládání
Vstup	Význam
W A S D	pohyb mezi místnostmi
F	v boji: útok pěstí
I	v boji: otevřít inventář
ano / ne	potvrzení výběru předmětu
zpet	zavřít inventář
Jak hra probíhá
Začátek – zadáš jméno a jdeš W do chodby, kde stojí obrovský muž (100 HP).
První souboj – po výhře můžeš získat nůž (+20 damage).
Velká místnost – tady se rozhoduješ, kam dál:
W – boj s dalším nepřítelem (150 HP), po výhře si vybereš jednu odměnu: meč (25 damage) nebo štít (50 % šance na blok).
A – finální boss (300 HP). Když ho porazíš, hra končí výhrou.
S – nic tam není, vrátíš se zpět.
D – schody na povrch, ale… je to past (konec hry – prohra).
Ve velké místnosti si také můžeš vzít lektvar a brnění (jednorázově).
Souboj

Boj je kolový. V každém kole zaútočíš ty a nepřítel ti hned oplatí – může se stát, že se zabijete navzájem v jednom kole.

Pěst – náhodný damage (1, 4, 12, 17, 19 nebo 25).
Zbraně (nůž, meč) – použiješ je z inventáře, dají pevný damage a dají se používat opakovaně.
Brnění – stačí vybavit jednou, platí do konce hry.
Štít – vybavíš jednou, platí do konce hry.
Lektvar – obnoví zdraví na 100, jde použít jen jednou.
Damage, který dostaneš od nepřítele
Vybavení	Damage za kolo
nic	1–7
brnění	1–4
štít	0–7 (přibližně 50 % šance na 0)
štít + brnění	0, 0, 3 nebo 4

Pokud zdraví klesne na 0, hra končí prohrou.

Struktura kódu
Funkce	Popis
zacatek()	úvod hry, jméno, první souboj
big_room()	hlavní místnost, výběr směru
lootchec()	nabídka lektvaru a brnění
loot_room()	výběr odměny po druhém bossovi
final()	finální souboj a konec hry
death()	falešný východ – prohra
fight()	smyčka souboje
utok()	útok pěstí
cyclus()	výpočet damage, který dostane hráč
storage() / pre_storage()	inventář a jeho kontrola
pohyb()	načtení pohybu W/A/S/D
smrt()	kontrola smrti hráče
Herní data

Stav hry je uložen v globálních seznamech: inventar, health, enemy_health, armor, shield, loot, loot_2, damage_storage, pohyb_storage.

