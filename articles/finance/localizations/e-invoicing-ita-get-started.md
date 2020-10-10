---
title: Komme i gang med tillegget Elektronisk fakturering for Italia
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Italia i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ea0408f4ef72bf77a0659799075338e4e6b2aa30
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836008"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="7cc89-103">Komme i gang med tillegget Elektronisk fakturering for Italia</span><span class="sxs-lookup"><span data-stu-id="7cc89-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="7cc89-104">Det er ikke sikkert at tillegget Elektroniske fakturering for Italia støtter alle funksjonene som er tilgjengelige for elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7cc89-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="7cc89-105">Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Italia.</span><span class="sxs-lookup"><span data-stu-id="7cc89-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="7cc89-106">Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Services (RCS) og Finance.</span><span class="sxs-lookup"><span data-stu-id="7cc89-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="7cc89-107">Det leder deg også gjennom prosessen med å sende elektroniske fakturaer som genereres i det Italia-spesifikke **FatturaPA**-formatet via tjenesten, og det forklarer hvordan du gjennomgår resultatene av behandlingen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7cc89-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7cc89-108">Prerequisites</span></span>

<span data-ttu-id="7cc89-109">Før du fullfører trinnene i dette emnet må du fullføre trinnene i [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="7cc89-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="7cc89-110">RCS-oppsett</span><span class="sxs-lookup"><span data-stu-id="7cc89-110">RCS setup</span></span>

<span data-ttu-id="7cc89-111">Under RCS-oppsettet vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="7cc89-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="7cc89-112">Importer funksjonen for e-fakturering for eksport av elektroniske fakturaer for kunder i **FatturaPA**-formatet.</span><span class="sxs-lookup"><span data-stu-id="7cc89-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="7cc89-113">Gå gjennom formatkonfigurasjonene som kreves for å generere, sende og motta svar om elektroniske fakturaer.</span><span class="sxs-lookup"><span data-stu-id="7cc89-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="7cc89-114">Konfigurer hendelsene som støtter innsendingsscenarioene for elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="7cc89-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="7cc89-115">Publiser funksjonen for e-fakturering.</span><span class="sxs-lookup"><span data-stu-id="7cc89-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="7cc89-116">"E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="7cc89-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="7cc89-117">I dette tilfellet er eksport av elektroniske fakturaer for kunder e-fakturafunksjonen du skal konfigurere.</span><span class="sxs-lookup"><span data-stu-id="7cc89-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="7cc89-118">Importere funksjonen for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="7cc89-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="7cc89-119">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7cc89-120">I **Globaliseringsfunksjoner**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="7cc89-121">På siden for **e-faktureringsfunksjoner** velger du **Importer** for å importere e-faktureringsfunksjonen fra det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="7cc89-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cc89-122">Hvis du ikke ser listen over tilgjengelige funksjoner, velger du **Synkroniser**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="7cc89-123">Velg funksjonen for **e-fakturaeksport (IT)**, og velg deretter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Importere funksjonen for e-fakturaeksport (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="7cc89-125">Når du importerer funksjonen for **e-fakturaeksport (IT)** fra det globale lageret, blir alle innstillingene som er beskrevet i de neste delene, også importert.</span><span class="sxs-lookup"><span data-stu-id="7cc89-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="7cc89-126">Opprette en ny versjon av funksjonen for e-fakturaeksport</span><span class="sxs-lookup"><span data-stu-id="7cc89-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="7cc89-127">På siden for **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Legge til en ny versjon av e-fakturafunksjonen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="7cc89-129">Deretter konfigurerer du formatene for Elektronisk rapportering (ER) som er knyttet til e-fakturafunksjonen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="7cc89-130">I kategorien **Konfigurasjoner** velger du **Legg til** for å administrere konfigurasjonsversjonene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Behandle konfigurasjonsversjonene av e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="7cc89-132">På dette trinnet skal du legge til og konfigurere ER-formater av forskjellige filer som brukes til å eksportere italienske e-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="7cc89-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="7cc89-133">For italienske FatturaPA-e-fakturaer bruker du enten følgende standardkonfigurasjoner eller de faktiske egendefinerte konfigurasjonene du bruker for e-fakturering:</span><span class="sxs-lookup"><span data-stu-id="7cc89-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="7cc89-134">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="7cc89-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="7cc89-135">Prosjektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="7cc89-135">Project invoice (IT)</span></span>

    <span data-ttu-id="7cc89-136">Når du oppretter en e-faktureringsfunksjon som er avledet fra en annen e-faktureringsfunksjon, arves alle ER-formatene fra den opprinnelige funksjonen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="7cc89-137">Velg en bestemt ER-formatfilkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="7cc89-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="7cc89-138">Velg **Rediger** eller **Vis** for å åpne **Formatutforming**-siden.</span><span class="sxs-lookup"><span data-stu-id="7cc89-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Åpne Formatutforming-siden](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="7cc89-140">Bruk siden **Formatutforming** til å redigere og vise ER-formatfilkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="7cc89-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Formatutformingsside](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="7cc89-142">Administrere oppsett for e-faktureringsfunksjonen</span><span class="sxs-lookup"><span data-stu-id="7cc89-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="7cc89-143">På siden for **E-postfunksjoner**, i kategorien **Oppsett**, velger du **Legg til**, **Slett** eller **Rediger** for å behandle e-faktureringsoppsettene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Administrere oppsett for e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="7cc89-145">I dette trinnet konfigurerer du hendelsene som gjelder elektroniske fakturaer, inkludert generering av XML-utdatafilene i **FatturaPA**-format og digital signering (om nødvendig).</span><span class="sxs-lookup"><span data-stu-id="7cc89-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="7cc89-146">Konfigurere oppsettet av salgsfakturafunksjonen</span><span class="sxs-lookup"><span data-stu-id="7cc89-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="7cc89-147">På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="7cc89-148">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-148">Select **Edit**.</span></span>
3. <span data-ttu-id="7cc89-149">På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger.</span><span class="sxs-lookup"><span data-stu-id="7cc89-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="7cc89-150">Handlinger definerer en liste over operasjoner som må kjøres i sekvensiell rekkefølge for å oppnå full utførelse av hendelsen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Kategorien Handlinger](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="7cc89-152">Handlings-ID</span><span class="sxs-lookup"><span data-stu-id="7cc89-152">Action ID</span></span> | <span data-ttu-id="7cc89-153">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="7cc89-153">Action name</span></span>        | <span data-ttu-id="7cc89-154">Handlingsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="7cc89-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="7cc89-155">1</span><span class="sxs-lookup"><span data-stu-id="7cc89-155">1</span></span>         | <span data-ttu-id="7cc89-156">Transformere dokument</span><span class="sxs-lookup"><span data-stu-id="7cc89-156">Transform document</span></span> | <span data-ttu-id="7cc89-157">Opprett XML-filen for e-faktura i **FatturaPA**-format.</span><span class="sxs-lookup"><span data-stu-id="7cc89-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="7cc89-158">2</span><span class="sxs-lookup"><span data-stu-id="7cc89-158">2</span></span>         | <span data-ttu-id="7cc89-159">Signer dokument</span><span class="sxs-lookup"><span data-stu-id="7cc89-159">Sign document</span></span>      | <span data-ttu-id="7cc89-160">Bruk en digital signatur på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="7cc89-161">Velg **Relevansregler**-kategorien for å vise og vedlikeholde de gjeldende reglene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="7cc89-162">Relevansregler definerer konteksten der handlingen skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="7cc89-162">Applicability rules define the context where the action will be run.</span></span>

    ![Kategorien Relevansregler](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="7cc89-164">Velg kategorien **Variabler** for å vise og vedlikeholde variablene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Kategorien Variabler](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="7cc89-166">Definer de offentlige variablene som kreves for å kjøre handlingene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="7cc89-167">Konfigurere oppsettet av prosjektfakturafunksjonen</span><span class="sxs-lookup"><span data-stu-id="7cc89-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="7cc89-168">Trinnene og innstillingene som kreves for å konfigurere oppsettet av funksjonen **Prosjektfaktura**, er svært like fremgangsmåten og innstillingene for oppsett av funksjonen **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="7cc89-169">Når du arbeider med prosjektfakturaer, kan du se fremgangsmåtene for salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="7cc89-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="7cc89-170">Tilordne e-postfakturafunksjonen til-miljøet</span><span class="sxs-lookup"><span data-stu-id="7cc89-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="7cc89-171">På siden for **E-faktureringsfunksjoner**, i kategorien **Miljøer**, velger du **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="7cc89-172">I feltet **Miljø** velger du miljøet.</span><span class="sxs-lookup"><span data-stu-id="7cc89-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="7cc89-173">I **Gyldig fra**-feltet angir du datoen for når miljøet skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="7cc89-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="7cc89-174">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-174">Select **Enable**.</span></span> 

![Aktivere e-faktureringsmiljøet](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="7cc89-176">Publisere funksjonen for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="7cc89-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="7cc89-177">Du kan publisere funksjonen for e-fakturering ved å endre versjonsstatusen til **Fullført** eller **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="7cc89-178">Endre versjonsstatusen til Fullført</span><span class="sxs-lookup"><span data-stu-id="7cc89-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="7cc89-179">På siden for **e-fakturafunksjoner** i kategorien **Versjoner** velger du versjonen av e-fakturafunksjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="7cc89-180">Velg **Endre status \> Fullført**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="7cc89-181">Endre versjonsstatusen til Publisert</span><span class="sxs-lookup"><span data-stu-id="7cc89-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="7cc89-182">På siden for **e-fakturafunksjoner**, i kategorien **Versjoner**, velger du versjonen av e-fakturafunksjonen med statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="7cc89-183">Velg **Endre status \> Publiser**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-183">Select **Change status \> Publish**.</span></span>

![Endre statusen for e-fakturafunksjonen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="7cc89-185">Konfigurere integrasjon av tillegget Elektronisk fakturering i Finance</span><span class="sxs-lookup"><span data-stu-id="7cc89-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="7cc89-186">Under Finance-oppsettet vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="7cc89-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="7cc89-187">Importer ER-datamodellen, ER-datamodelltilordningen og kontekstkonfigurasjonene for FatturaPA-e-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="7cc89-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="7cc89-188">Konfigurer sertifikatet som kreves for å signere italienske e-fakturaer digitalt.</span><span class="sxs-lookup"><span data-stu-id="7cc89-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="7cc89-189">Importere datamodellen, datamodelltilordningen og formatene for ER</span><span class="sxs-lookup"><span data-stu-id="7cc89-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="7cc89-190">I arbeidsområdet for **Elektronisk rapportering** kontrollerer du at konfigurasjonsleverandøren for **forretningsdokumenttjenesten** er satt til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="7cc89-191">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="7cc89-192">Velg **Global ressurs \> Åpne**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="7cc89-193">Importer **Fakturamodell**, **Fakturamodelltilordning** og **kontekstmodell for kundefaktura**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="7cc89-194">Slå på funksjonen for eksport av elektroniske fakturaer for kunder for Italia</span><span class="sxs-lookup"><span data-stu-id="7cc89-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="7cc89-195">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="7cc89-196">I kategorien **Funksjoner** merker du av for **Aktivert** i raden for funksjonsreferanse **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Slå på FatturaPA-funksjonen](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="7cc89-198">Konfigurere elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="7cc89-198">Configure electronic documents</span></span>

1. <span data-ttu-id="7cc89-199">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="7cc89-200">I kategorien **Elektronisk dokument** velger du **Legg til** og angir tabellene som kreves for å generere italienske e-fakturaer:</span><span class="sxs-lookup"><span data-stu-id="7cc89-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="7cc89-201">**Tabellnavn:** Kundefakturajournal</span><span class="sxs-lookup"><span data-stu-id="7cc89-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="7cc89-202">**Tabellnavn:** Prosjektfaktura</span><span class="sxs-lookup"><span data-stu-id="7cc89-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="7cc89-203">For hver tabell definerer du en relatert dokumentkontekst:</span><span class="sxs-lookup"><span data-stu-id="7cc89-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="7cc89-204">For **Kundefakturajournal** velger du **Kundefakturakontekst**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="7cc89-205">I **Prosjektfaktura** velger du **Prosjektfakturakontekst**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Konfigurere svartyper](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="7cc89-207">Behandle elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="7cc89-207">Electronic invoice processing</span></span>

<span data-ttu-id="7cc89-208">Under behandlingen i Finance vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="7cc89-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="7cc89-209">Generere italienske e-fakturaer ved hjelp av tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7cc89-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="7cc89-210">Vise utførelsesloggene og se gjennom resultatene av behandlingen</span><span class="sxs-lookup"><span data-stu-id="7cc89-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="7cc89-211">Generere elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="7cc89-211">Generate electronic invoices</span></span>

<span data-ttu-id="7cc89-212">Når du har aktivert funksjonen for **konfigurerbar integrasjon av tillegget Elektronisk fakturering** og aktivert **IT00036**-funksjonen, kan ikke den gamle Finance-prosessen for generering av italienske e-fakturaer lenger brukes.</span><span class="sxs-lookup"><span data-stu-id="7cc89-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="7cc89-213">Den erstattes av en ny prosess som kalles **Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="7cc89-214">Du kan sende dokumentene manuelt, basert på etterspørselen etter e-fakturadokumenter.</span><span class="sxs-lookup"><span data-stu-id="7cc89-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="7cc89-215">Før du fortsetter må du kontrollere at oppsettet som kreves for italienske e-fakturaer, ble fullført.</span><span class="sxs-lookup"><span data-stu-id="7cc89-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="7cc89-216">Hvis du vil ha mer informasjon, kan du se [Elektroniske fakturaer for kunde](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="7cc89-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="7cc89-217">Vær oppmerksom på at noen av oppsettrinnene som beskrives i dette emnet, kanskje ikke er tilgjengelige på grunn av aktivering av tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="7cc89-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="7cc89-218">Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="7cc89-219">For første innsending av et dokument må du sette alternativet **Send dokumenter på nytt** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="7cc89-220">Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="7cc89-221">I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.</span><span class="sxs-lookup"><span data-stu-id="7cc89-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Dialogboksen Send elektroniske dokumenter](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="7cc89-223">Filterspørring</span><span class="sxs-lookup"><span data-stu-id="7cc89-223">Filter query</span></span>

1. <span data-ttu-id="7cc89-224">I dialogboksen **Forespørsel** konfigurerer du filtreringsbetingelser for både salgsfakturaer og prosjektfakturaer, eller lar betingelsene stå tomme for å inkludere alle fakturaer som ikke er sendt.</span><span class="sxs-lookup"><span data-stu-id="7cc89-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Definere filterkriterier for sending](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="7cc89-226">Velg **OK** for å lukke dialogboksen **Forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="7cc89-227">Velg **OK** for å sende de valgte dokumentene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="7cc89-228">![Merk] Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="7cc89-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="7cc89-229">Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="7cc89-230">Vise sendelogger</span><span class="sxs-lookup"><span data-stu-id="7cc89-230">View submission logs</span></span>

<span data-ttu-id="7cc89-231">Du kan vise sendelogger for alle sendte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="7cc89-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="7cc89-232">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="7cc89-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="7cc89-233">I feltet **Dokumenttype** velger du **Kundefakturajournal** eller **Prosjektfaktura** for å filtrere etter de påkrevde elektroniske dokumentene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Velge en dokumenttype for å vise sendelogger](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="7cc89-235">Verdien som vises i kolonnen **Status for sending**, representerer statusen for innsendingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="7cc89-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="7cc89-236">Den viser om prosessen kjørte som konfigurert, og om det kreves tilleggshandling.</span><span class="sxs-lookup"><span data-stu-id="7cc89-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="7cc89-237">I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Vise detaljene for innsendingsloggen](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="7cc89-239">I hurtigfanen **Behandlingshandlinger** kan du vise utførelsesloggen for handlingene som er konfigurert i funksjonsversjonen som er definert i RCS.</span><span class="sxs-lookup"><span data-stu-id="7cc89-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="7cc89-240">**Status**-kolonnen viser om handlingen ble kjørt uten feil.</span><span class="sxs-lookup"><span data-stu-id="7cc89-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="7cc89-241">I hurtigfanen **Handlingsfiler** kan du vise de mellomliggende filene som ble generert under utføring av handlingene.</span><span class="sxs-lookup"><span data-stu-id="7cc89-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="7cc89-242">Du kan velge **Vis** for å laste ned XML-filen for utdata i **FatturaPA**-format og vise innholdet i den.</span><span class="sxs-lookup"><span data-stu-id="7cc89-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cc89-243">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="7cc89-243">Related topics</span></span>

- [<span data-ttu-id="7cc89-244">Oversikt over tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7cc89-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="7cc89-245">Komme i gang med tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7cc89-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="7cc89-246">Konfigurere tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7cc89-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
