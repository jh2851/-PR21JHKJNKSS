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


Prva tabela prikazuje število zamud glede na posamezen mesec v letu. 
Vertikalna os prikazuje količino zamud, druga pa mesec v letu označen z številko. 
Opazno je, da je več zamud v poletnih in zgodnjih jesenskih mesecih in sicer 
največ avgusta in septembra. Ti rezultati so neskladni z našimi pričakovanji, 
saj smo predhodno ocenili, da bo največ zamud v zimskem delu meseca zaradi 
potencialnih neugodnih vremenskih razmer.

![vsi_delays](./Grafi/vsi_delays.png?raw=true)


Drugi diagram prikazuje število zamud tipa D (zamude v odhodu) glede na posamezen 
mesec v letu. Rezultati so zelo podobni tistim na prvem grafu, le da je bilo največ 
zamud tipa D v mesecu septembru, najmanj pa v mesecih november in december.

![D_delays](./Grafi/D_delays.png?raw=true)


Tretji diagram prikazuje število zamud tipa A (zamude v prihodu) glede na posamezen 
mesec v letu. Največ zamud tipa A je bilo meseca avgusta, najmanj pa novembra 
in decembra.

![a_delays](./Grafi/a_delays.png?raw=true)


Četrti diagram prikazuje število zamud tipa E (pričakovane zamude) glede na posamezen 
mesec v letu. Tudi tukaj prevladujejo zamude v mesecu avgustu, je pa njihova 
količina nekoliko nižja v septembru, kot pri ostalih zamudah. Opazno nižje so tudi 
v mesecih november in december.

![e_delays](./Grafi/e_delays.png?raw=true)


Ta slika prikazuje še črtni diagram za boljšo predstavo o razlikah med posameznimi 
tipi zamud. Opazimo lahko, da izrazito prevladujejo zamude v odhodu, med tem ko so 
ostali tipi zamud opazno nižji.

![vsi_delays_bolsi](./Grafi/vsi_delays_bolsi.png?raw=true)


Slika prikazuje količino zamud tipa D glede na različne modele vlakov. V zamudah 
tipa D močno prevladujesta vlak tipa LPV in LP, ki pa spadata pod počasnejše 
lokalne vlake. Zelo mogoče je, da so rezultati takšni kot so, ker je 
takih potniških vlakov največ.

![delays_a_vlaki](./Grafi/delays_a_vlaki.png?raw=true)


Slika prikazuje količino zamud tipa A glede na različne modele vlakov. 
Razvidno je, da je največ zamud pri tipu vlaka EC, ta pa spada v skupino 
internacionalnih vlakov. Visoke količine zamud so opazne tudi pri vlakih LP in LPV. 
Najmanj zamud povzročajo internacionalni vlak MO in hitri vlak ICS.

![delays_d_vlaki](./Grafi/delays_d_vlaki.png?raw=true)


Slika prikazuje količino zamud tipa E glede na različne modele vlakov. 
Najbolj prevladujejo vlaki tipa LP in LPV

![delays_e_vlaki](./Grafi/delays_e_vlaki.png?raw=true)


Tortni diagram prikazuje 10 glavnih postaj z največjimi količinami zamud.

![postaje_delays](./Grafi/postaje_delays.png?raw=true)



