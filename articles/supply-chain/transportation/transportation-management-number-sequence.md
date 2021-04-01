---
title: Nummerserie for transportstyring
description: Dette emnet beskriver hvordan du definerer nummerserier for transportstyring.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cc19110f481c11ab28532d69a4689c1db048f6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233373"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="2624f-103">Nummerserie for transportstyring</span><span class="sxs-lookup"><span data-stu-id="2624f-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2624f-104">Bruk siden **Nummerserier** i transportstyringsmodulen til å definere ulike pronumre.</span><span class="sxs-lookup"><span data-stu-id="2624f-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="2624f-105">Pronumre brukes av transportører til å organisere og spore fremdriften for hver forsendelse.</span><span class="sxs-lookup"><span data-stu-id="2624f-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="2624f-106">Opprett en nummerserie for et pronummer</span><span class="sxs-lookup"><span data-stu-id="2624f-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="2624f-107">Hvis du vil opprette en nummerserie for et pronummer, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="2624f-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="2624f-108">Gå til **Transportstyring \> Oppsett \> Transportører \> Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="2624f-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="2624f-109">Velg **Ny** for å opprette en ny nummerserie.</span><span class="sxs-lookup"><span data-stu-id="2624f-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="2624f-110">Angi en unik ID og et beskrivende navn for nummerserien.</span><span class="sxs-lookup"><span data-stu-id="2624f-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="2624f-111">I feltet **Nummerserietype** er *Pronummer* det eneste alternativet.</span><span class="sxs-lookup"><span data-stu-id="2624f-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="2624f-112">I feltet **Kontrollsiffer** er *Kontrollsiffer* det eneste alternativet, og det er satt opp som en generell motor.</span><span class="sxs-lookup"><span data-stu-id="2624f-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="2624f-113">Angi informasjon om serien i hurtigfanen **Sekvens**.</span><span class="sxs-lookup"><span data-stu-id="2624f-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="2624f-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2624f-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="2624f-115">Knytte en nummerserie til en transportør</span><span class="sxs-lookup"><span data-stu-id="2624f-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="2624f-116">Hvis du vil knytte en nummerserie til en transportør, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="2624f-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="2624f-117">Gå til **Transportstyring \> Oppsett \> Transpotører \> Transportører**.</span><span class="sxs-lookup"><span data-stu-id="2624f-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="2624f-118">Velg en transportør.</span><span class="sxs-lookup"><span data-stu-id="2624f-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="2624f-119">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="2624f-119">Select **Edit**.</span></span>
1. <span data-ttu-id="2624f-120">I hurtigfanen **Oversikt** velger du et alternativ i feltet **Pronummerserie**.</span><span class="sxs-lookup"><span data-stu-id="2624f-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="2624f-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2624f-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]