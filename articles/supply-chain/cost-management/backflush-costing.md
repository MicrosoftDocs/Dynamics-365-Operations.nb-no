---
title: Backflush-etterkalkulering
description: Dette emnet introduserer konseptet med backflush-etterkalkuleringen som skal brukes for Lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 484bac74ccb498f0b006458f5e6d8fb0e9461a8f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556076"
---
# <a name="backflush-costing"></a>Backflush-etterkalkulering

[!include [banner](../includes/banner.md)]

Dette emnet introduserer konseptet med backflush-etterkalkuleringen som skal brukes for Lean manufacturing. 

Med etterkalkulering for Lean manufacturing kan produksjonsflyten bruke kostnadskalkylemetoden kjent som backflush-etterkalkulering. I metoden backflush-etterkalkulering akkumuleres direkte materialer som er brukt i produksjonsflytens VIA-kostnadskonto. Lagermodellgruppen for standard kostpris brukes. Produktene som er mottatt fra produksjonsflyten, trekkes fra VIA ved standardkostnad. Den viktigste forskjellen mellom backflush-etterkalkuleringen og standardkostnad er at for backflush-etterkalkulering beregnes ikke avvik per kanban eller ferdig produkt. I stedet beregnes avvik per produksjonsflyt over en periode. Denne metoden introduserer et virkelig lean-begrep for rapportering av materialforbruk. Dedikert plukket antall av materialet rapporteres ikke til en kanban eller produksjonsordre. I stedet klargjøres hele antallet for partier eller håndteringsenheter til produksjonsflyten. Når partiene eller håndteringsenhetene er registrert som tomme, deklareres de brukt. Avansert forbruk kan brukes, avhengig av [konfigurasjonen av produksjonsflyten](../production-control/lean-manufacturing-modeling-lean-organization.md). Før avansert forbruk kan brukes, må organisasjoner tillate seg selv å slette material i VIA for produksjonsflyten. Den periodiske backflush-etterkalkuleringen bestemmer effektive den verdien av VIA til slutten av perioden. Denne fastsettelsen er basert på kanban-håndteringsenhetene og kanban-jobbstatusen. Avvik mellom de gjeldende verdiene og de faktiske VIA-verdiene per kostgruppe og vare beregnes og vises som avvik.

## <a name="configuring-backflush-costing"></a>Konfigurere backflush-etterkalkulering
For å aktivere etterkalkulering må du fullføre følgende oppsett:

-   **Definer VIA-kontoer for produksjonsgruppen og produksjonsflyten.** VIA-kontoene for produksjonsflyten er angitt i produksjonsgruppen. Avvik beregnes i produksjonsflyten for backflush-etterkalkulering som differansen i VIA-verdien før og etter at backflush-etterkalkuleringen kjøres for hver produksjonsflyt. Vi anbefaler derfor at du oppretter en VIA-konto for hver produksjonsflyt.
-   **Tilordne en kostnadskategori til ressursgruppen.** Du må tilordne en kostnadskategori til kjøretidskategorien for arbeidscellen. Hvis du vil finne avvik etter aktivitet, bør du opprette en kostnadskategori for hver arbeidscelle. Kostnadskategorier for oppsett og antall vurderes ikke i etterkalkulering for lean manufacturing. VIA-kontoene per ressursgruppe ignoreres i backflush-etterkalkuleringen. For aktiviteter i underleveranser kreves det ikke noen kostnadskategori. Kostgruppen som er tilordnet den aktive tjenesten, brukes i stedet.
-   **Tilordne kostnadsgrupper.** Hvis du vil aktivere segmentering av kostbidrag i en produksjonsflyt, må du tilordne kostgrupper etter kostgruppetype:
    -   **Kostgruppen direkte materialer** - Direkte materialer krever en kostgruppe som identifiserer materialkategorien for etterkalkulering. Denne kostgruppen aktiverer en aggregert visning av kostnader, VIA og avvik etter direkte materialer.
    -   **Kostgruppen Direkte produksjon** - Kostgruppen Direkte produksjonskost registrerer det direkte kostbidraget for driftsressurser til produksjonsflyten. Denne kostgruppen aktiverer en aggregert visning av kostnader, VIA og avvik etter direkte produksjonskostnad.
    -   **Indirekte kostgruppe** - Den indirekte kostgruppen er nødvendig for å beregne det indirekte kostbidraget til produksjonsflyten. Denne kostgruppen aktiverer en aggregert visning av kostnader, VIA og avvik etter indirekte kostnader.
    -   **Kostgruppen Direkte outsourcing** - Kostgruppen for tjenestene aktiverer en aggregert visning av tilordnet kostnad og VIA, og bestemmer kostnadsavvikene for underleveranser.
    -   **Kostgruppen for ferdige produkter** - Ferdige produkter krever en kostgruppe som identifiserer produktkategorien for etterkalkulering. Denne kostgruppen aktiverer en aggregert visning av kostnader, VIA og avvik etter produktkategori. Standardkostnaden for produkter beregnes ved å bruke kostnadsberegningen som er basert på stykklisten, og produksjonsflyten og kanban-reglene eller ruten.

