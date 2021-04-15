---
title: Aktivere og konfigurere automatiske avregninger etter kanal
description: Dette emnet forklarer hvordan du aktiverer og konfigurerer automatiske gebyrer per kanal i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 23d02cf96faf3753303435acc148bf71e487d791
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799924"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="5795a-103">Aktivere og konfigurere automatiske avregninger etter kanal</span><span class="sxs-lookup"><span data-stu-id="5795a-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="5795a-104">Dette emnet forklarer hvordan du aktiverer og konfigurerer automatiske gebyrer per kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5795a-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5795a-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="5795a-105">Overview</span></span>

<span data-ttu-id="5795a-106">Du kan ha scenarioer der resirkuleringsgebyrer eller andre gebyrer må brukes på en gruppe produkter som selges i alle eller enkelte butikker i en bestemt delstat (for eksempel California).</span><span class="sxs-lookup"><span data-stu-id="5795a-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="5795a-107">Med funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** i Commerce kan du angi automatiske gebyrer per kanal (for eksempel en bestemt fysisk kanal).</span><span class="sxs-lookup"><span data-stu-id="5795a-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="5795a-108">Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.10 og senere.</span><span class="sxs-lookup"><span data-stu-id="5795a-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="5795a-109">Du må fullføre følgende oppgaver for å aktivere og konfigurere automatiske gebyrer per kanal:</span><span class="sxs-lookup"><span data-stu-id="5795a-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="5795a-110">Aktiver funksjonen **Aktiver filtrering av automatiske gebyrer per kanal**.</span><span class="sxs-lookup"><span data-stu-id="5795a-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="5795a-111">Konfigurer formålet for organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="5795a-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="5795a-112">Definer automatiske gebyrer per kanal.</span><span class="sxs-lookup"><span data-stu-id="5795a-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="5795a-113">Funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** fungerer bare hvis funksjonen for avanserte automatiske gebyrer også er aktivert.</span><span class="sxs-lookup"><span data-stu-id="5795a-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="5795a-114">Hvis du vil ha informasjon om hvordan du aktiverer funksjonen for avanserte automatiske gebyrer, kan du se [Avanserte automatiske gebyrer for omnikanal](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="5795a-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="5795a-115">Aktivere funksjonen Aktiver filtrering av automatiske gebyrer per kanal</span><span class="sxs-lookup"><span data-stu-id="5795a-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="5795a-116">Følg denne fremgangsmåten for å aktivere automatiske gebyrer per kanal i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5795a-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5795a-117">Gå til **Systemadministrator \> Arbeidsområder \> Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="5795a-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="5795a-118">I kategorien **Ikke aktivert**, i listen **Funksjonsnavn** finner og velger du **Aktiver filtrering av automatiske gebyrer per kanal**.</span><span class="sxs-lookup"><span data-stu-id="5795a-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="5795a-119">Velg **Aktiver nå** i hjørnet nederst til høyre.</span><span class="sxs-lookup"><span data-stu-id="5795a-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="5795a-120">Når funksjonen er slått på, vil den vises i listen i kategorien **Alle**.</span><span class="sxs-lookup"><span data-stu-id="5795a-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="5795a-121">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="5795a-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5795a-122">I venstre rute finner du og velger jobben **1110** (**Global konfigurasjon**).</span><span class="sxs-lookup"><span data-stu-id="5795a-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="5795a-123">Velg **Kjør nå** i handlingsruten for å overføre konfigurasjonsendringene.</span><span class="sxs-lookup"><span data-stu-id="5795a-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="5795a-124">Hvis du deaktiverer funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** etter at du allerede har brukt den, vises ikke feltet **Relasjon med detaljhandelskanal** under **Automatiske gebyrer** lenger, og du mister alle eksisterende konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="5795a-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="5795a-125">Hvis fjerning av konfigurasjonene for **Relasjon med detaljhandelskanal** forårsaker duplisering av regler for automatiske gebyrer, vil et forsøk på å deaktivere funksjonen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="5795a-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="5795a-126">Før du slår av funksjonen, må du passe på å se gjennom alle regler for automatiske gebyrer og foreta eventuelle endringer som kreves.</span><span class="sxs-lookup"><span data-stu-id="5795a-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="5795a-127">Konfigurere formålet for organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="5795a-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="5795a-128">Et nytt formål for organisasjonshierarki kalt **Automatisk gebyr for detaljhandel** er opprettet for å administrere hierarkiet for automatiske gebyrer per kanal.</span><span class="sxs-lookup"><span data-stu-id="5795a-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="5795a-129">Følg denne fremgangsmåten for å tilordne et standardhierarki til et formål for organisasjonshierarki i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5795a-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="5795a-130">Gå til **Organisasjonsstyring \> Organisasjoner \> Formål for organisasjonshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="5795a-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="5795a-131">I den venstre ruten velger du **Automatisk gebyr for detaljhandel**.</span><span class="sxs-lookup"><span data-stu-id="5795a-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="5795a-132">Under **Tilordnede hierarkier** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="5795a-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="5795a-133">I dialogboksen **Organisasjonshierarkier** velger du et organisasjonshierarki (for eksempel **Detaljhandelbutikker etter område**), og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="5795a-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="5795a-134">Under **Tilordnede hierarkier** velger du **Bruk som standard**.</span><span class="sxs-lookup"><span data-stu-id="5795a-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="5795a-135">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="5795a-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5795a-136">I venstre rute finner du og velger jobben **1040** (**Produkter**).</span><span class="sxs-lookup"><span data-stu-id="5795a-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="5795a-137">Velg **Kjør nå** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5795a-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="5795a-138">Gjenta de to forrige trinnene for å kjøre jobbene **1070** (**Kanalkonfigurasjon**) og **1110** (**Global konfigurasjon**).</span><span class="sxs-lookup"><span data-stu-id="5795a-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Konfigurasjon av formålet for automatisk gebyr for detaljhandel per organisasjonshierarki](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="5795a-140">Definere automatiske gebyrer per kanal</span><span class="sxs-lookup"><span data-stu-id="5795a-140">Define auto charges by channel</span></span>

<span data-ttu-id="5795a-141">Når du har aktivert funksjonen **Aktiver filtrering av automatiske gebyrer per kanal** og konfigurert formålet **Automatisk gebyr for detaljhandel** for organisasjonshierarki, kan automatiske gebyrer per kanal defineres på ordrehodenivå eller ordrelinjenivå.</span><span class="sxs-lookup"><span data-stu-id="5795a-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="5795a-142">Følg denne fremgangsmåten for å definere automatiske gebyrer per kanal i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5795a-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5795a-143">Gå til **Kunder \> Oppsett for tillegg \> Automatiske gebyrer**.</span><span class="sxs-lookup"><span data-stu-id="5795a-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="5795a-144">I den venstre ruten, i **Nivå**-feltet, velger du enten **Hode** eller **Linje**, alt etter forretningskravene dine.</span><span class="sxs-lookup"><span data-stu-id="5795a-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="5795a-145">I feltet **Detaljhandelskanalkode** velger du den aktuelle kanalkoden (for eksempel **Tabell** eller **Gruppe**).</span><span class="sxs-lookup"><span data-stu-id="5795a-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="5795a-146">Hvis standardinnstillingen **Alle** er brukt, brukes gebyrregler på alle kanaler.</span><span class="sxs-lookup"><span data-stu-id="5795a-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="5795a-147">Hvis du velger **Gruppe**, må du kontrollere at en gebyrgruppe for detaljhandelskanal opprettes under **Retail og Commerce \> Kanaloppsett \> Gebyrer \> Gebyrgrupper for detaljhandelskanal**.</span><span class="sxs-lookup"><span data-stu-id="5795a-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="5795a-148">Hvis du velger **Tabell**, kan du velge en bestemt kanal (for eksempel **San Francisco**) i feltet **Relasjon med detaljhandelskanal**.</span><span class="sxs-lookup"><span data-stu-id="5795a-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="5795a-149">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="5795a-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5795a-150">I venstre rute finner du og velger jobben **1040** (**Produkter**).</span><span class="sxs-lookup"><span data-stu-id="5795a-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="5795a-151">Velg **Kjør nå** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5795a-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="5795a-152">Gjenta de to forrige trinnene for å kjøre jobbene **1070** (**Kanalkonfigurasjon**) og **1110** (**Global konfigurasjon**).</span><span class="sxs-lookup"><span data-stu-id="5795a-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automatiske gebyrer definert per kanal](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="5795a-154">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="5795a-154">Example scenario</span></span>

<span data-ttu-id="5795a-155">I følgende eksempel vises fremgangsmåten som kreves for å konfigurere et produkt, slik at resirkuleringsgebyrer belastes når produktet selges via en fysisk kanal i San Francisco.</span><span class="sxs-lookup"><span data-stu-id="5795a-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="5795a-156">Eksemplet viser også hvordan de automatiske gebyrene vises i POS-appen (salgssted) i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5795a-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="5795a-157">Organisasjonen definerer en gebyrkode som heter **RESIRKULERING**, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="5795a-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Gebyrkoden RESIRKULERING](media/Auto-charges-charge-code.png)

