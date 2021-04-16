---
title: Komme i gang med Elektronisk fakturering for Mexico
description: Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Mexico.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 2f5dd1d6bc520c9f5349c77dfcabdf2d538881ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840058"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="448ae-103">Komme i gang med Elektronisk fakturering for Mexico</span><span class="sxs-lookup"><span data-stu-id="448ae-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="448ae-104">Det kan hende at Elektronisk fakturering for Mexico ikke støtter alle funksjonene som er tilgjengelige i CFDI-dokumentet (Comprobante Fiscal Digital por Internet) og i den relaterte integrasjonen som er innebygd i Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="448ae-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="448ae-105">Dette emnet inneholder informasjon som vil hjelpe deg med å komme i gang med elektronisk fakturering for Mexico.</span><span class="sxs-lookup"><span data-stu-id="448ae-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="448ae-106">Det leder deg gjennom konfigurasjonstrinnene som er landsavhengige i Regulatory Configuration Services (RCS) og Finance.</span><span class="sxs-lookup"><span data-stu-id="448ae-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="448ae-107">Den leder deg også gjennom trinnene du må følge i Finance for å sende CFDI-fakturaer gjennom tjenesten, og forklarer hvordan du gjennomgår behandlingsresultatene og statusen for CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="448ae-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="448ae-108">Prerequisites</span></span>