### <a name="costing-sheet"></a>Kostark

Kostarket modellerer kostnadsstrukturen for firmaet, og er bygget av kostgruppene for å klassifisere kostnaden. Kostarket har forskjellige skjemaer. Det viser kostnadsinformasjon i henhold til strukturen som er laget i den. I kostarket kan du også definere formelen som brukes til å beregne den indirekte kostnaden. Beregningsformelen kan være basert på antall, vekt, volum eller verdi.

-   **Definere en etterkalkuleringsversjon.** I etterkalkuleringsversjonen definerer firmaet hvordan kostnaden skal vedlikeholdes. En etterkalkuleringsversjon kan inneholde et sett med standard kostnadsposter, eller et sett med planlagte kostnadsposter, avhengig av etterkalkuleringsversjonen som er tilordnet etterkalkuleringsversjonen. Etterkalkuleringsversjonen som brukes for etterkalkulering for lean manufacturing, må være basert på standardkostnad.
-   **Tilordne en lagermodellgruppe for frigitte produkter.** Alle produkter som er knyttet til produksjonsflyten, må tilordnes en lagermodellgruppe som bruker lagermodellgruppen **Standardkostnad**. Standardkostnad vedlikeholdes per område og aktiveringsdato. For produktstandarder kan lagermodellgruppen velges hvis kostnaden vedlikeholdes per variant eller produktstandard.
-   **Per definisjon er underleveranser ikke-lagerførte tjenester.** Aktiviteter i underleveranser har ingen lagermodellgruppe. Hvis du vil kostnadsberegne en aktivitet i underleveranser på riktig måte, må du kontrollere at serviceaktiviteten hører til en lagermodellgruppe der lagerpolicyen er satt til **Lagerført produkt = Usann**.

For utdataprodukter krever kostnadsberegning som er basert på produksjonsflyten, at en standardkostnad vedlikeholdes for tjenestene som er knyttet til aktiviteter i underleveranser. Kostgruppen som er tilordnet til tjenestene, brukes til å bestemme kostnadsavvikene for aktiviteten i underleveranse.

## <a name="cost-calculation-for-lean-manufacturing"></a>Etterkalkulering for Lean manufacturing
Stykklisteberegningen må være basert på en ruteversjon eller en produksjonsflyt for produkter som leveres utenfor en produksjonsflyt. Stykklisteberegningen beregner kostnaden for et produkt og den tilknyttede nedbrytingen til ressurser og materialer som kreves for å bygge produktet. Fradraget fra VIA-kontoen for produksjonsflyten utføres ved hjelp av nedbrytingen for et produkt etter vare og kostnadsgruppe.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Beregning som er basert på produksjonsflyten

Lean manufacturing for Microsoft Dynamics 365 for Finance and Operations er uavhengig av ruter. Kostnadsberegningen for produkter som leveres fra en produksjonsflyt, kan baseres på selve produksjonsflyten. Før du kan utføre beregningen, må en kanban-regel opprettes som leverer produktet utenfor produksjonsflyten. Hvis et produkt kan angis fra flere produksjonsflyter fra samme sted på beregningsdatoen, kan du velge produksjonsflyten for stykklisteberegningen. På siden **Standard produksjonsflyt** kan du konfigurere en standard produksjonsflyt for hver vare. Hvis det finnes flere kanban-regler for det samme produktet i den samme produksjonsflyten som er aktiv på beregningsdatoen, velger beregningen den første kanban-regelen som er aktiv for beregningen.

### <a name="calculation-that-is-based-on-the-route"></a>Beregning som er basert på ruten

