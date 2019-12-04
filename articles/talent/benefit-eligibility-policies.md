---
title: Policyer for fordelsrettigheter
description: Denne artikkelen inneholder informasjon om policyer for fordelsrettigheter, som hjelper deg med å definere hvem som er kvalifisert for spesifikke fordeler
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: b44287bf22f0b6c4e33a29b4b86aaae934505a43
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814703"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="1b583-103">Policyer for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="1b583-103">Benefit eligibility policies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b583-104">Dette emnet inneholder informasjon om policyer for fordelsrettigheter, som hjelper deg med å definere hvem som er kvalifisert for spesifikke fordeler</span><span class="sxs-lookup"><span data-stu-id="1b583-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="1b583-105">Når du oppretter fordeler, kan du bestemme hvilke fordeler som skal være tilgjengelige for ansatte.</span><span class="sxs-lookup"><span data-stu-id="1b583-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="1b583-106">Tabellen nedenfor viser eksempler på fordeler du kan gjøre tilgjengelige for bestemte ansatte.</span><span class="sxs-lookup"><span data-stu-id="1b583-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="1b583-107">Fordel</span><span class="sxs-lookup"><span data-stu-id="1b583-107">Benefit</span></span>          | <span data-ttu-id="1b583-108">Hvem fordelen er tilgjengelig for</span><span class="sxs-lookup"><span data-stu-id="1b583-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="1b583-109">Helseforsikring</span><span class="sxs-lookup"><span data-stu-id="1b583-109">Health insurance</span></span> | <span data-ttu-id="1b583-110">Alle ansatte</span><span class="sxs-lookup"><span data-stu-id="1b583-110">All employees</span></span>                   |
| <span data-ttu-id="1b583-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="1b583-111">Mobile phone</span></span>     | <span data-ttu-id="1b583-112">Salgsstab, ledere</span><span class="sxs-lookup"><span data-stu-id="1b583-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="1b583-113">Parkeringsoblater</span><span class="sxs-lookup"><span data-stu-id="1b583-113">Parking passes</span></span>   | <span data-ttu-id="1b583-114">Ledere</span><span class="sxs-lookup"><span data-stu-id="1b583-114">Executives</span></span>                      |

<span data-ttu-id="1b583-115">Følgende komponenter brukes til å opprette rettighetspolicyer:</span><span class="sxs-lookup"><span data-stu-id="1b583-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="1b583-116">Policyregeltyper</span><span class="sxs-lookup"><span data-stu-id="1b583-116">Policy rule types</span></span>
-   <span data-ttu-id="1b583-117">Policyer for fordelsrettigheter</span><span class="sxs-lookup"><span data-stu-id="1b583-117">Benefit eligibility policies</span></span>

<span data-ttu-id="1b583-118">Policyregeltyper definerer spørringsparameterne som brukes når du utvikler bestemte policyregler.</span><span class="sxs-lookup"><span data-stu-id="1b583-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="1b583-119">Når du oppretter policyregeltyper, kan du opprette policyer for fordelsrettigheter.</span><span class="sxs-lookup"><span data-stu-id="1b583-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="1b583-120">Policyene lar deg opprette en samling regler som gjelder for én eller flere juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="1b583-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="1b583-121">I hver policy kan du vise en hvilken som helst av policyregeltypene for fordelsrettigheter du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="1b583-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="1b583-122">Du kan definere omfanget av regelen i policyen.</span><span class="sxs-lookup"><span data-stu-id="1b583-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="1b583-123">Hvis du for eksempel oppretter en policyregeltype for fordelsrettigheter kalt **Ledelse**, kan du angi hva regelen er i denne policyen.</span><span class="sxs-lookup"><span data-stu-id="1b583-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="1b583-124">Regelen kan for eksempel være at alle stillingsnavn som inneholder ordet «leder» eller «sjef» skal være med i regelen.</span><span class="sxs-lookup"><span data-stu-id="1b583-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="1b583-125">Når du har definert parameterne for regelen eller reglene som er inkludert i policyen, kan du tilordne en bestemt regel til fordelen.</span><span class="sxs-lookup"><span data-stu-id="1b583-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1b583-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1b583-126">Additional resources</span></span>
--------

[<span data-ttu-id="1b583-127">Definere og administrere et fordelsprogram</span><span class="sxs-lookup"><span data-stu-id="1b583-127">Define and manage a benefits program</span></span>](manage-benefit-program.md)



