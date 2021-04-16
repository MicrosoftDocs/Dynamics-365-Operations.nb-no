---
title: Feilsøking for import av bankkontoutdragsfil
description: Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter. På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig. Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater. Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen. Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815890"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="2abec-107">Feilsøking for import av bankkontoutdragsfil</span><span class="sxs-lookup"><span data-stu-id="2abec-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2abec-108">Det er viktig at bankkontoutdragsfilen fra banken stemmer overens med oppsettet som Microsoft Dynamics 365 Finance støtter.</span><span class="sxs-lookup"><span data-stu-id="2abec-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="2abec-109">På grunn av strenge standarder for bankkontoutdrag vil de fleste integreringer fungere riktig.</span><span class="sxs-lookup"><span data-stu-id="2abec-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="2abec-110">Noen ganger kan imidlertid ikke utdragsfilen importeres eller har feil resultater.</span><span class="sxs-lookup"><span data-stu-id="2abec-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="2abec-111">Disse problemene forårsakes vanligvis av små forskjeller i bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="2abec-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="2abec-112">Denne artikkelen forklarer hvordan disse forskjellene kan korrigeres og problemene løses.</span><span class="sxs-lookup"><span data-stu-id="2abec-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="2abec-113">Hva er feilen?</span><span class="sxs-lookup"><span data-stu-id="2abec-113">What is the error?</span></span>
------------------

<span data-ttu-id="2abec-114">Når du har forsøkt å importere en bankkontoutdragsfil, går du til jobbloggen for databehandling og kjøringsdetaljene for å finne feilen.</span><span class="sxs-lookup"><span data-stu-id="2abec-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="2abec-115">Feilen kan være til hjelp ved at du peker på utdraget, saldoen eller utdragslinjen.</span><span class="sxs-lookup"><span data-stu-id="2abec-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="2abec-116">Det er imidlertid ikke sannsynligvis at dette gir nok informasjon til at du finner feltet eller elementet som forårsaker problemet.</span><span class="sxs-lookup"><span data-stu-id="2abec-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="2abec-117">Importerte bankkontoutdrag kan bare overlappe for ett enkelt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="2abec-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="2abec-118">Hvis et utdrag for eksempel slutter klokken 12:00 1. januar 2021, kan startdatoen for det neste utdraget være 12:00 1. januar 2021.</span><span class="sxs-lookup"><span data-stu-id="2abec-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="2abec-119">Hva er forskjellene?</span><span class="sxs-lookup"><span data-stu-id="2abec-119">What are the differences?</span></span>
<span data-ttu-id="2abec-120">Sammenlign bankfiloppsettsdefinisjonen med Finance-importdefinisjonen, og merk deg forskjellene i feltene og elementene.</span><span class="sxs-lookup"><span data-stu-id="2abec-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="2abec-121">Sammenlign bankkontoutdragsfilen med den tilknyttede Finance-eksempelfilen.</span><span class="sxs-lookup"><span data-stu-id="2abec-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="2abec-122">Eventuelle forskjeller bør være lett å se i ISO20022-filene.</span><span class="sxs-lookup"><span data-stu-id="2abec-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="2abec-123">Tidssoneforskjeller på importerte bankkontoutdrag</span><span class="sxs-lookup"><span data-stu-id="2abec-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="2abec-124">Dato- og klokkeslettverdiene i importfilen kan være forskjellige fra dato- og klokkeslettverdiene som vises i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2abec-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="2abec-125">Hvis du vil unngå dette avviket, angir du en tidssoneinnstilling på siden **Konfigurer datakilder**.</span><span class="sxs-lookup"><span data-stu-id="2abec-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="2abec-126">Hvis du vil ha mer informasjon om hvordan du angir en tidssoneinnstilling, kan du se [Definere prosessen for avansert bankavstemmingsimport](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="2abec-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="2abec-127">Transformasjoner</span><span class="sxs-lookup"><span data-stu-id="2abec-127">Transformations</span></span>
<span data-ttu-id="2abec-128">Endringen må vanligvis foretas i én av tre transformasjoner.</span><span class="sxs-lookup"><span data-stu-id="2abec-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="2abec-129">Hver enkelt transformasjon er skrevet for en bestemt standard.</span><span class="sxs-lookup"><span data-stu-id="2abec-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="2abec-130">Ressursnavn</span><span class="sxs-lookup"><span data-stu-id="2abec-130">Resource name</span></span>                                         | <span data-ttu-id="2abec-131">Filnavn</span><span class="sxs-lookup"><span data-stu-id="2abec-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="2abec-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="2abec-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="2abec-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="2abec-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="2abec-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="2abec-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="2abec-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="2abec-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="2abec-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="2abec-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="2abec-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="2abec-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="2abec-138">Feilsøking av transformasjoner</span><span class="sxs-lookup"><span data-stu-id="2abec-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="2abec-139">Juster BAI2- og MT940-filene</span><span class="sxs-lookup"><span data-stu-id="2abec-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="2abec-140">BAI2- og MT940-filene er tekstbaserte filer, og krever en justering for å gjøre det mulig med feilsøking av Extensible Stylesheet Language Transformations (XSLT).</span><span class="sxs-lookup"><span data-stu-id="2abec-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="2abec-141">Programmet gjør denne justeringen når en fil importeres.</span><span class="sxs-lookup"><span data-stu-id="2abec-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="2abec-142">Opprett en XML-fil, og kopier følgende tekst til den.</span><span class="sxs-lookup"><span data-stu-id="2abec-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="2abec-143">Kopier innholdet i bankkontoutdragsfilen og lim det inn i XML-filen slik at det erstatter **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="2abec-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="2abec-144">Feilsøking av XSLT</span><span class="sxs-lookup"><span data-stu-id="2abec-144">Debug the XSLT</span></span>

