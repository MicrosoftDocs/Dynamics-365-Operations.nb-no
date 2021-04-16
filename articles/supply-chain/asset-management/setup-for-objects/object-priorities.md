---
title: Tjenestenivåer for aktiva
description: Dette emnet beskriver tjenestenivåer for aktiva i Aktivastyring.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4163d059fda4ae0120d5c989e744c5a5fe0f5892
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808302"
---
# <a name="asset-service-levels"></a><span data-ttu-id="4b593-103">Tjenestenivåer for aktiva</span><span class="sxs-lookup"><span data-stu-id="4b593-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4b593-104">Dette emnet beskriver tjenestenivåer for aktiva i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="4b593-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="4b593-105">Tjenestenivåer for aktiva er knyttet til aktiva og overføres til meldinger og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="4b593-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="4b593-106">De brukes til å beregne prioriteten for arbeidsordrer under planlegging av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="4b593-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="4b593-107">Servicenivåer for aktiva kan endres hvis det er nødvendig med endringer.</span><span class="sxs-lookup"><span data-stu-id="4b593-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="4b593-108">Hvis du vil ha mer informasjon om oppsettet som er knyttet til beregning av poengsummer for arbeidsordreplanlegging, kan du se [Parametere i Aktivastyring](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4b593-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="4b593-109">Du må definere minst én standardpost for servicenivået for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="4b593-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="4b593-110">Denne standardposten brukes hvis ingen andre treff blir funnet under planleggingen av arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="4b593-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="4b593-111">**Eksempel 1:** Standard tjenestenivå som brukes hvis ingen andre treff blir funnet.</span><span class="sxs-lookup"><span data-stu-id="4b593-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="4b593-112">I denne oppføringen velger du bare et tjenestenivå.</span><span class="sxs-lookup"><span data-stu-id="4b593-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="4b593-113">**Eksempel 2:** Et høyt servicenivå som brukes til å planlegge jobber for en Volvo-lastebilmotor.</span><span class="sxs-lookup"><span data-stu-id="4b593-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="4b593-114">I denne oppføringen velger du en relevant aktivatype (for eksempel **Lastebilmotor**), en produsent (**Volvo**) og et servicenivå.</span><span class="sxs-lookup"><span data-stu-id="4b593-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="4b593-115">Definere tjenestenivåer for aktiva</span><span class="sxs-lookup"><span data-stu-id="4b593-115">Set up asset service levels</span></span>

1. <span data-ttu-id="4b593-116">Velg **Aktivastyring** \> **Oppset** \> **Tjenestenivåer for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="4b593-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="4b593-117">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="4b593-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="4b593-118">Avhengig av detaljnivået som kreves for tjenestenivået for aktiva, kan du foreta relevante valg i feltene **Arbeidssted**, **Aktivatype**, **Produsent**, **Modell**, **Aktivum**, **Arbeidsordretype** og **Tjenestenivå**.</span><span class="sxs-lookup"><span data-stu-id="4b593-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4b593-119">Når servicenivået for aktiva brukes til meldinger og arbeidsordrer, går Aktivastyring gjennom alle poster på servicenivå for aktiva for å kontrollere om det finnes et mulig samsvar.</span><span class="sxs-lookup"><span data-stu-id="4b593-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="4b593-120">Den kontrollerer alltid den mest spesifikke kombinasjonen først.</span><span class="sxs-lookup"><span data-stu-id="4b593-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="4b593-121">Med andre ord ser Aktivastyring først etter et treff i **Arbeidsordretype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b593-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="4b593-122">Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Aktivum**-feltet, og så videre.</span><span class="sxs-lookup"><span data-stu-id="4b593-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="4b593-123">Som du kan se i oppsettet av siden **Tjenestenivåer for aktiva**, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff.</span><span class="sxs-lookup"><span data-stu-id="4b593-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="4b593-124">Hvis det ikke blir funnet noen treff, brukes standardoppføringen, der det ikke er noen valg i disse feltene.</span><span class="sxs-lookup"><span data-stu-id="4b593-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="4b593-125">I feltet **Servicenivå** velger du et tall som angir servicenivået (prioriteten).</span><span class="sxs-lookup"><span data-stu-id="4b593-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="4b593-126">Hvis du endrer en post for servicenivå for aktiva på siden **Servicenivåer for aktiva** etter at du allerede har brukt den på en arbeidsordre, oppdateres ikke servicenivået på meldinger og arbeidsordrer i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="4b593-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]