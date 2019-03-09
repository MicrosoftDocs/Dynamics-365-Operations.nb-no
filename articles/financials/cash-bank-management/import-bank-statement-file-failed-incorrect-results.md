---
title: Feilsøking for import av bankkontoutdragsfil
description: Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 for Finance and Operations støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4006bf35673e3bb61bcf11619ecc68d295f29eb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "324451"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="cacc5-107">Feilsøking for import av bankkontoutdragsfil</span><span class="sxs-lookup"><span data-stu-id="cacc5-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cacc5-108">Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 for Finance and Operations støtter.</span><span class="sxs-lookup"><span data-stu-id="cacc5-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="cacc5-109">På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig.</span><span class="sxs-lookup"><span data-stu-id="cacc5-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="cacc5-110">Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater.</span><span class="sxs-lookup"><span data-stu-id="cacc5-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="cacc5-111">Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="cacc5-112">Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.</span><span class="sxs-lookup"><span data-stu-id="cacc5-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="cacc5-113">Hva er feilen?</span><span class="sxs-lookup"><span data-stu-id="cacc5-113">What is the error?</span></span>
------------------

<span data-ttu-id="cacc5-114">Når du har forsøkt å importere en bankkontoutdragsfil, går du til jobbloggen for databehandling og kjøringsdetaljene for å finne feilen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="cacc5-115">Feilen kan være til hjelp ved at du peker på utdraget, saldoen eller utdragslinjen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="cacc5-116">Det er imidlertid ikke sannsynligvis at dette gir nok informasjon til at du finner feltet eller elementet som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="cacc5-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="cacc5-117">Hva er forskjellene?</span><span class="sxs-lookup"><span data-stu-id="cacc5-117">What are the differences?</span></span>
<span data-ttu-id="cacc5-118">Sammenlign bankfiloppsettsdefinisjonen med Finance and Operations-importdefinisjonen, og merk deg forskjellene i feltene og elementene.</span><span class="sxs-lookup"><span data-stu-id="cacc5-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="cacc5-119">Sammenlign bankkontoutdragsfilen med den tilknyttede Finance and Operations-eksempelfilen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="cacc5-120">Eventuelle forskjeller bør være lett å se i ISO20022-filene.</span><span class="sxs-lookup"><span data-stu-id="cacc5-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="cacc5-121">Transformasjoner</span><span class="sxs-lookup"><span data-stu-id="cacc5-121">Transformations</span></span>
<span data-ttu-id="cacc5-122">Endringen må vanligvis foretas i én av tre transformasjoner.</span><span class="sxs-lookup"><span data-stu-id="cacc5-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="cacc5-123">Hver enkelt transformasjon er skrevet for en bestemt standard.</span><span class="sxs-lookup"><span data-stu-id="cacc5-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="cacc5-124">Ressursnavn</span><span class="sxs-lookup"><span data-stu-id="cacc5-124">Resource name</span></span>                                         | <span data-ttu-id="cacc5-125">Filnavn</span><span class="sxs-lookup"><span data-stu-id="cacc5-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="cacc5-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="cacc5-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="cacc5-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="cacc5-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="cacc5-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="cacc5-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="cacc5-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="cacc5-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="cacc5-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="cacc5-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="cacc5-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="cacc5-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="cacc5-132">Feilsøking av transformasjoner</span><span class="sxs-lookup"><span data-stu-id="cacc5-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="cacc5-133">Juster BAI2- og MT940-filene</span><span class="sxs-lookup"><span data-stu-id="cacc5-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="cacc5-134">BAI2- og MT940-filene er tekstbaserte filer, og krever en justering for å gjøre det mulig med feilsøking av Extensible Stylesheet Language Transformations (XSLT).</span><span class="sxs-lookup"><span data-stu-id="cacc5-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="cacc5-135">Programmet gjør denne justeringen når en fil importeres.</span><span class="sxs-lookup"><span data-stu-id="cacc5-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="cacc5-136">Opprett en XML-fil, og kopier følgende tekst til den.</span><span class="sxs-lookup"><span data-stu-id="cacc5-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="cacc5-137">Kopier innholdet i bankkontoutdragsfilen og lim det inn i XML-filen slik at det erstatter **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="cacc5-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="cacc5-138">Feilsøking av XSLT</span><span class="sxs-lookup"><span data-stu-id="cacc5-138">Debug the XSLT</span></span>