<span data-ttu-id="5795a-159">Et automatisk gebyr opprettes på linjenivå.</span><span class="sxs-lookup"><span data-stu-id="5795a-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="5795a-160">Det har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="5795a-160">It has the following configuration:</span></span>

- <span data-ttu-id="5795a-161">Feltet **Kontokode** settes til **Alle**.</span><span class="sxs-lookup"><span data-stu-id="5795a-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="5795a-162">Feltet **Varekode** settes til **Tabell**.</span><span class="sxs-lookup"><span data-stu-id="5795a-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="5795a-163">Feltet **Varerelasjon** settes til produkt-ID **91001**.</span><span class="sxs-lookup"><span data-stu-id="5795a-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="5795a-164">Feltet **Kode for leveringsmåte** settes til **Alle**.</span><span class="sxs-lookup"><span data-stu-id="5795a-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="5795a-165">Feltet **Detaljhandelskanalkode** settes til **Tabell**.</span><span class="sxs-lookup"><span data-stu-id="5795a-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="5795a-166">Feltet **Relasjon med detaljhandelskanal** settes til butikken i **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="5795a-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="5795a-167">En linje for automatiske gebyrer opprettes.</span><span class="sxs-lookup"><span data-stu-id="5795a-167">An auto charges line is created.</span></span> <span data-ttu-id="5795a-168">Det har følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="5795a-168">It has the following configuration:</span></span>

