---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (19. mars 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f636dbd3b0ba59ea6cafbc431af46315210dded1
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555266"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (19. mars 2020)?

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3014. Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Grenser for Human Resources-miljø er nå basert på den oppdaterte lisensen (394595)

Grensen for antall miljøer per prosjekt i Lifecycle Services (LCS) er endret. Den forrige grensen var to miljøer. Grensen for antall produksjons- og sandkassemiljøer du kan opprette for Human Resources i LCS, er nå basert på oppdatert lisens. Du kan nå opprette så mange miljøer som nødvendig per LCS-prosjekt, avhengig av antall lisenser som er kjøpt. Den nye lisensieringen, som oppdateres 1. februar 2020, gjør det mulig for kundene å kjøpe flere miljøer. Hvis du vil ha mer informasjon om lisenskrav for flere miljøer, kan du se [lisensieringsveiledningen for Dynamics 365](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Gi kryssfirmavisning av kompensasjonsdata for ansatte og ledere (403904)

Aktiver denne funksjonen i arbeidsområdet **Funksjonsbehandling**. Hvis du vil ha mer informasjon, kan du se [Aktivere eller deaktivere forhåndsvisning av funksjoner](hr-admin-manage-features.md#enable-or-disable-preview-features).

Når du aktiverer denne funksjonen, kan ledere se kompensasjon for direkte og utvidede rapporter uten å måtte logge på ansettelsesfirmaet. Fullstendig kompensasjonslogg er tilgjengelig fra alle påloggede firmaer lederen har tilgang til. Hvis du vil ha mer informasjon, se [Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Aktiver funksjonalitet for fletting av global adressebok (427189)

Du kan nå flette like adressebokoppføringer ved å velge de like postene og velge **Flett** fra siden **Global adressebok**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Kan ikke justere permisjonssaldo for en plan uten avsetninger som ble opprettet med funksjonen Flere permisjonstyper på (419635)

Nå kan du justere saldoer for permisjonsplaner som ble opprettet med forhåndsvisningsfunksjonen **Flere permisjonstyper** aktivert i Funksjonsbehandling.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Hovedstilling-felt i WorkerPositionAssignmentEntity når en ansatt er sluttet (420774)

For ansatte med et avsluttet ansettelsesforhold, vises den primære stillingen som var aktiv ved avslutningen, i enheten. For integreringer vil det ikke lenger opprettes en duplikat post for den ansattes tilordning for arbeiderstilling. 

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

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer

Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:

1. Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen. Du kan vise denne informasjonen på **Bruker**-siden. Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData. Som standard finnes ikke e-postadressen i Excel-utformingen. Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere. Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.

3. Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.

4. Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-33"></a>Plattform update 33

- Helside-apper (forhåndsvisning) - Denne forhåndsvisningsfunksjonen, som krever at du aktiverer funksjonen Lagrede visninger, gjør at Power Apps og tredjepartsapper kan legges til som helside-opplevelser via instrumentbordet.

- Lagrede visninger (forhåndsvisning) - Denne forhåndsvisningsfunksjonen aktiverer lagrede visninger, som er en betydelig forbedring av delsystemet for tilpassing. Med denne funksjonen kan brukere ha flere navngitte sett med tilpasninger per side. Du kan også publisere visninger til sikkerhetsroller.

- Optimalisert "er en av"-filtreringsopplevelse - Denne funksjonen aktiverer en optimalisert "er en av"-filtreringsopplevelse som gjør det enklere å angi flere filterverdier, har enklere mekanisme for å fjerne individuelle eller alle filterverdier, og har en mer kompakt og intuitiv visualisering av filterverdier.

- Anbefalte felt – Brukere må ofte legge til felt i et rutenett eller en side. Dette kan være vanskelig med så mange tilgjengelige felt. I stedet for å måtte søke gjennom en stor liste, gjør denne funksjonen det mulig for systemet å bruke et sett av anbefalte felt basert på hvilke andre brukere oftest legger til i lignende scenarioer.

- Trege standardhandlinger i rutenett – Denne funksjonen sikrer at standardhandlingen i et rutenett er koblet til en bestemt kolonne i et rutenett, uansett om kolonnen er flyttet eller skjult.

## <a name="new-production-release-cadence"></a>Ny produksjonslanseringsfrekvens

Fra og med april vil lanseringsfrekvensen for Human Resources skifte fra en ukentlig oppdatering til en oppdatering annenhver uke. Dette gir sikker distribusjonspraksis og høye standarder for stabilitet og pålitelighet i tjenesten. Vi legger til flere tester og skjermer på plass for å bekrefte vellykket distribusjon på hvert trinn i prosessen. Hvis du vil ha mer informasjon om lanseringsfrekvens, kan du se [Oppdateringsprosess](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>I forhåndsvisning

Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:

- **Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)