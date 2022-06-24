---
title: Postering av indirekte kostnader
description: Denne artikkelen beskriver hvordan du posterer indirekte kostnader, oppretter kostgrupper og legger til noder i kostarket for indirekte kostnader.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868438"
---
# <a name="indirect-cost-posting"></a>Postering av indirekte kostnader

Indirekte kostnader er kostnader som ikke er direkte relatert til noen enkeltaktivitet i produksjonsprosessen. Eksempler inkluderer administrative kostnader, som ansattes lønn, regnskapsavdelingskostnader og administrasjonskostnader som husleie, strømutgifter og maskinkostnader.

## <a name="calculating-indirect-costs"></a>Beregne indirekte kostnader

Microsoft Dynamics 365 Finance har ingen automatisert måte å beregne satsen for indirekte kostnader på. Du må bestemme indirekte kostnader, opprette indirekte kostnadskoder og vedlikeholde satsen for hver indirekte kostnad i kostarket.

Den nøyaktige prosessen som brukes til å beregne indirekte kostnader, kan variere litt fra firma til firma. Generelt består imidlertid prosessen av følgende grunnleggende trinn:

1. Opprett en liste over indirekte kostnader som skal gjenkjennes i produksjonen. Denne listen kan omfatte husleie, administrative utgifter, regnskapsgebyrer og juridiske gebyrer. Den bør ikke inneholde råvarekostnader eller arbeidskostnader som gjenkjennes i produksjonsruter.
2. Summer alle indirekte kostnader. Du kan gruppere lignende typer indirekte kostnader, eller holde dem atskilt. Hver indirekte kostnad som konfigureres, kan ha ulike hovedkontoer som brukes til postering til økonomimodulen.
3. Sammenlign de indirekte kostnadene med en faktor, som også omtales som absorpsjonsgrunnlaget. Faktoren kan være noe du velger. Her er noen få vanlige eksempler:

    - Inntekt
    - Totalt antall som er produsert
    - Oppstillingstid
    - Kjøretid

    Du kan velge perioden du vil beregne indirekte kostnader for, for eksempel månedlig, kvartalsvis eller årlig. Summen av de indirekte kostnadene og summen av faktoren bør være på samme tid. Følgende formel brukes til å beregne den indirekte kostnadssatsen:

    *Indirekte kostnadssats* = *Totale indirekte kostnadsutgifter* &divide; *Total faktor*

4. Opprette indirekte kostnadsgrupper.
5. Konfigurer kostarket med satsene.
6. Vedlikehold kostnadene for de indirekte kostnadene i etterkalkuleringsversjonen.

