# -PR21JHKJNKSS
Repozitorij za predmet Podatkovno rudarjenje
Sama seminarska naloga se navezuje na zzamude potniških vlakov v Sloveniji v obdobju od januarja 2020 do oktobra 2021

Člani skupine:
- Jakob Horvat
- Klemen Jerman
- Nejc Kaluža
- Sebastjan Šibenik

### PREDSTAVITEV MNOŽICE PODATKOV 
-----

Naša množica podatkov, predstavlja zamude potniških vlakov v Sloveniji med Januarjem 2020 in Oktobrom 2021. Množica podatkov vsebuje 19268154 elementov. 

Za te podatke smo se odločili, saj se nam sami vlaki zdijo zanimivi in nas je tudi zanimalo če so same zamude res tako pogoste kot se nam je zdelo. 

Atribut | Opis      | Tip  |
--------|-----------|-------
timestamp | časovna značka, kdaj je bila zamuda | Time stamp
train_no | številka vlaka | Int
train_type | tip vlaka | Varchar
station_id | id postaje | Int
delay_type | tip zamude  | Char
delay | trajanje zamude | Int
station_name | ime postaje | String
lat | geografska širina  | Float
lng | geografska dolžina | Float
edge links from | id postaje od | Int
edge links to | id postaje do | Int

### PODROBEN OPIS PODATKOV
-----
Atrbiut train_type nam pove tip vlaka, seveda poznamo več različnih tipov, avtor podatkov je uporabil sledeče oznake:
oznaka | Opis      |
--------|-----------|
LP/LPV | lokalni vlak |
RG | regionalni vlak |
MO, MV, EC | internacionalni vlak |
en | internacionalni nočni vlak |
IC/ICS | InterCity vlak, InterCity Slovenia vlak |
AVT | avtovlak |
UNKNOWN | nedoločen tip vlaka |

Atrbiut delay_type nam pove tip zamude, seveda poznamo več različnih tipov, avtor podatkov je uporabil sledeče oznake:
oznaka | Opis      |
--------|-----------|
D | zamuda ob odhodu |
A | zamuda ob prihodu |
E | pričakovana zamuda |
