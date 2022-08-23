---
title: Synkronisere med prismotoren for Supply Chain Management ved behov
description: Denne artikkelen beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Supply Chain Management fra Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 727e60ceee3f5c8c33d2da93128eedc1dc7bcb9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288964"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synkronisere med prismotoren for Supply Chain Management ved behov

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management inkluderer en prissettingsmotor som håndterer forretningsavtaler, prislister, fordelsprogrammer, kampanjer og rabatter. Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre. Når du bruker dobbel skriving, bruker du enten statisk prissetting eller prissettingsmotoren fra Supply Chain Management på sidene **Tilbud** og **Ordre** i Microsoft Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Bruk prissettingsmotoren fra Supply Chain Management i Sales

1. I Sales går du til **Salg \> Ordrer**.
1. Velg **Ny** for å opprette en ny ordre, eller velg en eksisterende ordre i **Mine ordrer**-listen.
1. Legg til en ny ordrelinje.
1. Hvis du oppretter en ny ordre, velger du **Prisordre** i handlingsruten. Hvis du oppdaterer en eksisterende ordre, velger du **Beregn på nytt** i handlingsruten.
1. Følgende kolonner fylles ut automatisk:

    - Detaljbeløp
    - Rabatt-%
    - Rabatt
    - Beløp før frakt
    - Fraktbeløp
    - Samlet avgift
    - Totalbeløp

> [!NOTE]
> En lignende prosess gjelder når du oppretter tilbud.

## <a name="how-it-works"></a>Hvordan det fungerer

Når du oppretter en ordre i Salg, synkroniseres denne ordren umiddelbart med Supply Chain Management ved hjelp av verdiene du angav i Salg. Når du velger **Prisordre** eller **Pristilbud** i Salg, beregner Supply Chain Management prisen for hver ordrelinje, samt totalordren, basert på forretningsavtaleregler som er definert i Supply Chain Management. De nye beregnede verdiene blir deretter synkronisert tilbake til Salg.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Angi evalueringsalternativer for forretningsavtaler i Supply Chain Management

Du kan konfigurere Supply Chain Management til å enten overholde eller ignorere forretningsavtaler når det beregner prisen på en ordre som ble opprettet i Salg. Følg fremgangsmåten nedenfor for å definere dette alternativet.

1. Logg på Supply Chain Management-miljøet.
1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
1. På fanen **Priser**, på hurtigfanen **Evaluering av handelssavtale**, legger du til eller fjerner raden for policyen **Manuell registrering** etter behov. Prissettingsmotoren i Supply Chain Management vil automatisk overstyre salgsprisen som ble angitt i Salg, avhengig av om denne policyen finnes eller ikke.

    - Hvis policyen **Manuell registrering** *ikke* finnes i oppsettet av **Evaluering av handelsavtale**, bestemmes prisen av Supply Chain Management. Når en bruker velger **Prisordre** eller **Pristilbud** i handlingsruten i Salg, kalles prissettingsmotoren i Supply Chain Management, og salgsprisen som ble angitt i Salg, overskrives hvis den ikke tilsvarer salgsprisen som er beregnet i Supply Chain Management.
    - Hvis policyen **Manuell registrering** *ikke* finnes i oppsettet av **Evaluering av handelsavtale**, bestemmes prisen av Salg. Salgsprisen som ble angitt i Salg, blir forhindret fra å bli automatisk overskrevet når en bruker velger **Prisordre** eller **Pristilbud** i handlingsruten i Salg.
    - Ordrelinjer og tilbudslinjer som har en verdi for **Pris per enhet** og/eller **Rabatt** på *0* (null) i Salg, behandles som et spesialtilfelle. Hvis en relevant forretningsavtalepris er tilgjengelig, vil Supply Chain Management *alltid* bruke den på disse feltene, uavhengig av oppsettet for **Evaluering av handelssavtale**.

    Hvis du vil se et eksempel på hvert av disse tilfellene, kan du se scenarioene nedenfor.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Eksempelscenario 1: Evaluering av handelssavtale uten alternativet Manuell registrering

I dette scenarioet vil oppsettet for **Evaluering av forretningsavtale** i Supply Chain Management *ikke* inkludere policyen **Manuell registrering**. En salgsbruker angir en ordrelinje som har en salgspris som ikke er null, i Salg, og det er ikke definert noen salgspris for varen i Supply Chain Management.

