---
title: Opprette en teamkalender
description: Du kan vise og opprette teamkalendere i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0679a69b4d607f9d466474026d5dd0ceef0dad6f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692205"
---
# <a name="view-team-and-company-calendars"></a>Vis team- og firmakalendere

>[!Important]
>Funksjonaliteten som er nevnt i dette emnet, er for øyeblikket tilgjengelig for kunder i frittstående Dynamics 365 Human Resources. Noe av eller all funksjonaliteten vil være tilgjengelig som en del av en fremtidig versjon av Finance-infrastrukturen etter Finance versjon 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan vise team- og firmakalendere i Dynamics 365 Human Resources. Teamkalendere viser bare direkte underordnede, som definert i linjehierarkiet.

## <a name="view-your-team-calendar-as-an-employee"></a>Vise teamkalenderen som en ansatt

- I arbeidsområdet **Ansattselvbetjening** velger du **Fraværskalender for team** under **Sammendrag**.

## <a name="view-your-team-calendar-as-a-manager"></a>Vise teamkalenderen som en leder

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mitt team**.

2. Velg **Permisjon og fravær**, og velg deretter **Vis fraværskalender for ledere**.

Ledere kan også få tilgang til teamkalenderen fra **Ventende fritidsforespørsler for teamet mitt**, **Godkjent avspasering** og **Avspaseringsforespørsler**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Vise fraværsbehandlingskalenderen som fraværsansvarlig

> [!NOTE]
> Hvis du vil vise fraværsbehandlingskalenderen, må du først aktivere funksjonen for **(forhåndsversjon) fraværsbehandling for å administrere permisjon** i Funksjonsbehandling. Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

Brukere i fraværsbehandlingsrollen kan vise tidsforespørsler i kalenderen. Hvis du vil ha tilgang til fraværskalenderen, kan du følge disse trinnene.

1. I arbeidsområdet **Ansattselvbetjening** velger du **Fraværsbehandling** og deretter **Fraværsbehandlingskalender**.

2. Angi ønskede datoer i **Dato**-feltet.

3. Oppdater visningsalternativene etter behov.

Fraværsbehandlingskalenderen viser alle postene for de ansatte som rapporterer til fraværslederen i permisjonshierarkiet.

## <a name="view-a-company-calendar"></a>Vise en firmakalender

Personer som er i Human Resources-roller, kan vise firmakalendere. Firmakalendere viser alle ansatte. Som standard viser kalenderen dagens dato pluss 28 dager, men du kan endre datointervallet. Du kan også filtrere kalenderen etter **Navn**, **Personalnummer** og **Permisjonstype**.

1. I arbeidsområdet **Permisjon og fravær** velger du **Koblinger**.

2. Velg **Permisjons- og fraværskalender**.

Human Resources-roller kan også få tilgang til firmakalenderen fra **Permisjons- og fraværsforespørsler**, **Godkjent avspasering** og **Avspaseringsforespørsler**. 

Kalendere inneholder nå flere filtre og alternativer. Alle kalendere inneholder visningsalternativer for:

- Godkjente forespørsler
- Ventende forespørsler
- Ansatte med permisjonsforespørsler
- Ansatte uten permisjonsforespørsler
- Ansattes fødselsdager
- Forespørsler om fridager 
- Permisjonsforespørsler

Kalenderkonfigurasjon på siden for **permisjons- og fraværsparametere** bestemmer tilgjengelige visningsalternativer.

Du kan også filtrere kalendere etter leder eller avdeling. Den primære stillingstilordningen bestemmer hvilke ansatte som vises når disse filtrene stilles inn. 

> [!IMPORTANT]
> Du kan aktivere funksjonen **Permisjonsvisning på tvers av firmaer** i Funksjonsbehandling. Deretter må du aktivere funksjonen på siden **delte parametere for Human Resources** for å vise filteret for juridisk enhet i kalendere. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværsparametere](hr-leave-and-absence-parameters.md).
> 
> Du kan filtrere kalenderen etter juridisk enhet. Hvis du vil se alle ansatte uavhengig av juridisk enhet, fjerner du filterfeltet og velger **Enter**. 

Hvis du vil ha informasjon om kalenderinnstillinger, kan du se [Konfigurere kalenderparametere](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