- <span data-ttu-id="5795a-169">Feltet **Valuta** settes til **USD**.</span><span class="sxs-lookup"><span data-stu-id="5795a-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="5795a-170">Feltet **Tilleggskode** settes til **RESIRKULERING**.</span><span class="sxs-lookup"><span data-stu-id="5795a-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="5795a-171">Feltet **Kategori** settes til **Fast**.</span><span class="sxs-lookup"><span data-stu-id="5795a-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="5795a-172">Feltet **Gebyrer** settes til **USD 6,25**.</span><span class="sxs-lookup"><span data-stu-id="5795a-172">The **Charges** field is set to **$6.25**.</span></span>

![Konfigurasjon av automatisk gebyr på linjenivå og linjen for automatiske gebyrer](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="5795a-174">I POS-appen opprettes det en salgsordre i butikkanalen **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="5795a-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="5795a-175">Linjen **Gebyrer** viser resirkulasjonsgebyret på **USD 6,25**.</span><span class="sxs-lookup"><span data-stu-id="5795a-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="5795a-176">Ved å velge **Transaksjonsalternativer \> Gebyrer \> Behandle gebyrer** i POS-appen kan du vise gebyrkoden og beskrivelsen for resirkuleringsgebyret.</span><span class="sxs-lookup"><span data-stu-id="5795a-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Resirkuleringsgebyr i POS-appen](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="5795a-178">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5795a-178">Additional resources</span></span>

[<span data-ttu-id="5795a-179">Avanserte automatiske tillegg for omnikanal</span><span class="sxs-lookup"><span data-stu-id="5795a-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="5795a-180">Fordele hodegebyrer til samsvarende salgslinjer</span><span class="sxs-lookup"><span data-stu-id="5795a-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]