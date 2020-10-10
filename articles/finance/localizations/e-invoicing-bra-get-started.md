---
title: Komme i gang med tillegget Elektronisk fakturering for Brasil
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Brasil i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2020
ms.locfileid: "3836013"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="bcde1-103">Komme i gang med tillegget Elektronisk fakturering for Brasil</span><span class="sxs-lookup"><span data-stu-id="bcde1-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="bcde1-104">Tillegget Elektronisk fakturering for Brasil støtter ikke alle funksjonene som er tilgjengelige i regnskapsdokumentet som er innebygd i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bcde1-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="bcde1-105">Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med tillegget Elektronisk fakturering for Brasil.</span><span class="sxs-lookup"><span data-stu-id="bcde1-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="bcde1-106">Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Services (RCS) og i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bcde1-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="bcde1-107">Det leder deg også gjennom prosessen med å sende et NF-e-regnskapsdokument (elektronisk regnskapsdokumentmodell 55) gjennom tjenesten, og det forklarer hvordan du gjennomgår behandlingsresultatene og statusen til regnskapsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="bcde1-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bcde1-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="bcde1-108">Prerequisites</span></span>

<span data-ttu-id="bcde1-109">Før du fullfører trinnene i dette emnet må du fullføre trinnene i [Komme i gang med tillegget Elektronisk fakturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="bcde1-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="bcde1-110">RCS-oppsett</span><span class="sxs-lookup"><span data-stu-id="bcde1-110">RCS setup</span></span>

<span data-ttu-id="bcde1-111">Under RCS-oppsettet vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="bcde1-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="bcde1-112">Importer funksjonen for e-fakturering for NF-e-regnskapsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcde1-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="bcde1-113">Gå gjennom filformatene som kreves for å sende NF-e-regnskapsdokumenter for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="bcde1-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="bcde1-114">Se gjennom filformatene som kreves for å be om annullering av en godkjent NF-e.</span><span class="sxs-lookup"><span data-stu-id="bcde1-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="bcde1-115">Konfigurer hendelse som kreves for å sende NF-e-regnskapsdokumenter for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="bcde1-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="bcde1-116">Konfigurer hendelse som kreves for å be om annullering av en godkjent NF-e.</span><span class="sxs-lookup"><span data-stu-id="bcde1-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="bcde1-117">Tilordne funksjonen for e-fakturering til et miljø for tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="bcde1-118">Publiser funksjonen for e-fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="bcde1-119">"E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="bcde1-120">Oppsettet av funksjonen for E-fakturering kombinerer, blant annet, bruken av konfigurasjonsformater for Elektronisk rapportering (ER) for å opprette konfigurerbare eksport- og importfiler, og bruken av handlinger og handlingsflyter for å gjøre det mulig å opprette konfigurerbare regler for å sende forespørsler, importere svar og analysere svarinnholdet.</span><span class="sxs-lookup"><span data-stu-id="bcde1-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="bcde1-121">Importere funksjonen for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="bcde1-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="bcde1-122">Logge på RCS-kontoen</span><span class="sxs-lookup"><span data-stu-id="bcde1-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="bcde1-123">I **Globaliseringsfunksjoner**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="bcde1-124">På siden for **e-faktureringsfunksjoner** velger du **Importer** for å importere en e-faktureringsfunksjon for et NF-e-regnskapsdokument fra det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="bcde1-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![Importer-knappen](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="bcde1-126">Velg funksjonen for NF-e-regnskapsdokument, og velg deretter **Importer**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![Importere NF-e-funksjonen](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="bcde1-128">Opprette en ny versjon av funksjonen for NF-e-regnskapsdokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="bcde1-129">På siden for **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Legge til en ny versjon av e-fakturafunksjonen](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="bcde1-131">Oppdatere konfigurasjonsversjonen</span><span class="sxs-lookup"><span data-stu-id="bcde1-131">Update the configuration version</span></span>

1. <span data-ttu-id="bcde1-132">På siden **E-faktureringsfunksjoner**, i kategorien **Konfigurasjoner**, velger du **Legg til** eller **Slett** for å behandle konfigurasjonsversjonene (ER-filformatkonfigurasjoner).</span><span class="sxs-lookup"><span data-stu-id="bcde1-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Behandle konfigurasjoner for e-faktureringsfunksjon](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="bcde1-134">Når du oppretter en ny versjon av funksjonen for NF-e-regnskapsdokument, arves alle konfigurasjonsversjoner (ER-filformater) fra den nyeste versjonen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="bcde1-135">Hvis du vil sende NF-e-regnskapsdokumentet for godkjenning, kreves følgende konfigurasjonsversjoner:</span><span class="sxs-lookup"><span data-stu-id="bcde1-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="bcde1-136">Eksportformat for NFe-innsending</span><span class="sxs-lookup"><span data-stu-id="bcde1-136">NFe submit export format</span></span>
        - <span data-ttu-id="bcde1-137">Import av NFe-svarmelding</span><span class="sxs-lookup"><span data-stu-id="bcde1-137">NFe response message import</span></span>
        - <span data-ttu-id="bcde1-138">Import av NFe-feillogg</span><span class="sxs-lookup"><span data-stu-id="bcde1-138">NFe error log import</span></span>

    - <span data-ttu-id="bcde1-139">Hvis du vil sende NF-e-avbrytelsen, kreves følgende konfigurasjonsversjon:</span><span class="sxs-lookup"><span data-stu-id="bcde1-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="bcde1-140">Eksportformat for NFe-annullering</span><span class="sxs-lookup"><span data-stu-id="bcde1-140">NFe cancel export format</span></span>

2. <span data-ttu-id="bcde1-141">Velg en konfigurasjonsversjon fra listen, og velg deretter **Rediger** eller **Vis** for å åpne siden **Formatutforming**, der du kan redigere eller vise konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Åpne Formatutforming-siden](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="bcde1-143">Bruk siden **Formatutforming** til å redigere eller vise ER-formatfilkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="bcde1-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="bcde1-144">Hvis du vil ha mer informasjon, kan du se [Opprette konfigurasjoner for elektronisk dokument](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span><span class="sxs-lookup"><span data-stu-id="bcde1-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![Formatutformingsside](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="bcde1-146">Administrere oppsett for e-faktureringsfunksjonen</span><span class="sxs-lookup"><span data-stu-id="bcde1-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="bcde1-147">På siden for **E-postfunksjoner**, i kategorien **Oppsett**, velger du **Legg til** eller **Slett** for å behandle e-faktureringsoppsettene (dvs. NF-e-hendelsene).</span><span class="sxs-lookup"><span data-stu-id="bcde1-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![Administrere oppsett for e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="bcde1-149">Når du oppretter en ny versjon av NF-e-regnskapsdokumentfunksjonen som er avledet fra en annen e-faktureringsfunksjon, arves alle funksjonsoppsett (NF-e-hendelser) fra den nyeste versjonen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="bcde1-150">Funksjonen **Send** kreves for å sende NF-e-regnskapsdokumenter for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="bcde1-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="bcde1-151">Hvis du skal sende NF-e-annullering, kreves oppsett av funksjonen for **Annullering**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="bcde1-152">Konfigurere oppsett av Send-funksjonen</span><span class="sxs-lookup"><span data-stu-id="bcde1-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="bcde1-153">På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Send**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="bcde1-154">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-154">Select **Edit**.</span></span>

    ![Redigere oppsett for e-faktureringsfunksjon](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="bcde1-156">På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger.</span><span class="sxs-lookup"><span data-stu-id="bcde1-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![Kategorien Handlinger](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="bcde1-158">Gå gjennom handlingene som kreves for å sende en NF-e for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="bcde1-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="bcde1-159">Handlings-ID</span><span class="sxs-lookup"><span data-stu-id="bcde1-159">Action ID</span></span> | <span data-ttu-id="bcde1-160">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="bcde1-160">Action name</span></span>                  | <span data-ttu-id="bcde1-161">Handlingsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcde1-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="bcde1-162">1</span><span class="sxs-lookup"><span data-stu-id="bcde1-162">1</span></span>         | <span data-ttu-id="bcde1-163">Transformere dokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-163">Transform document</span></span>           | <span data-ttu-id="bcde1-164">Opprett NF-e-XML-filen for sending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="bcde1-165">2</span><span class="sxs-lookup"><span data-stu-id="bcde1-165">2</span></span>         | <span data-ttu-id="bcde1-166">Signer dokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-166">Sign document</span></span>                | <span data-ttu-id="bcde1-167">Bruk den digitale signaturen på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="bcde1-168">3</span><span class="sxs-lookup"><span data-stu-id="bcde1-168">3</span></span>         | <span data-ttu-id="bcde1-169">Kalle opp brasiliansk SEFAZ-tjeneste</span><span class="sxs-lookup"><span data-stu-id="bcde1-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="bcde1-170">Send den signerte XML-filen til webtjenestene for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="bcde1-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="bcde1-171">4</span><span class="sxs-lookup"><span data-stu-id="bcde1-171">4</span></span>         | <span data-ttu-id="bcde1-172">Behandle svar</span><span class="sxs-lookup"><span data-stu-id="bcde1-172">Process response</span></span>             | <span data-ttu-id="bcde1-173">Hent webtjenestesvaret.</span><span class="sxs-lookup"><span data-stu-id="bcde1-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="bcde1-174">5</span><span class="sxs-lookup"><span data-stu-id="bcde1-174">5</span></span>         | <span data-ttu-id="bcde1-175">Transformere dokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-175">Transform document</span></span>           | <span data-ttu-id="bcde1-176">Analyser innholdet i filen som er mottatt som et svar.</span><span class="sxs-lookup"><span data-stu-id="bcde1-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="bcde1-177">6</span><span class="sxs-lookup"><span data-stu-id="bcde1-177">6</span></span>         | <span data-ttu-id="bcde1-178">Transformere dokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-178">Transform document</span></span>           | <span data-ttu-id="bcde1-179">Opprett XML-filen for å spørre om statusen for sendingen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="bcde1-180">7</span><span class="sxs-lookup"><span data-stu-id="bcde1-180">7</span></span>         | <span data-ttu-id="bcde1-181">Kalle opp brasiliansk SEFAZ-tjeneste</span><span class="sxs-lookup"><span data-stu-id="bcde1-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="bcde1-182">Send XML-filen som ber om sendestatusen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="bcde1-183">8</span><span class="sxs-lookup"><span data-stu-id="bcde1-183">8</span></span>         | <span data-ttu-id="bcde1-184">Behandle svar</span><span class="sxs-lookup"><span data-stu-id="bcde1-184">Process response</span></span>             | <span data-ttu-id="bcde1-185">Hent webtjenestesvaret.</span><span class="sxs-lookup"><span data-stu-id="bcde1-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="bcde1-186">Konfigurere URL-adressen for SEFAZ-webtjenester</span><span class="sxs-lookup"><span data-stu-id="bcde1-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="bcde1-187">På siden for **funksjonsversjonsoppsett**, i kategorien **Handlinger** i hurtigkategorien **Handlinger**, velger du å **Kalle opp meksikansk PAC-tjeneste** (handlings-ID **3**).</span><span class="sxs-lookup"><span data-stu-id="bcde1-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="bcde1-188">I hurtigkategorien **Parametere** i feltet for **URL-adresseparameter**, angir du URL-adressen til webtjenesten for SEFAZ for NF-e-sending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="bcde1-189">I hurtigfanen **Handlinger** velger du å **Kalle opp brasiliansk SEFAZ-tjeneste** (handlings-ID **7**).</span><span class="sxs-lookup"><span data-stu-id="bcde1-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="bcde1-190">I hurtigkategorien **Parametere** i feltet for **URL-adresseparameter**, angir du URL-adressen til webtjenesten for SEFAZ for NF-e-sending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="bcde1-191">Konfigurere oppsett av kaselleringsfunksjonen</span><span class="sxs-lookup"><span data-stu-id="bcde1-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="bcde1-192">På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Annullering**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="bcde1-193">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-193">Select **Edit**.</span></span>
3. <span data-ttu-id="bcde1-194">På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger.</span><span class="sxs-lookup"><span data-stu-id="bcde1-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="bcde1-195">Se gjennom handlingene som kreves for å be om anullering av en godkjent NF-e.</span><span class="sxs-lookup"><span data-stu-id="bcde1-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="bcde1-196">Handlings-ID</span><span class="sxs-lookup"><span data-stu-id="bcde1-196">Action ID</span></span> | <span data-ttu-id="bcde1-197">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="bcde1-197">Action name</span></span>                  | <span data-ttu-id="bcde1-198">Handlingsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcde1-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="bcde1-199">1</span><span class="sxs-lookup"><span data-stu-id="bcde1-199">1</span></span>         | <span data-ttu-id="bcde1-200">Transformere dokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-200">Transform document</span></span>           | <span data-ttu-id="bcde1-201">Opprett XML-filen for NF-e-annullering for innsending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="bcde1-202">2</span><span class="sxs-lookup"><span data-stu-id="bcde1-202">2</span></span>         | <span data-ttu-id="bcde1-203">Signer dokument</span><span class="sxs-lookup"><span data-stu-id="bcde1-203">Sign document</span></span>                | <span data-ttu-id="bcde1-204">Bruk den digitale signaturen på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="bcde1-205">3</span><span class="sxs-lookup"><span data-stu-id="bcde1-205">3</span></span>         | <span data-ttu-id="bcde1-206">Kalle opp brasiliansk SEFAZ-tjeneste</span><span class="sxs-lookup"><span data-stu-id="bcde1-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="bcde1-207">Send den signerte XML-filen til webtjenestene for annullering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="bcde1-208">4</span><span class="sxs-lookup"><span data-stu-id="bcde1-208">4</span></span>         | <span data-ttu-id="bcde1-209">Behandle svar</span><span class="sxs-lookup"><span data-stu-id="bcde1-209">Process response</span></span>             | <span data-ttu-id="bcde1-210">Hent webtjenestesvaret.</span><span class="sxs-lookup"><span data-stu-id="bcde1-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="bcde1-211">Konfigurere URL-adressen for SEFAZ-webtjenester</span><span class="sxs-lookup"><span data-stu-id="bcde1-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="bcde1-212">På siden for **funksjonsversjonsoppsett**, i kategorien **Handlinger** i hurtigkategorien **Handlinger**, velger du å **Kalle opp meksikansk PAC-tjeneste** (handlings-ID **3**).</span><span class="sxs-lookup"><span data-stu-id="bcde1-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="bcde1-213">I hurtigkategorien **Parametere** i feltet for **URL-adresseparameter** angir du URL-adressen til webtjenesten for SEFAZ for annullering av en godkjent NF-e.</span><span class="sxs-lookup"><span data-stu-id="bcde1-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="bcde1-214">Gjøre et e-faktureringsmiljø tilgjengelig og tilordne en kladdeversjon</span><span class="sxs-lookup"><span data-stu-id="bcde1-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="bcde1-215">På siden for **E-faktureringsfunksjoner**, i kategorien **Miljøer**, velger du **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="bcde1-216">I feltet **Miljø** velger du miljøet.</span><span class="sxs-lookup"><span data-stu-id="bcde1-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="bcde1-217">I **Gyldig fra**-feltet angir du datoen for når miljøet skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="bcde1-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="bcde1-218">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-218">Select **Enable**.</span></span>

![Aktivere et e-faktureringsmiljø](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="bcde1-220">Endre statusen til Fullført</span><span class="sxs-lookup"><span data-stu-id="bcde1-220">Change the status to Completed</span></span>

1. <span data-ttu-id="bcde1-221">På siden for **e-fakturafunksjoner** i kategorien **Versjoner** velger du versjonen av e-fakturafunksjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="bcde1-222">Velg **Endre status \> Fullført**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="bcde1-223">Endre statusen til Publiser</span><span class="sxs-lookup"><span data-stu-id="bcde1-223">Change the status to Publish</span></span>

1. <span data-ttu-id="bcde1-224">På siden for **e-fakturafunksjoner**, i kategorien **Versjoner**, velger du versjonen av e-fakturafunksjonen med statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="bcde1-225">Velg **Endre status \> Publiser**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-225">Select **Change status \> Publish**.</span></span>

![Publisere funksjonen for e-fakturering](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="bcde1-227">Konfigurere integrasjon av tillegget Elektronisk fakturering i Finance eller Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="bcde1-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="bcde1-228">Under oppsettet vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="bcde1-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="bcde1-229">Slå på funksjonen for føderal NF-e for Brasil.</span><span class="sxs-lookup"><span data-stu-id="bcde1-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="bcde1-230">Importer den spesifikke ER-datamodellen, datamodelltilordningen og formatene som kreves for NF-e-regnskapsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcde1-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="bcde1-231">Importer ER-konfigurasjonen og konfigurer svartypene som kreves for å oppdatere statusen til regnskapsdokumentet etter sendingsprosessen er returnert.</span><span class="sxs-lookup"><span data-stu-id="bcde1-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="bcde1-232">Slå på funksjonen for føderal NF-e for Brasil</span><span class="sxs-lookup"><span data-stu-id="bcde1-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="bcde1-233">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="bcde1-234">I kategorien **Funksjoner** merker du av for **Aktiver** i raden for funksjonsreferanse **BR00053**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="bcde1-235">Importere ER-datamodelltilordningen som er nødvendig for NF-e-regnskapsdokumenter</span><span class="sxs-lookup"><span data-stu-id="bcde1-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="bcde1-236">Logg på Finance.</span><span class="sxs-lookup"><span data-stu-id="bcde1-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="bcde1-237">I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="bcde1-238">Kontroller at konfigurasjonsleverandøren er satt til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="bcde1-239">Hvis du ha mer informasjon om hvordan du setter en leverandør til **Aktiv**, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="bcde1-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="bcde1-240">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="bcde1-241">Velg **Global ressurs \> Åpne**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="bcde1-242">Importer konfigurasjoner for **regnskapsdokumenttilordning**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="bcde1-243">Importere ER-konfigurasjoner og konfigurere svartypene for regnskapsdokumenter</span><span class="sxs-lookup"><span data-stu-id="bcde1-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="bcde1-244">I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du flisen **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="bcde1-245">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="bcde1-246">Velg **Global ressurs \> Åpne**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="bcde1-247">Importer **Import av NF-e-feillogg (BR)**, **Format for dataimport av NF-e-svar (BR)** og **Import av NF-e-svarmelding (BR)**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="bcde1-248">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="bcde1-249">I kategorien **Elektronisk dokument** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="bcde1-250">I feltet **Tabellnavn** angir du **regnskapsdokumenthode**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="bcde1-251">I feltet **Dokumentkontekst** velger du **kontekstmodell for kundefaktura – regnskapsdokumentkontekst**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="bcde1-252">Velg **Svartyper**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-252">Select **Response types**.</span></span>
9. <span data-ttu-id="bcde1-253">Velg **Ny**, og deretter, i **Svartype**-feltet, velg **Svar**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="bcde1-254">I feltet for **innsendingsstatus** velger du **Venter**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="bcde1-255">I feltet **Modelltilordning** velg **svarmeldingsimportformat – modelltilordning fra svarmelding**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="bcde1-256">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-256">Select **Save**.</span></span>
13. <span data-ttu-id="bcde1-257">Velg **Ny** og deretter, i **Svartype**-feltet, angir du **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="bcde1-258">I feltet for **innsendingsstatus** velger du **Venter**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="bcde1-259">I **Modelltilordning**-feltet velger du **Format for dataimport av NFe-svar – dataimport av svar**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="bcde1-260">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="bcde1-261">Behandle elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="bcde1-261">Electronic invoice processing</span></span>

<span data-ttu-id="bcde1-262">Under behandlingen i Finance vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="bcde1-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="bcde1-263">Send et regnskapsdokument via tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="bcde1-264">Vise utførelsesloggene for sending og se gjennom resultatene av behandlingen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="bcde1-265">Send annulleringen for et regnskapsdokument via tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="bcde1-266">Sende NF-e-regnskapsdokumenter for SEFAZ-autorisasjon</span><span class="sxs-lookup"><span data-stu-id="bcde1-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="bcde1-267">Når du har aktivert funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**, kan ikke den gamle prosessen for sending av NF-e-regnskapsdokumenter for godkjenning (**Eksport/import av NF-e-prosess**) brukes lenger.</span><span class="sxs-lookup"><span data-stu-id="bcde1-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="bcde1-268">Den erstattes av en ny prosess som kalles **Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="bcde1-269">Før du fortsetter må du kontrollere at du har én eller flere kunderegnskapsdokumenter modell 55 som ble utstedt av kundens regnskapsfirma.</span><span class="sxs-lookup"><span data-stu-id="bcde1-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="bcde1-270">Retningen for disse regnskapsdokumentene må settes til **Utgående**, og statusen må være **Opprettet**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="bcde1-271">Hvis du vil ha mer informasjon, kan du se [Utstede regnskapsdokumenter for kunde (Brasil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="bcde1-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="bcde1-272">Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="bcde1-273">For første innsending av et dokument må du alltid sette alternativet **Send dokumenter på nytt** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="bcde1-274">Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="bcde1-275">I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="bcde1-276">Velg **Legg til** i kategorien **Område**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="bcde1-277">I feltet **Tabellnavn** velger du **regnskapsdokumenthode**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="bcde1-278">I feltet **Avledet tabell** velger du **regnskapsdokumenthode**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="bcde1-279">Velg **Nummer** i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="bcde1-280">I **Vilkår**-feltet angir du nummeret på regnskapsdokumentet som skal sendes.</span><span class="sxs-lookup"><span data-stu-id="bcde1-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="bcde1-281">Velg **OK** for å lukke dialogboksen **Forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="bcde1-282">Velg **OK** for å sende de valgte dokumentene.</span><span class="sxs-lookup"><span data-stu-id="bcde1-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="bcde1-283">Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="bcde1-284">Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="bcde1-285">Vise alle sendelogger</span><span class="sxs-lookup"><span data-stu-id="bcde1-285">View all submission logs</span></span>

<span data-ttu-id="bcde1-286">Når du har aktivert funksjonen **Konfigurerbar integrasjon av tillegget Elektronisk fakturering**, er en ny side tilgjengelig der du kan følge opp dokumentsendingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="bcde1-287">Du kan bruke denne siden til å vise sendelogger for alle sendte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcde1-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="bcde1-288">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="bcde1-289">I **Dokumenttype**-feltet velger **regnskapsdokumenthode** for å filtrere bare etter regnskapsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcde1-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="bcde1-290">I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.</span><span class="sxs-lookup"><span data-stu-id="bcde1-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![Vise detaljene for innsendingsloggen](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="bcde1-292">For NF-e-regnskapsdokumenter er viser kolonnen **Feilkode** returkoden som ble returnert av webtjenesten SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="bcde1-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="bcde1-293">Vise sendelogger via regnskapsdokumentsiden</span><span class="sxs-lookup"><span data-stu-id="bcde1-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="bcde1-294">Når du har aktivert funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**, kan du også vise sendeloggene fra regnskapsdokumentsiden.</span><span class="sxs-lookup"><span data-stu-id="bcde1-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="bcde1-295">Gå til **Økonomimodul \> Forespørsler og rapporter \> Regnskapsdokumenter \> Alle regnskapsdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="bcde1-296">Velg et regnskapsdokument som tidligere ble sendt via tillegget Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="bcde1-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="bcde1-297">Velg **logg for elektronisk dokument** i kategorien for **føderal NF-e** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bcde1-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![Vise sendelogger fra regnskapsdokumentsiden](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="bcde1-299">Sende godkjente NF-e-regnskapsdokumenter for SEFAZ-annullering</span><span class="sxs-lookup"><span data-stu-id="bcde1-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="bcde1-300">Når du har aktivert funksjonen for **Konfigurerbar integrasjon for tillegget Elektronisk fakturering**, kan ikke lenger den gamle prosessen for annullering av føderale NF-e-dokumenter brukes.</span><span class="sxs-lookup"><span data-stu-id="bcde1-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="bcde1-301">Den erstattes av en ny avlysningsprosess som er innebygd på siden for **sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="bcde1-302">Kontroller at du har kjørt annulleringen av kunderegnskapsdokumentet for et godkjent NF-e-regnskapsdokument.</span><span class="sxs-lookup"><span data-stu-id="bcde1-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="bcde1-303">Hvis du vil ha mer informasjon, kan du se [Annullere regnskapsdokument for kunde (Brasil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="bcde1-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="bcde1-304">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="bcde1-305">Velg regnskapsdokumentet, og velg deretter **Funksjoner \> Send relaterte innsendinger**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="bcde1-306">Angi en beskrivelse for den tilknyttede sendingen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="bcde1-307">Vise sendelogger for annullering</span><span class="sxs-lookup"><span data-stu-id="bcde1-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="bcde1-308">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="bcde1-309">I **Dokumenttype**-feltet velger **regnskapsdokumenthode** for å filtrere bare etter regnskapsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcde1-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="bcde1-310">Velg regnskapsdokumentet, og velg deretter **Forespørsler \> Relatert sending** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bcde1-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="bcde1-311">Tilknyttede sendinger er sendinger som er relatert til en hovedsending som ble opprettet først.</span><span class="sxs-lookup"><span data-stu-id="bcde1-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="bcde1-312">Eksempelvis er innsendingen som autoriserer en bestemt NF-e, hovedinnsendingen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="bcde1-313">Innsendingen som ber om annullering av den samme NF-e i SEFAZ, er en relatert sending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="bcde1-314">Den finnes bare fordi den ber om å annullere jobben som ble gjort gjennom en annen innsending.</span><span class="sxs-lookup"><span data-stu-id="bcde1-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="bcde1-315">Siden **Relatert innsendinger** viser alle tilknyttede innsendinger, og sendestatusen, for et gitt regnskapsdokument.</span><span class="sxs-lookup"><span data-stu-id="bcde1-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="bcde1-316">I illustrasjonen nedenfor representerer den første linjen innsendingen som ber om godkjenning av regnskapsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="bcde1-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="bcde1-317">Den andre linjen representerer innsendingen som avbrøt regnskapsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="bcde1-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![Vise sendeloggene for annullering](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="bcde1-319">I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.</span><span class="sxs-lookup"><span data-stu-id="bcde1-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Vise detaljer for sendeloggen for annullering](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="bcde1-321">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="bcde1-321">Privacy notice</span></span>
<span data-ttu-id="bcde1-322">Aktivering av funksjonen for BR-00053 (føderal NF-e) kan kreve sending av begrensede data, som inkluderer registrerings-IDen for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="bcde1-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="bcde1-323">Dette overføres til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="bcde1-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="bcde1-324">En administrator kan aktivere og deaktivere funksjonen BR-00053 (føderal NF-e) ved å navigere til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcde1-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="bcde1-325">Velg kategorien **Funksjoner**, velg raden som inneholder BR-00053-funksjonen, og velg deretter riktig valg.</span><span class="sxs-lookup"><span data-stu-id="bcde1-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="bcde1-326">Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="bcde1-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="bcde1-327">Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.</span><span class="sxs-lookup"><span data-stu-id="bcde1-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="bcde1-328">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bcde1-328">Additional resources</span></span>

- [<span data-ttu-id="bcde1-329">Oversikt over tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="bcde1-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="bcde1-330">Komme i gang med tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="bcde1-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="bcde1-331">Konfigurere tillegget Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="bcde1-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
