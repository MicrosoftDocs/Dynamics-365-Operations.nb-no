---
title: Negative dager og dynamiske negative dager
description: Dette emnet inneholder informasjon om negative dager og dynamiske negative dager og hvordan du kan bruke dem til å hjelpe virksomheten.
author: ChristianRytt
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37ae6ebd4347d3bbb414b7f1e4e0d54150878c02
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097240"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Negative dager og dynamiske negative dager

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om negative dager og dynamiske negative dager og hvordan du kan bruke dem til å hjelpe virksomheten. *Horisonten for negative dager* representerer hvor mange dager du er villig til å vente før du bestiller ny etterfylling, når du har en negativ beholdning.

I dette emnet lærer du følgende:

- Hvordan planlagte ordrer opprettes
- Korrelasjonen mellom horisonten for negative dager og varens leveringstid
- Hvordan horisonten for negative dager beregnes, og hvordan varens leveringstid tas med i beregningen
- Hvordan du tolker [forslag for å forbedre kjøretiden for planlegging av materialbehov (MRP) (hovedplanlegging)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) som er knyttet til negative dager

Dette emnet bruker tre hypotetiske scenarier som kan hjelpe deg å forstå denne informasjonen. Forskjellen mellom scenariene har å gjøre med når du får behov: før, under eller etter varens leveringstidsperiode.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Scenario 1: Du får behov før varens leveringstidsperiode

Du kan få behov relativt tidlig i varens leveringstid eller like før leveringstidsperioden begynner. Her er et eksempel på dette scenariet:

- DemoProduct-varen har en leveringstid for innkjøp på seks dager.
- På dag null (1. januar) er lagernivået for DemoProduct-varen 0 (null).
- På dag null (1. januar) får du en salgsordre for et antall på 10 av DemoProduct-varen.
- Det finnes en eksisterende bestilling for et antall på 10 av DemoProduct-varen på dag sju (8. januar).

Illustrasjonen nedenfor viser en grafisk visning av dette scenariet.

