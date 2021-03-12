---
title: Bedriftskonsept i Dataverse
description: Dette emnet beskriver integreringen av firmadata mellom Finance and Operations og Dataverse .
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: bbe634b87b3cb30ed993f9b3afeb4321d70f07e6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744885"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="d3cc6-103">Bedriftskonsept i Dataverse</span><span class="sxs-lookup"><span data-stu-id="d3cc6-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="d3cc6-104">I Finance and Operations er konseptet av et *selskap* både en juridisk konstruksjon og en virksomhetskonstruksjon.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="d3cc6-105">Det er også en sikkerhets- og synlighetsgrense for data.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="d3cc6-106">Brukerne arbeider alltid i sammenheng med et enkelt selskap, og de fleste dataene er stripete av selskapet.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="d3cc6-107">Dataverse ikke har et tilsvarende begrep.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="d3cc6-108">Det nærmeste konseptet er *forretningsenhet*, som hovedsakelig er en sikkerhets- og synlighetsgrense for brukerdata.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="d3cc6-109">Dette konseptet har ikke de samme juridiske eller forretningsmessige implikasjoner som selskapskonsept.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="d3cc6-110">Fordi forretningsenhet og firma ikke er identiske konsepter, er det ikke mulig å tvinge en en-til-en (1:1) tilordning mellom dem for formålet Dataverse-integrering.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="d3cc6-111">Siden brukere imidlertid som standard må kunne se de samme radene i programmet og Dataverse, har Microsoft innført en ny tabell i Dataverse kalt cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="d3cc6-112">Denne tabellen tilsvarer Firma-tabellen i programmet.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="d3cc6-113">For å garantere at synligheten til rader er lik mellom programmet og Dataverse fra starten av, anbefaler vi følgende oppsett for data i Dataverse:</span><span class="sxs-lookup"><span data-stu-id="d3cc6-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="d3cc6-114">For hver Finance and Operations Company-rad som er aktivert for dobbel skriving, opprettes det en tilknyttet cdm\_Company-rad.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="d3cc6-115">Når en cdm\_Company-rad opprettes og aktiveres for dobbel skriving, opprettes det en standard forretningsenhet som har samme navn.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="d3cc6-116">Selv om det opprettes automatisk et standardteam for denne forretningsenheten, brukes ikke forretningsenheten.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="d3cc6-117">Det opprettes et separat eierteam som har samme navn.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="d3cc6-118">Det er også knyttet til forretningsenheten.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="d3cc6-119">Som standard er eieren av enhver rad som er opprettet og dobbeltskrevet til Dataverse, satt til DW Owner-teamet som er koblet til den tilknyttede forretningsenheten.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="d3cc6-120">Illustrasjonen nedenfor viser et eksempel på dette dataoppsettet i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Dataoppsett i Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="d3cc6-122">På grunn av denne konfigurasjonen eies alle rader som er relatert til USMF-firmaet, av et team som er koblet til USMF-forretningsenheten i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="d3cc6-123">Derfor kan en hvilken som helst bruker som har tilgang til denne forretningsenheten gjennom en sikkerhetsrolle som er satt til synlighet på forretningsenhetsnivå, nå se disse radene.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="d3cc6-124">Følgende eksempel viser hvordan grupper kan brukes til å gi riktig tilgang til disse radene.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="d3cc6-125">Rollen "Salgssjef" er tilordnet medlemmer av "USMF Sales"-teamet.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="d3cc6-126">Brukere som har Salgssjef-rollen, kan få tilgang til alle kontorader som er medlemmer av samme forretningsenhet som de er medlemmer av.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="d3cc6-127">"USMF Sales"-teamet er knyttet til USMF-forretningsenheten som ble nevnt tidligere.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="d3cc6-128">Derfor kan medlemmer av "USMF Sales"-teamet se alle kontoer som eies av "USMF DW"-brukeren, som ville ha kommet fra USMF-firmatabellen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Hvordan team kan brukes](media/dual-write-company-2.png)

