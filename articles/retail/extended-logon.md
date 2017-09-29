---
title: "Definere utvidet påloggingsfunksjonalitet for Skysalgssted og MPOS"
description: "Dette emnet dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="e2958-103">Definere utvidet påloggingsfunksjonalitet for Skysalgssted og MPOS</span><span class="sxs-lookup"><span data-stu-id="e2958-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e2958-104">Dette emnet dekker alternativene for å definere utvidet pålogging for skyesalgssted og moderne salgssted for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="e2958-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

<a name="setting-up-extended-logon"></a><span data-ttu-id="e2958-105">Definere utvidet pålogging</span><span class="sxs-lookup"><span data-stu-id="e2958-105">Setting up extended logon</span></span>
=========================

<span data-ttu-id="e2958-106">Du kan finne oppsettet for strekkodemasker på **Retail** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Funksjonalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="e2958-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="e2958-107">Hurtigkategorien **Funksjoner** inneholder følgende alternativer som er knyttet til utvidet pålogging.</span><span class="sxs-lookup"><span data-stu-id="e2958-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="e2958-108">Strekkodepålogging for stab</span><span class="sxs-lookup"><span data-stu-id="e2958-108">Staff bar code logon</span></span>

<span data-ttu-id="e2958-109">Når alternativet **Strekkodepålogging for stab** er aktivert, kan arbeidere som har en utvidet pålogging tilordnet til legitimasjon for salgssted, logge på ved hjelp av en strekkode.</span><span class="sxs-lookup"><span data-stu-id="e2958-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="e2958-110">Stabspålogging med strekkode krever passord</span><span class="sxs-lookup"><span data-stu-id="e2958-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="e2958-111">Når alternativet **Stabspålogging med strekkode krever passord** er aktivert, velger stabspålogging med strekkode bare arbeideren som er tilordnet til den utvidede påloggingen som vises.</span><span class="sxs-lookup"><span data-stu-id="e2958-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="e2958-112">Arbeidere må fremdeles angi passord når dette alternativet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="e2958-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="e2958-113">Kortpålogging for stab</span><span class="sxs-lookup"><span data-stu-id="e2958-113">Staff card logon</span></span>

<span data-ttu-id="e2958-114">Når alternativet **Kortpålogging for stab** er aktivert, kan arbeidere som har en utvidet pålogging tilordnet til legitimasjon for salgssted, logge på ved hjelp av en kortleser.</span><span class="sxs-lookup"><span data-stu-id="e2958-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="e2958-115">Stabspålogging med kort krever passord</span><span class="sxs-lookup"><span data-stu-id="e2958-115">Staff card logon requires password</span></span>

<span data-ttu-id="e2958-116">Når alternativet **Stabspålogging med kort krever passord** er aktivert, velger stabspålogging med kort bare arbeideren som er tilordnet til den utvidede påloggingen som vises.</span><span class="sxs-lookup"><span data-stu-id="e2958-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="e2958-117">Arbeidere må fremdeles angi passord når dette alternativet er aktivert.</span><span class="sxs-lookup"><span data-stu-id="e2958-117">Workers must still enter their password when this option is enabled.</span></span>

<a name="assigning-an-extended-logon"></a><span data-ttu-id="e2958-118">Tilordne en utvidet pålogging</span><span class="sxs-lookup"><span data-stu-id="e2958-118">Assigning an extended logon</span></span>
===========================

<span data-ttu-id="e2958-119">Som standard kan bare ledere tilordne utvidet pålogging til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="e2958-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="e2958-120">Hvis du vil tilordne utvidet pålogging, kan du gå til **Utvidet pålogging** i POS.</span><span class="sxs-lookup"><span data-stu-id="e2958-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="e2958-121">Søk deretter etter en arbeider ved å angi hans eller hennes operatør-ID i søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="e2958-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="e2958-122">Velg arbeideren, og klikk deretter **Tilordne**.</span><span class="sxs-lookup"><span data-stu-id="e2958-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="e2958-123">Dra eller skann utvidet pålogging for å tilordne arbeideren på neste side.</span><span class="sxs-lookup"><span data-stu-id="e2958-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="e2958-124">Hvis dra eller skanning blir lest, blir **OK**-knappen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e2958-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="e2958-125">Klikk **OK** for å lagre den utvidede påloggingen for denne arbeideren.</span><span class="sxs-lookup"><span data-stu-id="e2958-125">Click **OK** to save the extended logon for that worker.</span></span>

<a name="deleting-an-extended-logon"></a><span data-ttu-id="e2958-126">Slette en utvidet pålogging</span><span class="sxs-lookup"><span data-stu-id="e2958-126">Deleting an extended logon</span></span>
==========================

<span data-ttu-id="e2958-127">Du kan slette den utvidede påloggingen som er tilordnet til en arbeider, ved å søke etter arbeideren ved hjelp av **Utvidet pålogging** operasjonen.</span><span class="sxs-lookup"><span data-stu-id="e2958-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="e2958-128">Velg arbeideren, og klikk deretter **Ikke tilordnet**.</span><span class="sxs-lookup"><span data-stu-id="e2958-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="e2958-129">All utvidet påloggingslegitimasjon som er knyttet til denne arbeider fjernes.</span><span class="sxs-lookup"><span data-stu-id="e2958-129">All extended logon credentials that are associated with that worker are removed.</span></span>

<a name="extending-extended-logon"></a><span data-ttu-id="e2958-130">Utvide utvidet pålogging</span><span class="sxs-lookup"><span data-stu-id="e2958-130">Extending extended logon</span></span>
========================

<span data-ttu-id="e2958-131">Påloggingstjenesten kan utvides for å støtte flere utvidede påloggingsenheter, for eksempel håndholdte skannere.</span><span class="sxs-lookup"><span data-stu-id="e2958-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="e2958-132">Hvis du vil ha mer informasjon, kan du se i dokumentasjonen for utvidelsesmuligheter for salgssted.</span><span class="sxs-lookup"><span data-stu-id="e2958-132">For more information, see the POS extensibility documentation.</span></span>

<a name="using-extended-logon"></a><span data-ttu-id="e2958-133">Bruke utvidet pålogging</span><span class="sxs-lookup"><span data-stu-id="e2958-133">Using extended logon</span></span>
====================

<span data-ttu-id="e2958-134">Når utvidet pålogging er konfigurert, og en arbeider er tilordnet til en strekkode eller magnetstripe, trenger arbeideren bare å dra eller skanne hans eller hennes kort mens Salgsstedets påloggingsside vises.</span><span class="sxs-lookup"><span data-stu-id="e2958-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="e2958-135">Hvis et passord kreves også før pålogging kan fortsette, blir arbeideren bedt om å angi passordet sitt.</span><span class="sxs-lookup"><span data-stu-id="e2958-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>




