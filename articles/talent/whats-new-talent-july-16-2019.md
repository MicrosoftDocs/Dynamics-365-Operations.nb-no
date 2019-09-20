---
title: Hva er nytt eller endret i Dynamics 365 for Talent (16. juli 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ac0990a72224395cf109c7eb42cbb48ece2a0b4f
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795202"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-16-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (16. juli 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Endringer i Attract
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Kommer snart i Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Jobbgodkjenninger vises på startsiden

Godkjenninger vises i en **Godkjenning**-del på instrumentbordet. Godkjennere kan se gjennom godkjenningene sine under **Tilordnet til deg**, som viser jobb-ID, jobbtittel, andre godkjennere og datoen da jobben ble tilordnet. Brukere som sender inn en jobb til godkjenning, kan se gjennom jobbene under **Forespurt av deg**, som viser godkjennerne som fortsatt må godkjenne den sendte jobben.

## <a name="changes-in-onboard"></a>Endringer i Onboard
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service-enheter som nå støtter egendefinerte felt

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Kan ikke se målene og gjennomgangene i lederselvbetjening

Denne ukens endringer tillater nå visning og redigering av mål og gjennomganger for ledere på hopp over-nivåer i lederselvbetjening.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Målskjema kan ikke lukkes etter at en bruker har redigert et målfelt

Denne versjonen retter opp et problem der målskjemaet ikke lukkes når du velger **Lukk**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Opprette nye mål og lagre viser feil

Denne versjonen retter opp et problem ved lagring av mål i ansatt- og lederselvbetjening.

### <a name="unable-to-add-a-field-to-position-details"></a>Kan ikke legge til et felt i stillingsdetaljer 

I denne versjonen støttes nå egendefinerte felt i stillingsdetaljer.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Kan ikke definere utløpsdato for inntektskoden via databehandling

Med disse endringene kan du nå angi utløpsdatoer for inntektskoder i databehandling.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Nye egendefinerte felt synkroniseres ikke raskt nok

Ytelsen til synkronisering av egendefinerte felt til Common Data Service er forbedret med denne ukens versjon.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Enhetseksport til databasejobber mislyktes med feilmeldingen: "Formatet på initialiseringsstrengen samsvarer ikke med spesifikasjonen som starter ved indeks 0."

Denne versjonen retter opp problemet der satsvise jobber for databasen mislykkes. Slik oppdaterer du manuelt:

1. Gå til **Databehandling**.
2. Velg **Konfigurer enhetseksport til database**.
3. Angi tilkoblingsstrengen til måldatabasen på nytt, og velg **Lagre**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>Konfigurasjon av SMTP-e-post mislykkes plutselig med følgende feilmelding: "SMTP-serveren krever en sikker tilkobling, eller klienten ble ikke godkjent."

Denne versjonen retter opp en SMTP-e-postkonfigurasjon som mislykkes plutselig. Slik oppdaterer du manuelt:

1. Gå til **Systemadministrasjon**.
2. Velg **E-postparametere**.
3. Velg **SMTP-innstillinger**. 
4. Skriv inn brukernavnet og passordet som brukes for SMTP-serveren, på nytt, og velg **Lagre**.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Forhåndsvisningsfunksjoner blir bare aktivert i sandkasseforekomster

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er **Produksjon** eller **Sandkasse**. Forekomster av typen **Sandkasse** gjør at nye funksjoner kan testes tidlig. Alle eksisterende Talent-forekomster vil bli oppdatert til **Produksjon**-forekomsttypen. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen **Sandkasse**, kan du kontakte [kundestøtten](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrens permisjonstypene i fritidsforespørsler

Organisasjoner kan tilby mange forskjellige typer permisjon til ansatte. Det er imidlertid kanskje ikke aktuelt for ansatte å sende inn fritidsforespørsler for enkelte permisjonstyper. Disse permisjonstypene kan administreres av Personale i stedet. I denne versjonen kan du konfigurere hvilke permisjonstyper ansatte kan sende inn fritidsforespørsler for. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Vise prestasjonsinformasjon for direkte underordnede og deres underordnede i lederselvbetjening

Et nytt alternativ lar ledere vise prestasjonen til både direkte underordnede og deres underordnede. For øyeblikket kan linjeledere tilordne og oppdatere prestasjonsmål og utstede nye vurderinger. I tillegg kan linjeledere og deres ansatte vedlikeholde og oppdatere prestasjonsjournaler for å bidra til å sikre at prestasjonsvurderingsprosessen går knirkefritt. Når denne endringen er implementert, kan ledere vise og vedlikeholde prestasjonsrelatert informasjon for både direkte underordnede og deres underordnede.
