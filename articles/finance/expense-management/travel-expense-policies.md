---
title: Definer utgiftspolicyer
description: Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389721"
---
# <a name="define-expense-policies"></a><span data-ttu-id="1697b-103">Definer utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="1697b-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1697b-104">Du kan definere policyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="1697b-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="1697b-105">Ved å bruke policyer for reiseregning kan du administrere utgiftene dine på en effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="1697b-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="1697b-106">For eksempel kan du sette opp en policy for hotellutgifter i New York City, som angir at det per natt ikke kan overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="1697b-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="1697b-107">Hvis en ansatt sender en reiseregning eller en reiserekvisisjon der romprisen per dag er høyere enn dette beløpet, vasler systemet</span><span class="sxs-lookup"><span data-stu-id="1697b-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="1697b-108">den ansatte om at policybeløpet for utgifter er overskredet.</span><span class="sxs-lookup"><span data-stu-id="1697b-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="1697b-109">Du kan konfigurere meldingen som den ansatte får når du</span><span class="sxs-lookup"><span data-stu-id="1697b-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="1697b-110">definer policyreglene.</span><span class="sxs-lookup"><span data-stu-id="1697b-110">define the policy.</span></span>      
        
<span data-ttu-id="1697b-111">Du kan definere tre typer policyer.</span><span class="sxs-lookup"><span data-stu-id="1697b-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="1697b-112">Advarsel – Tillater arbeidstakeren å sende inn en utgiftsrapport eller reiseregning, men kostnaden vil markeres for godkjennere</span><span class="sxs-lookup"><span data-stu-id="1697b-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="1697b-113">for senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="1697b-113">for later reporting.</span></span>        

- <span data-ttu-id="1697b-114">Feil – Krever at arbeidstakeren reviderer utgiftene for samsvar med policyen før innsending av utgiftsrapporten elle reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="1697b-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="1697b-115">Begrunnelse – Krever at arbeidstakeren eller en leder skal legge inn en begrunnelse for å overskride beløpet før innsending av utgiftsrapport eller reiseregning.</span><span class="sxs-lookup"><span data-stu-id="1697b-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="1697b-116">Policytips</span><span class="sxs-lookup"><span data-stu-id="1697b-116">Policy tips</span></span>
<span data-ttu-id="1697b-117">Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="1697b-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="1697b-118">Policyer har ikrafttredelsesdato og vil ikke tre i kraft hvis policyen opprettes med en dato etter datoen da utgiften fant sted.</span><span class="sxs-lookup"><span data-stu-id="1697b-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="1697b-119">Hvis du for eksempel oppretter en ny policy i dag for å bruke en maksimal måltidsutgift på NOK 500, blir eksisterende utgifter registrert fra i går ikke kontrollert mot denne policyen.</span><span class="sxs-lookup"><span data-stu-id="1697b-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="1697b-120">Når du oppretter en policy for en utgiftskategori som kan være spesifisert, må du vurdere å legge til en betingelse for utgiftslinjetype.</span><span class="sxs-lookup"><span data-stu-id="1697b-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="1697b-121">Noen policyer, for eksempel å kreve en kvittering, vil kanskje ikke gi mening for spesifiserte linjer, og bør bare brukes på hodelinjen eller en ikke-spesifisert linje.</span><span class="sxs-lookup"><span data-stu-id="1697b-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="1697b-122">Policyer for reiseregning evalueres mot kildeenheten som standard.</span><span class="sxs-lookup"><span data-stu-id="1697b-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="1697b-123">I konserninterne scenarioer kan du angi at policyen i stedet skal evalueres mot målenheten (enheten som låner).</span><span class="sxs-lookup"><span data-stu-id="1697b-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="1697b-124">Hvis du vil kjøre policyene mot målenheten, kan du aktivere funksjonen Evaluer utgiftspolicy mot juridisk enhet som låner i arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="1697b-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="1697b-125">Når skal policyer evalueres</span><span class="sxs-lookup"><span data-stu-id="1697b-125">When to evaluate policies</span></span>

<span data-ttu-id="1697b-126">I reiseregningsparametere finnes det et alternativ for å evaluere policyer for utgiftsadministrasjon når en linje lagres eller når en reiseregning sendes.</span><span class="sxs-lookup"><span data-stu-id="1697b-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="1697b-127">Hvis du velger å evaluere når en linje lagres, sikrer du at brukerne har tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig.</span><span class="sxs-lookup"><span data-stu-id="1697b-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="1697b-128">Ellers kan du utsette policyevalueringen og spare tid hvis du lar valideringen skje på slutten, under sending til arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="1697b-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
