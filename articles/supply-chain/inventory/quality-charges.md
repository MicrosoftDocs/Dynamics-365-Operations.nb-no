---
title: Tillegg for avviksoperasjoner
description: Dette emnet beskriver hvordan du oppretter kvalitetsgebyrer som kan brukes sammen med operasjoner for et avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956772"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="0c8ac-103">Tillegg for avviksoperasjoner</span><span class="sxs-lookup"><span data-stu-id="0c8ac-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c8ac-104">Dette emnet beskriver hvordan du oppretter kvalitetsgebyrer som kan brukes sammen med operasjoner for et avvik.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="0c8ac-105">Du bruker siden **Kvalitetsstyringstillegg** til å definere typene tillegg som kan legges til i operasjoner for et avvik.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="0c8ac-106">Med tillegg kan du spore detaljer om gebyrer eller tillegg som du skylder en kunde for produkter med avvik, eller som en leverandør skylder deg for produkter med avvik som du har mottatt.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="0c8ac-107">Du kan også bruke tillegg til å spore kostnader som kreves for at eksterne leverandører eller tjenester kan utføre en operasjon.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="0c8ac-108">Eksempler på kvalitetsgebyrer</span><span class="sxs-lookup"><span data-stu-id="0c8ac-108">Examples of quality charges</span></span>

<span data-ttu-id="0c8ac-109">Du jobber for et produksjonsfirma.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-109">You work for a manufacturing company.</span></span> <span data-ttu-id="0c8ac-110">Firmaet har kontrakter med flere leverandører.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="0c8ac-111">Disse kontraktene beskriver standarder for forsendelser i tide, skader og produktkvalitet for varer.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="0c8ac-112">På samme måte har flere av kundene dine avtaler med firmaet om returer, skade og produktkvalitet.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="0c8ac-113">Det defineres og angis en gebyrstruktur for hvert tilfelle i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="0c8ac-114">Du kan konfigurere kvalitetstillegg for å vise de ulike typene tillegg, for eksempel *Skader*, *Forsinket levering* og *Kvalitet*.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="0c8ac-115">Når du deretter oppretter et avvik, legger du til én eller flere operasjoner.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="0c8ac-116">For hver operasjon velger du **Tillegg** for å definere detaljene for gebyrene.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="0c8ac-117">Opprette et kvalitetstillegg</span><span class="sxs-lookup"><span data-stu-id="0c8ac-117">Create a quality charge</span></span>

1. <span data-ttu-id="0c8ac-118">Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Kvalitetsstyringstillegg**.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="0c8ac-119">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="0c8ac-120">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="0c8ac-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="0c8ac-121">**Tilleggskode** – Angi en unik ID eller et navn for kvalitetstillegget.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="0c8ac-122">**Beskrivelse** – Angi en detaljert beskrivelse av kvalitetstillegget.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="0c8ac-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c8ac-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="0c8ac-124">Legge til et kvalitetstillegg i en operasjon for et avvik</span><span class="sxs-lookup"><span data-stu-id="0c8ac-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="0c8ac-125">Hvis du vil ha mer informasjon om hvordan du legger til operasjoner i et avvik og beregner tillegg for dem, kan du se [Operasjoner for avvik](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="0c8ac-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c8ac-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0c8ac-126">Additional resources</span></span>

- [<span data-ttu-id="0c8ac-127">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="0c8ac-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="0c8ac-128">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="0c8ac-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="0c8ac-129">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="0c8ac-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="0c8ac-130">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="0c8ac-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="0c8ac-131">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="0c8ac-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="0c8ac-132">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="0c8ac-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="0c8ac-133">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="0c8ac-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="0c8ac-134">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="0c8ac-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
