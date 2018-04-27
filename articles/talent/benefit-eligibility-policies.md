---
title: Policyer for fordelsrettigheter
description: "Denne artikkelen inneholder informasjon om policyer for fordelsrettigheter, som hjelper deg med å definere hvem som er kvalifisert for spesifikke fordeler"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 46dba3a61cf96b19b5bc4d2956d028bbbeaaa60e
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="benefit-eligibility-policies"></a>Policyer for fordelsrettigheter

[!INCLUDE [banner](includes/banner.md)]

Dette emnet inneholder informasjon om policyer for fordelsrettigheter, som hjelper deg med å definere hvem som er kvalifisert for spesifikke fordeler

Når du oppretter fordeler, kan du bestemme hvilke fordeler som skal være tilgjengelige for ansatte. Tabellen nedenfor viser eksempler på fordeler du kan gjøre tilgjengelige for bestemte ansatte.

| Fordel          | Hvem fordelen er tilgjengelig for |
|------------------|---------------------------------|
| Helseforsikring | Alle ansatte                   |
| Mobiltelefon     | Salgsstab, ledere         |
| Parkeringsoblater   | Ledere                      |

Følgende komponenter brukes til å opprette rettighetspolicyer:

-   Policyregeltyper
-   Policyer for fordelsrettigheter

Policyregeltyper definerer spørringsparameterne som brukes når du utvikler bestemte policyregler. Når du oppretter policyregeltyper, kan du opprette policyer for fordelsrettigheter. Policyene lar deg opprette en samling regler som gjelder for én eller flere juridiske enheter. I hver policy kan du vise en hvilken som helst av policyregeltypene for fordelsrettigheter du opprettet tidligere. 

Du kan definere omfanget av regelen i policyen. Hvis du for eksempel oppretter en policyregeltype for fordelsrettigheter kalt **Ledelse**, kan du angi hva regelen er i denne policyen. Regelen kan for eksempel være at alle stillingsnavn som inneholder ordet «leder» eller «sjef» skal være med i regelen. Når du har definert parameterne for regelen eller reglene som er inkludert i policyen, kan du tilordne en bestemt regel til fordelen.

<a name="see-also"></a>Se også
--------

[Definere og administrere et fordelsprogram](manage-benefit-program.md)




