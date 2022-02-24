---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (10. mars 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 10. mars 2020.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
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
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 944481727f3222a10f128ac3078c117f5ae7d193
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526926"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (10. mars 2020)?

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.2985. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Får ikke tilgang til rapport for kompetansegapanalyse (394460)

Denne rapporten støttes ikke i Dynamics 365 Human Resources. Menyelementet som skal brukes til å skrive ut SSRS-rapporten, fjernes.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Feil melding ved tilgang til siden Komme i gang (417950)

Med denne endringen skjuler sikkerhet dette menyelementet hvis du ikke har tilgang til skjemaet.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Strømlinjeformet oppgavevedlikehold for ansatte (380538)

Skjemaet for vedlikehold av arbeidsoppgave viser alle aktiviteter for en ansatt på tvers av jobbintroduksjon, jobbavslutning, overganger og forretningsprosesser. Du kan nå slette, tilordne på nytt eller oppdatere statusen for oppgaver.

Eksempel: Benjamin Martin er en fordelsadministrator. Under jobbintroduksjon av ansatte opprettes oppgaver for Benjamin for å se gjennom den nyansattes fordelsvalg. Benjamin har tidligere oppgaver som han er fullført, og fremtidige oppgaver han må fullføre. Benjamin bestemmer seg for å forlate firmaet, slik at aktivitetene må enten tilordnes på nytt eller fjernes. Skjemaet for oppgavevedlikehold (i handlingsruten i **Arbeider**-skjemaet) gjør at alle Benjamins oppgaver kan tilordnes på nytt til en annen arbeider eller fjernes.  

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
| Ny **Tittel**-enhet | <ul><li>**Tittel** lagt til</li></ul> Den nye **Tittel**-enheten er inkludert i Common Data Service, men refereres ikke til fra **Stilling**- eller **Jobb**-enhetene på dette tidspunktet. |

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

Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:

- **Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-33"></a>Plattform update 33

- Helside-apper (forhåndsvisning) - Denne forhåndsvisningsfunksjonen, som krever at du aktiverer funksjonen Lagrede visninger, gjør at Power Apps og tredjepartsapper kan legges til som helside-opplevelser via instrumentbordet.

- Lagrede visninger (forhåndsvisning) - Denne forhåndsvisningsfunksjonen aktiverer lagrede visninger, som er en betydelig forbedring av delsystemet for tilpassing. Med denne funksjonen kan brukere ha flere navngitte sett med tilpasninger per side. Du kan også publisere visninger til sikkerhetsroller.

- Optimalisert "er en av"-filtreringsopplevelse - Denne funksjonen aktiverer en optimalisert "er en av"-filtreringsopplevelse som gjør det enklere å angi flere filterverdier, har enklere mekanisme for å fjerne individuelle eller alle filterverdier, og har en mer kompakt og intuitiv visualisering av filterverdier.

- Anbefalte felt – Brukere må ofte legge til felt i et rutenett eller en side. Dette kan være vanskelig med så mange tilgjengelige felt. I stedet for å måtte søke gjennom en stor liste, gjør denne funksjonen det mulig for systemet å bruke et sett av anbefalte felt basert på hvilke andre brukere oftest legger til i lignende scenarioer.

- Trege standardhandlinger i rutenett – Denne funksjonen sikrer at standardhandlingen i et rutenett er koblet til en bestemt kolonne i et rutenett, uansett om kolonnen er flyttet eller skjult.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)