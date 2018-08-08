--- 
title: Legge inn et tillegg til et anleggsmiddel
description: "Denne fremgangsmåten viser hvordan du legger til et tillegg i et eksisterende anleggsmiddel."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: bf87c968e940c730082eb1dba6745de2d1ca367a
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="62fe1-103">Legge inn et tillegg til et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="62fe1-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62fe1-104">Denne fremgangsmåten viser hvordan du legger til et tillegg i et eksisterende anleggsmiddel.</span><span class="sxs-lookup"><span data-stu-id="62fe1-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="62fe1-105">Formålet med Anleggsmiddeltillegg brukes til å spore varetillegg, vedlikehold eller forbedringer for aktiva, og er kun til informasjon.</span><span class="sxs-lookup"><span data-stu-id="62fe1-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="62fe1-106">Eventuelle endringer i verdien eller levetiden til anleggsmidlet må gjøres hver for seg.</span><span class="sxs-lookup"><span data-stu-id="62fe1-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="62fe1-107">Fremgangsmåten bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="62fe1-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="62fe1-108">Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="62fe1-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="62fe1-109">I listen finner og merker du anleggsmidlet for tillegget.</span><span class="sxs-lookup"><span data-stu-id="62fe1-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="62fe1-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="62fe1-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="62fe1-111">Klikk Anleggsmiddel i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="62fe1-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="62fe1-112">Klikk Anleggsmiddeltillegg.</span><span class="sxs-lookup"><span data-stu-id="62fe1-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="62fe1-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="62fe1-113">Click New.</span></span>
7. <span data-ttu-id="62fe1-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="62fe1-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="62fe1-115">Angi datoen for tilleggskjøpet eller -tjenesten.</span><span class="sxs-lookup"><span data-stu-id="62fe1-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="62fe1-116">Angi kostnad for vare, vedlikehold eller andre forbedringer for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="62fe1-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="62fe1-117">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="62fe1-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="62fe1-118">Den totale kostnaden har ingen innvirkning på verdien til anleggsmidlet og er bare til sporings- og informasjonsformål.</span><span class="sxs-lookup"><span data-stu-id="62fe1-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="62fe1-119">Hvis kostnaden skal kapitaliseres, må en oppskrivingsjusteringstransaksjon posteres separat.</span><span class="sxs-lookup"><span data-stu-id="62fe1-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="62fe1-120">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="62fe1-120">Click the General tab.</span></span>
    * <span data-ttu-id="62fe1-121">Angi Øker levetiden hvis tillegget øker levetiden for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="62fe1-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="62fe1-122">Dette feltet er kun veiledende.</span><span class="sxs-lookup"><span data-stu-id="62fe1-122">This field is informational only.</span></span> <span data-ttu-id="62fe1-123">Hvis du vil øke levetiden, kan du endre levetiden for verdimodeller og/eller avskrivningstablåene for aktivaet.</span><span class="sxs-lookup"><span data-stu-id="62fe1-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


