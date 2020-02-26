---
title: Fjerne en forekomst
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010023"
---
# <a name="remove-an-instance"></a>Fjerne en forekomst

Denne artikkelen leder deg gjennom prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Fjerne et testversjonsmiljø

Testversjoner av Human Resources er klargjort med en policy for utløpsdato på 60 dagers. Eiere av testversjonsmiljøer har imidlertid mulighet til å avslutte prøveversjonen tidlig ved å fullføre trinnene nedenfor. 

1. Gå til [Power Apps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).
2. Velg **Miljøer**.
3. Velg testversjonsmiljøet, som har et navngivingsmønster som ser slik ut: TestDrive - alias@domain
4. Velg **Slett**, og bekreft beslutningen. 

Det eksisterende testversjonsmiljøet fjernes. Når det fjernes, kan du registrere deg for et nytt testversjonsmiljø. 

## <a name="remove-a-production-environment"></a>Fjerne et produksjonsmiljø

Denne artikkelen antar at du har kjøpt Human Resources gjennom en Cloud Solution Provider (CSP)- eller en enterprise architecture (EA)-avtale. 

Siden et enkelt Human Resources-miljø er inkludert i et enkelt Power Apps-miljø, finnes det to alternativer du bør vurdere. Første alternativ er å fjerne hele Power Apps-miljøet. Det andre alternativet er å fjerne bare Human Resources. Det første alternativet bør velges når du har opprettet et Power Apps-miljø uttrykkelig for klargjøring av Human Resources, og du akkurat har begynt implementering, eller du ikke har noen etablerte integreringer. Det andre alternativet er riktig når du har et etablert Power Apps-miljø fylt ut med rike data som brukes i Power Apps og Power Automate.

> [!Important]
> Før du fjerner Power Apps-miljøet, kontrollerer du at det ikke brukes for rike data-integreringer utenfor området for Human Resources. Merk også at standard Power Apps-miljøer ikke kan fjernes. 

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
4.  Logg på LCS ved hjelp av kontoen du brukte til å abonnere på Human Resources. 
5. Velg Human Resources-prosjektet som inneholder miljøet. 
6. I LCS prosjektet velger du flisen **Human Resources-appbehandling**. 
7. Velg forekomsten du vil fjerne, som skal være merket med distribusjonsstatusen **Mislykket**.
8. Velg **Fjern forekomst**, og bekrefte beslutningen. 
