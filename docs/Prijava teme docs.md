HIKU - Aplikacija za pohodnike

Člani: Manca Vavpotič, Andraž Klobučar, Filip Gros

Številka projektne skupine: 20

Opis:  
Spletna in mobilna aplikacija, ki pohodnikom omogoča iskanje planinskih poti, beleženje svojega napredka in osvojenih vrhov ter deljenje utrinkov iz pohodov med uporabniki. Ponuja moderno rešitev po zgledu že obstoječih aplikacij z dodatnimi funkcionalnostmi za boljšo interaktivnost in digitalno planinsko knjižico. Prav tako bi aplikacija spodbujala poročanje aktualnega stanja na poteh.

Ogrodje in razvojno okolje:
Izbrali bomo naslednje tehnologije:
Mikrostoritveno ogrodje: KumuluzEE, ogrodje za razvoj mikro storitev v Javi. Omogoča modularno arhitekturo, neodvisno delovanje storitev in enostavno integracijo z bazami in sporočilnimi sistemi.
Podatkovna baza: PostgreSQL. Relacijska podatkovna baza z visoko zmogljivostjo.
Zaledje: programski jezik Java in ogrodje Spring Boot, ki omogoča izdelavo REST API-jev in zalednih funkcionalnosti.
Čelni del: React native. Framework za razvoj mobilnih aplikacij za iOS in Android. Podpira dinamične uporabniške vmesnike in enostavno povezavo z backend API-ji.
Sporočilni posrednik med mikro storitvami: RabbitMQ. Sistem za asinhrono sporočanje med mikro storitvami.
Orodje za CI/CD: GitHub Actions. Podpira avtomatizacijo gradnje, testiranja in nameščanja aplikacij. 
Namestitev v oblaku: Azure. Ponuja oblačno infrastrukturo za gostovanje mikrostoritev, podatkovnih baz in sporočilnih sistemov. Omogoča skalabilnost, visoko razpoložljivost in enostavno upravljanje z viri.
Centralizirano beleženje dnevnikov: Fluentd. Omogoča strukturirano zbiranje in obdelavo dnevnikov iz različnih virov.
Zbiranje metrik: Prometheus, ki zbira metrike delovanja aplikacije, kot so CPU, pomnilnik, odzivnost API-jev in število zahtevkov.
Vizualizacija: Grafana
Prikazuje metrike v grafih, tabelah in nadzornih ploščah.
Sistem za nadzor verzij: Git(hub)
Kontejnerizacija: Docker, ki je platforma za ustvarjanje in izvajanje aplikacij v kontejnerjih. Pakira aplikacijo skupaj z vsemi odvisnostmi, zagotavlja delovanje v različnih okoljih (lokalno, test, produkcija).
Orkestracija / nameščanje: Kubernetes, ki je sistem za avtomatizirano orkestracijo kontejnerjev.


Shema arhitekture:

Seznam funkcionalnosti mikrostoritev:	

1. Avtentikacija (Authentication Service)
Dodelitev in preverjanje JWT žetonov,
Upravljanje prijave,
Nadzor dostopa glede na uporabniško vlogo.

2. Uporabniški profili (User Service)
Upravljanje uporabniškega profila (podatki o uporabniku, nastavitve),
Upravljanje odnosov med sledilci in funkcionalnost sledenja.

3. Vrhovi in poti (Peaks and Hikes Service)
Iskanje poti in vrhov,
Shranjevanje in prikaz informacij o poteh,
Podatki o trenutnem stanju na poti,
Shranjevanje in prikaz mnenj in komentarjev o poteh.

4. Vremenski podatki (Weather Service)
Komunikacija z zunanjim API za pridobivanje vremenskih podatkov,
Generiranje opozoril glede na vremsko stanje.

5. Statistika in dosežki (Stats and Achievements Service)
Izračun in beleženje statistike o pohodih,
Hranjenje digitalne planinske knjižice,
Beleženje dosežkov.

6. Beleženje osvojenih vrhov (Badge Service)
Beleženje osvojenih vrhov v planinsko knjižico,
Validacija GPS lokacije ob beleženju.

