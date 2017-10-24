---
title: Prosjektprognoser og budsjetter
description: 
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 32dd89d92a496d6601d1983dbc3c8e7e579ee0b3
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="project-forecasts-and-budgets"></a>Prosjektprognoser og budsjetter

[!include[banner](../includes/banner.md)]




Du kan styre og kontrollere prosjekter i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition på to måter: prosjektprognoser og prosjektbudsjetter. 

Du kan bruke prosjektprognose hvis organisasjonen har et driftsperspektiv, og hvis den fokuserer på inntekter og kostnader som er avledet fra bestemte transaksjoner. Bruk prosjektbudsjettering hvis organisasjonen fokuserer mer på økonomiske beløp. 

Både prosjektprognoser og prosjektbudsjetter bruker prognosemodeller til å holde de forventede transaksjonsbeløpene. 

Hver metode har sine fordeler. Du bør vurdere følgende punkt før du velger en metode for din organisasjon.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Prosjektprognoser**                                                                                                                                                                                                                                 | **Prosjektbudsjettering**                                                                                                                                                   |
| **Periodetilordning**     | Du kan ikke eksplisitt fordele transaksjoner over en regnskapsperiode. I stedet er prognosen og styringen av prognosen basert på prosjektets levetid. Ettersom prognoser er basert på en bestemt dato, må du utlede perioden fra dato. | Du kan fordele transaksjoner over hele prosjektet eller en regnskapsperiode. Hvis du fordeler over en periode, kan du overføre ubrukte beløp til neste regnskapsperiode. |
| **Vise transaksjoner**  | Du kan vise transaksjoner i prognoseskjemaene der du ser prognosene for hele firmaet, og for alle prosjekter uavhengig av hierarkiet. Hvis du vil fokusere på et bestemt prosjekt, må du filtrere dataene.                                       | Du kan vise budsjetterte transaksjoner for ett enkelt prosjekthierarki. Derfor kan du vise transaksjonsdetaljer for et overordnet prosjekt eller dets underprosjekter.                 |
| **Transaksjonsvariabler** | Når du angir prognosetransaksjoner, kan du bruke alle attributter som finnes for en faktisk transaksjon. Dette muliggjør flere detaljer i prognosen. Du kan for eksempel angi detaljer for antall, ansatte, varer eller linjeegenskaper.         | Når du angir detaljer for budsjett, kan du bare bruke beløp, kategorier og aktiviteter.                                                                                    |
| **Sikkerhet**              | Prognose er basert på transaksjonene som du angir i prognoseskjemaene, og omfatter ingen prosesskontrollmekanisme. Alle arbeidere som har tillatelser for et prognoseskjema, kan se gjennom informasjon uten godkjenning.                                        | Budsjettering bruker arbeidsflytsystemet, som muliggjør endringsadministrasjon og lar deg beholde en logg over endringene.                                                       |
| **Oppføringstyper**           | Prognosetransaksjonsoppføringer er basert på antall enheter og på kostnad og salgsenhetspriser.                                                                                                                                                       | Budsjettdetaljer er basert på beløp som deles mellom kostnader og inntekter.                                                                                        |
| **Prognosemodeller**       | Fordi hver prognose må være knyttet til en modell, kan du opprette flere prognosemodeller og også definere undermodeller.                                                                                                                               | Prosjektbudsjetteringsgrenser prognosemodeller som er brukt for budsjettering. Færre prognosemodeller kan øke konsekvensen i prognoser.                           |
| **Kostnadsoverskridelser**         | Du kan bare tillate eller ikke tillate innlegging av transaksjoner som vil føre til en kostnadsoverskridelse.                                                                                                                                                                | Prosjektbudsjettering gir ekstra kontrollalternativer for brukere. Du kan tillate advarsler og overskridelser.                                                                   |
| **Styring**               | Prognosestyring utføres ved hjelp av prognosereduksjon. Faktiske beløp trekkes fra prognosetransaksjonssaldoer uten revisjonsspor. Dette kan gjøre det vanskeligere å spore hvor de faktiske transaksjonene fant sted.                   | I prosjektbudsjettkontroll er faktiske beløp trukket fra beløpene i det gjenstående budsjettet. Dette fører til et tydeligere revisjonsspor.                                   |

## <a name="project-forecasts"></a>Prosjektprognoser
Når du bruker prosjektprognoser, kan du angi prognosetransaksjoner i prognoseskjemaer for hver transaksjonstype. Hver attributt som er tilgjengelig for en faktisk transaksjon, kan brukes for en prognosetransaksjon – for eksempel linjelønnsomhet, linjeattributter, arbeidere eller beskrivelser. Du kan også prosjektere hvor lenge etter at du har pådratt deg en kostnad, du vil fakturere en kunde. 

