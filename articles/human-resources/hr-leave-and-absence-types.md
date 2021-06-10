---
title: Konfigurere permisjons- og fraværstyper
description: Definer permisjonstyper som de ansatte kan ta i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 098f614da80a1e7e3e31b30cea707ecfbd5b0a70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056618"
---
# <a name="configure-leave-and-absence-types"></a>Konfigurere permisjons- og fraværstyper

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

2. Under **Oppsett** velger du **Permisjons- og fraværstyper**.

3. Velg **Ny**.

4. Angi et navn for permisjonstypen under **Type**, velg en arbeidsflyt fra **Arbeidsflyt-ID**, og angi en beskrivelse under **Beskrivelse**.

5. I **Generelt** velger du **Ingen**, **Planlagt** eller **Ikke planlagt** fra rullegardinlisten **Kategori**.

6. Velg en inntektskode fra rullegardinlisten **Inntektskode**.

7. Under **Årsakskode kreves** må du velge om du vil kreve en årsakskode. Hvis du vil kreve årsakskoder, kan det hende at du må legge dem til. Under **Årsakskoder** velger du **Legg til**, velger en årsakskode og merker av for **Aktivert** ved siden av den.

8. Under **Begrens tilgang til valgte roller** velger du om du vil begrense tilgangen. Deretter velger du sikkerhetsrollene under **Sikkerhetsroller for denne permisjonstypen**. Sikkerhetsrollene er definert i arbeidsflyten du valgte under **Arbeidsflyt-ID** tidligere i denne prosedyren.

9. Under **Kalenderfarge** velger du hvilken farge som skal vises på permisjons- og fraværskalendere for denne permisjonstypen. 

10. Under **Suspensjonsforbindelser** velger du om du vil at denne permisjonstypen skal suspendere en annen permisjonstype eller bli deaktivert av en annen permisjonstype. Når en fraværsforespørsel sendes for permisjonstypen "avbrudd", opprettes det automatisk et permisjonstidspunkt for den avbrutte permisjonstypen. 

10. Velg **Lagre**.

## <a name="configure-leave-type-rules"></a>Konfigurer regler for permisjonstyper

1. Angi avrundingsalternativer for permisjonstypen. Alternativene omfatter **Ingen**, **Opp**, **Ned** og **Nærmest**. Du kan også angi avrundingspresisjonen for permisjonstypen.

2. Angi **Helligdagskorrigering** for permisjonstypen. Når du velger dette alternativet, bruker Human Resources antallet helligdager som faller på en arbeidsdag, for å bestemme hvordan det skal avsettes avspasering for permisjonstypen. Hvis for eksempel første juledag faller på en mandag, vil Human Resources trekke én dag fra permisjonstypen ved behandling av avsetninger.

   Du angir helligdager i arbeidstidskalenderen. Hvis du vil ha mer informasjon, kan du se [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)
   
 3. Angi **Permisjonstypen overføring** som permisjonstype. Når du velger dette alternativet, blir alle overføringssaldoer overført til den angitte permisjonstypen. Permisjonstypen for overføring må også være inkludert i permisjons- og fraværsplanen. 
 
 4. Definer **Utløpsregler** for permisjonstypen. Når du konfigurerer dette alternativet, kan du velge dager eller måneder som enhet, og angi varigheten for utløpstiden. Du kan også angi gjeldende dato for utløpsregelen. Gyldighetsdatoen brukes til å avgjøre når den satsvise jobben som behandler permisjonsutløpet, eller datoen når regelen trer i kraft. Selve utløpet vil alltid skje på startdatoen for permisjonsplanen når den satsvise jobben er satt til behandling. Startdatoen for planen kan for eksempel være 1.1.2020, men regelen vil ikke bli opprettet før 1.6.2020. Hvis du setter gyldighetsdatoen til 1.6.2020, behandles regelen ved neste års grense, nemlig 1.1.2021. Eventuelle permisjonssaldoer som finnes på utløpstidspunktet, trekkes fra permisjonstypen, og gjenspeiles i permisjonssaldoen. 
 
## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)
- [Opprette en arbeidstidskalender](hr-leave-and-absence-working-time-calendar.md)
- [Suspender permisjon](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
