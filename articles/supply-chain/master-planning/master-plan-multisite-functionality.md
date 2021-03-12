---
title: Oversikt over hovedplanlegging og multisite-funksjonalitet
description: Hovedplanlegging tar hensyn til innstillingene for område- og lagerdimensjonene.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c42fbd42288a072803e4f5de46560d13129515db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005158"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="b3704-103">Oversikt over hovedplanlegging og multisite-funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="b3704-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3704-104">Hovedplanlegging tar hensyn til innstillingene for område- og lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="b3704-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="b3704-105">Områdedimensjonen er obligatorisk, og du må angi at lagerdimensjonen er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b3704-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="b3704-106">Når en dimensjon er obligatorisk, må du angi en dimensjonsverdi for alle lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="b3704-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="b3704-107">I hovedplanleggingen er derfor området og lageret for det opprinnelige behovet kjent.</span><span class="sxs-lookup"><span data-stu-id="b3704-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="b3704-108">Områdedimensjonen er også konsekvent slik at stedsverdien ikke endres i løpet av nedbrytingen av lavnivåbehov.</span><span class="sxs-lookup"><span data-stu-id="b3704-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="b3704-109">Når lageret ikke er satt til obligatorisk, kan det være at det ikke er kjent fra det opprinnelige behovet.</span><span class="sxs-lookup"><span data-stu-id="b3704-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="b3704-110">Planleggingsmotoren må bestemme hvilket lager som skal brukes, basert på innstillingene som er angitt for varen, individuelle lagre og detaljene i ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="b3704-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="b3704-111">Følgende emner beskriver hvordan planleggingsmotoren fungerer når forskjellige innstillinger er definert for å bestemme hvilket lager som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="b3704-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="b3704-112">Hovedplanlegging for område- og lagerdekning, lager obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3704-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b3704-113">Hovedplanlegging for områdedekning, obligatorisk lager</span><span class="sxs-lookup"><span data-stu-id="b3704-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b3704-114">Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3704-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b3704-115">Hovedplanlegging for områdedekning, lager ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3704-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b3704-116">Fastslå stykklisteversjonen</span><span class="sxs-lookup"><span data-stu-id="b3704-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