<span data-ttu-id="d3cc6-130">Som den foregående illustrasjonen viser, er denne 1:1-tilordningen mellom forretningsenhet, firma og team bare et utgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="d3cc6-131">I dette eksemplet opprettes en ny forretningsenhet for "Europa" manuelt i Dataverse som overordnet for både DEMF og ESMF.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="d3cc6-132">Denne nye rotforretningsenheten er ikke relatert til dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="d3cc6-133">Den kan imidlertid brukes til å gi medlemmer av "EUR Sales"-gruppen tilgang til kontodata i både DEMF og ESMF ved å angi data synligheten til **overordnet/underordnet bu** i den tilknyttede sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="d3cc6-134">Et siste emne for å diskutere er hvordan dobbel skriving bestemmer hvilket eierteam det skal tildeles rader til.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="d3cc6-135">Denne virkemåten styres av kolonnen **Standard eiende team** i cdm\_Company-raden.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="d3cc6-136">Når en cdm\_Company-rad er aktivert for dobbel skriving, oppretter en plugin-modul automatisk den tilknyttede forretningsenheten og eiergruppen (hvis den ikke allerede finnes), og angir kolonnen **Standard eiende team**.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="d3cc6-137">Administratoren kan endre denne kolonnen til en annen verdi.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="d3cc6-138">Administratoren kan imidlertid ikke tømme kolonnen så lenge tabellen er aktivert for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="d3cc6-139">![Kolonnen Standard eiende team](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="d3cc6-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="d3cc6-140">Selskapets striping og bootstrapping</span><span class="sxs-lookup"><span data-stu-id="d3cc6-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="d3cc6-141">Dataverse-integrasjon bringer selskapet paritet ved hjelp av en bedrifts-ID til stripe data.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="d3cc6-142">Som følgende illustrasjon viser, er alle firmaspesifikke tabeller utvidet slik at de har en mange-til-én-relasjon (N:1) til cdm\_Company-tabellen.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="d3cc6-143">![N:1-relasjon mellom en firmaspesifikk tabell og cdm_Company-tabellen](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="d3cc6-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="d3cc6-144">Når et selskap er lagt til og lagret for rader, blir verdien skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="d3cc6-145">Derfor bør brukerne sørge for at de velger riktig firma.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="d3cc6-146">Bare rader som har firmadata, er kvalifisert for dobbelt skriving mellom programmet og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="d3cc6-147">For eksisterende Dataverse-data, en admin-ledet bootstrapping-erfaring vil snart være anvendelig.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="d3cc6-148">Autofylling av firmanavn i Customer Engagement-apper</span><span class="sxs-lookup"><span data-stu-id="d3cc6-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="d3cc6-149">Det finnes flere måter å fylle ut firmanavnet på automatisk i Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="d3cc6-150">Hvis du er systemansvarlig, kan du velge standardfirmaet ved å navigere til **Avanserte innstillinger > System > Sikkerhet > Brukere**.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="d3cc6-151">Åpne **Bruker**-skjemaet, og i delen **Organisasjonsinformasjon** angir du verdien for **firma som standard på skjemaer**.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Angi standardfirma i delen Organisasjonsinformasjon.":::

+ <span data-ttu-id="d3cc6-153">Hvis du har **Skrive**-tilgang til **SystemUser**-tabellen for nivået **Forretningsenhet**, kan du endre standardfirmaet i et hvilket som helst skjema ved å velge et firma på rullegardinmenyen **Firma**.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Endre firmanavnet på en ny forretningsforbindelse.":::

+ <span data-ttu-id="d3cc6-155">Hvis du har **Skrive**-tilgang til data i flere firmaer, kan du endre standardfirmaet ved å velge en rad som tilhører et annet firma.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Hvis du velger en rad, endres standardfirmaet.":::

+ <span data-ttu-id="d3cc6-157">Hvis du er en systemkonfigurator eller -administrator, og du vil fylle ut firmadata automatisk i et egendefinert skjema, kan du bruke [skjemahendelser](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="d3cc6-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="d3cc6-158">Legg til en JavaScript-referanse i **msdyn_/DefaultCompany.js**, og bruk følgende hendelser.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="d3cc6-159">Du kan bruke et hvilket som helst standardskjema, for eksempel i skjemaet for **Forretningsforbindelse**.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="d3cc6-160">**OnLoad**-hendelsen for skjemaet: Angi **defaultCompany**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="d3cc6-161">**OnChange**-hendelse for **Firma**-kolonnen: Angi kolonnen **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="d3cc6-162">Bruk filtrering basert på firmakonteksten</span><span class="sxs-lookup"><span data-stu-id="d3cc6-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="d3cc6-163">Hvis du vil bruke filtrering basert på firmakonteksten i de egendefinerte skjemaene eller på egendefinerte oppslagskolonner som er lagt til i standardskjemaene, åpner du skjemaet og bruker delen **Relatert oppføringsfiltrering** til å bruke firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="d3cc6-164">Du må angi dette for hver oppslagskolonne som krever filtrering, basert på det underliggende firmaet for en gitt rad.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="d3cc6-165">Innstillingen vises for **Forretningsforbindelse** i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="d3cc6-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Bruk firmakontekst":::

