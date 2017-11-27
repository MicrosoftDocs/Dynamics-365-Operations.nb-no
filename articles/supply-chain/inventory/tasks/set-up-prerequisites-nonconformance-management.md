---
title: Definere forutsetninger for behandling
description: "Bruk denne fremgangsmåten for å aktivere prosjektstyringsprosesser for avvik."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: nb-no
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="d8397-103">Definere forutsetninger for behandling</span><span class="sxs-lookup"><span data-stu-id="d8397-103">Set up prerequisites for management</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8397-104">Bruk denne fremgangsmåten for å aktivere prosjektstyringsprosesser for avvik.</span><span class="sxs-lookup"><span data-stu-id="d8397-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="d8397-105">Et avvik beskriver en prosedyre eller vare som har et kvalitetsproblem, der den beskrivende informasjonen inkluderer kilden og problemtypen.</span><span class="sxs-lookup"><span data-stu-id="d8397-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="d8397-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d8397-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="d8397-107">Denne prosedyren utføres vanligvis av en kvalitetssjef.</span><span class="sxs-lookup"><span data-stu-id="d8397-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="d8397-108">Aktivere kvalitetsstyringsprosesser i firmaet</span><span class="sxs-lookup"><span data-stu-id="d8397-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="d8397-109">Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="d8397-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="d8397-110">Klikk kategorien Kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="d8397-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="d8397-111">Velg Ja i feltet Bruk kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="d8397-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="d8397-112">Velg denne parameteren for å aktivere kvalitetsstyringsprosesser for firmaet.</span><span class="sxs-lookup"><span data-stu-id="d8397-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="d8397-113">Angi et tall i Timepris-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8397-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="d8397-114">Bruk Timepris-feltet for å angi en timepris for arbeid i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="d8397-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="d8397-115">Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik.</span><span class="sxs-lookup"><span data-stu-id="d8397-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="d8397-116">Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik, og de har ingen betydning for annen funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="d8397-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="d8397-117">Klikk Rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="d8397-117">Click Report setup.</span></span>
    * <span data-ttu-id="d8397-118">Denne siden lar deg definere merknadstypene for kvalitetsrapport som skal brukes i ulike typer kvalitetsstyringsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d8397-118">This page allows you to define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="d8397-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-119">Close the page.</span></span>
