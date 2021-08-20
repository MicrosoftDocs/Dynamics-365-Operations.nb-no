---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (18. februar 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 18. februar 2020.
author: andreabichsel
ms.date: 02/18/2020
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f74692ffe8afbdeea7519ac8bdfbbe54105b9ccee83031a9b1c223be78fc12e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770414"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (18. februar 2020)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.2903. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="platform-update-32"></a>Plattform update 32 

Platform Update 32 er nå tilgjengelig. Hvis du vil ha mer informasjon, se [Hva er nytt eller endret i Platform Update 32 for Finance and Operations (februar 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Søkeverdier huskes ved endring av visningsalternativer i strømlinjeformet ansatt-skjemaet (383833)

Det nye **Arbeider**-skjemaet husker nå søkeverdier når du endrer visningsalternativene og bruker endringer.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Sammendragsfliser for kompensasjonsstyring i forhåndsvisningsfunksjonen omadresser til feil format (401861)

Faste og variable kompensasjonsstyringsfliser viser nå de riktige postene i det nye **Arbeider**-skjemaet. Gjelder bare den forhåndsvisningsfunksjonen for strømlinjeformede ansatte. Du kan aktivere denne forhåndsvisningsfunksjonen **Funksjonsbehandling**. Hvis du vil ha mer informasjon, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Tomt Status-felt for enkelte oen permisjonsforespørselsposter i Dataverse (414915)

Denne endringen løser et problem i Dataverse når **Status**-feltet i en permisjonsforespørsel er angitt til **Gjennomgang**. Dataverse gjenspeiler nå statusen.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Kompetansegapanalyse er bare mulig for tilordnet jobb (411390)

Du kan nå foreta en kompetansegapanalyse på en hvilken som helst jobb som er definert i Human Resources.

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>Systemvaluta synkroniseres ikke fra Dataverse til Human Resources i nye miljøer (418011)

Systemvalutaen i Dataverse kan nå synkroniseres til Human Resources.

## <a name="in-preview"></a>I forhåndsvisning

- [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Forhåndsvisningsfunksjoner for ordelsbehandling](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Kommer snart

### <a name="updated-dataverse-solution"></a>Oppdatert Dataverse-løsning

En ny Dataverse-løsning vil snart være tilgjengelig med følgende endringer:

| Beskrivelse | Vekslepenger |
| ----------------------------------------- | --- |
| Endringer i enheten **Jobb/stilling** | **Kompensasjonsområde** lagt til</br>**Finansdimensjoner** lagt til |
| Endringer i **Arbeider**-enheten | **Navnerekkefølge** lagt til</br>**Arbeider hjemmefra** lagt til</br>**Språk** lagt til</br>**Ansiennitetsdato** lagt til</br>**Jubileumsdato** lagt til</br>**Opprinnelig ansettelsesdato** lagt til |
| Endringer i **Ansettelse**-enheten | **Finansdimensjoner** lagt til</br>**Avslutningsårsak** lagt til</br>**Avslutningsdato** endret navn fra **Overgangsdato**</br>**Prøvedato** lagt til |
| Endringer i **Arbeideradresse**-enheten | **Gateadresse** lagt til</br>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving |
| Nye enheter for oppsett av variabel kompensasjon | **Type variabel kompensasjonsplan**</br>**Variabel plan for kompensasjon**</br>**Overdragelsesregler**</br>**Nivå for variabel kompensasjonsplan** |
| Ny enhet, **Ansettelse i arbeiderkalender** | **Arbeidskalenderenhet** lagt til |
| Ny enhet, **Lønnstillingsdetaljer** | **Lønnsstillingsdetaljer** lagt til |
| Ny **Tittel**-enhet | **Tittel** lagt til. Den nye **Tittel**-enheten blir tatt med i synkroniseringsprosessen mellom Human Resources og Dataverse. Det blir i utgangspunktet ikke referert fra enhetene **Stilling** eller **Jobb**. |

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Personale?](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]