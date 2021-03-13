---
title: ER Tilordne komponenter i det opprettede formatet til datamodellelementer (november 2016)
description: Dette emnet beskriver hvordan du tilordner datamodellelementer til komponenter i den opprettede ER-konfigurasjonen (Elektronisk rapportering).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 043c66cf3345678aa7750ef50323700384579299
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093779"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="01801-103">ER Tilordne komponenter i det opprettede formatet til datamodellelementer (november 2016)</span><span class="sxs-lookup"><span data-stu-id="01801-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01801-104">Følgende prosedyre viser hvordan en bruker med rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne datamodellelementer til komponenter i den opprettede konfigurasjonen for elektronisk rapportering (ER), som definerer et elektronisk dokumentformat for forretningsområdet for betalinger.</span><span class="sxs-lookup"><span data-stu-id="01801-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="01801-105">Dette formatet brukes senere til å generere elektroniske dokumenter for behandling av betalinger.</span><span class="sxs-lookup"><span data-stu-id="01801-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="01801-106">I dette eksemplet skal du opprette en formatkonfigurasjon for eksempelfirmaet "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="01801-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="01801-107">Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles for alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="01801-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="01801-108">For å fullføre disse trinnene må du først fullføre trinnene i oppgaveveiledningen "Opprette en formatkonfigurasjon".</span><span class="sxs-lookup"><span data-stu-id="01801-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="01801-109">Velge en formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="01801-109">Select a format configuration</span></span>
1. <span data-ttu-id="01801-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="01801-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="01801-111">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="01801-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="01801-112">Vis Betalinger (forenklet model) i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="01801-113">Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="01801-114">Klikk på Utforming.</span><span class="sxs-lookup"><span data-stu-id="01801-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="01801-115">Tilordne formatkomponenter til datamodellelementer</span><span class="sxs-lookup"><span data-stu-id="01801-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="01801-116">Klikk på Vis/skjul.</span><span class="sxs-lookup"><span data-stu-id="01801-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="01801-117">Klikk på fanen Tilordning.</span><span class="sxs-lookup"><span data-stu-id="01801-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="01801-118">Utvid noden 'model' i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="01801-119">Velg Xml\Melding\ProcessingDate\DateTime i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="01801-120">Velg modell\ProcessingDateTime i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="01801-121">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-121">Click Bind.</span></span>
7. <span data-ttu-id="01801-122">Velg Xml\Melding\MessageId\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="01801-123">Velg modell\MessageIdentification i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="01801-124">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-124">Click Bind.</span></span>
10. <span data-ttu-id="01801-125">Utvid modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="01801-126">Velg Xml\Melding\Betalinger\Vare\Beløp\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="01801-127">Velg modell\Betalinger\InstructedAmount i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="01801-128">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-128">Click Bind.</span></span>
14. <span data-ttu-id="01801-129">Velg Xml\Melding\Betalinger\Vare\TransDate\DateTime i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="01801-130">Velg modell\Betalinger\TransactionDate i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="01801-131">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-131">Click Bind.</span></span>
17. <span data-ttu-id="01801-132">Velg Xml\Melding\Betalinger\Vare\Beskrivelse\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="01801-133">Velg modell\Betalinger\Beskrivelse i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="01801-134">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-134">Click Bind.</span></span>
20. <span data-ttu-id="01801-135">Velg Xml\Melding\Betalinger\Vare\Beløp\Valuta\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="01801-136">Velg model\Payments\Currency i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="01801-137">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-137">Click Bind.</span></span>
23. <span data-ttu-id="01801-138">Velg Xml\Melding\Betalinger\Vare\Id i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="01801-139">Velg modell\Betalinger\End2EndID i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="01801-140">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-140">Click Bind.</span></span>
26. <span data-ttu-id="01801-141">Utvid modell\Betalinger\Kreditor i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="01801-142">Utvid modell\Betalinger\Kreditor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="01801-143">Utvid modell\Betalinger\Kreditor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="01801-144">Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="01801-145">I treet velger du modell\Betalinger\Kreditor\Navn.</span><span class="sxs-lookup"><span data-stu-id="01801-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="01801-146">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-146">Click Bind.</span></span>
32. <span data-ttu-id="01801-147">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\RoutingNumber\String i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="01801-148">I treet velger du modell\Betalinger\Kreditor\Agent\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="01801-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="01801-149">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-149">Click Bind.</span></span>
35. <span data-ttu-id="01801-150">Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\AccountNumber\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="01801-151">I treet velger du modell\Betalinger\Kreditor\Konto\Nummer.</span><span class="sxs-lookup"><span data-stu-id="01801-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="01801-152">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-152">Click Bind.</span></span>
38. <span data-ttu-id="01801-153">Velg Xml\Melding\Betalinger\Vare\Betaler\Navn\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="01801-154">Utvid modell\Betalinger\Debitor i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="01801-155">Utvid modell\Betalinger\Debitor\Konto i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="01801-156">Utvid modell\Betalinger\Debitor\Agent i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="01801-157">I treet velger du modell\Betalinger\Debitor\Navn.</span><span class="sxs-lookup"><span data-stu-id="01801-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="01801-158">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-158">Click Bind.</span></span>
44. <span data-ttu-id="01801-159">Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\RoutingNumber\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="01801-160">Velg modell\Betalinger\Debitor\Agent\RoutingNumber i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="01801-161">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-161">Click Bind.</span></span>
47. <span data-ttu-id="01801-162">Velg Xml\Melding\Betalinger\Vare\Betaler\Bank\AccountNumber\Streng i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="01801-163">I treet velger du modell\Betalinger\Debitor\Konto\Nummer.</span><span class="sxs-lookup"><span data-stu-id="01801-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="01801-164">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-164">Click Bind.</span></span>
50. <span data-ttu-id="01801-165">Velg Xml\Melding\Betalinger\Vare i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="01801-166">Velg modell\Betalinger i treet.</span><span class="sxs-lookup"><span data-stu-id="01801-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="01801-167">Klikk på Bind.</span><span class="sxs-lookup"><span data-stu-id="01801-167">Click Bind.</span></span>
53. <span data-ttu-id="01801-168">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="01801-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="01801-169">Validere formattilordning</span><span class="sxs-lookup"><span data-stu-id="01801-169">Validate format mapping</span></span>
1. <span data-ttu-id="01801-170">Klikk på Valider.</span><span class="sxs-lookup"><span data-stu-id="01801-170">Click Validate.</span></span>
    * <span data-ttu-id="01801-171">Valider den nye tilordningen for å sikre at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="01801-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="01801-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="01801-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="01801-173">Endre status for gjeldende versjon av formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="01801-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="01801-174">I de neste trinnene endrer du statusen for formatkonfigurasjonen fra Utkast til Fullført for å gjøre den tilgjengelig for generering av betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="01801-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="01801-175">Klikk på Endre status.</span><span class="sxs-lookup"><span data-stu-id="01801-175">Click Change status.</span></span>
