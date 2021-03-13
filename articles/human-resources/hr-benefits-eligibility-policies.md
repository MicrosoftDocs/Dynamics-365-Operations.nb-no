---
title: Policyer for fordelsrettigheter
description: Denne artikkelen inneholder informasjon om policyer for fordelsrettigheter, som hjelper deg med å definere hvem som er kvalifisert for spesifikke fordeler
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cc5dfedc0022cbf9bdbc636bbe96971422c29838
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113671"
---
# <a name="benefit-eligibility-policies"></a>Policyer for fordelsrettigheter

Denne artikkelen inneholder informasjon om policyer for fordelsrettigheter, som hjelper deg med å definere hvem som er kvalifisert for spesifikke fordeler

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