Beregning som er basert på en rute, er like gyldig som beregning som er basert på en produksjonsflyt. Beregning som er basert på en rute, bruker imidlertid ikke etterkalkulering for Lean manufacturing-funksjonalitet. Ruten bør bruke ressurskrav for ressursgrupper. For å unngå systematiske avvik bør den også bruke de samme arbeidscellene, eller i det minste samme kostnadskategorier. Igjen bør du unngå kostnadskategorier for oppsett og antall. De bidrar ikke til å beregne kostnadene i en mer detaljert analyse enn etterkalkulering for Lean manufacturing. Vurder resultatet av kostnadsoppdelingen for å finne ut hvilket alternativ (produksjonsflyt eller rute) du bør bruke til å beregne kostnaden. Versjonen som er nærmere utgangspunktet og gir færre avvik generelt, er det beste alternativet. I et Lean manufacturing-miljø der et produkt leveres av en enkelt produksjonsflyt og en enkelt kanban-regel, er beregningen som er basert på produksjonsflyten, sannsynligvis mer nøyaktig. For et produkt som kan leveres av Lean manufacturing og produksjonsordrer i samme område, eller som kan ha flere produksjonsflyter eller flere kanban-regler i den samme flyten, kan en beregning bli mer nøyaktige hvis den er basert på en ruteversjon som er bygget spesielt for kostnadsberegningen, ikke for produksjonen. Beregningen av produksjonsflyt må brukes til å beregne produkter som involverer bruk av underleverandører. I Microsoft Dynamics 365 for Finance and Operations bruker kostmodellene for bruk av underleverandører via produksjonsordrer og bruk av underleverandører i Lean manufacturing to ulike tilnærminger. Lean manufacturing introduserer en ny kostgruppetype, **Direkte outsourcing**, for å beregne underleveranser.

## <a name="material-consumption"></a>Materialforbruk
Når materiale forbrukes fra lager til VIA, legges kostnaden for materialer til VIA ved de faktiske standardkostnadene for en kostgruppe. Denne operasjonen skjer under følgende betingelser:

-   Kanban-avganger posteres for kanban-plukklinjer som oppdaterer beholdningen.
-   Overføringsjobber er fullført som oppdaterer lageret ved plukking, men ikke mottak (overføring av materiale fra lager til VIA).

## <a name="receiving-products-from-the-production-flow"></a>Mottak av produkter fra produksjonsflyten
Du mottar varer fra produksjonsflyten under følgende betingelser:

-   Prosessjobber er fullført som har **Oppdater beholdning ved mottak** satt til **Ja**.
-   Overføringsjobber er fullført som oppdaterer beholdning ved mottak, men som har **Oppdater beholdning ved plukking** satt til **Nei** (overføring fra VIA til beholdning). Med dette alternativet kan du motta produkter utenfor en produksjonsflyt uavhengig av stykklisten og rutekonfigurasjonen. Prosessen følger bare de fysiske flytene. Dette alternativet er spesielt godt egnet til å motta biprodukter, koprodukter eller svinn utenfor en produksjonsflyt, og for å korrigere kostnadssaldoen for VIA for produksjonsflyt i henhold til dette.

Produkter som er mottatt fra produksjonsflyten, trekkes fra VIA.

## <a name="products-in-wip"></a>Produkter i VIA
VIA-modellen for Lean manufacturing i Microsoft Dynamics 365 for Finance and Operations lar deg bruke kanban-håndteringsenhetsstatusen til å administrere materialer, halvfabrikata og ferdige produkter som er en del av VIA.

-   **Tilordnet** - Kanbanen kan ha brukt materiale som er etterkalkulert i VIA.
-   **Mottatt** - Hvis Kanbanen refererer til en siste aktivitet der **Oppdater beholdning ved mottak** er satt til **Nei**, representerer den en full håndteringsenhet for et produkt eller et halvfabrikata som ikke er registrert på lager.

Legg merke til materiale i VIA ikke vises i oversikten over lagerbeholdning. Det er imidlertid synlig i oversikter over kanban-antall.

## <a name="consuming-products-in-wip"></a>Forbruke produkter i VIA
Produkter i VIA forbrukes når de tilsvarende kanban-håndteringsenhetene er tømt. Et tomt kanban-signal gir ikke en aktiv etterkalkuleringstransaksjon, men vil tre i kraft når neste backflush-etterkalkuleringen kjøres. Tømte Kanban-håndteringsenheter regnes ikke lenger som på lager og beregnes derfor som forbrukt i perioden.

