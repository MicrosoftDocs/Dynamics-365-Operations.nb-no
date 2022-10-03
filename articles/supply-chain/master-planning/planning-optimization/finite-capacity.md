---
title: Planlegge og tidsplanlegge med begrenset kapasitet
description: Planlegging og tidsplanlegging med begrenset kapasitet hjelper deg å forstå hvor mye arbeid som kan produseres i løpet av en bestemt periode når det tas hensyn til begrensninger på ulike ressurser.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c5eebe9ef6258b43daa7c7007ee28b0278fe5b09
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573139"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Planlegge og tidsplanlegge med begrenset kapasitet

[!include [banner](../../includes/banner.md)]

Begrenset kapasitet er en tilnærming som hjelper deg å forstå hvor mye arbeid som kan produseres i løpet av en bestemt periode når det tas hensyn til begrensninger på ulike ressurser. Formålet med planlegging med begrenset kapasitet er å sikre at arbeidet pågår jevnt og effektivt på hele anlegget.

Planlegging og tidplanlegging med begrenset kapasitet oppretter en mer realistisk plan for produksjonsprosessene enn den ubegrensete tilnærmingen. Hvis det ikke er nok kapasitet på ressursene, blir leveringsdatoen forskjøvet, og jobben blir planlagt når det er nok kapasitet.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Planleggingsoptimaliseringsstøtte for begrenset kapasitetsplanlegging

Planlegging og tidsplanlegging med begrenset kapasitet fungerer på nesten samme måte, uansett om du bruker planleggingsoptimalisering eller den innebygde hovedplanleggingsmotoren. Planleggingsoptimalisering bruker imidlertid ikke horisontparameteren **flaskehalshorisont**. Når du bruker planleggingsoptimalisering, planlegges alltid flaskehalsressurser ved å bruke den samme tidshorisonten som ikke-flaskehalsressurser (som angitt av den horisonten for begrensede kapasitet).

## <a name="set-up-finite-capacity-functionality"></a>Definere funksjonalitet for begrenset kapasitet

Hvis du vil bruke funksjonalitet for begrenset kapasitet, må du aktivere kapasitetsplanlegging globalt, og du må aktivere planlegging med begrenset kapasitet både for hovedplanen der du vil bruke den, og for hver ressurs den gjelder. For planer og ressurser der begrenset kapasitet er aktivert, blir kapasitet som allerede er reservert for planleggingen av de planlagte produksjonsordrene, tatt med i betraktning. Planlagte produksjonsordrer planlegges i omvendt rekkefølge ut fra behovsdatoen. Hvis kapasitet ikke er tilgjengelig for å oppfylle den optimale planen, vil systemet prøve å kreve komponentelementer på en tidligere dato. Hvis kapasiteten kan endres i henhold til når behov endres (for eksempel ved skiftarbeid), bør du ikke bruke begrenset kapasitet, fordi det da vil oppstå feil i de beregnede behandlingstidene. Planlegging tar bare forhåndsreservert kapasitet med i betraktningen for ressurser der begrenset kapasitet er aktivert. Ved å aktivere begrenset kapasitet for en ressurs gjør du det mulig å endre den begrensede kapasitetshorisonten.

### <a name="activate-master-planning-parameters"></a>Aktivere parametere for hovedplanlegging

Hvis du vil bruke funksjonaliteten for begrenset kapasitet, må du aktivere kapasitetsplanlegging på siden **Parametere for hovedplanlegging**.

1. Gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**.
1. Sett **Produksjon**-alternativet til **Ja** i **Kapasitetsplanlegging**-delen i kategorien *Planlagte bestillinger*.

### <a name="activate-a-master-plan"></a>Aktivere en hovedplan

Du må aktivere planlegging og tidsplanlegging for begrenset kapasitet for hver hovedplan der du vil bruke den.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en hovedplan som du vil konfigurere til å bruke begrenset kapasitetsplanlegging og planlegging, i listeruten.
1. Sett **Begrenset kapasitet**-alternativet til **Ja** i **Planlagte produksjonsordrer**-delen i hurtigfanen *Generelt*.
1. Gjenta trinn 2 og 3 for hver ytterligere hovedplan som du vil konfigurere.

### <a name="activate-resources"></a>Aktivere ressurser

Du må aktivere planlegging og tidsplanlegging for begrenset kapasitet for hver ressurs der du vil bruke den.

1. Gå til **Produksjonskontroll \> Oppsett \> Ressurser \> Ressursfunksjoner**.
1. Velg en ressurs som du vil konfigurere til å bruke begrenset kapasitetsplanlegging og planlegging, i listeruten.
1. I hurtigfanen **Operasjon** i delen **Kapasitetsknapp** angir du alternativet **Begrenset kapasitet** til *Ja*.
1. Gjenta trinn 2 og 3 for hver ytterligere ressurs som du vil konfigurere.

## <a name="examples"></a>Eksempler

Denne delen inneholder følgende eksempler som viser hvordan du arbeider med både ubegrenset og begrenset kapasitetsplanlegging og -planlegging:

- Eksempel 1 – Ubegrenset kapasitetsplanlegging
- Eksempel 2 – Planlegging med begrenset kapasitet med en horisont på én dag
- Eksempel 3 – Planlegging med begrenset kapasitet med en horisont på to dager

### <a name="preconditions"></a>Forhåndskrav

Alle de tre eksemplene forutsetter forutsetningene som er beskrevet i denne delen.

Produkt *Produkt1* har en rute som inneholder følgende operasjoner.

