---
title: Definere et lokasjonsdirektiv for bestillings
description: Dette emnet forklarer hvordan du definerer et enkelt lokasjonsdirektiv.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a363b452cbee539aeee62146f545b1f7c2eb842
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576214"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Definere et lokasjonsdirektiv for bestillings

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du definerer et enkelt lokasjonsdirektiv. Eksemplet som vises, oppretter et lokasjonsdirektiv som skal brukes til å avgjøre hvor du vil plassere varer som er mottatt for en bestilling. Du kan spille av denne oppgaveveiledningen med dataene som er nevnt, ved hjelp av demonstrasjonsdataselskapet USMF. Forutsetninger: Du må opprette en disposisjonskode. I denne fremgangsmåten bruker vi en disposisjonskode kalt Endre navn. Hvis du oppretter et lokasjonsdirektiv i dine egne data, må du ha definert avansert lagerstyring for lager og varer. Denne fremgangsmåten er ment for lagersjef.

1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Lokasjonsdirektiv**.
2. Velg **Bestillinger** i feltet **Arbeidsordretype**.

## <a name="create-a-location-directive-header"></a>Opprette et lokasjonsdirektivhode
1. Velg **Ny**.
2. Angi et nummer i **Sekvensnummer**-feltet. Dette er rekkefølgen for behandling av lokasjonsdirektivet for den valgte arbeidstypen. Du kan også om nødvendig endre rekkefølgen.  
3. Skriv inn en verdi i **Navn**-feltet. Dette er den unike identifikatoren for dette direktivet.  
4. Velg **Plasser** i **Arbeidstype**-feltet. Velg hvilken type arbeid som skal utføres. **Plasser** er den eneste støttede verdien for direktivet med arbeidsordretypen Bestilling.  
5. Skriv inn en verdi i **Område**-feltet.
6. Skriv inn en verdi i **Lager**-feltet. La direktivkoden stå tom.  Direktivkodene brukes til å koble en arbeidsordrelinje av typen Plasser til et bestemt direktiv. For bestillinger løses lokasjonen for den siste arbeidsordrelinje av typen Plasser før arbeidsmalen bestemmes. Det er derfor ikke mulig å koble til den siste linjen i en arbeidsmal på et bestemt direktiv.   
7. Skriv inn en verdi i **Disposisjonskode**-feltet. Disposisjonskoden begrenser bruken av lokasjonsdirektivet slik at lokasjonsdirektivet brukes bare hvis lagermedarbeideren angir denne bestemte verdien under registrering av varen med en mobil enhet.  
8. Velg **Lagre**.

## <a name="edit-the-query-for-directive"></a>Redigere spørringen for direktivet
1. Velg **Rediger spørring**. Bruk av dette direktivet er allerede begrenset for bruk for varer som er registrert i lageret som du har angitt, og med disposisjonskoden som du har angitt. Du kan legge til andre begrensninger ved hjelp av spørringen.  
2. Velg **OK**.

## <a name="add-directive-lines"></a>Legge til direktivlinjer
1. Velg **Ny**. Dette er rekkefølgen for behandling av lokasjonsdirektivlinjene for den valgte arbeidstypen. Du kan også om nødvendig endre rekkefølgen.  
2. Angi et tall i feltet **Fra-antall**. Dette er det laveste antallet som denne direktivlinjen er gyldig for.  
3. Angi et tall i feltet **Til-antall**.
4. Skriv inn en verdi i feltet **Enhet**. Enheten fra-antallet og til-antallet uttrykkes i. Hvis du lar dette feltet stå tomt, brukes lagerenheten fra varen.  
5. Velg et alternativ i feltet **Plasser antall**.
    - Ingen, eller nummerskiltantall: antallet som er registrert på hvert nummerskilt.  
    - Antall delt opp i enheter: hele antallet som er registrert.  
    - Restantall: Antallet som ikke ennå er registrert fra bestillingslinjen.  
    - Forventet antall: Det totale antallet som er angitt på bestillingslinjen.  
6. Merk av eller fjern merket i boksen **Begrens etter enhet**. Hvis du velger dette alternativet, og angir enheten på siden av **Begrens etter enhet**, kan bare varer med denne enheten plasseres på lokasjonen. Hvis måleenheten for eksempel er paller, så kan bare varer på paller plasseres på den angitte lokasjonen.  
7. Merk av eller fjern merket i boksen **Tillat deling**. Dette gjør at direktivet kan dele antallet mellom flere lokasjoner.  
8. Velg **Lagre**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Begrense direktivlinjen til en bestemt enhet
1. Velg **Begrens etter enhet**. Denne knappen er bare tilgjengelig når du trykker **Lagre** etter at du har merket av for **Begrens etter enhet**.  
2. Skriv inn en verdi i feltet **Enhet**.
3. Lukk siden.

## <a name="add-a-location-directive-action-line"></a>Legge til en handlingslinje for lokasjonsdirektiv
1. Velg **Ny**. Dette er rekkefølgen for behandling av lokasjonsdirektivhandlingslinjene for den valgte arbeidstypen. Du kan også om nødvendig endre rekkefølgen.  
2. Skriv inn en verdi i **Navn**-feltet. Dette er den unike identifikatoren for denne direktivhandlingen.  
3. Velg et alternativ i feltet **Bruk av fast lokasjon**.
    - Faste og ikke-faste lokasjoner: Alle ikke-faste lokasjoner er gyldige i tillegg til produktets egne faste lokasjon innenfor området som er angitt i spørringen.  
    - Bare faste lokasjoner for produktet: Faste lokasjoner for produktet er gyldige, og alle produktvarianter deler det samme settet med fast lokasjoner.  
    - Bare faste lokasjoner for produktvarianten: Bare faste lokasjoner som er angitt for hver produktvariant er gyldige.  
4. Velg et alternativ i feltet **Strategi**. Arbeidsordrer av typen Bestilling støtter følgende strategier: 
    - Ingen: Varen plasseres på den første lokasjonen som blir funnet.  
    - Konsolider: Varen plasseres i en lokasjon der lignende varer finnes allerede.  
    - Tom lokasjon uten innkommende arbeid: varen plasseres i den første tomme lokasjonen som blir funnet. En lokasjon anses som tom hvis den ikke har fysisk beholdning og ikke forventet innkommende arbeid.  
5. Velg **Lagre**.

## <a name="edit-the-query-for-directive-action-line"></a>Redigere spørringen for direktivhandlingslinje
1. Velg **Rediger spørring**.
2. Velg **Legg til**.
3. Skriv inn `location profile ID` i feltet **Felt**. I dette eksemplet skal vi begrense mulige lokasjoner ved hjelp av en lokasjonsprofil-ID.  
4. Skriv inn en verdi i **Kriterier**-feltet.
5. Velg **OK**. Du kan fortsette å legge til direktivlinjer og direktivhandlinger før du dekket alle mulige scenarier i lageret.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]