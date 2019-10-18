---
title: Opprette og anskaffe anleggsmidler som opprettes fra kunder
description: Denne oppgaveveiledningen går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025639e6e5bdc6b95e9c496f11f29ed8ec8d388c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179194"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="056b1-103">Opprette og anskaffe anleggsmidler som opprettes fra kunder</span><span class="sxs-lookup"><span data-stu-id="056b1-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="056b1-104">Denne oppgaveveiledningen går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen.</span><span class="sxs-lookup"><span data-stu-id="056b1-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="056b1-105">Den bruker regnskapsføreren og regnskapsassistenten og demonstrasjonsselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="056b1-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="056b1-106">Angi parametere for anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="056b1-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="056b1-107">I **navigasjonsruten** går du til **Moduler > Anleggsmidler > Oppsett > Parametere for anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="056b1-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="056b1-108">Vis hurtigfanen **Bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="056b1-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="056b1-109">Merk av for **Tillat anleggsmiddelanskaffelse fra innkjøp**.</span><span class="sxs-lookup"><span data-stu-id="056b1-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="056b1-110">Merk av for **Opprett anleggsmiddel under postering av produktkvittering eller faktura**.</span><span class="sxs-lookup"><span data-stu-id="056b1-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="056b1-111">Opprette en ny leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="056b1-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="056b1-112">I **navigasjonsruten** går du til **Moduler > Leverandører > Arbeidsområder > Leverandørfakturaregistrering**.</span><span class="sxs-lookup"><span data-stu-id="056b1-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="056b1-113">Klikk **Ny leverandørfaktura**.</span><span class="sxs-lookup"><span data-stu-id="056b1-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="056b1-114">Klikk rullegardinknappen i **Fakturakonto**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="056b1-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="056b1-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="056b1-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="056b1-116">Skriv inn en verdi i **Nummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="056b1-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="056b1-117">Angi en dato i **Posteringsdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="056b1-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="056b1-118">Klikk **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="056b1-118">Click **Add line**.</span></span>
8. <span data-ttu-id="056b1-119">Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="056b1-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="056b1-120">Både varer som ikke er lagerført, og innkjøpskategorier kan brukes til anleggsmiddelanskaffelse.</span><span class="sxs-lookup"><span data-stu-id="056b1-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="056b1-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="056b1-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="056b1-122">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="056b1-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="056b1-123">Én fakturalinje oppretter bare ett anleggsmiddel, uavhengig av antallet.</span><span class="sxs-lookup"><span data-stu-id="056b1-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="056b1-124">Verdien i feltet Fakturaantall overføres til antallet anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="056b1-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="056b1-125">Angi et tall i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="056b1-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="056b1-126">Utvid hurtigfanen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="056b1-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="056b1-127">Klikk kategorien **Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="056b1-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="056b1-128">Merk av i avmerkingsboksen **Opprett et nytt anleggsmiddel**.</span><span class="sxs-lookup"><span data-stu-id="056b1-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="056b1-129">Klikk rullegardinknappen i feltet **Anleggsmiddelgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="056b1-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="056b1-130">I listen velger du anleggsmiddelgruppen som skal brukes til å opprette det nye anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="056b1-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="056b1-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="056b1-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="056b1-132">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="056b1-132">Click **Post**.</span></span> <span data-ttu-id="056b1-133">Anleggsmidlet opprettes og anskaffes når fakturaen posteres.</span><span class="sxs-lookup"><span data-stu-id="056b1-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

