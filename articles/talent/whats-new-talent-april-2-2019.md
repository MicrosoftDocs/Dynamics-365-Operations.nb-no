---
title: Hva er nytt eller endret i Dynamics 365 Talent (2. april 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
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
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68dc73b7316a3ceb7129c9ea46bc60669ed2be95
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896940"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (2. april 2019)?

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="approval-emails-in-attract"></a>Godkjenningse-post i Attract
Nye godkjenningse-postmeldinger forbedrer innsikten i godkjenningsprosessen. E-postmeldinger sendes til godkjennere når en av følgende situasjoner oppstår:

- En anmoder sender en jobb til godkjenning.
- En jobb blir avvist eller godkjent.
- En godkjenner har ikke behandlet en godkjenningsforespørsel innen 24 timer.

Du kan tilpasse innholdet i e-postmeldinger for godkjenning med nye maler.

### <a name="application-and-profile-attachments"></a>Søknads- og profilvedlegg
Forbedringer i **Dokumenter**-kategorien i søknads- og talentsamlingsprofiler viser nå både dokumentnavnet og -typen.

## <a name="changes-in-onboard"></a>Endringer i Onboard
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="coming-soon-attract-and-onboard"></a>Kommer snart (Attract og Onboard)

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services-integrasjon (LCS) med "rapporter et problem"
Problemer som er logget av sluttbrukere via rapporter-et-problem-funksjonen i Attract og Onboard, oppretter nå automatisk kundestøtteproblemer i kundens LCS-prosjekt. Administratorer kan deretter sortere problemene og sende dem til Microsoft når det er nødvendig. Dette er konsekvent med hvordan Core HR behandler kundestøtteproblemer for sluttbrukeren.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2216.

### <a name="platform-update-25-for-finance-and-operations"></a>Platform update 25 for Finance and Operations
Hvis du vil ha mer informasjon om Platform update 25 for Finance and Operations, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 for Finance and Operations Platform Update 25 (april 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avansert kompensasjonssikkerhet (fast og variabel)
I mange organisasjoner kan kompensasjons- og fordelsansvarlige bare ha tilgang til bestemte kompensasjonsposter. Disse kan inkludere poster for ledere eller regionale ansatte. Med denne endringen kan HR administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen. Du kan tilordne sikkerhetsroller til faste og variable planer. Disse sikkerhetsrollene bestemmer tilgang til planer og tilknyttede ansattdata, for eksempel lønns- eller bonusposter, slik at bare disse rollene kan behandle kompensasjon for ansattgruppene.

### <a name="upgrade-to-common-data-service"></a>Oppgradere til Common Data Service
Tidsfrister for å oppgradere til Common Data Service nærmer deg raskt. Logg på Microsoft Power Apps-administrasjonssenteret for å bestemme om databasen må oppgraderes. Hvis du vil ha mer informasjon om tidsfrister og de nødvendige trinnene for å oppgradere, kan du se [Oppgradere til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>I forhåndsvisning

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Tillate angivelse av årsakskoder for permisjonstyper
Organisasjoner må kanskje ha tilleggsinformasjon om fraværsforespørsler. Du kan nå angi årsakskoder for fraværstyper og gi de ansatte mulighet til å velge en årsakskode i fraværsforespørsler.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Kreve årsakskoder for bestemte fraværstyper i forespørsler om fravær
Organisasjoner kan kreve årsakskoder for bestemte fraværstyper når ansatte sender fraværsforespørsler. Dette kan være på grunn av firmapolicy eller lovbestemte krav. Du kan nå angi hvilke permisjonstyper som krever en årsakskode, og du kan kreve at ansatte må angi en årsakskode for fraværstypen i forespørsler om fravær.

## <a name="coming-soon"></a>Kommer snart

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Forbedringer av brukergrensesnittet for kontroll av dupliserte ansatte
Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange duplikater som ble funnet. Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet. For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.

###  <a name="email-support-for-alerts"></a>E-poststøtte for varsler
Med platform update 25 for Finance and Operations kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse. 
