---
title: Definere mva-grupper og mva-grupper for vare
description: Denne oppgaveregistreringen leder deg gjennom oppsettet av merverdiavgift og mva-grupper for vare.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e35f98de715af95b0bec2b2ca5d7e7570aa8fdba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994496"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="480d3-103">Definere mva-grupper og mva-grupper for vare</span><span class="sxs-lookup"><span data-stu-id="480d3-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="480d3-104">Denne oppgaveregistreringen leder deg gjennom oppsettet av merverdiavgift og mva-grupper for vare.</span><span class="sxs-lookup"><span data-stu-id="480d3-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="480d3-105">Mva-grupper er grupper av mva-koder som er knyttet til kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="480d3-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="480d3-106">De er også knyttet til finanskontoer for transaksjoner som ikke er postert til en bestemt leverandør eller kunde.</span><span class="sxs-lookup"><span data-stu-id="480d3-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="480d3-107">Mva-grupper for vare er grupper av mva-koder som er knyttet til ressurser som produkter.</span><span class="sxs-lookup"><span data-stu-id="480d3-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="480d3-108">Merverdiavgiften som gjelder for en bestemt transaksjon, fastsettes av mva-kodene som er inkludert både i mva-gruppen og i mva-gruppen for vare for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="480d3-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="480d3-109">Merverdiavgift kan bare beregnes hvis en mva-gruppe og en mva-gruppe for vare er valgt for hver transaksjon det skal beregnes eller posteres merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="480d3-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="480d3-110">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Merverdiavgift > Mva-grupper**.</span><span class="sxs-lookup"><span data-stu-id="480d3-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="480d3-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="480d3-111">Click **New**.</span></span>
3. <span data-ttu-id="480d3-112">Skriv inn en verdi i **Mva-gruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="480d3-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="480d3-113">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="480d3-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="480d3-114">Aktiver/deaktiver utvidelsen av delen **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="480d3-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="480d3-115">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="480d3-115">Click **Add**.</span></span>
7. <span data-ttu-id="480d3-116">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="480d3-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="480d3-117">Klikk rullegardinknappen i **Mva-kode**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="480d3-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="480d3-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="480d3-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="480d3-119">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="480d3-119">Click **Save**.</span></span>
11. <span data-ttu-id="480d3-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="480d3-120">Close the page.</span></span>
12. <span data-ttu-id="480d3-121">Gå til **Avgift > Indirekte avgifter > Merverdiavgift > Vare, mva-grupper**.</span><span class="sxs-lookup"><span data-stu-id="480d3-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="480d3-122">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="480d3-122">Click **New**.</span></span>
14. <span data-ttu-id="480d3-123">Skriv inn en verdi i feltet **Vare, mva-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="480d3-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="480d3-124">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="480d3-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="480d3-125">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="480d3-125">Click **Add**.</span></span>
17. <span data-ttu-id="480d3-126">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="480d3-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="480d3-127">Klikk rullegardinknappen i **Mva-kode**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="480d3-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="480d3-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="480d3-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="480d3-129">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="480d3-129">Click **Save**.</span></span>

