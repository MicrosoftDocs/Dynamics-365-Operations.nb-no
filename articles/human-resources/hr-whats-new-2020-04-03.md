---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (3. april 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 3. april 2020.
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 03fe38c8e2a8de6957cdc1adf5e89d7d0421d997
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712501"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (3. april 2020)?

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3111. Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funksjoner som er generelt tilgjengelige i uken rundt 6. april

- **Permisjons- og fraværsfunksjoner** – For mer informasjon, se [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md).

- **Funksjoner for fordelsbehandling** – For mer informasjon, se [Oversikt over fordelsbehandling](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Grenser for Human Resources-miljø er nå basert på den oppdaterte lisensen (394595)

Grensen for antall miljøer per prosjekt i LCS er endret. Den forrige grensen var to miljøer. Grensen for antall produksjons- og sandkassemiljøer du kan opprette for Human Resources i LCS, er nå basert på oppdatert lisens. Du kan nå opprette så mange miljøer som nødvendig per LCS-prosjekt, avhengig av antall lisenser som er kjøpt. Den nye lisensieringen, som oppdateres 1. februar 2020, gjør det mulig for kundene å kjøpe flere miljøer. Hvis du vil ha mer informasjon om lisenskrav for flere miljøer, kan du se [lisensieringsveiledningen for Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Feil under forsøk på å slette et spørreskjema (428603)

Oppdateringen for denne uken retter et problem der følgende feil vises under forsøk på å slette et spørreskjema:

Et ubalansert par av typen X++ TTSBEGIN/TTSCOMMIT er oppdaget.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Sikkerhets problem i ytelsesjournal og med profesjonelle sertifikater (428499)

Denne endringen begrenser synligheten for både ytelsesjournaler og profesjonelle sertifikater basert på firmaene de har tilgang til. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Forkortelsen for Quebec og Manitoba (387510)

Oppstartsdata er oppdatert for å gjenspeile riktig forkortelse for Manitoba og Quebec.

## <a name="new-entities-available-in-data-management-framework"></a>Nye enheter er tilgjengelige i Data Management Framework

Følgende enheter er nå tilgjengelige. Hvis du ikke ser disse enhetene oppført i enhetslisten, bruker du alternativet **Oppdater enheter** i **Rammeverkparametere > Enhetsinnstillinger > Oppdater enhetsliste**.

 - Banktransaksjon for permisjon og fravær V2
 - Permisjons- og fraværsregistrering V2
 - Lag i permisjons- og fraværsplan V2
 - Permisjons- og fraværsplan V2

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service-løsningen er nå tilgjengelig med følgende endringer:

| beskrivelse | Vekslepenger |
| --- | --- |
| Endringer i enheten **Jobb/stilling** | <ul><li>**Kompensasjonsområde** lagt til</li>|
| **Stillingsdimensjon**-enhet er lagt til | <ul><li>**Finansdimensjoner** lagt til</li>
| Endringer i **Arbeider**-enheten | <ul><li>**Navnerekkefølge** lagt til</li><li>**Arbeider hjemmefra** lagt til</li><li>**Språk** lagt til</li><li>**Ansiennitetsdato** lagt til</li><li>**Jubileumsdato** lagt til</li><li>**Opprinnelig ansettelsesdato** lagt til</li></ul> |
| Endringer i **Ansettelse**-enheten | <ul><li>**Finansdimensjoner** lagt til</li><li>**Avslutningsårsak** lagt til</li><li>**Avslutningsdato** endret navn fra **Overgangsdato**</li><li>**Prøvedato** lagt til</li></ul> |
| Endringer i **Arbeideradresse**-enheten | <ul><li>**Gateadresse** lagt til</li><li>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving</li></ul> |
| Nye enheter for oppsett av variabel kompensasjon | <ul><li>**Type variabel kompensasjonsplan**</li><li>**Variabel plan for kompensasjon**</li><li>**Overdragelsesregler**</li><li>**Nivå for variabel kompensasjonsplan**</li></ul> |
| Ny enhet, **Ansettelse i arbeiderkalender** | <ul><li>**Arbeidskalenderenhet** lagt til</li></ul> |
| Ny enhet, **Lønnstillingsdetaljer** | <ul><li>**Lønnsstillingsdetaljer** lagt til</li></ul> |
| Ny **Tittel**-enhet | <ul><li>**Tittel** lagt til</li></ul>Den nye **Tittel**-enheten er inkludert i Common Data Service, men refereres ikke til fra **Stilling**- eller **Jobb**-enhetene på dette tidspunktet. |

> [!NOTE]
> Finansdimensjoner for både stillinger og ansettelse tilbyr en-veis integrering for oppdateringer fra Human Resources til Common Data Service. Finansdimensjon-oppdateringer synkroniseres for øyeblikket ikke fra Common Data Service til Human Resources.

De neste ukene vil disse enhetsendringene være tilgjengelige i alle miljøer. Slik installerer du den nyeste Common Data Service-løsningen for Human Resources manuelt:

1.  Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com).

2.  Velg **Miljøer**.

3.  Finn miljøet du vil oppgradere. Miljøet må samsvare med **miljønavn** i **Common Data Service**-informasjonsdelen i **Om**-skjemaet i Human Resources.

4.  Velg miljøet for å vise miljødetaljer.

5.  Velg **Administrer løsninger** på handlingslinjen øverst. Et nytt leservindu åpner og navigerer til **Administrasjonssenter for Dynamics 365** i konteksten til miljøet ditt.

6.  I **Løsning**-listen velger du **Dynamics 365 Human Resources Anker**.

7.  Velg **Oppgrader** hvis du vil bruke den nyeste løsningen.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="leave-suspension"></a>Avbryt permisjon

Du kan avbryte permisjon og fravær i Human Resources for en ansatt. Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper. Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo. Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Overføringsregler

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Kommer snart

## <a name="new-production-release-cadence"></a>Ny produksjonslanseringsfrekvens

Fra og med april vil lanseringsfrekvensen for Human Resources skifte fra en ukentlig oppdatering til en oppdatering annenhver uke. For å sikre innretting etter sikre distribusjonspraksiser og opprettholde høye standarder for stabilitet og pålitelighet i tjenesten, vil prosessen med å distribuere serviceoppdateringer til alle områder bli en to-ukes distribusjon. Flere tester og skjermer vil være på plass for å bekrefte vellykket distribusjon på hvert trinn i prosessen. Hvis du vil ha mer informasjon om lanseringsfrekvensen, kan du se [Oppdateringsprosess](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Kjente problemer

## <a name="employment-detail-entity"></a>Enheten Ansettelsesdetalj

Enheten **Ansettelsesdetalj** er oppdatert med følgende felt: **Lønnsfrekvens**, **ID for ansettelseskategori**, **Ansettelsestyper**, **ID for ansettelsestype** og **Ansettelsesstatus for fordel**. Oppsettsdataene for disse feltene er avhengig av fordelsadministrasjonen som aktiveres i Funksjonsbehandling. Disse feltene bør ikke fylles ut eller oppdateres enheten **Ansettlesesdetalj** fordi det vil føre til feil under importen.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer

Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:

1. Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen. Du kan vise denne informasjonen på **Bruker**-siden. Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData. Som standard finnes ikke e-postadressen i Excel-utformingen. Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere. Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.

3. Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.

4. Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)