<span data-ttu-id="cacc5-139">Hvis du vil ha mer informasjon, kan du se <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="cacc5-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="cacc5-140">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cacc5-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="cacc5-141">Opprett et konsollprogram.</span><span class="sxs-lookup"><span data-stu-id="cacc5-141">Create a console application.</span></span>
3.  <span data-ttu-id="cacc5-142">Åpne aktuell XSLT.</span><span class="sxs-lookup"><span data-stu-id="cacc5-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="cacc5-143">Klikk XLST-en og den tilhørende egenskapssiden.</span><span class="sxs-lookup"><span data-stu-id="cacc5-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="cacc5-144">Angi inndataene til plasseringen av bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="cacc5-145">Definer en plassering og et filnavn for utdataene.</span><span class="sxs-lookup"><span data-stu-id="cacc5-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="cacc5-146">Angi de nødvendige bruddpunktene.</span><span class="sxs-lookup"><span data-stu-id="cacc5-146">Set the required break points.</span></span>
8.  <span data-ttu-id="cacc5-147">Klikk **XML** på menyen &gt; **Start XSLT Debugging**.</span><span class="sxs-lookup"><span data-stu-id="cacc5-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="cacc5-148">Formater XSLT-utdataene</span><span class="sxs-lookup"><span data-stu-id="cacc5-148">Format the XSLT output</span></span>

<span data-ttu-id="cacc5-149">Når transformeringen kjøres, opprettes det en utdatafil som du kan vise i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cacc5-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="cacc5-150">Bruk Ctrl + A, Ctrl + K og Ctrl + D til raskt å formatere utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="cacc5-151">Juster transformasjonen</span><span class="sxs-lookup"><span data-stu-id="cacc5-151">Adjust the transformation</span></span>

<span data-ttu-id="cacc5-152">Juster transformasjonen for å hente det riktige feltet eller elementet i bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="cacc5-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="cacc5-153">Tilordne deretter feltet eller elementet til det aktuelle elementet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cacc5-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="cacc5-154">Indikator for debet/kredit</span><span class="sxs-lookup"><span data-stu-id="cacc5-154">Debit/credit indicator</span></span>

<span data-ttu-id="cacc5-155">Noen ganger importeres debetbeløp som kreditbeløp og kreditbeløp som debetbeløp.</span><span class="sxs-lookup"><span data-stu-id="cacc5-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="cacc5-156">Du kan løse dette problemet ved å endre riktig XSLT-fil.</span><span class="sxs-lookup"><span data-stu-id="cacc5-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="cacc5-157">Hvis bankkontoutdrag kommer fra flere banker, må du kontrollere at alle bruker samme fremgangsmåte for debet/kredit, eller opprette egne transformasjoner.</span><span class="sxs-lookup"><span data-stu-id="cacc5-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="cacc5-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-malen</span><span class="sxs-lookup"><span data-stu-id="cacc5-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="cacc5-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit-malen</span><span class="sxs-lookup"><span data-stu-id="cacc5-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="cacc5-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-malen</span><span class="sxs-lookup"><span data-stu-id="cacc5-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="cacc5-161">Eksempler på bankkontoutdragsformater og tekniske oppsett</span><span class="sxs-lookup"><span data-stu-id="cacc5-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="cacc5-162">Tabellen nedenfor inneholder eksempler på definisjonene av tekniske oppsett for avanserte bankavstemmingsimportfiler og tre tilknyttede filer med eksempler på bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="cacc5-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="cacc5-163">Du kan laste ned eksempelfilene og tekniske oppsett her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="cacc5-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="cacc5-164">Definisjon av teknisk oppsett</span><span class="sxs-lookup"><span data-stu-id="cacc5-164">Technical layout definition</span></span>                             | <span data-ttu-id="cacc5-165">Fil med bankkontoutdragseksempler</span><span class="sxs-lookup"><span data-stu-id="cacc5-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="cacc5-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="cacc5-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="cacc5-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="cacc5-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="cacc5-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="cacc5-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="cacc5-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="cacc5-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="cacc5-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="cacc5-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="cacc5-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="cacc5-171">BAI2StatementExample</span></span>                 |





