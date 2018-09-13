--- 
title: "Konfigurere alle nødvendige nummerserier ved å bruke en veiviser"
description: "Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem."
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abd59b96a2e5dceb2492c2db2c617485b332fbd3
ms.openlocfilehash: 1808ab9240ab291f9d203893a634bd390f16e2e7
ms.contentlocale: nb-no
ms.lasthandoff: 09/13/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="20532-103">Konfigurere alle nødvendige nummerserier ved å bruke en veiviser</span><span class="sxs-lookup"><span data-stu-id="20532-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20532-104">Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem.</span><span class="sxs-lookup"><span data-stu-id="20532-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="20532-105">En hoveddata- eller transaksjonspost som krever en ID kalles en referanse.</span><span class="sxs-lookup"><span data-stu-id="20532-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="20532-106">Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse.</span><span class="sxs-lookup"><span data-stu-id="20532-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="20532-107">Denne fremgangsmåten beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser.</span><span class="sxs-lookup"><span data-stu-id="20532-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="20532-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="20532-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="20532-109">Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="20532-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="20532-110">Klikk Generer.</span><span class="sxs-lookup"><span data-stu-id="20532-110">Click Generate.</span></span>
3. <span data-ttu-id="20532-111">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="20532-111">Click Next.</span></span>
    * <span data-ttu-id="20532-112">På denne siden kan du endre ID-koden, den laveste verdien og den høyeste verdien.</span><span class="sxs-lookup"><span data-stu-id="20532-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="20532-113">Du kan i tillegg angi om nummerserien må være sammenhengende.</span><span class="sxs-lookup"><span data-stu-id="20532-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="20532-114">Ikke velg Fortløpende-alternativet hvis du må forhåndstildele numre for nummerserien.</span><span class="sxs-lookup"><span data-stu-id="20532-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="20532-115">Hvis du vil legge til et omfangssegment for formatet for en nummerserie, velger du formatet i listen og klikker deretter Ta med omfang i format.</span><span class="sxs-lookup"><span data-stu-id="20532-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="20532-116">Hvis du vil fjerne et omfangssegment fra formatet for en nummerserie, velger du formatet i listen og klikker deretter Fjern omfang fra format.</span><span class="sxs-lookup"><span data-stu-id="20532-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="20532-117">Hvis du vil utelukke en nummerserie fra automatisk generering, velger du nummerserien i listen og klikker deretter Slett.</span><span class="sxs-lookup"><span data-stu-id="20532-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="20532-118">Klikk Neste.</span><span class="sxs-lookup"><span data-stu-id="20532-118">Click Next.</span></span>
5. <span data-ttu-id="20532-119">Klikk Finish.</span><span class="sxs-lookup"><span data-stu-id="20532-119">Click Finish.</span></span>


