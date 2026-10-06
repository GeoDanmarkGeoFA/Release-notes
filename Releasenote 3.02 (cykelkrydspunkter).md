# GeoFA, releasenote 3.02



Version: 3.02

Dato: 2026-07-03

Status: Udgivet

Tags: Cykeldata, cykelkrydspunkt, cykelkrydspunktsstrækninger, rekreativt cykelnet

Overordnet beskrivelse: Dansk Kyst- og Naturturisme har i samarbejde med Nordiq Group evalueret de to datasæt Cykelkrydspunkter (5608) og Cykelkrydspunktsstrækninger (5609). Det har betydet kvalitative, små ændringer af datamodellen. Du kan læse mere om cykelnettet generelt her og konkret i forhold til GeoFA her



## Detaljeret beskrivelser (release details):



### Cykelkrydspunkter (5608)


#### Slettet:
Temaet slettes følgende attributter/felter:

Feltnavn: id_cykelkrydspunkt

* Feltnavn10: id_cykelkrydspunkt
* Formål og registreringsvejledning, og evt. eksempel: Unik identifikation af cykelkrydspunktet. Eksisterende cykelkrydspunkter er født med et genereret nummer fra ’dknt’. Nummeret består af tal. Hvis kommunerne tilføjer et nyt cykelknudepunkt, skal nummeret være unikt og kan sammensættes af Nummeret anvendes udelukkende til drift og svarer ikke til det skiltede nummer. Ved skiltning bruges i stedet ’kyrdspunktnummer’. Eksempel: XY1000[CL1.1]
* Datatype: Tegn
* Værdiområde: 1-25 cifre
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: refmain

* Feltnavn10: refmain
* Formål og registreringsvejledning, og evt. eksempel: Sikring af datamæssig sammenhæng i netværket. Et støttepunkt / mellemknudepunkt, der sættes som en del af en cykelstrækning, men som ikke har sit eget knudepunkt, tildeles et nummer, der referer til en hovedknude. Nummeret skal følge systematikken bag ”Metodehåndbog – fra planlægningsnetværk til digital visning”. Eksempel: 957DD8[CL2.1]
* Datatype: Tegn
* Værdiområde: 1-25 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F



#### Tilrettet:
Temaet tilrettes følgende attributter/felter:

Metadata:
* Temanavn: Cykelkrydspunkter
* Temakode: 5608
* Definition: Det rekreative cykelnet er er konceptuelt udviklet i et samarbejde mellem Dansk Kyst- og Naturturisme og Dansk Cykelturisme. Cykelnettet bliver implementeret i samarbejde med kommuner. Det er et cykelrutenetværk bestående af cykelkrydspunkter og cykelkrydspunktsstrækninger.
* Beskrivelse: Et nyt rekreativt cykelnet skal give rekreative cyklister bedre mulighed for at planlægge deres cykelture. Det skal styrke grundlaget for at øge fritids- og feriecyklismen og bidrage til at skabe en ny international konkurrence¬kraft for kyst- og naturturismen i Danmark.
* Formaal: Anvendes til visning og kvalificering af det rekreative cykelnet.
* Noegleord\_hovedgruppe: Cykelkrydspunkter
* Nogle\_ord: Cykelkrydspunkter
* Geometri type: Punkt
* Lovgrundlag: 
* KLE\_koder: 

Registreringsvejledning:
* Registreringsinstruks: Kortet under Vej og Trafik kaldes i daglig tale det rekreative cykelnet – teknisk kort.
Kortet er indlagt for hele Danmark af brugeren ’dknt’ med planstatus: 2 – planlagt samt off_kode:3
Når kommunerne har arbejdet med kortet og kvalificeret det til et færdigt digitalt netværk, skal kommunerne overtage ejerskab til data. Dette gøres ved:

    •	skrift ”cvr” fra ’dknt’ til kommunens cvr-nummer
    
    •	skift off_kode til 1: synligt for alle
    
    •	skift planstatus til 1: etableret.

* Klassificering/opdeling: 
* Minimum størrelser for objekt: 
* Entydige objekter: 
* Geometrisk konsistens mellem objekter: Sørg for at sætte punkter for cykelkrydspunkter på den geografisk korrekte placering i forbindelse med cykelkrydspunktsstrækninger, så der dannes et samlet netværk.
* Geometrisk konsistens mellem objekter i andre datasæt: Har geografisk, topologisk sammenhæng med 5609 (cykelkrydspunktsstrækninger)

Feltnavn: krydspunktsnummer

