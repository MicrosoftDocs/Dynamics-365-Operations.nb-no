--- 
title: Definere et lokasjonsdirektiv for bestillings
description: "Denne fremgangsmåten viser hvordan du setter opp et enkelt lokasjonsdirektiv."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4c2456fffd9a010728154749b35c58db13f142bb
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Definere et lokasjonsdirektiv for bestillings

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du setter opp et enkelt lokasjonsdirektiv. Eksemplet som vises, oppretter et lokasjonsdirektiv som skal brukes til å avgjøre hvor du vil plassere varer som er mottatt for en bestilling. Du kan spille av denne oppgaveveiledningen med dataene som er nevnt, ved hjelp av demonstrasjonsdataselskapet USMF. Forutsetninger: Du må opprette en disposisjonskode. I denne fremgangsmåten bruker vi en disposisjonskode kalt Endre navn. Hvis du oppretter et lokasjonsdirektiv i dine egne data, må du ha definert avansert lagerstyring for lager og varer.  Denne fremgangsmåten er ment for lagersjef.

1. Gå til Lagerstyring > Oppsett > Lokasjonsdirektiver.
2. Velg Bestillinger i feltet Arbeidsordretype.

## <a name="create-a-location-directive-header"></a>Opprette et lokasjonsdirektivhode
1. Klikk Ny.
2. Angi et nummer i Sekvensnummer-feltet.
    * Dette er rekkefølgen for behandling av lokasjonsdirektivet for den valgte arbeidstypen. Du kan også om nødvendig endre rekkefølgen.  
3. Skriv inn en verdi i Navn-feltet.
    * Dette er den unike identifikatoren for dette direktivet.  
4. Velg Plasser i Arbeidstype-feltet.
    * Velg hvilken type arbeid som skal utføres. Plasser er den eneste støttede verdien for direktivet med arbeidsordretypen Bestilling.  
5. Skriv inn en verdi i Område-feltet.
6. Skriv inn en verdi i Lager-feltet.
    * La direktivkoden stå tom.  Direktivkodene brukes til å koble en arbeidsordrelinje av typen Plasser til et bestemt direktiv. For bestillinger løses lokasjonen for den siste arbeidsordrelinje av typen Plasser før arbeidsmalen bestemmes. Det er derfor ikke mulig å koble til den siste linjen i en arbeidsmal på et bestemt direktiv.   
7. Skriv inn en verdi i Disposisjonskode-feltet.
    * Disposisjonskoden begrenser bruken av lokasjonsdirektivet slik at lokasjonsdirektivet brukes bare hvis lagermedarbeideren angir denne bestemte verdien under registrering av varen med en mobil enhet.  
8. Klikk Lagre.

## <a name="edit-the-query-for-directive"></a>Redigere spørringen for direktivet
1. Klikk Rediger spørring.
    * Bruk av dette direktivet er allerede begrenset for bruk for varer som er registrert i lageret som du har angitt, og med disposisjonskoden som du har angitt. Du kan legge til andre begrensninger ved hjelp av spørringen.  
2. Klikk OK.

## <a name="add-directive-lines"></a>Legge til direktivlinjer
1. Klikk Ny.
    * Dette er rekkefølgen for behandling av lokasjonsdirektivlinjene for den valgte arbeidstypen. Du kan også om nødvendig endre rekkefølgen.  
2. Angi et tall i feltet Fra-antall.
    * Dette er det laveste antallet som denne direktivlinjen er gyldig for.  
3. Angi et tall i feltet Til-antall.
4. Skriv inn en verdi i feltet Enhet.
    * Enheten fra-antallet og til-antallet uttrykkes i. Hvis du lar dette feltet stå tomt, brukes lagerenheten fra varen.  
5. Velg et alternativ i feltet Plasser antall.
    * Ingen, eller Nummerskiltantall: antallet som er registrert på hvert nummerskilt. Antall delt opp i enheter: hele antallet som er registrert. Restantall: Antallet som ikke ennå er registrert fra bestillingslinjen. Forventet antall: Det totale antallet som er angitt på bestillingslinjen.  
6. Merk av eller fjern merket i boksen Begrens etter enhet.
    * Hvis du velger dette alternativet, og angir enheten på siden av Begrens etter enhet, kan bare varer med denne enheten plasseres på lokasjonen. Hvis måleenheten for eksempel er paller, så kan bare varer på paller plasseres på den angitte lokasjonen.  
7. Merk av eller fjern merket i boksen Tillat deling.
    * Dette gjør at direktivet kan dele antallet mellom flere lokasjoner.  
8. Klikk Lagre.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Begrense direktivlinjen til en bestemt enhet
1. Klikk Begrens etter enhet.
    * Denne knappen er bare tilgjengelig når du trykker Lagre etter at du har merket av for Begrens etter enhet.  
2. Skriv inn en verdi i feltet Enhet.
3. Lukk siden.

## <a name="add-a-location-directive-action-line"></a>Legge til en handlingslinje for lokasjonsdirektiv
1. Klikk Ny.
    * Dette er rekkefølgen for behandling av lokasjonsdirektivhandlingslinjene for den valgte arbeidstypen. Du kan også om nødvendig endre rekkefølgen.  
2. Skriv inn en verdi i Navn-feltet.
    * Dette er den unike identifikatoren for denne direktivhandlingen.  
3. Velg et alternativ i feltet Bruk av fast lokasjon.
    * Faste og ikke-faste lokasjoner: Alle ikke-faste lokasjoner er gyldige i tillegg til produktets egne faste lokasjon innenfor området som er angitt i spørringen.  Bare faste lokasjoner for produktet: Faste lokasjoner for produktet er gyldige, og alle produktvarianter deler det samme settet med fast lokasjoner. Bare faste lokasjoner for produktvarianten: Bare faste lokasjoner som er angitt for hver produktvariant er gyldige.  
4. Velg et alternativ i feltet Strategi.
    * Arbeidsordrer av typen Bestilling støtter følgende strategier: Ingen: varen plasseres i den første lokasjonen som blir funnet. Konsolider: Varen plasseres i en lokasjon der lignende varer finnes allerede. Tom lokasjon uten innkommende arbeid: varen plasseres i den første tomme lokasjonen som blir funnet. En lokasjon anses som tom hvis den ikke har fysisk beholdning og ikke forventet innkommende arbeid.  
5. Klikk Lagre.

## <a name="edit-the-query-for-directive-action-line"></a>Redigere spørringen for direktivhandlingslinje
1. Klikk Rediger spørring.
2. Klikk Legg til.
3. Skriv inn lokasjonsprofil-ID i feltet Felt.
    * I dette eksemplet skal vi begrense mulige lokasjoner ved hjelp av en lokasjonsprofil-ID.  
4. Skriv inn en verdi i Kriterier-feltet.
5. Klikk OK.
    * Du kan fortsette å legge til direktivlinjer og direktivhandlinger før du dekket alle mulige scenarier i lageret.  

