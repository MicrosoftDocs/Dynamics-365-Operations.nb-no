---
title: Utsetting
description: Dette emnet hjelper deg med å bygge en gjennomgang av utsetting i produksjonen i Microsoft Dynamics 365 for Finance and Operations.
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568402"
---
# <a name="subcontracting"></a><span data-ttu-id="9b757-103">Utsetting</span><span class="sxs-lookup"><span data-stu-id="9b757-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b757-104">Dette emnet hjelper deg med å bygge en gjennomgang av utsetting i produksjonen i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9b757-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9b757-105">Den første delen av dette emnet beskriver oppsettet av dataene.</span><span class="sxs-lookup"><span data-stu-id="9b757-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="9b757-106">Den andre delen leder deg gjennom trinnene i gjennomgangen.</span><span class="sxs-lookup"><span data-stu-id="9b757-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="9b757-107">Målpublikum</span><span class="sxs-lookup"><span data-stu-id="9b757-107">Target audience</span></span>

<span data-ttu-id="9b757-108">I dette emnet lærer du hvordan du konfigurerer bruk av utsetting i produksjon.</span><span class="sxs-lookup"><span data-stu-id="9b757-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="9b757-109">Du vil bruke eksisterende data i den juridiske enheten HQUS for å gjøre det grunnleggende oppsettet av en aktivitetsflyt for utsetting.</span><span class="sxs-lookup"><span data-stu-id="9b757-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="9b757-110">Demodataene i den juridiske enheten HQUS inneholder oppsettsparametere som har blitt forhåndsdefinerte for å støtte trinnene i gjennomgangen.</span><span class="sxs-lookup"><span data-stu-id="9b757-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="9b757-111">Selv om gjennomgangen håndterer viktige vanskelige punkt og utfordringer for forskjellige roller, kan den fullføres av systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="9b757-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="9b757-112">Demoscenario</span><span class="sxs-lookup"><span data-stu-id="9b757-112">Demo scenario</span></span>

<span data-ttu-id="9b757-113">I den juridiske enheten HQUS produseres avanserte høyttalere.</span><span class="sxs-lookup"><span data-stu-id="9b757-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="9b757-114">I løpet av produksjonsprosessen går høyttalerne gjennom følgende tre operasjoner.</span><span class="sxs-lookup"><span data-stu-id="9b757-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="9b757-115">**Før montering** – Høytalerkabinettet monteres.</span><span class="sxs-lookup"><span data-stu-id="9b757-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="9b757-116">Materialet for kabinettet plukkes på materialelageret før operasjonen startes.</span><span class="sxs-lookup"><span data-stu-id="9b757-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="9b757-117">**Lakkering** – Når høyttalerkabinettet er montert, må det lakkeres.</span><span class="sxs-lookup"><span data-stu-id="9b757-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="9b757-118">Denne operasjonen utføres av en leverandør (underleverandør).</span><span class="sxs-lookup"><span data-stu-id="9b757-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="9b757-119">Det pre-monterte høyttalerkabinettet sendes til lakkeringsunderleverandøren sammen med to materialer.</span><span class="sxs-lookup"><span data-stu-id="9b757-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="9b757-120">**Fullføring** – Etter et høyttalerkabinettet er blitt lakkert av underleverandøren, kommer det tilbake til den juridiske enheten HQUS, slik at monteringen av høyttaleren kan fullføres.</span><span class="sxs-lookup"><span data-stu-id="9b757-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="9b757-121">Illustrasjonen nedenfor viser de tre operasjonene og materialene som de bruker.</span><span class="sxs-lookup"><span data-stu-id="9b757-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Før-montering, lakkering og fullføring, og materialene de bruker](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="9b757-123">Installasjon</span><span class="sxs-lookup"><span data-stu-id="9b757-123">Setup</span></span>

<span data-ttu-id="9b757-124">Før du starter gjennomgangen, må du definere dataene.</span><span class="sxs-lookup"><span data-stu-id="9b757-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="9b757-125">Definer det ferdige produktet</span><span class="sxs-lookup"><span data-stu-id="9b757-125">Set up the finished product</span></span>

