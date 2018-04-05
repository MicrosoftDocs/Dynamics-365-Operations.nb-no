---
title: Definer utgiftspolicyer
description: "Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3b2a28fe6acf03e52c292048a797ce997f58bcce
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="expense-policies"></a><span data-ttu-id="91dda-103">Utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="91dda-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="91dda-104">Du kan definere policyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="91dda-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="91dda-105">Ved å bruke policyer for reiseregning kan du administrere utgiftene dine på en effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="91dda-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="91dda-106">For eksempel kan du sette opp en policy for hotellutgifter i New York City, som angir at det per natt ikke kan overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="91dda-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="91dda-107">Hvis en ansatt sender en reiseregning eller en reiserekvisisjon der romprisen per dag er høyere enn dette beløpet, vasler systemet</span><span class="sxs-lookup"><span data-stu-id="91dda-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="91dda-108">den ansatte om at policybeløpet for utgifter er overskredet.</span><span class="sxs-lookup"><span data-stu-id="91dda-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="91dda-109">Du kan konfigurere meldingen som den ansatte får når du</span><span class="sxs-lookup"><span data-stu-id="91dda-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="91dda-110">definer policyreglene.</span><span class="sxs-lookup"><span data-stu-id="91dda-110">define the policy.</span></span>      
        
<span data-ttu-id="91dda-111">Du kan definere tre typer policyer.</span><span class="sxs-lookup"><span data-stu-id="91dda-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="91dda-112">Advarsel – Tillater arbeidstakeren å sende inn en utgiftsrapport eller reiseregning, men kostnaden vil markeres for godkjennere</span><span class="sxs-lookup"><span data-stu-id="91dda-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
<span data-ttu-id="91dda-113">for senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="91dda-113">for later reporting.</span></span>        

- <span data-ttu-id="91dda-114">Feil – Krever at arbeidstakeren reviderer utgiftene for samsvar med policyen før innsending av utgiftsrapporten elle reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="91dda-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="91dda-115">Begrunnelse – Krever at arbeidstakeren eller en leder skal legge inn en begrunnelse for å overskride beløpet før innsending av utgiftsrapport eller reiseregning.</span><span class="sxs-lookup"><span data-stu-id="91dda-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
 <span data-ttu-id="91dda-116">Du kan også sette opp en datoperioden for når utgiftpolicyen er effektiv.</span><span class="sxs-lookup"><span data-stu-id="91dda-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="91dda-117">For eksempel, flybilletter for fly mellom Danmark</span><span class="sxs-lookup"><span data-stu-id="91dda-117">For example, airline fares for flights between Denmark</span></span>      
 <span data-ttu-id="91dda-118">og New York City kan være kostbare i høysesongen.</span><span class="sxs-lookup"><span data-stu-id="91dda-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="91dda-119">Du kan definere en utgiftsregel for flyvninger som begrenses av</span><span class="sxs-lookup"><span data-stu-id="91dda-119">You can define a flight expense rule that restricts the</span></span>      
 <span data-ttu-id="91dda-120">en grense for kostnaden på flybilletter til New York City på DKK 5000, og du kan spesifisere at regelen er gyldig mellom 15. mars og</span><span class="sxs-lookup"><span data-stu-id="91dda-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
 <span data-ttu-id="91dda-121">15. september.</span><span class="sxs-lookup"><span data-stu-id="91dda-121">September 15.</span></span>

