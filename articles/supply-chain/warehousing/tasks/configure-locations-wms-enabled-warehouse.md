---
title: Konfigurere lokasjoner i et WMS-aktivert lager
description: Denne veiledningen viser deg hvordan du konfigurerer lokasjonsoppsettet for et nytt WMS-aktivert lager (et lager som bruker avanserte lagerstyringsprosesser).
author: perlynne
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59835d28afc6f855f109cf9b875624f8fd11191a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977320"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Konfigurere lokasjoner i et WMS-aktivert lager

[!include [banner](../../includes/banner.md)]

Denne veiledningen viser deg hvordan du konfigurerer lokasjonsoppsettet for et nytt WMS-aktivert lager (et lager som bruker avanserte lagerstyringsprosesser). Prosessen gjøres vanligvis av en lagersjef. Du kan kjøre denne veiledningen i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. En forutsetning er at du har konfigurert minst ett område.


## <a name="create-a-new-warehouse"></a>Opprette et nytt lager
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lageroppdeling > Lagre**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Lager**-feltet.
4. Skriv inn en verdi i **Navn**-feltet.
5. Skriv inn en verdi i **Område**-feltet.
6. Vis delen **Lager**.
7. Angi alternativet **Bruk lagerstyringsprosesser** til Ja. Denne innstillingen lar deg kjøre avanserte lagerprosesser som bruker lagerarbeid og mobilenheter.
8. Lukk siden.

## <a name="define-a-location-format"></a>Definere et lokasjonsformat
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Lokasjonsformater**. Lokasjonsformatene er et navngivningssystem som skal brukes til å opprette unike og konsekvente navn for de ulike lokasjonsboksposisjonene som brukes i et lager. Det kan være nyttig å bruke skilletegn som del av lokasjonsformatet for å gjøre det enklere å identifisere komponenter i lokasjonen for eksempel gangnummeret. I dette eksemplet skal vi opprette et navn med fire komponenter. Dette kan for eksempel være gang, reol, hylle og boks.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Lokasjonsformat**.
4. Skriv inn en verdi i **Navn**-feltet.
5. Skriv inn en verdi i feltet **Segmentbeskrivelse**. Dette beskriver hva den første delen av lokasjonsnavnet representerer. Det kan for eksempel være Gang.
6. Angi et tall i feltet **Lengde**. Dette bestemmer hvor mange tegn denne delen av lokasjonsnavnet må ha. Legg merke til at summen av alle komponenter i navnet, inkludert skilletegnene, ikke kan overskride 10 tegn.    
7. Skriv inn en verdi i feltet **Skilletegn**. Dette bestemmer hvilket tegn eller symbol som brukes mellom første og andre komponent av navnet.  
8. Klikk på **Ny** i **Detaljer**-delen.
9. Skriv inn en verdi i feltet **Segmentbeskrivelse**.
10. Angi et tall i feltet **Lengde**.
11. Skriv inn en verdi i feltet **Skilletegn**.
12. Klikk på **Ny** i **Detaljer**-delen.
13. Skriv inn en verdi i feltet **Segmentbeskrivelse**.
14. Angi et tall i feltet **Lengde**.
15. Skriv inn en verdi i feltet **Skilletegn**.
16. Klikk på **Ny** i **Detaljer**-delen.
17. Skriv inn en verdi i feltet **Segmentbeskrivelse**.
18. Angi et tall i feltet **Lengde**.
19. Klikk på **Lagre**.
20. Lukk siden.

## <a name="define-location-types"></a>Definere lokasjonstyper
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Lokasjonstyper**. Lokasjonstyper kan brukes som filtreringsalternativer for å styre de ulike lagerstyringsprosessene. Som et minimum må du opprette typer for oppsamling og endelig levering for å definere den utgående lagerstyringsprosessen. 
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Lokasjonstype**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Lukk siden.