| Operasjonsnr. | Operasjonsnavn | Ressurs        | Kjøretid | Prosessantall | Neste |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Sveising        | Sveiselinje    | 1        | 2            | 20   |
| 20            | Monterer     | Monteringslinje | 1        | 4            |      |

Arbeidere i ditt firma arbeider i ett skift i åtte timer (8:00–16:00).

Det er en planlagt produksjonsordre for *24 stk.* av *produkt1*. Den har leveringsdato *I dag + 3 dager*.

Som et resultat av planleggingen laster systemet inn ressursene på følgende måte:

- **Sveiselinje:** Denne ressursen lastes fra *I dag klokken 8:00* til *I dag + 1 kl. 12:00*.
- **Monteringslinje:** Denne ressursen lastes fra *I dag + 1 kl 12:00* til *I dag + 2 kl 10:00*.

Illustrasjonen nedenfor viser det resulterende Gantt-diagrammet (velg det for en større visning).

[![Gantt-diagram som viser forutsetninger.](media/finite-examples-conditions-small.png "Gantt-diagram som viser forutsetninger")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Eksempel 1 – Ubegrenset kapasitetsplanlegging

Dette eksemplet viser planleggingsresultatene når du bruker ubegrenset kapasitetsplanlegging i stedet for begrenset kapasitetsplanlegging.

Hovedplanen har følgende relevante innstilling, som deaktiverer begrenset kapasitetsplanlegging for planen:

- **Begrenset kapasitet:** *Nei*

Alternativet **Begrenset kapasitet** er også angitt til *Nei* for begge de relevante ressurser for å deaktivere begrenset kapasitetsplanlegging for dem:

- Sveiselinje
- Monteringslinje

Nå legger du til en ny salgsordre for *8 stk* av *Produkt1*, og kjører planen. Systemet laster nå salgslinjen fra *I dag klokken 8:00* til *I dag klokken 12:00*. Når operasjonene på sveiselinjen er fullført, laster systemet inn monteringslinjen fra *i dag klokken 12:00* til *I dag klokken 14:00*.

Illustrasjonen nedenfor viser det resulterende Gantt-diagrammet (velg det for en større visning).

[![Gantt-diagram som viser et eksempel på ubegrenset kapasitetsplanlegging.](media/finite-examples-example1-small.png "Gantt-diagram som viser et eksempel på ubegrenset kapasitetsplanlegging")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Eksempel 2 – Planlegging med begrenset kapasitet med en horisont på én dag

Dette eksemplet viser planleggingsresultatene når du bruker begrenset kapasitetsplanlegging og en tidsgrense på én dag.

Hovedplanen har følgende relevante innstillinger, som aktiverer begrenset kapasitetsplanlegging og angir en tidsgrense for planen:

- **Begrenset kapasitet:** *Ja*
- **Horisont for begrenset kapasitet:** *1*

Alternativet **Begrenset kapasitet** er også angitt til *Ja* for begge de relevante ressurser for å aktivere begrenset kapasitetsplanlegging for dem:

- Sveiselinje
- Monteringslinje

Nå legger du til en ny salgsordre for *8 stk* av *Produkt1*, og kjører planen. Systemet laster nå salgslinjen fra *I dag + 1 kl 8:00* til *I dag + 1 kl 12:00*. Når operasjonene på sveiselinjen er fullført, laster systemet inn monteringslinjen fra *i dag + 1 kl 12:00* til *I dag + 1 kl 14:00*. Systemet vurderer den begrensede kapasiteten bare for én dag.

Illustrasjonen nedenfor viser det resulterende Gantt-diagrammet (velg det for en større visning).

[![Gantt-diagram som viser begrenset kapasitetsplanlegging med en horisont på én dag.](media/finite-examples-example2-small.png "Gantt-diagram som viser begrenset kapasitetsplanlegging med en horisont på én dag")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Eksempel 3 – Planlegging med begrenset kapasitet med en horisont på to dager

Dette eksemplet viser planleggingsresultatene når du bruker begrenset kapasitetsplanlegging og en tidsgrense på to dager.

Hovedplanen har følgende relevante innstillinger, som aktiverer begrenset kapasitetsplanlegging og angir en tidsgrense for planen:

- **Begrenset kapasitet:** *Ja*
- **Horisont for begrenset kapasitet:** *2*

Alternativet **Begrenset kapasitet** er også angitt til *Ja* for begge de relevante ressurser for å aktivere begrenset kapasitetsplanlegging for dem:

- Sveiselinje
- Monteringslinje

Nå legger du til en ny salgsordre for *8 stk* av *Produkt1*, og kjører planen. Systemet laster nå salgslinjen fra *I dag + 1 kl 12:00* til *I dag + 1 kl 16:00*. Når operasjonene på sveiselinjen er fullført, laster systemet inn monteringslinjen fra *i dag + 2 kl 8:00* til *I dag + 2 kl 10:00*. Systemet vurderer den begrensede kapasiteten bare for to dager.

Illustrasjonen nedenfor viser det resulterende Gantt-diagrammet (velg det for en større visning).

[![Gantt-diagram som viser begrenset kapasitetsplanlegging med en horisont på to dager.](media/finite-examples-example3-small.png "Gantt-diagram som viser begrenset kapasitetsplanlegging med en horisont på to dager")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Du bør alltid angi den begrensede kapasitetshorisonten etter behov for å dekke dine forretningsbehov. Eksemplene som oppgis i denne artikkelen, viser bare funksjonaliteten. I realiteten er en enkeltdagshorisont sannsynligvis for lav for de fleste produsenter som bruker begrenset kapasitetsplanlegging.
