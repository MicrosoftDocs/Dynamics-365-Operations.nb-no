---
title: Oversikt over lagerkonfigurasjon
description: Denne artikkelen forklarer hvordan du konfigurerer et lager. Det inneholder informasjon om hvordan du aktiverer et oppsett for lageret og lagerprosesser.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b0ebb5d7f77e2104d0280bcee7c018d9cf97bd5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970162"
---
# <a name="warehouse-configuration-overview"></a>Oversikt over lagerkonfigurasjon

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer et lager. Det inneholder informasjon om hvordan du aktiverer et oppsett for lageret og lagerprosesser.

> [!NOTE]
> Denne artikkelen gjelder funksjoner i modulen **Lagerstyring** (avanserte lageraktiviteter). Det gjelder ikke for lagerfunksjoner i modulen **Lagerstyring**.

## <a name="warehouse-layout"></a>Lageroppsett
Lagerstyringssystemet i Supply Chain Management gir deg fleksible måter å definere lageroppsettet på for å oppfylle bedriftens ulike behov, slik at du kan oppnå optimal lagereffektivitet.

-   Du kan opprette områder for lagring med høy prioritet og lav prioritet for optimal plassering av varer.
-   Du kan dele lageret inn i soner for å imøtekomme ulike lagringsbehov, for eksempel temperaturkrav eller ulike omsetningshastigheter for varer.
-   Du kan angi lagerlokasjoner på alle nivåer (for eksempel område, lager, gang, reol, hylle og boksposisjon).
-   Du kan gruppere lokasjoner ved hjelp av innstillingene for fysisk kapasitetsbegrensning.
-   Du kan styre hvordan varer oppbevares og plukkes, basert på spørringsdefinerte regler.

Hvis du vil bruke lagerstyring i Supply Chain Management, må du opprette et lager og aktivere det for mer avanserte eller spesialiserte lagerstyringsaktiviteter. På **Lagre**-siden velger du alternativet **Bruk lagerstyringsprosesser**.

### <a name="zone-groups-zones-location-types-and-locations"></a>Sonegrupper, soner, lokasjonstyper og lokasjoner

Som en del av prosessen for aktivering av lageroppsett må du definere lagersonegrupper, og soner, lokasjonsprofiler, lokasjonstyper og lokasjoner.

-   **Sonegrupper** – En logisk eller fysisk gruppering av soner i et lager.
-   **Soner** – En logisk eller fysisk gruppering av lokasjoner i et lager.
-   **Lokasjonsprofiler** – En logisk eller fysisk gruppering av lokasjoner som har de samme lagerlokasjonsprosesspolicyene (for eksempel en blanding av ulike varenumre kan lagres der, og de samme fysiske kapasitetsbegrensningene gjelder).
-   **Lokasjonstyper** – En logisk eller fysisk gruppering av lagerlokasjonene. Du kan for eksempel opprette en lokasjonstype for alle oppsamlingslokasjoner. Obligatoriske innstillinger på **Lagerstyringsparametere**-siden driver prosessen med å definere oppsamlingslokasjonstypene og endelig leveringslokasjonstype.
-   **Lokasjoner** – Det laveste nivået av lokasjonsinformasjon. Lokasjoner brukes til å spore hvor lagerbeholdningen lagres og plukkes på et lager.

Enhetene som du oppretter for å definere oppsettet for lageret, brukes i spørringene som du definerer i arbeidsmaler for å drive arbeidsordrer i lageret. Derfor, når du definerer sonene, vurderer lokasjonstyper og så videre hvordan ulike områder i lageret brukes til forskjellige prosesser. I tillegg må du vurdere faktorer som for eksempel fysiske egenskaper for et bestemt område. Det kan for eksempel være områder der du bare kan bruke en bestemt type truck. Eller, hvis firmaet har produksjonsvarer og ferdige varer innenfor de samme fasilitetene, kan det hende at du vil opprette et enkelt lager i Supply Chain Management, men dele inn de to operasjonene ved å opprette to sonegrupper. Gi enhetene beskrivende navn slik at det er enkelt å identifisere dem når du bruker dem i malspørringer.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Lagringsgrenser for lokasjon, lokasjonsprofiler og faste plukklokasjoner

Du må vurdere det fysiske oppsettet av lageret, både for å bestemme lagringskapasiteter (lokasjonslagringsgrenser og lokasjonsprofiler), og som en del av dine forsøk på å oppnå optimale lagerprosesser. 

Lagringsgrenser for lokasjonen garanterer at arbeid ikke opprettes for å be om at lageret blir plassert på en lokasjon som ikke har den fysiske kapasiteten til å føre lageret. Hvis for eksempel noen steder i et lager kan inneholde bare én pall per lokasjon, kan lokasjonslagringsgrenser aktiveres. **Antall**-verdien kan settes til **1**, og **Enhet** -verdien kan settes til **PL** i en bestemt lokasjonsprofilgruppering. 

Hvis mer avanserte beregninger kreves for å styre lokasjonskapasitetsbegrensningene, kan lokasjonsprofilinnstillingene brukes. I så fall vurderes vekt og volum når kapasitetsberegninger utføres. 

