---
title: Vareprøve for kvalitetsstyring
description: Dette emnet beskriver hvordan du setter opp vareprøver.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022234"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="bde6f-103">Vareprøve for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="bde6f-103">Quality management item sampling</span></span>

<span data-ttu-id="bde6f-104">Vareprøve brukes som del av en kvalitetskontroll.</span><span class="sxs-lookup"><span data-stu-id="bde6f-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="bde6f-105">Den definerer mengden gjeldende fysisk lager som må kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="bde6f-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="bde6f-106">Prøver kan være basert på faste antall, en prosentdel, eller et fullstendig nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="bde6f-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="bde6f-107">Definere vareprøver</span><span class="sxs-lookup"><span data-stu-id="bde6f-107">Set up item sampling</span></span>

<span data-ttu-id="bde6f-108">Gjør følgende for å konfigurere vareprøve.</span><span class="sxs-lookup"><span data-stu-id="bde6f-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="bde6f-109">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Vareprøve**.</span><span class="sxs-lookup"><span data-stu-id="bde6f-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="bde6f-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bde6f-110">Select **New**.</span></span>
1. <span data-ttu-id="bde6f-111">Skriv inn en verdi i **Vareprøve**-feltet.</span><span class="sxs-lookup"><span data-stu-id="bde6f-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="bde6f-112">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="bde6f-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="bde6f-113">Angi et tall i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="bde6f-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="bde6f-114">Denne verdien er knyttet til spesifikasjonen av antall som er valgt i feltet ved siden av.</span><span class="sxs-lookup"><span data-stu-id="bde6f-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="bde6f-115">I **Prosess**-delen merker du av for **Full blokkering** hvis hele partiet eller ordrelinjeantallet skal blokkeres hvis en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="bde6f-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="bde6f-116">Hvis du fjerner merket i boksen, blokkeres bare varene i kvalitetsordren hvis en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="bde6f-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="bde6f-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bde6f-117">Select **Save**.</span></span>
1. <span data-ttu-id="bde6f-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bde6f-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="bde6f-119">Funksjonen *Kvalitetsstyring for lagerprosesser* gir flere vareprøvefunksjoner.</span><span class="sxs-lookup"><span data-stu-id="bde6f-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="bde6f-120">Den legger til begrepet *vareprøveområde* og muligheten til å definere et fullstendig nummerskilt som spesifikasjon av antall.</span><span class="sxs-lookup"><span data-stu-id="bde6f-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="bde6f-121">Hvis du har aktivert denne funksjonen, se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="bde6f-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
