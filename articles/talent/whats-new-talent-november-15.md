---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (15. november 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a571568850a675f3472f2b62df33c0c35d905af0
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551386"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="c7015-103">Hva er nytt eller endret i Dynamics 365 Talent – Core HR (15. november 2018)</span><span class="sxs-lookup"><span data-stu-id="c7015-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7015-104">**Build 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="c7015-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="c7015-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="c7015-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="c7015-106">Andre endringer/reparasjoner</span><span class="sxs-lookup"><span data-stu-id="c7015-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="c7015-107">Kan ikke endre den ansattes gjeldende stilling til en fremtidig åpen stilling</span><span class="sxs-lookup"><span data-stu-id="c7015-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="c7015-108">En endring er gjort for å aktivere stillingsoverføringer når stillingen bare er tilgjengelig i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="c7015-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="c7015-109">Stillingen vises ikke når du oppretter en ny ansatt</span><span class="sxs-lookup"><span data-stu-id="c7015-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="c7015-110">En endring er gjort for å vise alle ledige stillinger som er tilgjengelige for tilordningen, når du ansetter nye personer i Talent.</span><span class="sxs-lookup"><span data-stu-id="c7015-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="c7015-111">Dette inkluderer historiske stillinger eller om stillingene er fremtidig daterte.</span><span class="sxs-lookup"><span data-stu-id="c7015-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="c7015-112">Stillinger vises nå på riktig måte basert på startdatoen for ansettelsen.</span><span class="sxs-lookup"><span data-stu-id="c7015-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="c7015-113">Avslutningsdatoen vises basert på brukerinnstillinger</span><span class="sxs-lookup"><span data-stu-id="c7015-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="c7015-114">Har gjort en endring i listen over tidligere ansatte for å ta hensyn til alle tidssoneforskyvninger for den foretrukne tidssonen for ansatte når du viser avslutningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="c7015-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="c7015-115">Koblinger til Arbeidselementer som er tilordnet til meg viser ikke riktig informasjon</span><span class="sxs-lookup"><span data-stu-id="c7015-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="c7015-116">Med denne endringer vil navigasjon til detaljene i de individuelle arbeidselementene i listen vise riktig informasjon for det valgte elementet.</span><span class="sxs-lookup"><span data-stu-id="c7015-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="c7015-117">Dette problemet oppstod bare med avanserte sikkerhetsalternativer.</span><span class="sxs-lookup"><span data-stu-id="c7015-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="c7015-118">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="c7015-118">Known issue</span></span>

- <span data-ttu-id="c7015-119">**Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene.</span><span class="sxs-lookup"><span data-stu-id="c7015-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="c7015-120">**Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="c7015-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c7015-121">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="c7015-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c7015-122">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="c7015-122">(This issue will be fixed in the next platform update.)</span></span>