![Grafisk visning av scenario 1](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Tilfelle A: negative dager er mindre enn varens leveringstid

Hvis du setter negative dager til et tall som er mindre enn varens leveringstid, søker MRP etter mottak for DemoProduct-varen i horisonten for negative dager. Siden MRP ikke finner noen mottak, oppretter den et nytt bestillingsforslag. Dette bestillingsforslaget forsinkes umiddelbart med seks dager (leveringstiden). Derfor ankommer det 7. januar. Den eksisterende bestillingen får handlingsmeldingen **Annuller** fordi opprettelsen av det nye bestillingsforslaget har gjort den overflødig.

Illustrasjonen nedenfor viser et skjermbilde av dette tilfellet.

![Skjermbilde av tilfelle A for scenario 1](./media/negative-days-2.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle A for scenario 1](./media/negative-days-3.png)

Hvis du vurderer MRP-ytelse og planlegger nervøsitet, fungerer ikke dette tilfellet bra. MRP må opprette en ny planlagt ordre og beregne forsinkelser og handlinger. Disse oppgavene er tidkrevende. Dette tilfellet legger også til to ytterligere transaksjoner i planen. På den annen side blir salgsordren forsinket med bare seks dager, ikke sju dager.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Tilfelle B: negative dager er større enn varens leveringstid

Du kan bidra til å forbedre MRP-ytelsen ved å sette antall negative dager til et tall som er større enn varens leveringstid. Siden du ikke kan få forsyningen innen leveringstiden i dette scenariet, kan du søke etter mottak så lenge dette søket gir mening. Selv om kjøretiden for MRP blir kortere, bør du se opp for ytterligere forsinkelser for ordrene.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Tilfelle C: Sette varens leveringstid automatisk i relasjon til horisonten for negative dager

Hvis du vil sette varens leveringstid automatisk i relasjon til horisonten for negative dager, bruker du dynamiske negative dager. Hvis du vil bruke dynamiske negative dager, går du til **Hovedplanlegging \> Oppsett \> Hovedplanleggingsparametere**, og deretter setter du alternativet **Bruk dynamiske negative dager** til **Ja** i **Dekning**-delen i **Generelt**-fanen. MRP ser deretter etter mottak innenfor horisonten for dynamiske negative dager. Denne horisonten beregnes med følgende formel:

Horisont for dynamiske negative dager = Leveringstid for innkjøp + Horisont for negative dager + (Gjeldende dato - Behovsdato)

(Hvis standard ordretype for DemoProduct-varen er **Produksjon** eller **Overføring**, er leveringstiden leveringstiden for **beholdning**.)

Når dynamiske negative dager brukes, er horisonten som MRP ser på etter mottak, nå 6 + 2 + 0 = 8 dager. MRP finner den eksisterende bestillingen og låser salgsordren til den. Ingen nye planlagte ordrer opprettes. Kjøretiden for MRP er derfor kortere. Illustrasjonen nedenfor viser nettobehov for DemoProduct-varen.

![Nettobehov for tilfelle C for scenario 1](./media/negative-days-4.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle C for scenario 1](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Tilfelle D: Bruk bare dynamiske negative dager

Hvis du setter negative dager til **0** (null) og bare bruker horisonten for dynamiske negative dager, er horisonten for dynamiske negative dager 6 + 0 + 0 = 6 dager. I dette tilfellet er resultatet det samme som resultatet i tilfelle A for dette scenariet. MRP må opprette en ny planlagt ordre og beregne forsinkelser og handlinger. Disse oppgavene er tidkrevende og kan også være frustrerende. Du har også to ekstra transaksjoner å behandle. Siden behovet ikke kan oppfylles tidsnok til at varen kan ankomme, fører dette tilfellet til unødvendige komplikasjoner i planen.

Illustrasjonen nedenfor viser et skjermbilde av dette tilfellet.

![Skjermbilde av tilfelle D for scenario 1](./media/negative-days-6.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle D for scenario 1](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Tilfelle E: Bruke både antall negative dager som er større enn varens leveringstid, og horisonten for dynamiske negative dager

Hvis du setter antall negative dager til et tall som er større enn varens leveringstid, og hvis du også bruker horisonten for dynamiske negative dager, er horisonten for dynamiske negative dager 6 + 6 + 0 = 12 dager. Denne fremgangsmåten kan gi en svært lang horisont som MRP må søke etter resultater i. Hvis du vil ha informasjon om hvordan tilfellet E er knyttet til en situasjon der du angir en lang horisont for negative dager, kan du se [Konklusjon](#conclusion)-delen i dette emnet.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Scenario 2: Du får behov i varens leveringstidsperiode

Du kan få behov i løpet av leveringstiden for varen. Her er et eksempel på dette scenariet:

- DemoProduct-varen har en leveringstid for innkjøp på seks dager. 
- På dag null (1. januar) er lagernivået for DemoProduct-varen 0 (null).
- På dag fire (5. januar), som er i løpet av varens leveringstid, får du en salgsordre for et antall på 10 av DemoProduct-varen.
- Det finnes en bestilling for et antall på 10 av DemoProduct-varen på dag sju (8. januar).

Illustrasjonen nedenfor viser en grafisk visning av dette scenariet.

![Grafisk visning av scenario 2](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Tilfelle A: negative dager er mindre enn varens leveringstid

Hvis du setter negative dager til et tall som er mindre enn varens leveringstid, søker MRP etter mottak for DemoProduct-varen i horisonten for negative dager. Siden MRP ikke finner noen mottak, oppretter den et nytt bestillingsforslag som bruker gjeldende dato som bestillingsdato. Dette bestillingsforslaget forsinkes umiddelbart med seks dager (leveringstiden). Derfor ankommer det 7. januar. Den eksisterende bestillingen får handlingsmeldingen **Annuller** fordi opprettelsen av det nye bestillingsforslaget har gjort den overflødig.

Illustrasjonen nedenfor viser et skjermbilde av dette tilfellet.

![Skjermbilde av tilfelle A for scenario 2](./media/negative-days-9.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle A for scenario 2](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Tilfelle B: negative dager er større enn varens leveringstid

Dette tilfellet ligner på tilfelle B for scenario 1. Hvis du setter antall negative dager til et tall som er større enn varens leveringstid, får du ikke en ny planlagt ordre. Salgsordren er knyttet til den eksisterende bestillingen.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Tilfelle C: Sette varens leveringstid automatisk i relasjon til horisonten for negative dager

Dette tilfellet ligner på tilfelle C for scenario 1 fordi dynamiske negative dager fungerer like bra som i det tilfellet. Horisonten for dynamiske negative dager er nå 6 + 2 - 4 = 4 dager. Hvis du bruker denne fremgangsmåten, finner MRP den eksisterende bestillingen og knytter salgsordren til den. Siden ingen nye planlagte ordrer opprettes, blir kjøretiden for MRP kortere.

Illustrasjonen nedenfor viser et skjermbilde av dette tilfellet.

![Skjermbilde av tilfelle C for scenario 2](./media/negative-days-11.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle C for scenario 2](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Tilfelle D: Bruk bare dynamiske negative dager

Hvis du setter negative dager til **0** (null) og bare bruker horisonten for dynamiske negative dager, er horisonten for dynamiske negative dager nå 6 + 0 - 4 = 2 dager. I dette tilfellet er resultatet det samme som resultatet i tilfelle A for dette scenariet. Hvis du vil ha en grafisk oversikt over hva som skjer, kan du se tilfelle A for dette scenariet.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Tilfelle E: Bruke både antall negative dager som er større enn varens leveringstid, og horisonten for dynamiske negative dager

Hvis du setter antall negative dager til et tall som er større enn varens leveringstid, og hvis du også bruker horisonten for dynamiske negative dager, er horisonten for dynamiske negative dager 6 + 6 - 4 = 8 dager. Denne fremgangsmåten kan gi en svært lang horisont som MRP må søke etter resultater i. Hvis du vil ha informasjon om hvordan tilfellet E er knyttet til en situasjon der du angir en lang horisont for negative dager, kan du se [Konklusjon](#conclusion)-delen i dette emnet.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Scenario 3: Du får behov etter varens leveringstidsperiode

Du kan få behov etter varens leveringstidsperiode. Her er et eksempel på dette scenariet:

- DemoProduct-varen har en leveringstid for innkjøp på seks dager.
- På dag null (1. januar) er beholdningen for DemoProduct-varen 0 (null).
- På dag sju (8. januar), som er utenfor varens leveringstid, får du en salgsordre for et antall på 10 av DemoProduct-varen.
- Det finnes en bestilling for et antall på 10 av DemoProduct-varen på dag ti (11. januar).

Illustrasjonen nedenfor viser en grafisk visning av dette scenariet.

![Grafisk visning av scenario 3](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Tilfelle A: negative dager er mindre enn varens leveringstid

Hvis du setter antall negative dager til et tall som er mindre enn varens leveringstid, ser MRP to dager foran salgsordrens behovsdato. Siden MRP ikke finner noe, oppretter den et nytt bestillingsforslag 2. januar. Dette bestillingsforslaget blir sendt akkurat tidsnok til å oppfylle salgsordrebehovet. Den eksisterende bestillingen får handlingsmeldingen **Annuller** fordi den ikke er nødvendig.

Illustrasjonen nedenfor viser et skjermbilde av dette tilfellet.

![Skjermbilde av tilfelle A for scenario 3](./media/negative-days-14.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle A for scenario 3](./media/negative-days-15.png)

> [!NOTE]
> På skjermbildet ovenfor er behovsdatoen for bestillingen 12. januar. Siden dette skjermbildet ble tatt i 2015, da 11. januar var en søndag, flyttet MRP behovsdatoen til neste arbeidsdag, som var mandag 12. januar. Bestillingen har likevel 11. januar som leveringsdato.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Tilfelle B: negative dager er større enn varens leveringstid

Hvis du setter antall negative dager til et tall som er større enn varens leveringstid, får du ikke en ny planlagt ordre. Salgsordren er låst til den eksisterende bestillingen. Derfor er salgsordren forsinket. Hvis du oppretter en planlagt ordre, kan du levere salgsordren i tide.

Illustrasjonen nedenfor viser et skjermbilde av dette tilfellet.

![Skjermbilde av tilfelle B for scenario 3](./media/negative-days-16.png)

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle B for scenario 3](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Tilfelle C: Sette varens leveringstid automatisk i relasjon til horisonten for negative dager

Dette tilfellet ligner på tilfelle C for scenario 1 fordi dynamiske negative dager fungerer like bra som, om ikke bedre enn, i tilfelle B for dette scenariet.

Horisonten for dynamiske negative dager er nå 6 + 2 - 7 = 1 dag. I dette tilfellet tar imidlertid systemet hensyn til leveringstiden i negative dager (2), fordi MRP tar hensyn til maksimumsverdien mellom leveringstiden i negative dager og leveringstiden i dynamiske negative dager. Derfor er resultatet i dette tilfellet det samme som resultatet i tilfelle A for dette scenariet.

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer i dette tilfellet.

![Grafisk visning av tilfelle C for scenario 3](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Tilfelle D: Bruk bare dynamiske negative dager

Hvis du setter negative dager til **0** (null) og bare bruker horisonten for dynamiske negative dager, er horisonten for dynamiske negative dager nå 6 + 0 - 7 = -1 dag. I dette tilfellet tar systemet fortsatt hensyn til ledetiden i negative dager (2). Derfor er resultatet i dette tilfellet det samme som resultatet i tilfelle A for dette scenariet, med alle de samme ulempene. Hvis du vil ha en grafisk oversikt over hva som skjer, kan du se tilfelle A for scenario 2.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Tilfelle E: Bruke både antall negative dager som er større enn varens leveringstid, og horisonten for dynamiske negative dager

Dette tilfellet er det samme som tilfelle E for scenario 1 og 2. Det har stort sett de samme fordelene og ulempene.

## <a name="conclusion"></a>Konklusjon

Som de tre scenariene i dette emnet viser, er det lurt å sette de negative dagene til et tall som er større enn leveringstiden for varene i dekningsgruppen. Det er også lurt å bruke bare dynamiske negative dager, og å sette de negative dagene til antallet dager du er villig å vente før du bestiller ny etterfylling, når du har negativ beholdning (med andre ord hvor mange dager du er villig til å forsinke behovet ytterligere). Varer i samme dekningsgruppe bør i tillegg ha lignende leveringstider.

Hvis du setter antall negative dager til **0** (null) og ikke bruker dynamiske negative dager, oppretter MRP alltid en ny planlagt ordre for å oppfylle behov. I denne situasjonen er det viktig at du arbeider med handlingsmeldingene for å være sikker på at beholdningen ikke hoper seg opp.

Det kan være aktuelt å sette de negative dagene til en lang horisont og deretter arbeide med handlingsmeldingene. Denne fremgangsmåten gir gode planleggingsresultater, men er også litt langsommere. Den kan også være vanskeligere å analysere, fordi du må analysere og bruke handlingsmeldingene. Her er et eksempel:

- DemoProduct-varen har en leveringstid for innkjøp på seks dager.
- På dag null (1. januar) er beholdningen for DemoProduct-varen 0 (null).
- På dag null (1. januar) får du en salgsordre for et antall på 10 av DemoProduct-varen.
- På dag ni (10. januar) får du en salgsordre for et antall på 10 av DemoProduct-varen.
- Det finnes en bestilling for et antall på 10 av DemoProduct-varen på dag ellve (12. januar).
- Antall negative dager settes til **20**, som er mye større enn varens leveringstid.

Illustrasjonen nedenfor viser en grafisk visning av hva som skjer.

![Grafisk gjennomgang av eksemplet](./media/negative-days-19.png)

MRP gir følgende resultater.

![Resultateksempel 1](./media/negative-days-20.png)

På skjermbildet ovenfor er behovsdatoen for salgsordren 9. januar i stedet for 10. januar. Siden dette skjermbildet ble tatt i 2015, da 10. januar var en lørdag, skal behovsdatoen for ordren være forrige arbeidsdag, som var fredag 9. januar.

MRP oppretter et bestillingsforslag for å oppfylle behovet som er forespurt i den første salgsordren, men den anbefaler også at du annullerer den planlagte ordren, fordi du kan gå videre med den eksisterende bestillingen og øke antallet i den.

Resultatene er ikke feil, men kjøretiden for MRP kan bli lengre fordi MRP må opprette alle forsinkelsene og forslagene. Det kan også hende at planleggeren trenger mer tid på å forstå MRP-resultatene. Det viktigste i dette tilfellet er at planleggeren forstår og bruker handlingsmeldingene.

Hvis du reduserer de negative dagene til et tall som er nærmere varens leveringstid, og bruker dynamiske negative dager, gir MRP følgende resultater.

![Resultateksempel 2](./media/negative-days-21.png)

MRP oppretter en planlagt ordre som er knyttet til den første salgsordren. Som forventet blir deretter den andre salgsordren låst til den eksisterende bestillingen basert på innstillingen for negative dager. Dette planleggingsresultatet er også riktig, og kjøretiden for MRP er kanskje kortere. I dette tilfellet er det ikke lenger avgjørende at du forstår og vet hvordan du arbeider med handlingsmeldingene.

For å sikre at de riktige verdiene registreres for virksomheten, må du ta hensyn til både funksjonalitet og kjøretid for MRP. Derfor må du kanskje bruke prøve- og feilemetoden til å finne de optimale verdiene.

## <a name="see-also"></a>Se også

Dette diskuteres mer i det opprinnelige blogginnlegget [Mer om (dynamiske) negative dager](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
