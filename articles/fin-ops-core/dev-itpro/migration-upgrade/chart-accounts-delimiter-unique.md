---
title: Gjøre skilletegnet for kontoplan unikt
description: Dette emnet beskriver hvordan du ikke kan ha samme skilletegn for kontoplanen og dimensjonsverdier. Du må endre skilletegnverdier etter oppgraderingen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 2ce91557334a4342fa85848fc1b746b6b12c8992
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688533"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="0ddc1-104">Gjøre skilletegnet for kontoplan unikt</span><span class="sxs-lookup"><span data-stu-id="0ddc1-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ddc1-105">Du kunne bruke samme skilletegn for kontoplanene og dimensjonsverdiene i Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="0ddc1-106">Du kan ikke ha samme skilletegn for kontoplan og dimensjonsverdier i gjeldende versjon av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="0ddc1-107">Hvis det finnes dupliserte skilletegn, kan du endre dem etter oppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="0ddc1-108">Denne funksjonen er ikke tilgjengelig i følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="0ddc1-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="0ddc1-109">Finance and Operations versjon 8.0</span><span class="sxs-lookup"><span data-stu-id="0ddc1-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="0ddc1-110">Finance and Operations versjon 7.1, KB 4094701 Kan ikke angi finansdimensjonene når dimensjonsverdiene inneholder skilletegn for kontoplan</span><span class="sxs-lookup"><span data-stu-id="0ddc1-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="0ddc1-111">Finance and Operations versjon 7.2, KB 4092967 Kan ikke velge underprosjektet som dimensjon når underprosjektformatet inneholder skilletegn for dimensjon</span><span class="sxs-lookup"><span data-stu-id="0ddc1-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="0ddc1-112">Oppdatere skilletegn</span><span class="sxs-lookup"><span data-stu-id="0ddc1-112">Update delimiter</span></span>
<span data-ttu-id="0ddc1-113">Hvis det er en konflikt med kontoplanen, kan skilletegn for kontoplanen og formatet for prosjekt/underprosjekt-ID endres.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="0ddc1-114">Ingen andre dimensjonsskilletegn kan endres.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="0ddc1-115">Du kan endre skilletegn for kontoplanen etter oppgradering i **Parametere for økonomimodul** > **Kontoplan og dimensjoner** > **Endre skilletegn**.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="0ddc1-116">Hvis den eneste konflikten er med formatet for prosjekt/underprosjekt-ID, kan du endre verdien i **Parametere for prosjektstyring og regnskap** > **Generell** > **Endre format for delprosjekt**.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="0ddc1-117">Slik fastslår du om miljøet ditt krever oppdaterte skilletegn</span><span class="sxs-lookup"><span data-stu-id="0ddc1-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="0ddc1-118">Hvis skilletegn i det oppgraderte miljøet er i konflikt, kan du oppleve ustabilitet når du angir verdier i en segmentert angivelseskontroll eller dimensjonsangivelseskontroll.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="0ddc1-119">Dette betyr at du alltid må bruke oppslag eller en undermeny når du angir kombinasjoner av konto og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="0ddc1-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
