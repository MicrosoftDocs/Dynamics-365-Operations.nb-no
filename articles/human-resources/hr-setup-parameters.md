---
title: Konfigurere parametere for Human Resources
description: Dette emnet forklarer hvordan du konfigurerer firmaspesifikke parametere i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889938"
---
# <a name="configure-human-resources-parameters"></a>Konfigurere parametere for Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Innstillingene for noen Human Resources-parametere deles mellom firmaer, mens innstillingene for andre parametere er firmaspesifikke. Dette emnet forklarer hvordan du konfigurerer firmaspesifikke parametere i Human Resources.

To sider brukes til å angi Human Resources-parametere. For parametere som deles på tvers av firmaer, bruker du siden **Delte parametere for personaladministrasjon**. For parameterne som er firmaspesifikke (altså innstillingene gjelder ett enkelt firma), bruker du siden **Personalparametere**.

![Gå til Human Resources-parametere](./media/hr-employee-self-service-human-resources-parameters.png)

På siden **Personalparametere** er innstillingene delt inn i seks kategorier:

- **Generelt**
- **Rekruttering** (denne fanen er ikke inkludert i Dynamics 365 Human Resources)
- **Kompensasjon**
- **Nummerserier**
- **FMLA**
- **Ansattselvbetjening**
- **Lederselvbetjening**
- **Fordelsbehandling**
- **Permisjon og fravær**
- **Betalingsmåter**

Hver kategori inneholder informasjon som gjelder ett enkelt firma.

## <a name="general"></a>Generelt

Innstillingene i kategorien **Generelt** definerer utseendet til informasjon om fravær, skade og sykdom og nye ansettelser. Innstillingene i denne kategorien definerer også noen standardoppføringer som vises når du arbeider. I denne fanen kan du spesifikt gjøre følgende:

- Velg en farge som skal brukes på åpne fraværstransaksjoner
- Angi stilarket som skal brukes for rapporter
- Aktivere integrering mellom kurs og fraværsregistrering
- Velg fraværskoden som skal brukes til å kontrollere denne integreringen.
- Angi hvor lenge hendelsene i tilfelle tilfeller av sykdom skal holdes under åpenhet og på grunn av sykdom.
- Angi standard identifikasjonsnummer som vises når en ny arbeider blir ansatt.

![Fanen Generelt](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Rekruttering

Innstillingene i fanen **Rekruttering** definerer dokumenttypene som brukes til korrespondanse, som automatisk sendes til søkere. Du kan også angi rekrutteringsprosjektet som brukes til uanførte søknader.

Perioden som er definert for aldersfordeling for rekrutteringsprosjekt bestemmer rekrutteringsprosjektene som er inkludert i flisen **Aldersfordelingsprosjekter** i arbeidsområdet **Rekrutteringsstyring**. Perioden som er definert for advarselen for tidsfrist for søknad, brukes til å vise rekrutteringsprosjekter som nærmer seg sin søknadsfrist på flisen **Søknadsfristen nærmer seg** i arbeidsområdet **Rekruttering**.

Hvis du vil ha mer informasjon om rekruttering, kan du se [Rekruttere jobbkandidater](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompensasjon

Innstillingene i fanen **Kompensasjon** i Dynamics 365 Finance definerer om brukere må bekrefte at de vil lagre informasjon for en fast eller variabel kompensasjonsplan. Hvis du merker av for **Aktiver lagring av validering**, mottar brukere en melding som spør om de vil lagre posten når de lukker en kompensasjonsrelatert side. Noen av sidene i Kompensasjonsstyring lar ikke brukere slette informasjon. Ved å be brukere bekrefte at de vil lagre informasjon, kan du kunne begrense mengden av informasjon som lagres, men som ikke kan slettes senere. Hvis du fjerner merket for **Aktiver lagring av validering**, lagres poster umiddelbart, muligens før brukeren er klar. Hvis du bruker Ytelsesstyring, kan du bruke fanen **Kompensasjon** til å velge en vurderingsmodell i stedet for å bruke modellen som er tilordnet til kompensasjonsplaner ved vurdering av ytelse.

I Human Resources kan du bruke fanen **Kompensasjon** til å velge å begrense tilgang til kompensasjonsplaner og angi en standardvaluta.

Hvis du vil ha mer informasjon om kompensasjon, kan du se [Oversikt over kompensasjonsplaner](hr-compensation-overview.md).

![Kategorien Kompensasjon](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Nummerserier

Innstillingene i fanen **Nummerserie** bestemmer seriene som brukes til automatisk å tilordne ID-er til varer i Human Resources, for eksempel:

- Søknader
- Fraværsregistreringer
- Resultater av kompensasjonsprosess
- Saksnumre
- Kurs
- Kursagendaer

Hvis du vil beholde nummerseriereferanser og -koder, kan du bruke listen **Nummerserier** (velg **Organisasjonsstyring > Nummerserier > Nummerserier**).

Hvis du vil ha mer informasjon, kan du se [Oversikt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Antall timer arbeidet kan ikke overskride 1250, og lengden på ansettelse kan ikke overskride 12 måneder. Disse maksimumsverdier er i overensstemmelse med gjeldende lovgivning i USA.

![Fanen Nummerserier](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

I fanen FMLA definerer du FMLA-rettighetskravene og FMLA-rettighetstimene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværsparametere](hr-leave-and-absence-parameters.md).

![FMLA-fane](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Ansattselvbetjening

Innstillingene i fanen **Selvbetjening for ansatte** påvirker hvordan Selvbetjening for ansatte vises for ansatte. I denne fanen kan du:

- Angi et navn for arbeidsområdet Selvbetjening for ansatte
- Velge hvilken informasjon en leder kan legge inn for ansatte
- Legge til nyttige koblinger for ansatte
- Hindre at ansatte legger til eller redigerer kontaktdetaljer for virksomhet. Hvis du vil ha mer informasjon, kan du se [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md).

Hvis du vil ha mer informasjon om hvordan du konfigurerer Selvbetjening for ansatte, kan du se [Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md).

![Fanen Selvbetjening for ansatte](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Lederselvbetjening

Innstillingene i fanen **Selvbetjening for leder** påvirker hva ledere ser i Selvbetjening for leder. I denne fanen kan du konfigurere følgende alternativer:

- Området for utløpsposter
- Informasjon som ledere kan vise i utløpsposter
- Om ledere kan vise åpne stillinger for utvidede rapporter
- Visninger av eksisterende arbeidere
- Nyttige koblinger for ledere

Hvis du vil ha mer informasjon om hvordan du konfigurerer Selvbetjening for leder, kan du se [Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md).

![Fanen Selvbetjening for leder](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Fordelsbehandling

I fanen Fordelsstyring kan du konfigurere e-postalternativer for Fordelsstyring. Hvis du vil ha informasjon om hvordan du konfigurerer og bruker Fordelsbehandling, kan du se [Oversikt over fordelsbehandling](hr-benefits-management-overview.md).

![Fanen Fordelsbehandling](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Permisjon og fravær

Hvis du vil ha informasjon om hvordan du konfigurerer og bruker Permisjon og fravær, kan du se [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Betalingsmåter

I fanen **Betalingsmåter** kan du velge betalingsmåtene som støttes av organisasjonen. Hvis du vil ha mer informasjon om hvordan du konfigurerer kompensasjon, kan du se [Oversikt over kompensasjonsplaner](hr-compensation-overview.md).

![Fanen Betalingsmåter](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]