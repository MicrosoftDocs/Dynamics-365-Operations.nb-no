---
title: Policyer for fordelsrettigheter
description: Dette emnet inneholder informasjon om policyer for fordelsrettigheter, som definerer hvem som er kvalifisert for spesifikke fordeler
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e1f64a0beffe12f6b4e0ad53d3bbaa96822dc7e8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066049"
---
# <a name="benefit-eligibility-policies"></a>Policyer for fordelsrettigheter


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet inneholder informasjon om policyer for fordelsrettigheter, som definerer hvem som er kvalifisert for spesifikke fordeler

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






[!INCLUDE[footer-include](../includes/footer-banner.md)]