<span data-ttu-id="2abec-145">Hvis du vil ha mer informasjon, kan du se <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="2abec-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="2abec-146">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2abec-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="2abec-147">Opprett et konsollprogram.</span><span class="sxs-lookup"><span data-stu-id="2abec-147">Create a console application.</span></span>
3.  <span data-ttu-id="2abec-148">Åpne aktuell XSLT.</span><span class="sxs-lookup"><span data-stu-id="2abec-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="2abec-149">Klikk XLST-en og den tilhørende egenskapssiden.</span><span class="sxs-lookup"><span data-stu-id="2abec-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="2abec-150">Angi inndataene til plasseringen av bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="2abec-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="2abec-151">Definer en plassering og et filnavn for utdataene.</span><span class="sxs-lookup"><span data-stu-id="2abec-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="2abec-152">Angi de nødvendige bruddpunktene.</span><span class="sxs-lookup"><span data-stu-id="2abec-152">Set the required break points.</span></span>
8.  <span data-ttu-id="2abec-153">Klikk **XML** på menyen &gt; **Start XSLT Debugging**.</span><span class="sxs-lookup"><span data-stu-id="2abec-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="2abec-154">Formater XSLT-utdataene</span><span class="sxs-lookup"><span data-stu-id="2abec-154">Format the XSLT output</span></span>

<span data-ttu-id="2abec-155">Når transformeringen kjøres, opprettes det en utdatafil som du kan vise i Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2abec-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="2abec-156">Bruk Ctrl + A, Ctrl + K og Ctrl + D til raskt å formatere utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="2abec-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="2abec-157">Juster transformasjonen</span><span class="sxs-lookup"><span data-stu-id="2abec-157">Adjust the transformation</span></span>

<span data-ttu-id="2abec-158">Juster transformasjonen for å hente det riktige feltet eller elementet i bankkontoutdragsfilen.</span><span class="sxs-lookup"><span data-stu-id="2abec-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="2abec-159">Tilordne deretter feltet eller elementet til det aktuelle elementet i Finance.</span><span class="sxs-lookup"><span data-stu-id="2abec-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="2abec-160">Indikator for debet/kredit</span><span class="sxs-lookup"><span data-stu-id="2abec-160">Debit/credit indicator</span></span>

<span data-ttu-id="2abec-161">Noen ganger importeres debetbeløp som kreditbeløp og kreditbeløp som debetbeløp.</span><span class="sxs-lookup"><span data-stu-id="2abec-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="2abec-162">Du kan løse dette problemet ved å endre riktig XSLT-fil.</span><span class="sxs-lookup"><span data-stu-id="2abec-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="2abec-163">Hvis bankkontoutdrag kommer fra flere banker, må du kontrollere at alle bruker samme fremgangsmåte for debet/kredit, eller opprette egne transformasjoner.</span><span class="sxs-lookup"><span data-stu-id="2abec-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="2abec-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-malen</span><span class="sxs-lookup"><span data-stu-id="2abec-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="2abec-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit-malen</span><span class="sxs-lookup"><span data-stu-id="2abec-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="2abec-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-malen</span><span class="sxs-lookup"><span data-stu-id="2abec-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="2abec-167">Eksempler på bankkontoutdragsformater og tekniske oppsett</span><span class="sxs-lookup"><span data-stu-id="2abec-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="2abec-168">Tabellen nedenfor inneholder eksempler på definisjonene av tekniske oppsett for avanserte bankavstemmingsimportfiler og tre tilknyttede filer med eksempler på bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="2abec-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="2abec-169">Du kan laste ned eksempelfilene og tekniske oppsett her: [Importer fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="2abec-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="2abec-170">Definisjon av teknisk oppsett</span><span class="sxs-lookup"><span data-stu-id="2abec-170">Technical layout definition</span></span>                             | <span data-ttu-id="2abec-171">Fil med bankkontoutdragseksempler</span><span class="sxs-lookup"><span data-stu-id="2abec-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="2abec-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="2abec-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="2abec-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="2abec-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="2abec-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="2abec-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="2abec-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="2abec-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="2abec-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="2abec-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="2abec-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="2abec-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
