# GeoFA, releasenote 3.03



Version: 3.03

Dato: 2026-07-03

Status: udgivet

Tags: Bevaringsværdige bygninger

Overordnet beskrivelse: Nye tabeller til vurdering af bevaringsværdige bygninger i GeoFA. Der findes en tabel (6205) til vurdering af enkeltbygninger og en tabel (6204) der anvendes til at gruppere enkeltvurderingerne. Tabellen til bygningsvurderingen indeholder de felter som indgår i en såkaldt SAVE-registrering og tabellen kan således rumme de data, der hidtil har ligget i Slots- og Kulturstyrelsen database for fredede og bevaringsværdige bygninger (FBB)



## Detaljeret beskrivelser (release details):



### Bygningsvurderingsgruppe (6204)



#### Tilføjet:
Nyt tema med navnet ’Bygningsvurderingsgruppe (6204)’ tilføjes til temagruppen ’Planlægning’.

Metadata:
* Temanavn: Bygningsvurderingsgruppe
* Temakode: 6204
* Definition: Gruppe af bygninger der ud fra relevante fællestræk (fx bygningstype, historie eller geografisk afgrænsning) har gennemgået en vurdering af bevaringsværdien.
* Beskrivelse: Ved vurdering af bygningers bevaringsværdi kan der oprettes en gruppe, som består af bygninger, der har et fælles tema (fx mejerier, stationer eller herregårde) eller som har en geografisk sammenhæng i form af et afgrænset område (fx en landsby eller en bydel). 
* Formaal: Bygningsvurderingsgruppen bliver ikke i sig selv vurderet eller karaktersat, men har alene til formål at sammenknytte en relevant samling af vurderede bygninger. En vurderet bygning kan høre til flere bygningsvurderingsgrupper.
* Noegleord\_hovedgruppe: Bevaringsværdige bygninger
* Nogle\_ord: Områdeafgrænsning, Bygningstema, Bebygget miljø, Kulturmiljø, Bebygget struktur, Baevaringsværdi.
* Geometri type: Polygon
* Lovgrundlag:
* KLE\_koder: 01.10.00 (Bygningsfredning og bygningsbevaring i almindelighed)

Registreringsvejledning:
* Registreringsinstruks: Bygningsvurderingsgruppen oprettes med navn og geometri, og der tilknyttes relevante bygninger til gruppen. Der kan indsættes kommentarer og fotos på gruppeniveau. Der kan henvises til eksterne sager eller planer som fx bevarende lokalplaner.
* Klassificering/opdeling: Der findes ingen klassificering af bygningsvurderingsgruppen
* Minimum størrelser for objekt: 0,1 m 
* Entydige objekter: -
* Geometrisk konsistens mellem objekter: Anvend gerne den konkrete polygon som gruppen henviser til - fx når der er tale om en lokalplanafgrænsning.
* Geometrisk konsistens mellem objekter i andre datasæt: Gruppen bør i videst muligt omfang have en geometri, der omfatter de bygninger, som indgår i gruppen - fx ved en lokalplanafgrænsning. Den geometriske afgrænsning kan dog være kompleks i tilfælde af grupper med en temamæssig sammenhæng mellem bygninger (fx stationsbygninger i forskellige byer i kommunen) - i sådanne tilfælde kan man oprette en geometri som blot omfatter en enkelt af de tilknyttede bygninger.

Temaet tilføjes følgende attributter/felter: 

Feltnavn: objekt_id

* Feltnavn10: objekt_id
* Formål og registreringsvejledning, og evt. eksempel: Entydig databasenøgle over tid. Eksempel: E6AB20EA-67E4-4C11-A051-B50A084788A3
* Datatype: UUID (128 bit)
* Værdiområde: 16 bytes
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: versions_id

* Feltnavn10: version_id
* Formål og registreringsvejledning, og evt. eksempel: Unik versions-id databasenøgle. Eksempel: E6AB20EA-67E4-4C11-A051-B50A084788A3
* Datatype: UUID (128 bit)
* Værdiområde: 16 bytes
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: systid_fra