Prognosetransaksjoner for prosjekter er basert på antall og beløp. 

Hver prosjektprognose må være tilknyttet en prognosemodell. Når du angir en prognosetransaksjon, foreslås det automatisk en prognosemodell. Prognosemodellen fungerer som en beholder for prognosetransaksjonene. 

Du kan angi prognosemodeller som undermodeller for en modell. Dette gjør at du kan angi prognoser etter region, tidsperiode eller avdeling. Du kan kopiere prognosetransaksjonene i en modell for å opprette en ny modell, og du kan også overføre transaksjonene til finans. Siden det er en én-til-én-relasjon mellom en prognose og en modell, utgjør hver prognosemodell et separat budsjett for et prosjekt. 

Prognosemodeller kan bruke prognosereduksjon som styremekanismen for prosjekter. I prognosereduksjon reduserer faktiske transaksjoner prognosetransaksjonssaldoer. Siden prognosereduksjon brukes på det høyeste prosjektet i hierarkiet, gir den imidlertid en begrenset visning av endringene i prognosen. Hvis en arbeider for eksempel er tilknyttet et underprosjekt, posteres de faktiske transaksjonene for arbeideren til det overordnede prosjektet. Derfor kan det være vanskelig å spore endringene, fordi du det ikke er enkelt å finne ut hvilken transaksjon i hvilket delprosjekt som forårsaket en reduksjon av prognosebeløpet. Det er derfor lurt å lage en kopi av en prognosemodell som prognosereduksjon kan bruke. Du kan deretter bruke rapporter til å vise det som opprinnelig ble anslått. 

Du kan revidere, kopiere, slette eller overføre prosjektprognoser til et økonomimodulbudsjett. Det finnes imidlertid ingen prosesskontroll. Alle arbeidere med tillatelse for et prognoseskjema, kan gjøre endringer uten gjennomgang.

-   **Revider** – Du kan revidere en prognosetransaksjon i de samme skjemaene der de opprinnelige oppføringene ble gjort.
-   **Kopier eller slett** – Når du kopierer prognosetransaksjoner, kopierer du transaksjonslinjene for én prognosemodell til en annen prognosemodell. Når du sletter en prognose, sletter du også prognosetransaksjonene fra en prognosemodell. Hvis du vil begrense prognosetransaksjonene du vil kopiere eller slette, velger du bestemte transaksjonstyper og datoer. Dette gjør at du kan kopiere eller slette bestemte deler av en prognose.
-   **Overføring** – Når du overfører en prosjektprognose til et økonomimodulbudsjett, overfører du prognosetransaksjonene for en prognosemodell til et økonomimodulbudsjett. Du kan overskrive alle tidligere overførte transaksjoner i økonomimodulbudsjettet som du overfører prosjektprognosen til.

## <a name="project-budgets"></a>Prosjektbudsjetter
Prosjektbudsjettering er en enklere metode enn prognoser, selv om den kan integreres med prognosemodeller. Den bruker ett enkelt skjema for opprinnelige budsjettdetaljer og endringer og muliggjør prognoser som bare er basert på beløp, kategori eller aktivitet. 

I prosjektbudsjettering må alle opprinnelige budsjetter og endringer sendes til en projektarbeidsflyt for godkjenning. Arbeidsflyter gir deg bedre kontroll over prosessen og oppretter en endringshistorikkpost. 

Prosjektbudsjettering ligner økonomimodulbudsjettering, men er raskere og enklere å sette opp. Mange av alternativene i økonomimodulbudsjettering, for eksempel nummerserier eller valuta, må ikke defineres separat for prosjekter.

Prosjektbudsjetter knyttes automatisk til to prognosemodeller, én for opprinnelig budsjett og én for gjenstående budsjett. Rapporter som er basert på prognosemodeller, kan derfor bruke budsjettdata. Når et prosjektbudsjett er utført, oppretter systemet prognosetransaksjonene basert på de tilknyttede modellene, som brukes for rapportering og kontroll.

## <a name="forecast-models"></a>Prognosemodeller
Prognosemodeller har et enkeltlagshierarki. Dette betyr at én prosjektprognose må være tilknyttet én prognosemodell.

Hvis du bruker prosjektprognoser, kan du identifisere modeller som undermodeller. Du kan deretter opprette prognoser etter avdeling, tidsperiode eller område. Du kan for eksempel opprette en prognosemodell for et år og deretter opprette undermodeller for de regionale prognosene for Nordøst, Sørøst, Nordvest og Sørvest som regionale kontorer sender. Ved å velge forskjellige alternativer i de tilgjengelige rapportene kan du vise informasjon etter samlet prognose eller etter undermodell.