7. Lestvice in izzivi (Scoreboards and Challenges Service)
Prikaz lestvic dosežkov uporabnikov,
Prikaz podatkov o izzivih in trenutni napredek,
Izračun rezultatov na podlagi statistik posameznikov.

8. Obvestila (Notification Service)
Upravljanje z obvestili,
Pošiljanje opozoril.

9. Ogled aktivnosti (Social Feed Service)
Ustvarjanje in prikaz objav profilov, katerim uporabnik sledi,
Objava slik in utrinkov s pohodov,
Avtomatizirane objave za dosežke uporabnikov,
Novice in oglasi.
Primeri uporabe:
Digitalna planinska knjižica
Andraž se je ponedeljek zgodaj zjutraj odpravil na Škrlatico. Vrh je dosegel ob 14.uri. Ker so bile na vrhu razmere dovolj ugodne za uporabo telefona, je prižgal na telefonu lokacijske storitve, odprl HIKU aplikacijo, posnel sliko razgleda iz vrha in zabeležil svoj dosežek.

Oglasna deska za pohode in Google maps
Manca v četrtek opazi ugodno vremensko napoved za vikend. Ne želi se sama odpraviti v hribe, zato odpre aplikacijo HIKU, kjer opazi zadnjo objavo skupine FRI Hribolazci, ki ji sledi. Filip vabi vse zainteresirane, da v soboto ob 9.00 vsi odrinejo izpred Merkatorja v Podlubniku na Lubnik. Ker Manca ne ve, kje je to, klikne gumb, ki jo preumseri na aplikacijo Google Maps, ki jo bo v soboto pripeljala na izhodišče. Tako si lahko načrtuje sobotni dan in se v petek označi, da se bo pridružila pohodu.
 
Izbira planinske poti in aktualno stanje, vreme
Filipu in Manci se v soboto pridruži še Andraž, ki ni član skupine. Informacijo za pohod je dobil v zahviku aplikacije za ogled aktivnosti (social feed). Filip odpre aplikacijo in najde sedem možnih poti do vrha. Prav tako aplikacija trdi, da je vreme primeno za izbiro katerekoli izmed njih. Skupaj se odločijo, da se bodo povzpeli po Severozahodnem grebenu / Kurirski poti. Pogledajo še objavo izpred dveh tednov, da je s potjo vse v redu. Po pol ure hoje slišijo motorno žago in za ovinkom opazijo zaporo poti zaradi varnosti planincev. Filip s pomočjo aplikacije najde alternativno pot čez Stari grad. Ko prispejo na vrh vsi z veseljem vnesejo doseženi vrh v digitalno knjižico. Aplikacija Filipa vpraša, po kateri poti je prišel na vrh. Spomni se zapore in objavi komentar v zavihku: Aktualno stanje poti. Andražu je bila družba všeč, zato se pridruži skupini. Prijatelja klikneta kljukico ob komentraju, tako da lahko vsi uporabniki aplikacije vidijo, da so vsaj tri osebe potrdile kredibilnost komentarja.

Skupine in Lestvice
Bivši Študent FRIja Kristjan si je v nedeljo naložil aplikacijo. V iskalnik vpiše Lubnik in opazi, da so FRI Hribolazci nazadnje dosegli vrh v soboto. Klikne na skupino in na desni strani aplikacije se mu prikaže lestvica uspeha vseh njenih članov. Znotraj skupine je sedaj najuspešnejši Andraž, ki je v tem tednu osvojil dva vrhova, sledita pa mu Filip in Manca. Spremeni časovni okvir in vidi, da je v zadnjih dvanajstih mesecih člani skupine osvojili 15, 14 in 10 vrhov. Na podlagi opisa in statističnih podatkov se Kristjan pridruži skupini.

Izzivi
Kristjan si želi večkrat v hribe, zato se pridruži izzivu, da se bo v naslednjih treh mesecih vsaj šestkrat povzpel na katerega izmed vrhov. Ker Andraž in Filip prav tako opravljata ta izziv računa, da ga bo lažje opravil.


