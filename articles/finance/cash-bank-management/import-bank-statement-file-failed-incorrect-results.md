---
title: Feilsøking for import av bankkontoutdragsfil
description: Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 612ded1f68cc8e1b26b8046501bae1707175e23a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188332"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="11253-107">Feilsøking for import av bankkontoutdragsfil</span><span class="sxs-lookup"><span data-stu-id="11253-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11253-108">Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter.</span><span class="sxs-lookup"><span data-stu-id="11253-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="11253-109">På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig.</span><span class="sxs-lookup"><span data-stu-id="11253-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="11253-110">Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater.</span><span class="sxs-lookup"><span data-stu-id="11253-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="11253-111">Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="11253-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="11253-112">Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.</span><span class="sxs-lookup"><span data-stu-id="11253-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="11253-113">Hva er feilen?</span><span class="sxs-lookup"><span data-stu-id="11253-113">What is the error?</span></span>
------------------

<span data-ttu-id="11253-114">Når du har forsøkt å importere en bankkontoutdragsfil, går du til jobbloggen for databehandling og kjøringsdetaljene for å finne feilen.</span><span class="sxs-lookup"><span data-stu-id="11253-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="11253-115">Feilen kan være til hjelp ved at du peker på utdraget, saldoen eller utdragslinjen.</span><span class="sxs-lookup"><span data-stu-id="11253-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="11253-116">Det er imidlertid ikke sannsynligvis at dette gir nok informasjon til at du finner feltet eller elementet som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="11253-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="11253-117">Hva er forskjellene?</span><span class="sxs-lookup"><span data-stu-id="11253-117">What are the differences?</span></span>
<span data-ttu-id="11253-118">Sammenlign bankfiloppsettsdefinisjonen med Finance-importdefinisjonen, og merk deg forskjellene i feltene og elementene.</span><span class="sxs-lookup"><span data-stu-id="11253-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="11253-119">Sammenlign bankkontoutdragsfilen med den tilknyttede Finance-eksempelfilen.</span><span class="sxs-lookup"><span data-stu-id="11253-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="11253-120">Eventuelle forskjeller bør være lett å se i ISO20022-filene.</span><span class="sxs-lookup"><span data-stu-id="11253-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="11253-121">Tidssoneforskjeller på importerte bankkontoutdrag</span><span class="sxs-lookup"><span data-stu-id="11253-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="11253-122">Dato- og klokkeslettverdiene i importfilen kan være forskjellige fra dato- og klokkeslettverdiene som vises i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11253-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="11253-123">Hvis du vil unngå dette avviket, angir du en tidssoneinnstilling på siden **Konfigurer datakilder**.</span><span class="sxs-lookup"><span data-stu-id="11253-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="11253-124">Hvis du vil ha mer informasjon om hvordan du angir en tidssoneinnstilling, kan du se [Definere prosessen for avansert bankavstemmingsimport](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="11253-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="11253-125">Transformasjoner</span><span class="sxs-lookup"><span data-stu-id="11253-125">Transformations</span></span>
<span data-ttu-id="11253-126">Endringen må vanligvis foretas i én av tre transformasjoner.</span><span class="sxs-lookup"><span data-stu-id="11253-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="11253-127">Hver enkelt transformasjon er skrevet for en bestemt standard.</span><span class="sxs-lookup"><span data-stu-id="11253-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="11253-128">Ressursnavn</span><span class="sxs-lookup"><span data-stu-id="11253-128">Resource name</span></span>                                         | <span data-ttu-id="11253-129">Filnavn</span><span class="sxs-lookup"><span data-stu-id="11253-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="11253-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="11253-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="11253-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="11253-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="11253-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="11253-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="11253-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="11253-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="11253-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="11253-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="11253-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="11253-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="11253-136">Feilsøking av transformasjoner</span><span class="sxs-lookup"><span data-stu-id="11253-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="11253-137">Juster BAI2- og MT940-filene</span><span class="sxs-lookup"><span data-stu-id="11253-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="11253-138">BAI2- og MT940-filene er tekstbaserte filer, og krever en justering for å gjøre det mulig med feilsøking av Extensible Stylesheet Language Transformations (XSLT).</span><span class="sxs-lookup"><span data-stu-id="11253-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="11253-139">Programmet gjør denne justeringen når en fil importeres.</span><span class="sxs-lookup"><span data-stu-id="11253-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="11253-140">Opprett en XML-fil, og kopier følgende tekst til den.</span><span class="sxs-lookup"><span data-stu-id="11253-140">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="11253-141">Kopier innholdet i bankkontoutdragsfilen og lim det inn i XML-filen slik at det erstatter **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="11253-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="11253-142">Feilsøking av XSLT</span><span class="sxs-lookup"><span data-stu-id="11253-142">Debug the XSLT</span></span>

