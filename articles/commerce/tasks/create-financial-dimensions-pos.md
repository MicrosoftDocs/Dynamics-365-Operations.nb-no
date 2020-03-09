---
title: " Opprette finansdimensjoner for kasser på salgssted og konfigurere dimensjonsverdier for kasser"
description: Denne prosedyren hjelper med å opprette finansdimensjoner for salgsstedskasser, og beskriver hvordan du konfigurerer finansdimensjonsverdiene på kassene.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e04af04de3d18d375ce3609ab4cd53f652c2fbc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023547"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="7b20d-103"> Opprette finansdimensjoner for kasser på salgssted og konfigurere dimensjonsverdier for kasser</span><span class="sxs-lookup"><span data-stu-id="7b20d-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7b20d-104">Denne prosedyren hjelper med å opprette finansdimensjoner for salgsstedskasser, og beskriver hvordan du konfigurerer finansdimensjonsverdiene på kassene.</span><span class="sxs-lookup"><span data-stu-id="7b20d-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="7b20d-105">Denne prosedyren inneholder ikke andre relaterte trinn, for eksempel å opprette dimensjonssett og kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="7b20d-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="7b20d-106">Du finner disse oppgavene i andre emner.</span><span class="sxs-lookup"><span data-stu-id="7b20d-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="7b20d-107">Denne registreringen bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="7b20d-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="7b20d-108">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="7b20d-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="7b20d-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7b20d-109">Click New.</span></span>
3. <span data-ttu-id="7b20d-110">Velg et alternativ i feltet Bruk verdier fra.</span><span class="sxs-lookup"><span data-stu-id="7b20d-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="7b20d-111">Skriv inn en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="7b20d-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="7b20d-112">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="7b20d-112">Click Activate.</span></span>
6. <span data-ttu-id="7b20d-113">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="7b20d-113">Click Close.</span></span>
7. <span data-ttu-id="7b20d-114">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="7b20d-114">Click Activate.</span></span>
8. <span data-ttu-id="7b20d-115">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="7b20d-115">Click Dimension values.</span></span>
9. <span data-ttu-id="7b20d-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7b20d-116">Close the page.</span></span>
10. <span data-ttu-id="7b20d-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7b20d-117">Click Save.</span></span>
11. <span data-ttu-id="7b20d-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7b20d-118">Close the page.</span></span>
12. <span data-ttu-id="7b20d-119">Gå til Detaljhandel og handel > Kanaloppsett > Salgsstedsoppsett > Kasser.</span><span class="sxs-lookup"><span data-stu-id="7b20d-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="7b20d-120">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7b20d-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="7b20d-121">Aktiver utvidelsen av delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="7b20d-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="7b20d-122">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="7b20d-122">Click Edit.</span></span>
16. <span data-ttu-id="7b20d-123">Klikk rullegardinknappen i Terminal-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7b20d-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="7b20d-124">Finn og velg dimensjonsverdien i listen for kassen som oppdateres.</span><span class="sxs-lookup"><span data-stu-id="7b20d-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="7b20d-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7b20d-125">Click Save.</span></span>
