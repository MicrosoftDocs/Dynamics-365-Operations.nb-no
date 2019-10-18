---
title: Integreringsparametere for Project Service Automation
description: Dette emnet forklarer hvordan du konfigurerer måten standarddata registreres på når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 Finance.
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
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174978"
---
# <a name="project-service-automation-integration-parameters"></a>Parametere for integrering av Project Service Automation

[!include[banner](../includes/banner.md)]

På siden **Parametere for integrering av Project Service Automation** kan konfigurere hvordan standarddata registreres når du integrerer Dynamics 365 Project Service Automation med Dynamics 365 Finance. For at prosjekter skal synkroniseres fra Project Service Automation to Finance, må feltene nedenfor konfigureres.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i versjon 8.0.
> - Integrasjon av faktiske data er tilgjengelig i versjon 8.0.1 eller nyere.


| Tab                    | Felt                | Beskrivelse |
|------------------------|----------------------|-------------|
| Generelt                | Standard prosjekttype | Velg standard prosjekttype. Når prosjekter synkroniseres fra Project Service Automation, brukes denne verdien hvis du ikke har angitt en standardverdi i integrasjonsmalen. Under synkronisering settes feltet **Prosjekttype** for nye prosjekter til denne verdien. Verdien kan imidlertid bli oppdatert når prosjektkontraktslinjene synkroniseres fra Project Service Automation. |
|                        | Tidskategori        | Velg standard tidskategori. Denne verdien brukes når timeestimater synkroniseres fra Project Service Automation. Når timeestimater og faktiske timer synkroniseres fra Project Service Automation, settes feltet **Kategori** for nye prosjekttimeprognoser i Finance til denne verdien. |
|                        | Avgiftskategori         | Velg standard avgiftskategori. Denne verdien brukes når faktiske avgifter synkroniseres fra Project Service Automation. Når faktiske avgifter synkroniseres fra Project Service Automation, settes feltet **Kategori** for nye avgiftstransaksjoner i Finance til denne verdien. |
| Standarder for prosjektgruppe | Prosjekttype         | Klikk på **Ny** for å legge til en rad der du kan velge prosjekttypen som standard prosjektgruppe skal angis for. En bestemt prosjekttype kan bare velges én gang i konfigurasjonen. |
|                        | Prosjektgruppe        | Velg standard prosjektgruppe for den valgte prosjekttypen. Når nye prosjekter synkroniseres fra Project Service Automation, angis **Prosjektgruppe**-feltet til standardverdien for prosjekttypen hvis du ikke har angitt en standardverdi i integrasjonsmalen. |
| Standarder for faktureringstype  | Faktureringstype         | Klikk på **Ny** for å legge til en rad der du kan velge faktureringstypen som standard linjeegenskap skal angis for. En bestemt faktureringstype kan bare velges én gang i konfigurasjonen. |
|                        | Linjeegenskap        | Velg standard linjeegenskap for den valgte faktureringstypen. Når nye timeestimater, nye utgiftsestimater eller nye faktiske data synkroniseres fra Project Service Automation, vil **Linjeegenskap**-feltet settes til standardverdien for faktureringstypen. |
| Funksjonalitetslåsing  | Gjelder ikke       | Velg funksjonen som skal deaktiveres i Finance for prosjekter og kontrakter som kommer fra Project Service Automation. Du kan for eksempel deaktivere muligheten for å redigere kontrakter og prosjekter, opprette arbeidsnedbrytningsstrukturer og angi timeregistreringer i Finance. Regnskapstilknyttede felt vil fortsatt være aktivert, selv om de ikke gjøres tilgjengelige av parameterinnstillingen. All funksjonalitet er aktivert som standard. |
