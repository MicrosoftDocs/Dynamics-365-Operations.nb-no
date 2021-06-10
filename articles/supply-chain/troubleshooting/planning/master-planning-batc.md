---
title: Du kan ikke filtrere hovedplanleggingselementer etter de tilknyttede dekningsgruppeverdiene
description: Du kan ikke filtrere hovedplanleggingselementer etter de tilknyttede dekningsgruppeverdiene.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049483"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="04e39-103">Du kan ikke filtrere hovedplanleggingselementer etter de tilknyttede dekningsgruppeverdiene</span><span class="sxs-lookup"><span data-stu-id="04e39-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="04e39-104">KB-nummer: 4612572</span><span class="sxs-lookup"><span data-stu-id="04e39-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="04e39-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="04e39-105">Symptoms</span></span>

<span data-ttu-id="04e39-106">Du vil filtrere varene som skal inkluderes i en satsvis jobb for hovedplanlegging, basert på verdiene til relaterte poster fra varedekningstabellen.</span><span class="sxs-lookup"><span data-stu-id="04e39-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="04e39-107">(Du vil for eksempel filtrere varene etter **Leverandør** og/eller **Dekningsgruppe**).</span><span class="sxs-lookup"><span data-stu-id="04e39-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="04e39-108">Med filteroppsettet for den satsvise jobben kan du opprette en kobling fra **Varer**-tabellen til **Varedekning**-tabellen og deretter angi feltverdier fra varedekningstabellen i spørringen.</span><span class="sxs-lookup"><span data-stu-id="04e39-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="04e39-109">Når du har fullført dette oppsettet, oppretter imidlertid systemet planlagte bestillinger for hele varedekningen, ikke bare for varene som samsvarer med de angitte feltverdiene fra varedekningstabellen.</span><span class="sxs-lookup"><span data-stu-id="04e39-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="04e39-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="04e39-110">Resolution</span></span>

<span data-ttu-id="04e39-111">Filteret for den satsvise jobben kan bare filtrere på varer.</span><span class="sxs-lookup"><span data-stu-id="04e39-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="04e39-112">Selv om du kan legge til en kobling i **Varedekning**-tabellen, vil ikke filterinnstillingene du gjør mot tabellen, påvirke resultatet av spørringen.</span><span class="sxs-lookup"><span data-stu-id="04e39-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="04e39-113">Ved kjøretid kjører systemet planlegging for alle dekningsgruppene og alle variasjonene de filtrerte varene har.</span><span class="sxs-lookup"><span data-stu-id="04e39-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="04e39-114">Når en vare allerede er inkludert i kjøringen, vil ikke dekningsgrupper som er inkludert i varefilteret, påvirke planleggingsresultatet.</span><span class="sxs-lookup"><span data-stu-id="04e39-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
