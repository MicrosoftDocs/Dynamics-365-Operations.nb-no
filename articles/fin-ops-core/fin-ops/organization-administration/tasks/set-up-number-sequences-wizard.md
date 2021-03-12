---
title: Konfigurere alle nødvendige nummerserier ved hjelp av en veiviser
description: Dette emnet beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684983d1ea54264cc378ded8e9dca3cf9ec2c901
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2020
ms.locfileid: "4799038"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="85035-103">Konfigurere alle nødvendige nummerserier ved hjelp av en veiviser</span><span class="sxs-lookup"><span data-stu-id="85035-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85035-104">Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem.</span><span class="sxs-lookup"><span data-stu-id="85035-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="85035-105">En hoveddata- eller transaksjonspost som krever en ID kalles en referanse.</span><span class="sxs-lookup"><span data-stu-id="85035-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="85035-106">Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse.</span><span class="sxs-lookup"><span data-stu-id="85035-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="85035-107">Dette emnet beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser.</span><span class="sxs-lookup"><span data-stu-id="85035-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="85035-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="85035-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="85035-109">Gå til **Navigasjon > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="85035-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="85035-110">Velg **Generer**.</span><span class="sxs-lookup"><span data-stu-id="85035-110">Select **Generate**.</span></span>
3. <span data-ttu-id="85035-111">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="85035-111">Select **Next**.</span></span>

   - <span data-ttu-id="85035-112">På denne siden kan du endre ID-koden, den laveste verdien og den høyeste verdien.</span><span class="sxs-lookup"><span data-stu-id="85035-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="85035-113">Du kan i tillegg angi om nummerserien må være sammenhengende.</span><span class="sxs-lookup"><span data-stu-id="85035-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="85035-114">Ikke velg **Fortløpende**-alternativet hvis du må forhåndstildele numre for nummerserien.</span><span class="sxs-lookup"><span data-stu-id="85035-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="85035-115">Hvis du vil legge til et omfangssegment for formatet for en nummerserie, velger du formatet i listen og velger deretter **Ta med omfang i format**.</span><span class="sxs-lookup"><span data-stu-id="85035-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="85035-116">Hvis du vil fjerne et omfangssegment fra formatet for en nummerserie, velger du formatet i listen og velger deretter **Fjern omfang fra format**.</span><span class="sxs-lookup"><span data-stu-id="85035-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="85035-117">Hvis du vil utelukke en nummerserie fra automatisk generering, velger du nummerserien i listen og velger deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="85035-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="85035-118">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="85035-118">Select **Next**.</span></span>
5. <span data-ttu-id="85035-119">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="85035-119">Select **Finish**.</span></span>

