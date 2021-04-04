---
title: Synkronisere dato og klokkeslett i importjobber
description: Bruk UTC-tidssoner i importjobber for å unngå problemer med tidssonekonvertering.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570487"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="c4bca-103">Synkronisere dato og klokkeslett i importjobber</span><span class="sxs-lookup"><span data-stu-id="c4bca-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4bca-104">Det er viktig å angi tidssonen UTC (Coordinated Universal Time) for importjobben.</span><span class="sxs-lookup"><span data-stu-id="c4bca-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c4bca-105">Du får kanskje uventede datoer og klokkeslett i de importerte dataene hvis du bruker en annen innstilling.</span><span class="sxs-lookup"><span data-stu-id="c4bca-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="c4bca-106">Uten riktig innstilling konverterer importprosessen UTC-datoen til det lokale formatet, og deretter konverterer systeminnstillingene den på nytt.</span><span class="sxs-lookup"><span data-stu-id="c4bca-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="c4bca-107">Denne doble konverteringen gjør at datoer endres mellom programmer.</span><span class="sxs-lookup"><span data-stu-id="c4bca-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="c4bca-108">Den doble konverteringen kan for eksempel gjøre at startdatoen for en ansatt, blir forskjellige i Dynamics 365 Human Resources og Dynamics 365 Finance på grunn av forskjeller i lokale tidssoner.</span><span class="sxs-lookup"><span data-stu-id="c4bca-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="c4bca-109">Du løser dette problemet ved å angi UTC for importjobben.</span><span class="sxs-lookup"><span data-stu-id="c4bca-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="c4bca-110">Velg **Databehandling** i Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4bca-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="c4bca-111">Velg **Importer prosjekter**, og velg deretter prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c4bca-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="c4bca-112">Velg **CSV-Unicode** under **Kildedatoformat**.</span><span class="sxs-lookup"><span data-stu-id="c4bca-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="c4bca-113">[![Endre kildedatoformatet til UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="c4bca-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="c4bca-114">Endre **Tidssone** til **Coordinated Universal Timezone**, og endre **Språk** til **En-US**.</span><span class="sxs-lookup"><span data-stu-id="c4bca-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]