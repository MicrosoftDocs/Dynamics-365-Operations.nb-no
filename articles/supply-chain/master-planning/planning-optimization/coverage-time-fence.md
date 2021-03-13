---
title: Dekningshorisonter
description: Dette emnet beskriver hvordan du definerer dekningshorisonter når du bruker planleggingsoptimalisering. En dekningshorisont angir planleggingshorisonten og -grensen.
author: ChristianRytt
manager: tfehr
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f970d7aa9f758d3bc35b7a1b9d1e43be928fd250
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033224"
---
# <a name="coverage-time-fences"></a>Dekningshorisonter

Dette emnet beskriver hvordan du definerer *dekningshorisonter* når du bruker planleggingsoptimalisering. Planleggere kan definere planleggingshorisonten (dekningshorisonten i dager), og utelate forsyning og behov som faller utenfor denne horisonten. Dekningshorisonter kan derfor bidra til å forhindre «støy» som forårsakes av forsyningsforslag det er måneder til du må reagere på. Eksempler omfatter neste års prognose og kundeordrer som er lagt inn med en leveringstid langt utover det normale.

En dekningshorisont er antallet dager etter dagens dato (eller nærmere bestemt datoen du foretar planleggingskjøringen) som forsyning og behov skal utelates. For å unngå forsinkelser må du sørge for at dekningshorisonten er lengre enn den totale leveringstiden. Standardverdien i systemet er 100 dager.

Du kan angi en dekningshorisont på hvert av følgende nivåer:

- **Dekningsgruppe** – Du kan angi en standard dekningshorisont for hver dekningsgruppe.
- **Varedekning** – Du kan overstyre dekningshorisonten som arves fra dekningsgruppen som er tilordnet til en vare.
- **Hovedplan** – Du kan overstyre dekningshorisontene som arves fra innstillingene for dekningsgruppe og varedekning.

Delene nedenfor forklarer hvordan du angir en dekningsgruppe på hvert nivå.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Angi en dekningshorisont for en dekningsgruppe

Når du angir en dekningshorisont for en dekningsgruppe, gjelder innstillingen for alle varer (produkter) som hører til i denne gruppen. Du kan imidlertid overstyre innstillingen for bestemte varer eller bestemte hovedplaner.

Følg denne fremgangsmåten for å angi en dekningshorisont for en dekningsgruppe.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**.
1. Velg eksisterende dekningsgruppe i listen, eller opprett en ny dekningsgruppe.
1. Angi antall dager du vil bruke som dekningshorisonten for dekningsgruppen, i feltet **Dekningshorisont (dager)** i hurtigfanen **Generelt**.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Angi en dekningshorisont for en bestemt vare

Hver vare (produkt) hører til i en dekningsgruppe. Hvis ingen dekningsgruppe er uttrykkelig tilordnet til en vare, brukes en standard dekningsgruppe. Hver vare arver en dekningshorisont fra dekningsgruppen den tilhører. Du kan imidlertid overstyre denne horisonten for bestemte varer etter behov.

Følg denne fremgangsmåten for å angi en dekningshorisont for en bestemt vare.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg et produkt i rutenettet.
1. Velg **Varedekning** i **Dekning**-gruppen i **Plan**-fanen i handlingsruten.
1. Velg eller opprett en rad for området der du vil angi en dekningshorisont, i **Oversikt**-fanen på **Varedekning**-siden.
1. Velg **Generelt**-fanen for å åpne innstillingene for det valgte området.
1. Merk av for **Overstyr dekningsgruppeinnstillinger**.
1. Angi antall dager du vil bruke som dekningshorisonten for varen, i feltet **Dekningshorisont (dager)**.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Angi en dekningshorisont for en bestemt hovedplan

Du kan angi en dekningshorisont på hovedplannivået. På denne måten kan du definere hvor mange dager hovedplanleggingsberegningen dekker for en hovedplan. Denne innstillingen overstyrer alle innstillinger for dekningstid som er definert for hver relevante vare og dekningsgruppe.

Følg denne fremgangsmåten for å angi en dekningshorisont for en bestemt hovedplan.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en eksisterende hovedplan i listen, eller opprett en ny hovedplan.
1. Angi *Ja* for alternativet **Dekning** i hurtigfanen **Horisonter i dager**. Angi deretter antall dager du vil bruke som dekningshorisonten for hovedplanen, i feltet under alternativet.

## <a name="considerations-for-coverage-time-fences"></a>Hensyn ved dekningshorisonter

Når du definerer dekningshorisonter, må du ta hensyn til følgende:

- Dekningshorisonter påvirker bare inndata for hovedplanlegging. Hvis det oppstår forsinkelser, kan de resulterende planlagte ordrene ha en dato som er etter dagens dato pluss dekningshorisonten.
- Dekningshorisonter angis i kalenderdager. Kalendere som bruker virkedager, påvirker ikke beregningen av horisonten. En uke regnes for eksempel alltid som sju dager, selv om helger er definert som lukkede dager i arbeidstidskalenderen.
- Behovstransaksjoner blir ikke generert for forsyning og behov som faller utenfor dekningshorisonten.
- Hvis godkjent forsyning og behov faller utenfor dekningshorisonten, blir den ikke lastet inn i motoren. Den utløser derfor ikke noe etterfylling, og forsinkelser blir ikke beregnet. Denne forsyningen og dette behovet bør likevel ikke slettes fra systemet.
- Variasjoner i sikkerhetslagerantall (fra minimumsnøkler) ignoreres hvis de faller utenfor dekningshorisonten.
- Konserninternt behov ignoreres hvis ønsket forsendelsesdato som beregnes, ikke er innenfor dekningshorisonten. Merk at for innebygd hovedplanlegging er ikke konserninternt behov begrenset av dekningshorisonten.
- Behovsprognoser ignoreres hvis budsjettdatoen ikke er innenfor dekningshorisonten. Merk at for innebygd hovedplanlegging er ikke behovsprognoser begrenset av dekningshorisonten.
- Planleggingsoptimalisering er tidssonefølsom. Den tar hensyn til tidssonen ved forsynings- og behovsområdene, og tidspunktet for planleggingskjøringen. La oss for eksempel si at hovedplanlegging utløses 15. oktober kl. 11 fra et område i Danmark (tidssonen GMT+1), og det brukes en dekningshorisont på ti dager. I dette tilfellet blir forsyning og behov fra et område i Seattle (tidssonen GMT-8) tatt med frem til 25. oktober kl. 02 (= ti 24-timers dager etter at hovedplanleggingen ble utløst, minus tidssonedifferansen på ni timer). Merk at den innebygde hovedplanleggingsmotoren bare tar hensyn til datoen for horisonten. Resultatet kan derfor variere.