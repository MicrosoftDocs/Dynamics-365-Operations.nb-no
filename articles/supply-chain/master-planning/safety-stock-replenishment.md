---
title: Fullføring av sikkerhetslager for varer
description: Dette emnet omhandler fullføring av sikkerhetslager og hvordan du konfigurerer sikkerhetslagerantall for varer.
author: thethehelga
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-oldolg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 28f902c589cd80f1c34dc2758232548309db9aca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474634"
---
# <a name="safety-stock-fulfillment-for-items"></a>Fullføring av sikkerhetslager for varer

[!include [banner](../includes/banner.md)]

Sikkerhetslager angir en tilleggsmengde for en vare i lageret for å redusere risikoen for at varen er utsolgt. Sikkerhetslager brukes som et reservelager i tilfelle salgsordrer kommer inn og leverandøren kan ikke levere flere varer for å oppfylle kundens ønskede leveringsdato. Når sikkerhetslager brukes til å oppfylle en salgsordre, reduseres sikkerhetslagerantallet. Du kan bruke hovedplanlegging å flytte beholdningen automatisk tilbake til sikkerhetsnivået.

## <a name="set-up-safety-stock-levels-for-items"></a>Definere sikkerhetslagernivåer for varer

Sikkerhetslager er definert som en del av varedekning på siden **Varedekning** under **Frigitte produkter \> Plan \> Dekning**.

Angi sikkerhetslagernivået som du vil opprettholde for varen, i feltet **Minimum**. Verdien uttrykkes i lagerenheter. Hvis du lar dette feltet være tomt, er standardverdien null. Dette feltet er tilgjengelig når du velger **Periode**, **Behov** eller **Min/maks** i **Dekningskode**-listen. Lagernivågrensen gjelder for tilgjengelig beholdning, som betyr at reservasjoner og merkinger kan utløse etterfylling av sikkerhetslageret før det fysiske antallet kommer under det angitte minimumsnivået.

> [!NOTE]
> Du må definere alle andre planlagte dekningsdimensjoner før du kan definere **Minimum**-feltet. Dette forhindrer at en ugyldig post brukes under hovedplanlegging. Denne situasjonen kan for eksempel oppstå hvis en dimensjonsgruppe blir utvidet med en ekstra planlagt dekningsdimensjon som det ennå ikke er definert minimums- og maksimumslagerantall for.

Du kan bruke minimumsnøkler til å håndtere sesongbetont variasjon i etterspørselen. Du kan for eksempel redusere minimumslagernivået for en vare i lavsesongen og deretter gradvis øke nivået i de under de andre månedene. Du oppretter en minimumsnøkkel ved å gå til **Hovedplanlegging \> Oppsett \> Dekning \> Minimums-/maksimumsnøkler**. Du angir minimumsnøkkelen for å justere sikkerhetslagernivået etter årstid i feltet **Minimumsnøkkel** på siden **Varedekning**.

## <a name="example-minimum-key"></a>Eksempel: Minimumsnøkkel

Følgende fremgangsmåte er et eksempel som viser hvordan du definerer en minimumsnøkkel som står for økt sesongetterspørsel i vår- og sommermånedene.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Minimums-/maksimumsnøkler**.
1. Velg **Ny** for å opprette en minimums-/maksimumsnøkkel.
1. I feltet **Minimums- eller maksimumsnøkkel** angir du en ID for nøkkelen. I **Navn**-feltet angir du et navn på nøkkelen.
1. Sett alternativet **Bruk gyldig dato** til *Ja*, og la feltet **Ikrafttredelsesdato** stå tomt for å gjøre nøkkelen gyldig fra første dag i gjeldende år.

    > [!NOTE]
    > Kombinasjonen av innstillingene **Bruk gyldig dato** og **Ikrafttredelsesdato** definerer datoen som nøkkelen er gyldig fra.
    >
    > - Når alternativet **Bruk gyldig dato** er satt til *Nei*, er nøkkelen gyldig fra gjeldende dato eller systemdatoen.
    > - Når alterantivet **Bruk gyldig dato** er satt til *Ja*, er nøkkelen gyldig fra datoen som er definert i feltet **Ikrafttredelsesdato**.

