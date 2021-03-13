---
title: Vedlikeholde funksjoner i Human Resources
description: Lær hvordan du aktiverer eller deaktiverer nye funksjoner i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d400604bf1b044de52457b3f7a6eb858220a1972
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113754"
---
# <a name="manage-features-in-human-resources"></a>Vedlikeholde funksjoner i Human Resources

Som en del av vår kontinuerlige distribusjonen av ny funksjonalitet for Microsoft Dynamics 365 Human Resources vil vi at kunder får nye funksjoner så snart som mulig. Vi tilbyr forhåndsversjon av funksjoner, som nesten er klar for generelle tilgjengeligheten og har gjennomgått omfattende testing. Vi er bare ute etter en endelig runde med tilbakemelding og godkjenning før vi gjør dem generelt tilgjengelige.

Hvis du vil ha mer informasjon om nye funksjoner i Human Resources, kan du se [Hva er nytt i Human Resources](hr-admin-whats-new.md) og [lanseringsplan for Dynamics 365 og Power Platform ](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Arbeidsområdet **Funksjonsbehandling** inneholder en liste over funksjoner som leveres i hver utgivelse. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem. Hvis du vil ha mer informasjon om funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for **funksjonsbehandling**, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.

Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for **funksjonsbehandling** angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere forhåndsvisning av funksjoner

Hvis du vil ha tilgang til forhåndsvisningsfunksjoner, må du først aktivere dem i miljøet ditt. Aktivering eller deaktivering av forhåndsvisningsfunksjoner er miljøspesifikt.

> [!IMPORTANT]
> Forhåndsvisningsfunksjoner er bare tilgjengelige i **Sandkasse**-miljøer. Når du aktiverer en forhåndsversjon av en funksjon, aktiverer du den for alle brukere i organisasjonen som er i miljøet. Når du slår av funksjonen, kan du deaktivere den og gjøre den utilgjengelig for brukerne. Forhåndsvisningsfunksjoner har begrenset støtte i Human Resources. Du kan bruke færre personvern- og sikkerhetstiltak, og de er ikke inkludert i Human Resources-servicenivåavtalen (SLA). Du bør ikke bruke forhåndsvisningsfunksjoner til å behandle personlige data (det vil si all informasjon som kan identifisere deg), eller til å behandle andre data som er gjenstand for juridiske eller samsvarskrav.

1. Velg **Systemadministrasjon** i Human Resources.

2. Velg flisen **Funksjonsbehandling**.

3. Hvis du vil aktivere en forhåndsversjon av en funksjon, velger du den fra listen og velger deretter **Aktiver**. Hvis du vil deaktivere en forhåndsversjon av en funksjon, velger du den fra listen og velger deretter **Deaktiver**.

## <a name="enable-or-disable-benefits-management"></a>Aktivere eller deaktivere Fordelsbehandling

Hvis du vil aktivere Fordelsbehandling, bruker du samme fremgangsmåte som i [Aktivere eller deaktivere forhåndsvisningsfunksjoner](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Du kan ikke deaktivere Fordelsbehandling i et **produksjonsmiljø** etter at du har aktivert det. Du kan imidlertid deaktivere Fordelsbehandling i **sandkassemiljøer**.

Hvis du vil ha mer informasjon om konfigurasjon og bruk av Fordelsbehandling, kan du se [Oversikt over fordelsbehandling](hr-benefits-management-overview.md).

Fordelsbehandling erstatter funksjonalitet i arbeidsområdet **Fordeler**. Når du aktiverer forhåndsversjonen av funksjonen Fordelsbehandling, har du ikke lenger tilgang til følgende skjemaer i arbeidsområdet **Fordeler**:

- **Fordeler**
- **Fordelselementer**
- **Bidragsberegningssatser**
- **Resultater av fordelsregistrering**
- **Resultater for utløp og utvidelse av fordel**
- **Policyregeltyper for fordelsrettigheter**
- **Policyer for fordelsrettigheter**
- **Rettighetshendelser**

Du kan vise informasjonen i disse skjemaene i skrivebeskyttet modus. Hvis du vil redigere informasjonen, må du først deaktivere Fordelsbehandling (gjelder kun for **Sandkasse**-miljøer).

## <a name="enable-or-disable-leave-and-absence"></a>Aktivere eller deaktivere permisjon og fravær

Hvis du vil aktivere Permisjon og fravær, bruker du samme fremgangsmåte som i [Aktivere eller deaktivere forhåndsvisningsfunksjoner](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Du kan ikke deaktivere funksjonen **Flere permisjonstyper** i Permisjon og fravær etter at du har aktivert den. Dette gjelder både for **Sandkasse**- og **Produksjon**-miljøer.

For mer informasjon om forhåndsversjonsfunksjoner i Permisjon og fravær, se [Forhåndsversjonsfunksjoner for Permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Send tilbakemelding til oss

Vi hører gjerne fra deg om din erfaring med forhåndsvisningsfunksjoner. Vi oppfordrer deg til å postere regelmessig tilbakemelding på følgende områder når du bruker denne eller andre funksjoner:

- [Fellesskap](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – dette området er en flott ressurs der brukere kan diskutere brukstilfeller, spørsmål og få hjelp til fellesskapet.
- Gi oss beskjed om funksjoner du vil se i produktet, eller si fra om eventuelle endringer du mener vi bør gjøre i eksisterende funksjoner. Foreslå produktideer på [Human Resources-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Ikke ta med personlige data (informasjon som kan identifisere deg) i tilbakemeldingene eller innsendingene av produktgjennomgang. Innsamlet informasjon kan analyseres ytterligere, og den brukes ikke til å svare på forespørsler under gjeldende personvernlover. Personopplysninger som samles inn separat under disse programmene, er underlagt [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Se også

- [Hva er nytt i Human Resources](hr-admin-whats-new.md)
- [Lanseringsplan for Dynamics 365 og Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)