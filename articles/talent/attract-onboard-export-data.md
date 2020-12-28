---
title: Eksportere data fra Attract og Onboard
description: Eksportere data fra Dynamics 365 Talent – Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462059"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="e71be-103">Eksportere data fra Attract og Onboard</span><span class="sxs-lookup"><span data-stu-id="e71be-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e71be-104">Som annonsert i [Trekke tilbake Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apper](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), trekker vi tilbake Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard 1. februar 2022.</span><span class="sxs-lookup"><span data-stu-id="e71be-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="e71be-105">For å hjelpe med migreringen til et annet produkt, tilbyr begge appene nå dataeksportmuligheter.</span><span class="sxs-lookup"><span data-stu-id="e71be-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="e71be-106">Eksportere data fra Attract</span><span class="sxs-lookup"><span data-stu-id="e71be-106">Export data from Attract</span></span>

<span data-ttu-id="e71be-107">Du kan eksportere dataene uten å begrense tilgangen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="e71be-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="e71be-108">Det kan være lurt å gjøre dette for testformål eller for å forstå datastrukturen vår.</span><span class="sxs-lookup"><span data-stu-id="e71be-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="e71be-109">Når du er klar til å overføre, kan du begrense tilgangen til Attract-miljøet ditt ved hjelp av instruksjonene etter denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="e71be-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="e71be-110">Sørg for at du eksporterer dataene dine igjen.</span><span class="sxs-lookup"><span data-stu-id="e71be-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="e71be-111">Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="e71be-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="e71be-112">Under **Dataeksport** velg **Be om en dataeksport**.</span><span class="sxs-lookup"><span data-stu-id="e71be-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="e71be-113">Be om en dataeksport fra Attract</span><span class="sxs-lookup"><span data-stu-id="e71be-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="e71be-114">Når meldingsboksen **Forespørselen din er under behandling** vises, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e71be-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="e71be-115">Dataeksporten kan ta opptil 20 minutter, avhengig av størrelsen på eksporten.</span><span class="sxs-lookup"><span data-stu-id="e71be-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="e71be-116">Når eksporten er fullført, velger du **Last ned**-knappen ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="e71be-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="e71be-117">Alle dataeksporter er tilgjengelige i sju dager, hvoretter **Last ned**-koblingen utløper.</span><span class="sxs-lookup"><span data-stu-id="e71be-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="e71be-118">Nedlastingen inneholder en ZIP-fil med Attract-dataene dine, inkludert følgende mapper:</span><span class="sxs-lookup"><span data-stu-id="e71be-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="e71be-119">Mappenavn</span><span class="sxs-lookup"><span data-stu-id="e71be-119">Folder name</span></span> | <span data-ttu-id="e71be-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e71be-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="e71be-121">Administrasjonsinnstillinger</span><span class="sxs-lookup"><span data-stu-id="e71be-121">Admin settings</span></span> | <span data-ttu-id="e71be-122">Konfigurasjoner for Attract-administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="e71be-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="e71be-123">Kandidater</span><span class="sxs-lookup"><span data-stu-id="e71be-123">Candidates</span></span> | <span data-ttu-id="e71be-124">Alle kandidater som er lagt til jobber eller talentsamlinger.</span><span class="sxs-lookup"><span data-stu-id="e71be-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="e71be-125">E-postmaler</span><span class="sxs-lookup"><span data-stu-id="e71be-125">Email templates</span></span> | <span data-ttu-id="e71be-126">Alle e-postmaler som er konfigurert for miljøet.</span><span class="sxs-lookup"><span data-stu-id="e71be-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="e71be-127">Jobbtilbudspakkemaler</span><span class="sxs-lookup"><span data-stu-id="e71be-127">Job offer package templates</span></span> | <span data-ttu-id="e71be-128">Alle jobbtilbudspakkemalene som er opprettet, pluss de tilknyttede konfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="e71be-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="e71be-129">Regelsett for jobbtilbud</span><span class="sxs-lookup"><span data-stu-id="e71be-129">Job offer rule sets</span></span> |  <span data-ttu-id="e71be-130">Alle regelsettfiler som er lastet opp for tilbudsbehandling.</span><span class="sxs-lookup"><span data-stu-id="e71be-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="e71be-131">Jobbtilbudsmaler</span><span class="sxs-lookup"><span data-stu-id="e71be-131">Job offer templates</span></span> | <span data-ttu-id="e71be-132">Alle dokumentmaler for jobbtilbud som er opprettet for miljøet.</span><span class="sxs-lookup"><span data-stu-id="e71be-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="e71be-133">Ledige stillinger</span><span class="sxs-lookup"><span data-stu-id="e71be-133">Job openings</span></span> | <span data-ttu-id="e71be-134">Alle opprettede jobber.</span><span class="sxs-lookup"><span data-stu-id="e71be-134">All created jobs.</span></span> <span data-ttu-id="e71be-135">Slettede jobber eksporteres ikke.</span><span class="sxs-lookup"><span data-stu-id="e71be-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="e71be-136">Undermappene inneholder kandidatsøknader, med undermapper for vedlegg til kandidatsøknader og tilbudspakker der det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="e71be-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="e71be-137">Maler for ledige stillinger</span><span class="sxs-lookup"><span data-stu-id="e71be-137">Job opening templates</span></span> | <span data-ttu-id="e71be-138">Jobbprosessmaler som er konfigurert i miljøet.</span><span class="sxs-lookup"><span data-stu-id="e71be-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="e71be-139">Talentsamlinger</span><span class="sxs-lookup"><span data-stu-id="e71be-139">Talent pools</span></span> | <span data-ttu-id="e71be-140">Alle opprettede talentsamlinger, deres bidragsyterlister og kandidatlistene for talentsamlingene.</span><span class="sxs-lookup"><span data-stu-id="e71be-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="e71be-141">Arbeidere</span><span class="sxs-lookup"><span data-stu-id="e71be-141">Workers</span></span> | <span data-ttu-id="e71be-142">Liste over alle arbeiderne som finnes i miljøet, pluss deres roller.</span><span class="sxs-lookup"><span data-stu-id="e71be-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="e71be-143">(rotmappe)</span><span class="sxs-lookup"><span data-stu-id="e71be-143">(root folder)</span></span> | <span data-ttu-id="e71be-144">En JSON-skjemafil som beskriver datastrukturfeltene.</span><span class="sxs-lookup"><span data-stu-id="e71be-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="e71be-145">Begrense tilgang til Attract</span><span class="sxs-lookup"><span data-stu-id="e71be-145">Restrict access to Attract</span></span>

