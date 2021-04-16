---
title: Definere tilbehørstilordninger
description: Denne prosedyren viser hvordan du setter opp en tilbehørstilordning.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06139e87596965a481fc7fb2e2f653594be0ac1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838472"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="6748d-103">Definere tilbehørstilordninger</span><span class="sxs-lookup"><span data-stu-id="6748d-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6748d-104">Denne prosedyren viser hvordan du setter opp en tilbehørstilordning.</span><span class="sxs-lookup"><span data-stu-id="6748d-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="6748d-105">Dette gjøres vanligvis av en transportkoordinator.</span><span class="sxs-lookup"><span data-stu-id="6748d-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="6748d-106">Du må kjøre veiledningen Definere gebyrer for hubtilbehør og tilbehørsmaler før du bruker denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="6748d-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="6748d-107">Definere tilbehørstilordning</span><span class="sxs-lookup"><span data-stu-id="6748d-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="6748d-108">Gå til Transportstyring > Oppsett > Vurdering > Tilbehørstilordninger.</span><span class="sxs-lookup"><span data-stu-id="6748d-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="6748d-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="6748d-109">Click New.</span></span>
3. <span data-ttu-id="6748d-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="6748d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6748d-111">Aktiver/deaktiver utvidelsen av delen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="6748d-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="6748d-112">Klikk på rullegardinknappen i Hub-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6748d-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6748d-113">Velg huben som du har opprettet en tilbehørsmal for da du kjørte veiledningen Definere gebyrer for hubtilbehør og tilbehørsmaler, i listen.</span><span class="sxs-lookup"><span data-stu-id="6748d-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="6748d-114">Klikk på rullegardinknappen i feltet ID for hubtilbehør for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6748d-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6748d-115">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6748d-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6748d-116">Aktiver/deaktiver utvidelsen av Kriterier-delen.</span><span class="sxs-lookup"><span data-stu-id="6748d-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="6748d-117">I Kriterier-delen kan du velge de nøyaktige kriteriene for når tillegget skal gjelde, basert på de ulike verdiene som tilbys her.</span><span class="sxs-lookup"><span data-stu-id="6748d-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="6748d-118">Sett alternativet Bruk alltid til Ja.</span><span class="sxs-lookup"><span data-stu-id="6748d-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="6748d-119">Velg et alternativ i feltet Nivå for tilbehørstilordning.</span><span class="sxs-lookup"><span data-stu-id="6748d-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="6748d-120">Aktiver/deaktiver utvidelsen av Beregning-delen.</span><span class="sxs-lookup"><span data-stu-id="6748d-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="6748d-121">Velg Flat i Tilbehørsgebyrtype-feltet.</span><span class="sxs-lookup"><span data-stu-id="6748d-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="6748d-122">Tilbehørsgebyrtypen bestemmer hvordan det faktiske tillegget skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="6748d-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="6748d-123">I dette eksemplet er det et flatt tillegg.</span><span class="sxs-lookup"><span data-stu-id="6748d-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="6748d-124">Angi et tall i Tilbehørsgebyr-feltet.</span><span class="sxs-lookup"><span data-stu-id="6748d-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="6748d-125">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="6748d-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]