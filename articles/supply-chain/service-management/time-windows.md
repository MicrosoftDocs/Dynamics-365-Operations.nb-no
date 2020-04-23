---
title: Tidsvinduer
description: Du kan bruke tidsvinduer for å optimalisere planleggingen av serviceordrelinjene.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63a166806c2c8ac84cc1d71d6ec84fcb28033feb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206525"
---
# <a name="time-windows"></a><span data-ttu-id="0d601-103">Tidsvinduer</span><span class="sxs-lookup"><span data-stu-id="0d601-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d601-104">Du kan bruke tidsvinduer for å optimalisere planleggingen av serviceordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="0d601-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="0d601-105">Du kan konfigurere systemet slik at serviceordrer opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="0d601-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="0d601-106">Basert på kriteriene som er definert i et tidsvindu, kan du koble til så mange serviceordrelinjer som mulig til så få serviceordrer som mulig.</span><span class="sxs-lookup"><span data-stu-id="0d601-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="0d601-107">Tidsvinduer definerer hvor langt en serviceordrelinje kan flyttes fra den beregnede datoen.</span><span class="sxs-lookup"><span data-stu-id="0d601-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="0d601-108">Den beregnede datoen er datoen som serviceordrelinjen skulle forekomme på.</span><span class="sxs-lookup"><span data-stu-id="0d601-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="0d601-109">Datoen er basert på intervallinnstillingen og serviceperioden du definerte på **Opprett serviceordrer**-siden.</span><span class="sxs-lookup"><span data-stu-id="0d601-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="0d601-110">Du definerer et tidsvindu ved hjelp av verdiene i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="0d601-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="0d601-111">Metode</span><span class="sxs-lookup"><span data-stu-id="0d601-111">Method</span></span> | <span data-ttu-id="0d601-112">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0d601-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d601-113">Uke</span><span class="sxs-lookup"><span data-stu-id="0d601-113">Week</span></span>   | <span data-ttu-id="0d601-114">Datoen som serviceordrelinjen kan flyttes til en hvilken som helst åpen dag i den samme uken som den opprinnelig beregnede datoen.</span><span class="sxs-lookup"><span data-stu-id="0d601-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="0d601-115">Måned</span><span class="sxs-lookup"><span data-stu-id="0d601-115">Month</span></span>  | <span data-ttu-id="0d601-116">Datoen som serviceordrelinjen kan flyttes til en hvilken som helst åpen dag i den samme måneden som den opprinnelig beregnede datoen.</span><span class="sxs-lookup"><span data-stu-id="0d601-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="0d601-117">Den beregnede datoen for en serviceordrelinje er for eksempel 15. februar 2017.</span><span class="sxs-lookup"><span data-stu-id="0d601-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="0d601-118">Serviceordrelinjen kan planlegges for en ukedag mellom 1. februar og 28. februar 2017.</span><span class="sxs-lookup"><span data-stu-id="0d601-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="0d601-119">Manuell</span><span class="sxs-lookup"><span data-stu-id="0d601-119">Manual</span></span> | <span data-ttu-id="0d601-120">Du kan definere det maksimale antallet dager før eller etter den opprinnelig beregnede datoen som serviceordrelinjen kan flyttes til.</span><span class="sxs-lookup"><span data-stu-id="0d601-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="0d601-121">Hvis du ikke angir et tidsvindu for en serviceavtalelinje, må serviceordrelinjen som utledes av serviceavtalelinjen, være på nøyaktig samme dato som den opprinnelig ble planlagt for.</span><span class="sxs-lookup"><span data-stu-id="0d601-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d601-122">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="0d601-122">Related topics</span></span>

[<span data-ttu-id="0d601-123">Opprette tidsvinduer</span><span class="sxs-lookup"><span data-stu-id="0d601-123">Create time windows</span></span>](create-time-windows.md)

