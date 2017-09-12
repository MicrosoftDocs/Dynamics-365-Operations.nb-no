---
title: Posteringskontoer for avhending av anleggsmidler
description: "Denne artikkelen forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="64b01-103">Posteringskontoer for avhending av anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="64b01-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="64b01-104">Denne artikkelen forklarer hvordan du setter opp bokføringskontoer i økonomimodulen for avhending av anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="64b01-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="64b01-105">På siden Posteringsprofiler for anleggsmidler i hurtigkategorien Finanskontoer velger du Avhendingssalg og salg og Avhending svinn for å konfigurere postering til finansmodulen.</span><span class="sxs-lookup"><span data-stu-id="64b01-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="64b01-106">Når det gjelder begge transaksjonstypene, krediteres finanskontoen med avhendingsverdien til anleggsmidlene.</span><span class="sxs-lookup"><span data-stu-id="64b01-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="64b01-107">Debetbeløpet posteres til en motkonto, som for eksempel kan være en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="64b01-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="64b01-108">Hvis anleggsmidler selges til en kunde, brukes kundekontoen i stedet for motkontoen.</span><span class="sxs-lookup"><span data-stu-id="64b01-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="64b01-109">Klikk Avhending og klikk deretter Salg eller Svinn. Definer deretter detaljerte kontoer for å tilbakeføre netto bokført verdi for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="64b01-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="64b01-110">Du kan også angi informasjon i feltet Postert verdi og Salgsverditype på siden Avhendingsparametere.</span><span class="sxs-lookup"><span data-stu-id="64b01-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="64b01-111">Avhendingstransaksjonen for et anleggsmiddel i en lavverdipulje reduserer den netto bokførte verdien av lavverdipuljen med bare det avhendede beløpet.</span><span class="sxs-lookup"><span data-stu-id="64b01-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="64b01-112">Hvis derimot salgssummen for et anleggsmiddel overskrider den bokførte verdien av lavverdipuljen, reduseres netto bokført verdi til null.</span><span class="sxs-lookup"><span data-stu-id="64b01-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