* Feltnavn10: systid_fra
* Formål og registreringsvejledning, og evt. eksempel: Start systemtid. Eksempel: 2006-12-31T23:59:00.000+01:00
* Datatype: ISO date/tid
* Værdiområde: 2006-12-31T23:59:00.000+01:00 – 2999-12-31T23:59:00.000+01:00
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: systid_til

* Feltnavn10: systid_til
* Formål og registreringsvejledning, og evt. eksempel: Slut systemtid. Eksempel: 2006-12-31T23:59:00.000+01:00
* Datatype: ISO date/tid
* Værdiområde: 2006-12-31T23:59:00.000+01:00 – 2999-12-31T23:59:00.000+01:00
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: oprettet

* Feltnavn10: oprettet
* Formål og registreringsvejledning, og evt. eksempel: Systemtid for objektets oprettelse. Eksempel: 2006-12-31T23:59:00.000+01:00
* Datatype: ISO date/tid
* Værdiområde: 2006-12-31T23:59:00.000+01:00 – 2999-12-31T23:59:00.000+01:00
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: cvr_kode

* Feltnavn10: cvr_kode
* Formål og registreringsvejledning, og evt. eksempel: CVR-kode på ansvarlig myndighed. Eksempel: 29189641
* Datatype: Heltal
* Værdiområde: 10000000-99999999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S/(O)

Feltnavn: cvr_navn

* Feltnavn10: cvr_navn
* Formål og registreringsvejledning, og evt. eksempel: CVR-navn på ansvarlig myndighed. Eksempel: Silkeborg Kommune
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: kommunekode

* Feltnavn10: kommu_kode
* Formål og registreringsvejledning, og evt. eksempel: 3-cifret kommunenummer for den kommune der har oprettet registreringen. Eksempel: 740
* Datatype: Heltal
* Værdiområde: 100-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: bruger_id

* Feltnavn10: bruger_id
* Formål og registreringsvejledning, og evt. eksempel: Brugernavn ved opdatering. Eksempel: Silkeborg1234
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S/(O)

Feltnavn: oprindkode

* Feltnavn10: oprindkode
* Formål og registreringsvejledning, og evt. eksempel: Kode for oprindelse for objekt. Eksempel: 1
* Datatype: Heltal
* Værdiområde: 0-11
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: oprindelse

* Feltnavn10: oprindelse
* Formål og registreringsvejledning, og evt. eksempel: Oprindelse for objekt. Eksempel: Ortofoto
* Datatype: Tekststreng
* Værdiområde: 0-35
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: statuskode

* Feltnavn10: statuskode
* Formål og registreringsvejledning, og evt. eksempel: Kode for gældende status. Eksempel: 3
* Datatype: Heltal
* Værdiområde: 0-4
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: status

* Feltnavn10: status
* Formål og registreringsvejledning, og evt. eksempel: Gældende status. Eksempel: Gældende/ Vedtaget
* Datatype: Tekststreng
* Værdiområde: 0-30
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: off_kode

