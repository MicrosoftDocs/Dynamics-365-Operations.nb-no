---
title: Integreringsparametere for Project Service Automation
description: Dette emnet forklarer hvordan du konfigurerer måten standarddata registreres på når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58d2de323395db97d1f8ea146da55bba4e0f9c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838997"
---
# <a name="project-service-automation-integration-parameters"></a>Parametere for integrering av Project Service Automation

[!include[banner](../includes/banner.md)]

På siden **Parametere for integrering av Project Service Automation** kan konfigurere hvordan standarddata registreres når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 for Finance and Operations. For at prosjekter skal synkroniseres fra Project Service Automation to Finance and Operations, må feltene nedenfor konfigureres.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.
> - Integrasjon av faktiske data er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere.
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefalte vi at du også installerer KB 4131710.

| Kategori                    | Felt                | beskrivelse |
|------------------------|----------------------|-------------|
| Generelt                | Standard prosjekttype | Velg standard prosjekttype. Når prosjekter synkroniseres fra Project Service Automation, brukes denne verdien hvis du ikke har angitt en standardverdi i integrasjonsmalen. Under synkronisering settes feltet **Prosjekttype** for nye prosjekter til denne verdien. Verdien kan imidlertid bli oppdatert når prosjektkontraktslinjene synkroniseres fra Project Service Automation. |
|                        | Tidskategori        | Velg standard tidskategori. Denne verdien brukes når timeestimater synkroniseres fra Project Service Automation. Når timeestimater og faktiske timer synkroniseres fra Project Service Automation, settes feltet **Kategori** for nye prosjekttimeprognoser i Finance and Operations til denne verdien. |
|                        | Avgiftskategori         | Velg standard avgiftskategori. Denne verdien brukes når faktiske avgifter synkroniseres fra Project Service Automation. Når faktiske avgifter synkroniseres fra Project Service Automation, settes feltet **Kategori** for nye avgiftstransaksjoner i Finance and Operations til denne verdien. |
| Standarder for prosjektgruppe | Prosjekttype         | Klikk på **Ny** for å legge til en rad der du kan velge prosjekttypen som standard prosjektgruppe skal angis for. En bestemt prosjekttype kan bare velges én gang i konfigurasjonen. |
|                        | Prosjektgruppe        | Velg standard prosjektgruppe for den valgte prosjekttypen. Når nye prosjekter synkroniseres fra Project Service Automation, angis **Prosjektgruppe**-feltet til standardverdien for prosjekttypen hvis du ikke har angitt en standardverdi i integrasjonsmalen. |
| Standarder for faktureringstype  | Faktureringstype         | Klikk på **Ny** for å legge til en rad der du kan velge faktureringstypen som standard linjeegenskap skal angis for. En bestemt faktureringstype kan bare velges én gang i konfigurasjonen. |
|                        | Linjeegenskap        | Velg standard linjeegenskap for den valgte faktureringstypen. Når nye timeestimater, nye utgiftsestimater eller nye faktiske data synkroniseres fra Project Service Automation, vil **Linjeegenskap**-feltet settes til standardverdien for faktureringstypen. |
| Funksjonalitetslåsing  | Gjelder ikke her       | Velg funksjonen som skal deaktiveres i Finance and Operations for prosjekter og kontrakter som kommer fra Project Service Automation. Du kan for eksempel deaktivere muligheten for å redigere kontrakter og prosjekter, opprette arbeidsnedbrytningsstrukturer og angi timeregistreringer i Finance and Operations. Regnskapstilknyttede felt vil fortsatt være aktivert, selv om de ikke gjøres tilgjengelige av parameterinnstillingen. All funksjonalitet er aktivert som standard. |