7. <span data-ttu-id="d8397-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="d8397-121">Aktivere bruker for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="d8397-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="d8397-122">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="d8397-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="d8397-123">Hvis du vil behandle godkjenningen av et avvik, må brukeren som godkjenner eller avviser avvik ha en "Navn"-verdi som er tilordnet på siden Brukere.</span><span class="sxs-lookup"><span data-stu-id="d8397-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="d8397-124">Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.</span><span class="sxs-lookup"><span data-stu-id="d8397-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="d8397-125">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="d8397-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d8397-126">Du kan for eksempel filtrere på Navn-feltet med verdien Ricardo.</span><span class="sxs-lookup"><span data-stu-id="d8397-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="d8397-127">Bruk filteret til å finne brukeren som skal godkjenne eller avvise avvikspostene.</span><span class="sxs-lookup"><span data-stu-id="d8397-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="d8397-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d8397-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d8397-129">Hvis du vil behandle godkjenningen av et avvik, må du passe på at brukeren som godkjenner eller avviser avvik har en "Navn"-verdi som er tilordnet på siden Brukere.</span><span class="sxs-lookup"><span data-stu-id="d8397-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="d8397-130">Klikk Brukeralternativer.</span><span class="sxs-lookup"><span data-stu-id="d8397-130">Click User options.</span></span>
5. <span data-ttu-id="d8397-131">Klikk kategorien Innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d8397-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="d8397-132">Velg Ja i feltet Aktiver dokumentoversikt.</span><span class="sxs-lookup"><span data-stu-id="d8397-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="d8397-133">Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.</span><span class="sxs-lookup"><span data-stu-id="d8397-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="d8397-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-134">Close the page.</span></span>
8. <span data-ttu-id="d8397-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-135">Close the page.</span></span>
9. <span data-ttu-id="d8397-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="d8397-137">Definere diagnosetyper for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="d8397-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="d8397-138">Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Diagnosetyper.</span><span class="sxs-lookup"><span data-stu-id="d8397-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="d8397-139">Bruk Diagnosetyper-siden til å definere en klassifisering av diagnosehandlinger.</span><span class="sxs-lookup"><span data-stu-id="d8397-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="d8397-140">En korrigering identifiserer hvilken type diagnosehandling som bør utføres når det gjelder godkjente avvik, hvem som skal utføre den og den ønskede og planlagte fullføringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d8397-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="d8397-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8397-141">Click New.</span></span>
3. <span data-ttu-id="d8397-142">Skriv inn en verdi i feltet Diagnose.</span><span class="sxs-lookup"><span data-stu-id="d8397-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="d8397-143">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8397-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8397-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="d8397-145">Definere kvalitetsendringer for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="d8397-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="d8397-146">Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Kvalitetsstyringstillegg.</span><span class="sxs-lookup"><span data-stu-id="d8397-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="d8397-147">Bruk siden Kvalitetsstyringstillegg til å definere en klassifisering av tilleggene som skal brukes til operasjoner som er knyttet til avvik.</span><span class="sxs-lookup"><span data-stu-id="d8397-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="d8397-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8397-148">Click New.</span></span>
3. <span data-ttu-id="d8397-149">Skriv inn en verdi i Tilleggskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8397-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="d8397-150">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8397-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8397-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="d8397-152">Definere operasjonene for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="d8397-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="d8397-153">Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Operasjoner.</span><span class="sxs-lookup"><span data-stu-id="d8397-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="d8397-154">Bruk Operasjoner-siden til å definere en klassifisering av arbeidet som kan utføres for et godkjent avvik.</span><span class="sxs-lookup"><span data-stu-id="d8397-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="d8397-155">Når du relaterer operasjon til et avvik, kan du angi informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen.</span><span class="sxs-lookup"><span data-stu-id="d8397-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="d8397-156">Denne informasjonen danner grunnlaget for beregning av en estimert kostnad for å utføre operasjonen.</span><span class="sxs-lookup"><span data-stu-id="d8397-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="d8397-157">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8397-157">Click New.</span></span>
3. <span data-ttu-id="d8397-158">Skriv inn en verdi i feltet Operasjon.</span><span class="sxs-lookup"><span data-stu-id="d8397-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="d8397-159">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8397-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8397-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="d8397-161">Definere problemtyper for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="d8397-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="d8397-162">Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Problemtyper.</span><span class="sxs-lookup"><span data-stu-id="d8397-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="d8397-163">Bruk Problemtyper-siden til å definere en klassifisering av kvalitetsproblemer som oppdages i de ulike avvikstypene.</span><span class="sxs-lookup"><span data-stu-id="d8397-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="d8397-164">Avvikstyper inkluderer Intern, Kunde, Leverandør, Tjenesteforespørsel, Produksjon og Koproduktproduksjon.</span><span class="sxs-lookup"><span data-stu-id="d8397-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="d8397-165">En enkelt problemtype kan være tilknyttet flere avvikstyper.</span><span class="sxs-lookup"><span data-stu-id="d8397-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="d8397-166">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8397-166">Click New.</span></span>
3. <span data-ttu-id="d8397-167">Skriv inn en verdi i feltet Problemtype.</span><span class="sxs-lookup"><span data-stu-id="d8397-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="d8397-168">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8397-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8397-169">Klikk Avvikstyper.</span><span class="sxs-lookup"><span data-stu-id="d8397-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="d8397-170">Bruk Avvikstyper-siden til å godkjenne bruk av en problemtype som skal brukes i én eller flere av avvikstypene.</span><span class="sxs-lookup"><span data-stu-id="d8397-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="d8397-171">For eksempel kan en problemtype som gjelder en mangelkode, gjelde alle avvikstyper, mens en problemtype som gjelder klager fra kunder, kan gjelde bare for avvikstypene kunde og serviceforespørsel.</span><span class="sxs-lookup"><span data-stu-id="d8397-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="d8397-172">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8397-172">Click New.</span></span>
7. <span data-ttu-id="d8397-173">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d8397-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d8397-174">Velg et alternativ i Avvikstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8397-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="d8397-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-175">Close the page.</span></span>
10. <span data-ttu-id="d8397-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="d8397-177">Definere karantenesoner for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="d8397-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="d8397-178">Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Karantenesoner.</span><span class="sxs-lookup"><span data-stu-id="d8397-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="d8397-179">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d8397-179">Click New.</span></span>
3. <span data-ttu-id="d8397-180">Skriv inn en verdi i feltet Karantenesone.</span><span class="sxs-lookup"><span data-stu-id="d8397-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="d8397-181">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8397-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8397-182">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d8397-182">Close the page.</span></span>

