---
title: Definer utgiftspolicyer
description: "Du kan definere utgiftspolicyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="1e9a8-103">Utgiftspolicyer</span><span class="sxs-lookup"><span data-stu-id="1e9a8-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1e9a8-104">Du kan definere policyer som dine arbeidstakere må følge når de går inn i og sender utgiftsrapporter og reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="1e9a8-105">Ved å bruke policyer for reiseregning kan du administrere utgiftene dine på en effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="1e9a8-106">For eksempel kan du sette opp en policy for hotellutgifter i New York City, som angir at det per natt ikke kan overstige USD 250.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="1e9a8-107">Hvis en arbeidstaker sender inn en utgiftsrapport for en reiseregning hvor romprisen er større enn dette beløpet, vil systemet varsle arbeidstakeren om at policybeløpet for denne utgiften er overskredet.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="1e9a8-108">Du kan konfigurere meldingen arbeidstakeren mottar når du definerer denne policyen.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="1e9a8-109">Du kan definere tre typer policyer.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="1e9a8-110">Advarsel – Tillater arbeidstakeren å sende inn en utgiftsrapport eller reiseregning, men kostnaden vil markeres for godkjennere</span><span class="sxs-lookup"><span data-stu-id="1e9a8-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="1e9a8-111">for senere rapportering.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-111">for later reporting.</span></span> 
 - <span data-ttu-id="1e9a8-112">Feil – Krever at arbeidstakeren reviderer utgiftene for samsvar med policyen før innsending av utgiftsrapporten elle reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="1e9a8-113">Begrunnelse – Krever at arbeidstakeren eller en leder skal legge inn en begrunnelse for å overskride beløpet før innsending av utgiftsrapport eller reiseregning.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="1e9a8-114">Du kan også sette opp en datoperioden for når utgiftpolicyen er effektiv.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="1e9a8-115">For eksempel kan flyprisene for flyvninger mellom Danmark og New York City være dyre under høysesonger.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="1e9a8-116">Du kan definere en utgiftsregel for flyvninger som begrenser kostanden for flyvninger til New York City til en grense på DKK 5000, og du kan spesifisere at denne regelen skal gjelde mellom 15. mars og 15. september.</span><span class="sxs-lookup"><span data-stu-id="1e9a8-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