* Feltnavn10: kryds_nr
* Formål og registreringsvejledning, og evt. eksempel: Identifikation af krydspunktets skiltede navn (nummer). Numre er altid tocifrede, så de løber fra 01, 02 … til 98, 99. Krydspunkternes numre er unikke for et givent område, men ikke i hele Danmark. Der anbefales at være 25 km. (målt efter korteste rute) mellem to krydspunkter, der har samme nummer, så cyklisterne ikke bliver forvirrede. Nogle krydspunkter er enkle, andre er komplekse. Eksempler på sidstnævnte kunne være en rundkørsel, eller andre kryds, hvor der er mere end et muligt valg. Selv i komplekse krydspunkter skal de forskellige punkter, der udgør krydspunktet, nummereres ens. Punkter, der ligger tæt sammen og hedder det samme (har samme krydspunktsnummer), skal markeres som enten true ’1’ eller false ’0’ i feltet "primaerpunkt". Så det fremgår, hvilket et af punkterne, der er det primære. Eksempel: 47
* Datatype: Heltal
* Værdiområde: 2 cifre
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: beliggenhedskommune

* Feltnavn10: belig_kom
* Formål og registreringsvejledning, og evt. eksempel: Kommunenummer for den kommune, som cykelkrydspunktet er beliggende i. Kan hjælpe med at filtrere data ift. hvilke cykelkrydspunkter, der er i hvilke kommuner. Udfyldes automatisk hver nat i GeoFA af systemet ud fra en analyse mellem facilitetspunktet og DAGI-kommunegrænse. Eksempel: 850
* Datatype: Tal
* Værdiområde: 100-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: planstatus_kode

* Feltnavn10: planstat_k
* Formål og registreringsvejledning, og evt. eksempel: Kode for hvilken planmæssig status der er på objektet. Kan antage værdier fra opslagstabellen d_basis_ planstatus. Dvs 1 (Eksisterende: Er anlagt/i drift) og 2 (planlagt: Fremtid plan). Cykelkrydspunkterne er default indlagt med status 2. Skiftes til status 1, når cykelkrydspunktsnetværket er kvalificeret. Eksempel: 2
* Datatype: Heltal
* Værdiområde: d_basis_ planstatus
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: Planstatus

* Feltnavn10: planstat
* Formål og registreringsvejledning, og evt. eksempel: Systemmæssig oversættelse af den indtastede værdi i feltet planstatus_kode. Eksempel: Fremtid plan
* Datatype: Tekst
* Værdiområde: d_basis_ planstatus
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: primaerpunkt

