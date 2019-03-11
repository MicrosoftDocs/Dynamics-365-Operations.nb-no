---
title: Fjerne Talent-miljøer
description: Dette emnet leder deg gjennom prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305713"
---
# <a name="remove-talent-environments"></a>Fjerne Talent-miljøer

[!include [banner](includes/banner.md)]

Dette emnet leder deg gjennom prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 for Talent.

## <a name="removing-a-test-drive-environment"></a>Fjerne et testversjonsmiljø

Testversjoner av Talent er klargjort med en policy for utløpsdato på 60 dagers. Eiere av testversjonsmiljøer har imidlertid mulighet til å avslutte prøveversjonen tidlig ved å fullføre trinnene nedenfor. 

1. Gå til [PowerApps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).
2. Velg **Miljøer**.
3. Velg testversjonsmiljøet, som har et navngivingsmønster som ser slik ut: TestDrive - alias@domain
4. Velg **Slett**, og bekreft beslutningen. 

Det eksisterende testversjonsmiljøet fjernes. Når det fjernes, kan du registrere deg for et nytt testversjonsmiljø. 

## <a name="removing-a-production-environment"></a>Fjerne et produksjonsmiljø

Dette emnet antar at du har kjøpt Talent gjennom en Cloud Solution Provider (CSP)- or enterprise architecture (EA)-avtale. 

Siden et enkelt Talent-miljø er inkludert i et enkelt PowerApps-miljø, finnes det to alternativer du bør vurdere. Første alternativ er å fjerne hele PowerApps-miljøet. Det andre alternativet er å fjerne bare Talent. Det første alternativet bør velges når du har opprettet et PowerApps-miljø uttrykkelig for klargjøring av Talent, og du akkurat har begynt implementering, eller du ikke har noen etablerte integreringer. Det andre alternativet er riktig når du har et etablert PowerApps-miljø fylt ut med rike data som brukes i PowerApps og flyter.

> [!Important]
> Før du fjerner PowerApps-miljøet, kontrollerer du at det ikke brukes for rike data-integreringer utenfor området for Talent. Merk også at standard PowerApps-miljøer ikke kan fjernes. 

Slik fjerner du hele PowerApps-miljøet, inkludert Talent og tilknyttede apper og flyter:

1. Gå til [PowerApps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).
2. Velg **Miljøer**.
3. Velg miljøet som skal fjernes.
4. Velg **Slett**, og bekreft beslutningen. 
5. Vent til slettingen er fullført.
6. Logg på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjelp av kontoen du brukte til å abonnere på Talent. 
7. Velg Talent-prosjektet som inneholder miljøet. 
8. I LCS prosjektet velger du flisen **Talent-appbehandling**. 
9. Velg forekomsten som skal fjernes. 
10. Velg **Fjern forekomst**, og bekrefte beslutningen.  

Hvis du vil fjerne et Talent-miljø fra et eksisterende PowerApps-miljø, kan du fullføre trinnene nedenfor. Legg merke til at behovet for å involvere støtte og kontakt Talent DevOps-teamet er midlertidig til denne funksjonen er aktivert direkte i LCS.

1. Kontakt kundestøtte for å starte en forespørsel om fjerning.
2. Kundestøtteteamet vil opprette en forespørsel om fjerning med Talent DevOps-teamet. 
3. Fortsett etter at du får beskjed om at miljøet er fjernet.
4.  Logg på LCS ved hjelp av kontoen du brukte til å abonnere på Talent. 
5. Velg Talent-prosjektet som inneholder miljøet. 
6. I LCS prosjektet velger du flisen **Talent-appbehandling**. 
7. Velg forekomsten du vil fjerne, som skal være merket med distribusjonsstatusen **Mislykket**.
8. Velg **Fjern forekomst**, og bekrefte beslutningen. 

