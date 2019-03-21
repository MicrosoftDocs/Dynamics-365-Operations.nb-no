---
title: Definere og generere positive betalingsfiler
description: Dette emnet forklarer hvordan du konfigurerer positiv betaling og genererer positive betalingsfiler.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: dbc512c6d214dc8cf2527ac23103529111896ec5
ms.sourcegitcommit: 065d9fab832b6bcc88c00dc78ac1ae854c762ec7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/06/2019
ms.locfileid: "778184"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="b3ac6-103">Definere og generere positive betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="b3ac6-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3ac6-104">Dette emnet forklarer hvordan du konfigurerer positiv betaling og genererer positive betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="b3ac6-105">Definer positiv betaling for å generere en elektronisk liste over sjekker som leveres til banken.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="b3ac6-106">Når sjekken presenteres til banken, sammenligner banken deretter sjekken med listen over sjekker.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="b3ac6-107">Hvis sjekken samsvarer med en sjekk i listen, betales sjekken av banken.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="b3ac6-108">Hvis sjekken ikke samsvarer med en sjekk i listen, beholder banken sjekken til gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="b3ac6-109">Sikkerhetsnøkkel for positive lønnsfiler</span><span class="sxs-lookup"><span data-stu-id="b3ac6-109">Security for positive pay files</span></span>
<span data-ttu-id="b3ac6-110">Positive betalingsfiler kan inneholde sensitiv informasjon om betalingsmottakere og sjekkbeløp.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="b3ac6-111">Derfor må du sørge for at du bruker riktige sikkerhetstiltak fra tidspunktet som filene er generert, til de er mottatt av banken.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="b3ac6-112">Positive lønnsfiler blir lastet ned til plasseringen som er angitt i webleseren.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="b3ac6-113">Siden positive lønnsfiler kan inneholde sensitiv informasjon, er det viktig at bare autoriserte brukere har tilgang til å generere og vise denne informasjonen i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b3ac6-114">Bruk tabellen nedenfor til å hjelpe deg med å bestemme rettighetene som kreves.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3ac6-115">Oppgave</span><span class="sxs-lookup"><span data-stu-id="b3ac6-115">Task</span></span></th>
<th><span data-ttu-id="b3ac6-116">Rettighet</span><span class="sxs-lookup"><span data-stu-id="b3ac6-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3ac6-117">Generer positiv lønn filer fra listesiden <strong>Bankkontoer</strong> eller siden <strong>Bankkontoer</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="b3ac6-118"><strong>Vedlikehold informasjon om positiv bankbetaling</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="b3ac6-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3ac6-120">Generere positive betalingsfiler for flere juridiske enheter og bankkontoer fra siden <strong>Generer en positiv betalingsfil</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="b3ac6-121"><strong>Vedlikehold informasjon om positiv bankbetaling</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="b3ac6-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3ac6-123">Vis positive betalingsfiler på siden <strong>Sammendrag av positiv betalingsfil</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="b3ac6-124"><strong>Vis informasjon om positiv bankbetaling for flere juridiske enheter</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3ac6-125">Bereft en positiv bankbetalingsfil på siden <strong>Sammendrag av positiv betalingsfil</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="b3ac6-126"><strong>Bekreft positiv betalingsfil</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3ac6-127">Tilbakekall en positiv bankbetalingsfil på siden <strong>Sammendrag av positiv betalingsfil</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="b3ac6-128"><strong>Tilbakekall positiv betalingsfil</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="b3ac6-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="b3ac6-129">Definer et positivt betalingsformat</span><span class="sxs-lookup"><span data-stu-id="b3ac6-129">Set up a positive pay format</span></span>
<span data-ttu-id="b3ac6-130">Positive betalingsfiler opprettes ved hjelp av dataenheter.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="b3ac6-131">Før du kan generere en positiv betalingsfil, må du definere et transformasjonsinndataformat som skal brukes til å oversette informasjonen i et format som kan kommunisere med banken.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="b3ac6-132">På siden **Positivt betalingsformat** kan du opprette en filformat-ID og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="b3ac6-133">Transformasjonsinndataformatet må være av XML-typen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="b3ac6-134">Det bestemte formatet avhengiger av transformasjonsfilen du bruker.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="b3ac6-135">XSLT-eksempelfilen (Extensible Stylesheet Language Transformations) som er oppgitt, bruker formatet **XML-Element**.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="b3ac6-136">Bruk handlingen **Last opp fil som brukes for transformasjon** til å angi plasseringen til transformeringsfilen for formatet som banken krever.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="b3ac6-137">Eksempel: XSLT-fil for positiv betalingsfil</span><span class="sxs-lookup"><span data-stu-id="b3ac6-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="b3ac6-138">Tilordne det positive betalingsformatet til en bankkonto</span><span class="sxs-lookup"><span data-stu-id="b3ac6-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="b3ac6-139">For hver bankkonto du vil generere informasjon om positiv betaling for, må du tilordne det positive betalingsformatet som ble angitt i forrige del.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="b3ac6-140">På **Bankkontoer**-siden velger du det positive lønnsformatet som samsvarer med bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="b3ac6-141">I feltet **Startdato for positiv betaling** angir du den første datoen for generering av positive betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="b3ac6-142">Det er viktig at du angir en dato i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="b3ac6-143">Ellers vil den første positive betalingsfilen du genererer, inkludere alle kontrollene som noen gang har blitt opprettet for denne bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="b3ac6-144">Tilordne en nummerserie for positive betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="b3ac6-145">Hver positiv lønnsfil må ha et unikt nummer.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="b3ac6-146">Bruk kategorien **Nummerserier** på siden **Parametere for kontant- og bankbehandling** til å opprette en nummerserie for positive betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="b3ac6-147">Generere en positiv betalingsfil for én bankkonto</span><span class="sxs-lookup"><span data-stu-id="b3ac6-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="b3ac6-148">Du kan generere en positiv betalingsfil for én juridisk enhet og én bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="b3ac6-149">For informasjon om hvordan du genererer positive betalingsfiler for flere juridiske enheter og bankkontoer samtidig, kan du se neste del.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="b3ac6-150">Hvis du vil generere en positiv betalingsfilen for en juridisk enhet og én bankkonto, kan du åpne dialogboksen **Generer en positiv betalingsfil** fra **Bankkontoer**-siden.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="b3ac6-151">I **Frist**-feltet angir du den siste sjekkdatoen som skal tas med i den positive betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="b3ac6-152">Alle sjekker som ikke har blitt tatt med i en positiv betalingsfil til og med denne sjekkdatoen, tas med i filen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="b3ac6-153">Generere en positiv betalingsfil for flere bankkontoer</span><span class="sxs-lookup"><span data-stu-id="b3ac6-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="b3ac6-154">Hvis du vil generere en positiv betalingsfiler for flere bankkontoer, bruker du den periodiske oppgaven **Generer en positiv betalingsfil**.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="b3ac6-155">Velg det positive betalingsformatet for filen, og angi om du vil generere filen for alle juridiske enheter eller for en valgt juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="b3ac6-156">Du kan også generere den positive betalingsfilen for alle bankkontoer som bruker det angitte positive betalingsformatet eller for en valgt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="b3ac6-157">I **Frist**-feltet angir du den siste sjekkdatoen som skal tas med i den positive betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="b3ac6-158">Alle sjekker som ikke har blitt tatt med i en positiv betalingsfil til og med denne sjekkdatoen, tas med i filen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="b3ac6-159">Vise resultatene av genereringen av den positive betalingsfilen</span><span class="sxs-lookup"><span data-stu-id="b3ac6-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="b3ac6-160">Når den positive betalingsfilen er opprettet, kan du vise resultatene på siden **Sammendrag av positiv betalingsfil** side.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="b3ac6-161">Hvis du vil vise detaljer om de individuelle kontrollene, kan du bruke siden **Detaljer for positiv betalingsfil**.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="b3ac6-162">Bekreft en positiv betalingsfil</span><span class="sxs-lookup"><span data-stu-id="b3ac6-162">Confirm a positive pay file</span></span>
<span data-ttu-id="b3ac6-163">Når kontrollene som er oppført i en positiv lønnsfilen er betalt, får du et bekreftelsesnummer fra banken.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="b3ac6-164">Du kan deretter bekrefte den positive betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="b3ac6-165">På siden **Sammendrag av positiv betalingsfil** velger du en positiv betalingsfil som har statusen **Opprettet**, og deretter velger du handlingen **Angi bekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="b3ac6-166">Når du bekrefter en positiv betalingsfil, registreres bekreftelsesnummeret du mottok fra banken.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="b3ac6-167">Tilbakekalle en positiv betalingsfil</span><span class="sxs-lookup"><span data-stu-id="b3ac6-167">Recall a positive pay file</span></span>
<span data-ttu-id="b3ac6-168">Hvis du må endre en positiv betalingsfil, kan du tilbakekalle den.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="b3ac6-169">På siden **Sammendrag av positiv betalingsfil** velger du en positiv betalingsfil som har statusen **Opprettet**, og deretter velger du handlingen **Tilbakekall**.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="b3ac6-170">For hver kontroll i den positive betalingsfilen tilbakestilles feltet som angir om kontrollen er inkludert i en positiv betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="b3ac6-171">Du kan deretter opprette en ny positiv betalingsfil med kontrollen som ble tilbakekalt.</span><span class="sxs-lookup"><span data-stu-id="b3ac6-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



