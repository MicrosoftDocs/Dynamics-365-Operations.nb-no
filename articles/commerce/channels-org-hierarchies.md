---
title: Definere organisasjonshierarkier
description: Dette emnet beskriver hvordan du setter opp organisasjonshierarkier i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800573"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="2508e-103">Definere organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="2508e-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2508e-104">Dette emnet beskriver hvordan du setter opp organisasjonshierarkier i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2508e-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2508e-105">Før du oppretter kanaler, må du definere organisasjonshierarkiene dine.</span><span class="sxs-lookup"><span data-stu-id="2508e-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="2508e-106">Du kan bruke organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver.</span><span class="sxs-lookup"><span data-stu-id="2508e-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="2508e-107">Du kan for eksempel definere ett hierarki for avgiftsrapportering, juridisk eller lovpålagt rapportering.</span><span class="sxs-lookup"><span data-stu-id="2508e-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="2508e-108">Du kan deretter definere et annet hierarki for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til intern rapportering.</span><span class="sxs-lookup"><span data-stu-id="2508e-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="2508e-109">Før du oppretter et organisasjonshierarki, må du opprette organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="2508e-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="2508e-110">Hvis du vil ha mer informasjon, kan du se [Opprette juridiske enheter](channels-legal-entities.md) eller [Opprette driftsenheter](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2508e-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="2508e-111">Hvis du vil ha mer informasjon, kan du se følgende emner.</span><span class="sxs-lookup"><span data-stu-id="2508e-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="2508e-112">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="2508e-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="2508e-113">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="2508e-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="2508e-114">Opprette et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="2508e-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="2508e-115">Opprette et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="2508e-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="2508e-116">Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="2508e-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2508e-117">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Organisasjonshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="2508e-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="2508e-118">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2508e-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2508e-119">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="2508e-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="2508e-120">I **Formål**-delen velger du **Tilordne formål**.</span><span class="sxs-lookup"><span data-stu-id="2508e-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="2508e-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2508e-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="2508e-122">Velg et formål som skal tilordnes til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="2508e-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="2508e-123">I delen **Tilordnede hierarkier** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="2508e-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="2508e-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2508e-124">In the list, mark the selected row.</span></span> <span data-ttu-id="2508e-125">Finn hierarkiet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="2508e-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="2508e-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2508e-126">Select **OK**.</span></span>

<span data-ttu-id="2508e-127">Det følgende bildet viser et eksempel på et organisasjonshierarki som er opprettet for et fiktivt "Adventure Works"-sett med butikker.</span><span class="sxs-lookup"><span data-stu-id="2508e-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Eksempel på organisasjonshierarki](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="2508e-129">Legge til organisasjoner i et hierarki</span><span class="sxs-lookup"><span data-stu-id="2508e-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="2508e-130">Hvis du vil legge til organisasjoner i et hierarki, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="2508e-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2508e-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2508e-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="2508e-132">Velg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="2508e-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="2508e-133">Velg **Vis** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2508e-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="2508e-134">Legg til organisasjoner etter behov.</span><span class="sxs-lookup"><span data-stu-id="2508e-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="2508e-135">Hvis du vil legge til en organisasjon, velger du **Rediger** og deretter **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="2508e-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="2508e-136">Når du er ferdig med endringene, kan du lagre en kladd og publisere endringene.</span><span class="sxs-lookup"><span data-stu-id="2508e-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="2508e-137">Det følgende bildet viser en juridisk enhet som er lagt til i hierarkiroten med fire kostsentre som er lagt til for kanalene "Kjøpesenter", "Utsalgssted", "Nett" og "Telefonsenter".</span><span class="sxs-lookup"><span data-stu-id="2508e-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="2508e-138">Det kan også legges til diverse typer detaljhandel-, telefonsenter- og Internett-kanaler.</span><span class="sxs-lookup"><span data-stu-id="2508e-138">Various retail, call center and online channels can then be added to each.</span></span>

![Eksempel på hierarkiutformer](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="2508e-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2508e-140">Additional resources</span></span>

[<span data-ttu-id="2508e-141">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="2508e-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2508e-142">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="2508e-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2508e-143">Opprett juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="2508e-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="2508e-144">Opprette driftsenheter</span><span class="sxs-lookup"><span data-stu-id="2508e-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2508e-145">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="2508e-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2508e-146">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="2508e-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