<span data-ttu-id="e71be-146">Når du er klar til å overføre, kan du begrense tilgangen for ikke-administratorer til Attract-miljøet ditt og eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="e71be-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="e71be-147">Begrensning av tilgang til Attract-miljøet ditt er permanent og kan ikke angres.</span><span class="sxs-lookup"><span data-stu-id="e71be-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="e71be-148">Hvis du vil at ikke-administrative brukere skal kunne fortsette å få tilgang til miljøet ditt, hopper du over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="e71be-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="e71be-149">Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="e71be-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="e71be-150">Hvis du vil begrense tilgangen for ikke-administratorer til Attract-miljøet ditt, velger du **Begrens tilgang nå** under **Begrens tilgang til denne appen**.</span><span class="sxs-lookup"><span data-stu-id="e71be-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="e71be-151">Når du begrenser tilgangen, oppheves også posteringen av eventuelle aktive jobber som er postert.</span><span class="sxs-lookup"><span data-stu-id="e71be-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="e71be-152">Begrense tilgang for ikke-administratorer til Attract</span><span class="sxs-lookup"><span data-stu-id="e71be-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="e71be-153">Når du ser advarselen **Dette er en permanent endring**, velger du **Begrens tilgang** for å begrense ikke-administrative brukere permanent fra dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="e71be-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="e71be-154">Hvis du ikke er klar til å fullføre dette trinnet, velger du **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="e71be-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="e71be-155">Advarsel om at begrensning av tilgang er en permanent endring</span><span class="sxs-lookup"><span data-stu-id="e71be-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="e71be-156">Administratorer kan fortsatt få tilgang til dataeksport- og personrapportsider etter at du har begrenset tilgang til Attract-miljøet.</span><span class="sxs-lookup"><span data-stu-id="e71be-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="e71be-157">Eksportere data fra Onboard</span><span class="sxs-lookup"><span data-stu-id="e71be-157">Export data from Onboard</span></span>

<span data-ttu-id="e71be-158">Når du er klar, kan du laste ned maler, veiledninger og kandidatdata fra Onboard.</span><span class="sxs-lookup"><span data-stu-id="e71be-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="e71be-159">Gå til [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="e71be-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="e71be-160">Under **Dataeksport** velg **Be om en dataeksport**.</span><span class="sxs-lookup"><span data-stu-id="e71be-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="e71be-161">Be om en dataeksport fra Onboard</span><span class="sxs-lookup"><span data-stu-id="e71be-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="e71be-162">Når meldingsboksen **Forespørselen din er under behandling** vises, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e71be-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="e71be-163">Dataeksporten kan ta opptil 20 minutter, avhengig av størrelsen på eksporten.</span><span class="sxs-lookup"><span data-stu-id="e71be-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="e71be-164">Når eksporten er fullført, velger du **Last ned**-knappen ved siden av den.</span><span class="sxs-lookup"><span data-stu-id="e71be-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="e71be-165">Laste ned dataeksport fra Onboard</span><span class="sxs-lookup"><span data-stu-id="e71be-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="e71be-166">Dataeksporten er tilgjengelig i sju dager.</span><span class="sxs-lookup"><span data-stu-id="e71be-166">Your data export is available for seven days.</span></span> <span data-ttu-id="e71be-167">Etter sju dager utløper **Last ned**-koblingen, og du må be om en ny eksport hvis du må laste ned dataene på nytt.</span><span class="sxs-lookup"><span data-stu-id="e71be-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="e71be-168">Når du starter en ny dataeksport, utløper eksisterende nedlastinger etter at den nye eksporten er fullført.</span><span class="sxs-lookup"><span data-stu-id="e71be-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="e71be-169">Nedlastingen er en ZIP-fil som inneholder:</span><span class="sxs-lookup"><span data-stu-id="e71be-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="e71be-170">Mappen **Maler** som inneholder Onboard-malene i Word-dokumentformat.</span><span class="sxs-lookup"><span data-stu-id="e71be-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="e71be-171">Mappen **Veiledninger** som inneholder Onboard-veiledningene i Word-dokumentformat.</span><span class="sxs-lookup"><span data-stu-id="e71be-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="e71be-172">Se også</span><span class="sxs-lookup"><span data-stu-id="e71be-172">See also</span></span>

[<span data-ttu-id="e71be-173">Trekke tilbake Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apper</span><span class="sxs-lookup"><span data-stu-id="e71be-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)