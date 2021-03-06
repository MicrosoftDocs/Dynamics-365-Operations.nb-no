---
title: Oversikt over fordelsbehandling
description: Oversikt over funksjonen Fordelsbehandling i Dynamics 365 Human Resources. Gi de ansatte utvidede fordelsalternativer med en brukervennlig Internett-opplevelse.
author: andreabichsel
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b6ace2ce83c668e83ec1b433f8062148a6dfaf4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059070"
---
# <a name="benefits-management-overview"></a>Oversikt over Fordelsbehandling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte. I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær. Med Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer. Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.

- Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag. Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.

- Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.

- Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.

- Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.

- Behandling av kvalifisert levetidshendelse støtter fremtidige levetidshendelser.

Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.

>[!NOTE]
>Du kan nå tilpasse skjemaer for Fordelsbehandling. Du kan nå legge til egendefinerte felt relatert til dekningssatser i **Dekningsalternativ**-skjemaet for fordelsplaner. Hvis du vil ha mer informasjon om å arbeide med egendefinerte felt, kan du se [Egendefinerte felt](hr-developer-custom-fields.md).
>![Egendefinerte felt for fordelsbehandling](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Aktivere Fordelsbehandling

Dette emnet beskriver hvordan du aktiverer funksjoner i Human Resources. Den forteller også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, eller som deaktiveres når du aktiverer Fordelsbehandling.

> [!IMPORTANT]
> Du kan ikke deaktivere Fordelsbehandling i et **produksjonsmiljø** etter at du har aktivert det. Det anbefales at du aktiverer og tester Fordelsbehandling i et **Sandkasse**-miljø før du aktiverer det i et **Produksjon**-miljø. Det er store forskjeller mellom den eldre Fordel-funksjonaliteten og den nye Fordelsbehandling-funksjonaliteten, som krever ekstra oppsett, og som bør testes før den blir satt i produksjon.

- [Behandle funksjoner](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Konfigurere informasjon om ansatte

Før du kan registrere ansatte i fordeler, må du angi nødvendig informasjon. Du må registrere en ansatt i en **fast kompensasjonsplan** på startdatoen, og du må velge en **frekvens for fordelsbetaling** i **ansettelsesdetaljene** i **Arbeider**-skjemaet.

Hvis du har en ansatt som får tilleggskompensasjon som provisjon, kan du legge til et **årlig lønnsbeløp for fordeler** fra ansattposten. Human Resources bruker **årlig lønnsbeløp for fordeler** når de fastsetter dekningsbeløp i stedet for det årlige beløpet for fast kompensasjonen. **Årlig lønnsbeløp for fordeler** må være gyldig per den ansattes startdato eller starte av fordelsperioden, avhengig av hva som er sist. Hvis både fast kompensasjon og årlig lønnsbeløp for fordeler registreres for en ansatt, blir årlig lønnsbeløp for fordeler brukt til å bestemme dekningsbeløp.

Når du oppretter en fordelsplan som bruker satser som er basert på kjønn eller alder, må du angi en fødselsdato og et kjønn for den ansatte for å beregne fordelskostnaden.

## <a name="configure-benefits-management"></a>Konfigurere fordelsbehandling

Før du kan opprette fordelsplaner for de ansatte, må du konfigurere alternativer for planene.

- [Se parametere i Fordelsbehandling](hr-benefits-setup-parameters.md)
- [Konfigurere rettighetsregler og -alternativer](hr-benefits-setup-eligibility-rules.md)
- [Konfigurere alternativer for personlige kontaktrettigheter](hr-benefits-setup-contact-eligibility-options.md)
- [Opprette dekningsalternativer](hr-benefits-setup-coverage-options.md)
- [Definere betalingshyppigheter](hr-benefits-setup-payment-frequencies.md)
- [Konfigurere hendelsestyper for levetid](hr-benefits-setup-life-event-types.md)
- [Opprette plantyper](hr-benefits-setup-plan-types.md)
- [Definer årsakskoder](hr-benefits-setup-reason-codes.md)
- [Definere lagkoder](hr-benefits-setup-tier-codes.md)
- [Konfigurere satser](hr-benefits-setup-rates.md)
- [Konfigurere fradrag](hr-benefits-setup-deductions.md)
- [Konfigurere ventedager](hr-benefits-setup-waiting-days.md)
- [Konfigurere venteperioder](hr-benefits-setup-waiting-periods.md)
- [Definere avrundingsregler](hr-benefits-setup-rounding-rules.md)
- [Opprette ansettelseskategorier](hr-benefits-setup-employment-categories.md)
- [Definere ansettelsestyper](hr-benefits-setup-employment-types.md)
- [Konfigurere ansattselvbetjening](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Opprette fordelsplaner

Disse artiklene viser hvordan du kan opprette fordelsplaner, inkludert bunter og fleksible kredittprogrammer.

- [Definere fordelsplaner](hr-benefits-plans-setup.md)
- [Definere fleksible kredittprogrammer](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Behandle fordelsplaner

Du må behandle noen av endringene for å aktivere dem.

- [Fordelsregistreringsrettighet](hr-benefits-process-enrollment-eligibility.md)
- [Behandle levetidshendelser](hr-benefits-process-life-events.md)
- [Behandle endringer i levetidshendelser](hr-benefits-process-life-event-changes.md)
- [Behandle rettighet for levetidshendelser](hr-benefits-process-life-event-eligibility.md)
- [Behandle satsendringer](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]