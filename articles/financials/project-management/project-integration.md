---
title: Integrering av Microsoft Project-klient
description: Planlegging og vedlikehold av en prosjektplan kan være komplisert, slik at prosjektledere må bruke verktøy som hjelper dem med denne oppgaven. Integrasjon med Microsoft Project-klienten gir støtte for å åpne og behandle en arbeidsnedbrytningsstruktur for prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 04b76b6c097a82e73aba007bff82b58dbbd6eb17
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838349"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="e1579-104">Integrering av Microsoft Project-klient</span><span class="sxs-lookup"><span data-stu-id="e1579-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1579-105">Planlegging og vedlikehold av en prosjektplan kan være komplisert, slik at prosjektledere må bruke verktøy som hjelper dem med denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="e1579-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="e1579-106">Integrasjon med Microsoft Project-klienten gir støtte for å åpne og behandle en arbeidsnedbrytningsstruktur for prosjekt.</span><span class="sxs-lookup"><span data-stu-id="e1579-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="e1579-107">Prosjektlederen kan publisere endringer tilbake til arbeidsnedbrytningsstrukturen for prosjekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1579-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="e1579-108">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, må du installere KB 4054797 og 4055884.</span><span class="sxs-lookup"><span data-stu-id="e1579-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="e1579-109">Konfigurere Microsoft Project-klienttillegget</span><span class="sxs-lookup"><span data-stu-id="e1579-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="e1579-110">For å aktivere integrasjonen med Microsoft Project-klienten, må et Microsoft Dynamics 365-tillegg installeres på brukerens Microsoft Project-programklient.</span><span class="sxs-lookup"><span data-stu-id="e1579-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="e1579-111">Dette gjøres ved å åpne **Prosjektstyringsarbeidsområdet**.</span><span class="sxs-lookup"><span data-stu-id="e1579-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="e1579-112">•   Klikk på **Konfigurer prosjektklienttillegget** fra **Koblinger** > **Oppsett**-delen i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="e1579-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="e1579-113">•   Klikk på **Åpne** og deretter **Kjør** når du blir spurt.</span><span class="sxs-lookup"><span data-stu-id="e1579-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="e1579-114">Åpne og redigere en eksisterende utkastarbeidsnedbrytningsstruktur i Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="e1579-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="e1579-115">Hvis et prosjekt i Finance and Operations allerede har opprettet en arbeidsnedbrytningsstruktur, kan arbeidsnedbrytningsstrukturen åpnes i Microsoft Project-klientprogrammet hvis arbeidsnedbrytningsstrukturen har statusen Utkast.</span><span class="sxs-lookup"><span data-stu-id="e1579-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="e1579-116">Hvis du vil åpne fra **Prosjekt**-siden, klikker du **Åpne i Microsoft Project**-koblingen fra **Plan**-kategorien. Denne siden kan også åpnes fra Microsoft Project-klientprogrammet ved å klikke **Åpne** i **Microsoft Dynamics 365**-kategorien. Velg **Juridisk enhet** og **Prosjekt** fra listen.</span><span class="sxs-lookup"><span data-stu-id="e1579-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="e1579-117">Hvis du bruker Internet Explorer som nettleser, må du klikke **Lagre** for å åpne manuelt fra plasseringen som filen er lastet ned til.</span><span class="sxs-lookup"><span data-stu-id="e1579-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="e1579-118">Eller klikk **Lagre og åpne** for å åpne filen i Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="e1579-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="e1579-119">Ikke endre navn på filnavnet når du lagrer.</span><span class="sxs-lookup"><span data-stu-id="e1579-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="e1579-120">Før du gjør endringer i filen ved hjelp av Microsoft Project-klienten, må du sjekke den ut. Klikk **Sjekk ut** i **Microsoft Dynamics 365**-kategorien. Dette hindrer andre brukere i å redigere arbeidsnedbrytningsstrukturen innenfra Finance and Operations samtidig.</span><span class="sxs-lookup"><span data-stu-id="e1579-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="e1579-121">For å publisere arbeidsnedbrytningsstrukturen når du har fullført alle endringer, klikker du på **Sjekk inn** i **Microsoft Dynamics 365**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="e1579-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="e1579-122">Hvis en prosjektgruppe allerede er lagt til prosjektet i Finance and Operations, fylles ressurslisten ut med gruppemedlemmene.</span><span class="sxs-lookup"><span data-stu-id="e1579-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="e1579-123">Hvis en prosjektgruppe ennå ikke er lagt til i prosjektet, kan du velge ressurser og bygge teamet i Microsoft Project-klienten ved å klikke **Ressurser**-knappen i **Microsoft Dynamics 365**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="e1579-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="e1579-124">Følgende data blir synkronisert tilbake til Finance and Operations som en del av sjekken som pågår:</span><span class="sxs-lookup"><span data-stu-id="e1579-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="e1579-125">•   Oppgavenavn</span><span class="sxs-lookup"><span data-stu-id="e1579-125">•   Task name</span></span>

