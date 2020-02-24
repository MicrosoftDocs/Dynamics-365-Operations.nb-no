---
title: Definere organisasjonshierarkier
description: Dette emnet beskriver hvordan du setter opp organisasjonshierarkier i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002341"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="fa70a-103">Definere organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="fa70a-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fa70a-104">Dette emnet beskriver hvordan du setter opp organisasjonshierarkier i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fa70a-104">This topic descibes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fa70a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="fa70a-105">Overview</span></span>

<span data-ttu-id="fa70a-106">Før du oppretter kanaler, må du definere organisasjonshierarkiene dine.</span><span class="sxs-lookup"><span data-stu-id="fa70a-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="fa70a-107">Du kan bruke organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver.</span><span class="sxs-lookup"><span data-stu-id="fa70a-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="fa70a-108">Du kan for eksempel definere ett hierarki for avgiftsrapportering, juridisk eller lovpålagt rapportering.</span><span class="sxs-lookup"><span data-stu-id="fa70a-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="fa70a-109">Du kan deretter definere et annet hierarki for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til intern rapportering.</span><span class="sxs-lookup"><span data-stu-id="fa70a-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="fa70a-110">Før du oppretter et organisasjonshierarki, må du opprette organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="fa70a-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="fa70a-111">Hvis du vil ha mer informasjon, kan du se [Opprette juridiske enheter](channels-legal-entities.md) eller [Opprette driftsenheter](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fa70a-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="fa70a-112">Hvis du vil ha mer informasjon, kan du se følgende emner.</span><span class="sxs-lookup"><span data-stu-id="fa70a-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="fa70a-113">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="fa70a-113">Organizations and organizational hierarchies overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [<span data-ttu-id="fa70a-114">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="fa70a-114">Plan your organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="fa70a-115">Opprette et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="fa70a-115">Create an organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="fa70a-116">Opprette et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="fa70a-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="fa70a-117">Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="fa70a-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="fa70a-118">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Organisasjonshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="fa70a-119">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fa70a-120">Angi en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="fa70a-121">I **Formål**-delen velger du **Tilordne formål**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="fa70a-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fa70a-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="fa70a-123">Velg et formål som skal tilordnes til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fa70a-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="fa70a-124">I delen **Tilordnede hierarkier** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="fa70a-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fa70a-125">In the list, mark the selected row.</span></span> <span data-ttu-id="fa70a-126">Finn hierarkiet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="fa70a-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="fa70a-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-127">Select **OK**.</span></span>

<span data-ttu-id="fa70a-128">Det følgende bildet viser et eksempel på et organisasjonshierarki som er opprettet for et fiktivt "Adventure Works"-sett med butikker.</span><span class="sxs-lookup"><span data-stu-id="fa70a-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Eksempel på organisasjonshierarki](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="fa70a-130">Legge til organisasjoner i et hierarki</span><span class="sxs-lookup"><span data-stu-id="fa70a-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="fa70a-131">Hvis du vil legge til organisasjoner i et hierarki, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="fa70a-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="fa70a-132">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fa70a-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="fa70a-133">Velg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fa70a-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="fa70a-134">Velg **Vis** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fa70a-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="fa70a-135">Legg til organisasjoner etter behov.</span><span class="sxs-lookup"><span data-stu-id="fa70a-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="fa70a-136">Hvis du vil legge til en organisasjon, velger du **Rediger** og deretter **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="fa70a-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="fa70a-137">Når du er ferdig med endringene, kan du lagre en kladd og publisere endringene.</span><span class="sxs-lookup"><span data-stu-id="fa70a-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="fa70a-138">Det følgende bildet viser en juridisk enhet som er lagt til i hierarkiroten med fire kostsentre som er lagt til for kanalene "Kjøpesenter", "Utsalgssted", "Nett" og "Telefonsenter".</span><span class="sxs-lookup"><span data-stu-id="fa70a-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="fa70a-139">Det kan også legges til diverse typer detaljhandel-, telefonsenter- og Internett-kanaler.</span><span class="sxs-lookup"><span data-stu-id="fa70a-139">Various retail, call center and online channels can then be added to each.</span></span>

![Eksempel på hierarkiutformer](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="fa70a-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fa70a-141">Additional resources</span></span>

[<span data-ttu-id="fa70a-142">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="fa70a-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="fa70a-143">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="fa70a-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="fa70a-144">Opprett juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="fa70a-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="fa70a-145">Opprette driftsenheter</span><span class="sxs-lookup"><span data-stu-id="fa70a-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="fa70a-146">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="fa70a-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fa70a-147">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="fa70a-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