<span data-ttu-id="448ae-109">Før du fullfører trinnene i dette emnet må du fullføre trinnene i [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="448ae-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="448ae-110">RCS-oppsett</span><span class="sxs-lookup"><span data-stu-id="448ae-110">RCS setup</span></span>

<span data-ttu-id="448ae-111">Under RCS-oppsettet vil du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="448ae-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="448ae-112">Importer funksjonen for e-fakturering for behandling av CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="448ae-113">Gå gjennom formatkonfigurasjonene som kreves for å generere, sende og motta svar om CFDI-fakturaer, og for å sende og motta svar om annullering.</span><span class="sxs-lookup"><span data-stu-id="448ae-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="448ae-114">Konfigurer hendelsene som støtter innsendingsscenarioene for CFDI-faktura.</span><span class="sxs-lookup"><span data-stu-id="448ae-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="448ae-115">Publiser funksjonen for e-fakturering for CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="448ae-116">"E-fakturering-funksjonen" er det generelle navnet på ressursen som er konfigurert og publisert til å bruke serveren for Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448ae-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="448ae-117">I dette tilfellet er CFDI-fakturaer (MX) e-faktureringsfunksjonen du vil definere.</span><span class="sxs-lookup"><span data-stu-id="448ae-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="448ae-118">Importere funksjonen for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="448ae-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="448ae-119">Logg på RCS-kontoen.</span><span class="sxs-lookup"><span data-stu-id="448ae-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="448ae-120">I **Globaliseringsfunksjoner**-arbeidsområder i delen **Funksjoner**, velger du flisen **E-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="448ae-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="448ae-121">På siden **E-faktureringsfunksjoner** velger du **Importer** for å importere **CFDI-fakturaer (MX)** fra det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="448ae-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="448ae-122">Hvis du ikke ser funksjonen i listen, velger du **Synkroniser**, og deretter gjentar du trinn 3.</span><span class="sxs-lookup"><span data-stu-id="448ae-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![Importere funksjonen for CFDI-fakturaer (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="448ae-124">Når du importerer funksjonen for **CFDI-fakturaer (MX)** fra det globale repositoriet, importeres alle funksjonsinnstillinger, inkludert konfigurasjoner og handlinger.</span><span class="sxs-lookup"><span data-stu-id="448ae-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="448ae-125">Opprette en ny versjon av funksjonen CFDI-fakturaer (MX)</span><span class="sxs-lookup"><span data-stu-id="448ae-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="448ae-126">Du kan opprette en ny versjon hvis for eksempel URL-adresser må oppdateres.</span><span class="sxs-lookup"><span data-stu-id="448ae-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="448ae-127">Hvis du vil ha mer informasjon, se [E-fakturering av CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="448ae-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="448ae-128">På siden for **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="448ae-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Legge til en ny versjon av e-fakturafunksjonen](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="448ae-130">Oppdatere konfigurasjonsversjonen</span><span class="sxs-lookup"><span data-stu-id="448ae-130">Update the configuration version</span></span>

1. <span data-ttu-id="448ae-131">På siden **E-faktureringsfunksjoner**, i kategorien **Konfigurasjoner**, velger du **Legg til** eller **Slett** for å behandle konfigurasjonsversjonene (ER-filformatkonfigurasjoner).</span><span class="sxs-lookup"><span data-stu-id="448ae-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Behandle konfigurasjoner for e-faktureringsfunksjon](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="448ae-133">Når du oppretter en ny versjon, arves alle konfigurasjoner fra den siste publiserte versjonen.</span><span class="sxs-lookup"><span data-stu-id="448ae-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="448ae-134">Hvis du skal behandle CFDI-fakturaer, kreves følgende konfigurasjoner:</span><span class="sxs-lookup"><span data-stu-id="448ae-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="448ae-135">CFDI-faktura (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="448ae-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="448ae-136">Import av CFDI-svarmelding</span><span class="sxs-lookup"><span data-stu-id="448ae-136">CFDI response message import</span></span>
    - <span data-ttu-id="448ae-137">Import av CFDI-feillogg</span><span class="sxs-lookup"><span data-stu-id="448ae-137">CFDI error log import</span></span>
    - <span data-ttu-id="448ae-138">CFDI-avbruddsforespørsel (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="448ae-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="448ae-139">CFDI-faktura (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="448ae-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="448ae-140">Velg en konfigurasjonsversjon fra listen, og velg deretter **Rediger** eller **Vis** for å åpne siden **Formatutforming**, der du kan redigere eller vise konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="448ae-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Åpne Formatutforming-siden](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="448ae-142">Bruk siden **Formatutforming** til å redigere og vise ER-formatfilkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="448ae-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="448ae-143">Hvis du vil ha mer informasjon, kan du se [Opprette konfigurasjoner for elektronisk dokument](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="448ae-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Formatutformingsside](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="448ae-145">Administrere oppsett for e-faktureringsfunksjonen</span><span class="sxs-lookup"><span data-stu-id="448ae-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="448ae-146">På siden for **E-postfunksjoner**, i kategorien **Oppsett**, velger du **Legg til**, **Slett** eller **Rediger** for å behandle e-faktureringsoppsettene.</span><span class="sxs-lookup"><span data-stu-id="448ae-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Administrere oppsett for e-faktureringsfunksjonen](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="448ae-148">Hvis du vil sende CFDI-fakturaer for autorisasjon (generere XML-filen, sende XML-filen og behandle svaret), kreves funksjonsoppsettet **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="448ae-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="448ae-149">Hvis du vil sende CFDI-fakturaannullering, kreves funksjonsoppsett for **Annullering** og **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="448ae-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="448ae-150">Konfigurere oppsettet av salgsfakturafunksjonen</span><span class="sxs-lookup"><span data-stu-id="448ae-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="448ae-151">På siden for **e-fakturafunksjoner**, i kategorien **Oppsett** i kolonnen **Funksjonsoppsett**, velger du **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="448ae-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="448ae-152">Velg **Rediger** for å konfigurere handlinger, relevansregler og variabler.</span><span class="sxs-lookup"><span data-stu-id="448ae-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![Redigere oppsettet for e-postfakturafunksjonen](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="448ae-154">På siden for **oppsett av funksjonsversjon** velger du kategorien **Handlinger** for å behandle listen over handlinger.</span><span class="sxs-lookup"><span data-stu-id="448ae-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="448ae-155">Handlinger definerer en liste over operasjoner som må kjøres i sekvensiell rekkefølge for å oppnå full utførelse av hendelsen.</span><span class="sxs-lookup"><span data-stu-id="448ae-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Kategorien Handlinger](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="448ae-157">Handlings-ID</span><span class="sxs-lookup"><span data-stu-id="448ae-157">Action ID</span></span> | <span data-ttu-id="448ae-158">Handling</span><span class="sxs-lookup"><span data-stu-id="448ae-158">Action</span></span>                   | <span data-ttu-id="448ae-159">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="448ae-159">Action name</span></span>                                  | <span data-ttu-id="448ae-160">Handlingsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="448ae-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="448ae-161">1</span><span class="sxs-lookup"><span data-stu-id="448ae-161">1</span></span>         | <span data-ttu-id="448ae-162">Transformere dokument</span><span class="sxs-lookup"><span data-stu-id="448ae-162">Transform document</span></span>       | <span data-ttu-id="448ae-163">Generere CFDI-e-faktura uten digital signatur</span><span class="sxs-lookup"><span data-stu-id="448ae-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="448ae-164">Generer CFDI-e-fakturaen.</span><span class="sxs-lookup"><span data-stu-id="448ae-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="448ae-165">2</span><span class="sxs-lookup"><span data-stu-id="448ae-165">2</span></span>         | <span data-ttu-id="448ae-166">Signer dokument</span><span class="sxs-lookup"><span data-stu-id="448ae-166">Sign document</span></span>            | <span data-ttu-id="448ae-167">Digital signatur</span><span class="sxs-lookup"><span data-stu-id="448ae-167">Digital sign</span></span>                                 | <span data-ttu-id="448ae-168">Signer e-fakturaen digitalt for innsending.</span><span class="sxs-lookup"><span data-stu-id="448ae-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="448ae-169">3</span><span class="sxs-lookup"><span data-stu-id="448ae-169">3</span></span>         | <span data-ttu-id="448ae-170">Kalle opp meksikansk PAC-tjeneste</span><span class="sxs-lookup"><span data-stu-id="448ae-170">Call Mexican PAC service</span></span> | <span data-ttu-id="448ae-171">Sende CFDI -e-faktura</span><span class="sxs-lookup"><span data-stu-id="448ae-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="448ae-172">Windows Communication Foundation (WCF)-klienten sender CFDI-e-faktura.</span><span class="sxs-lookup"><span data-stu-id="448ae-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="448ae-173">4</span><span class="sxs-lookup"><span data-stu-id="448ae-173">4</span></span>         | <span data-ttu-id="448ae-174">Behandle svar</span><span class="sxs-lookup"><span data-stu-id="448ae-174">Process response</span></span>         | <span data-ttu-id="448ae-175">Analysere webtjenestesvar</span><span class="sxs-lookup"><span data-stu-id="448ae-175">Analyze web service response</span></span>                 | <span data-ttu-id="448ae-176">Analyser webtjenestesvaret, og returner feilloggen.</span><span class="sxs-lookup"><span data-stu-id="448ae-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="448ae-177">Konfigurere URL-adressen for meksikanske PAC-webtjenester</span><span class="sxs-lookup"><span data-stu-id="448ae-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="448ae-178">På siden for **funksjonsversjonsoppsett**, i kategorien **Handlinger** i hurtigkategorien **Handlinger**, velger du **Kalle opp meksikansk PAC-tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="448ae-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="448ae-179">I hurtigkategorien **Parametere** i feltet **URL-adresse**, angir du URL-adressen til webtjenesten for CFDI-fakturainnsending.</span><span class="sxs-lookup"><span data-stu-id="448ae-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="448ae-180">Bruk de samme trinnene til å oppdatere URL-adressen for handlingen **Kalle opp meksikansk PAC-tjeneste** for funksjonsoppsettet for **Avbryt** og **Annulleringsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="448ae-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="448ae-181">Tilordne kladdeversjonen til et e-faktureringsmiljø</span><span class="sxs-lookup"><span data-stu-id="448ae-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="448ae-182">På siden for **E-faktureringsfunksjoner**, i kategorien **Miljøer**, velger du **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="448ae-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="448ae-183">I feltet **Miljø** velger du miljøet.</span><span class="sxs-lookup"><span data-stu-id="448ae-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="448ae-184">I **Gyldig fra**-feltet angir du datoen for når miljøet skal tre i kraft.</span><span class="sxs-lookup"><span data-stu-id="448ae-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="448ae-185">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="448ae-185">Select **Enable**.</span></span>

![Aktivere et e-faktureringsmiljø](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="448ae-187">Endre versjonsstatusen til Fullført</span><span class="sxs-lookup"><span data-stu-id="448ae-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="448ae-188">På siden for **e-fakturafunksjoner** i kategorien **Versjoner** velger du versjonen av e-fakturafunksjonen med statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="448ae-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="448ae-189">Velg **Endre status \> Fullført**.</span><span class="sxs-lookup"><span data-stu-id="448ae-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="448ae-190">Endre versjonsstatusen til Publisert</span><span class="sxs-lookup"><span data-stu-id="448ae-190">Change the version status to Published</span></span>

- <span data-ttu-id="448ae-191">På siden **E-faktureringsfunksjoner**, i kategorien **Versjoner**, velger du **Endre status \> Publiser**.</span><span class="sxs-lookup"><span data-stu-id="448ae-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="448ae-192">Publisere funksjonen for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="448ae-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="448ae-193">På siden **E-faktureringsfunksjoner** velger du kategorien **Versjoner** for å administrere statusen for funksjonen **CFDI-fakturaer (MX)**.</span><span class="sxs-lookup"><span data-stu-id="448ae-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="448ae-194">Velg **Endre status** for å endre statusen for funksjonen.</span><span class="sxs-lookup"><span data-stu-id="448ae-194">Select **Change status** to change the status of the feature.</span></span>

![Endre statusen for e-fakturafunksjonen](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="448ae-196">Konfigurere integrasjon av Elektronisk fakturering i Finance</span><span class="sxs-lookup"><span data-stu-id="448ae-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="448ae-197">Hvis du vil definere Elektronisk fakturering i Finance, må du fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="448ae-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="448ae-198">Importer ER-datamodellen, ER-datamodelltilordningen og formatene som kreves for CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="448ae-199">Konfigurer svartyper for oppdatering av CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="448ae-200">Disse svartypene brukes til svaret fra PAC-serveren (autorisert sertifiseringstjeneste).</span><span class="sxs-lookup"><span data-stu-id="448ae-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="448ae-201">Importere ER-datamodellen, ER-datamodelltilordning og kontekstkonfigurasjoner for CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="448ae-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="448ae-202">Logg på Finance.</span><span class="sxs-lookup"><span data-stu-id="448ae-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="448ae-203">I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du tittelen **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="448ae-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="448ae-204">Kontroller at konfigurasjonsleverandøren er satt til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="448ae-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="448ae-205">Hvis du ha mer informasjon om hvordan du setter en leverandør til **Aktiv**, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="448ae-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="448ae-206">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="448ae-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="448ae-207">Velg **Global ressurs \> Åpne**.</span><span class="sxs-lookup"><span data-stu-id="448ae-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="448ae-208">Importer **Fakturamodell**, **Fakturamodelltilordning**, **CFDI-fakturaformat (MX)**, **CFDI-fakturaannulleringsforespørselsformat (MX)** og **CFDI-fakturaavbruddsformat (MX)**.</span><span class="sxs-lookup"><span data-stu-id="448ae-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="448ae-209">Aktivere funksjonen for behandling av CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="448ae-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="448ae-210">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="448ae-211">I kategorien **Funksjoner** merker du av for **Aktiver** i radene for funksjonsreferanser **MX-00010** og **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="448ae-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![Aktivere funksjonene for behandling av CFDI-fakturaer](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="448ae-213">Importere ER-konfigurasjoner og konfigurere svartypene for oppdatering av CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="448ae-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="448ae-214">Importere ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="448ae-214">Import ER configurations</span></span>

1. <span data-ttu-id="448ae-215">I delen **Konfigurasjonsleverandører** i arbeidsområdet **Elektronisk rapportering** velger du tittelen **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="448ae-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="448ae-216">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="448ae-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="448ae-217">Velg **Global ressurs \> Åpne**.</span><span class="sxs-lookup"><span data-stu-id="448ae-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="448ae-218">Importer **Svarmeldingsmodell**, **Import av CFDI-feillogg (MX)** og **Import av CFDI-svarmelding (MX)**.</span><span class="sxs-lookup"><span data-stu-id="448ae-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="448ae-219">Definere svartypene</span><span class="sxs-lookup"><span data-stu-id="448ae-219">Set up the response types</span></span>

1. <span data-ttu-id="448ae-220">Gå til **Organisasjonsstyring \> Oppsett \> parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="448ae-221">I kategorien **Elektronisk dokument** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="448ae-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="448ae-222">Angi kundefakturajournalen, og deretter, i feltet **Tabellnavn**, velger du prosjektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="448ae-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="448ae-223">For hver tabell definerer du en relatert dokumentkontekst:</span><span class="sxs-lookup"><span data-stu-id="448ae-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="448ae-224">For **Kundefakturajournal** angir du **kundefakturakontekst**.</span><span class="sxs-lookup"><span data-stu-id="448ae-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="448ae-225">I **Prosjektfaktura** angir du **prosjektfakturakontekst**.</span><span class="sxs-lookup"><span data-stu-id="448ae-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="448ae-226">Velg **Svartyper** for å konfigurere svartypene som kan returneres fra Elektronisk fakturering og inkluderes i en kundefakturajournal eller prosjektfaktura.</span><span class="sxs-lookup"><span data-stu-id="448ae-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="448ae-227">Velg **Ny**, og deretter, i **Svartype**-feltet, velg **Svar**.</span><span class="sxs-lookup"><span data-stu-id="448ae-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="448ae-228">I feltet for **innsendingsstatus** velger du **Venter**.</span><span class="sxs-lookup"><span data-stu-id="448ae-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="448ae-229">I feltet **Modelltilordning** velg **svarmeldingsimportformat – modelltilordning fra svarmelding**.</span><span class="sxs-lookup"><span data-stu-id="448ae-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="448ae-230">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="448ae-230">Select **Save**.</span></span>
9. <span data-ttu-id="448ae-231">Velg **Ny**, og deretter, i **Svartype**-feltet, velg **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="448ae-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="448ae-232">I feltet for **innsendingsstatus** velger du **Venter**.</span><span class="sxs-lookup"><span data-stu-id="448ae-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="448ae-233">I **Modelltilordning**-feltet velger du **Format for dataimport av CFDI-svar (detaljer) – dataimport av svar**.</span><span class="sxs-lookup"><span data-stu-id="448ae-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="448ae-234">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="448ae-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="448ae-235">Behandle elektroniske fakturaer i Finance</span><span class="sxs-lookup"><span data-stu-id="448ae-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="448ae-236">Under behandlingen av CFDI-fakturaer i Finance via Elektronisk fakturering kan du utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="448ae-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="448ae-237">Sende CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="448ae-238">Vis utførelsesloggene for sending.</span><span class="sxs-lookup"><span data-stu-id="448ae-238">View the submission execution logs.</span></span>
- <span data-ttu-id="448ae-239">Send annullering for en CFDI-faktura.</span><span class="sxs-lookup"><span data-stu-id="448ae-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="448ae-240">Sende CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="448ae-240">Submit CFDI invoices</span></span>

<span data-ttu-id="448ae-241">Når du har aktivert funksjonen for **Konfigurerbar integrasjon av Elektronisk fakturering**, kan ikke prosessen for **eksport/import av elektronisk faktura** (**Kunder \> Fakturaer \> E-fakturaer**) for sending av CFDI-fakturaer brukes lenger.</span><span class="sxs-lookup"><span data-stu-id="448ae-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="448ae-242">Den erstattes av en ny prosess som kalles **Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="448ae-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="448ae-243">Før du bruker den nye prosessen **Send elektroniske dokumenter**, må du kontrollere at oppsettet som kreves for meksikanske e-fakturaer, ble fullført.</span><span class="sxs-lookup"><span data-stu-id="448ae-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="448ae-244">Hvis du vil ha mer informasjon, se [CFDI-oppsettversjon 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="448ae-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="448ae-245">Gå til **Organisasjonsstyring \> Periodiske \> Elektroniske dokumenter \> Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="448ae-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="448ae-246">For første innsending av et dokument må du alltid sette alternativet **Send dokumenter på nytt** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="448ae-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="448ae-247">Hvis du må sende et dokument på nytt via tjenesten, setter du dette alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="448ae-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="448ae-248">I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne **Forespørsel**-dialogboksen, der du kan bygge en spørring for å velge dokumenter for innsending.</span><span class="sxs-lookup"><span data-stu-id="448ae-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Sende et CFDI-dokument](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="448ae-250">Under det første forsøket på å sende et dokument via tjenesten, blir du bedt om å bekrefte tilkoblingen til Elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="448ae-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="448ae-251">Velg **Klikk her for å koble til innsendingstjeneste for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="448ae-252">Vise sendelogger</span><span class="sxs-lookup"><span data-stu-id="448ae-252">View submission logs</span></span>

<span data-ttu-id="448ae-253">Du kan vise sendeloggene for alle sendte dokumenter eller bare for ett sendt dokument.</span><span class="sxs-lookup"><span data-stu-id="448ae-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="448ae-254">Vise alle sendelogger</span><span class="sxs-lookup"><span data-stu-id="448ae-254">View all submission logs</span></span>

<span data-ttu-id="448ae-255">Når du har aktivert funksjonen **Konfigurerbar integrasjon av Elektronisk fakturering**, er en ny side tilgjengelig der du kan følge opp dokumentsendingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="448ae-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="448ae-256">Du kan bruke denne siden til å vise sendelogger for alle sendte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="448ae-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="448ae-257">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="448ae-258">I feltet **Dokumenttype** velger du **Kundefakturajournal** for å filtrere etter de påkrevde elektroniske dokumentene.</span><span class="sxs-lookup"><span data-stu-id="448ae-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Velge en dokumenttype for å vise sendelogger](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="448ae-260">I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.</span><span class="sxs-lookup"><span data-stu-id="448ae-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Vise detaljene for innsendingsloggen](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="448ae-262">Informasjonen i sendeloggene deles mellom tre hurtigfaner:</span><span class="sxs-lookup"><span data-stu-id="448ae-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="448ae-263">**Behandlingshandlinger** – Denne hurtigfanen viser utførelsesloggen for handlingene som er konfigurert i funksjonsversjonen som er definert i RCS.</span><span class="sxs-lookup"><span data-stu-id="448ae-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="448ae-264">**Status**-kolonnen viser om handlingen ble kjørt uten feil.</span><span class="sxs-lookup"><span data-stu-id="448ae-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="448ae-265">**Handlingsfiler** – Denne hurtigfanen viser de mellomliggende filene som ble generert under utføring av handlingene.</span><span class="sxs-lookup"><span data-stu-id="448ae-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="448ae-266">Du kan velge **Vis** for å laste ned filen og vise filen.</span><span class="sxs-lookup"><span data-stu-id="448ae-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="448ae-267">**Handlingslogg for behandling** – Denne hurtigfanen viser resultatet av kommunikasjonen mellom Elektronisk fakturering og målwebtjenesten.</span><span class="sxs-lookup"><span data-stu-id="448ae-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="448ae-268">Den viser også hva som ble returnert av behandlingen fra webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="448ae-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="448ae-269">Kolonnen **Feilkode** viser returkoden som ble returnert av webtjenesten for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="448ae-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="448ae-270">Når den sendte CFDI-fakturaen godkjennes, oppdateres statusen til **Godkjent**.</span><span class="sxs-lookup"><span data-stu-id="448ae-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="448ae-271">Vise sendelogger fra CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="448ae-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="448ae-272">Når du har aktivert funksjonen for **Konfigurerbar integrasjon av Elektronisk fakturering**, kan du også vise sendingsloggene fra CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="448ae-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="448ae-273">Gå til **Kunder \> Forespørsler og rapporter \> CFDI (elektroniske fakturaer)**.</span><span class="sxs-lookup"><span data-stu-id="448ae-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="448ae-274">Velg en CFDI-faktura som ble sendt etter at funksjonen for **Konfigurerbar integrasjon av Elektronisk fakturering** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="448ae-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="448ae-275">Velg **logg for elektronisk dokument** i kategorien **Logg** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="448ae-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Vise sendelogger fra CFDI-fakturaer](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="448ae-277">For CFDI-fakturaer som ble sendt før funksjonen for **Konfigurerbar integrasjon av Elektronisk fakturering** var aktivert, er **Logg**-knappen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="448ae-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="448ae-278">**Logg**-knappen ikke tilgjengelig for CFDI-fakturaer som ble sendt etter funksjonen for **Konfigurerbar integrasjon for Elektronisk fakturering** var aktivert.</span><span class="sxs-lookup"><span data-stu-id="448ae-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="448ae-279">Sende annullering for CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="448ae-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="448ae-280">Når du har aktivert funksjonen for **Konfigurerbar integrasjon av Elektronisk fakturering**, kan ikke lenger den gamle prosessen for avbryting av CFDI-fakturaer brukes.</span><span class="sxs-lookup"><span data-stu-id="448ae-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="448ae-281">Den erstattes av en ny avlysningsprosess som er innebygd på siden for **sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="448ae-282">Gå til **Kunder \> Forespørsler og rapporter \> CFDI (elektroniske fakturaer)**.</span><span class="sxs-lookup"><span data-stu-id="448ae-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="448ae-283">Hvis CFDI-fakturaen har statusen **Godkjent**, velger du **Funksjoner \> Avbryt CFDI**.</span><span class="sxs-lookup"><span data-stu-id="448ae-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="448ae-284">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="448ae-285">Velg CFDI-fakturaen, og velg deretter **Funksjoner \> Send relaterte innsendinger**.</span><span class="sxs-lookup"><span data-stu-id="448ae-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="448ae-286">Angi en beskrivelse for den tilknyttede sendingen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="448ae-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="448ae-287">Vise sendelogger for annullering</span><span class="sxs-lookup"><span data-stu-id="448ae-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="448ae-288">Gå til **Organisasjonsstyring \> Periodisk \> Elektroniske dokumenter \> sendingslogg for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="448ae-289">I feltet **Dokumenttype** velger du **Kundefakturajournal** for å filtrere etter bare kundefakturajournaldokumenter.</span><span class="sxs-lookup"><span data-stu-id="448ae-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="448ae-290">Velg CFDI-fakturaen, og velg deretter **Forespørsler \> Relatert sending** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="448ae-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="448ae-291">Siden **Relatert innsendinger** viser alle tilknyttede innsendinger, og sendestatusen, for en gitt CFDI-faktura.</span><span class="sxs-lookup"><span data-stu-id="448ae-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="448ae-292">I illustrasjonen nedenfor representerer den første linjen innsendingen som ber om godkjenning av CFDI-fakturaen.</span><span class="sxs-lookup"><span data-stu-id="448ae-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="448ae-293">Den andre linjen representerer innsendingen som avbrøt CFDI-fakturaen.</span><span class="sxs-lookup"><span data-stu-id="448ae-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Vise sendeloggene for annullering](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="448ae-295">I handlingsruten velger du **Forespørsler \> Innsendingsdetaljer** for å vise detaljene for sendeutførelsesloggene.</span><span class="sxs-lookup"><span data-stu-id="448ae-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Vise detaljer for sendeloggen for annullering](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="448ae-297">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="448ae-297">Privacy notice</span></span>
<span data-ttu-id="448ae-298">Aktivering av funksjonen **CFDI Meksikansk elektronisk faktura (MX)** krever kanskje sending av begrensede data, som inkluderer skatteregistrerings-ID-en for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="448ae-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="448ae-299">Dette overføres til tredjepartsleverandører autorisert av skattemyndigheten for å sende elektroniske fakturaer til skattemyndighetene i det forhåndsdefinerte formatet som kreves for integrering med myndighetenes webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="448ae-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="448ae-300">En administrator kan aktivere og deaktivere funksjonen **CFDI Meksikansk elektronisk faktura (MX)** ved å gå til **Organisasjonsstyring \> Oppsett \> Parametere for elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="448ae-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="448ae-301">Velg fanen **Funksjoner**, velg radene som inneholder funksjonen **CFDI Meksikansk elektronisk faktura (MX)**, og foreta deretter det riktige valget.</span><span class="sxs-lookup"><span data-stu-id="448ae-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="448ae-302">Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="448ae-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="448ae-303">Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.</span><span class="sxs-lookup"><span data-stu-id="448ae-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="448ae-304">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="448ae-304">Additional resources</span></span>

- [<span data-ttu-id="448ae-305">Oversikt over elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448ae-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="448ae-306">Komme i gang med Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448ae-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="448ae-307">Definere Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="448ae-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
