---
title: Utforme ER-konfigurasjoner for å slette BOM-tegn i genererte filer
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som sletter merker for byterekkefølge (BOM-tegn).
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060825"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="3d5a3-103">Utforme ER-konfigurasjoner for å slette BOM-tegn i genererte filer</span><span class="sxs-lookup"><span data-stu-id="3d5a3-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d5a3-104">Du kan utforme en [løsning](er-quick-start1-new-solution.md) for [Elektronisk rapportering (ER)](general-electronic-reporting.md) for å generere utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="3d5a3-105">Hvis du vil generere dokumentene som tekst- eller XML-filer, må løsningen omfatte en ER-[konfigurasjon](general-electronic-reporting.md#Configuration) som inneholder en komponent for ER-[format](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="3d5a3-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="3d5a3-106">Hvis du vil angi [tegnkodingen](https://docs.microsoft.com/windows/win32/intl/character-sets) som representerer tegnsettet i genererte filer, må ER-formatet inneholde formatelementet **Felles\\Fil**.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="3d5a3-107">Hvis du vil konfigurere ER-formatkomponenten, åpner du [utkast](general-electronic-reporting.md#component-versioning)versjonen av ER-konfigurasjonen i ER-formatutformingen og legger til elementet **Felles\\Fil**.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="3d5a3-108">I **Koding**-feltet angir du kodingen for utgående filer som genereres ved kjøretid ved hjelp av denne komponenten.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="3d5a3-109">Hvis formatet inneholder feil kodingsnavn, oppstår det en feil når du lagrer endringene i innstillingene for formatet.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Legge til et rotelement på Formatutforming-siden](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="3d5a3-111">Hvis du angir **UTF-8**, **UTF-16** eller **UTF-32** som kodingen, blir alternativet **Slett BOM-tegn** tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="3d5a3-112">Sett dette alternativet til **Ja** for å slette [merker for byterekkefølge (BOM-tegn)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) i utgående filer som genereres ved kjøretid når det redigerbare ER-formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="3d5a3-113">Hvis du lar **Koding**-feltet være tomt, brukes standard **UTF-8**-koding.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Angi alternativet Slett BOM-tegn på Formatutforming-siden](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="3d5a3-115">Fullfør den riktige fremgangsmåten for å gå gjennom funksjonaliteten ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="3d5a3-116">Fullfør for eksempel fremgangsmåten i emnet [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md).</span><span class="sxs-lookup"><span data-stu-id="3d5a3-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="3d5a3-117">Når du har fullført fremgangsmåten i delen [Endre formatet slik at beregningen baseres på genererte utdata](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) i det emnet, følger du disse tilleggstrinnene.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="3d5a3-118">Angi UTF-kodingen:</span><span class="sxs-lookup"><span data-stu-id="3d5a3-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="3d5a3-119">Velg **Rapport**-elementet av typen **Felles\\Fil**.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="3d5a3-120">Angi **UTF-8**-kodingen i **Koding**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="3d5a3-121">Generer en XML-fil som inneholder et BOM-tegn:</span><span class="sxs-lookup"><span data-stu-id="3d5a3-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="3d5a3-122">Angi **Nei** for alternativet **Slett BOM-tegn** for å ta med BOM-tegn i genererte XML-filer.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="3d5a3-123">Fullfør fremgangsmåten i delen [Utsett kjøringen av XML-elementet Sammendrag slik at beregnet sum brukes](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) i emnet [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md), og lagre den genererte filen som **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="3d5a3-124">Generer en XML-fil som ikke inneholder et BOM-tegn:</span><span class="sxs-lookup"><span data-stu-id="3d5a3-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="3d5a3-125">Angi **Ja** for alternativet **Slett BOM-tegn** for å slette BOM-tegn i genererte XML-filer.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="3d5a3-126">Fullfør fremgangsmåten i delen [Utsett kjøringen av XML-elementet Sammendrag slik at beregnet sum brukes](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) i emnet [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md), og lagre den genererte filen som **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="3d5a3-127">Sammenlign de genererte filene i et verktøy for sammenligning av filer.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="3d5a3-128">Den første forskjellen du vil legge merke til, er i filhodet.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="3d5a3-129">Filen SampleXmlReport.xml inneholder et BOM-tegn, mens filen SampleXmlReport (1).xml ikke gjør det.</span><span class="sxs-lookup"><span data-stu-id="3d5a3-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Sammenligne genererte filer ved å bruke et verktøy for sammenligning av filer](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="3d5a3-131">Se også</span><span class="sxs-lookup"><span data-stu-id="3d5a3-131">See also</span></span>

- [<span data-ttu-id="3d5a3-132">Utsette kjøringen av XML-elementer i ER-formater</span><span class="sxs-lookup"><span data-stu-id="3d5a3-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)
