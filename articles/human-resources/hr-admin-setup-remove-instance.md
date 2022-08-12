---
title: Fjerne en forekomst
description: Denne artikkelen beskriver prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178480"
---
# <a name="remove-an-instance"></a>Fjerne en forekomst

_**Gjelder For:** Human Resources i den frittstående infrastrukturen_ 

> [!NOTE]
> Fra og med juli 2022 kan ikke nye Human Resources-miljøer klargjøres i den frittstående Human Resources-infrastrukturen, og nye Microsoft Dynamics Lifecycle Services-prosjekter (LCS) kan ikke opprettes i den. Kunder kan distribuere Human Resources-miljøer i infrastrukturen i Finance and Operations. Hvis du vil ha mer informasjon , kan du se [Klargjøring av Human Resources i infrastrukturen i Finance and Operations](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finance and Operations-infrastrukturen støtter sletting av et miljø. Hvis du vil ha mer informasjon om hvordan du sletter et miljø, kan du se [Slett et miljø](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

Denne artikkelen forklarer prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Fjerne et testversjonsmiljø

Testversjoner av Human Resources er klargjort med en policy for utløpsdato på 60 dagers. Eiere av testversjonsmiljøer har imidlertid mulighet til å avslutte prøveversjonen tidlig ved å fullføre trinnene nedenfor. 

1. Gå til [Power Apps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).
2. Velg **Miljøer**.
3. Velg testversjonsmiljøet, som har et navngivingsmønster som ser slik ut: TestDrive - alias@domain
4. Velg **Slett**, og bekreft beslutningen. 

Det eksisterende testversjonsmiljøet fjernes. Når det fjernes, kan du registrere deg for et nytt testversjonsmiljø. 

## <a name="remove-a-production-environment"></a>Fjerne et produksjonsmiljø

Denne artikkelen antar at du har kjøpt Human Resources gjennom en Cloud Solution Provider (CSP)- eller en enterprise architecture (EA)-avtale. 

Siden et enkelt Human Resources-miljø er inkludert i et enkelt Power Apps-miljø, finnes det to alternativer du bør vurdere når du skal fjerne et miljø: 
- **Fjern hele Power Apps-miljøet.** Dette alternativet bør velges når Power Apps-miljøet ble opprettet uttrykkelig for klargjøring av Human Resources, og implementering nettopp er begynt, eller du ikke har noen etablerte integreringer.  
- **Fjern bare Human Resources.** Dette alternativet passer når du har et etablert Power Apps-miljø fylt ut med rike data som brukes i Microsoft Power Apps og Power Automate.


> [!Important]
> Før du fjerner Power Apps-miljøet, kontrollerer du at det ikke brukes for dataintegreringer utenfor området for Human Resources. Merk også at standard Power Apps-miljøer ikke kan fjernes. 

Slik fjerner du hele Power Apps-miljøet, inkludert Human Resources og tilknyttede apper og flyter:

1. Gå til [Power Apps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).
2. Velg **Miljøer**.
3. Velg miljøet som skal fjernes.
4. Velg **Slett**, og bekreft beslutningen. 
5. Vent til slettingen er fullført.
6. Logg på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjelp av kontoen du brukte til å abonnere på Human Resources. 
7. Velg Human Resources-prosjektet som inneholder miljøet. 
8. I LCS prosjektet velger du flisen **Human Resources-appbehandling**. 
9. Velg forekomsten som skal fjernes. 
10. Velg **Fjern forekomst**, og bekrefte beslutningen.  

Hvis du vil fjerne et Human Resources-miljø fra et eksisterende Power Apps-miljø, kan du fullføre trinnene nedenfor. Legg merke til at behovet for å involvere støtte og kontakt Human Resources DevOps-teamet er midlertidig til denne funksjonen er aktivert direkte i LCS.

1. Kontakt kundestøtte for å starte en forespørsel om fjerning.
2. Kundestøtteteamet vil opprette en forespørsel om fjerning med Human Resources DevOps-teamet. 
3. Fortsett etter at du får beskjed om at miljøet er fjernet.
4. Logg på LCS ved hjelp av kontoen du brukte til å abonnere på Human Resources. 
5. Velg Human Resources-prosjektet som inneholder miljøet. 
6. I LCS prosjektet velger du flisen **Human Resources-appbehandling**. 
7. Velg forekomsten du vil fjerne, som skal være merket med distribusjonsstatusen **Slettet**.
8. Velg **Fjern forekomst**, og bekrefte beslutningen. 

## <a name="recover-a-soft-deleted-environment"></a>Gjenopprette et mykt slettet miljø

Hvis du sletter Power Apps-miljøet som personalmiljøet ditt er koblet til, vil statusen for personalmiljøet i LCS være **Mykt slettet**. I dette tilfellet kan ikke brukere koble til personalmiljøet.

Slik gjenoppretter du miljøet:

1. Følg instruksjonene i [Gjenopprette Power Apps-miljøet](/power-platform/admin/recover-environment).

2. Kontakt kundestøtte for å gjenopprette personalmiljøet. For mer informasjon, se [Få kundestøtte](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps-miljøer lagres bare i sju dager etter sletting. Du må gjenopprette miljøet i løpet av denne perioden på sju dager.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
