---
title: Betalingsmåter
description: Hver betalingstype en forhandler godtar, må konfigureres når systemet defineres. Denne artikkelen beskriver betalingstypene som du kan sette opp og beskriver fremgangsmåten for hvordan du definerer dem.
author: BrianShook
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.industry: Retail
ms.search.form: RetailTenderTypeTable
ms.openlocfilehash: d16cdf237042471d367adb7081bf34e9c8a9460f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272829"
---
# <a name="payment-methods"></a>Betalingsmåter

[!include [banner](includes/banner.md)]

Hver betalingstype en forhandler godtar, må konfigureres når systemet defineres. Denne artikkelen beskriver betalingstypene som du kan sette opp og beskriver fremgangsmåten for hvordan du definerer dem.

Forhandlere kan ta imot ulike typer betaling i bytte mot produktene og tjenestene de selger. Selv om kontanter er den vanligste formen for betaling, kan forhandlerne også mottar betaling i form av sjekker, kort, bilag og så videre. Hver betalingstype en forhandler godtar, må konfigureres i Dynamics 365 Commerce når systemet defineres. Listen nedenfor beskriver hver betalingstype som kan settes opp:

- **Kontant** – Penger i den fysiske formen av valuta, for eksempel pengesedler og mynter. Valutaen kan være enten firmavalutaen eller butikkens lokale valuta.
- **Sjekk** – Et omsettelig dokument som instruerer om betaling av et bestemt beløp av en angitt valuta, og dette trekkes fra en spesifikk bank. En sjekk er vanligvis gyldig på ubestemt tid eller i seks måneder etter utstedelsesdatoen, med mindre en annen gyldighetsperioden er angitt. Denne perioden varierer avhengig av banken som sjekken trekkes fra. Det finnes ulike typer sjekker, for eksempel ordresjekker, blankosjekker, ihendehaversjekker og kryssede sjekker. Du kan definere sjekker som betalingsmåte for hver butikk. Sjekker kan tas imot i valutaen som er definert på firmanivå eller butikknivå. Du må definere sjekker som betalingsmåte før du godkjenner en sjekk som betaling i en butikk.
- **Valuta** – Den primære betalingsmåten bortsett fra firmaets standardvaluta. Mynter og papirpenger er begge former for valuta. Valutabetalingsmåten representerer all valutaer som brukes. Før du kan bruke denne betalingsmåten, må du definere valutaer og angi kursinformasjon for valutaene.
- **Kort** – Alle typer kort som brukes, for eksempel debetkort og kredittkort. Det er lurt å definere én betalingsmåte på organisasjonsnivå som representerer alle korttyper. Deretter defineres en betalingsmåte på butikknivå for hvert kort eller sett med kort behandles ved hjelp av de samme innstillingene. Du må definere produsentkortene som er tilgjengelige på markedet, for eksempel debet- og kredittkort, før du kan godta kort som betaling i en butikk.
- **Kreditnota** – Kreditnotaer som er utstedt eller innløst på salgsstedet. Kreditnotaen kan være en kreditnota eller mottakskreditnota som er utstedt mot retursalg. Hvis kreditnotaer bare innløses delvis, utsteder programmet en ny kreditnota for den nye saldoen. Den nye kreditnotaen har et nytt nummer. En kreditnota kan bare brukes én gang, og systemet holder oversikten over alle numrene som er brukt. Posten kan vises på siden **Kreditnotatabell**. En kunde kan ikke innløse mer enn verdien av kreditnotaen.
- **Gavekort** – Gavekort som er utstedt og innløst på salgsstedet. Overbetaling er ikke tillatt på gavekort. Alle gavekort bør ha kortnummertilordninger. 
- **Kundekonto** – Betalinger som kan belastes en kundekonto ved registrering på salgstidspunktet. Du kan også bruke denne betalingsmåten for å samle inn salgsinformasjon eller kundespesifikke rabatter når kunden foretar en betaling ved hjelp av en annen betalingsmåte. Hvis det er tilfelle, må du definere kundespesifikk informasjon.
- **Fordelspoeng** – Poengene som kunder akkumulerer gjennom fordelsprogrammer. Hvis du oppretter fordelsprogrammer, kan kunder få poeng og innløse dem på forskjellige måter. I noen fordelsprogrammer kan for eksempel kunder løse inn fordelspoeng i form av en rabatt eller til og med bruke dem som en form for betaling.

Du må fullføre følgende oppgaver hvis du vil definere betalingsmåter.

1. Definer betalingsmåter for en organisasjon. Definer betalingsmåtene som godtas av hele organisasjonen.
2. Opprett korttyper og kortnumre for hele organisasjonen. Hvis kredittkortene eller debetkortene godtas, må du opprette én betalingsmetode for kort og deretter opprette korttypene og kortnumrene for hele organisasjonen.
3. Definere betalingsmåte i butikker Knytt betalingsmåter til hver butikk, og angi deretter de butikkspesifikke innstillingene for hvert betalingsmåte.
4. Definer kortbetalingsmåter for butikker. Fullfør kortoppsettet for alle kortbetalingsmåter som butikken godtar.

## <a name="handle-change-tendering-for-payment-methods"></a>Håndter endring av betaling for betalingsmetoder

Noen betalingsmetoder støtter ikke direkte endring av betaling hvis midler forfaller tilbake til kunder under salgsstedstransaksjoner. Det er bare betalingsmetodene **Kontant** og **Valuta** som kan brukes til endring av betaling. 

For å håndtere tilfeller der endring av betaling kreves under en transaksjon, men betalingsmetoden ikke støtter dette, kan du definere en betalingsmetode for **endring av betaling**. Når du definerer betalingsmetoder for butikken, velger du betalingsmetoden som skal brukes. Deretter, i **Endre**-delen, i feltet **Endre betaling**, angir du et betalingsalternativ for å endre betaling. Du kan for eksempel angi **1** for å angi at kontanter kan brukes som et alternativ for endring av betaling.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