* Feltnavn10: off_kode
* Formål og registreringsvejledning, og evt. eksempel: Kode for Tilgængelighed. Eksempel: 1
* Datatype: Heltal
* Værdiområde: 1-3 (default = 1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: offentlig

* Feltnavn10: offentlig
* Formål og registreringsvejledning, og evt. eksempel: Tilgængelighed. Eksempel: Synlig for alle
* Datatype: Tekststreng
* Værdiområde: 0-60
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: noegle

* Feltnavn10: noegle
* Formål og registreringsvejledning, og evt. eksempel: Fremmed nøgle til objektet i en anden databasetabel. Eksempel: 12853468A
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: note

* Feltnavn10: note
* Formål og registreringsvejledning, og evt. eksempel: Notering af forhold som har betydning for gruppen. Eksempel: Gruppen omfatter ikke den nye hal mod nord.
* Datatype: Tekststreng
* Værdiområde: 0-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geometri

* Feltnavn10: geometri
* Formål og registreringsvejledning, og evt. eksempel: Geometrisk beskrivelse af objekt. Eksempel: For et punkt: 543210,999 6123456,111
* Datatype: Punkt, Linje, Flade
* Værdiområde: X: -370.000,000-1.777.483,999, Y: 5.200.000,000-7.347.483,999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: gyldig_fra

* Feltnavn10: gyldig_fra
* Formål og registreringsvejledning, og evt. eksempel: Start gyldighedsperiode. Eksempel: 2006-12-31
* Datatype: ISO date
* Værdiområde: 2006-12-31 – 2999-12-31
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: gyldig_til

* Feltnavn10: gyldig_til
* Formål og registreringsvejledning, og evt. eksempel: Slut gyldighedsperiode. Eksempel: 2006-12-31
* Datatype: ISO date
* Værdiområde: 2006-12-31 – 2999-12-31
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link

* Feltnavn10: link
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link1

* Feltnavn10: link1
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link2

* Feltnavn10: link2
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link3

* Feltnavn10: link3
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto

* Feltnavn10: geofafoto
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Feltet vil blive brugt til det primære foto for objektet sat i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto1

* Feltnavn10: geofafoto1
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto2

* Feltnavn10: geofafoto2
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto3

* Feltnavn10: geofafoto3
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto4

* Feltnavn10: geofafoto4
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto5

* Feltnavn10: geofafoto5
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto6

* Feltnavn10: geofafoto6
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto7

* Feltnavn10: geofafoto7
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto8

* Feltnavn10: geofafoto8
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto9

* Feltnavn10: geofafoto9
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: sagsnr

* Feltnavn10: sagsnr
* Formål og registreringsvejledning, og evt. eksempel: Identifikation af sag i ESDH. Eksempel: 8-70-21-3-743-6-96
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: omraade

* Feltnavn10: omraade
* Formål og registreringsvejledning, og evt. eksempel: Unikt områdenavn. Eksempel: Lilleskov Teglværk, Tommerup
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: beliggenhedskommune

* Feltnavn10: belig_kom
* Formål og registreringsvejledning, og evt. eksempel: Kommunenummer for den kommune, som facilitet er beliggende i. Kan hjælpe med at filtrere data ift. hvilke faciliteter der er i hvilke kommuner. Udfyldes automatisk hver nat ud fra en analyse mellem facilitetspunktet og DAGI-kommunegrænse. Eksempel: 860
* Datatype: Heltal
* Værdiområde: 100-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: geometri_beskrivelse

* Feltnavn10: geom_beskr
* Formål og registreringsvejledning, og evt. eksempel: En beskrivelse af den geometriske afgrænsning af bygningsvurderingsgruppen. Eksempel: Området er defineret ved lokalplanafgrænsning 23-12
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: omfang

* Feltnavn10: gr_omfang
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af omfanget. Eksempel: Lilleskov Teglværks ældste bygninger
* Datatype: Tekststreng
* Værdiområde: 0-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: beskrivelse

* Feltnavn10: gr_beskriv
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af gruppen. Eksempel: Garageanlæg til biler
* Datatype: Tekststreng
* Værdiområde: 0-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: registrator

* Feltnavn10: gr_regnavn
* Formål og registreringsvejledning, og evt. eksempel: Navn på den person eller myndighed der har oprettet gruppen. Eksempel: Jens Andersen
* Datatype: Tekststreng
* Værdiområde: 0-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F




## Detaljeret beskrivelser (release details):



### Bygningsvurdering (6205)



#### Tilføjet:

Nyt tema med navnet ’Bygningsvurdering (6205)’ tilføjes til temagruppen ’Planlægning’.

Metadata:
* Temanavn: Bygningsvurdering
* Temakode: 6205
* Definition: En bevaringsmæssig vurdering af en bygning fx baseret på SAVE-metoden.
* Beskrivelse:Bygningens bevaringsværdi vurderes ud fra en række fastlagte vurdereringselementer i hht. SAVE-metoden. Der kan dog også foretages en "light-udgave" af bygningsvurderingen, hvor kun den samlede bevaringsværdi angives. 
* Formaal: Bygningsvurderingen skal sikre at bevaringsværdige bygninger kan blive beskyttet i den kommunale planlægning ligesom det kan have betydning for ejendommens værdi
* Noegleord\_hovedgruppe: Bevaringsværdige bygninger
* Nogle\_ord: Bevaringsværdi, Arkitektur, Bygningshistorie, Bebyggelsesmiljø, Bygningstilstand, Bygningsoriginalitet
* Geometri type: Polygon
* Lovgrundlag:
* KLE\_koder:  01.10.00 (Bygningsfredning og bygningsbevaring i almindelighed)

Registreringsvejledning:
* Registreringsinstruks: Bygningsvurderingen oprettes med en geometri der udpeger den bygning (eller dele af den) som er blevet vurderet. Der udfyldes karakterer og vurderingstekster. Der kan tilknyttes fotos. Bygningsvurderingen kan være del af én eller flere bygningsvurderingsgrupper.
* Klassificering/opdeling: Der findes ingen fælles klassificering af bygningsvurderingen idet bevaringsværdien (0-9) kan vurderes forskelligt fra kommune til kommune.
* Minimum størrelser for objekt: 0,1 m
* Entydige objekter: -
* Geometrisk konsistens mellem objekter: Bygningspolygonerne for sammenhængende bygninger skal snappe til hinanden. Der bør ikke være overlap mellem bygningsvurderingerne.
* Geometrisk konsistens mellem objekter i andre datasæt: Tag udgangspunkt i bygningspolygonen fra GeoDanmark grunddata. Tilpas den evt. så afgrænsningen afspejler den bygning (eller dele af den) som er omfattet af vurderingen.

Temaet tilføjes følgende attributter/felter:

Feltnavn: objekt_id

* Feltnavn10: objekt_id
* Formål og registreringsvejledning, og evt. eksempel: Entydig databasenøgle over tid. Eksempel: E6AB20EA-67E4-4C11-A051-B50A084788A3
* Datatype: UUID (128 bit)
* Værdiområde: 16 bytes
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: versions_id

* Feltnavn10: version_id
* Formål og registreringsvejledning, og evt. eksempel: Unik versions–id databasenøgle. Eksempel: E6AB20EA-67E4-4C11-A051-B50A084788A3
* Datatype: UUID (128 bit)
* Værdiområde: 16 bytes
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: systid_fra

* Feltnavn10: systid_fra
* Formål og registreringsvejledning, og evt. eksempel: Start systemtid. Eksempel: 2006-12-31T23:59:00.000+01:00
* Datatype: ISO date/tid
* Værdiområde: 2006-12-31T23:59:00.000+01:00 – 2999-12-31T23:59:00.000+01:00
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: systid_til

* Feltnavn10: systid_til
* Formål og registreringsvejledning, og evt. eksempel: Slut systemtid. Eksempel: 2006-12-31T23:59:00.000+01:00
* Datatype: ISO date/tid
* Værdiområde: 2006-12-31T23:59:00.000+01:00 – 2999-12-31T23:59:00.000+01:00
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: oprettet

* Feltnavn10: oprettet
* Formål og registreringsvejledning, og evt. eksempel: Systemtid for objektets oprettelse. Eksempel: 2006-12-31T23:59:00.000+01:00
* Datatype: ISO date/tid
* Værdiområde: 2006-12-31T23:59:00.000+01:00 – 2999-12-31T23:59:00.000+01:00
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: cvr_kode

* Feltnavn10: cvr_kode
* Formål og registreringsvejledning, og evt. eksempel: CVR-kode på ansvarlig myndighed. Eksempel: 29189641
* Datatype: Heltal
* Værdiområde: 10000000-99999999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S/(O)

Feltnavn: cvr_navn

* Feltnavn10: cvr_navn
* Formål og registreringsvejledning, og evt. eksempel: CVR-navn på ansvarlig myndighed. Eksempel: Silkeborg Kommune
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: kommunekode

* Feltnavn10: kommu_kode
* Formål og registreringsvejledning, og evt. eksempel: 3-cifret kommunenr. Eksempel: 740
* Datatype: Heltal
* Værdiområde: 100-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: bruger_id

* Feltnavn10: bruger_id
* Formål og registreringsvejledning, og evt. eksempel: Brugernavn ved opdatering. Eksempel: Silkeborg1234
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S/(O)

Feltnavn: oprindkode

* Feltnavn10: oprindkode
* Formål og registreringsvejledning, og evt. eksempel: Kode for oprindelse for objekt. Eksempel: 1
* Datatype: Heltal
* Værdiområde: 0-11
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: oprindelse

* Feltnavn10: oprindelse
* Formål og registreringsvejledning, og evt. eksempel: Oprindelse for objekt. Eksempel: Ortofoto
* Datatype: Tekststreng
* Værdiområde: 0-35
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: statuskode

* Feltnavn10: statuskode
* Formål og registreringsvejledning, og evt. eksempel: Kode for gældende status. Eksempel: 3
* Datatype: Heltal
* Værdiområde: 0-4
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: status

* Feltnavn10: status
* Formål og registreringsvejledning, og evt. eksempel: Gældende status. Eksempel: Gældende / Vedtaget
* Datatype: Tekststreng
* Værdiområde: 0-30
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: off_kode

* Feltnavn10: off_kode
* Formål og registreringsvejledning, og evt. eksempel: Kode for Tilgængelighed. Eksempel: 1
* Datatype: Heltal
* Værdiområde: 1-3 (default = 1)
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: offentlig

* Feltnavn10: offentlig
* Formål og registreringsvejledning, og evt. eksempel: Tilgængelighed. Eksempel: Synlig for alle
* Datatype: Tekststreng
* Værdiområde: 0-60
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: noegle

* Feltnavn10: noegle
* Formål og registreringsvejledning, og evt. eksempel: Fremmed nøgle til objektet i en anden databasetabel. Eksempel: 12853468A
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: note

* Feltnavn10: note
* Formål og registreringsvejledning, og evt. eksempel: Notering af forhold som har betydning for registreringen. Eksempel: Vurderingen omfatter alene den oprindelige del af bygning 1 og ikke den tilbyggede udestue.
* Datatype: Tekststreng
* Værdiområde: 0-254 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geometri

* Feltnavn10: geometri
* Formål og registreringsvejledning, og evt. eksempel: Geometrisk beskrivelse af objekt. Eksempel: For et punkt: 543210,999 6123456,111
* Datatype: Punkt, Linje, Flade
* Værdiområde: X: -370.000,000-1.777.483,999, Y: 5.200.000,000-7.347.483,999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: gyldig_fra

* Feltnavn10: gyldig_fra
* Formål og registreringsvejledning, og evt. eksempel: Start gyldighedsperiode. Eksempel: 2006-12-31
* Datatype: ISO date
* Værdiområde: 2006-12-31 – 2999-12-31
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: gyldig_til

* Feltnavn10: gyldig_til
* Formål og registreringsvejledning, og evt. eksempel: Slut gyldighedsperiode. Eksempel: 2006-12-31
* Datatype: ISO date
* Værdiområde: 2006-12-31 – 2999-12-31
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: vejkode

* Feltnavn10: vejkode
* Formål og registreringsvejledning, og evt. eksempel: Vejkode (DAR). Eksempel: 46100128
* Datatype: Heltal
* Værdiområde: 0001-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: vejnavn

* Feltnavn10: vejnavn
* Formål og registreringsvejledning, og evt. eksempel: Vejnavn der refererer til vejkode. Eksempel: Borgergade
* Datatype: Tekststreng
* Værdiområde: 0-40 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: husnr

* Feltnavn10: husnr
* Formål og registreringsvejledning, og evt. eksempel: Husnummer. Eksempel: 122C
* Datatype: Tekststreng
* Værdiområde: 0-4 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: postnr

* Feltnavn10: postnr
* Formål og registreringsvejledning, og evt. eksempel: Postnr. Eksempel: 8600
* Datatype: Heltal
* Værdiområde: 0001-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: postnr_by

* Feltnavn10: postnr_by
* Formål og registreringsvejledning, og evt. eksempel: By der refererer til Postnr. Eksempel: Silkeborg
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: adr_id

* Feltnavn10: adr_id
* Formål og registreringsvejledning, og evt. eksempel: Entydig databasenøgle fra det officielle adresseregister (UUID). Eksempel: E6AB20EA-67E4-4C11-A
* Datatype: Tekststreng 16 bytes
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: koordinat_north

* Feltnavn10: koord_n
* Formål og registreringsvejledning, og evt. eksempel: Koordinat til brug i navigations systemer. Eksempel: 55° 42' 41.1000''N
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: koordinat_east

* Feltnavn10: koord_e
* Formål og registreringsvejledning, og evt. eksempel: Koordinat til brug i navigations systemer. Eksempel: 12° 33' 56.2424''E
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link

* Feltnavn10: link
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link1

* Feltnavn10: link1
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link2

* Feltnavn10: link2
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: link3

* Feltnavn10: link3
* Formål og registreringsvejledning, og evt. eksempel: URL-link. Eksempel: http://www.link.dk/123
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto

* Feltnavn10: geofafoto
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Feltet vil blive brugt til det primære foto for objektet sat i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto1

* Feltnavn10: geofafoto1
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto2

* Feltnavn10: geofafoto2
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto3

* Feltnavn10: geofafoto3
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto4

* Feltnavn10: geofafoto4
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto5

* Feltnavn10: geofafoto5
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto6

* Feltnavn10: geofafoto6
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto7

* Feltnavn10: geofafoto7
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto8

* Feltnavn10: geofafoto8
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: geofafoto9

* Feltnavn10: geofafoto9
* Formål og registreringsvejledning, og evt. eksempel: Automatisk dannet URL-link til foto lagt ind i GeoFA billedunderstøttelsesmodulet. Eksempel: https://geofa.geodanmark.dk/geofa/foto.png
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: sagsnr

* Feltnavn10: sagsnr
* Formål og registreringsvejledning, og evt. eksempel: Identifikation af sag i ESDH. Eksempel: 8-70-21-3-743-6-96
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: beliggenhedskommune

* Feltnavn10: belig_kom
* Formål og registreringsvejledning, og evt. eksempel: Kommunenummer for den kommune, som facilitet er beliggende i. Kan hjælpe med at filtre data ift. hvilke faciliteter der er i hvilke kommuner. Udfyldes automatisk hver nat ud fra en analyse mellem facilitetspunktet og DAGI-kommunegrænse. Eksempel: 860
* Datatype: Heltal
* Værdiområde: 100-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S

Feltnavn: BFE-nummer

* Feltnavn10: bfe_nr
* Formål og registreringsvejledning, og evt. eksempel: BFE-nummer. BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 9025416
* Datatype: Heltal
* Værdiområde: 1-9999999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: bygningsnummer

* Feltnavn10: byg_nr
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 1
* Datatype: Heltal
* Værdiområde: 1-999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: matrikel_ejerlav

* Feltnavn10: matrikel
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 11A, Skibinge By, Skibinge
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: opfoerelsesaar

* Feltnavn10: opf_aar
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 1900
* Datatype: Heltal
* Værdiområde: 1-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: anvendelse

* Feltnavn10: anvendelse
* Formål og registreringsvejledning, og evt. eksempel: BBR anvendelse ("fryses" for registreringsdatoen). Eksempel: Enfamiliehus
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: ombygningsaar

* Feltnavn10: omb_aar
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 1900
* Datatype: Heltal
* Værdiområde: 1-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: tagdaekning

* Feltnavn10: tagdaekn
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: Fibercement
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: ydervaeg

* Feltnavn10: ydervaeg
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: Mursten
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bebyggetareal

* Feltnavn10: beb_areal
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 190
* Datatype: Heltal
* Værdiområde: 1-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: totalbygningsareal

* Feltnavn10: tot_areal
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 300
* Datatype: Heltal
* Værdiområde: 1-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: etager

* Feltnavn10: etager
* Formål og registreringsvejledning, og evt. eksempel: BBR-oplysning ("fryses" for registreringsdatoen). Eksempel: 2
* Datatype: Heltal
* Værdiområde: 1-9999
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bbr_uuid

* Feltnavn10: bbr_uuid
* Formål og registreringsvejledning, og evt. eksempel: Id der anvendes til kobling med BBR. Eksempel: c017d5cd-c554-4410-9aee-79b5dfe3fab0
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bygningsnavn

* Feltnavn10: byg_navn
* Formål og registreringsvejledning, og evt. eksempel: Typisk bygningens navn eller type. Eksempel: SOLHJEM
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bygningsnotat

* Feltnavn10: byg_notat
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til bygningsbeskrivelsen. Eksempel: Bygningen har tidligere fungeret som administrationsbygning for Præstø kommune
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: objekt

* Feltnavn10: objekt
* Formål og registreringsvejledning, og evt. eksempel: Specificering af bygningen. Eksempel: KURSUSCENTER
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: registreringsproblem

* Feltnavn10: reg_probl
* Formål og registreringsvejledning, og evt. eksempel: Særlige omstændigheder omkring registreringen. Eksempel: Bygningen kan ikke identificeres, registreringen opgivet
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: komplekstype

* Feltnavn10: kompl_type
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af hvilken komplekstype bygningen indgår i. Eksempel: Bondegård
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bygningsfunktion

* Feltnavn10: byg_funkt
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af bygningens funktion og hvordan den evt. har ændret sig over tid. Eksempel: Tidligere stuehus til landbrugsejendom, nu enfamiliehus
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: vurderingsbaseline

* Feltnavn10: baseline
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af hvilken periodemæssig udgave af bygningen som registreringen tager udgangspunkt i. Eksempel: Bygningen er ombygget af flere omgange siden opførelsen i 1922. Vurderingen tager udgangspunkt i de bygningstræk der kan relateres til 1920'erne
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bygningsdel

* Feltnavn10: byg_del
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige bygningsdele. Eksempel: Veranda, udestue
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: doereporte

* Feltnavn10: doereporte
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige døre/porte. Eksempel: Ny dør
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: gavlkonstruktion

* Feltnavn10: gavl
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige gavltyper. Eksempel: Grundmuret gavl
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: gesims

* Feltnavn10: gesims
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige gesimstyper. Eksempel: Muret gesims
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: hovedplan

* Feltnavn10: hovedplan
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige bygningsplantyper. Eksempel: Enfløjet bygning
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: kvist

* Feltnavn10: kvist
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige kvisttyper. Eksempel: Facade-/frontkvist
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: sokkel

* Feltnavn10: sokkel
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige sokkeltyper. Eksempel: Støbt (beton)
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: stilart

* Feltnavn10: stilart
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige stilarter. Eksempel: Anden stilart
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: tagkonstruktion

* Feltnavn10: tagkonstr
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige tagkonstruktioner. Eksempel: Mansardtag
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: udsmykning

* Feltnavn10: udsmykning
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige udsmykninger. Eksempel: Frise, bånd
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: vindue

* Feltnavn10: vindue
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige vinduestyper. Eksempel: Retkantet
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: ydermur

* Feltnavn10: ydermur
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige murtyper. Eksempel: Diverse pladebeklædninger
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bebyggelsesmiljoe

* Feltnavn10: beb_miljoe
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af det bebyggelsesmiljø / den bebyggede struktur som bygningen indgår i. Eksempel: Fritliggende ejendom
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: ydre_forhold

* Feltnavn10: yd_forhold
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af det forhold bygningen har til andre bygninger i nærheden. Eksempel: Fritliggende, uden arkitektonisk tilknytning til andre bygninger uden for matriklen
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: indre_forhold

* Feltnavn10: in_forhold
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af det forhold bygningen har til andre bygninger på grunden. Eksempel: Fritliggende, med arkitektonisk tilknytning til andre bygninger på matriklen
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: omgivelser

* Feltnavn10: omgivelser
* Formål og registreringsvejledning, og evt. eksempel: Fremhævelse af særlige omgivelser. Beskrivelse af særlige elementer i omgivelser. Eksempel: Mark, eng
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: arkitektonisk_vaerdi

* Feltnavn10: ark_kar
* Formål og registreringsvejledning, og evt. eksempel: Karakter for den arkitektoniske værdi. Eksempel: 4
* Datatype: Heltal
* Værdiområde: 0-9
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: arkitektonisk_vurdering

* Feltnavn10: ark_vurd
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til karakter. Eksempel: Murværket står blankt som det bør være, jævnfør dansk funktionalisme.
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: kulturhistorisk_vaerdi

* Feltnavn10: kul_kar
* Formål og registreringsvejledning, og evt. eksempel: Karakter for den kulturhistoriske værdi. Eksempel: 5
* Datatype: Heltal
* Værdiområde: 0-9
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: kulturhistorisk_vurdering

* Feltnavn10: kul_vurd
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til karakter. Eksempel: Et eksempel på variation i baggårdene af forskellige stilarter, her funktionalisme
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: miljømæssig_vaerdi

* Feltnavn10: mil_kar
* Formål og registreringsvejledning, og evt. eksempel: Karakter for den miljømæssige værdi. Eksempel: 4
* Datatype: Heltal
* Værdiområde: 0-9
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: miljømæssig_vurdering

* Feltnavn10: mil_vurd
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til karakter. Eksempel: Bygningen ligger i en baggård med en fin belægning og bidrager positivt til gårdmiljøet
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: originalitetsvaerdi

* Feltnavn10: orig_kar
* Formål og registreringsvejledning, og evt. eksempel: Karakter for originaliteten af bygningen. Eksempel: 3
* Datatype: Heltal
* Værdiområde: 0-9
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: originalitetsvurdering

* Feltnavn10: orig_vurd
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til karakter. Eksempel: Bygningen er bevaret som den oprindeligt er bygget, dog er der plastikvinduer.
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: tilstandsvaerdi

* Feltnavn10: tilst_kar
* Formål og registreringsvejledning, og evt. eksempel: Karakter for bygningens tilstand. Eksempel: 3
* Datatype: Heltal
* Værdiområde: 0-9
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: tilstandsvurdering

* Feltnavn10: tilst_vurd
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til karakter. Eksempel: Fin stand
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bevaringsmæssig_vaerdi

* Feltnavn10: bev_kar
* Formål og registreringsvejledning, og evt. eksempel: Karakter for bygningens samlede bevaringsværdi (SAVE-vurderingen). Eksempel: 4
* Datatype: Heltal
* Værdiområde: 0-9
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bevaringsmæssig_vurdering

* Feltnavn10: bev_vurd
* Formål og registreringsvejledning, og evt. eksempel: Forklaring til karakter. Eksempel: Enkel funktionalistisk bygning i blank gul mur med detaljering i murværk omkring vinduer
* Datatype: Tekststreng
* Værdiområde: 0-1024 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: registreringsdato

* Feltnavn10: reg_dato
* Formål og registreringsvejledning, og evt. eksempel: Dato for registreringen. Eksempel: 2006-12-31
* Datatype: ISO date
* Værdiområde: 1006-12-31 – 2999-12-31
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: registrator

* Feltnavn10: registra
* Formål og registreringsvejledning, og evt. eksempel: Navn på den person der har foretaget bygningsregistreringen. Eksempel: Jens Hansen
* Datatype: Tekststreng
* Værdiområde: 0-128 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): F

