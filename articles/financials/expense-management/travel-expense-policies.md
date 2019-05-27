---
title: Definer utgiftspolicyer
description: Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514445"
---
# <a name="expense-policies"></a><span data-ttu-id="71f98-103">Utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="71f98-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71f98-104">Du kan definere policyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="71f98-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="71f98-105">Ved å bruke policyer for reiseregning kan du administrere utgiftene dine på en effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="71f98-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="71f98-106">For eksempel kan du sette opp en policy for hotellutgifter i New York City, som angir at det per natt ikke kan overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="71f98-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="71f98-107">Hvis en ansatt sender en reiseregning eller en reiserekvisisjon der romprisen per dag er høyere enn dette beløpet, vasler systemet</span><span class="sxs-lookup"><span data-stu-id="71f98-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="71f98-108">den ansatte om at policybeløpet for utgifter er overskredet.</span><span class="sxs-lookup"><span data-stu-id="71f98-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="71f98-109">Du kan konfigurere meldingen som den ansatte får når du</span><span class="sxs-lookup"><span data-stu-id="71f98-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="71f98-110">definer policyreglene.</span><span class="sxs-lookup"><span data-stu-id="71f98-110">define the policy.</span></span>      
        
<span data-ttu-id="71f98-111">Du kan definere tre typer policyer.</span><span class="sxs-lookup"><span data-stu-id="71f98-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="71f98-112">Advarsel – Tillater arbeidstakeren å sende inn en utgiftsrapport eller reiseregning, men kostnaden vil markeres for godkjennere</span><span class="sxs-lookup"><span data-stu-id="71f98-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="71f98-113">for senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="71f98-113">for later reporting.</span></span>        

- <span data-ttu-id="71f98-114">Feil – Krever at arbeidstakeren reviderer utgiftene for samsvar med policyen før innsending av utgiftsrapporten elle reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="71f98-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="71f98-115">Begrunnelse – Krever at arbeidstakeren eller en leder skal legge inn en begrunnelse for å overskride beløpet før innsending av utgiftsrapport eller reiseregning.</span><span class="sxs-lookup"><span data-stu-id="71f98-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

# <a name="policy-tips"></a><span data-ttu-id="71f98-116">Policytips</span><span class="sxs-lookup"><span data-stu-id="71f98-116">Policy tips</span></span>
<span data-ttu-id="71f98-117">Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="71f98-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="71f98-118">Policyer har ikrafttredelsesdato og vil ikke tre i kraft hvis policyen opprettes med en dato etter datoen da utgiften fant sted.</span><span class="sxs-lookup"><span data-stu-id="71f98-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="71f98-119">Hvis du for eksempel oppretter en ny policy i dag for å bruke en maksimal måltidsutgift på NOK 500, blir eksisterende utgifter registrert fra i går ikke kontrollert mot denne policyen.</span><span class="sxs-lookup"><span data-stu-id="71f98-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="71f98-120">Når du oppretter en policy for en utgiftskategori som kan være spesifisert, må du vurdere å legge til en betingelse for utgiftslinjetype.</span><span class="sxs-lookup"><span data-stu-id="71f98-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="71f98-121">Noen policyer, for eksempel å kreve en kvittering, vil kanskje ikke gi mening for spesifiserte linjer, og bør bare brukes på hodelinjen eller en ikke-spesifisert linje.</span><span class="sxs-lookup"><span data-stu-id="71f98-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

# <a name="when-to-evaluate-policies"></a><span data-ttu-id="71f98-122">Når skal policyer evalueres</span><span class="sxs-lookup"><span data-stu-id="71f98-122">When to evaluate policies</span></span>

<span data-ttu-id="71f98-123">I reiseregningsparametere finnes det et alternativ for å evaluere policyer for utgiftsadministrasjon når en linje lagres eller når en reiseregning sendes.</span><span class="sxs-lookup"><span data-stu-id="71f98-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="71f98-124">Hvis du velger å evaluere når en linje lagres, sikrer du at brukerne har tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig.</span><span class="sxs-lookup"><span data-stu-id="71f98-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="71f98-125">Ellers kan du utsette policyevalueringen og spare tid hvis du lar valideringen skje på slutten, under sending til arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="71f98-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
