---
title: Integreringsparametere for Project Service Automation
description: Du kan konfigurere hvordan data skal brukes som standard ved integrering av Project Service Automation med Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Integreringsparametere for Project Service Automation

På siden **Integreringsparametere for Project Service Automation** kan du konfigurere hvordan data skal brukes som standard ved integrering av Project Service Automation med Finance and Operations. Følgende må defineres for at prosjekter skal være synkronisert fra Project Service Automation i Finance and Operations.

> [!NOTE]
> Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0.




| **Kategori**                      | **Felt**                          | **Beskrivelse**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Generelt**                  | **Standard prosjekttype**               | Velg standard for **Prosjekttype**, som er når prosjekter synkroniseres fra Project Service Automation hvis du ikke har angitt en standardverdi i integrasjonsmalen. Under synkroniseringen vil nye prosjekter ha **Prosjekttype** satt til denne verdien og kan bli oppdatert når prosjektkontraktlinjene synkroniseres fra Project Service Automation.               |
| **Generelt**                  | **Tidskategori**                      | Velg standard for **Tidskategori**, som er når timeestimater synkroniseres fra Project Service Automation. Under synkroniseringen vil nye prosjekttimeprognoser i Finance and Operations ha **Kategori** satt til denne verdien når timeestimater og faktiske timer synkroniseres fra Project Service Automation.   |
| **Generelt**                  | **Avgiftskategori**                       | Velg standard for **Avgiftskategori**, som er når faktiske avgifter synkroniseres fra Project Service Automation. Under synkroniseringen vil nye avgiftstransaksjoner i Finance and Operations ha **Kategori** satt til denne verdien når faktiske avgifter synkroniseres fra Project Service Automation.          |
| **Standarder for prosjektgruppe**   | **Prosjekttype** | Klikk **Ny** for å legge til en rad der du kan velge prosjekttypen som det skal angis standard prosjektgruppe for. En bestemt prosjekttype kan bare velges én gang i konfigurasjonen.              
|                              | **Prosjektgruppe**          | Velg standard prosjektgruppe for den angitte prosjekttypen. Når nye prosjekter synkroniseres fra Project Service Automation, vil **Prosjektgruppe** være standarden basert på prosjekttypen hvis du ikke har angitt en standardverdi i integrasjonsmalen.  |
| **Standarder for faktureringstype**    | **Faktureringstype** | Klikk **Ny** for å legge til en rad der du kan velge faktureringstype som det skal angis standard linjeegenskap for. En bestemt faktureringstype kan bare velges én gang i konfigurasjonen.          |
|                              | **Linjeegenskap**| Velg standard linjeegenskap for den angitte faktureringstypen. Når nye timeestimater, nye utgiftsestimater eller nye faktiske data synkroniseres fra Project Service Automation, vil **Linjeegenskap** være standard basert på faktureringstypen.          |
| **Funksjonalitetslåsing**    |                   | Velg funksjonen som skal deaktiveres i Finance and Operations for prosjekter og kontrakter som kommer fra Project Service Automation. Du kan for eksempel velge å deaktivere muligheten til å redigere kontrakter og prosjekter, opprette arbeidsnedbrytningsstrukturer og angi timeregistreringer i Finance and Operations. Regnskapstilknyttede felt vil fortsatt være aktivert, selv om de ikke gjøres tilgjengelige av parameterinnstillingen. All funksjonalitet vil være aktivert som standard.           |

