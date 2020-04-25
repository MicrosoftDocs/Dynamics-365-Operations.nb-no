---
title: Konfigurere permisjons- og fraværstyper
description: Definer permisjonstyper som de ansatte kan ta i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198056"
---
# <a name="configure-leave-and-absence-types"></a>Konfigurere permisjons- og fraværstyper

Permisjonstyper i Dynamics 365 Human Resources definerer de ulike typene fravær som ansatte kan rapportere. Du kan skreddersy permisjonstyper i henhold til behovene i organisasjonen. Eksempler på permisjonstyper omfatter:

- Betalt avspasering (PTO)
- Fravær uten lønn
- Betalt ferie
- Sykepermisjon
- Sykepermisjon
- Familiepermisjon
- Kortsiktig uførhet
- Eksamenspermisjon

## <a name="add-a-leave-type"></a>Legge til en permisjonstype

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett**velger du **Permisjons- og fraværstyper**.

3. Velg **Ny**.

4. Angi et navn for permisjonstypen under **Type**, velg en arbeidsflyt fra **Arbeidsflyt-ID**, og angi en beskrivelse under **Beskrivelse**.

5. I **Generelt** velger du **Ingen**, **Planlagt** eller **Ikke planlagt** fra rullegardinlisten **Kategori**.

6. Velg en inntektskode fra rullegardinlisten **Inntektskode**.

7. Under **Årsakskode kreves** må du velge om du vil kreve en årsakskode. Hvis du vil kreve årsakskoder, kan det hende at du må legge dem til. Under **Årsakskoder** velger du **Legg til**, velger en årsakskode og merker av for **Aktivert** ved siden av den.

8. Under **Begrens tilgang til valgte roller** velger du om du vil begrense tilgangen. Deretter velger du sikkerhetsrollene under **Sikkerhetsroller for denne permisjonstypen**. Sikkerhetsrollene er definert i arbeidsflyten du valgte under **Arbeidsflyt-ID** tidligere i denne prosedyren.

9. Velg **Lagre**.

## <a name="configure-leave-type-rules"></a>Konfigurer regler for permisjonstyper

1. Angi avrundingsalternativer for permisjonstypen. Alternativene omfatter **Ingen**, **Opp**, **Ned** og **Nærmest**. Du kan også angi avrundingspresisjonen for permisjonstypen.

2. Angi **Helligdagskorrigering** for permisjonstypen. Når du velger dette alternativet, bruker Human Resources antallet helligdager som faller på en arbeidsdag, for å bestemme hvordan det skal avsettes avspasering for permisjonstypen. Hvis for eksempel første juledag faller på en mandag, vil Human Resources trekke én dag fra permisjonstypen ved behandling av avsetninger.

   Du angir helligdager i arbeidstidskalenderen. Hvis du vil ha mer informasjon, kan du se [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)
   
## <a name="configure-preview-features"></a>Konfigurere forhåndsversjonsfunksjoner

Hvis du har aktivert forhåndsversjonsfunksjoner for permisjon og fravær, må du konfigurere innstillinger for dem også.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Velg permisjonstypen for overføringssaldoer som skal overføres. Du kan også opprette en ny permisjonstype for overføring. 

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)
- [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)