1. Opprett 12 linjer i **Perioder**-delen, og angi følgende verdier for dem:

    - **Endre** – Tilordne hver linje et unikt nummer fra 1 til og med 12. Dette feltet angir en trinnvis endring i tidsenheten som defineres av **Enhet**-feltet.
    - **Enhet** – Velg *Måneder* for hver linje.
    - **Fra dato**, **Til dato** og **Måned** – Disse feltene angis automatisk, basert på innstillingene for **Endre** og **Enhet**. Månedlige perioder starter fra den første dagen i gjeldende år.
    - I **Faktor** – Angi verdiene som er beskrevet i tabellen nedenfor. Dette feltet definerer faktoren du vil multiplisere minimumslageret med.

        | Linje (endring) | Omregningsfaktor | Resultat |
        |---|---|---|
        | 1–3 | 1 | Minimumslager er basert på innstillingen for januar til mars på siden **Varedekning**. |
        | 4–5 | 2 | Minimumslager ganges med 2 for april og mai. |
        | 6–8 | 2.5 | Minimumslager ganges med 2,5 for juni til august. |
        | 9–12 | 1 | Minimumslager går tilbake til innstillingen for september til desember på siden **Varedekning**. |

    Innstillingene skal nå ligne på innstillingene i illustrasjonen nedenfor.

    ![Minimums- eller maksimumsnøkkelperioder.](media/min-max-key-periods.png "Minimums- eller maksimumsnøkkelperioder")

> [!NOTE]
> Du kan også bruke en veiviser til å opprette og definere en minimums-/maksimumsnøkkel. På siden **Minimums- eller maksimumsnøkler** i handlingsruten velger du **Veiviser** for å åpne veiviseren **Minimums-/maksimumsnøkler**. Veiviseren leder deg trinnvis gjennom prosessen med å opprette og definere minimums-/maksimumsnøkkelen.

Hvis dekningskoden er *Min/maks*, kan du også angi lagerbeholdningen for Maksimum som du vil opprettholde for en vare. Verdien uttrykkes også i lagerenheter. Hvis fremtidig tilgjengelig lagerbeholdning synker til under minimumsantallet, genererer hovedplanleggingen en planlagt bestilling for å oppfylle alle åpne behov og bringer lagernivået tilbake opp til det angitte maksimumsantallet. Akkurat som da du definerte minimumslagerantallet, må du definere alle andre planlagte dekningsdimensjoner før du kan definere **Maksimum**-feltet.

## <a name="example-minmax-coverage-code"></a>Eksempel: Dekningskoden Min/maks

Minimumsantallet er 10 og maksimumsantallet er 15. Nåværende lagerbeholdning er 4. Dette gir et minimumsbehov for antall på 6. Men siden maksimumsantallet er 15, genererer hovedplanleggingen en planlagt bestilling på 11 varer.

For varer som kommer etter sesongbaserte behov, kan du bli nødt til å opprettholde forskjellige maksimumsnivåer. For å gjøre dette må du definere **Maksimumsnøkler** ved å gå til **Hovedplanlegging \> Oppsett \> Dekning \> Minimums-/maksimumsnøkler**. Fyll ut feltet **Maksimumsnøkkel** på siden **Varedekning**. Du kan vise informasjon om sikkerhetslagernivåer, definert via minimumsnøklene på fanen **Min/maks** på siden **Varedekning**. Du må du kontrollere at minimums- og maksimumsverdiene holdes synkronisert, for en bestemt periode.

## <a name="safety-stock-fulfillment"></a>Fullføring av sikkerhetslager

Med parameteren **Fyll opp minimum** kan du velge datoen eller perioden der lagernivået må oppfylle antallet du har angitt i **Minimum**-feltet. Dette feltet er tilgjengelig når du velger **Periode**, **Behov** eller **Min/maks** i **Dekningskode**-listen.

Hvis **Minimumsnøkler** er brukt, merker du av for **Minimumsperioder** for å oppfylle minimumslagernivået for alle periodene som er definert i minimumsnøkkelen. Hvis du fjerner merket i boksen, fylles minimumslageret bare opp for den aktuelle perioden.

Dette scenariet viser hvordan denne parameteren fungerer, og hva som er forskjellen mellom verdiene.

