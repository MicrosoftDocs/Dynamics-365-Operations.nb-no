---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (24. mars 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 83f24dd6f094715f96666c3ae94faa4bdb97a652
ms.sourcegitcommit: fac1d519a85eab0c936b54e0a9247f6a11842871
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2020
ms.locfileid: "3177943"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-24-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (24. mars 2020)?

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3073. Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Grenser for Human Resources-miljø er nå basert på den oppdaterte lisensen (394595)

Grensen for antall miljøer per prosjekt i Lifecycle Services (LCS) er endret. Den forrige grensen var to miljøer. Grensen for antall produksjons- og sandkassemiljøer du kan opprette for Human Resources i LCS, er nå basert på oppdatert lisens. Du kan nå opprette så mange miljøer som nødvendig per LCS-prosjekt, avhengig av antall lisenser som er kjøpt. Den nye lisensieringen, som oppdateres 1. februar 2020, gjør det mulig for kundene å kjøpe flere miljøer. Hvis du vil ha mer informasjon om lisenskrav for flere miljøer, kan du se [lisensieringsveiledningen for Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="platform-changes"></a>Plattformendringer

- Helside-apper (forhåndsvisning) - Denne forhåndsvisningsfunksjonen, som krever at du aktiverer funksjonen Lagrede visninger, gjør at Power Apps og tredjepartsapper kan legges til som helside-opplevelser via instrumentbordet.

- Lagrede visninger (forhåndsvisning) - Denne forhåndsvisningsfunksjonen aktiverer lagrede visninger, som er en betydelig forbedring av delsystemet for tilpassing. Med denne funksjonen kan brukere ha flere navngitte sett med tilpasninger per side. Du kan også publisere visninger til sikkerhetsroller.

- Optimalisert "er en av"-filtreringsopplevelse - Denne funksjonen aktiverer en optimalisert "er en av"-filtreringsopplevelse som gjør det enklere å angi flere filterverdier, har enklere mekanisme for å fjerne individuelle eller alle filterverdier, og har en mer kompakt og intuitiv visualisering av filterverdier.

- Anbefalte felt – Brukere må ofte legge til felt i et rutenett eller en side. Dette kan være vanskelig med så mange tilgjengelige felt. I stedet for å måtte søke gjennom en stor liste, gjør denne funksjonen det mulig for systemet å bruke et sett av anbefalte felt basert på hvilke andre brukere oftest legger til i lignende scenarioer.

- Trege standardhandlinger i rutenett – Denne funksjonen sikrer at standardhandlingen i et rutenett er koblet til en bestemt kolonne i et rutenett, uansett om kolonnen er flyttet eller skjult.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-multiple-leave-type-feature-on-419635"></a>Kan ikke justere permisjonssaldo for en plan uten avsetninger som ble opprettet med funksjonen Flere permisjonstyper på (419635)

Med denne endringen kan du justere saldoer for permisjonsplaner som har blitt opprettet med funksjonen Flere permisjonstyper (forhåndsvisning) aktivert i Funksjonsbehandling.

## <a name="in-preview"></a>I forhåndsvisning

Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:

- **Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service-løsningen er nå tilgjengelig med følgende endringer:

| beskrivelse | Vekslepenger |
| --- | --- |
| Endringer i enheten **Jobb/stilling** | <ul><li>**Kompensasjonsområde** lagt til</li>|
| **Stillingsdimensjon**-enhet er lagt til | <ul><li>**Finansdimensjoner** lagt til</li>
| Endringer i **Arbeider**-enheten | <ul><li>**Navnerekkefølge** lagt til</li><li>**Arbeider hjemmefra** lagt til</li><li>**Språk** lagt til</li><li>**Ansiennitetsdato** lagt til</li><li>**Jubileumsdato** lagt til</li><li>**Opprinnelig ansettelsesdato** lagt til</li></ul> |
| Endringer i **Ansettelse**-enheten | <ul><li>**Finansdimensjoner** lagt til</li><li>**Avslutningsårsak** lagt til</li><li>**Avslutningsdato** endret navn fra **Overgangsdato**</li><li>**Prøvedato** lagt til</li></ul> |
| Endringer i **Arbeideradresse**-enheten | <ul><li>**Gateadresse** lagt til</li><li>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving</li></ul> |
| Nye enheter for oppsett av variabel kompensasjon | <ul><li>**Type variabel kompensasjonsplan**</li><li>**Variabel plan for kompensasjon**</li><li>**Overdragelsesregler**</li><li>**Nivå for variabel kompensasjonsplan**</li></ul> |
| Ny enhet, **Ansettelse i arbeiderkalender** | <ul><li>**Arbeidskalenderenhet** lagt til</li></ul> |
| Ny enhet, **Lønnstillingsdetaljer** | <ul><li>**Lønnsstillingsdetaljer** lagt til</li></ul> |
| Ny **Tittel**-enhet | <ul><li>**Tittel** lagt til</li></ul>Den nye **Tittel**-enheten er inkludert i Common Data Service, men refereres ikke til fra **Stilling**- eller **Jobb**-enhetene på dette tidspunktet. |

> [!NOTE]
> Finansdimensjoner for både stillinger og ansettelse tilbyr en-veis integrering for oppdateringer fra Human Resources til Common Data Service. Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Common Data Service til Human Resources.

De neste ukene vil disse enhetsendringene være tilgjengelige i alle miljøer. Slik installerer du den nyeste Common Data Service-løsningen for Human Resources manuelt:

1.  Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com).

2.  Velg **Miljøer**.

3.  Finn miljøet du vil oppgradere. Miljøet må samsvare med **miljønavn** i **Common Data Service**-informasjonsdelen i **Om**-skjemaet i Human Resources.

4.  Velg miljøet for å vise miljødetaljer.

5.  Velg **Administrer løsninger** på handlingslinjen øverst. Et nytt leservindu åpner og navigerer til **Administrasjonssenter for Dynamics 365** i konteksten til miljøet ditt.

6.  I **Løsning**-listen velger du **Dynamics 365 Human Resources Anker**.

7.  Velg **Oppgrader** hvis du vil bruke den nyeste løsningen.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer

Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:

1. Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen. Du kan vise denne informasjonen på **Bruker**-siden. Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData. Som standard finnes ikke e-postadressen i Excel-utformingen. Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere. Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.

3. Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.

4. Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.

## <a name="coming-soon"></a>Kommer snart

## <a name="new-production-release-cadence"></a>Ny produksjonslanseringsfrekvens

Fra og med april vil lanseringsfrekvensen for Human Resources skifte fra en ukentlig oppdatering til en oppdatering annenhver uke. For å sikre innretting etter sikre distribusjonspraksiser og opprettholde høye standarder for stabilitet og pålitelighet i tjenesten, vil prosessen med å distribuere serviceoppdateringer til alle områder bli en to-ukes distribusjon. Flere tester og skjermer vil være på plass for å bekrefte vellykket distribusjon på hvert trinn i prosessen. Hvis du vil ha mer informasjon om lanseringsfrekvensen, kan du se [Oppdateringsprosess](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Kjente problemer

## <a name="employment-detail-entity"></a>Enheten Ansettelsesdetalj

Enheten **Ansettelsesdetalj** er oppdatert med følgende felt: **Lønnsfrekvens**, **ID for ansettelseskategori**, **Ansettelsestyper**, **ID for ansettelsestype** og **Ansettelsesstatus for fordel**. Oppsettsdataene for disse feltene er avhengig av fordelsadministrasjonen som aktiveres i Funksjonsbehandling. Disse feltene bør ikke fylles ut eller oppdateres enheten **Ansettlesesdetalj** fordi det vil føre til feil under importen.
