---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (12. februar 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 12. februar 2020.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ce265627bf5cef023770be3f8953e12d49866be
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686918"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (12. februar 2020)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.2867. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Eksisterende enheter CompFixedEmpls og HcmPersonImage skal være tilgjengelige fra OData (414178)

Med denne ukens utgivelse er enhetene **CompFixedEmpls** og **HcmPersonImage** nå offentlige og tilgjengelige via ODAta.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Sletting av ansettelse fra Dataverse fungerer ikke når ansettelsesdetaljer ikke er aktive (403193)

Denne endringen tillater nå sletting av ansettelse via Dataverse når det ikke finnes noen aktive ansattdetaljer.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Arbeidsflyten for kursregistrering endrer status til fullført og feil etter andre godkjenning (409749)

Arbeidsflyten for kursregistrering er oppdatert for å tillate flere godkjennere.

## <a name="in-preview"></a>I forhåndsvisning

Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:

- **Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-32"></a>Plattform update 32 

Platform Update 32 er snart tilgjengelig. [Finn ut mer om Platform Update 32 her](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

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