--- 
title: Opprette en rekvisisjon for forbruk
description: "Denne prosedyren hjelper deg gjennom prosessen for å opprette en rekvisisjon."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7d8ca4e7eedea140f32e264c205b243027a06d03
ms.openlocfilehash: d1ea95d0bc283297fcedaee730e1829850f07998
ms.contentlocale: nb-no
ms.lasthandoff: 11/20/2017

---
# <a name="create-a-requisition-for-consumption"></a>Opprette en rekvisisjon for forbruk

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom prosessen for å opprette en rekvisisjon. Den viser forskjellige måter å søke etter produkter på i innkjøpskatalogen og hvordan du legger til et produkt som ikke finnes i katalogen. Før du starter denne fremgangsmåten, må en innkjøpspolicy være definert med Forbruk som standardtype for rekvisisjon. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Prosedyren kan bare utføres av en brukerprofil som er definert som arbeider.  Denne oppgaven vil vanligvis utføres av en ansatt. Med sikkerhetsrollen som ansatt kan du utføre oppgavene, eller hvis du bruker USMF, kan du logge inn med Alicia.


## <a name="create-a-new-requisition"></a>Opprett en ny rekvisisjon
1. Gå til Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg.
2. Klikk Ny.
3. Gi rekvisisjonen et navn i Navn-feltet.
4. Angi en dato i feltet Ønsket dato.
    * Som standard kopieres den forespurte datoen og regnskapsdatoen til innkjøpsrekvisisjonslinjene. De kan endres på linjenivå. Ønsket dato er ønsket leveringsdato.  
5. Angi en dato i feltet Regnskapsdato.
    * Regnskapsdatoen brukes til å registrere regnskapsoppføringen i økonomimodulen, og til å validere hvorvidt budsjettmidler er tilgjengelige.  
6. Klikk OK.
7. Klikk rullegardinknappen i feltet Årsak for å åpne oppslaget.
    * Bestillingsårsaken du velger, vises som standard for innkjøpsrekvisisjonslinjene, men du kan endre den på linjenivået.    
8. Finn og velg ønsket post i listen.
9. Velg årsaken
10. I Detaljer-feltet angir du en mer beskrivende begrunnelse for rekvisisjonen

## <a name="add-a-line-to-the-requisition"></a>Legge til en linje i rekvisisjonen
1. Klikk Legg til linje.
    * Det finnes to måter å legge til linjer i innkjøpsrekvisisjonen på. Hvis du allerede kjenner produktnummer, eller du allerede vet at du ber om et produkt som ikke er i produktkatalogen, kan du legge til linjen direkte med "Legg til linje". Den andre måten er å bruke "Legg til produkter", der du kan bruke søk og filtrering til å finne varer i produktkatalogen.    
2. Klikk i raden du nettopp opprettet.
    * Bestilleren er arbeideren som har bedt om rekvisisjonen.   
    * Som standard er personen som klargjør rekvisisjonen, arbeideren som har bedt om den. Du må få tillatelse til å klargjøre en rekvisisjonslinje på vegne av en annen arbeider. Hvis du har slike tillatelser, vises de andre arbeiderne i dette oppslaget.  
3. Skriv inn en verdi i Varenummer-feltet.
    * Varene som er tilgjengelige for deg å velge, begrenses av kategoritilgangspolicyen og innkjøpskatalogen for den juridiske enheten for innkjøp.   
4. Angi et tall i feltet Antall.

## <a name="add-more-products-to-the-requisition"></a>Legge til flere produkter i rekvisisjonen
1. Klikk Legg til produkter.
    * Dette er alternativet der du kan søke etter produkter i produktkatalogen.    
2. I Finn innkjøpskategorinode-feltet skriver du inn første del av navnet på kategorien du leter etter, og klikk deretter Enter.
    * Skriv for eksempel comput.  
3. Bruk InvokeDefaultButton-snarveien.
4. Bruk filteret til å filtrere listen over produkter i den valgte kategorien.
5. Velg produktkortet som du vil legge til i rekvisisjonen.
6. Klikk Tilføy til linjer.
7. Angi et tall i Antall-feltet.
8. I Finn innkjøpskategorinode-feltet skriver du inn første del av navnet på kategorien du leter etter, og klikk deretter Enter.
    * Skriv for eksempel Høy (merkepenner).  
9. Bruk InvokeDefaultButton-snarveien.
10. Klikk Tilføy ulistede produkter til linjer for å legge til et produkt som ikke er oppført i innkjøpskatalogen.
11. Skriv inn en verdi i feltet Produktnavn.
12. Skriv inn en verdi i feltet Enhet.
13. Klikk OK.
14. Legg til en beskrivelse av produktet i Varebeskrivelse-feltet.
15. Angi et tall i feltet Antall.
16. Angi et tall i feltet Enhetspris.
    * Hvis du kjenner prisen for en bestemt leverandør (som du velger i leverandørkontofeltet), kan du angi denne prisen   
17. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
    * Leverandører som er tilgjengelige i dette feltet avhenger av innkjøpspolicyer og statusen som leverandøren har for gjeldende innkjøpskategori. Som et alternativ til å velge en leverandør her, kan du klikke knappen Foreslå leverandør.    
18. Velg leverandøren du vil bruke, i listen.
19. Skriv inn en verdi i feltet Eksternt varenummer.
    * Dette er et referansenummer for produktet som er kjent av leverandøren. Dette kan for eksempel være varenummeret for produktet i leverandørens egen katalog.  
20. Klikk OK.

## <a name="distribute-amounts"></a>Fordel beløp
1. Klikk Finans.
2. Klikk Fordel beløp.
    * Denne prosessen viser deg hvordan du distribuerer kostnaden for den første linjen mellom 2 kontoer. Dette kan også gjøres senere når rekvisisjonen er til vurdering.  
3. Klikk Del for å opprette en ny distribusjonslinje.
4. Velg det første kostsenteret som skal ta del i kostnaden i feltet Finanskonto.
5. Velg den andre distribusjonslinjen.
6. Angir det andre kostsenteret i Finanskonto-feltet.
7. Klikk Fordel likt.
8. Lukk siden.

## <a name="view-line-details"></a>Vise linjedetaljer
1. Aktiver/deaktiver utvidelsen av delen Linjedetaljer.

## <a name="submit-the-requisition"></a>Sende rekvisisjonen
1. Klikk Arbeidsflyt for å åpne nedtrekksdialogen.
2. Klikk Send.
3. Lukk siden.
4. I feltet Kommentar skriver du inn en merknad for godkjenneren av rekvisisjonen.
5. Klikk Send.
6. Lukk siden.
7. Oppdater siden.


