---
title: Oversikt over Fordelsbehandling
description: Oversikt over forhåndsversjonen av funksjonen Fordelsbehandling i Dynamics 365 Human Resources. Gi de ansatte utvidede fordelsalternativer med en brukervennlig Internett-opplevelse.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029469"
---
# <a name="benefits-management-overview"></a>Oversikt over Fordelsbehandling

[!include [banner](includes/preview-feature.md)]

For å være konkurransedyktig må du tilby et stort utvalg av fordeler for å tiltrekke deg og beholde de beste ansatte. I tillegg til standardfordeler som dekning av lege- og tannlegeutgifter ønsker du kanskje også å tilby utvidede tjenester, for eksempel starthjelp, rekreasjonsprogrammer og dekning av klær. Med forhåndsversjonen av funksjonen Fordelsbehandling i Microsoft Dynamics 365 Human Resources får du en fleksibel løsning som støtter en rekke ulike fordelsalternativer. Human Resources inneholder også en brukervennlig ansattopplevelse som viser tilbudene dine.

- Med forbedrede fordelsplaner kan du opprette og behandle unike fordelsplaner og støtte komplekse fordelsgradtabeller og nestede lag. Du kan enkelt opprette fordelsprogrammer, bunter og automatiske registreringsregler for å få en enklere ansattopplevelse.

- Med fleksible kredittprogrammer kan du vurdere å støtte pensjon og andre levetidshendelser.

- Omfattende rettighetsregler sikrer at du gjør de riktige fordelene tilgjengelig for de riktige ansatte.

- Fordelsregistrering på nettet gir en enkel opplevelse for dine ansatte.

- Kvalifisert levetidsbehandling er integrert med selvbetjening for ansatte, og støtter også fremtidige livshendelser.

Hvis du vil ha tilgang til demonstrasjonsdataene, må du distribuere sandkassemiljøet på nytt.

Du kan gi direkte tilbakemelding eller rapport problemer til: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Kjente problemer med Fordelsbehandling

### <a name="eligibility-processing"></a>Rettighetsbehandling

Ved pågående rettighet for fordeler som bruker et dekningsbeløp av typen 1–5 ganger lønn, prosent av lønn og flatt beløp, må du angi datoen for **Fordelsdetaljer** til **Medarbeiderens startdato** i **Ansettelseshistorikk**. Du må også ta med **Arbeidstimer**, **Betalingsfrekvens** og **Årlig lønnsbeløp for fordeler**. Hvis arbeideren har fast kompensasjon, angir du **Arbeidstimer** og **Betalingsfrekvens**. Det årlige lønnsbeløpet blir beregnet. Hvis den ansatte har fast lønn, trenger du ikke angi **Arbeidstimer**. Det anbefales at du angir fast kompensasjon først når du oppretter nye arbeidere. Du kan oppdatere posten med fordelsdetaljer ved å gå til **Arbeider > Arbeiderlogg > Ansettelsesdetaljer**. Juster datoen til arbeiderens startdato.

### <a name="employee-self-service"></a>Ansattselvbetjening

Den ansattes beløp beregnes ikke ved oppdatering av dekningsbeløpet for livsforsikring. Når en ansatt for eksempel blir tilbudt en livsforsikringsplan, kan de velge opptil $50 000 i dekning med en kost på $0,36 per $1000 dekning.  Når den ansatte oppdaterer dekningsbeløpet, forblir den ansattes tilknyttede kostpris null.

For en fordelsplan som bare tillater ett valg av denne plantypen, får brukeren en feilmelding hvis de prøver å frafalle en plan etter å ha valgt en plan. En bruker velger for eksempel en medisinsk plan og setter den inn i handlekurven. Brukeren velger deretter **Frafall** for en annen medisinsk plan. Brukeren vil motta en feil.

## <a name="enable-benefits-management"></a>Aktivere Fordelsbehandling

Fordelsbehandling er en forhåndsversjon av en funksjon og er bare tilgjengelig i **sandkassemiljøer**. Disse artiklene beskriver hvordan du aktiverer forhåndsversjoner av funksjoner i Human Resources. De forteller også hvilke eksisterende funksjoner i Human Resources som Fordelsbehandling erstatter, eller som deaktiveres når du aktiverer Fordelsbehandling.

- [Behandle funksjoner](hr-admin-manage-features.md)
- [Forhåndsversjon av funksjon: Fordelsbehandling](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Konfigurere Fordelsbehandling

Før du kan opprette fordelsplaner for de ansatte, må du konfigurere alternativer for planene.

- [Se parametere i Fordelsbehandling](hr-benefits-setup-parameters.md)
- [Konfigurere rettighetsregler og -alternativer](hr-benefits-setup-eligibility-rules.md)
- [Konfigurere alternativer for personlige kontaktrettigheter](hr-benefits-setup-contact-eligibility-options.md)
- [Opprette dekningsalternativer](hr-benefits-setup-coverage-options.md)
- [Definere betalingsfrekvenser](hr-benefits-setup-payment-frequencies.md)
- [Konfigurere levetidshendelsestyper](hr-benefits-setup-life-event-types.md)
- [Opprette plantyper](hr-benefits-setup-plan-types.md)
- [Definer årsakskoder](hr-benefits-setup-reason-codes.md)
- [Definer lagkoder](hr-benefits-setup-tier-codes.md)
- [Konfigurere satser](hr-benefits-setup-rates.md)
- [Konfigurere fradrag](hr-benefits-setup-deductions.md)
- [Konfigurere ventedager](hr-benefits-setup-waiting-days.md)
- [Konfigurere venteperioder](hr-benefits-setup-waiting-periods.md)
- [Definere avrundingsregler](hr-benefits-setup-rounding-rules.md)
- [Opprett ansettelseskategorier](hr-benefits-setup-employment-categories.md)
- [Definere ansettelsestyper](hr-benefits-setup-employment-types.md)
- [Konfigurere ansattselvbetjening](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Opprette fordelsplaner

Disse artiklene viser hvordan du kan opprette fordelsplaner, inkludert bunter og fleksible kredittprogrammer.

- [Definere fordelsplaner](hr-benefits-plans-setup.md)
- [Opprette fordelsplaner for ansatte](hr-benefits-plans-worker.md)
- [Definere fleksible kredittprogrammer](hr-benefits-plans-flex-credit-programs.md)
- [Konfigurere fremtidige levetidshendelser](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Behandle fordelsplaner

Du må behandle noen av endringene for å aktivere dem.

- [Fordelsregistreringsrettighet](hr-benefits-process-enrollment-eligibility.md)
- [Behandle levetidshendelser](hr-benefits-process-life-events.md)
- [Behandle endringer i levetidshendelser](hr-benefits-process-life-event-changes.md)
- [Behandle rettighet for levetidshendelser](hr-benefits-process-life-event-eligibility.md)
- [Behandle satsendringer](hr-benefits-process-rate-changes.md)

