---
title: Vareprøve for kvalitetsstyring
description: Dette emnet beskriver hvordan du setter opp vareprøver.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956767"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="35ec1-103">Vareprøve for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="35ec1-103">Quality management item sampling</span></span>

<span data-ttu-id="35ec1-104">Vareprøve brukes som del av en kvalitetskontroll.</span><span class="sxs-lookup"><span data-stu-id="35ec1-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="35ec1-105">Den definerer mengden gjeldende fysisk lager som må kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="35ec1-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="35ec1-106">Prøver kan være basert på faste antall, en prosentdel, eller et fullstendig nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="35ec1-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="35ec1-107">Definere vareprøver</span><span class="sxs-lookup"><span data-stu-id="35ec1-107">Set up item sampling</span></span>

<span data-ttu-id="35ec1-108">Gjør følgende for å konfigurere vareprøve.</span><span class="sxs-lookup"><span data-stu-id="35ec1-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="35ec1-109">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="35ec1-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="35ec1-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="35ec1-110">Select **New**.</span></span>
1. <span data-ttu-id="35ec1-111">Skriv inn en verdi i **Vareprøve**-feltet.</span><span class="sxs-lookup"><span data-stu-id="35ec1-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="35ec1-112">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="35ec1-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="35ec1-113">Angi et tall i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="35ec1-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="35ec1-114">Denne verdien er knyttet til spesifikasjonen av antall som er valgt i feltet ved siden av.</span><span class="sxs-lookup"><span data-stu-id="35ec1-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="35ec1-115">I **Prosess**-delen merker du av for **Full blokkering** hvis hele partiet eller ordrelinjeantallet skal blokkeres hvis en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="35ec1-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="35ec1-116">Hvis du fjerner merket i boksen, blokkeres bare varene i kvalitetsordren hvis en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="35ec1-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="35ec1-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="35ec1-117">Select **Save**.</span></span>
1. <span data-ttu-id="35ec1-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="35ec1-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="35ec1-119">Funksjonen *Kvalitetsstyring for lagerprosesser* gir flere vareprøvefunksjoner.</span><span class="sxs-lookup"><span data-stu-id="35ec1-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="35ec1-120">Den legger til begrepet *vareprøveområde* og muligheten til å definere et fullstendig nummerskilt som spesifikasjon av antall.</span><span class="sxs-lookup"><span data-stu-id="35ec1-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="35ec1-121">Hvis du har aktivert denne funksjonen, se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="35ec1-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