For å oppnå optimale utgående prosesser, bør du vurdere om du vil bruke faste plukklokasjoner og/eller emballasjelokasjoner. Ofte brukes minimums-/maksimumsetterfylling for etterfyllingsprosesser fra et partiområde til de faste plukklokasjonene, og flere faste plukklokasjoner kan aktiveres innenfor samme lager og for produktvarianter. Vurder fleksibiliteten som du oppnår ved å aktivere dedikerte lokasjoner for behovsetterfyllingsoverflyt som bare brukes for etterfyllingbehandling for bølge/last.

### <a name="location-setup-wizard"></a>Veiviser for lokasjonsoppsett

Du kan bruke veiviseren for **lokasjonsoppsett** for å raskt lage lokasjonene i et lager. Som en del av denne prosessen kan du enkelt beholde formatet til lokasjonsnavnene.

## <a name="warehouse-processes"></a>Lagerprosesser
Som en del av konfigurasjonen av lageret er det viktig at du aktiverer lagerprosesser i henhold til bedriftens behov. De viktigste komponentene du må konfigurere, er bølgemaler, arbeidsmaler, arbeidsutvalg og lokasjonsdirektiver.

### <a name="wave-templates"></a>Bølgemaler

Bølgemaler bidrar til å aktivere den utgående "Frigi til lager"-prosessen. Så snart ordrelinjer frigis (enten direkte fra kildedokumenter, via prosesser for satsvise jobber eller via belastninger som allerede er opprettet), brukes funksjonen for bølgemal. 

Du kan opprette tre typer bølgemaler: 
-   **Forsendelse**
-   **Produksjonsordre**
-   **Kanban** 

Parametere brukes til å definere hvor langt systemet automatisk skal gå i utgående arbeidsbehandling. En bølgemal velges basert på bølgemalrekkefølgen og -kriteriene som er angitt i malen. Hvis en mal vises øverst i rekkefølgen, kontrolleres først vilkårene i denne malen. Hvis vilkårene kan oppfylles, behandles bølgemalen. Hvis ikke kontrolleres kriteriene i neste mal og så videre. Det er derfor lurt å plassere malen som har de mest spesifikke kriteriene, øverst på listen for bølgemalensekvens slik at den blir behandlet først. Du vil for eksempel behandle alt arbeid for en bestemt transportør i dag og midlertidig utsette behandlingen av arbeidet for andre transportører. I så fall skal bølgemalen som velger arbeid for transportøren, vises høyere i sekvensen enn andre maler. Hvis ikke kan det hende at arbeidet for andre transportører behandles før arbeidet for denne leverandøren er fullført. 

Du må angi metodene for bølgeprosess i hver bølgemal. Metodene som er tilgjengelige, varierer avhengig av bølgemaltypen.

### <a name="work-templates"></a>Arbeidsmaler

Arbeidsmaldefinisjoner spiller en viktig rolle i definisjonen av arbeidsprosesser i lagerstyring. De definerer hva slags arbeid som utføres, og hvordan arbeidet utføres. Maler kan også inneholde en direktivkode med kobling til et lokasjonsdirektiv for å fastsette hvor arbeid skal utføres. Arbeidsmaler inkluderer en spørring som oppfyller kriteriene for arbeidet. Hver mal må inneholde minst én plukkoperasjon og én plasseringsopersasjon for å kjøre den grunnleggende arbeidsoperasjonen for overføring av lagerbeholdning fra ett sted til et annet. 

Hvis flere arbeidere må kunne behandle arbeid for noen av dine lageroperasjoner, vil du kanskje bruke konseptet *oppsamling* for lageret og dele inn arbeidsutførelsen i forskjellige arbeidsklasser.

### <a name="work-pools"></a>Arbeidsutvalg

Arbeidspuljer brukes for å organisere arbeidet i grupper. Du kan for eksempel opprette en arbeidspulje for å klassifisere arbeid som skjer på en bestemt lagerlokasjon. For alle arbeidstypene unntatt opptelling, kan du tilordne en arbeidspulje til en arbeidsmal. For syklustelling kan du tilordne en arbeidspulje på følgende sider:

-   Planer for syklustelling
-   Terskler for syklustelling
-   Syklustellingsarbeid etter lokasjon
-   Syklustellingsarbeid etter vare

Når du bruker arbeidsmaler til å opprette arbeid, tilordnes arbeidspuljen automatisk til arbeidet. 

Arbeidspulje-ID-er kan også brukes til å begrense typen arbeid som er rettet mot en bestemt lagermedarbeider, forutsatt at denne funksjonaliteten er konfigurert på det relevante menyelementet for mobilenhet.

### <a name="location-directives"></a>Lokasjonsdirektiver

Som navnet antyder brukes lokasjonsdirektiver til å styre arbeidstransaksjonene til de relevante lokasjonene i lageret. De definerer med andre ord hvor det skal plukkes og plasseres. 

Hvis du vil gjøre det lettere og raskere å angi hvilke handlinger som er knyttet til hver lokasjonsdirektivlinje, kan du bruke en av de forhåndsdefinerte strategiene. Du kan for eksempel bruke **Tom lokasjon uten innkommende arbeid**-strategien for å søke etter ledige lokasjoner i et lager, eller du kan bruke **FEFO-partireservering**-strategien for utgående salgsplukking.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Konfigurere lokasjoner i et WMS-aktivert lager](tasks/configure-locations-wms-enabled-warehouse.md)



