---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (15. november 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: nb-no
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="606cd-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (15. november 2018)</span><span class="sxs-lookup"><span data-stu-id="606cd-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="606cd-104">**Build 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="606cd-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="606cd-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="606cd-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="606cd-106">Andre endringer/reparasjoner</span><span class="sxs-lookup"><span data-stu-id="606cd-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="606cd-107">Kan ikke endre den ansattes gjeldende stilling til en fremtidig åpen stilling</span><span class="sxs-lookup"><span data-stu-id="606cd-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="606cd-108">En endring er gjort for å aktivere stillingsoverføringer når stillingen bare er tilgjengelig i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="606cd-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="606cd-109">Stillingen vises ikke når du oppretter en ny ansatt</span><span class="sxs-lookup"><span data-stu-id="606cd-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="606cd-110">En endring er gjort for å vise alle ledige stillinger som er tilgjengelige for tilordningen, når du ansetter nye personer i Talent.</span><span class="sxs-lookup"><span data-stu-id="606cd-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="606cd-111">Dette inkluderer historiske stillinger eller om stillingene er fremtidig daterte.</span><span class="sxs-lookup"><span data-stu-id="606cd-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="606cd-112">Stillinger vises nå på riktig måte basert på startdatoen for ansettelsen.</span><span class="sxs-lookup"><span data-stu-id="606cd-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="606cd-113">Avslutningsdatoen vises basert på brukerinnstillinger</span><span class="sxs-lookup"><span data-stu-id="606cd-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="606cd-114">Har gjort en endring i listen over tidligere ansatte for å ta hensyn til alle tidssoneforskyvninger for den foretrukne tidssonen for ansatte når du viser avslutningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="606cd-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="606cd-115">Koblinger til Arbeidselementer som er tilordnet til meg viser ikke riktig informasjon</span><span class="sxs-lookup"><span data-stu-id="606cd-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="606cd-116">Med denne endringer vil navigasjon til detaljene i de individuelle arbeidselementene i listen vise riktig informasjon for det valgte elementet.</span><span class="sxs-lookup"><span data-stu-id="606cd-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="606cd-117">Dette problemet oppstod bare med avanserte sikkerhetsalternativer.</span><span class="sxs-lookup"><span data-stu-id="606cd-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="606cd-118">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="606cd-118">Known issue</span></span>

- <span data-ttu-id="606cd-119">**Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene.</span><span class="sxs-lookup"><span data-stu-id="606cd-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="606cd-120">**Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="606cd-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="606cd-121">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="606cd-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="606cd-122">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="606cd-122">(This issue will be fixed in the next platform update.)</span></span>

