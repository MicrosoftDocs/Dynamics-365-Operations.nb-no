---
title: Hovedplanlegging genererer planlagte bestillinger for fantomprodukter
description: Planlagte ordrer genereres for fantomprodukter etter hovedplanlegging kjøres.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026786"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="0e7b3-103">Hovedplanlegging genererer planlagte bestillinger for fantomprodukter</span><span class="sxs-lookup"><span data-stu-id="0e7b3-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="0e7b3-104">KB-nummer: 4614729</span><span class="sxs-lookup"><span data-stu-id="0e7b3-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="0e7b3-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="0e7b3-105">Symptoms</span></span>

<span data-ttu-id="0e7b3-106">Planlagte ordrer genereres for fantomprodukter etter hovedplanlegging kjøres.</span><span class="sxs-lookup"><span data-stu-id="0e7b3-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="0e7b3-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="0e7b3-107">Resolution</span></span>

<span data-ttu-id="0e7b3-108">Innstillingen for **Fantom**-alternativet for frigitte produkter bestemmer standard linjetype i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="0e7b3-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="0e7b3-109">Hvis **Fantom**-alternativet er satt til *Ja*, vil systemet fremdeles opprette planlagte bestillinger for varen, men alternativet for **Direkte avledet behov** for hver planlagte bestilling blir satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="0e7b3-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="0e7b3-110">Derfor kan ikke den planlagte produksjonsordren autoriseres på egen hånd.</span><span class="sxs-lookup"><span data-stu-id="0e7b3-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="0e7b3-111">I stedet inkluderes den alltid automatisk når den overordnede produksjonsordren autoriseres.</span><span class="sxs-lookup"><span data-stu-id="0e7b3-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="0e7b3-112">I tillegg blir stykklistelinjene til den planlagte fantomordren tatt med i stykklisten til den overordnede produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="0e7b3-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
