---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (6. desember 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-12-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e46000414436b5a2fa211428dcd10131b9d588c1
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897701"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-6-2018"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (6. desember 2018)

**Build 8.1.2071**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.


## <a name="platform-update-22-for-finance-and-operations"></a>Platform update 22 for Finance and Operations

### <a name="export-up-to-1-million-rows-to-excel"></a>Eksportere opptil 1 million rader til Excel

Funksjonen Eksporter til Excel kan nå konfigureres slik at brukerne kan eksportere opptil 1 million rader fra et rutenett i Talent, en vesentlig økning fra den forrige grensen på 10 000 rader. 

### <a name="restyled-personalization-toolbar"></a>Ny utforming på verktøylinjen for tilpassing

Verktøylinjen for tilpassing har fått ny utforming i Platform update 22 for Finance and Operations slik at brukerne lettere kan tilpasse sine egne opplevelser i Talent. Følgende endringer ble gjort: 

-  Navnet på hvert tilpassingsverktøy vises nå sammen med et ikon, som hjelper brukere med å raskt gjenkjenne verktøyet de ønsker å bruke.
-  Beskrivelsen av hvordan gjeldende verktøy brukes, vises også nå, som hjelper brukerne med å forstå hvordan de gjør de nødvendige tilpasningene.  
-  Hele verktøylinjen for tilpassing kan flyttes på skjermen ved å dra og slippe på et bestemt område helt til venstre på verktøylinjen. Dette gjør det mulig for brukere å tilpasse elementer som tidligere ble skjult av verktøylinjen.   

### <a name="optimized-is-one-of-filtering-experience"></a>Optimalisert opplevelse for "er en av"-filtrering

Filtreringsoperatoren "er en av" er tilgjengelig for de fleste feltene når du bruker filtreringsruten og rullegardinlistene i rutenetthodet. Med denne operatoren kan en bruker filtrere et felt basert på flere verdier. En ny og forbedret opplevelse for operatoren "er en av" er tilgjengelig i Platform update 22 for Finance and Operations. Hvis du vil vite mer, kan du se [Optimalisert "er en av"-filtreringopplevelsen](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering).

### <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>Lime inn lister fra Excel i filterfelter med operatoren "er en av"

For enkelte oppgaver kan det hende at brukere har en liste med verdier i Excel som de vil bruke til å filtrere data i Talent En personaladministrasjonsbruker kan for eksempel ha funnet en gruppe ansatte fra en rapport som må undersøkes nærmere i systemet, og det vil være ideelt for denne brukeren å kunne kopiere listen direkte fra Excel til et filterfelt i Talent.

Fra og med Platform update 22 for Finance and Operations gjenkjenner operatoren "er en av" i filtreringsruten og rutenettkolonnefiltreringen nå lister som er kopiert fra Excel, slik at de kan limes direkte inn i et filterfelt. Dette inkluderer en samling med verdier som er kopiert fra ulike rader og kolonner i Excel. Hvis du vil vite mer om denne funksjonen, kan du se [Lime inn lister fra Excel i filterfelter med operatoren "er en av"](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel).

## <a name="in-preview"></a>I forhåndsvisning

### <a name="configure-uk-payroll-integration-between-talent-and-dayforce"></a>Konfigurere lønnsintegrering for Storbritannia mellom Talent og Dayforce

Integrasjonen mellom Talent og Ceridian Dayforce er tilgjengelig i forhåndsvisning for Storbritannia. Se følgende emner hvis du vil ha mer informasjon, [Konfigurere lønnsintegrering mellom Talent og Dayforce](https://docs.microsoft.com/dynamics365/unified-operations/talent/configure-payroll-integration).

## <a name="coming-soon"></a>Kommer snart

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Permisjon og fravær: Saldoer for fremtidig permisjon og permisjonsprognoser

Med endringene som gjøres for å la ansatte planlegge avspasering og be om fremtidige fraværsforespørsler uten å påvirke gjeldende avspaseringssaldoer, endres også måten avspaseringssaldoer vises på. 

Tilgjengelig saldo som vises nå, er hvor mye avspasering som er tilgjengelig for forespørsler, inkludert avsetninger til og med i dag og alle godkjente permisjonsforespørsler til sluttidspunktet. 

Når muligheten for prognostisering gis ut, endres den viste saldoen til gjeldende avspaseringssaldo, inkludert avsetninger til og med i dag og forespørsler til og med i dag. Ansatte og ledere vil se disse oppdaterte saldoene i ansatt- og lederselvbetjening på **Fridager**-kortet og i vinduet for **avspaseringssaldoer**. Personalledere vil se disse oppdaterte saldoene i **Personer**-arbeidsområdet og i vinduet **Tilordnede permisjonsplaner** for ansatte.

## <a name="other-changes"></a>Andre endringer 

### <a name="termination-code-is-not-populated-to-the-worker-position-assignment-record"></a>Opphørskode fylles ikke ut i tilordningsposten for arbeiderstilling

En endring er implementert som fyller ut årsakskoden i tilordningsposten for stilling under oppsigelsesprosessen.

### <a name="validation-for-personnel-number-being-in-use-needs-additional-details"></a>Validering for personalnummer som brukes, trenger flere detaljer

Tilleggsinformasjon vises når nummerserier er i bruk, for å kunne forstå bedre problemer når et nytt nummer ikke kan genereres.
 
### <a name="attachments-buttons-not-available-for-workers"></a>Vedlegg-knapper er ikke tilgjengelige for arbeidere

Endringer er gjort for å rette vedlegg. Når du legger til en nytt vedlegg til en arbeider, er nå **Ny**- og **Rediger**-knappene tilgjengelige når faktabokser er åpne i arbeidervinduet. 

## <a name="known-issues"></a>Kjente problemer

### <a name="mapping-errors-in-the-integration-with-finance"></a>Tilordningsfeil i integrasjonen med Finance

Følgende problemer er identifisert i gjeldende mal for integrering av Talent med Finance. En ny mal blir snart publisert og skal brukes på alle nye integrasjonsprosjekter som opprettes. For eksisterende integrasjonsprosjekter kan oppgavetilordningene oppdateres. Se følgende tabell for oppdaterte tilordninger. 

>[!NOTE]
> Den overordnede jobbtilordningsoppgaven for jobbstillinger til stillinger kan ikke integrere data. Dette er et problem som undersøkes nå. Det finnes ingen løsning i gjeldende tilordning. 

Avdelinger til driftsenhet-oppgaven må ha følgende tilordninger oppdatert.

| Eksisterende kildefelt          | Nytt kildefelt |
| -------------------------------|------------------|
| cdm_description (beskrivelse)  | cdm_name (navn)  |

En ekstra tilordning må også legges til. Velg det siste **Ingen**-feltet for å legge til følgende tilordning.

| Kildefelt                   | Målfelt    |
| -------------------------------|----------------------|
| cdm_description (beskrivelse)  | NAMEALIAS (NAMEALIAS)|

De oppdaterte tilordningene skal se slik ut.

![Avdelinger til driftsenhet-oppgaven](./media/DepartmentMapping.png)


Jobber til jobbdetaljer-oppgaven må ha følgende tilordninger oppdatert.

| Eksisterende kildefelt          | Nytt kildefelt                   |
| -------------------------------|------------------------------------|
| cdm_name (navn)                | cdm_description (beskrivelse)      |
| cdm_name (beskrivelse)         | cdm_jobdescription(jobbeskrivelse)|


De oppdaterte tilordningene skal se slik ut.

![Jobber til jobbdetaljer-oppgaven](./media/JobMapping.png)

Arbeidere til arbeid-oppgaven må ha følgende tilordninger oppdatert.

| Eksisterende kildefelt                 | Nytt kildefelt                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-postadresse 1)   | cdm_primaryemailaddress (primær e-postadresse) |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (hovedtelefon)       |

Endringen av Kjønn-feltet må også oppdateres. Velg tilordningstypen **fn** (funksjon) for kjønn og oppdater følgende verditilordninger.

| Common Data Service-verdi   | Finance and Operations-verdi | | ------------|------------------ -----------| | 75440000    | Mann                         | | 75440001    | Kvinne                       | | 75440002    | Ingen                         | | 75440003    | Ikke-spesifikk                  |

De oppdaterte tilordningene skal se slik ut.

![Arbeidere til arbeider-oppgaven](./media/WorkerMapping.png)

![Endring av Kjønn-feltet](./media/WorkerTransform.png)