<span data-ttu-id="9b757-126">Denne prosedyren tar deg gjennom installasjonen av frigitt produkt D8100, "Lakkert kabinett".</span><span class="sxs-lookup"><span data-stu-id="9b757-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="9b757-127">Velg **Behandling av produktinformasjon \> Produkter \> Frigitte produkter** for å åpne siden **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="9b757-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="9b757-128">Skriv inn **D8100** i hurtigfilterfeltet for å finne det eksisterende frigitte produktet.</span><span class="sxs-lookup"><span data-stu-id="9b757-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Filtrering for frigitt produkt D8100 på siden Detaljer om frigitt produkt](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="9b757-130">I handlingsruten i kategorien **Utvikling** velger du **Rute** for å åpne **Rute**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b757-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="9b757-131">**Rute**-siden viser de åtte ruteversjonene for det frigitte produktet D8100.</span><span class="sxs-lookup"><span data-stu-id="9b757-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="9b757-132">De åtte ruteversjonene er fordelt mellom fire ruter på område 1 og område 5.</span><span class="sxs-lookup"><span data-stu-id="9b757-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="9b757-133">Rute 000400 brukes for etterkalkulering, rute 00041 brukes når lakkeringsoperasjonen er en intern operasjon, og rute 00042 som brukes når lakkeringsoperasjonen er en ekstern operasjon.</span><span class="sxs-lookup"><span data-stu-id="9b757-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Åtte ruteversjoner på Rute-siden](./media/subcontract03_route-page.png)