> [!NOTE]
> For alle illustrasjonene i dette emnet representerer x-aksen lager, y-aksen dager, linjene lagernivået, pilene transaksjoner, for eksempel salgsordrelinjer, bestillingslinjer eller planlagte ordrer.

[![Vanlig scenario for fullføring av sikkerhetslager.](media/Scenario1.png)](media/Scenario1.png)

**Fyll opp minimum**-parameteren kan ha følgende verdier:

### <a name="todays-date"></a>Dagens dato

Det angitte minimumsantallet er oppfylt på datoen når hovedplanleggingen kjøres. Systemet prøver å oppfylle sikkerhetslagergrensen så snart som mulig, selv om den kan være urealistisk på grunn av leveringstiden.

[![Behov for dagens dato.](media/TodayReq.png)](media/TodayReq.png)

Planlagt bestilling P1 opprettes for dagens dato for å brunge tilgjengelig beholdning over sikkerhetslagernivået på denne datoen. Salgsordrelinjene S1 til S3 fortsetter å senke lagernivået. Planlagte bestillinger P2 til P4 genereres av hovedplanleggingen slik at lagernivået bringes tilbake til sikkerhetsgrensen etter behovet for hver salgsordre.

Når dekningskoden **Krav** brukes, opprettes flere planlagte bestillinger. Det er alltid lurt å bruke dekningen **Periode** eller **Min/maks** for varer og materialer som det ofte er behov for, for å kunne etterfylle i grupper. Illustrasjonen nedenfor viser et eksempel på dekningskoden **Periode**.

[![Periode. Dagens dato.](media/TodayPeriod.png)](media/TodayPeriod.png)

Illustrasjonen nedenfor viser et eksempel på dekningskoden **Min/maks.**.

