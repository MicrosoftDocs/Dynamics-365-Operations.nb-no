---
title: NMFC-koder (National Motor Freight Classification)
description: Dette emnet beskriver hvordan du arbeider med NMFC-koder (National Motor Freight Classification) i Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941888"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="7c82d-103">NMFC-koder (National Motor Freight Classification)</span><span class="sxs-lookup"><span data-stu-id="7c82d-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c82d-104">NMFC-koder (National Motor Freight Classification) hjelper deg med å klassifisere varer som kan sendes.</span><span class="sxs-lookup"><span data-stu-id="7c82d-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="7c82d-105">NMFC-koden er en betegnelse som brukes til å gruppere varer.</span><span class="sxs-lookup"><span data-stu-id="7c82d-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="7c82d-106">På denne måten kan transportfirmaer evaluere varer for forsendelse ved å klassifisere varer basert på hensyn som lastebilegenskaper, lasteproblemer, håndteringsproblemer og forgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="7c82d-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="7c82d-107">Varer grupperes i én av 18 fraktklasser ved hjelp av en rekke tall, fra 50 til 500.</span><span class="sxs-lookup"><span data-stu-id="7c82d-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="7c82d-108">Klassen som en vare grupperes i, er basert på evaluering av fire transportegenskaper: tetthet, oppbevaringsevne, håndtering og skyld.</span><span class="sxs-lookup"><span data-stu-id="7c82d-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="7c82d-109">Til sammen fastsetter disse egenskapene varens transporterbarhet.</span><span class="sxs-lookup"><span data-stu-id="7c82d-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="7c82d-110">En NMFC-kode er tilknyttet alle forsendelsesvarene som er mindre enn vognlastklasser (LTL).</span><span class="sxs-lookup"><span data-stu-id="7c82d-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="7c82d-111">En bærbar datamaskin kan for eksempel være tilordnet en NMFC som er klasse 2.5, mens strømkabler kan være tilordnet en NMFC som er klasse 65.</span><span class="sxs-lookup"><span data-stu-id="7c82d-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="7c82d-112">Denne funksjonen kan hjelpe arbeidere med å bruke NMFC-koder til å klassifisere LTL-forsendelsesvarer.</span><span class="sxs-lookup"><span data-stu-id="7c82d-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="7c82d-113">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="7c82d-113">Here are some examples:</span></span>

- <span data-ttu-id="7c82d-114">Hvis firmaet inneholder en fraktbeskrivelse på fraktbrevet, vil transportøren ha en anelse om hva frakten er.</span><span class="sxs-lookup"><span data-stu-id="7c82d-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="7c82d-115">Frakt er en viktig klassifisering, fordi mange transportfirmaer baserer hele forretningsmodellen på hvilke typer frakt de sender.</span><span class="sxs-lookup"><span data-stu-id="7c82d-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="7c82d-116">Denne klassifiseringen kan være vesentlig for ditt firma fordi den brukes til å avgjøre kostnadene ved en gitt last.</span><span class="sxs-lookup"><span data-stu-id="7c82d-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="7c82d-117">Firmaet kan identifisere lønnsomheten til et LTL-logistikk- og transportfirma.</span><span class="sxs-lookup"><span data-stu-id="7c82d-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="7c82d-118">Dette emnet beskriver hvordan du arbeider med NMFC-koder i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7c82d-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7c82d-119">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7c82d-119">Prerequisites</span></span>

<span data-ttu-id="7c82d-120">Før du kan opprette NMFC-koder må du konfigurere alle LTL-fraktklassene som må tilordnes dem.</span><span class="sxs-lookup"><span data-stu-id="7c82d-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="7c82d-121">LTL-fraktklasser representerer varekategorier, mens NMFC-koder er relatert til bestemte varer i hver av de 18 fraktklassene.</span><span class="sxs-lookup"><span data-stu-id="7c82d-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="7c82d-122">Hvis du vil ha mer informasjon om hvordan du arbeider med LTL-klasser, kan du se [Mindre enn vognlastklasser](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="7c82d-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="7c82d-123">Opprette en NMFC-kode</span><span class="sxs-lookup"><span data-stu-id="7c82d-123">Create an NMFC code</span></span>

<span data-ttu-id="7c82d-124">Hvis du vil opprette en NMFC-kode, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="7c82d-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="7c82d-125">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="7c82d-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="7c82d-126">Gå til **Lagerstyring \> Oppsett \> Lager \> NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="7c82d-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="7c82d-127">Gå til **Transportstyring \> Oppsett \> Transportstandarder \> NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="7c82d-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="7c82d-128">Velg **Ny** for å opprette en NMFC-kode.</span><span class="sxs-lookup"><span data-stu-id="7c82d-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="7c82d-129">Deretter angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="7c82d-129">Then set the following fields:</span></span>

    - <span data-ttu-id="7c82d-130">**NMFC-kode** – Angi NMFC-koden for varetypen.</span><span class="sxs-lookup"><span data-stu-id="7c82d-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="7c82d-131">**Navn** – Angi et navn for NMFC-koden.</span><span class="sxs-lookup"><span data-stu-id="7c82d-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="7c82d-132">**LTL-klasse** – Velg LTL-klassen som er knyttet til NMFC-koden.</span><span class="sxs-lookup"><span data-stu-id="7c82d-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="7c82d-133">**BOL-håndteringsenhet** – Definer standard håndteringstype for forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="7c82d-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="7c82d-134">Eksempel: Definer NMFC-koder</span><span class="sxs-lookup"><span data-stu-id="7c82d-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="7c82d-135">Følgende eksempel viser hvordan du konfigurerer to ulike NMFC-koder som du kan brukes med forskjellige produkter.</span><span class="sxs-lookup"><span data-stu-id="7c82d-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="7c82d-136">Gå til **Lagerstyring \> Oppsett \> Lager \> NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="7c82d-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="7c82d-137">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7c82d-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7c82d-138">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="7c82d-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7c82d-139">**NMFC-kode:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="7c82d-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="7c82d-140">**Navn:** *Datamaskiner*</span><span class="sxs-lookup"><span data-stu-id="7c82d-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="7c82d-141">**LTL-klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="7c82d-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="7c82d-142">**BOL-håndteringsenhet:** *Enhet*</span><span class="sxs-lookup"><span data-stu-id="7c82d-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="7c82d-143">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7c82d-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="7c82d-144">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7c82d-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="7c82d-145">På den nye linjen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="7c82d-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="7c82d-146">**NMFC-kode:** *125*</span><span class="sxs-lookup"><span data-stu-id="7c82d-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="7c82d-147">**Navn:** *Telefoner*</span><span class="sxs-lookup"><span data-stu-id="7c82d-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="7c82d-148">**LTL-klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="7c82d-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="7c82d-149">**BOL-håndteringsenhet:** *Enhet*</span><span class="sxs-lookup"><span data-stu-id="7c82d-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="7c82d-150">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7c82d-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c82d-151">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7c82d-151">Additional resources</span></span>

- [<span data-ttu-id="7c82d-152">Mindre enn vognlastklasser</span><span class="sxs-lookup"><span data-stu-id="7c82d-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="7c82d-153">Opprette et fraktbrev</span><span class="sxs-lookup"><span data-stu-id="7c82d-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
