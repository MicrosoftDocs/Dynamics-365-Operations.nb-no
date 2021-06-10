---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (13. april 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 13. april 2020.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a43b55c075102056ed7c752b72a85f2c9012d46
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051047"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (13. april 2020)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3136. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="new-production-release-cadence"></a>Ny produksjonslanseringsfrekvens

Med denne ukens lansering vil lanseringsfrekvensen for Human Resources skifte fra en ukentlig oppdatering til en oppdatering annenhver uke. For å sikre innretting etter sikre distribusjonspraksiser og opprettholde høye standarder for stabilitet og pålitelighet i tjenesten, vil prosessen med å distribuere serviceoppdateringer til alle områder er nå en to-ukes distribusjon. Flere tester og skjermer er på plass for å bekrefte vellykket distribusjon på hvert trinn i prosessen. Hvis du vil ha mer informasjon om lanseringsfrekvensen, kan du se [Oppdateringsprosess](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Avrundingspresisjonsfelt kan ikke redigeres når en avrundingstype er angitt (435616)

Med denne endringen er feltet **Avrundingspresisjon** nå tilgjengelig etter at du har oppdatert feltet **Avrundingstype**.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Kan ikke redigere sluttdatoen for permisjonsregistrering når permisjonsplanen ikke har avsetningsperioder (413628)

Du kan nå redigere sluttdatoen for registrering uten å få feil meldingen "Feltet Datogrunnlag for avsetning må være fylt ut".

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>Ansettelsesenhet synkroniseres ikke til Dataverse (430834)

Denne endringen løser et problem der ansettelsesdataene ikke ble synkronisert til Dataverse etter å ha lagt til finansdimensjoner. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Fjern flere overordnede for enheten Tidsintervall for arbeidskalender (431775)

Denne endringen fjerner flere overordnede for enheten **Tidsintervall for arbeidskalender**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filter med CAST-funksjon fungerer ikke på OData-kall til enheten Stillingstilordning (431699)

Denne oppdateringen inneholder en endring for å tillate filter med CAST-funksjonen i OData for enheten **Stillingstilordning**.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="leave-suspension"></a>Avbryt permisjon

Du kan avbryte permisjon og fravær i Human Resources for en ansatt. Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper. Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo. Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Overføringsregler

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Kjente problemer

## <a name="employment-details-entity"></a>Enheten Ansettelsesdetaljer

Enheten **Ansettelsesdetalj** er oppdatert med følgende felt:

- **Lønnsfrekvens**
- **ID for ansettelseskategori**
- **Ansettelsestype**
- **ID for ansettelsestype**
- **Ansettelsesstatus for fordel**

Oppsettsdataene for disse feltene er avhengig av fordelsadministrasjonen som aktiveres i arbeidsområdet **Funksjonsbehandling**. Ikke fyll ut eller oppdater disse feltene i enheten **Ansettlesesdetalj** fordi dette vil føre til feil under importen.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer

Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:

1. Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen. Du kan vise denne informasjonen på **Bruker**-siden. Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData. Som standard finnes ikke e-postadressen i Excel-utformingen. Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere. Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.

3. Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.

4. Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]