* Feltnavn10: primar_pkt
* Formål og registreringsvejledning, og evt. eksempel: Vejvisning og kommunikation. Her angives, om et punkt er primært eller støttende. I simple krydspunkter med kun ét punkt er punktet altid primært. I kryds og rundkørsler, hvor flere punkter deler samme krydspunktsnummer, udpeges ét primært punkt, som de øvrige punkter støtter op om. Støttepunkter er vigtige for den datamæssige sammenhæng og for entydig vejvisning. Primærpunkt tildeles værdien ’1’. Støttepunkt tildeles værdien ’0’. Eksempel: 1
* Datatype: Boolean
* Værdiområde: False (0)/True (1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: blindt_punkt

* Feltnavn10: blindt_pkt
* Formål og registreringsvejledning, og evt. eksempel: Vejvisning og kommunikation. Hvis krydspunktet er et blindt punkt, hvorfra man skal cykle tilbage af samme vej, som man kom fra, angives dette her. Blindt punkt tildeles værdien ’1’. Andre krydspunkter (indgår som en del af det samlede netværk) tildeles værdien ’0’. Eksempel: 1
* Datatype: Boolean
* Værdiområde: False (0)/True (1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O


Feltnavn: afm_krydspunkt

* Feltnavn10: afm_kryds
* Formål og registreringsvejledning, og evt. eksempel: Vejvisning og kommunikation. Angiver om et krydspunkt er afmærket med skiltning i den fysiske virkelighed eller ej. I krydspunkter med flere punkter (et primært og op til flere støttepunkter) tildeles alle punkterne samme værdi i dette felt. Krydspunkter, som er skiltede, tildeles værdien ’1’. Krydspunkter, som ikke er skiltede, tildeles værdien ’0’. Eksempel: 1
* Datatype: Boolean
* Værdiområde: False (0)/True (1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: note

* Feltnavn10: note
* Formål og registreringsvejledning, og evt. eksempel: Mulighed for at angive ekstra kommentarer til cykelkrydspunktet. Felt stammer fra 3. Generel datamodel. Eksempel: Supplerende beskrivelse af cykelkrydspunktet
* Datatype: Tekststreng
* Værdiområde: 1-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F





## Detaljeret beskrivelser (release details):



### Cykelkrydspunktsstrækninger (5609)

#### Tilrettet:

Temaet tilrettes følgende attributter/felter:

Metadata:
* Temanavn: Cykelkrydspunktsstrækninger 
* Temakode: 5609
* Definition: Det rekreative cykelnet er er konceptuelt udviklet i et samarbejde mellem Dansk Kyst- og Naturturisme og Dansk Cykelturisme. Cykelnettet bliver implementeret i samarbejde med kommuner. Det er et cykelrutenetværk bestående af cykelkrydspunkter og cykelkrydspunktsstrækninger.
* Beskrivelse: Et nyt rekreativt cykelnet skal give rekreative cyklister bedre mulighed for at planlægge deres cykelture. Det skal styrke grundlaget for at øge fritids- og feriecyklismen og bidrage til at skabe en ny international konkurrence¬kraft for kyst- og naturturismen i Danmark.
* Formaal: Anvendes til visning og kvalificering af det rekreative cykelnet
* Noegleord\_hovedgruppe: Cykelkrydspunktsstrækninger
* Nogle\_ord: Cykelkrydspunktsstrækninger
* Geometri type: Linje
* Lovgrundlag: 
* KLE\_koder: 

Registreringsvejledning:
* Registreringsinstruks: Kortet under Vej og Trafik kaldes i daglig tale det rekreative cykelnet – teknisk kort.
Kortet er indlagt for hele Danmark af brugeren ’dknt’ med planstatus: 2 – planlagt samt off_kode:3
Når kommunerne har arbejdet med kortet og kvalificeret det til et færdigt digitalt netværk, skal kommunerne overtage ejerskab til data. Dette gøres ved:

    •	skrift ”cvr” fra ’dknt’ til kommunens cvr-nummer

    •	skift off_kode til 1: synligt for alle

    •	skift planstatus til 1: etableret.

* Klassificering/opdeling: 
* Minimum størrelser for objekt: 
* Entydige objekter: 
* Geometrisk konsistens mellem objekter: Sørg for at sætte linjer for cykelkrydspunktsstrækninger på den geografisk korrekte placering (stimidte, vejmidte eller vejkant fra GeoDanmark grunddata) og i forbindelse med cykelkrydspunkter, så der dannes et samlet netværk.
* Geometrisk konsistens mellem objekter i andre datasæt: Har geografisk, topologisk sammenhæng med 5608 (cykelkrydspunkter)

Feltnavn: beliggenhedskommune

* Feltnavn10: belig_kom
* Formål og registreringsvejledning, og evt. eksempel: Kommunenummer for den kommune, som cykelkrydspunktsstrækningen er beliggende i. Kan hjælpe med at filtrere data ift. hvilke cykelkrydspunktsstrækninger, der i hvilke kommuner. Udfyldes automatisk hver nat i GeoFA af systemet ud fra en analyse mellem facilitetspunktet og DAGI-kommunegrænse. Eksempel: 850
* Datatype: Tal
* Værdiområde: 100-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: planstatus_kode

* Feltnavn10: planstat_k
* Formål og registreringsvejledning, og evt. eksempel: Kode for hvilken planmæssigstatus der er på objektet. Kan antage værdier fra opslagstabellen d_basis_ planstatus. Dvs 1 (Eksisterende: Er anlagt/i drift) og 2 (planlagt: Fremtid plan). Cykelkrydspunktsstrækningerne er default indlagt med status 2. Skiftes til status 1, når cykelnettet er kvalificeret. Eksempel: 2
* Datatype: Heltal
* Værdiområde: d_basis_ planstatus
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: planstatus

* Feltnavn10: planstat
* Formål og registreringsvejledning, og evt. eksempel: Systemmæssig oversættelse af den indtastede værdi i feltet planstatus_kode. Eksempel: Fremtid plan
* Datatype: Tekst
* Værdiområde: d_basis_ planstatus
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: privatvej

* Feltnavn10: privatvej
* Formål og registreringsvejledning, og evt. eksempel: Vejvisning og kommunikation. Angiver hvorvidt en strækning mellem to krydspunkter fører over private arealer. Oftest ikke tilfældet, men markeres, når det forekommer. Hvis strækningen fører over privatejede arealer angives dette med '1'. Hvis strækningen udelukkende fører over offentlige arealer angives dette med '0’. Eksempel: 1
* Datatype: Boolean
* Værdiområde: False (0)/True (1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: asfalteret

* Feltnavn10: asfalteret
* Formål og registreringsvejledning, og evt. eksempel: Vejvisning og kommunikation. Angiver hvorvidt der er fast belægning på hele strækningen. Er hele strækningen asfalteret angives dette med '1'. Er hele eller dele af strækningen med grus-underlag angives dette med '0'. Eksempel: 1
* Datatype: Boolean
* Værdiområde: False (0)/True (1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: ensrettet

* Feltnavn10: ensrettet
* Formål og registreringsvejledning, og evt. eksempel: Vejvisning og kommunikation. Angiver om, der er ensrettet på hele eller dele af strækningen mellem to cykelknudepunkter. Hvis hele eller dele af strækningen er ensrettet, angives dette med '1'. Hvis hele strækningen er to vejs (ikke ensrettet noget sted) angives dette med '0'. Eksempel: 1
* Datatype: Boolean
* Værdiområde: False (0)/True (1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: note

* Feltnavn10: note
* Formål og registreringsvejledning, og evt. eksempel: Mulighed for at angive ekstra kommentarer til cykelkrydspunktsstrækningen. Felt stammer fra 3. Generel datamodel. Eksempel: Supplerende beskrivelse af cykelknudepunktsstrækningen.
* Datatype: Tekststreng
* Værdiområde: 1-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F






\---
