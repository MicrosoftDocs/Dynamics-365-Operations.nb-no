---
title: Hva er nytt eller endret i Dynamics 365 Talent (21. januar 2020)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528128"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Hva er nytt eller endret i Dynamics 365 Talent (21. januar 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract. Vi har lagt til funksjonalitet i Attract for å støtte den nyeste kunngjøringen vår, [Sette sammen en mer vellykket arbeidsstyrke med Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Laste ned miljødata

Administratorer kan laste ned miljødataene. Dataene eksporteres i standard JSON-format med alle jobber, kandidater og konfigurasjon eksportert i en zip-fil. Hvis du vil ha mer informasjon, kan du se [Eksportere data fra Attract og Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Begrense tilgang til miljøer for brukere som ikke er administratorer

Administratorer kan nå begrense tilgang til miljøet for brukere som ikke er administratorer. Du kan ikke angre denne handlingen. Hvis du vil ha mer informasjon, kan du se [Begrense tilgang til Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Eksportere jobbintroduksjonsveiledninger

Brukere kan nå eksportere alle jobbintroduksjonsveiledninger og jobbintroduksjonsmaler i Word-dokumentformat. Hvis du vil ha mer informasjon, kan du se [Eksportere data fra Attract og Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2726. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Feltet Nyeste årlige kompensasjon i skjemaet Bekreft ansettelse er ikke konsekvent (392092)

Denne versjonen inneholder en endring som konsekvent viser den siste valutaen, basert på firmavelgeren i skjemaet **Bekreft ansattelse**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Kjent som-felt lagt til i oppslag for mottaker av tilbakemeldingen (407789)

Under tilbakemelding om ytelse gav ikke oppslaget for arbeidere nok informasjon til å finne ut om tilbakemeldinger kommer til riktig person. Vi la til en **Kjent som**-kolonne for å hjelpe til med å identifisere det unike navnet på den ansatte.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo-posten opprettes uten tilknytning til en arbeider (394526)

Denne versjonen inneholder en endring, slik at HCMWorkerPayrollInfo-poster ikke skrives uten referanse til en ansatt.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Kan ikke redigere avdeling ved navigering fra stillingshierarki (341001)

Når sikkerhet er konfigurert for å nekte tilgang til redigeringsavdelinger, deaktiveres redigering når du navigerer til **Avdelinger**-skjemaet i alle scenarioer.

## <a name="coming-soon"></a>Kommer snart

En ny Common Data Service-løsning vil snart være tilgjengelig med følgende endringer:

| Beskrivelse | Vekslepenger |
| --- | --- |
| Endringer i enheten **Jobb/stilling** | <ul><li>**Kompensasjonsområde** lagt til</li><li>**Finansdimensjoner** lagt til</li></ul> |
| Endringer i **Arbeider**-enheten | <ul><li>**Navnerekkefølge** lagt til</li><li>**Arbeider hjemmefra** lagt til</li><li>**Språk** lagt til</li><li>**Ansiennitetsdato** lagt til</li><li>**Jubileumsdato** lagt til</li><li>**Opprinnelig ansettelsesdato** lagt til</li></ul> |
| Endringer i **Ansettelse**-enheten | <ul><li>**Finansdimensjoner** lagt til</li><li>**Avslutningsårsak** lagt til</li><li>**Avslutningsdato** endret navn fra **Overgangsdato**</li><li>**Prøvedato** lagt til</li></ul> |
| Endringer i **Arbeideradresse**-enheten | <ul><li>**Gateadresse** lagt til</li><li>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving</li></ul> |
| Nye enheter for oppsett av variabel kompensasjon | <ul><li>**Type variabel kompensasjonsplan**</li><li>**Variabel plan for kompensasjon**</li><li>**Overdragelsesregler**</li><li>**Nivå for variabel kompensasjonsplan**</li></ul> |
| Ny enhet, **Ansettelse i arbeiderkalender** | <ul><li>**Arbeidskalenderenhet** lagt til</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]