## <a name="define-location-profile"></a>Definere lokasjonsprofil
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Lokasjonsprofiler**. Definisjonen av lokasjonsprofiler er svært viktig. Gruppert lokasjonskapasitet kan kontrolleres her, i tillegg til policyene som gjelder hva beholdning skal lagre, og hvordan den lagres. Lokasjonsprofiler kan brukes som filtreringsalternativer for å styre de ulike lagerstyringsprosessene. Som et minimum må du opprette en brukerlokasjonsprofil for å aktivere lagerstyringsprosesser.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Profil-ID for lokasjon**.
4. Skriv inn en verdi i **Navn**-feltet.
5. Klikk på rullegardinknappen i feltet **Lokasjonsformat** for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen.
8. Klikk på rullegardinknappen i feltet **Lokasjonstype** for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk på koblingen i den valgte raden i listen.
11. Merk av eller fjern merket i boksen **Tillat kombinerte lagerstatuser**. Aktiver dette alternativet hvis du vil tillate blandede lagerstatusverdier i lokasjoner som skal grupperes etter denne lokasjonsprofilen. 
12. Merk av eller fjern merket i boksen **Overstyr regler for partidager**. Aktiver dette alternativet for å overstyre regelen for hvor mange dager utløpsdatoene for beholdningsparti kan være forskjellig, for å tillate blanding av lagerpartier som ikke overholder denne regelen.  
13. Merk av eller fjern merket i boksen **Tillat syklustelling**. Aktiver dette alternativet hvis du vil tillate syklustellingbehandling i alle lokasjoner som skal grupperes etter denne lokasjonsprofilen. 
14. Vis eller skjul delen **Dimensjoner**. Med fanen Dimensjoner kan du definere parametere og metoder for å aktivere nøyaktige beregninger av belastningskapasitet i hver enkelt lokasjon.  
15. Lukk siden.

## <a name="enable-warehouse-management-parameters"></a>Aktivere parametere for lagerstyring
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lagerstyringsparametere**. Hvis du skal kunne behandle lagerarbeid, må du angi parametere for brukerlokasjonsprofilen, oppsamlingslokasjonstypen og den endelige leveringslokasjonstypen. Så snart den utgående prosessen slutter ved den endelige forsendelseslokasjonstypen som du definerer, oppdateres de relaterte utgående transaksjonene til Plukket.
2. Vis delen **Lokasjonsprofiler**.
3. Klikk på rullegardinknappen i feltet **Brukerlokasjon** for å åpne oppslaget.
4. Klikk på koblingen i den valgte raden i listen.
5. Vis delen **Lokasjonstyper**.
6. Klikk på rullegardinknappen i feltet **Oppsamlingslokasjonstype** for å åpne oppslaget.
7. Klikk på koblingen i den valgte raden i listen.
8. Klikk på rullegardinknappen i feltet **Endelig leveringslokasjonstype** for å åpne oppslaget.
9. Klikk på koblingen i den valgte raden i listen.
10. Lukk siden.

## <a name="define-warehouse-zone-groups"></a>Definere lagersonegrupper
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Lagersonegrupper**. Lagersoner kan brukes som filtre for alternativer for å styre de ulike lagerstyringsprosessene. Du må opprette en sonegruppe før du kan definere en sone.   
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **ID for sonegruppe**.
4. Skriv inn en verdi i feltet **Navn på sonegruppe**.
5. Lukk siden.

## <a name="define-warehouse-zones"></a>Definere lagersoner
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Soner**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Sone-ID**.
4. Skriv inn en verdi i feltet **Sonenavn**.
5. Klikk på rullegardinknappen i feltet **ID for sonegruppe** for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen.
8. Lukk siden.

