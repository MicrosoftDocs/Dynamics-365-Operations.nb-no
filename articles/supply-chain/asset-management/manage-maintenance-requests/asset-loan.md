---
title: Lån av gjenstander
description: Dette emnet beskriver hvordan du registrerer lån av aktiva i Aktivumbehandling.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8680241b1300aceda3280893982a1eff3d2e09e0
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847488"
---
# <a name="asset-loans"></a><span data-ttu-id="95eff-103">Lån av gjenstander</span><span class="sxs-lookup"><span data-stu-id="95eff-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="95eff-104">Hvis firmaet ditt mottar aktiva for reparasjons- eller vedlikeholdsjobber fra enten interne lokasjoner eller kunder, og hvis du midlertidig låner ut aktiva til de aktuelle stedene eller kundene, kan Aktivumbehandling spore lånet av gjenstander.</span><span class="sxs-lookup"><span data-stu-id="95eff-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="95eff-105">Registrere lån av gjenstander på en vedlikeholdsanmodning</span><span class="sxs-lookup"><span data-stu-id="95eff-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="95eff-106">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlilkeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="95eff-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="95eff-107">Velg vedlikeholdsanmondningen du skal registrere et lån av gjenstander for, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="95eff-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="95eff-108">På **Forespørsel**-siden velger du **Send lån av gjenstander**.</span><span class="sxs-lookup"><span data-stu-id="95eff-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="95eff-109">Velg aktivumet, og angi den forventede returdatoen.</span><span class="sxs-lookup"><span data-stu-id="95eff-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="95eff-110">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="95eff-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="95eff-111">Du kan bare sende et lån av gjenstander hvis et aktivum av samme type er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="95eff-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="95eff-112">Aktivumet du låner ut, må ha en livsløpstilstand som gjør at det kan brukes som et låneaktivum, for eksempel **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="95eff-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="95eff-113">Når lånet av gjenstander er registrert, oppdateres aktivumets livsløpstilstand automatisk til for eksempel **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="95eff-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="95eff-114">Hvis du vil vise en liste over alle aktivumene du har lånt ut til andre lokasjoner eller kunder, velger du **Anleggsmiddelbehandling** \> **Felles** \> **Lån av gjenstander** \> **Alle lån av gjenstander**.</span><span class="sxs-lookup"><span data-stu-id="95eff-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="95eff-115">Hvis det er merket av for **Avsluttet** for et aktivum, er aktivumet registrert som returnert til firmaet.</span><span class="sxs-lookup"><span data-stu-id="95eff-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Figur 1](media/06-manage-maintenance-requests.png)

<span data-ttu-id="95eff-117">På siden **Aktive lån av gjenstander** kan du vise en liste over alle lånegjenstander som ennå ikke er returnert til selskapet.</span><span class="sxs-lookup"><span data-stu-id="95eff-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="95eff-118">Registrer lånegjenstander som returnert</span><span class="sxs-lookup"><span data-stu-id="95eff-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="95eff-119">Velg **Anleggsmiddelbehandling** \> **Felles** \> **Lån av gjenstander** \> **Aktive lån av gjenstander**.</span><span class="sxs-lookup"><span data-stu-id="95eff-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="95eff-120">Velg lånet av gjenstander du vil registrere som returnert, og velg deretter **Returner lån av gjenstander**.</span><span class="sxs-lookup"><span data-stu-id="95eff-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="95eff-121">Angi dato og klokkeslett i feltet **Returnert**.</span><span class="sxs-lookup"><span data-stu-id="95eff-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="95eff-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="95eff-122">Select **OK**.</span></span>
5. <span data-ttu-id="95eff-123">Oppdater listesiden **Aktive lån av gjenstander**, og legg merke til at lånet av gjenstander ikke lenger vises i listen.</span><span class="sxs-lookup"><span data-stu-id="95eff-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
