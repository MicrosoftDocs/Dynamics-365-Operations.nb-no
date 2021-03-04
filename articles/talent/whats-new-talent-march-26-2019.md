---
title: Hva er nytt eller endret i Dynamics 365 Talent (26. mars 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 17eae6c2aa2a1305b1d6f403c595c022f71da48f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529096"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (26. mars 2019)?

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="enhancements-to-interview-scheduling"></a>Forbedringer i intervjuplanlegging
Følgende forbedringer er tilgjengelige i planlegging av intervjuet.

- Ansettelsesansvarlig eller rekruttereren for jobben kan nå manuelt utløse en påminnelse til intervjueren for å gi tilbakemelding. Den tilknyttede e-postmalen for påminnelsen kan også konfigureres.
- Når intervjusammendraget deles med kandidaten, kan planleggeren av intervjuet velge å skjule navnene på intervjuerne og skjule rader fra sammendragsvisningen for intervjuet.

## <a name="changes-in-onboard"></a>Endringer i Onboard

### <a name="embedded-images-in-activities"></a>Innebygde bilder i aktiviteter
Nå kan du bygge inn bilder direkte i aktiviteter. I tillegg til å kunne kopiere og lime inn bilder fra weben, kan du laste opp bilder fra det lokale filsystemet. Størrelsen på aktiviteten er begrenset til 1 MB. Hvis bildet er for stort, endre størrelse, og prøv å laste opp på nytt.

[![Tildeling](./media/embedimages.png)](./media/embedimages.png)

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
**Build 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Støtte for egendefinert felt er tilgjengelig for utvalgte enheter i Common Data Service 

Følgende Common Data Service-enheter støtter nå kundefelt som er opprettet i Talent:

- Arbeider
- Etnisk opprinnelse
- Veteranstatus
- Språkkode
- Stilling
- Jobbtype
- Jobbfunksjon
- Posisjon
- Stillingstype
 
### <a name="employment-history-not-displayed-chronologically"></a>Ansettelseshistorikken vises ikke kronologisk
Med denne endringen viser nå ansettelsesloggsiden ansettelsesposter kronologisk, uavhengig av firma. Du kan også bruke sorteringsalternativer for å sortere etter firma.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Fast kompensasjon-planer vises ikke når brukeren begrenses etter firma i sikkerhet.
I denne utgivelsen vises nå fast kompensasjon-planer når brukere begrenses etter firma i sikkerhet. Alle sikkerhetsinnstillinger vil tre i kraft, og faste planer vil vises for firmaene som brukeren har tilgang til. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Kan ikke slette jobbposter ved hjelp av Åpne i Excel-alternativet i Talent
Med denne versjonen kan du nå fjerne jobbposter ved hjelp av **Åpen i Excel**-alternativet i Talent.

### <a name="upgrade-to-common-data-service"></a>Oppgradere til Common Data Service
Tidsfrister for å oppgradere til Common Data Service nærmer deg raskt. Logg på Power Apps-administrasjonssenteret for å bestemme om databasen må oppgraderes. Hvis du vil ha mer informasjon om tidsfrister og de nødvendige trinnene for å oppgradere, kan du se [Oppgradere til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>I forhåndsvisning

Hvis du vil ha informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, se [Tilgang til forhåndsvisningsfunksjoner i Microsoft Dynamics 365 Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tillate angivelse av årsakskoder for permisjonstyper
Organisasjoner må kanskje ha tilleggsinformasjon relatert til fraværsforespørsler. For å få denne informasjonen må ansatte inkludere en årsakskode i fraværsforespørslene. I denne versjonen kan du nå angi årsakskoden som er forbundet med en gitt permisjonstype, og gi de ansatte mulighet til å velge en årsakskode i fraværsforespørsler.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Konfigurere at årsakskoder er nødvendige ved sending av fraværsforespørsler for bestemte fraværstyper
Organisasjoner kan kreve at årsakskoder skal angis for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kan være nødvendig basert på forskriftsmessige krav i landet/området eller en firmapolicy. I denne versjonen er det mulighet for HR å angi hvilke fraværstyper som skal kreve en årsakskode. Dette trer i kraft når ansatte sender fraværsforespørsler der fraværet krever en årsakskode.

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avansert kompensasjonssikkerhet (fast og variabel)
I mange organisasjoner kan kompensasjons- og fordelsansvarlige bare ha tilgang til bestemte kompensasjonsposter. Disse kan være for ledere eller regionale ansatte. Med denne endringen kan HR administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen. Faste og variable planer kan tilordnes til sikkerhetsroller, som bestemmer tilgangen til planene og ansattdataene som er knyttet til dem, for eksempel lønns- eller bonusposter. Bare rollene som er gitt tilgang, kan behandle kompensasjon for disse ansatte.

###  <a name="email-support-for-alerts"></a>E-poststøtte for varsler
Med Platform update 25 for Finance and Operations kan brukere opprette varslingsregler som automatisk fordeler e-postmeldinger til kontakter når de utløses av en hendelse. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Kontroll av dupliserte ansatte: Endringer i brukergrensesnittet
Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange duplikater som ble funnet. Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet. For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.


[!INCLUDE[footer-include](../includes/footer-banner.md)]