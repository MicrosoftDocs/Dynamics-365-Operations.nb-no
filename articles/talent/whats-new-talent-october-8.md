---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (1. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 92f06d29dfa8110106a2a0e71434b2c0c75110b5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518766"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="5b319-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (8. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="5b319-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b319-104">**Build 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="5b319-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="5b319-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="5b319-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="5b319-106">Tillate at andre datoer brukes på lagbasis for permisjon (permisjonsadministrasjon)</span><span class="sxs-lookup"><span data-stu-id="5b319-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="5b319-107">Når permisjon innvilges til ansatte, bestemmer belønningslagbasisen hvor mange fridager som påløper for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="5b319-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="5b319-108">Disse tre lagene er for øyeblikket basert på startdato og ansiennitetsdato for ansatt.</span><span class="sxs-lookup"><span data-stu-id="5b319-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="5b319-109">I enkelte tilfeller må organisasjoner basere disse tre lagene på andre datoer, som jubileumsdato eller opprinnelig ansettelsesdato.</span><span class="sxs-lookup"><span data-stu-id="5b319-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="5b319-110">Disse datoene er allerede brukt på permisjonsplanen for å finne ut når avsetninger skjer. Muligheten til å bruke de samme datoene når en ansatt registreres i en plan, er lagt til for å bestemme det påløpte beløpet.</span><span class="sxs-lookup"><span data-stu-id="5b319-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="5b319-111">Andre endringer</span><span class="sxs-lookup"><span data-stu-id="5b319-111">Other changes</span></span>
<span data-ttu-id="5b319-112">Diverse reparasjoner er inkludert i denne versjonen.</span><span class="sxs-lookup"><span data-stu-id="5b319-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="5b319-113">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="5b319-113">Known issue</span></span>

<span data-ttu-id="5b319-114">**Problem:** Når du legger til en ny tilknytning til en arbeider, er knappenei **Ny** og **Rediger** nedtonet. **Løsning:** Før du åpner vedleggssiden, må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="5b319-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="5b319-115">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="5b319-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="5b319-116">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="5b319-116">(This issue will be fixed in the next platform update.)</span></span>