Feltnavn: bevaringsvaerdig

* Feltnavn10: bev_status
* Formål og registreringsvejledning, og evt. eksempel: Angivelse af om en bygning er udpeget som bevaringsværdig (TRUE = ja, FALSE = nej). Eksempel: Ja
* Datatype: Boolean
* Værdiområde: Ja/nej
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: bevaringsaarsag_kode

* Feltnavn10: bev_bggr_k
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af hvad der ligger til grund for en udpegning af en bevaringsværdig bygning. Eksempel: 2
* Datatype: Heltal
* Værdiområde: 0-3
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): O

Feltnavn: bevaringsaarsag

* Feltnavn10: bev_bggr
* Formål og registreringsvejledning, og evt. eksempel: Beskrivelse af hvad der ligger til grund for en udpegning af en bevaringsværdig bygning. Eksempel: udpeget som bevaringsværdig i kommuneplan
* Datatype: Tekststreng
* Værdiområde: 0-256 tegn
* Obligatorisk (O) / Frit (F) / Systemgenereret (S): S


I opslagslisten ’d\_6205\_bevaringsaarsag’ tilføjes følgende udfaldsrum

bevaringsaarsag\_kode: 0
* bevaringsaarsag: ikke udpeget som bevaringsværdig
* Aktiv: 1
* Begrebsdefinition:

bevaringsaarsag\_kode: 1
* bevaringsaarsag: udpeget som bevaringsværdig i lokalplan
* Aktiv: 1
* Begrebsdefinition:

bevaringsaarsag\_kode: 2
* bevaringsaarsag: udpeget som bevaringsværdig i kommuneplan
* Aktiv: 1
* Begrebsdefinition:

bevaringsaarsag\_kode: 3
* bevaringsaarsag: udpeget som bevaringsværdig i kommuneplan og lokalplan
* Aktiv: 1
* Begrebsdefinition:


\---