<span data-ttu-id="e1579-126">•   Startdato</span><span class="sxs-lookup"><span data-stu-id="e1579-126">•   Start date</span></span>

<span data-ttu-id="e1579-127">•   Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="e1579-127">•   Finish date</span></span>

<span data-ttu-id="e1579-128">•   Foregående aktiviteter</span><span class="sxs-lookup"><span data-stu-id="e1579-128">•   Predecessors</span></span>

<span data-ttu-id="e1579-129">•   Ressursnavn</span><span class="sxs-lookup"><span data-stu-id="e1579-129">•   Resource names</span></span>

<span data-ttu-id="e1579-130">•   Kategori</span><span class="sxs-lookup"><span data-stu-id="e1579-130">•   Category</span></span>

<span data-ttu-id="e1579-131">•   Ressurskategori</span><span class="sxs-lookup"><span data-stu-id="e1579-131">•   Resource category</span></span>

<span data-ttu-id="e1579-132">•   Arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="e1579-132">•   Work hours</span></span>

<span data-ttu-id="e1579-133">•   Merknader</span><span class="sxs-lookup"><span data-stu-id="e1579-133">•   Notes</span></span>

<span data-ttu-id="e1579-134">•   Prioritet</span><span class="sxs-lookup"><span data-stu-id="e1579-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="e1579-135">Hvis du legger til andre kolonner i Microsoft Project-klientfilen, vil de ikke bli lagret i filen, og ikke vises når filen åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="e1579-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="e1579-136">Opprette arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="e1579-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="e1579-137">Når du skal opprette en ny arbeidsnedbrytningsstruktur ved hjelp av Microsoft Project-klienten, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="e1579-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="e1579-138">Åpne Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="e1579-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e1579-139">I kategorien **Microsoft Dynamics 365** klikker du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="e1579-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="e1579-140">Velg **Juridisk enhet** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="e1579-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="e1579-141">Velg **prosjektet**.</span><span class="sxs-lookup"><span data-stu-id="e1579-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="e1579-142">Klikk på **Sjekk ut** i kategorien **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e1579-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="e1579-143">Når du er klar til å publisere til Finance and Operations, klikker du **Sjekk inn** i **Microsoft Dynamics 365**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="e1579-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="e1579-144">Erstatt den eksisterende arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="e1579-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="e1579-145">Hvis du vil opprette en ny arbeidsnedbrytningsstruktur ved hjelp av Microsoft Project-klienten og erstatte en eksisterende arbeidsnedbrytningsstruktur for et eksisterende prosjekt, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="e1579-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="e1579-146">Åpne Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="e1579-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e1579-147">Opprett tidsplanen i Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="e1579-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="e1579-148">I **Microsoft Dynamics 365**-kategorien klikker du **Lagre endringer** > **Erstatt eksisterende prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="e1579-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="e1579-149">Velg **Juridisk enhet** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="e1579-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="e1579-150">Velg **prosjektet**.</span><span class="sxs-lookup"><span data-stu-id="e1579-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="e1579-151">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1579-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="e1579-152">Opprette et nytt prosjekt fra Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="e1579-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="e1579-153">Åpne Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="e1579-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e1579-154">Opprett tidsplanen i Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="e1579-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="e1579-155">I **Microsoft Dynamics 365**-kategorien klikker du **Lagre endringer** > **Lagre i nytt prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="e1579-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="e1579-156">Velg **Juridisk enhet** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="e1579-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="e1579-157">Angi **prosjekt-ID**-en om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e1579-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="e1579-158">Skriv inn **prosjektnavnet**.</span><span class="sxs-lookup"><span data-stu-id="e1579-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="e1579-159">Velg **prosjekttype**, **prosjektgruppe** og **prosjektkontrakt-ID**.</span><span class="sxs-lookup"><span data-stu-id="e1579-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="e1579-160">Du kan eventuelt opprette en ny prosjektkontrakt ved å klikke **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e1579-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="e1579-161">Velg **Kalender** som skal brukes for ressurser.</span><span class="sxs-lookup"><span data-stu-id="e1579-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="e1579-162">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1579-162">Click **OK**.</span></span>
