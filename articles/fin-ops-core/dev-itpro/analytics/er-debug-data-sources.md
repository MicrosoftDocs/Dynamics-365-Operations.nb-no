---
title: Feilsøke datakilder for et utført ER-format for å analysere dataflyt og transformasjon
description: Dette emnet beskriver hvordan du kan feilsøker datakildene i et utført ER-format for bedre forståelse av den konfigurerte dataflyten og transformasjonen.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5b51c4beac0ddf1e2b53fe300e10c0f608e5d1e1
ms.sourcegitcommit: 153bb33722c02501bf7bcfd56ac887602d5dfbd3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2020
ms.locfileid: "3318672"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="2257c-103">Feilsøke datakilder for et utført ER-format for å analysere dataflyt og transformasjon</span><span class="sxs-lookup"><span data-stu-id="2257c-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="2257c-104">Når du [konfigurerer](tasks/er-format-configuration-2016-11.md) en ER-løsning (elektronisk rapportering) for å generere utgående dokumenter, definerer du metoden som brukes til å hente data ut av applikasjonen, og angir den i utdataene som genereres.</span><span class="sxs-lookup"><span data-stu-id="2257c-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="2257c-105">For å få livssyklusstøtten for ER-løsningen mer effektiv, bør løsningen bestå av en ER [datamodell](general-electronic-reporting.md#DataModelComponent) og kompentene for [tilordning](general-electronic-reporting.md#ModelMappingComponent) og også et ER-[format](general-electronic-reporting.md#FormatComponentOutbound) og de tilhørende tilordningskomponentene, slik at modelltilordningen er programspesifikk mens andre komponenter forblir programagnostiske.</span><span class="sxs-lookup"><span data-stu-id="2257c-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="2257c-106">Derfor kan flere ER-komponenter [påvirke](general-electronic-reporting.md#FormatComponentOutbound) prosessen med å registrere data i de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="2257c-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="2257c-107">Noen ganger vil dataene i den genererte utskriften se annerledes ut enn de samme dataene i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="2257c-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="2257c-108">I disse tilfellene vil du avgjøre hvilken ER-komponent som er ansvarlig for datatransformasjonen.</span><span class="sxs-lookup"><span data-stu-id="2257c-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="2257c-109">Feilsøkerfunksjonen for ER-datakilde reduserer tiden og kostnadene som er involvert i denne undersøkelsen betydelig.</span><span class="sxs-lookup"><span data-stu-id="2257c-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="2257c-110">Du kan avbryte utførelsen av et ER-format og åpne feilsøkergrensesnittet for datakilden.</span><span class="sxs-lookup"><span data-stu-id="2257c-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="2257c-111">Der kan du bla gjennom de tilgjengelige datakildene og velge en enkelt datakilde for utførelse.</span><span class="sxs-lookup"><span data-stu-id="2257c-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="2257c-112">Denne manuelle utførelsen simulerer utførelsen av datakilden under den virkelige kjøringen av et ER-format.</span><span class="sxs-lookup"><span data-stu-id="2257c-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="2257c-113">Resultatet vises på en side der du kan analysere de mottatte dataene.</span><span class="sxs-lookup"><span data-stu-id="2257c-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="2257c-114">Hvis du vil aktivere funksjonen for feilsøking av datakilde, setter du alternativet **Aktiver datafeilsøking ved formatkjøring** til **Ja** i ER-brukerparameterne.</span><span class="sxs-lookup"><span data-stu-id="2257c-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="2257c-115">Du kan deretter starte feilsøking av datakilde mens du kjører et ER-format for å generere utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="2257c-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="2257c-116">Du kan også bruke alternativet for **start feilsøking** for å starte feilsøking av datakilde for et ER-format som er konfigurert i [ER-operasjonsutforming](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="2257c-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="2257c-117">Dette emnet inneholder retningslinjer for hvordan du starter feilsøking av datakilder for utførte ER-formater.</span><span class="sxs-lookup"><span data-stu-id="2257c-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="2257c-118">Den forklarer hvordan informasjonen kan hjelpe deg med å forstå dataflyten og datatransformeringene.</span><span class="sxs-lookup"><span data-stu-id="2257c-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="2257c-119">Eksemplene i dette emnet bruker forretningsprosessen for behandling av leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="2257c-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="2257c-120">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="2257c-120">Limitations</span></span>

<span data-ttu-id="2257c-121">Du kan bruke feilsøkingsprogrammet for datakilde til å få tilgang til data i datakilder som brukes i ER-formater som kjøres for å generere utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="2257c-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="2257c-122">Den kan ikke brukes til å feilsøke datakilder med ER-formater som er utformet for å analysere innkommende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="2257c-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="2257c-123">Følgende innstillinger for ER-formater er for øyeblikket ikke tilgjengelige for datakildefeilsøking:</span><span class="sxs-lookup"><span data-stu-id="2257c-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="2257c-124">Formattransformasjoner</span><span class="sxs-lookup"><span data-stu-id="2257c-124">Format transformations</span></span>
- <span data-ttu-id="2257c-125">Formatere og tilordne valideringsregler</span><span class="sxs-lookup"><span data-stu-id="2257c-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="2257c-126">Aktivere uttrykk</span><span class="sxs-lookup"><span data-stu-id="2257c-126">Enabling expressions</span></span>
- <span data-ttu-id="2257c-127">Detaljer om datainnsamling i minnet</span><span class="sxs-lookup"><span data-stu-id="2257c-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2257c-128">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="2257c-128">Prerequisites</span></span>

- <span data-ttu-id="2257c-129">Hvis du vil fullføre eksemplene i dette emnet, må du ha tilgang til følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="2257c-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="2257c-130">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="2257c-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="2257c-131">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="2257c-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="2257c-132">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="2257c-132">System administrator</span></span>

- <span data-ttu-id="2257c-133">Firmaet må settes til **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="2257c-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="2257c-134">Følg trinnene i [tillegg 1](#appendix1) i dette emnet for å laste ned komponentene i Microsoft ER-løsningen som kreves for å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="2257c-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="2257c-135">Følg trinnene i [tillegg 2](#appendix2) i dette emnet for å klargjøre leverandører for leverandørbetalingsbehandling ved hjelp av ER-løsningen du vil laste ned.</span><span class="sxs-lookup"><span data-stu-id="2257c-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="2257c-136">Behandle en leverandørbetaling for å hente en betalingsfil</span><span class="sxs-lookup"><span data-stu-id="2257c-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="2257c-137">Følg trinnene i [tillegg 3](#appendix3) i dette emnet for å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="2257c-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Leverandørbetalingsbehandling pågår](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="2257c-139">Last ned og lagre zip-filen på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="2257c-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="2257c-140">Pakk ut betalingsfilen **ISO20022 Credit transfer.xml** fra zip-filen.</span><span class="sxs-lookup"><span data-stu-id="2257c-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="2257c-141">Åpne den utpakkede betalingsfilen ved hjelp av visningsprogrammet for XML-filen.</span><span class="sxs-lookup"><span data-stu-id="2257c-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="2257c-142">Betalingsfilen for det internasjonale bankkontonummeret (IBAN) til leverandørens bankkonto inneholder ikke mellomrom.</span><span class="sxs-lookup"><span data-stu-id="2257c-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="2257c-143">Derfor er det forskjellig fra verdien som ble [angitt](#enteredIBANcode) på siden **Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="2257c-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN-kode uten mellomrom](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="2257c-145">Du kan bruke feilsøkingsprogrammet for ER-datakilde til å lære hvilken komponent i ER-løsningen som brukes til å avkorte mellomrom i IBAN-koden.</span><span class="sxs-lookup"><span data-stu-id="2257c-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="2257c-146">Aktivere feilsøking for datakilde</span><span class="sxs-lookup"><span data-stu-id="2257c-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="2257c-147">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="2257c-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2257c-148">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="2257c-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="2257c-149">Sett **Aktiver datafeilsøking ved formatkjøring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2257c-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2257c-150">Denne parameteren er brukerspesifikk og selskapsspesifikk.</span><span class="sxs-lookup"><span data-stu-id="2257c-150">This parameter is user-specific and company-specific.</span></span>

    ![Dialogboksen Brukerparametere](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="2257c-152">Behandle en leverandørbetaling for feilsøking</span><span class="sxs-lookup"><span data-stu-id="2257c-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="2257c-153">Følg trinnene i [tillegg 3](#appendix3) i dette emnet for å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="2257c-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="2257c-154">I meldingsboksen velger **Ja** for å bekrefte at du vil avbryte leverandørbetalingsbehandling og i stedet starte datakildefeilsøking på siden for **feilsøke datakilder**.</span><span class="sxs-lookup"><span data-stu-id="2257c-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Meldingsboks for bekreftelse](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="2257c-156">Feilsøke datakilder som brukes i betalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="2257c-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="2257c-157">Feilsøke modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="2257c-157">Debug the model mapping</span></span>

1. <span data-ttu-id="2257c-158">På siden for **feilsøk datakilder** i handlingsruten velger du **Modelltilordning** for å starte feilsøking fra denne ER-komponenten.</span><span class="sxs-lookup"><span data-stu-id="2257c-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="2257c-159">I datakilderuten til venstre velger du datakilden **\$notSentTransactions**, og velg deretter **Les alle poster**.</span><span class="sxs-lookup"><span data-stu-id="2257c-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="2257c-160">Du kan velge **Les 1 post**, **Les 10 poster**, **Les 100 poster** eller **Les alle poster** for å tvinge det aktuelle antallet poster til å leses fra den valgte datakilden.</span><span class="sxs-lookup"><span data-stu-id="2257c-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="2257c-161">På denne måten kan du simulere tilgang til datakilden fra det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="2257c-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="2257c-162">Deretter velger du **Vis alle** i dataruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="2257c-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="2257c-163">Du kan se at den valgte datakilden for typen **Postliste** inneholder én enkelt post.</span><span class="sxs-lookup"><span data-stu-id="2257c-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="2257c-164">Utvid datakilden **\$notSentTransactions**, og velg den nestede **vendBankAccountInTransactionCompany()**-metoden.</span><span class="sxs-lookup"><span data-stu-id="2257c-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="2257c-165">Utvid **vendBankAccountInTransactionCompany()**-metoden, og velg det nestede **IBAN**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2257c-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="2257c-166">Velg **Hent verdi**.</span><span class="sxs-lookup"><span data-stu-id="2257c-166">Select **Get value**.</span></span>

    <span data-ttu-id="2257c-167">Du kan velge **Hent verdi** for å fremtvinge verdien av et valgt felt i den valgte datakilden som skal leses.</span><span class="sxs-lookup"><span data-stu-id="2257c-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="2257c-168">På denne måten kan du simulere tilgang til dette feltet fra det kjørende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="2257c-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="2257c-169">Velg **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="2257c-169">Select **Expand all**.</span></span>

    ![Verdien til IBAN-feltet i modelltilordningen](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="2257c-171">Som du kan se, er ikke modelltilordningen ansvarlig for de avkortede områdene, fordi IBAN-koden som den returnerer for leverandørbankkontoen, omfatter mellomrom.</span><span class="sxs-lookup"><span data-stu-id="2257c-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="2257c-172">Derfor må du fortsette feilsøkingen av datakilder.</span><span class="sxs-lookup"><span data-stu-id="2257c-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="2257c-173">Feilsøke formattilordningen</span><span class="sxs-lookup"><span data-stu-id="2257c-173">Debug the format mapping</span></span>

1. <span data-ttu-id="2257c-174">På siden for **feilsøk datakilder** i handlingsruten velger du **Formattilordning** for å fortsette feilsøkingen fra denne ER-komponenten.</span><span class="sxs-lookup"><span data-stu-id="2257c-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="2257c-175">Velg datakilden **\$PaymentByDebtor**, og velg deretter **Les alle poster**.</span><span class="sxs-lookup"><span data-stu-id="2257c-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="2257c-176">Utvid **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="2257c-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="2257c-177">Utvid **\$PaymentByDebtor.Lines**, og velg deretter **Les alle poster**.</span><span class="sxs-lookup"><span data-stu-id="2257c-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="2257c-178">Utvid **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="2257c-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="2257c-179">Utvid **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, og velg deretter **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="2257c-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="2257c-180">Velg **Hent verdi**.</span><span class="sxs-lookup"><span data-stu-id="2257c-180">Select **Get value**.</span></span>
8. <span data-ttu-id="2257c-181">Velg **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="2257c-181">Select **Expand all**.</span></span>

    ![Verdien til IBAN-feltet i formattilordningen](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="2257c-183">Som du kan se, er ikke datakildene i formattilordningen ansvarlig for de avkortede områdene, fordi IBAN-koden som den returnerer for leverandørbankkontoen, omfatter mellomrom.</span><span class="sxs-lookup"><span data-stu-id="2257c-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="2257c-184">Derfor må du fortsette feilsøkingen av datakilder.</span><span class="sxs-lookup"><span data-stu-id="2257c-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="2257c-185">Feilsøke formatet</span><span class="sxs-lookup"><span data-stu-id="2257c-185">Debug the format</span></span>

1. <span data-ttu-id="2257c-186">På siden for **feilsøk datakilder** i handlingsruten velger du **Format** for å fortsette feilsøkingen fra denne ER-komponenten.</span><span class="sxs-lookup"><span data-stu-id="2257c-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="2257c-187">Utvid formatelementene for å velge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, og velg deretter **Les alle poster**.</span><span class="sxs-lookup"><span data-stu-id="2257c-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="2257c-188">Utvid formatelementene for å velge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, og velg deretter **Les alle poster**.</span><span class="sxs-lookup"><span data-stu-id="2257c-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="2257c-189">Utvid formatelementene for å velge **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, og velg deretter **Hent verdi**.</span><span class="sxs-lookup"><span data-stu-id="2257c-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="2257c-190">Velg **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="2257c-190">Select **Expand all**.</span></span>

    ![Verdien til IBAN-feltet i formatet](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="2257c-192">Som du kan se, er ikke formatbinding ansvarlig for de avkortede områdene, fordi IBAN-koden som den returnerer for leverandørbankkontoen, omfatter mellomrom.</span><span class="sxs-lookup"><span data-stu-id="2257c-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="2257c-193">Derfor er **BankIBAN**-elementet konfigurert til å bruke en formattransformering som avkorter mellomrom.</span><span class="sxs-lookup"><span data-stu-id="2257c-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="2257c-194">Lukk feilsøkingsprogrammet for datakilde.</span><span class="sxs-lookup"><span data-stu-id="2257c-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="2257c-195">Se gjennom formattransformasjoner</span><span class="sxs-lookup"><span data-stu-id="2257c-195">Review the format transformations</span></span>

1. <span data-ttu-id="2257c-196">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="2257c-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2257c-197">På siden **Konfigurasjoner** velger du **Betalingsmodell** \> **ISO20022-kredittoverføring**.</span><span class="sxs-lookup"><span data-stu-id="2257c-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="2257c-198">Velg **Utforming**, og utvid deretter elementene for å velge **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="2257c-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN-elementet på Formatutforming-siden](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="2257c-200">Som du kan se, er **BankIBAN**-elementet konfigurert til å bruke transformeringen **fjern ikke alfanumerisk**.</span><span class="sxs-lookup"><span data-stu-id="2257c-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="2257c-201">Velg kategorien **Transformasjoner**.</span><span class="sxs-lookup"><span data-stu-id="2257c-201">Select the **Transformations** tab.</span></span>

    ![Kategorien Transformasjoner for BankIBAN-elementet](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="2257c-203">Som du kan se, er transformeringen **fjern ikke-alfanumerisk** konfigurert til å bruke et uttrykk som avkorter mellomrom fra tekststrengen som er angitt.</span><span class="sxs-lookup"><span data-stu-id="2257c-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="2257c-204">Start feilsøking i operasjonsutforming</span><span class="sxs-lookup"><span data-stu-id="2257c-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="2257c-205">Når du konfigurerer en kladdeversjon av ER-formatet som kan kjøres direkte fra operasjonsutformingen, får du tilgang til datakildefeilsøkeren ved å velge **Start feilsøking** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2257c-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Knappen Start feilsøking på siden Formatutforming](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="2257c-207">Formattilordning og formatkomponentene i ER-formatet som redigeres, er tilgjengelige for feilsøking.</span><span class="sxs-lookup"><span data-stu-id="2257c-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="2257c-208">Start feilsøking i Modelltilordningsutforming</span><span class="sxs-lookup"><span data-stu-id="2257c-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="2257c-209">Når du konfigurerer en ER-modelltilordning som kan kjøres direkte fra siden **Modelltilordning**, får du tilgang til datakildefeilsøkeren ved å velge **Start feilsøking** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2257c-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Knappen Start feilsøking på siden Modellkartleggingsutforming](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="2257c-211">Modelltilordningskomponenten for ER-tilordningen som redigeres, er tilgjengelig for feilsøking.</span><span class="sxs-lookup"><span data-stu-id="2257c-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="2257c-212">Tillegg 1: Få en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="2257c-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="2257c-213">Laste ned en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="2257c-213">Download an ER solution</span></span>

<span data-ttu-id="2257c-214">Hvis du vil bruke en ER-løsning for å generere en elektronisk betalingsfil for en leverandørbetaling som er behandlet, kan du [laste ned](download-electronic-reporting-configuration-lcs.md) det ER-betalingsformatet **ISO20022-kredittoverføring** som er tilgjengelig fra det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) eller fra det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="2257c-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![Importere ER-betalingsformatet på Konfigurasjonsrepositorium-siden](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="2257c-216">I tillegg til det valgte ER-formatet må følgende [konfigurasjoner](general-electronic-reporting.md#Configuration) importeres automatisk til Microsoft Dynamics 365 Finance-forekomsten som en del av ER-løsningen **ISO20022-kredittoverføring**:</span><span class="sxs-lookup"><span data-stu-id="2257c-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="2257c-217">**Betalingsmodell** [ER-datamodellkonfigurasjon](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="2257c-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="2257c-218">**ISO20022-kredittoverføring** [ER-formatkonfigurasjon](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="2257c-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="2257c-219">**Betalingsmodelltilordning 1611** [ER-modelltilordningskonfigurasjon](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="2257c-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="2257c-220">**Betalingsmodelltilordning til mål ISO20022** – ER-modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="2257c-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="2257c-221">Du finner disse konfigurasjonene på siden **Konfigurasjoner** i ER-rammeverket (**Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**).</span><span class="sxs-lookup"><span data-stu-id="2257c-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Konfigurasjoner er importert på Konfigurasjoner-siden](./media/er-data-debugger-configurations.png)

<span data-ttu-id="2257c-223">Hvis noen av de tidligere angitte konfigurasjonene mangler i konfigurasjonstreet, må du laste dem ned manuelt fra det delte LCS-aktivabibliotek på samme måte som du har lastet ned ER-betalingsformatet **ISO20022-kredittoverføring**.</span><span class="sxs-lookup"><span data-stu-id="2257c-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="2257c-224">Analysere den nedlastede ER-løsningen</span><span class="sxs-lookup"><span data-stu-id="2257c-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="2257c-225">Se gjennom modelltilordningen</span><span class="sxs-lookup"><span data-stu-id="2257c-225">Review the model mapping</span></span>

1. <span data-ttu-id="2257c-226">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="2257c-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2257c-227">Velg **Betalingsmodell** \> **Betalingsmodelltilordning 1611**.</span><span class="sxs-lookup"><span data-stu-id="2257c-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="2257c-228">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="2257c-228">Select **Designer**.</span></span>
4. <span data-ttu-id="2257c-229">Velg tilordningsposten **Betalingsmodelltilordning ISO20022-kredittoverføring**.</span><span class="sxs-lookup"><span data-stu-id="2257c-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="2257c-230">Velg **Utforming**, og gå deretter gjennom modelltilordningen som åpnes.</span><span class="sxs-lookup"><span data-stu-id="2257c-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="2257c-231">Legg merke til at **Betalinger**-feltet for datamodellen er bundet til **\$notSentTransactions**-datakilden som returnerer listen over leverandørbetalingslinjer som behandles.</span><span class="sxs-lookup"><span data-stu-id="2257c-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Betalinger-feltet på siden for modelltilordningsutforming](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="2257c-233">Se gjennom formattilordningen</span><span class="sxs-lookup"><span data-stu-id="2257c-233">Review the format mapping</span></span>

1. <span data-ttu-id="2257c-234">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="2257c-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2257c-235">Velg **Betalingsmodell** \> **ISO20022-kredittoverføring**.</span><span class="sxs-lookup"><span data-stu-id="2257c-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="2257c-236">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="2257c-236">Select **Designer**.</span></span>
4. <span data-ttu-id="2257c-237">I kategorien **Tilordning** kontrollerer du formattilordningen som åpnes.</span><span class="sxs-lookup"><span data-stu-id="2257c-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="2257c-238">Legg merke til at **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**-elementet i **ISO20022CTReports** \> **XMLHeader**-filen er bundet til datakilden **\$PaymentByDebtor**, som er konfigurert til å gruppere poster i datamodellens **Betalinger**-felt.</span><span class="sxs-lookup"><span data-stu-id="2257c-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf-elementet på Formatutforming-siden](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="2257c-240">Se gjennom format</span><span class="sxs-lookup"><span data-stu-id="2257c-240">Review the format</span></span>

1. <span data-ttu-id="2257c-241">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="2257c-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="2257c-242">Velg **Betalingsmodell** \> **ISO20022-kredittoverføring**.</span><span class="sxs-lookup"><span data-stu-id="2257c-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="2257c-243">Velg **Utforming**, og gå deretter gjennom formatet som åpnes.</span><span class="sxs-lookup"><span data-stu-id="2257c-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="2257c-244">Merk at formatelementet under **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** er konfigurert til å angi IBAN-koden for leverandørkontoen i betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="2257c-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN-elementet på Formatutforming-siden](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="2257c-246">Tillegg 2: Konfigurere leverandører</span><span class="sxs-lookup"><span data-stu-id="2257c-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="2257c-247">Endre en leverandøregenskap</span><span class="sxs-lookup"><span data-stu-id="2257c-247">Modify a vendor property</span></span>

1. <span data-ttu-id="2257c-248">Gå til **Leverandører** \> **Leverandører** \> **Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="2257c-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="2257c-249">Velg leverandør **DE-01002**, og gå deretter til handlingsruten, kategorien **Leverandør** i gruppen **Oppsett**, og velg **Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="2257c-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="2257c-250">I hurtigkategorien **Identifikasjon** i feltet **IBAN** <a name="enteredIBANcode"></a>angir du **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="2257c-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="2257c-251">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2257c-251">Select **Save**.</span></span>

![IBAN-feltet er satt siden Leverandørbankkontoer](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="2257c-253">Definere en betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="2257c-253">Set up a method of payment</span></span>

1. <span data-ttu-id="2257c-254">Gå til **Leverandører** \> **Betalingsoppsett** \> **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="2257c-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="2257c-255">Velg betalingsmåten **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="2257c-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="2257c-256">I hurtigfanen **Filformater** i delen **Filformater** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2257c-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="2257c-257">I feltet **Eksportformatkonfigurasjon** velger du ER-formatet **ISO20022-kredittoverføring**.</span><span class="sxs-lookup"><span data-stu-id="2257c-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="2257c-258">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2257c-258">Select **Save**.</span></span>

![Filformatinnstillingene på siden for Betalingsmåter](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="2257c-260">Legge til en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="2257c-260">Add a vendor payment</span></span>

1. <span data-ttu-id="2257c-261">Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="2257c-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="2257c-262">Legg til ny betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="2257c-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="2257c-263">Velg **Linjer**, og legg til en ny betalingslinje.</span><span class="sxs-lookup"><span data-stu-id="2257c-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="2257c-264">I feltet **Konto** velger du leverandøren **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="2257c-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="2257c-265">Angi en verdi i **Debet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2257c-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="2257c-266">Velg **SEPA CT** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="2257c-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="2257c-267">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2257c-267">Select **Save**.</span></span>

![Leverandørbetaling er lagt til på siden Leverandør](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="2257c-269">Tillegg 3: Behandle en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="2257c-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="2257c-270">Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="2257c-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="2257c-271">På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du opprettet tidligere, og deretter velger du **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="2257c-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="2257c-272">Velg betalingslinjen, og velg deretter **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="2257c-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="2257c-273">Velg **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="2257c-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="2257c-274">Velg **SEPA CT** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="2257c-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="2257c-275">Velg **DEMF OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="2257c-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="2257c-276">Velg **OK** i dialogboksen **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="2257c-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="2257c-277">I dialogboksen **Parametere for elektronisk rapport** velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="2257c-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>