### <a name="automatic-empty-registration"></a>Automatisk tom registrering

Planlagte eller hendelses-Kanbaner kan settes til automatisk tom registrering i kanban-regelen:

-   **Når håndteringsenheter er mottatt** - For planlagte Kanbaner deklareres materialet som standard som forbrukt når den siste jobben for kanbanen er fullført. For Kanbaner med fast antall anbefales dette alternativet bare for Kanbaner i én boks fordi det returnerer kortet til kilden for behovet hver gang en kanban mottas på den endelige målet.
-   **Når kildebehovet er registrert** - Dette alternativet er bare tilgjengelig for hendelses-Kanbaner og er standardalternativet. I forbindelse med VIA er dette alternativet nyttig når du skal holde VIA ren, fordi Kanbaner for komponenter i VIA tømmes automatisk, og forbrukes derfor fra VIA når den overordnede Kanbanen er klargjort.

Som en konklusjon kan Kanban-håndteringsenheter tilordnes (= i arbeid), mottas (=full) eller tømmes. Det finnes ingen delvis tømming. Hvis du vil muliggjøre nøyaktig registrering av forbruk, er det derfor viktig at du begrenser produktantallene for en kanban slik at de er mindre enn forbruket per periode. Produkter som flyttes til shop floor i store partier som dekker dager eller uker av behov, bør ikke forbrukes til VIA. I stedet skal disse produktene beholdes i lageret.

## <a name="backflush-costing"></a>Backflush-etterkalkulering
Kjør backflush-etterkalkulering for periodisk å verdiberegne VIA og produsere en status på slutten av perioden som beregner avvikene i materialer, arbeid og indirekte kostnader. De beregnede avvikene posteres til avvikskontoene. I backflush-etterkalkuleringsprosessen brukes alle produksjonsflyter for den juridiske enheten i den samme bunkeutførelsen. Når backflush-etterkalkuleringen kjøres i en bunke, kan behandlingen være flertrådet av produksjonsflyten. Backflush-perioden er definert av en sluttdato. Du kan ikke postere nye transaksjoner til en dato når en backflush-etterkalkulering er kjørt. Du bør aldri kjøre backflush-etterkalkulering for gjeldende dato før dagen er faktisk over. Backflush-etterkalkuleringen utfører trinnene nedenfor.

1.  Bestem de ubrukte antallene i produksjonsflyten per periodens sluttdato. Når backflush-etterkalkuleringen er kjørt, kan du vise de ubrukte antallene på datoen for etterkalkuleringskjøringen i dialogboksen **Ubrukte antall**.
2.  Beregn produksjonsflytens netto realiserte forbruk over perioden.
3.  Fjern VIA fra det realiserte ressursforbruket og produktene.
4.  Beregn produksjonsavvik til standardkostnad for perioden. **For forbrukte komponenter for perioden:**
    -   Oppdater økonomisk netto realisert antall materiale som ble forbrukt av produksjonsflyten over perioden. Systemet behandler først inn, først ut-ordren (FIFO) på de individuelle lagertransaksjonene for å oppdatere økonomisk de fysisk oppdaterte transaksjonene for produksjonsflyten, til netto realisert antall for perioden er nådd.
    -   Transaksjoner deles økonomisk for å tilordne det nøyaktige forbrukte antallet.
    -   Ubrukte antall i VIA for produksjonsflyt blir værende i fysisk oppdatert status.

    **For fullførte produksjonsantall for perioden:**
    -   Oppdater økonomisk lagertransaksjonene for det fullførte antallet for perioden.

    **For konverteringskostnaden:**
    -   De brukte transaksjonene for konverteringskostnad (rutetransaksjoner) som ble registrert for perioden, oppdateres økonomisk.
    -   Alle direkte produksjonskostnader oppdateres økonomisk. Alle kanban-prosessjobber som fullført i løpet av perioden, akkumuleres.
    -   Alle indirekte kostnader som beregnes for det forbrukte materialet i perioden, beregnes og trekkes fra VIA. Gjenstående indirekte kostnader posteres som et avvik.

5.  Beregn produksjonsavvikene til standardkostnad. Avviket beregnes per kostgruppe.





