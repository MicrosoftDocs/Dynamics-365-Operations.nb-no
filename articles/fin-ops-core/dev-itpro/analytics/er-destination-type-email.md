---
title: Sende ER-måltype per e-post
description: Dette emnet inneholder informasjon om hvordan du konfigurerer et e-postmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019926"
---
# <span data-ttu-id="551ae-103"><a name="EmailDestinationType">E-postmål</a></span><span class="sxs-lookup"><span data-stu-id="551ae-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="551ae-104">Du kan konfigurere et e-postmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="551ae-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="551ae-105">Basert på målinnstillingen leveres et generert dokument som et vedlegg til en elektronisk post.</span><span class="sxs-lookup"><span data-stu-id="551ae-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="551ae-106">Sett **Aktivert** til **Ja** for å sende en utdatafil via e-post.</span><span class="sxs-lookup"><span data-stu-id="551ae-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="551ae-107">Når dette alternativet er aktivert, kan du angi e-postmottakere og redigere emnet og brødteksten i e-postmeldingen.</span><span class="sxs-lookup"><span data-stu-id="551ae-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="551ae-108">Du kan definere konstante tekster for e-postemnet og meldingsteksten, eller du kan bruke ER-[formler](er-formula-language.md) for å opprette e-posttekster dynamisk.</span><span class="sxs-lookup"><span data-stu-id="551ae-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="551ae-109">Du kan konfigurere e-postadresser for ER på to måter.</span><span class="sxs-lookup"><span data-stu-id="551ae-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="551ae-110">Konfigurasjonen kan fullføres på samme måte som Utskriftsbehandling-funksjonen fullfører den, eller du kan løse en e-postadresse ved å bruke en direkte referanse til ER-konfigurasjonen via en formel.</span><span class="sxs-lookup"><span data-stu-id="551ae-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="551ae-111">[![Aktivere e-postmål](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="551ae-112">Typer e-postadresser</span><span class="sxs-lookup"><span data-stu-id="551ae-112">Email address types</span></span>

<span data-ttu-id="551ae-113">Når du velger **Rediger** i **Til**- eller **Cc**-feltet, vises**E-post til**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="551ae-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="551ae-114">Du kan deretter velge hvilken type e-postadresse som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="551ae-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="551ae-115">E-posttypene **Konfigurasjons-e-post** og **Utskriftsbehandling** støttes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="551ae-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="551ae-116">[![Velge e-posttype](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="551ae-117">Utskriftsbehandling</span><span class="sxs-lookup"><span data-stu-id="551ae-117">Print management</span></span>

<span data-ttu-id="551ae-118">Hvis du velger e-posttypen **Utskriftsbehandling**, kan du angi faste e-postadresser i **Til**-feltet.</span><span class="sxs-lookup"><span data-stu-id="551ae-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="551ae-119">[![Konfigurere faste e-postadresser](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="551ae-120">Hvis du vil bruke e-postadresser som ikke er faste, må du velge kildetypen e-post for et filmål.</span><span class="sxs-lookup"><span data-stu-id="551ae-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="551ae-121">Følgende verdier støttes: **kunde**, **leverandør**, **kundeemne**, **kontakt**, **konkurrent**, **arbeider**, **søker**, **potensiell leverandør** og **sperret leverandør**.</span><span class="sxs-lookup"><span data-stu-id="551ae-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="551ae-122">Når du har valgt en e-postkildetype, bruker du knappen ved siden av feltet **Kildekonto for e-post** til å åpne skjemaet **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="551ae-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="551ae-123">Du kan bruke dette skjemaet til å legge ved en formel som ved kjøretid returnerer **partskontoen** for den valgte kildetypen fra det behandlede dokumentet til e-postmålet.</span><span class="sxs-lookup"><span data-stu-id="551ae-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="551ae-124">[![Konfigurere e-postkildekonto](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="551ae-125">Formler er spesifikke for ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="551ae-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="551ae-126">Angi en dokumentspesifikk referanse til en kunde- eller leverandørparttype i **Formel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="551ae-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="551ae-127">I stedet for å skrive inn kan du finne en datakildenode som representerer kunde- eller leverandørkontoen, og deretter velge **Legg til datakilde** for å oppdatere formelen.</span><span class="sxs-lookup"><span data-stu-id="551ae-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="551ae-128">Hvis du for eksempel bruker **ISO 20022-kredittoverføring**-konfigurasjonen, er noden som representerer en leverandørkonto, `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="551ae-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="551ae-129">Hvis du angir en strengverdi, for eksempel `"DE-001"` og lagrer en formel, sendes det en e-postmelding til leverandørens kontaktperson, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="551ae-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="551ae-130">[![ER-formelutforming-siden](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="551ae-131">[![Konfigurere e-postkildekonto](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="551ae-132">E-post for konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="551ae-132">Configuration email</span></span>

<span data-ttu-id="551ae-133">Bruk denne e-posttypen hvis konfigurasjonen du bruker, har en node i datakildene som returnerer en **e-postadresse**.</span><span class="sxs-lookup"><span data-stu-id="551ae-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="551ae-134">Du kan bruke datakilder og funksjoner i formeldesigner for å få en riktig formatert e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="551ae-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="551ae-135">Hvis du for eksempel bruker **ISO 20022-kredittoverføring**-konfigurasjonen, er noden som representerer en e-postadresse til en leverandørs kontaktperson, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="551ae-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="551ae-136">[![Konfigurere e-postadressekilde](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="551ae-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="551ae-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="551ae-137">Additional resources</span></span>

- [<span data-ttu-id="551ae-138">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="551ae-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="551ae-139">Mål for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="551ae-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="551ae-140">Formeldesigner i elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="551ae-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
