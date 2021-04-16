---
title: Administrere en datakilde for kostnadsregnskapsfinansen
description: Bruk denne fremgangsmåten til å administrere økonomimoduldatakilden for kostnadsregnskapsfinans.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da4d351f4bce6494a107a55895866e4d3d43953f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841075"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="5d0f5-103">Administrere en datakilde for kostnadsregnskapsfinansen</span><span class="sxs-lookup"><span data-stu-id="5d0f5-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d0f5-104">Bruk denne fremgangsmåten til å administrere økonomimoduldatakilden for kostnadsregnskapsfinans.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="5d0f5-105">Før du fullfører denne oppgaven, må du se gjennom oppgaveveiledningene "Opprette kostnadsregnskapsfinans" og "Definere kostnadskontrollenheter".</span><span class="sxs-lookup"><span data-stu-id="5d0f5-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="5d0f5-106">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="5d0f5-107">Gå til Kostnadsregnskap > Finansoppsett > Kostnadsregnskapsfinans.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="5d0f5-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5d0f5-109">Klikk Faktiske versjoner.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-109">Click Actual versions.</span></span>
4. <span data-ttu-id="5d0f5-110">Klikk Administrer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="5d0f5-111">Klikk Økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-111">Click General ledger.</span></span>
6. <span data-ttu-id="5d0f5-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-112">Click New.</span></span>
7. <span data-ttu-id="5d0f5-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="5d0f5-114">Angi eller velg en verdi i feltet Dataleverandør.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="5d0f5-115">I dette eksemplet velger du Dynamics 365 Finance - Finansposter.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="5d0f5-116">Angi eller velg en verdi i feltet Kostnadselementdimensjon.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="5d0f5-117">Velg Kostnadselementer for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="5d0f5-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-118">Click Save.</span></span>
11. <span data-ttu-id="5d0f5-119">Klikk Konfigurer dataleverandør.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="5d0f5-120">Angi eller velg en verdi i feltet Juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="5d0f5-121">Velg USP2 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="5d0f5-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-122">Click New.</span></span>
14. <span data-ttu-id="5d0f5-123">Velg Gjeldende i feltet Posteringslag.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="5d0f5-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5d0f5-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]