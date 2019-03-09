---
title: Gjøre skilletegnet for kontoplan unikt
description: I Dynamics 365 for Finance and Operations kan du ikke ha samme skilletegn for kontoplanen og dimensjonsverdier. Du må endre skilletegnverdier etter oppgraderingen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "335859"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="caecd-104">Gjøre skilletegnet for kontoplan unikt</span><span class="sxs-lookup"><span data-stu-id="caecd-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="caecd-105">Du kunne bruke samme skilletegn for kontoplanene og dimensjonsverdiene i Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="caecd-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="caecd-106">I Dynamics 365 for Finance and Operations kan du ikke ha samme skilletegn for kontoplanen og dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="caecd-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="caecd-107">Hvis det finnes dupliserte skilletegn, kan du endre dem etter oppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="caecd-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="caecd-108">Denne funksjonen er tilgjengelig i:</span><span class="sxs-lookup"><span data-stu-id="caecd-108">This feature is available in:</span></span>
- <span data-ttu-id="caecd-109">Dynamics 365 for Finance and Operations versjon 8.0</span><span class="sxs-lookup"><span data-stu-id="caecd-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="caecd-110">Dynamics 365 for Finance and Operations versjon 7.1, KB 4094701 Kan ikke angi finansdimensjonene når dimensjonsverdiene inneholder skilletegn for kontoplan</span><span class="sxs-lookup"><span data-stu-id="caecd-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="caecd-111">Dynamics 365 for Finance and Operations versjon 7.2, KB 4092967 Kan ikke velge underprosjektet som dimensjon når underprosjektformatet inneholder skilletegn for dimensjon</span><span class="sxs-lookup"><span data-stu-id="caecd-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="caecd-112">Oppdatere skilletegn</span><span class="sxs-lookup"><span data-stu-id="caecd-112">Update delimiter</span></span>
<span data-ttu-id="caecd-113">Hvis det er en konflikt med kontoplanen, kan skilletegn for kontoplanen og formatet for prosjekt/underprosjekt-ID endres.</span><span class="sxs-lookup"><span data-stu-id="caecd-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="caecd-114">Ingen andre dimensjonsskilletegn kan endres.</span><span class="sxs-lookup"><span data-stu-id="caecd-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="caecd-115">Du kan endre skilletegn for kontoplanen etter oppgradering til Finance and Operations i **Parametere for økonomimodul** > **Kontoplan og dimensjoner** > **Endre skilletegn**.</span><span class="sxs-lookup"><span data-stu-id="caecd-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="caecd-116">Hvis den eneste konflikten er med formatet for prosjekt/underprosjekt-ID, kan du endre verdien i **Parametere for prosjektstyring og regnskap** > **Generell** > **Endre format for delprosjekt**.</span><span class="sxs-lookup"><span data-stu-id="caecd-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="caecd-117">Slik fastslår du om miljøet ditt krever oppdaterte skilletegn</span><span class="sxs-lookup"><span data-stu-id="caecd-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="caecd-118">Hvis skilletegn i det oppgraderte miljøet er i konflikt, kan du oppleve ustabilitet når du angir verdier i en segmentert angivelseskontroll eller dimensjonsangivelseskontroll.</span><span class="sxs-lookup"><span data-stu-id="caecd-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="caecd-119">Dette betyr at du alltid må bruke oppslag eller en undermeny når du angir kombinasjoner av konto og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="caecd-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
