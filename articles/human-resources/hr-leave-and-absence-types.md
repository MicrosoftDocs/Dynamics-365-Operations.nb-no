---
title: Konfigurere permisjons- og fraværstyper
description: Definer permisjonstyper som de ansatte kan ta i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 07/16/2021
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
ms.openlocfilehash: 63970f69a437864675eada975c54446325fb60e2
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639588"
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
 
4. Definer **Utløpsregler** for permisjonstypen. Når du konfigurerer dette alternativet, kan du velge dager eller måneder som enhet, og angi varigheten for utløpstiden. Gyldighetsdatoen for utløpsregelen brukes til å avgjøre når den satsvise jobben som behandler permisjonsutløpet, eller datoen når regelen trer i kraft. Selve utløpet skjer alltid på startdatoen for avsetningsperioden. Hvis startdatoen for avsetningsperioden for eksempel er 3. august 2021, og utløpsregelen ble definert til 6 måneder, behandles regelen basert på utløpsdatoen fra startdatoen for avsetningsperioden, slik at den vil bli utført 3. februar 2022. Eventuelle permisjonssaldoer som finnes på utløpstidspunktet, trekkes fra permisjonstypen, og gjenspeiles i permisjonssaldoen.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Konfigurere nødvendig vedlegg per permisjonstype

> [!NOTE]
> For å bruke feltet **Vedlegg kreves** må du først slå på funksjonen for å **(forhåndsversjon) konfigurere nødvendige vedlegg for permisjonsforespørsler** i Funksjonsbehandling. Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

1. På siden **Permisjon og fravær**, i kategorien **Koblinger** under **Oppsett**, velger du **Permisjons- og fraværstyper**.

2. Velg en permisjons- og fraværstype i listen. I delen **Generelt** bruker du feltet **Vedlegg kreves** til å angi om et vedlegg må lastes opp når en ansatt sender en ny permisjonsforespørsel for den valgte permisjonstypen. 

Ansatte må laste opp et vedlegg når de sender en ny permisjonsforespørsel som har en permisjonstype der feltet **Vedlegg kreves**, er aktivert. Hvis du vil vise vedlegget som ble lastet opp som en del av en permisjonsforespørsel, kan godkjennere av permisjonsforespørsel bruke **Vedlegg**-alternativet for arbeidselementene som er tilordnet dem. Hvis du får tilgang til en permisjonsforespørsel ved hjelp av Human Resources-appen i Microsoft Teams kan **Vis detaljer**-alternativet for permisjonsforespørselen brukes til å vise detaljer og vedlegg.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Konfigurer permisjonsenheter (timer/dager) per permisjonstype

> [!NOTE]
> Hvis du vil bruke permisjonsenhetene per permisjonstype-funksjonalitet, må du først aktivere funksjonen **(Forhåndsversjon) Konfigurer permisjonsenheter per permisjonstype** i Funksjonsbehandling. Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

> [!IMPORTANT]
> Som standard bruker permisjonstypene i en juridisk enhet permisjonsenhetene fra konfigurasjonen av permisjonsparametere på juridisk enhet-nivå.
> 
> Permisjonsenheten for en permisjons- og fraværstype kan bare endres hvis det ikke er noen permisjonstransaksjoner for denne permisjonstypen.
> 
> Når funksjonen er aktivert, kan den ikke deaktiveres.

1. På siden **Permisjon og fravær**, i kategorien **Koblinger** under **Oppsett**, velger du **Permisjons- og fraværstyper**.

2. Velg en permisjons- og fraværstype i listen. Velg permisjonsenheten i **Generelt**-delen i **Enhet**-feltet. Du kan velge **Timer** eller **Dager**.

3. Valgfritt: Hvis du valgte **Timer** i **Enhet**-feltet, kan du bruke feltet **Aktiver halvdagsdefinisjon** til å angi om ansatte kan velge den første halve dagen eller den andre dagen fri hvis de ber om en permisjon halv dag.

Ansatte som sender inn en ny permisjonsforespørsel, kan velge ulike permisjonstyper for å konstruere permisjonsforespørselen. Alle permisjonstyper som er valgt som del av én enkelt permisjonsforespørsel, bør imidlertid ha samme permisjonsenhet. Ansatte kan vise permisjonsenheten for hver permisjonstype i **Be om fridager**-skjemaet.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)
- [Opprette en arbeidstidskalender](hr-leave-and-absence-working-time-calendar.md)
- [Suspender permisjon](hr-leave-and-absence-suspend-leave.md)
- [Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
