---
title: Knytte anleggsmidler til leieavtaler
description: Emnet forklarer hvordan du knytter et eksisterende anleggsmiddel til en ny leieavtale.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e2261755d98ee38564b4b864daf8e79551d1239
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814086"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="e8cf6-103">Knytte anleggsmidler til leieavtaler</span><span class="sxs-lookup"><span data-stu-id="e8cf6-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8cf6-104">Emnet forklarer hvordan du knytter et eksisterende anleggsmiddel til en ny leieavtale.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="e8cf6-105">Når du knytter et anleggsmiddel til en leieavtale, er verdien til bruksrettseiendelen ved opprinnelig føring anskaffelseskostnaden til anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="e8cf6-106">Før du kan knytte et anleggsmiddel til en leieavtale, må du opprette en post for anleggsmidlet i Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="e8cf6-107">På siden **Leiesammendrag** må du deretter opprette en leieavtale og koble anleggsmiddelet til denne leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="e8cf6-108">Legg til en leieavtale ved å følge trinnene i [Legge til eller kopiere leieavtaler](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf6-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="e8cf6-109">I feltet **Anleggsmiddelnummer** på siden **Legg til leieavtale** velger du anleggsmidlet som ennå ikke er anskaffet.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="e8cf6-110">Velg **Tablåer** og bekreft betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="e8cf6-111">Velg **Opprinnelig føring**.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="e8cf6-112">Velg **Journal for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="e8cf6-113">Journaloppføringen for opprinnelig føring for leieavtalen debiterer anleggsmidlet for beløpet som vanligvis debiteres til kontoen for bruksrettseiendel.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="e8cf6-114">Du kan nå vise transaksjonstypen og tablået for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="e8cf6-115">Velg **Journaldetaljer**.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="e8cf6-116">Velg **Linjer** for å vise enkeltlinjene for journaloppføringen.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="e8cf6-117">Velg journallinjen som inneholder anleggsmidlet, og velg deretter fanen **Anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="e8cf6-118">Fanen **Anleggsmidler** viser transaksjonstypen og tablået.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="e8cf6-119">Feltet **Transaksjonstype** er som standard satt til **Anskaffelse**, og **Tablå**-feltet settes til gjeldende tablå for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="e8cf6-120">Når du har postert journaloppføringen for opprinnelig føring, vises transaksjonen som en anskaffelsestransaksjon for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="e8cf6-121">Hvis du vil vise transaksjonstabellen, kan du gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**, velge det aktuelle aktivumet og deretter velge **Vurderinger**.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="e8cf6-122">Du skal se at journaloppføringen for opprinnelig føring har opprettet en anskaffelsestransaksjon for det angitte anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="e8cf6-123">Anleggsmidlet kan nå avskrives ved hjelp av standard avskrivningsfunksjonalitet i Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="e8cf6-124">Hvis du vil ha mer informasjon om avskrivning, kan du se [Avskrivningsmetoder og -konvensjoner](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="e8cf6-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e8cf6-125">Hvis du knytter et anleggsmiddel til en leieavtale, deaktiveres knappene **Avskrivning av anleggsmiddel** og **Verdiforringelse for leieavtale** i Aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="e8cf6-126">Du kan vise transaksjoner for avskrivning av aktiva og verdiforringelse for leieavtale fra Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="e8cf6-127">Knappen **Aktivatransaksjoner**, som brukes til å åpne et forespørselsskjema, blir også deaktivert.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="e8cf6-128">Du kan også åpne forespørselsskjemaet **Aktivatransaksjoner** i Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="e8cf6-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]