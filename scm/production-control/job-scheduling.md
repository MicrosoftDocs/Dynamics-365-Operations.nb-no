---
title: Finplanlegging
description: "Denne artikkelen inneholder informasjon om finplanlegging, som er en mer detaljert versjon av planlegging enn grovplanlegging. Du kan bruke jobbplanlegging for å planlegge individuelle jobber eller butikkordrer og styre produksjonsmiljøet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 99348a2e4a08af1107841cb211a138105fcac9ff
ms.lasthandoff: 03/31/2017


---

# <a name="job-scheduling"></a>Finplanlegging

Denne artikkelen inneholder informasjon om finplanlegging, som er en mer detaljert versjon av planlegging enn grovplanlegging. Du kan bruke jobbplanlegging for å planlegge individuelle jobber eller butikkordrer og styre produksjonsmiljøet.

Du kan bruke jobbplanlegging for å planlegge individuelle jobber eller butikkordrer og styre produksjonsmiljøet. Finplanlegging deler hver operasjon inn i individuelle oppgaver eller jobber. Disse jobbene tilordnes deretter til operasjonsressursene som skal utføre dem. Finplanlegging lar deg også synkronisere alle jobber som er referert til av den valgte jobben. Du kan angi startdato og -klokkeslett eller sluttdato og -klokkeslett for jobben, og deretter kjøre planleggingen. Tidspunktet du angir, kan være start- eller sluttidspunktet, avhengig av planleggingsretningen. Denne funksjonen er nyttig når for eksempel en jobb bare kan kjøres på én maskin om gangen, eller når du ønsker å optimere jobben som kjøres for hver ressurs.

## <a name="tasks-in-the-job-scheduling-process"></a>Oppgaver i finplanleggingsprosessen
Finplanleggingsprosessen omfatter følgende oppgaver:

-   Dele operasjoner inn i jobber.
-   Planlegge jobber, basert på datoene og klokkeslettene for ressursene som er angitt for den tilknyttede operasjonen.
-   Beregne start- og sluttidspunkter for hver jobb. Du kan bruke begrenset kapasitet for å være sikker på at det ikke finnes tidsoverlapping.
-   Avgjøre hvilke ressurser i ressursgruppen til å kjøre jobben på. Denne oppgaven krever at det angis en ressursgruppe for en operasjon. Finplanlegging velger ressurser eller ressursgrupper basert på kortest leveringstid og vurderer også eventuelle tidligere reserveringer for ressursene.
-   Dele opp operasjoner i jobber når du kjører finplanlegging. Jobbene planlegges etter dato og klokkeslett i den rekkefølgen som er angitt av produksjonsruten. Oppsettet for operasjonen bestemmer jobbene som deles opp i planleggingsprosessen. Rutegruppen som er tilordnet til operasjonen, kontrollerer om jobber genereres. En jobb genereres bare hvis den har en viss varighet. En transporttidsjobb genereres for eksempel hvis transporttid er angitt for den valgte operasjonen.

## <a name="scheduling-direction"></a>Planleggingsretning
Du kan planlegge jobber fremover eller bakover.

-   **Fremover** – Bruk fremover planleggingsretningen for å starte produksjonen så tidlig som mulig. Dette kalles også for fremskyvningsmetoden, fordi produksjonen skyves fremover i produksjonsprosessen. Produksjonen planlegges å starte og slutte på de tidligste mulige datoene.
-   **Bakover** – Bruk bakover planleggingsretningen for å starte produksjonen så sent som mulig. Dette er også kjent som trekkmetoden, fordi den er basert på datoen når produksjonen må være fullført. Planlegging bakover teller tilbake til den seneste mulige datoen da produksjonen kan startes uten at det ødelegger for tidsfristen.

