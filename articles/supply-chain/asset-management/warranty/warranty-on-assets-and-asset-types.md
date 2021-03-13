---
title: Garantier for eiendeler og anleggsmiddeltyper
description: Dette emnet forklarer hvordan du definerer garantier for aktiva og aktivatyper i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c0359bfe31b3d01f28028bb17d5d30af39a1db9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021610"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="e0b18-103">Garantier for eiendeler og anleggsmiddeltyper</span><span class="sxs-lookup"><span data-stu-id="e0b18-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e0b18-104">Dette emnet forklarer hvordan du definerer garantier for aktiva og aktivatyper i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="e0b18-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="e0b18-105">Definere en garanti for en aktivatype</span><span class="sxs-lookup"><span data-stu-id="e0b18-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="e0b18-106">Velg **Aktivastyring** \> **Oppsett** \> **Aktivatyper** \> **Aktivatyper**.</span><span class="sxs-lookup"><span data-stu-id="e0b18-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="e0b18-107">I venstre rute velger du anleggsmiddeltypen du vil knytte en leverandørgarantiavtale til, og deretter velger du **Standarder for aktivatype**.</span><span class="sxs-lookup"><span data-stu-id="e0b18-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="e0b18-108">Velg avtalen i **Leverandørgaranti**-feltet på hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="e0b18-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="e0b18-109">Definere en garanti for et aktivum</span><span class="sxs-lookup"><span data-stu-id="e0b18-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="e0b18-110">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="e0b18-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="e0b18-111">Velg anleggsmidlet, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e0b18-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="e0b18-112">I hurtigfanen **Leverandør** i delen **Leverandørgaranti**, i feltet **Garanti**, velger du garantiavtalen.</span><span class="sxs-lookup"><span data-stu-id="e0b18-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="e0b18-113">Velg start- og sluttdatoer i feltene **Garantistart** og **Garantislutt**.</span><span class="sxs-lookup"><span data-stu-id="e0b18-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e0b18-114">Hvis en dato er valgt i **Garantistart**-feltet i en arbeidsordre, blir garantien gyldig for arbeidsordren på denne datoen.</span><span class="sxs-lookup"><span data-stu-id="e0b18-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="e0b18-115">Når du oppretter en arbeidsordre, settes **Garantistart**-feltet automatisk til opprettelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="e0b18-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="e0b18-116">Du kan imidlertid endre datoen slik at den tilsvarer for eksempel startdatoen for en garantiavtale.</span><span class="sxs-lookup"><span data-stu-id="e0b18-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Siden Arbeidsordre](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="e0b18-118">Når du oppretter en arbeidsordre for et anleggsmiddel som dekkes av en leverandørgaranti, får du en varsling om garantiavtalen hvis arbeidsordren har en forventet startdato i løpet av garantiperioden.</span><span class="sxs-lookup"><span data-stu-id="e0b18-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="e0b18-119">Du kan deretter annullere arbeidsordren etter behov.</span><span class="sxs-lookup"><span data-stu-id="e0b18-119">You can then cancel the work order, as you require.</span></span>