> [!NOTE]
> Du kan bruke **Kostnadsregnskap**-modulen til å akkumulere kostnader og bestemme administrasjonskostnader fra ulike kilder, for eksempel produksjon, prosjekter og økonomimodulen. Hvis du vil ha mer informasjon, kan du se [Kostnadsregnskap](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Ulike reguleringsvirksomheter har publisert retningslinjer om hvilke typer kostnader som kan inkluderes som indirekte kostnader eller indirekte kostnader i kostnaden av ferdigvarene. Før du begynner å konfigurere indirekte kostnader, anbefaler vi at du sjekker med regnskapsføreren og lokale bestemmelser for å sikre at du er i overensstemmelse.

## <a name="create-cost-groups-for-indirect-costs"></a>Opprette kostnadsgrupper for indirekte kostnader

Du må opprette minst én kostgruppe som skal brukes for indirekte kostnader. Det er ingen begrensninger på hvor mange kostgrupper du kan bruke. Vurder hvordan du beregner kostnadene, og om det er ulike satser for ulike kostnadstyper. Organisasjonen produserer for eksempel matprodukter. Noen råvarer og ferdigvarer er tørrvarer og har én indirekte kostnad for lager. Andre råvarer og ferdigvarer blir nedkjølt og har en høyere indirekte kostnad. I dette tilfellet vil du kanskje opprette to kostnadsgrupper: **Administrasjonskostnader for tørrvarer** og **Administrasjonskostnader for nedkjølte varer**.

Følg denne fremgangsmåten for å opprette en kostgruppe for indirekte kostnader.

1. Gå til **Produksjonskontroll &gt; Oppsett &gt; Ruter &gt; Kostgrupper**.
2. Velg **Ny** for å opprette en gruppe.
3. I **Kostgruppe**-feltet angir du et unikt navn for kostgruppen, for eksempel **MATOVH**.
4. I **Navn**-feltet angir du en beskrivelse avkostgruppen, for eksempel **Administrasjonskostnader for varer**.
5. I feltet **Kostgruppetype** velger du **Indirekte**.
6. Valgfritt: I feltet **Virkemåte** velger du **Fast kostnad** eller **Variabel kostnad**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Konfigurere kostarket for indirekte kostnader

Når du har opprettet én eller flere kostgrupper, kan du konfigurere kostarket med indirekte kostnader og definere beregningen. Det kan hende at du vil gruppere indirekte kostnader i kostarket. Hvis du vil gruppere indirekte kostnader, kan du opprette et valgfritt hode i kostarket. Du må opprette minst én node for hver kostgruppe i kostarket. For hver kostgruppe for indirekte kostnader kan du legge til enda en indirekte kostnadsberegning.

### <a name="indirect-cost-node-types"></a>Nodetyper for indirekte kostnad

Denne delen beskriver de ulike nodetypene for indirekte kostnader.

#### <a name="surcharge"></a>Tillegg

**Tilleggsavgift** en av de vanligste typene indirekte kostnader. Den beregner en prosentdel av kostnaden fra et absorberingsgrunnlag for kostnader i produksjonsordren. Du definerer absorpsjonsgrunnlaget ved å velge kostgruppene som er koblet til material- eller tidskomponentene i kostarket.

Et tilleggsgebyr på 3 prosent kan for eksempel legges til produksjonskostnaden for alle råvarene på en produksjonsordre.

#### <a name="rate"></a>Kurs

En indirekte kostnad av **Sats**-typen brukes til å legge til et fast kostnadsbeløp i produksjonsordren fra et absorberingsgrunnlag av kostnader på produksjonsordren. Satsen kan være basert på én av tre undertyper:

- **Prosess** – Satsen er basert på kjøretiden i ruten.
- **Oppsett** – Satsen er basert på oppstillingstid i ruten.
- **Antall** – Satsen er basert på antallet som produseres.

Du definerer absorpsjonsgrunnlaget ved å velge kostgruppene som er koblet til material- eller tidskomponentene i kostarket.

Et fast beløp på USD 2.00 legges for eksempel til hver produksjonsordre basert på kjøretiden i ruten for arbeidskostnadsgruppen i kostarket.

#### <a name="output-unit-based"></a>Basert på utdataenhet

En indirekte kostnad av for typen **Basert på utdataenhet** beregnes ved å multiplisere beløpet som er angitt i hurtigkategorien **Sats** i kostarket med den valgte undertypen. Du kan velge antall, vekt eller volum for ferdigvaren som multiplikator for den indirekte kostnaden.

Du bruker for eksempel antallet til å beregne USD 1.50 for maskinavskrivning for hvert antall som produseres. Som et annet eksempel bruker du volumet til å beregne USD 2.00 i kjølekostnader for volumet av plass som de ferdige varene tar i nedkjølingsenhetene.

#### <a name="input-unit-based"></a>Basert på inndataenhet

En indirekte kostnad av typen **Basert på inndataenhet** beregnes ved å multiplisere mengden råvarer som forbrukes på en produksjonsordre med et beløp. Du kan bruke vekten eller volumet for inndataene i produksjonsordren til å beregne totalen. Du kan begrense beregningen til et delsett av materialer ved å velge én eller flere kostnadsgrupper i hurtigkategorien **Absorberingsgrunnlag** i kostarket.

For eksempel bruker du volumet av inndata for en bestemt kostgruppe som er koblet til kjøleprodukter for å legge til USD 1.00 til produksjonsordren.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Opprette en totalnode for indirekte kostnader i kostarket

Følg denne fremgangsmåten for å opprette en totalnode for indirekte kostnader i kostarket.

1. Gå til **Kostnadsstyring &gt; Oppsett for regnskapspolicyer for indirekte kostnad &gt; Kostark**.
2. I treet velger du en node som representerer varekostnaden som er produsert.
3. Velg **Ny** for å opprette en node.
4. I feltet **Velg nodetype** velger du **Total**.
5. I **Kode**-feltet angir du en unik ID for noden, for eksempel **Produksjonskostnader**.
6. Merk av for **Hode**.
7. Merk av for **Total**.
8. Velg **OK**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Opprette en node for indirekte kostgruppe i kostarket

Følg denne fremgangsmåten for å opprette en node for indirekte kostgruppe i kostarket.

1. Gå til **Kostnadsstyring &gt; Oppsett for regnskapspolicyer for indirekte kostnad &gt; Kostark**.
2. Velg noden du vil opprette indirekte kostnader under, i treet. Du kan for eksempel velge totalnoden for **Produksjonskostnader**.
3. Velg **Ny** for å opprette en node.
4. I feltet **Velg nodetype** velger du **Kostnadsgruppe**.
5. I **Kode**-feltet angir du en unik ID for noden, for eksempel **TRANSP**.
6. I **Beskrivelse**-feltet skriver du inn en kort beskrivelse, for eksempel **Transportkostnader**.
7. Velg **OK**.
8. I **Kostgruppe**-feltet velger du kostgruppen, for eksempel **ADMKOST1: Administrasjonskostnader for transport**.

### <a name="create-a-surcharge-indirect-cost"></a>Opprette en indirekte kostnad for tilleggsavgift

Følg denne fremgangsmåten for å opprette en indirekte kostnad for tilleggsavgift i kostarket.

1. Gå til **Kostnadsstyring &gt; Oppsett for regnskapspolicyer for indirekte kostnad &gt; Kostark**.
2. Velg noden for node for indirekte kostgruppe du vil opprette indirekte kostnader under, i treet. Velg for eksempel totalnode for **TRANSP - Transportkostnader**.
3. Velg **Ny** for å opprette en node.
4. I feltet **Velg nodetype** velger du **TIlleggsavgift**.
5. I **Kode**-feltet angir du en unik ID for noden, for eksempel **Tilleggsavgift for transport**.
6. Velg **OK**.
7. Velg **Total** i **Undertype**-feltet.
8. På hurtigfanen **Absorberingsgrunnlag** velger du **Ny** for å opprette en kostnadskode.
9. Velg en kostgruppe som skal brukes til å beregne tillegget, i **Kode**-feltet.
10. Valgfritt: Gjenta trinn 8 til og med 9 for hver kostgruppe du vil bruke til beregningen.
11. På hurtigfanen **Tilleggsavgift** velger du **Ny** for å opprette en sats.
12. Velg kostnadsversjonen du vil legge til tillegget i, i **Versjon**-feltet.
13. Valgfritt: Angi et område som tillegget skal brukes på, i **Område**-feltet.
14. I **Prosent**-feltet angir du prosenten som skal beregnes på produksjonsordrer fra kostgruppene som er definert i hurtigkategorien **Absorberingsgrunnlag**.
15. I hurtigkategorien for **Finansposteringer** velger du hovedkontoen som skal brukes for feltene **Estimert indirekte kostnad absorbert**, **Estimert kostnad for indirekte kostnad brukt, VIA**, **Indirekte kostnad absorbert** og **Kostnad for indirekte kostnad brukt, VIA**.
16. Valgfritt: I hurtigkategorien for **Finansdimensjoner** angir du alle finansdimensjoner som skal registreres som standard for transaksjoner når de posteres til økonomimodulen.

Fremgangsmåten over viser hvordan du oppretter en indirekte kostnad for **Tilleggsavgift**-typen. Lignende trinn brukes til å opprette andre typer indirekte kostnader. Delene nedenfor beskriver forskjellene for hver type.

#### <a name="rate"></a>Kurs

- I trinn 4 velger du **Sats** i stedet **Tilleggsavgift**.
- I trinn 7 velger du **Prosess**, **Oppsett** eller **Antall** i stedet for **Total**.
- I trinn 11 bruker du hurtigkategorien **Sats** i stedet for hurtigkategorien **Tilleggsavgift**.
- I trinn 14 angir du et beløp i **Beløp**-feltet i stedet for en prosent i **Prosent**-feltet.

#### <a name="output-unit-based"></a>Basert på utdataenhet

- I trinn 4 velger du **Basert på utdataenhet** i stedet for **Tilleggsavgift**.
- I trinn 7 velger du **Antall**, **Vekt** eller **Volum** i stedet for **Total**.
- Hopp over trinn 8 til 10.
- I trinn 11 bruker du hurtigkategorien **Sats** i stedet for hurtigkategorien **Tilleggsavgift**.

#### <a name="input-unit-based"></a>Basert på inndataenhet

- I trinn 4 velger du **Basert på inndataenhet** i stedet for **Tilleggsavgift**.
- I trinn 7 velger du **Vekt** eller **Volum** i stedet for **Total**.
- I trinn 11 bruker du hurtigkategorien **Sats** i stedet for hurtigkategorien **Tilleggsavgift**.
