---
title: "Bruke oppslag til å finne informasjon"
description: "I Microsoft Dynamics 365 for operasjoner har mange felt oppslag som kan hjelpe deg å finne den riktige verdien ønsket. Flere forbedringer har blitt lagt til oppslag som gjør disse kontrollene mer brukervennlige og gjøre brukere mer produktive. I dette emnet du vil lære mer om disse nye funksjonene lookup og får noen nyttige tips for å få optimal bruk av oppslag i systemet."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Bruke oppslag til å finne informasjon

I Microsoft Dynamics 365 for operasjoner har mange felt oppslag som kan hjelpe deg å finne den riktige verdien ønsket. Flere forbedringer har blitt lagt til oppslag som gjør disse kontrollene mer brukervennlige og gjøre brukere mer produktive. I dette emnet du vil lære mer om disse nye funksjonene lookup og får noen nyttige tips for å få optimal bruk av oppslag i systemet.  

<a name="responsive-lookups"></a>Følsom oppslag
------------------

I tidligere versjoner av Dynamics 365 for operasjoner, når du bruker en kontroll med oppslag, må en bruker en eksplisitt tiltakene for å åpne rullegardinmenyen. Dette kan ha vært ved å skrive inn en stjerne (\*) i kontrollen for å filtrere oppslaget basert på gjeldende verdi i kontrollen, når du klikker rullegardinlisten, eller ved å bruke den **Alt**+**pil ned** hurtigtast. Oppslag-kontrollene har blitt endret på følgende måter å justere bedre med gjeldende web-fremgangsmåter:

-   Oppslag rullegardinmenyene åpnes nå automatisk etter en liten pause i å skrive, med rullegardinlisten innholdet menyen filtrert basert på verdien for kontrollen for oppslag.
    -   Legg merke til at den gamle virkemåten for automatisk åpning av rullegardinlisten etter å skrive inn en stjerne (\*) har blitt avverget.
-   Når du har åpnet rullegardinmenyen oppslag, skjer følgende:
    -   Markøren blir værende i oppslag-kontrollen (i stedet for å flytte inn i rullegardinmenyen fokus) slik at du kan fortsette å gjøre endringer i verdien for kontrollen. Brukeren kan imidlertid fortsatt bruke den **pil opp** og **pil ned** til å endre rader i på rullegardinmenyen, og Skriv inn for å merke gjeldende rad i på rullegardinmenyen.
    -   Justerer innholdet i i rullegardinmenyen når endringer er gjort i slå opp verdien.

Anta for eksempel at et oppslagsfelt kalt **by**. 

Når fokuset er i den **by** -feltet, kan du starte etter byen som du vil bruke, ved å skrive inn noen få bokstaver, som "Kol."  Etter at du slutter å skrive, åpnes oppslag automatisk, filtrert til disse byene som begynner med "k". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Markøren er på dette tidspunktet fremdeles i oppslagsfeltet. Hvis du fortsetter å skrive slik at verdien er "kolonner", justeres innholdet oppslag automatisk for å gjenspeile den siste verdien i kontrollen. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Selv om fokus er fremdeles i oppslag-kontrollen, kan du også bruke den **pil opp** eller **pil ned** til å merke raden som du vil merke. Hvis du trykker **Enter** den merkede raden vil bli valgt fra oppslaget og verdien vil bli oppdatert. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Å skrive inn mer enn IDer
Når du angir data, er det naturlig for brukere å prøve å identifisere en enhet, for eksempel en kunde eller leverandør i navnet i stedet for en identifikator som representerer enheten. I den gjeldende versjonen av Dynamics 365 for operasjoner, mange (men ikke alle) oppslag nå dataregistrering kontekstavhengig. Denne kraftige funksjonen gjør det mulig for brukeren å skrive inn IDen eller tilsvarende navnet i oppslag-kontrollen. 

Anta for eksempel at **kundekontoen** -feltet når du oppretter en salgsordre. Dette feltet viser den **konto-ID** for kunden, men en bruker vanligvis vil angi en **kontonavnet** i stedet for en **konto-ID** for dette feltet når du oppretter en salgsordre, for eksempel "Skog Wholesales" i stedet for "US-003."

Hvis brukeren startet til å skrive inn et **konto-ID** i oppslag-kontroll på rullegardinmenyen vil åpnes automatisk som beskrevet i den forrige delen, og brukeren ser oppslaget som vist nedenfor.

[![Kontekstavhengige oppslag når du angir en kundekonto-ID](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Brukeren kan imidlertid nå også angi begynnelsen på en **kontonavnet** også. Hvis det blir funnet, vil brukeren se følgende oppslaget. Legg merke til hvordan **navn** flyttes kolonnen til å være den første kolonnen i oppslaget, og hvordan oppslaget er sortert og filtrert basert på den **navn** kolonnen.

[![Kontekstavhengige oppslag når det angis et kundenavn](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Ved hjelp av kolonneoverskriftene i rutenettet for mer avansert filtrering og sortering
Oppslag-forbedringer som er beskrevet i de forrige to delene betydelig forbedre en brukers mulighet til å navigere radene i et oppslag som er basert på et "begynner med" Søk på den **ID** eller **navnet** i oppslaget. Det finnes imidlertid situasjoner der mer avansert filtrering (eller sortering) er nødvendig for å finne den riktige raden. I slike tilfeller må brukeren bruke alternativer for filtrering og sortering i rutenettet kolonneoverskriftene i oppslaget. Anta for eksempel at en ansatt angir en salgsordrelinje som trenger å finne høyre "kabel" som produktet. Å skrive inn "kabel" i den **varenummer** kontroll ikke er nyttig, fordi det ikke finnes noen produktnavn som begynner med "kabel." 

![emptyitemlookup](./media/emptyitemlookup.png) 

I stedet, må brukeren fjerne verdien for kontrollen oppslag, åpne rullegardinmenyen oppslag og filtrere rullegardinmenyen ved hjelp av kolonneoverskriften rutenett, som vist nedenfor. En mus (eller trykk) bruker kan ganske enkelt klikk (eller rør) en kolonneoverskrift for å få tilgang til filtrerings- og sorteringsalternativer for den aktuelle kolonnen. For en bruker tastatur, brukeren bare trenger å trykke **Alt**+**ned****pil** en gang til for å flytte fokus til rullegardinmenyen, etter som brukeren kan tab til den riktige kolonnen, og trykk deretter **Ctrl**+**G** å åpne i rutenett-kolonnen hodet rullegardinmenyen. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Etter at filteret er brukt (se bildet nedenfor), kan brukeren finne og merke raden som vanlig. 

![filtereditemlookup](./media/filtereditemlookup.png)