## <a name="finite-capacity"></a>Begrenset kapasitet
Du kan planlegge jobber ved hjelp av begrenset kapasitet. Når du bruker begrenset kapasitet, kan ikke kapasitet som er planlagt, være større enn kapasiteten som er tilgjengelig for ressursen. Tilgjengelig tid er definert som intervallet når ressursen er tilgjengelig og der det ikke er noen andre reserveringer på kapasiteten. Planlegging som er basert på begrenset kapasitet sikrer at start- og sluttidspunkt for en operasjon på en bestemt dato ikke overlapper. Ressurskapasiteten som allerede er reservert, vurderes, og overlappinger mellom starttidspunkt og sluttidspunkt, vurderes også. Begrenset kapasitet fastsetter hvor mye kapasitet som må være tilgjengelig for en ressurs for å oppnå full nytte av den ressursen. Denne fastsettelsen balanseres mot en beregning av den korteste mulig leveringstiden mellom operasjoner.

## <a name="finite-materials"></a>Begrensede materialer
Finplanlegging som er basert på begrenset materiale, sørger for at de nødvendige materialene er tilgjengelige når operasjonen starter. Dekningsregler for varer definerer disse grensene. Planlegging bruker behovsnedbryting til å bestemme når komponentvarene er tilgjengelige. Hvis du planlegger uten å angi begrensede materialer, vil systemet anta at alle varer er tilgjengelige etter behov.

## <a name="finite-properties"></a>Begrensede egenskaper
Finplanlegging som er basert på spesielle egenskaper, krever at egenskapene angis for operasjonene på produksjonsruten. Disse egenskapene må oppfylles for å reservere kapasitet.

## <a name="references"></a>Referanser
Jobbplanlegging planlegger alle produksjoner som det refereres til av den gjeldende produksjonen. Hvis en produksjon har én eller flere underproduksjoner, bør underproduksjonene planlegges på samme tid som hovedproduksjonen, fordi hovedproduksjonen ikke kan startes før de relaterte underproduksjonene er ferdige.

## <a name="schedule-resources"></a>Planlegg ressurser
Planleggingsmotoren undersøker kombinasjoner av ressurser for å identifisere kombinasjonene som kan tilfredsstille kravene. Du kan angi utvalgskriterier ved å velge én av følgende verdier i feltet **Valg av primærressurs** på siden **Planleggingsparametere**:

-   **Varighet** – planleggingsmotoren velger ressursen med kortest leveringstid. **Obs!** Planlegging etter varighet kan føre til redusert ytelse når samme ressursgruppe inneholder mange ressurser og sekundære arbeidssentre brukes. Du kan planlegge maksimalt 32 ressurser per operasjon. Hvis du overskrider dette antallet, vises en infologgmelding, og finplanlegging finner ikke den beste alternative ressursen.
-   **Prioritet** – planleggingsmotoren velger ressursen som har høyest prioritet hvis to eller flere ressurser har identiske egenskaper og nivåer. Ressursen som har den laveste numeriske verdien i dette feltet har høyest prioritet.

Når finplanlegging kjøres, planlegger systemet ressursene basert på begrensningene som er definert i ressursparameterne. Du kan styre kapasiteten for ressurser ved hjelp av kalenderinnstillingene. Systemet beregner belastningen for ressurser under planleggingsprosessen. **Obs!** For produksjonsprosesser som bruker grovplanleggingsfunksjonen, kan du kjøre finplanlegging etter grovplanlegging. Hvis du ikke bruker grovplanlegging, kan du kjøre finplanlegging alene.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Maksimale kapasiteter for ressurser per jobbordre
Ressurser tilordnes til jobber via finplanlegging. Du kan opprette maksimale kapasiteter for ressurser per jobbordre. Du kan for eksempel definere systemet for å planlegge ikke mer enn 50 prosent av samlet kapasitet for en produksjonsordre. Dette oppsettet gir deg mer kontroll over planlegging av ressurser på finplanleggingsnivå. Derfor kan det forhindre problemer hvis det ikke finnes nok kapasitet for å utføre flere produksjonsprosesser samtidig.

## <a name="resource-efficiency"></a>Ressurseffektivitet
Finplanlegging tar hensyn til effektivitetsprosenter som er angitt for ressursene. Effektivitetsprosenter reduserer eller øker tiden som er reservert for ressursen. Derfor blir også leveringstiden økt eller redusert. Følgende formel brukes ved beregningen: Planleggingstid = tid x 100 ÷ effektivitetsprosenten. I denne formelen inneholder *tid* både kjøretiden og oppstillingstiden.