2. <span data-ttu-id="01801-176">Klikk på Fullført.</span><span class="sxs-lookup"><span data-stu-id="01801-176">Click Complete.</span></span>
3. <span data-ttu-id="01801-177">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="01801-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="01801-178">For eksempel versjon 1.</span><span class="sxs-lookup"><span data-stu-id="01801-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="01801-179">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="01801-179">Click OK.</span></span>
5. <span data-ttu-id="01801-180">Velg den fullførte versjonen av den gjeldende konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="01801-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="01801-181">Legg merke til at konfigurasjonen er lagret som fullført versjon 1.1. Dette er versjon 1 av formatet, som er basert på versjon 1 av datamodellen.</span><span class="sxs-lookup"><span data-stu-id="01801-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="01801-182">Definere gyldighetsdato for fullført versjon av format</span><span class="sxs-lookup"><span data-stu-id="01801-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="01801-183">Du kan konfigurere hver formatversjon som tilgjengelig for bruk fra en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="01801-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="01801-184">Når mer enn én formatversjon er aktiv på en bestemt dato, velges det nyeste formatet (basert på versjonsnummeret) for bruk.</span><span class="sxs-lookup"><span data-stu-id="01801-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="01801-185">Datoverdien for økten brukes for valg av riktig versjon.</span><span class="sxs-lookup"><span data-stu-id="01801-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="01801-186">Begrense tilgang til formatet som er opprettet fra firmaer</span><span class="sxs-lookup"><span data-stu-id="01801-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="01801-187">Utvid delen ISO-land-/områdekoder.</span><span class="sxs-lookup"><span data-stu-id="01801-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="01801-188">Hver formattilgang kan begrenses ved å identifisere bestemte land/regioner der et format er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="01801-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="01801-189">Når listen over land/områder for et bestemt format er tomt, kan dette formatet brukes i et hvilket som helst firma.</span><span class="sxs-lookup"><span data-stu-id="01801-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="01801-190">Når det settes noen ISO-land-/områdekoder i denne listen over land/regioner, kan formatet bare brukes i firmaer hvis den primære adressen er i landet/regionen.</span><span class="sxs-lookup"><span data-stu-id="01801-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

