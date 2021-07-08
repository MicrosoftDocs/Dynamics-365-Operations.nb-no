---
title: Leverandørkode er ikke autorisert for et bestemt produkt og en bestemt dato
description: Når du prøver å autorisere en planlagt bestilling eller legge til en linje i en bestilling, får du en feilmelding som angir at leverandørkoden ikke har autorisasjon for et produkt og en dato.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294149"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="45bd6-103">Leverandørkode er ikke autorisert for et bestemt produkt og en bestemt dato</span><span class="sxs-lookup"><span data-stu-id="45bd6-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="45bd6-104">Feilkode: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="45bd6-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="45bd6-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="45bd6-105">Symptoms</span></span>

<span data-ttu-id="45bd6-106">Når du prøver å autorisere en planlagt ordre eller legge til en linje i bestillingen, mottar du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="45bd6-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="45bd6-107">Leverandørkoden %1 er ikke autorisert for %2 på %3.</span><span class="sxs-lookup"><span data-stu-id="45bd6-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="45bd6-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="45bd6-108">Cause</span></span>

<span data-ttu-id="45bd6-109">Feilen oppstår fordi feltet **Godkjent leverandørkontrollmetode** er satt til *Bare advarsel* eller *Ikke tillatt* for det angitte produktet, og leverandøren har i øyeblikket ikke tillatelse til å levere dette produktet.</span><span class="sxs-lookup"><span data-stu-id="45bd6-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="45bd6-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="45bd6-110">Resolution</span></span>

<span data-ttu-id="45bd6-111">Hvis du vil korrigere dette problemet, kan du enten deaktivere leverandørsjekken for det aktuelle produktet eller godkjenne leverandøren.</span><span class="sxs-lookup"><span data-stu-id="45bd6-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="45bd6-112">Følg denne fremgangsmåten for å deaktivere leverandørsjekken for et produkt.</span><span class="sxs-lookup"><span data-stu-id="45bd6-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="45bd6-113">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="45bd6-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="45bd6-114">Åpne det relevante produktet.</span><span class="sxs-lookup"><span data-stu-id="45bd6-114">Open the relevant product.</span></span>
1. <span data-ttu-id="45bd6-115">I hurtigfanen **Kjøp** setter du feltet **Godkjent leverandørkontrollmetode** til en annen verdi enn *Bare advarsel* eller *Ikke tillatt*.</span><span class="sxs-lookup"><span data-stu-id="45bd6-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="45bd6-116">Følg denne fremgangsmåten for å godkjenne en leverandør for et produkt.</span><span class="sxs-lookup"><span data-stu-id="45bd6-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="45bd6-117">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="45bd6-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="45bd6-118">Åpne det relevante elementet.</span><span class="sxs-lookup"><span data-stu-id="45bd6-118">Open the relevant item.</span></span>
1. <span data-ttu-id="45bd6-119">I handlingsruten i fanen **Kjøp** i gruppen **Godkjent leverandør** velger du **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="45bd6-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="45bd6-120">På listesiden **Godkjent leverandør** legger du til en rad i rutenettet, og angi deretter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="45bd6-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="45bd6-121">**Leverandør** – Velg leverandøren som skal godkjenne for gjeldende produkt.</span><span class="sxs-lookup"><span data-stu-id="45bd6-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="45bd6-122">**Ikrafttredelsesdato** – Velg den første datoen som leverandøren er godkjent for.</span><span class="sxs-lookup"><span data-stu-id="45bd6-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="45bd6-123">**Utløpsdato** – Velg den siste datoen som leverandøren er godkjent for.</span><span class="sxs-lookup"><span data-stu-id="45bd6-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="45bd6-124">Hvis du vil ha mer informasjon, kan du se [Godkjenne leverandører for spesifikke produkter](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="45bd6-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
