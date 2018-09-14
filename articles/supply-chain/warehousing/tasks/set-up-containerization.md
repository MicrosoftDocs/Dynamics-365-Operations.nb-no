--- 
title: Definere containerbruk
description: "Denne fremgangsmåten beskriver hvordan du automatiserer containerbruken av laster i Lagerstyring."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="f3626-103">Definere containerbruk</span><span class="sxs-lookup"><span data-stu-id="f3626-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3626-104">Denne fremgangsmåten beskriver hvordan du automatiserer containerbruken av laster i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="f3626-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="f3626-105">Automatisert containerbruk oppretter containere og plukkarbeidet for forsendelser når en bølge behandles, og arbeidslinjer kan deles inn i antall som får plass i containerne.</span><span class="sxs-lookup"><span data-stu-id="f3626-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="f3626-106">På denne måten kan lagermedarbeidere plukke varene direkte til den valgte containeren.</span><span class="sxs-lookup"><span data-stu-id="f3626-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="f3626-107">Sammenlignet med den manuelle pakkeprosessen kan oppgaver som oppretting av beholdere, tilordning av varer og lukking av beholdere, automatiseres av systemet.</span><span class="sxs-lookup"><span data-stu-id="f3626-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="f3626-108">Denne fremgangsmåten bruker USMF-demofirmaet og utføres av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="f3626-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="f3626-109">Definere en bølgemal</span><span class="sxs-lookup"><span data-stu-id="f3626-109">Set up a wave template</span></span>
1. <span data-ttu-id="f3626-110">Gå til Lagerstyring > Oppsett > Bølger > Bølgemaler.</span><span class="sxs-lookup"><span data-stu-id="f3626-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="f3626-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-111">Click New.</span></span>
3. <span data-ttu-id="f3626-112">Angi en verdi i feltet Navn på bølgemal.</span><span class="sxs-lookup"><span data-stu-id="f3626-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="f3626-113">Skriv inn en verdi i feltet Beskrivelse av bølgemal.</span><span class="sxs-lookup"><span data-stu-id="f3626-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="f3626-114">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3626-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f3626-115">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="f3626-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="f3626-116">Vis delen Metoder.</span><span class="sxs-lookup"><span data-stu-id="f3626-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="f3626-117">Valgte metoder-ruten viser metodene for den valgte bølgemaltypen.</span><span class="sxs-lookup"><span data-stu-id="f3626-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="f3626-118">Bølgemalen må inneholde containerbruk-metoden.</span><span class="sxs-lookup"><span data-stu-id="f3626-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="f3626-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f3626-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f3626-120">Skriv inn en verdi i feltet Bølgetrinn.</span><span class="sxs-lookup"><span data-stu-id="f3626-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="f3626-121">Angi en bølgetrinnkode for metoden som legges til, som kan være en hvilken som helst kode.</span><span class="sxs-lookup"><span data-stu-id="f3626-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="f3626-122">Det er mulig å legge til metoden mer enn én gang og tilordne forskjellige bølgetrinnkoder.</span><span class="sxs-lookup"><span data-stu-id="f3626-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="f3626-123">Hvis du vil gjøre dette, velg Kan gjentas for denne metoden på siden Bølgebehandlingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="f3626-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="f3626-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3626-124">Click Save.</span></span>
11. <span data-ttu-id="f3626-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3626-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="f3626-126">Definere en containertype</span><span class="sxs-lookup"><span data-stu-id="f3626-126">Set up a container type</span></span>
1. <span data-ttu-id="f3626-127">Gå til Lagerstyring > Oppsett > Containere > Containertyper.</span><span class="sxs-lookup"><span data-stu-id="f3626-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="f3626-128">Du kan definere containerne på siden i Containertyper.</span><span class="sxs-lookup"><span data-stu-id="f3626-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="f3626-129">Du kan konfigurere de fysiske målene til containere, inkludert taravekt, maksimumsvekt, maksimalt volum, lengde, bredde og høyde.</span><span class="sxs-lookup"><span data-stu-id="f3626-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="f3626-130">I dette eksemplet har vi bokser med tre forskjellige størrelser.</span><span class="sxs-lookup"><span data-stu-id="f3626-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="f3626-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-131">Click New.</span></span>
3. <span data-ttu-id="f3626-132">Skriv inn en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f3626-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="f3626-133">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="f3626-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="f3626-134">Angi et tall i feltet Maksimumsvekt.</span><span class="sxs-lookup"><span data-stu-id="f3626-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="f3626-135">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="f3626-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="f3626-136">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="f3626-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="f3626-137">Angi et tall i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="f3626-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="f3626-138">Angi et tall i feltet Høyde.</span><span class="sxs-lookup"><span data-stu-id="f3626-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="f3626-139">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f3626-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f3626-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3626-140">Click Save.</span></span>
12. <span data-ttu-id="f3626-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-141">Click New.</span></span>
13. <span data-ttu-id="f3626-142">Skriv inn en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f3626-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="f3626-143">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f3626-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="f3626-144">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="f3626-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="f3626-145">Angi et tall i feltet Maksimumsvekt.</span><span class="sxs-lookup"><span data-stu-id="f3626-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="f3626-146">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="f3626-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="f3626-147">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="f3626-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="f3626-148">Angi et tall i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="f3626-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="f3626-149">Angi et tall i feltet Høyde.</span><span class="sxs-lookup"><span data-stu-id="f3626-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="f3626-150">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3626-150">Click Save.</span></span>
22. <span data-ttu-id="f3626-151">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-151">Click New.</span></span>
23. <span data-ttu-id="f3626-152">Skriv inn en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f3626-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="f3626-153">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f3626-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="f3626-154">Angi et tall i feltet Taravekt.</span><span class="sxs-lookup"><span data-stu-id="f3626-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="f3626-155">Angi et tall i feltet Maksimumsvekt.</span><span class="sxs-lookup"><span data-stu-id="f3626-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="f3626-156">Angi et tall i feltet Volum.</span><span class="sxs-lookup"><span data-stu-id="f3626-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="f3626-157">Angi et tall i feltet Lengde.</span><span class="sxs-lookup"><span data-stu-id="f3626-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="f3626-158">Angi et tall i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="f3626-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="f3626-159">Angi et tall i feltet Høyde.</span><span class="sxs-lookup"><span data-stu-id="f3626-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="f3626-160">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3626-160">Click Save.</span></span>
32. <span data-ttu-id="f3626-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3626-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="f3626-162">Konfigurere en containergruppe</span><span class="sxs-lookup"><span data-stu-id="f3626-162">Set up a container group</span></span>
1. <span data-ttu-id="f3626-163">Gå til Lagerstyring > Oppsett > Containere > Containergrupper.</span><span class="sxs-lookup"><span data-stu-id="f3626-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="f3626-164">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-164">Click New.</span></span>
    * <span data-ttu-id="f3626-165">Du kan definere logiske grupper med containertyper.</span><span class="sxs-lookup"><span data-stu-id="f3626-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="f3626-166">Du kan angi rekkefølgen som containerne skal pakkes i og containernes fyllprosent for hver gruppe. Varens størrelsesdimensjoner brukes til å bestemme om den passer i en container.</span><span class="sxs-lookup"><span data-stu-id="f3626-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="f3626-167">Containeren som er nærmest størrelsesdimensjonen for varen, brukes.</span><span class="sxs-lookup"><span data-stu-id="f3626-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="f3626-168">Hvis du har flere containertyper i en gruppe, anbefaler vi at du ordner rekkefølgen etter størrelse, slik at den største containeren kommer først, som nummer 1 i rekkefølgen, og den minste containeren kommer sist.</span><span class="sxs-lookup"><span data-stu-id="f3626-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="f3626-169">Skriv inn en verdi i feltet Containergruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="f3626-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="f3626-170">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f3626-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3626-171">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-171">Click New.</span></span>