<span data-ttu-id="11253-143">Hvis du vil ha mer informasjon, kan du se <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="11253-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="11253-144">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="11253-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="11253-145">Opprett et konsollprogram.</span><span class="sxs-lookup"><span data-stu-id="11253-145">Create a console application.</span></span>
3.  <span data-ttu-id="11253-146">Åpne aktuell XSLT.</span><span class="sxs-lookup"><span data-stu-id="11253-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="11253-147">Klikk XLST-en og den tilhørende egenskapssiden.</span><span class="sxs-lookup"><span data-stu-id="11253-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="11253-148">Angi inndataene til plasseringen av bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="11253-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="11253-149">Definer en plassering og et filnavn for utdataene.</span><span class="sxs-lookup"><span data-stu-id="11253-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="11253-150">Angi de nødvendige bruddpunktene.</span><span class="sxs-lookup"><span data-stu-id="11253-150">Set the required break points.</span></span>
8.  <span data-ttu-id="11253-151">Klikk **XML** på menyen &gt; **Start XSLT Debugging**.</span><span class="sxs-lookup"><span data-stu-id="11253-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="11253-152">Formater XSLT-utdataene</span><span class="sxs-lookup"><span data-stu-id="11253-152">Format the XSLT output</span></span>

<span data-ttu-id="11253-153">Når transformeringen kjøres, opprettes det en utdatafil som du kan vise i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="11253-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="11253-154">Bruk Ctrl + A, Ctrl + K og Ctrl + D til raskt å formatere utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="11253-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="11253-155">Juster transformasjonen</span><span class="sxs-lookup"><span data-stu-id="11253-155">Adjust the transformation</span></span>

<span data-ttu-id="11253-156">Juster transformasjonen for å hente det riktige feltet eller elementet i bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="11253-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="11253-157">Tilordne deretter feltet eller elementet til det aktuelle elementet i Finance.</span><span class="sxs-lookup"><span data-stu-id="11253-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="11253-158">Indikator for debet/kredit</span><span class="sxs-lookup"><span data-stu-id="11253-158">Debit/credit indicator</span></span>

<span data-ttu-id="11253-159">Noen ganger importeres debetbeløp som kreditbeløp og kreditbeløp som debetbeløp.</span><span class="sxs-lookup"><span data-stu-id="11253-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="11253-160">Du kan løse dette problemet ved å endre riktig XSLT-fil.</span><span class="sxs-lookup"><span data-stu-id="11253-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="11253-161">Hvis bankkontoutdrag kommer fra flere banker, må du kontrollere at alle bruker samme fremgangsmåte for debet/kredit, eller opprette egne transformasjoner.</span><span class="sxs-lookup"><span data-stu-id="11253-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="11253-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-malen</span><span class="sxs-lookup"><span data-stu-id="11253-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="11253-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit-malen</span><span class="sxs-lookup"><span data-stu-id="11253-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="11253-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-malen</span><span class="sxs-lookup"><span data-stu-id="11253-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="11253-165">Eksempler på bankkontoutdragsformater og tekniske oppsett</span><span class="sxs-lookup"><span data-stu-id="11253-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="11253-166">Tabellen nedenfor inneholder eksempler på definisjonene av tekniske oppsett for avanserte bankavstemmingsimportfiler og tre tilknyttede filer med eksempler på bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="11253-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="11253-167">Du kan laste ned eksempelfilene og tekniske oppsett her: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="11253-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="11253-168">Definisjon av teknisk oppsett</span><span class="sxs-lookup"><span data-stu-id="11253-168">Technical layout definition</span></span>                             | <span data-ttu-id="11253-169">Fil med bankkontoutdragseksempler</span><span class="sxs-lookup"><span data-stu-id="11253-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="11253-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="11253-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="11253-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="11253-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="11253-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="11253-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="11253-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="11253-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="11253-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="11253-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="11253-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="11253-175">BAI2StatementExample</span></span>                 |