4. <span data-ttu-id="9b757-135">I den øvre ruten, i **Versjoner**-rutenettet, velger du ruteversjon **00042** for område **5**.</span><span class="sxs-lookup"><span data-stu-id="9b757-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="9b757-136">I den nedre ruten, i kategorien **Oversikt**, velger du operasjon **20** (**Cbnt CtSc**) i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="9b757-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Operasjon 20 ruteversjon 00042 for område 5 valgt](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="9b757-138">Velg kategorien **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="9b757-138">Select the **General** tab.</span></span>

    <span data-ttu-id="9b757-139">Legg merke til at feltet **Rutetype** er satt til **Leverandør**.</span><span class="sxs-lookup"><span data-stu-id="9b757-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="9b757-140">Denne verdien angir at operasjon 20 (Cbnt CtSc) er en utsatt operasjon.</span><span class="sxs-lookup"><span data-stu-id="9b757-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Rutetype-feltet satt til Leverandør i kategorien Generelt](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="9b757-142">Velg kategorien **Ressursbehov**.</span><span class="sxs-lookup"><span data-stu-id="9b757-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="9b757-143">Funksjonene blir brukt til å finne en aktuell ressurs under produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="9b757-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="9b757-144">For operasjon 20 (Cbnt CtSc), legg merke til at en ressurs som har to egenskaper, **Lakkering** og **Lakkerte kabinetter**, kreves.</span><span class="sxs-lookup"><span data-stu-id="9b757-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Egenskapene Lakkering og Lakkerte kabinetter i kategorien Ressurskrav](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="9b757-146">Velg **Gjeldende ressurser** for å åpne dialogboksen **Gjeldende ressurser** .</span><span class="sxs-lookup"><span data-stu-id="9b757-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="9b757-147">Det finnes tre ressurser som samsvarer med ressurskravene for operasjonen.</span><span class="sxs-lookup"><span data-stu-id="9b757-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="9b757-148">Legg merke til at 8851 og 8852 er av **Leverandør**-typen.</span><span class="sxs-lookup"><span data-stu-id="9b757-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Tre aktuelle ressurser i dialogboksen Gjeldende ressurser](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="9b757-150">Velg **OK** for å lukke dialogboksen **Gjeldende ressurser** og gå tilbake til **Rute**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b757-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="9b757-151">Lukk **Rute**-siden for å returnere til siden **Detaljer om frigitt produkt**.</span><span class="sxs-lookup"><span data-stu-id="9b757-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Siden Detaljer om frigitt produkt](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="9b757-153">I handlingsruten i kategorien **Utvikling** velger du **Stykklisteversjoner** for å åpne **Stykklisteversjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b757-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="9b757-154">**Stykklisteversjoner**-siden viser fire stykklisteversjoner for det frigitte produktet D8100.</span><span class="sxs-lookup"><span data-stu-id="9b757-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="9b757-155">000040 brukes for etterkalkulering og planlegging, stykkliste 000041 brukes hvis lakkeringsoperasjonen gjøres internt, og stykkliste 000042 og 000043 brukes hvis lakkeringsoperasjonen er satt ut.</span><span class="sxs-lookup"><span data-stu-id="9b757-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="9b757-156">Legg merke til at vare S8050 er et produkt av **Service**-varetypen.</span><span class="sxs-lookup"><span data-stu-id="9b757-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="9b757-157">Denne varen representerer arbeidet som er satt ut.</span><span class="sxs-lookup"><span data-stu-id="9b757-157">This item represents the subcontracted work.</span></span>

    ![Fire stykklisteversjoner på siden Stykklisteversjoner](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="9b757-159">På hurtigfanen **Stykklistelinjer**, velg **Rediger** for å åpne dialogboksen **Rediger stykklistelinje**.</span><span class="sxs-lookup"><span data-stu-id="9b757-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="9b757-160">Når en produksjonsordre er opprettet og estimert for frigitt produkt D8100, blir en bestilling generert automatisk for vare S8050.</span><span class="sxs-lookup"><span data-stu-id="9b757-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="9b757-161">Denne bestillingen knyttes til produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="9b757-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="9b757-162">For at bestillinger skal genereres automatisk, må **Linjetype**-feltet være satt til **Leverandør**, og leverandørkontoen for underleverandøren må være valgt.</span><span class="sxs-lookup"><span data-stu-id="9b757-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="9b757-163">I dette tilfellet er leverandørkontoen US-801.</span><span class="sxs-lookup"><span data-stu-id="9b757-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="9b757-164">Legg merke til at stykklistelinjen er koblet til lakkeringsoperasjonen gjennom operasjonsnummeret (i dette tilfellet 20).</span><span class="sxs-lookup"><span data-stu-id="9b757-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialogboksen Rediger stykklistelinje](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="9b757-166">Opprett et passord for lagerarbeidere</span><span class="sxs-lookup"><span data-stu-id="9b757-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="9b757-167">Du må definere et passord for lagerarbeiderne som bruker den håndholdte enheten.</span><span class="sxs-lookup"><span data-stu-id="9b757-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="9b757-168">Velg **Lagerstyring \> Oppsett \> Arbeider** for å åpne siden **Arbeidsbrukere**.</span><span class="sxs-lookup"><span data-stu-id="9b757-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="9b757-169">På hurtigfanen **Brukere** merker du raden for bruker **51**.</span><span class="sxs-lookup"><span data-stu-id="9b757-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Siden Arbeidsbrukere](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="9b757-171">Velg **Tilbakestill passord**.</span><span class="sxs-lookup"><span data-stu-id="9b757-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="9b757-172">I feltene **Passord** og **Bekreft passord**, angi **1**.</span><span class="sxs-lookup"><span data-stu-id="9b757-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="9b757-173">Velg **Angi passord**.</span><span class="sxs-lookup"><span data-stu-id="9b757-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="9b757-174">Trinnvis gjennomgang</span><span class="sxs-lookup"><span data-stu-id="9b757-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="9b757-175">**Scenario og bakgrunn**</span><span class="sxs-lookup"><span data-stu-id="9b757-175">**Scenario and background**</span></span>

<span data-ttu-id="9b757-176">En produksjonsordre på 10 deler opprettes for produkt D8100, "Lakkert kabinett".</span><span class="sxs-lookup"><span data-stu-id="9b757-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="9b757-177">Lakkeringen av kabinetter er en operasjon som er satt ut, som utføres hos leverandør US-801, Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="9b757-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="9b757-178">Produksjonsordren består av tre operasjoner.</span><span class="sxs-lookup"><span data-stu-id="9b757-178">The production order consists of three operations.</span></span> <span data-ttu-id="9b757-179">I den første operasjonen forhåndsmonteres kabinettet i en intern operasjon.</span><span class="sxs-lookup"><span data-stu-id="9b757-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="9b757-180">Materialet for forhåndsmonteringen frigis for plukking i råvarelageret.</span><span class="sxs-lookup"><span data-stu-id="9b757-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="9b757-181">Når forhåndsmonteringen er fullført, sendes kabinettet til Perfect Coating Solutions sammen med to materialer som kreves for lakkeringsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="9b757-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="9b757-182">Når det lakkerte kabinettet er mottatt fra leverandøren, går det gjennom en siste intern monteringsoperasjon før det blir rapportert som fullført.</span><span class="sxs-lookup"><span data-stu-id="9b757-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="9b757-183">Velg **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer** for å åpne siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="9b757-184">I handlingsruten velger du **Ny produksjonsordre** for å åpne dialogboksen **Opprett produksjonsordre**.</span><span class="sxs-lookup"><span data-stu-id="9b757-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialogboksen Opprett produksjonsordre](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="9b757-186">Velg **D8100** i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="9b757-187">Feltene for lagerdimensjoner vises når du velger varenummeret.</span><span class="sxs-lookup"><span data-stu-id="9b757-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="9b757-188">I **Farge**-feltet velger du **Krom**.</span><span class="sxs-lookup"><span data-stu-id="9b757-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="9b757-189">Det vises en meldingsboks der du blir spurt om de aktive versjonene for stykklisten og ruten skal settes inn.</span><span class="sxs-lookup"><span data-stu-id="9b757-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Meldingsboks](./media/subcontract13_message-box.png)

5. <span data-ttu-id="9b757-191">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9b757-191">Select **Yes**.</span></span> 

    <span data-ttu-id="9b757-192">I dialogboksen **Opprett produksjonsordre** er de aktive versjonene av stykklisten og ruten for produkt D8100 valgt automatisk i feltene **Stykklistenummer** og **Rutenummer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="9b757-193">I dette tilfellet er stykkliste **000040** og rute **000040** valgt.</span><span class="sxs-lookup"><span data-stu-id="9b757-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9b757-194">Både for stykklisten og ruten brukes versjon 000040 til etterkalkulering og planlegging.</span><span class="sxs-lookup"><span data-stu-id="9b757-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="9b757-195">I **Område**-feltet velger du **5**.</span><span class="sxs-lookup"><span data-stu-id="9b757-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="9b757-196">I **Lager**-feltet velger du **51**.</span><span class="sxs-lookup"><span data-stu-id="9b757-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="9b757-197">I feltene **Stykklistenummer** og **Rutenummer** endrer du verdien som ble valgt automatisk, til **000042**.</span><span class="sxs-lookup"><span data-stu-id="9b757-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b757-198">Både for stykklisten og ruten brukes versjon 000042 til å sette ut lakkeringen av kabinettet til leverandør US-801.</span><span class="sxs-lookup"><span data-stu-id="9b757-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Verdier angitt i dialogboksen Opprett produksjonsordre](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="9b757-200">Velg **Opprett** for å opprette produksjonsordren og gå tilbake til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Ny produksjonsordre på siden Alle produksjonsordrer](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="9b757-202">i handlingsruten, i kategorien **Produksjonsordre** velger du **Estimat** for å åpne dialogboksen **Estimat**.</span><span class="sxs-lookup"><span data-stu-id="9b757-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialogboksen Estimat](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="9b757-204">Velg **OK** for å bekrefte estimatet og gå tilbake til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b757-205">Når produksjonsordren er estimert, genereres bestillingen for servicevare S8050 for leverandør US-801.</span><span class="sxs-lookup"><span data-stu-id="9b757-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="9b757-206">I handlingsruten, i kategorien **Produksjonsordre** velger du **Stykkliste** for å åpne **Stykkliste**-siden, der du kan vise stykklistelinjene for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="9b757-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="9b757-207">Legg merke til at det er en referanse til bestillingen som ble generert da produksjonsordren ble estimert for servicevare S8050.</span><span class="sxs-lookup"><span data-stu-id="9b757-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Stykklistelinjer i produksjonsordre på Stykkliste-siden](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="9b757-209">Lukk **Stykkliste**-siden for å returnere til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="9b757-210">i handlingsruten, i kategorien **Planlegg** velger du **Planlegg jobber** for å åpne dialogboksen **Finplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="9b757-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="9b757-211">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="9b757-211">Specify the following values:</span></span>

    - <span data-ttu-id="9b757-212">Velg **Fremover fra i morgen** i **Planleggingsretning**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9b757-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="9b757-213">Sett **Begrenset kapasitet** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9b757-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialogboksen Finplanlegging](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="9b757-215">Velg **OK** for å lukke dialogboksen **Finplanlegging** og gå tilbake til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="9b757-216">I handlingsruten, i kategorien **Planlegg** velger du **Gantt** for å åpne siden **Gantt-diagram - Ressursvisning**.</span><span class="sxs-lookup"><span data-stu-id="9b757-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="9b757-217">Gantt-diagrammet gir en visuell oversikt over hvordan produksjonsjobbene er planlagt på ressursene.</span><span class="sxs-lookup"><span data-stu-id="9b757-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="9b757-218">Legg merke til at den eksterne lakkeringen består av tre jobber: en prosessjobb, en transportjobb og en køtidjobb.</span><span class="sxs-lookup"><span data-stu-id="9b757-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantt-diagram på siden Gantt-diagram - Ressursvisning](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="9b757-220">Lukk siden **Gantt-diagram - Ressursvisning** for å returnere til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="9b757-221">I handlingsruten, i kategorien **Produksjonsordre** velger du **Frigi** for å åpne dialogboksen **Frigi**.</span><span class="sxs-lookup"><span data-stu-id="9b757-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialogboksen Frigi](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="9b757-223">Velg **OK** for å lukke dialogboksen **Frigi**.</span><span class="sxs-lookup"><span data-stu-id="9b757-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="9b757-224">Velg **Produksjonskontroll \> Periodiske oppgaver \> Frigi til lager \> Automatisk frigivelse av stykkliste og formellinjer** for å åpne dialogboksen **Automatisk frigivelse av stykkliste og formellinjer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialogboksen Automatisk frigivelse av stykkliste og formellinjer](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="9b757-226">Velg **OK** for å kjøre jobben Automatisk frigivelse av stykkliste og formellinjer.</span><span class="sxs-lookup"><span data-stu-id="9b757-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="9b757-227">Denne jobben frigi plukkarbeid for råvarer til lageret.</span><span class="sxs-lookup"><span data-stu-id="9b757-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="9b757-228">Velg **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer** for å åpne siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="9b757-229">Bruk hurtigfilterfeltet til å velge produksjonsordren du har arbeidet med.</span><span class="sxs-lookup"><span data-stu-id="9b757-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="9b757-230">I handlingsruten i kategorien **Lager** velger du **Arbeidsdetaljer** for å åpne **Arbeid**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b757-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="9b757-231">Legg merke til at siden viser to sett med arbeid for råvareplukking.</span><span class="sxs-lookup"><span data-stu-id="9b757-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="9b757-232">Det første arbeidet er for materialene M8100 og M8101.</span><span class="sxs-lookup"><span data-stu-id="9b757-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="9b757-233">Disse materialene forbrukes av operasjonen 10.</span><span class="sxs-lookup"><span data-stu-id="9b757-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="9b757-234">Det andre arbeidet er for materialene M8202 og M8250.</span><span class="sxs-lookup"><span data-stu-id="9b757-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="9b757-235">Disse materialene forbrukes av operasjon 20, som er operasjonen som er satt ut.</span><span class="sxs-lookup"><span data-stu-id="9b757-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![To sett med arbeid for råvareplukking på Arbeid-siden.](./media/subcontract22_work-page.png)

26. <span data-ttu-id="9b757-237">Start lagerappen for å prosessere lagerarbeidet for operasjon 10.</span><span class="sxs-lookup"><span data-stu-id="9b757-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="9b757-238">Velg **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer** for å åpne siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="9b757-239">Bruk hurtigfilterfeltet til å velge produksjonsordren du har arbeidet med.</span><span class="sxs-lookup"><span data-stu-id="9b757-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="9b757-240">I handlingsruten, i kategorien **Produksjonsordre** velger du **Start** for å åpne dialogboksen **Start**.</span><span class="sxs-lookup"><span data-stu-id="9b757-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="9b757-241">I kategorien **Generelt** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="9b757-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="9b757-242">I feltet **Fra oper.nr.**</span><span class="sxs-lookup"><span data-stu-id="9b757-242">In the **From Oper. No.**</span></span> <span data-ttu-id="9b757-243">velg **10**.</span><span class="sxs-lookup"><span data-stu-id="9b757-243">field, select **10**.</span></span>
    - <span data-ttu-id="9b757-244">I feltet **Til oper.nr.**</span><span class="sxs-lookup"><span data-stu-id="9b757-244">In the **To Oper. No.**</span></span> <span data-ttu-id="9b757-245">velg **10**.</span><span class="sxs-lookup"><span data-stu-id="9b757-245">field, select **10**.</span></span>

    ![Verdier angitt i kategorien Generelt](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="9b757-247">Velg **OK** for å lukke dialogboksen **Start** og gå tilbake til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="9b757-248">Legg merke til at statusen for produksjonsordren nå er **Startet**.</span><span class="sxs-lookup"><span data-stu-id="9b757-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="9b757-249">Materialene for operasjon 10 forbrukes av en automatisk postering av plukklistejournalen.</span><span class="sxs-lookup"><span data-stu-id="9b757-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="9b757-250">Tidsforbruket for operasjon 10 er gjort rede for av en automatisk bokføring av en rutekortjournal.</span><span class="sxs-lookup"><span data-stu-id="9b757-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="9b757-251">Start lagerappen for å prosessere lagerarbeidet for operasjon 20.</span><span class="sxs-lookup"><span data-stu-id="9b757-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="9b757-252">I handlingsruten, i kategorien **Produksjonsordre** velger du **Start** for å åpne dialogboksen **Start**.</span><span class="sxs-lookup"><span data-stu-id="9b757-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="9b757-253">I kategorien **Generelt** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="9b757-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="9b757-254">I feltet **Fra oper.nr.**</span><span class="sxs-lookup"><span data-stu-id="9b757-254">In the **From Oper. No.**</span></span> <span data-ttu-id="9b757-255">velg **20**.</span><span class="sxs-lookup"><span data-stu-id="9b757-255">field, select **20**.</span></span>
    - <span data-ttu-id="9b757-256">I feltet **Til oper.nr.**</span><span class="sxs-lookup"><span data-stu-id="9b757-256">In the **To Oper. No.**</span></span> <span data-ttu-id="9b757-257">velg **20**.</span><span class="sxs-lookup"><span data-stu-id="9b757-257">field, select **20**.</span></span>
    - <span data-ttu-id="9b757-258">I feltet **Antall** angi **10**.</span><span class="sxs-lookup"><span data-stu-id="9b757-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="9b757-259">Sett alternativet **Poster plukkliste nå** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="9b757-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Verdier angitt i kategorien Generelt](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="9b757-261">Velg **OK** for å lukke dialogboksen **Start** og gå tilbake til siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9b757-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="9b757-262">Det opprettes en plukkliste for materialene som skal brukes for lakkeringsoperasjonen, og for servicevaren.</span><span class="sxs-lookup"><span data-stu-id="9b757-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="9b757-263">Servicevaren representerer kostnaden av operasjonen som er satt ut.</span><span class="sxs-lookup"><span data-stu-id="9b757-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="9b757-264">I handlingsruten, i kategorien **Vis** velger du **Plukkliste** for å åpne siden **Plukkliste**.</span><span class="sxs-lookup"><span data-stu-id="9b757-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="9b757-265">Velg plukklisten som ikke er postert, og velg deretter journalnummeret for å vise journallinjene.</span><span class="sxs-lookup"><span data-stu-id="9b757-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Journallinjer på siden Plukkliste](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="9b757-267">I handlingsruten, velger du **Skriv ut** \> **Plukklisterapport** for å åpne dialogboksen **Plukklisterapport**.</span><span class="sxs-lookup"><span data-stu-id="9b757-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="9b757-268">Angi alternativet **Bruk følgeseddeloppsett** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9b757-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialogboksen Plukklisterapport](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="9b757-270">Velg **OK** for å generere en **Plukkliste**-rapport.</span><span class="sxs-lookup"><span data-stu-id="9b757-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="9b757-271">I dette tilfellet skrives en leverandørfølgeseddel ut fra produksjonsplukklistejournalen.</span><span class="sxs-lookup"><span data-stu-id="9b757-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="9b757-272">Følgeseddelen angir materialene som sendes til leverandøren som skal utføre lakkeringsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="9b757-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Plukklisterapport](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="9b757-274">Lukk **Plukkliste**-rapporten for å gå tilbake til **Plukkliste**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b757-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="9b757-275">I handlingsruten, velger du **Poster** for å åpne dialogboksen **Poster journal**.</span><span class="sxs-lookup"><span data-stu-id="9b757-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialogboksen Poster journal](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="9b757-277">Velg **OK** for å lukke dialogboksen **Poster journal**.</span><span class="sxs-lookup"><span data-stu-id="9b757-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="9b757-278">Åpne bestillingen.</span><span class="sxs-lookup"><span data-stu-id="9b757-278">Open the purchase order.</span></span>

    ![Bestilling-siden](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="9b757-280">I handlingsruten, i kategorien **Kjøp** velger du **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="9b757-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="9b757-281">Velg **Poster** for å åpne dialogboksen **Poster journal**.</span><span class="sxs-lookup"><span data-stu-id="9b757-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="9b757-282">Velg **OK** for å lukke dialogboksen **Poster journal** og gå tilbake til siden **Bestilling**.</span><span class="sxs-lookup"><span data-stu-id="9b757-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="9b757-283">Endre enhetsprisen fra **33** til **40**.</span><span class="sxs-lookup"><span data-stu-id="9b757-283">Change the unit price from **33** to **40**.</span></span>

    ![Enhetspris endret på siden Bestilling](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="9b757-285">Bekreft bestillingen på nytt.</span><span class="sxs-lookup"><span data-stu-id="9b757-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="9b757-286">Mottaksseddel.</span><span class="sxs-lookup"><span data-stu-id="9b757-286">Product receipt.</span></span>

    ![Dialogboksen Poster mottaksseddel](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="9b757-288">Kjøpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="9b757-288">Purchase invoice.</span></span>
52. <span data-ttu-id="9b757-289">Oppdater samsvarsstatusen.</span><span class="sxs-lookup"><span data-stu-id="9b757-289">Update the match status.</span></span>

    ![Siden Leverandørfaktura](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="9b757-291">Ferdigmeld.</span><span class="sxs-lookup"><span data-stu-id="9b757-291">Report as finished.</span></span>

    ![Dialogboksen Ferdigmeld](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="9b757-293">Slutt.</span><span class="sxs-lookup"><span data-stu-id="9b757-293">End.</span></span>

    ![Dialogboks Slutt](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="9b757-295">Kostnadssammenligning.</span><span class="sxs-lookup"><span data-stu-id="9b757-295">Cost comparison.</span></span>

    ![Kostnadssammenligningsdiagrammer](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="9b757-297">Manglende oppsett i data.</span><span class="sxs-lookup"><span data-stu-id="9b757-297">Missing setup in data.</span></span>
