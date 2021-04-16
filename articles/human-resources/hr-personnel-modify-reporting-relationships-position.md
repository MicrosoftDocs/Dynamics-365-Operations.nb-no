---
title: Endre rapporteringsrelasjoner for en stilling
description: Denne prosedyren viser hvordan du endrer rapporteringsrelasjonen for en ansatt.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4f54a162305a81b65f0657cd572df75a9dcbd38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794451"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="701d3-103">Endre rapporteringsrelasjoner for en stilling</span><span class="sxs-lookup"><span data-stu-id="701d3-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="701d3-104">Denne prosedyren viser hvordan du endrer rapporteringsrelasjonen for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="701d3-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="701d3-105">Rapporteringsrelasjonen kan brukes for å rute dokumenter via arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="701d3-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="701d3-106">Prosedyren viser også hvordan du tilordner en ansatt til flere hierarkier.</span><span class="sxs-lookup"><span data-stu-id="701d3-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="701d3-107">En ansatt kan for eksempel være en del av et prosjektteam med en uformell rapporteringsrelasjon til en prosjektansvarlig.</span><span class="sxs-lookup"><span data-stu-id="701d3-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="701d3-108">Du kan definere flere rapporteringsrelasjoner for stillingen som passer til ulike prosjekt- eller matrisescenarier.</span><span class="sxs-lookup"><span data-stu-id="701d3-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="701d3-109">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="701d3-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="701d3-110">Gå til Personale > Stillinger > Stillinger.</span><span class="sxs-lookup"><span data-stu-id="701d3-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="701d3-111">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="701d3-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="701d3-112">Du kan for eksempel filtrere på Stilling-feltet med verdien 000091.</span><span class="sxs-lookup"><span data-stu-id="701d3-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="701d3-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="701d3-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="701d3-114">Utvid delen Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="701d3-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="701d3-115">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="701d3-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="701d3-116">Angi eller velg en verdi i feltet Rapporter til.</span><span class="sxs-lookup"><span data-stu-id="701d3-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="701d3-117">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="701d3-117">Click Create.</span></span>
8. <span data-ttu-id="701d3-118">Vis delen Relasjoner.</span><span class="sxs-lookup"><span data-stu-id="701d3-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="701d3-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="701d3-119">Click Add.</span></span>
10. <span data-ttu-id="701d3-120">Merk av i boksen til venstre i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="701d3-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="701d3-121">Angi eller velg en verdi i feltet Navn på hierarki.</span><span class="sxs-lookup"><span data-stu-id="701d3-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="701d3-122">Eksempel: Prosjekt</span><span class="sxs-lookup"><span data-stu-id="701d3-122">Example: Project</span></span>  
12. <span data-ttu-id="701d3-123">Angi eller velg en verdi i feltet Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="701d3-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="701d3-124">Eksempel: 000437</span><span class="sxs-lookup"><span data-stu-id="701d3-124">Example:  000437</span></span>
13. <span data-ttu-id="701d3-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="701d3-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]