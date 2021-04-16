---
title: Behandle og spore kildedata
description: All databehandling kjøres av jobber.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34612469f763cf1b30be46ff088605ae22883022
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841003"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="f1c74-103">Behandle og spore kildedata</span><span class="sxs-lookup"><span data-stu-id="f1c74-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1c74-104">All databehandling kjøres av jobber.</span><span class="sxs-lookup"><span data-stu-id="f1c74-104">All data processing is run by jobs.</span></span> <span data-ttu-id="f1c74-105">For hver enkelt leverandør for jobb og data opprettes en journal til dokumentet som prosessen har blitt kjørt, og som oppføringene som ble behandlet i den gjeldende jobben.</span><span class="sxs-lookup"><span data-stu-id="f1c74-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="f1c74-106">Bruk denne fremgangsmåten til å definere en datakilde, og deretter spore opprinnelsen til en bestemt kostpost.</span><span class="sxs-lookup"><span data-stu-id="f1c74-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="f1c74-107">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="f1c74-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="f1c74-108">Før du fullfører denne oppgaven, må du se gjennom følgende oppgaveveiledninger: "Opprette kostnadsregnskapsfinans", "Definere kostnadskontrollenheter" og "Administrere datakilde for kostnadsregnskapsfinans".</span><span class="sxs-lookup"><span data-stu-id="f1c74-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="f1c74-109">Gå til Kostnadsregnskap > Finansoppsett > Kostnadsregnskapsfinans.</span><span class="sxs-lookup"><span data-stu-id="f1c74-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="f1c74-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f1c74-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f1c74-111">Velg kostnadsregnskapsfinans som du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f1c74-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="f1c74-112">Klikk Faktiske versjoner.</span><span class="sxs-lookup"><span data-stu-id="f1c74-112">Click Actual versions.</span></span>
4. <span data-ttu-id="f1c74-113">I handlingsruten, klikker du kilden for databehandling.</span><span class="sxs-lookup"><span data-stu-id="f1c74-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="f1c74-114">Klikk Overføringsjournaler for økonomimoduloppføring.</span><span class="sxs-lookup"><span data-stu-id="f1c74-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="f1c74-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f1c74-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f1c74-116">Klikk Journaloppføringer.</span><span class="sxs-lookup"><span data-stu-id="f1c74-116">Click Journal entries.</span></span>
8. <span data-ttu-id="f1c74-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f1c74-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f1c74-118">Klikk Kostnadsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="f1c74-118">Click Cost entries.</span></span>
10. <span data-ttu-id="f1c74-119">Klikk Kildeoppføring.</span><span class="sxs-lookup"><span data-stu-id="f1c74-119">Click Source entry.</span></span>
11. <span data-ttu-id="f1c74-120">I handlingsruten, klikker du kilden for databehandling.</span><span class="sxs-lookup"><span data-stu-id="f1c74-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="f1c74-121">Klikk Økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="f1c74-121">Click General ledger.</span></span>
13. <span data-ttu-id="f1c74-122">Angi eller velg en verdi i feltet Regnskapskalenderperiode.</span><span class="sxs-lookup"><span data-stu-id="f1c74-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c74-123">I dette eksemplet, velg regnskapsår 2017, periode 9.</span><span class="sxs-lookup"><span data-stu-id="f1c74-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="f1c74-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1c74-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]