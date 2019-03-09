---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (24. september 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305643"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a><span data-ttu-id="b2354-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (24. september 2018)</span><span class="sxs-lookup"><span data-stu-id="b2354-103">What's new or changed in Dynamics 365 for Talent Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2354-104">**Build 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="b2354-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="b2354-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="b2354-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="b2354-106">Valutaen lagt til i Fordeler</span><span class="sxs-lookup"><span data-stu-id="b2354-106">Currency added to Benefits</span></span>

<span data-ttu-id="b2354-107">Fordelsplaner er oppdatert for å inkludere valutaen for fordelen.</span><span class="sxs-lookup"><span data-stu-id="b2354-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="b2354-108">Dette nye feltet er også tilgjengelig på fordeler registrert av arbeider.</span><span class="sxs-lookup"><span data-stu-id="b2354-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="b2354-109">Dette nye feltet er en del av vedlikeholdsfordelene og sikkerhetsrettigheten Vis en liste over fordeler.</span><span class="sxs-lookup"><span data-stu-id="b2354-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="b2354-110">Oppdatere fordelingsprosessen - permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="b2354-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="b2354-111">Organisasjoner belønner de ansatte med fritid på forskjellige måter, basert på når ansatte starter hos og forlater firmaet.</span><span class="sxs-lookup"><span data-stu-id="b2354-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="b2354-112">For ansatte som forlater organisasjonen, må noen avslutte bonusen på avslutningsdatoen, mens andre er avhengige av den siste arbeidsdagen for å stoppe avsetningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b2354-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="b2354-113">Disse endringene gir organisasjoner muligheten til å velge når de vil avslutte registrering i løpet av avslutningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b2354-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="b2354-114">Disse nye alternativene er en del av rettighetene for Si opp en arbeider, og Avslutt en arbeider fra lederselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="b2354-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="b2354-115">Andre endringer</span><span class="sxs-lookup"><span data-stu-id="b2354-115">Other changes</span></span>

<span data-ttu-id="b2354-116">Denne versjonen inneholder flere andre feilrettinger.</span><span class="sxs-lookup"><span data-stu-id="b2354-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="b2354-117">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="b2354-117">Known Issue</span></span>

-   <span data-ttu-id="b2354-118">**Problem:** Når du legger til en ny tilknytning til en arbeider, er knappenei **Ny** og **Rediger** nedtonet. **Løsning:** Før du åpner vedleggssiden, må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="b2354-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="b2354-119">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="b2354-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="b2354-120">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="b2354-120">(This issue will be fixed in the next platform update.)</span></span>
