# GeoFA, releasenote X.XX



Version: X.XX

Dato: yyyy-mm-dd

Status: Kommende/ i proces/ udgivet

Tags: Indskriv stikord alfabetisk

Overordnet beskrivelse: Skriv en blød tekst her (et resume eller en introduktion), som forklarer hvad release noten indeholder, så man kan orientere sig om indholdet uden at læse hele dokumentet.



## Detaljeret beskrivelser (release details):



### Temanavn (temanummer)



#### Tilføjet:



#### Slettet:



#### Tilrettet:



#### Fejlrettelse:





\---



Følgende skabelontekst slettes før udgivelse af releasenoten



Hvis der **tilføjes et nyt tema** skrives:

Nyt tema med navnet ’Navn (temanummer)’ tilføjes til temagruppen ’Navn på temagruppe’.

Metadata:
* Temanavn: Skriv tekst
* Temakode: Skriv tekst
* Definition: Skriv tekst
* Beskrivelse: Skriv tekst
* Formaal: Skriv tekst
* Noegleord\_hovedgruppe: Skriv tekst
* Nogle\_ord: Skriv tekst
* Geometri type: Skriv tekst
* Lovgrundlag: Skriv tekst
* KLE\_koder: Skriv tekst

Registreringsvejledning:
* Registreringsinstruks: Skriv tekst
* Klassificering/opdeling: Skriv evt. tekst
* Minimum størrelser for objekt: Skriv evt. tekst
* Entydige objekter: Skriv evt. tekst
* Geometrisk konsistens mellem objekter: Skriv evt. tekst
* Geometrisk konsistens mellem objekter i andre datasæt: Skriv evt. tekst



**Eksempel**:

Nyt tema med navnet ’Kort til cykelplanlægning (5609)’ tilføjes til temagruppen ’Vej og trafik’.

Metadata:
* Temanavn: Kort til cykelplanlægning
* Temakode: 5610
* Definition: Et kortlag til at arbejde med planlægningen af cykelruter på tværs af administrative grænser.
* Beskrivelse: Der er mulighed for at arbejde med to typer af kort: et korridorkort (et oversigtskort, der viser de helt overordnede planer om nye ruteforbindelser mellem to punkter (f.eks. mellem to byer)) og et planlægningskort (et planlægningskort, med detaljerede angivelser af mulige vej- og stiforløb af ruteforbindelserne – med mulighed for at angive ruteforløb, alternative forløb og perspektivruter). Ofte vil kortet have en værdi ved planlægning af tværgående ruter, hvor data kan deles mellem de samarbejdende myndigheder. Dermed opbevares, udstilles og tilrettes data kun ét sted, så der er sikkerhed for, at der på tværs af deltagere arbejdes i det samme kort.
* Formaal: Formålet med kortet er at kunne arbejde på tværs af administrative grænser med planlægningen af cykelruter.
* Noegleord\_hovedgruppe: Cykelplanlægning
* Nogle\_ord: Cykelplanlægning
* Geometri type: Linje
* Lovgrundlag:
* KLE\_koder:
Registreringsvejledning:
* Registreringsinstruks: For begge planlægningskort bør følgende data registreres: rutetype og evt. undertype, om der er tale om et overordnet korridorkort eller et mere detaljeret planlægningskort samt endeligt detaljer om navn, nummer og beskrivelse/formål. For planlægningskortet kan yderligere detaljer om finansiering og prioritering tilføjes
* Klassificering/opdeling:
* Minimum størrelser for objekt:
* Entydige objekter:
* Geometrisk konsistens mellem objekter: Sørg for at sætte linjer for ruterne på den geografisk korrekte placering (stimidte, vejmidte eller vejkant fra GeoDanmark grunddata) og i forbindelse med stationeringspunkter (5611), hvis disse benyttes, så der dannes et samlet netværk.
* Geometrisk konsistens mellem objekter i andre datasæt: Har geografisk, topologisk sammenhæng med 5611 (stationeringspunkter) 



Hvis der **tilføjes et nyt felt/nye felter** skrives:

Temaet tilføjes følgende attributter/felter:



Feltnavn: teknisk navn

* Feltnavn10: teknisk navn i max. 10 tegn
* Formål og registreringsvejledning: Skriv tekst om formål, registreringsvejledning og evt. eksempler. Hvis der er tale om en systemoversættelse af en værdi, kan der skrives: Systemoversættes ud fra valgt kode vha. opslagsliste d\_navn\_navn (selve opslagslisten/opslagslisterne indskrives samlet efter alle felterne)
* Datatype: Tal/tegn/tekststreng
* Værdiområde: Angives
* Obligatorisk (0) / Frit (F) / Systemgenereret (S): O



**Eksempel**

Feltnavn: rutetype\_kode

* Feltnavn10: rutetype\_k
* Formål og registreringsvejledning: At angive hvilken type af rute, man planlægger for. Forklaring: Pt. der er kun muligt at planlægge for cykelruter, men på sigt kan flere rutetyper komme i spil. Værdi vælges fra opslagsliste d\_5809\_ty. Eksempel: 1
* Datatype: Tal
* Værdiområde: 1-3 cifre
* Obligatorisk (0) / Frit (F) / Systemgenereret (S): O



Hvis der **tilføjes en ny opslagsliste/nye udfaldsrum** i opslagsliste skrives:

Ovenstående implementering af felter suppleres med implementering af følgende opslagslister:



I opslagslisten ’d\_nummer\_navn’ tilføjes følgende udfaldsrum

* Indskriv\_navn\_type\_kode: angiv nummer
* Indskriv\_navn\_type: angiv navn/type
* Aktiv: 1
* Begrebsdefinition: Skriv tekst



**Eksempel**

I opslagslisten ’d\_5606\_inventar\_type’ tilføjes følgende udfaldsrum

* inventar\_type\_kode: 16
* inventar\_type: Fodhviler
* Aktiv: 1
* Begrebsdefinition: Installation til cyklister, som venter på grønt lys i cykelbyen. Cyklistgelænder kaldes den også. Her kan cyklisten støtte foden på fodstykket og tage et greb i gelænderet, så de er fri for at stige af sadlen, mens trafikken kører forbi.



Hvis der **tilføjes/ændres i ‘metadata’ eller ‘registreringsvejledning’** skrives dette til sidst – efter evt. opslagslister





**Generelle regler**

* Æ/Ø/Å – temaer må godt hedde navne med æ. ø. å, men ikke feltnavne og opslagslister, idet der er tale om navne på elementer i databasen, (fx tabelnavne: t\_born\_skole\_dis, kodelistenavne: d\_base\_trin, feltnavne: vedtaegt) 
* Temanavnet vil også have et teknisk navn t\_XXXX, som vores udvikler tildeles datasættet
* Opslagslister hedder altid: (d\_5710\_udd\_distrikt\_type) – altså d\_temalagsnummer\_valgt navn. Hvis listen er i de Standardiserede felter i datasæt specifikke datamodeller hedder opslagslisten altid d\_basis\_xxxx