6. <span data-ttu-id="f3626-172">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f3626-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f3626-173">Angi eller velg en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f3626-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="f3626-174">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-174">Click New.</span></span>
9. <span data-ttu-id="f3626-175">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f3626-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f3626-176">Angi eller velg en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f3626-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="f3626-177">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-177">Click New.</span></span>
12. <span data-ttu-id="f3626-178">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f3626-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f3626-179">Angi eller velg en verdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f3626-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="f3626-180">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3626-180">Click Save.</span></span>
15. <span data-ttu-id="f3626-181">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3626-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="f3626-182">Definere en mal for containerversjon</span><span class="sxs-lookup"><span data-stu-id="f3626-182">Set up a container build template</span></span>
1. <span data-ttu-id="f3626-183">Gå til Lagerstyring > Oppsett > Containere > Maler for containerbygging.</span><span class="sxs-lookup"><span data-stu-id="f3626-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="f3626-184">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-184">Click New.</span></span>
    * <span data-ttu-id="f3626-185">Malen for containerbygging er basert hvilken av containerbrukprosessene som utføres.</span><span class="sxs-lookup"><span data-stu-id="f3626-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="f3626-186">Hver mal for containerbygging definerer én containerbrukprosess som skal brukes som bølgemal.</span><span class="sxs-lookup"><span data-stu-id="f3626-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="f3626-187">Alternativet Rediger spørring lar deg definere betingelsene som den valgte malen skal behandles etter.</span><span class="sxs-lookup"><span data-stu-id="f3626-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="f3626-188">Du kan for eksempel bare kjøre containerbruk for bestemte kunder, produkter eller lagre, eller du kan legge til de tilsvarende spørringsområdene i malen.</span><span class="sxs-lookup"><span data-stu-id="f3626-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="f3626-189">Feltet Bølgetrinnkode er hvordan en mal for containerbygging er knyttet til trinnene i en bølgemal.</span><span class="sxs-lookup"><span data-stu-id="f3626-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="f3626-190">Når bølgen kjøres, fastsettes hvilke maler for containerbygging som brukes til å starte containerbruk.</span><span class="sxs-lookup"><span data-stu-id="f3626-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="f3626-191">Feltet Grunnleggende spørringstyper bestemmer hva som skal pakkes og hva filterspørringen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="f3626-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="f3626-192">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f3626-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f3626-193">Skriv inn en verdi i feltet Containermal-ID.</span><span class="sxs-lookup"><span data-stu-id="f3626-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="f3626-194">Angi eller velg en verdi i feltet Containergruppe-ID.</span><span class="sxs-lookup"><span data-stu-id="f3626-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="f3626-195">Skriv inn en verdi i feltet Bølgetrinn.</span><span class="sxs-lookup"><span data-stu-id="f3626-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="f3626-196">Merk av for Tillat oppdeling av plukking.</span><span class="sxs-lookup"><span data-stu-id="f3626-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="f3626-197">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f3626-197">Click Save.</span></span>
9. <span data-ttu-id="f3626-198">Klikk Begrensninger for containerkombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="f3626-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="f3626-199">Blanding av brudd i kombinasjonslogikk lar deg definere regler for pakketildelingslinjer i containere.</span><span class="sxs-lookup"><span data-stu-id="f3626-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="f3626-200">Hvis du for eksempel legger til feltet Varenummer når varer tildeles containere, opprettes en ny container når det er et nytt varenummer.</span><span class="sxs-lookup"><span data-stu-id="f3626-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="f3626-201">Dette er vil hindre at ansatte pakker tildelingslinjer for to ulike kunder i den samme containeren.</span><span class="sxs-lookup"><span data-stu-id="f3626-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="f3626-202">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f3626-202">Click New.</span></span>
11. <span data-ttu-id="f3626-203">Velg et alternativ i feltet Tabell.</span><span class="sxs-lookup"><span data-stu-id="f3626-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="f3626-204">Angi eller velg en verdi i feltet Feltvalg.</span><span class="sxs-lookup"><span data-stu-id="f3626-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="f3626-205">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f3626-205">Click OK.</span></span>


