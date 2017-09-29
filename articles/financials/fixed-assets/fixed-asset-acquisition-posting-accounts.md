---
title: Posteringskontoer for anskaffelse av anleggsmidler
description: "Denne artikkelen beskriver hvordan du setter opp bokføringskontoer i økonomimodulen for anskaffelse av anleggsmidler."
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
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 887616463856875e2382a00b1d56520391ead844
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="19b17-103">Posteringskontoer for anskaffelse av anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="19b17-103">Fixed asset acquisition posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19b17-104">Denne artikkelen beskriver hvordan du setter opp bokføringskontoer i økonomimodulen for anskaffelse av anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="19b17-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="19b17-105">Kontoene som brukes for postering av anskaffelse av anleggsmidler, kan variere avhengig av metoden som brukes til å ansaffe anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="19b17-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="19b17-106">På siden Posteringsprofiler for anleggsmidler, i kategorien Finanskontoer, velger du Anskaffelse og Anskaffelsesjustering for å definere anleggsmiddelkontoer som posteres til finans.</span><span class="sxs-lookup"><span data-stu-id="19b17-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="19b17-107">I journalen og på bestillinger er Finanskonto vanligvis balansekontoen, der anskaffelsesverdien til det nye anleggsmiddelet debiteres.</span><span class="sxs-lookup"><span data-stu-id="19b17-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="19b17-108">Denne kontoen vises ikke i journalen og kan ikke erstattes i transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="19b17-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="19b17-109">Motkonto er også en balansekonto.</span><span class="sxs-lookup"><span data-stu-id="19b17-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="19b17-110">I den generelle journalen og anleggsmiddeljournalen brukes ofte denne kontoen som bankkontoen til å betale for anskaffelsen av varen.</span><span class="sxs-lookup"><span data-stu-id="19b17-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="19b17-111">Motkontoen er en standardkonto, noe som foreslås i journalen.</span><span class="sxs-lookup"><span data-stu-id="19b17-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="19b17-112">I journalen kan du endre den til enhver konto fra kontoplanen eller til en leverandørkonto hvis anleggsmidlet ble kjøpt fra en leverandør.</span><span class="sxs-lookup"><span data-stu-id="19b17-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="19b17-113">Når Fakturajournal eller Bestillinger i Leverandører brukes til anskaffelse av anleggsmidler, erstattes motkontoen for anleggsmiddeltransaksjonen av leverandørkontoen som er valgt for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="19b17-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="19b17-114">Når det gjelder anskaffelser som er postert via journalen Lager til anleggsmidler i Økonomimodul, blir ikke anleggsmidlene kjøpt fra ekstern kilder, men overføres fra firmaets eget lager.</span><span class="sxs-lookup"><span data-stu-id="19b17-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="19b17-115">Derfor er motkontoen en lageravgangskonto for lagervaren i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="19b17-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="19b17-116">Hvis du vil ha mer informasjon, se [Skaffe anleggsmidler ved hjelp av innkjøp](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="19b17-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>