1. I Salg oppretter en bruker en ordrelinje som har en verdi for **Pris per enhet** på 1 dollar (USD).
1. Ordrelinjen synkroniseres med Supply Chain Management med en salgspris på 1 USD.
1. I Salg velger brukeren **Prisordre** i handlingsruten.
1. Supply Chain Management søker etter relevante priser og rabatter og beregner deretter totalsummer. Fordi varen ikke har noen salgspris i Supply Chain Management, oppdaterer beregningen linjen slik at den har en salgspris på 0 USD.
1. Den nye salgsprisen for linjen synkroniseres tilbake til Salg.
1. Resultatet er en ordrelinje i Salg som har en salgspris på 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Eksempelscenario 2: Evaluering av handelssavtale med alternativet Manuell registrering

I dette scenarioet vil oppsettet for **Evaluering av forretningsavtale** i Supply Chain Management *inkludere* policyen **Manuell registrering**. En salgsbruker angir en ordrelinje som har en salgspris som ikke er null i Salg. Supply Chain Management inneholder en forretningsavtale som definerer en salgspris på 2 USD for den bestilte varen.

1. I Salg oppretter en bruker en ordrelinje for en vare som har en verdi for **Pris per enhet** på 1 USD.
1. Ordrelinjen synkroniseres med Supply Chain Management med en salgspris på 1 USD.
1. I Salg velger brukeren **Prisordre** i handlingsruten.
1. Siden oppsettet for **Evaluering av handelssavtale** i Supply Chain Management inkluderer policyen **Manuell registrering**, endres ikke salgsprisen, selv om en aktuell handelsavtale spesifiserer en annen salgspris.
1. Salgsprisen forblir uendret i Salg og i Supply Chain Management.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Eksempelscenario 3: Evaluering av handelsavtale for en vare som har en salgspris på null i Salg

I dette scenarioet vil oppsettet for **Evaluering av forretningsavtale** i Supply Chain Management *inkludere* policyen **Manuell registrering**. Salgsbrukeren angir en ordrelinje som har en salgspris på 0 (null) i Salg. Supply Chain Management inneholder en forretningsavtale som definerer en salgspris på 2 USD for en bestilt vare.

1. I Salg oppretter en bruker en ordrelinje som har en verdi for **Pris per enhet** på 0 USD og en verdi for **Linjerabatt** på 0 USD.
1. Ordrelinjen synkroniseres med Supply Chain Management med en salgspris på 0 USD.
1. Fordi den mottok en ordrelinje som har en salgspris på 0 (null), kaller Supply Chain Management opp dens prissettingsmotor, selv om alternativet **Manuell registrering** er aktivert. Prissettingsmotoren returnerer salgsprisen på 2 USD som er fastsatt av handelsavtalen, og oppdaterer ordrelinjen i Supply Chain Management.
1. Den oppdaterte salgsprisen er ennå ikke synkronisert med ordrelinjen i Salg.
1. I Salg velger brukeren **Prisordre** i handlingsruten.
1. Ordrelinjen i Supply Chain Management beholder salgsprisen på 2 USD, som nå synkroniseres tilbake til Salg. Derfor oppdateres verdien for **Pris per enhet** for ordrelinjen i Salg fra 0 USD til 2 USD.
1. I Salg angir brukeren en ny rabatt for **Linjerabatt** på 0,50 USD. Salg beregner nå at verdien av **Utvidet beløp** for linjen er på 1,50 USD.
1. Ordrelinjen synkroniseres med Supply Chain Management med en verdi for **Linjerabatt** på 0,50 USD.
1. I Salg velger brukeren **Prisordre** i handlingsruten.
1. Ingen priser eller rabatter endres for ordrelinjen i Salg.

## <a name="limitations"></a>Begrensninger

Når kolonnene i Sales fylles ut, gjelder følgende begrensninger:

- Oppsettet av gebyrer og gebyrfordelinger i Supply Chain Management replikeres ikke i Sales.
- Prissetting tar ikke hensyn til spesielle detaljhandelpriser som er angitt i **Detaljhandelskanal**-kolonnen på salgsordrelinje-siden i Supply Chain Management.
- Rabatter som er definert i delen **Handelsrabattbehandling** i Supply Chain Management, vurderes ikke.
- Prissetting vurderer ikke salgsavtaler.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