## <a name="create-locations-using-the-location-setup-wizard"></a>Opprette lokasjoner ved hjelp av veiviseren for lokasjonsoppsett
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lager > Veiviser for lokasjonsoppsett**.
2. Klikk på rullegardinknappen i **Lager**-feltet for å åpne oppslaget.
3. Finn og velg ønsket post i listen.
4. Klikk på koblingen i den valgte raden i listen.
5. Klikk på rullegardinknappen i feltet **Sone-ID** for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen.
8. Klikk på rullegardinknappen i feltet **Profil-ID for lokasjon** for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk på koblingen i den valgte raden i listen.
11. Merk den valgte raden i listen.
12. Angi et tall i feltet **Fra-nummer**. Feltene Fra-nummer og Til-nummer definerer hvor mange lokasjoner som skal opprettes. Hvis du for eksempel angir Fra-nummer 1 og Til-nummer 3 for alle fire linjer i lokasjonsformatet, opprettes 81 lokasjoner (3x3x3x3).   
13. Angi et tall i feltet **Til-nummer**.
14. Finn og velg ønsket post i listen.
15. Angi et tall i feltet **Fra-nummer**.
16. Angi et tall i feltet **Til-nummer**.
17. Finn og velg ønsket post i listen.
18. Angi et tall i feltet **Fra-nummer**.
19. Angi et tall i feltet **Til-nummer**.
20. Finn og velg ønsket post i listen.
21. Angi et tall i feltet **Fra-nummer**.
22. Angi et tall i feltet **Til-nummer**.
23. Klikk på Opprett.

## <a name="create-locations-manually"></a>Opprette lokasjoner manuelt
1. Gå til **Lagerstyring > Oppsett > Lager > Lokasjoner**. Manuell opprettelse av lokasjoner i et lager kan gjøres enkelt. Lokasjonens navn og lokasjonsprofil-ID-en er obligatoriske verdier. 
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Lager**-feltet.
4. Skriv inn en verdi i feltet **Lokasjon**. Vær oppmerksom på at du oppretter en ny lokasjon her, så du må skrive inn et nytt unikt navn, i stedet for å velge et eksisterende.
5. Skriv inn en verdi i feltet **Profil-ID for lokasjon**.
6. Lukk siden.

## <a name="define-pack-size-categories"></a>Definere kategorier for pakkestørrelse
1. Gå til **Lagerstyring > Oppsett > Lager > Kategorier for pakkestørrelse**. Kategorier for pakkestørrelse kan brukes til å gruppere varer med lignende fysiske pakkestørrelser. I dette eksemplet brukes pakkestørrelseskategorien til å styre kapasiteten ved plukklokasjoner i en bestemt sone i lageret. Vær oppmerksom på at pakkestørrelseskategori-ID må være tilordnet til frigitt produkt-enhet for å kunne brukes som en del av behandling av lagringsgrenser.  
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **ID for kategori for pakkestørrelse**.
4. Skriv inn en verdi i feltet **Navn på kategori for pakkestørrelse**.
5. Lukk siden.

## <a name="define-location-stocking-limits"></a>Definere lagringsgrenser for lokasjon
1. Gå til **Lagerstyring > Oppsett > Lager > Lokasjon – lagringsgrenser**. Lokasjon – lagringsgrenser hjelper med å være sikker på at arbeidet ikke er opprettet for å be om at lageret skal plasseres på en lokasjon som ikke har den fysiske kapasiteten til å føre beholdningen.  
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Lager**-feltet.
4. Skriv inn en verdi i feltet **Profil-ID for lokasjon**.
5. Skriv inn en verdi i feltet **ID for kategori for pakkestørrelse**.
6. Angi et tall i **Antall**-feltet.
7. Klikk på **Lagre**.
8. Lukk siden.

## <a name="define-fixed-picking-locations"></a>Definere faste plukklokasjoner
1. Gå til **Lagerstyring > Oppsett > Lager > Faste lokasjoner**. Du kan definere hvilke lokasjoner som skal brukes per produkt eller produktvariant. Det er mulig å opprette flere faste lokasjoner for det samme produktet innenfor samme lager.     
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Varenummer**-feltet.
4. Skriv inn en verdi i **Lager**-feltet.
5. Klikk på rullegardinknappen i **Lokasjon**-feltet for å åpne oppslaget.
6. Klikk på koblingen i den valgte raden i listen.
7. Lukk siden.