[![Min/maks. Dagens dato.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Dagens dato + leveringstid

Det angitte minimumsantallet er oppfylt på datoen da hovedplanleggingen er kjørt, pluss leveringstiden for innkjøp eller produksjon. Denne tiden omfatter eventuell sikkerhetsmarginer. Hvis det finnes en forretningsavtale for varen, og du har merket av for **Finn forretningsavtaler** på siden **Hovedplanleggingsparametere**, blir ikke leveringstiden fra forretningsavtalen tatt i betraktning. Leveringstiden hentes fra varens dekningsinnstillinger eller fra selve varen.

Denne oppfyllingsmodusen oppretter planer med mindre forsinkelser og færre planlagte bestillinger, uavhengig av dekningsgruppen som er definert for varen.

Illustrasjonen nedenfor viser resultatet av planen hvis dekningskoden er **Krav** eller **Periode**.

[![Krav eller Periode. Dagens dato og leveringstid.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Illustrasjonen nedenfor viser resultatet av planen hvis dekningskoden er **Min/maks**.

[![Min/maks. Dagens dato og leveringstid.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Første avgang

Det angitte minimumsantallet er oppfylt på datoen når det tilgjengelige lageret går under minimumsnivået, som vist i illustrasjonen nedenfor. Selv om det tilgjengelige lageret er under minimumsnivået på datoen når hovedplanlegging kjøres, vil **Første avgang** ikke forsøke å dekke dette før det neste behovet kommer inn.

Illustrasjonen nedenfor viser et eksempel på dekningskoden **Krav**.

[![Planlegge en vare med dekningskoden Krav og Første avgang.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Illustrasjonen nedenfor viser et eksempel på dekningskoden **Periode**.

[![Planlegge en vare med dekningskoden Periode og Første avgang.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Illustrasjonen nedenfor viser et eksempel på dekningskoden **Min/maks.**.

[![Planlegge en vare med dekningskoden Min/maks. og Første avgang.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

På datoen når hovedplanleggingen kjøres, vil **Dagens dato** og **Dagens dato + leveringstid** utløse etterfyllingen umiddelbart, hvis den tilgjengelige beholdningen allerede er under sikkerhetslagergrensen. **Første avgang** venter til det er en annen avgangstransaksjon, for eksempel en salgsordre og stykklistelinjebehov, for varen, og deretter utløses etterfyllingen på datoen for denne transaksjonen.

På datoen når hovedplanleggingen kjøres, vil **Dagens dato** og **Første avgang** gi nøyaktig det samme resultatet, som vist i illustrasjonen nedenfor, hvis den tilgjengelige beholdningen ikke er under sikkerhetslagergrensen.

[![Ikke under grense.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

På datoen når hovedplanleggingen kjøres, vil **Dagens dato + leveringstid** gi følgende resultat, fordi det utsetter oppfyllingen til slutten av leveringstiden for etterfyllingen, hvis den tilgjengelige beholdningen ikke er under sikkerhetslagergrensen.

![Innfrielse utsatt til slutten av leveringstiden for innkjøpet.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Dekningshorisont

Det angitte minimumsantallet er oppfylt innenfor perioden som er angitt i feltet **Dekningshorisont**. Dette alternativet er nyttig når hovedplanlegging ikke tillater at tilgjengelig beholdning brukes for reelle bestillinger, for eksempel salg eller overføringer, under forsøk på å opprettholde sikkerhetsnivået. Imidlertid i en fremtidig versjon, vil ikke lenger trenge denne modusen for etterfylling, og dette alternativet vil avverges.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Planlegge etterfylling av sikkerhetslager for varer av typen først utløpt først ut (FEFO)

Når som helst kan lagermottaket med den nyeste utløpsdatoen brukes for sikkerhetslageret, slik at reell etterspørsel, for eksempel salgslinjer eller stykklistelinjer, kan oppfylles i FEFO-rekkefølgen (først utløpt, først ut).

Hvis du vil se hvordan dette fungerer, kan du se følgende scenario.

[![FEFO-scenario.](media/FEFOScenario.png)](media/FEFOScenario.png)

Når planleggingen kjører, dekkes den første salgsordren fra den eksisterende lagerbeholdningen og en ny bestilling for det gjenværende antallet.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

En planlagt bestilling opprettes for å sikre at den tilgjengelige beholdningen importeres tilbake til sikkerhetsgrensen.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Når den andre salgsordren er planlagt, brukes den tidligere opprettede planlagte ordren som dekker sikkerhetslageret, til å dekke dette antallet. Derfor rulleres sikkerhetslageret konstant.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Til slutt opprettes en annen planlagt ordre for å dekke sikkerhetslageret.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Alle partiene utløper i henhold til dette, og planlagte ordrer opprettes for å etterfylle sikkerhetslageret etter det har utløpt.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Hvordan hovedplanlegging håndterer begrensningen for sikkerhetslageret

Sikkerhetslageret spores i systemet som en behovstype, akkurat som salgslinjer eller stykklistebehov. Du kan se linjen for sikkerhetslagerbehovet på siden **Nettobehov** hvis du fjerner standardfilteret i kolonnen **Behovstype**.

Oppfylling av behovstransaksjonen for sikkerhetslageret er ikke prioritert hvis systemet finner ut at dette forårsaker forsinkelser i oppfyllingen av reelt behov, for eksempel salgslinjer, stykklistelinjer, krav for overføring eller behovsprognose. Hvis ikke, vil kontrollering av at den tilgjengelige beholdningen er over sikkerhetslagerantallet, ha samme prioritet som andre behovstyper. Dette sikrer at det ikke oppstår forsinkelser for reelle transaksjoner, og forhindrer overetterfylling og for tidlig etterfylling av sikkerhetslageret.

Under dekningsfasen i hovedplanlegging er ikke etterfylling av sikkerhetslageret lenger underprioritert. Lagerbeholdningen kan brukes før eventuelle andre behovstyper. Under forsinkelsesberegningen legges den nye logikken til over de forsinkede salgslinjene, stykklistelinjebehovene og alle de andre behovstypene, for å bestemme om de kan leveres innen tidsfristen, forutsatt at sikkerhetslageret brukes. Hvis systemet identifiserer at det kan redusere forsinkelser ved å bruke sikkerhetslageret, vil salgslinjene eller stykklistelinjene erstatte den opprinnelige dekningen med sikkerhetslageret, og systemet vil utløse etterfylling for sikkerhetslageret i stedet.

Hvis planen eller varen ikke er definert for forsinket beregning, vil sikkerhetslagerbegrensningen ha samme prioritet som andre behovstyper. Dette betyr at det er en reserve med lagerbeholdning og annen tilgjengelige beholdning før andre behovstyper.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
