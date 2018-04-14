--- 
title: "Overføre et anleggsmiddel"
description: "Denne oppgaveveiledningen overfører den økonomiske informasjonen for et anleggsmiddeltablå fra én finansdimensjon som er satt til et nytt sett med finansdimensjoner."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ab115ff3bd79ba42de5b28be962ab2a55c1d4aa4
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="06544-103">Overføre et anleggsmiddel</span><span class="sxs-lookup"><span data-stu-id="06544-103">Transfer a fixed asset</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06544-104">Denne oppgaveveiledningen overfører den økonomiske informasjonen for et anleggsmiddeltablå fra én finansdimensjon som er satt til et nytt sett med finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="06544-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="06544-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="06544-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="06544-106">Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="06544-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="06544-107">I listen finner og merker du anleggsmidlet som skal overføres.</span><span class="sxs-lookup"><span data-stu-id="06544-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="06544-108">Klikk Anleggsmiddel i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="06544-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="06544-109">Klikk Overfør anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="06544-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="06544-110">Angi en dato i feltet Overføringsdato.</span><span class="sxs-lookup"><span data-stu-id="06544-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="06544-111">Angi kommentarer for å beskrive overføringen.</span><span class="sxs-lookup"><span data-stu-id="06544-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="06544-112">Denne listen viser alle tablåene for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="06544-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="06544-113">Merk tablåene du vil overføre til et nytt sett med finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="06544-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="06544-114">Denne listen viser de eksisterende finansdimensjonsverdiene for det valgte tablået.</span><span class="sxs-lookup"><span data-stu-id="06544-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="06544-115">Velg finansdimensjonen du vil oppdatere for det valgte anleggsmiddeltablået.</span><span class="sxs-lookup"><span data-stu-id="06544-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="06544-116">Klikk rullegardinknappen i feltet Finansdimensjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="06544-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="06544-117">Angi andre verdier for finansdimensjonen etter behov.</span><span class="sxs-lookup"><span data-stu-id="06544-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="06544-118">Alle finansdimensjonsverdier endres når det oppstår en overføring, enten en verdi er angitt eller står tom.</span><span class="sxs-lookup"><span data-stu-id="06544-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="06544-119">Hvis du for eksempel har angitt en verdi for BusinessUnit og latt finansdimensjonene CostCenter og Avdeling stå tom.</span><span class="sxs-lookup"><span data-stu-id="06544-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="06544-120">Hvis kontostrukturen tillater tomme verdier for CostCenter og Avdeling, fører overføringen til at hver verdimodell får den nye verdien for BusinessUnit og en tom verdi for CostCenter og Avdeling.</span><span class="sxs-lookup"><span data-stu-id="06544-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="06544-121">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="06544-121">Click Update.</span></span>
    * <span data-ttu-id="06544-122">Du har muligheten til å forhåndsvise endringene før du fullfører overføringen.</span><span class="sxs-lookup"><span data-stu-id="06544-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="06544-123">Se gjennom resultatene før du overfører anleggsmiddeltablåene.</span><span class="sxs-lookup"><span data-stu-id="06544-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="06544-124">Klikk Overfør.</span><span class="sxs-lookup"><span data-stu-id="06544-124">Click Transfer.</span></span>


