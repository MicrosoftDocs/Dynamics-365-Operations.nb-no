---
title: "Betalingsmåter"
description: "Hver betalingstype som godtar en forhandler må konfigureres i handel og handel i Microsoft Dynamics 365 for operasjoner når systemet er definert. Denne artikkelen beskriver betalingstypene som du kan sette opp og beskriver fremgangsmåten for hvordan du definerer dem."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: MargoC
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b887fc5d03ea8982515e92725ce98cc416e56f9e
ms.openlocfilehash: 011beec07bf1ab858892ab1c374f1acf3839e877
ms.lasthandoff: 03/31/2017


---

# <a name="payment-methods"></a>Betalingsmåter

Hver betalingstype som godtar en forhandler må konfigureres i handel og handel i Microsoft Dynamics 365 for operasjoner når systemet er definert. Denne artikkelen beskriver betalingstypene som du kan sette opp og beskriver fremgangsmåten for hvordan du definerer dem.

Forhandlere kan ta imot ulike typer betaling i bytte mot produktene og tjenestene de selger. Selv om kontanter er den vanligste formen for betaling, kan forhandlerne også mottar betaling i form av sjekker, kort, bilag og så videre. Hver betalingstype som godtar forhandleren må konfigureres i Dynamics 365 for operasjoner - Retail når systemet er definert. Følgende liste beskriver hver betalingstype som kan settes opp i Dynamics 365 for operasjoner - handel:

-   **Kontant ** – Penger i den fysiske formen av valuta, for eksempel pengesedler og mynter. Valutaen kan være enten firmavalutaen eller butikkens lokale valuta.
-   **Sjekk** – Et omsettelig dokument som instruerer om betaling av et bestemt beløp av en angitt valuta, og dette trekkes fra en spesifikk bank. En sjekk er vanligvis gyldig på ubestemt tid eller i seks måneder etter utstedelsesdatoen, med mindre en annen gyldighetsperioden er angitt. Denne perioden varierer avhengig av banken som sjekken trekkes fra. Det finnes ulike typer sjekker, for eksempel ordresjekker, blankosjekker, ihendehaversjekker og kryssede sjekker. Du kan definere sjekker som betalingsmåte for hver butikk. Sjekker kan tas imot i valutaen som er definert på firmanivå eller butikknivå. Du må definere sjekker som betalingsmåte før du godkjenner en sjekk som betaling i en butikk.
-   **Valuta** – Den primære betalingsmåten bortsett fra firmaets standardvaluta. Mynter og papirpenger er begge former for valuta. Valutabetalingsmåten representerer all valutaer som brukes i Detaljhandel og handel. Før du kan bruke denne betalingsmåten, må du definere valutaer og angi handelskursinformasjon for valutaene.
-   **Kort** – Alle typer kort som brukes i Detaljhandel og handel, for eksempel debetkort og kredittkort. Det er lurt å definere én betalingsmåte på organisasjonsnivå som representerer alle korttyper. Deretter defineres en betalingsmåte på butikknivå for hvert kort eller sett med kort behandles ved hjelp av de samme innstillingene. Du må definere produsentkortene som er tilgjengelige på markedet, for eksempel debet- og kredittkort, før du kan godta kort som betaling i en butikk.
-   **Kreditnota** – Kreditnotaer som er utstedt eller innløst på salgsstedet. Kreditnotaen kan være en kreditnota eller mottakskreditnota som er utstedt mot retursalg. Hvis kreditnotaer bare innløses delvis, utsteder programmet en ny kreditnota for den nye saldoen. Den nye kreditnotaen har et nytt nummer. En kreditnota kan bare brukes én gang, og systemet holder oversikten over alle numrene som er brukt. Posten kan vises på siden **Kreditnotatabell**. En kunde kan ikke innløse mer enn verdien av kreditnotaen.
-   **Gavekort** – Gavekort som er utstedt og innløst på salgsstedet. Overbetaling er ikke tillatt på gavekort.
-   **Kundekonto** – Betalinger som kan belastes en kundekonto ved registrering på salgstidspunktet. Du kan også bruke denne betalingsmåten for å samle inn salgsinformasjon eller kundespesifikke rabatter når kunden foretar en betaling ved hjelp av en annen betalingsmåte. Hvis det er tilfelle, må du definere kundespesifikk informasjon.
-   **Fordelspoeng** – punktene som kunder er akkumuleres gjennom lojalitetsprogrammer. Hvis du oppretter lojalitetsprogrammer, kan kunder får poeng og innløse dem på forskjellige måter. I noen fordelsprogrammer kan for eksempel kunder løse inn fordelspoeng i form av en rabatt eller til og med bruke dem som en form for betaling.

Hvis du vil definere betalingsmåter i Detaljhandel og handel, må du fullføre oppgavene nedenfor.

1.  Definer betalingsmåter for en organisasjon. Definer betalingsmåtene som godtas av hele organisasjonen.
2.  Opprette organisasjonsomfattende korttyper og kortnumre. Hvis kredittkort eller debetkort godtas, må du opprette én betalingsmåte for kort, og deretter opprette organisasjonsomfattende korttyper og kortnumre.
3.  Angi betalingsmåten som lager. Knytte betalingsmåter til hver butikk, og angi deretter butikk-spesifikke innstillingene for hver enkelt betalingsmåte.
4.  Definere betalingsmåter for kort for butikker. Fullfør kortoppsettet for alle kort betalingsmåter som butikken godtar.



