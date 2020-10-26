---
title: Formidle veiledninger for blandet virkelighet for arbeidere i produksjonen
description: Dette emnet beskriver hvordan du integrerer produksjonsstyringsmodulen i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: d8c2da17d4e3df37c55844f0aad00f883725f741
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989288"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="beb74-103">Formidle veiledninger for blandet virkelighet for arbeidere i produksjonen</span><span class="sxs-lookup"><span data-stu-id="beb74-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="beb74-104">Arbeidere i produksjonsprosesser vil dra nytte av relevante instruksjoner som gis til riktig tid i sammenheng med arbeidet.</span><span class="sxs-lookup"><span data-stu-id="beb74-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="beb74-105">*Instruksjoner* gjelder for flere arbeidsområder, inkludert: samling, tjeneste, operasjoner, sertifisering og sikkerhet.</span><span class="sxs-lookup"><span data-stu-id="beb74-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="beb74-106">På tvers av alle disse kjernefunksjonene kan pågående opplæringsinstruksjoner bidra til å gi ansatte muligheten til å oppnå mer og arbeide bedre.</span><span class="sxs-lookup"><span data-stu-id="beb74-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="beb74-107">Innledning</span><span class="sxs-lookup"><span data-stu-id="beb74-107">Introduction</span></span>

<span data-ttu-id="beb74-108">Du kan gi instruksjoner på forskjellige måter.</span><span class="sxs-lookup"><span data-stu-id="beb74-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="beb74-109">Ett effektivt system som leveres som standard, bruker [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="beb74-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="beb74-110">Dynamics 365 Guides kan bidra til å gi de ansatte praktisk læring.</span><span class="sxs-lookup"><span data-stu-id="beb74-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="beb74-111">Du kan definere standardiserte prosesser med trinnvise instruksjoner som leder de ansatte til verktøyene og delene de trenger, og viser de ansatte hvordan de skal bruke disse verktøyene i virkelige situasjoner.</span><span class="sxs-lookup"><span data-stu-id="beb74-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="beb74-112">Du kan knytte veiledninger til ulike deler av produksjonskontrollen, blant annet:</span><span class="sxs-lookup"><span data-stu-id="beb74-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="beb74-113">Ressurser</span><span class="sxs-lookup"><span data-stu-id="beb74-113">Resources</span></span>](#resources)
- [<span data-ttu-id="beb74-114">Ressursgrupper</span><span class="sxs-lookup"><span data-stu-id="beb74-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="beb74-115">Frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="beb74-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="beb74-116">Formler</span><span class="sxs-lookup"><span data-stu-id="beb74-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="beb74-117">Formelversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="beb74-118">Stykklister</span><span class="sxs-lookup"><span data-stu-id="beb74-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="beb74-119">Stykklisteversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="beb74-120">Ruter</span><span class="sxs-lookup"><span data-stu-id="beb74-120">Routes</span></span>](#routes)
- [<span data-ttu-id="beb74-121">Ruteversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="beb74-122">Ruteoperasjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="beb74-123">Du kan også knytte veiledninger til aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="beb74-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="beb74-124">Hvis du vil ha mer informasjon om dette alternativet, kan du se [Integrere Dynamics 365 Supply Chain Management (Aktivastyring) med Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="beb74-125">Når en førstelinjearbeider velger en jobb i produksjonen via Supply Chain Management, kan arbeideren se [de relevante veiledningene](#logic) på jobbkortet.</span><span class="sxs-lookup"><span data-stu-id="beb74-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="beb74-126">Når arbeideren velger en bestemt veiledning, vises det en QR-kode for denne veiledningen på skjermen.</span><span class="sxs-lookup"><span data-stu-id="beb74-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="beb74-127">Deretter bruker arbeideren sin HoloLens til å skanne QR-koden, som starter veiledninger og viser de nødvendige instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="beb74-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="beb74-128">Underdelene nedenfor beskriver noen få utvalgte scenarier der selskaper på tvers av bransjer, kan se den største verdien ved bruk av veiledninger til å presentere instruksjoner for produksjon.</span><span class="sxs-lookup"><span data-stu-id="beb74-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="beb74-129">Samling</span><span class="sxs-lookup"><span data-stu-id="beb74-129">Assembly</span></span>

<span data-ttu-id="beb74-130">![Bruke veiledninger i monteringsoppgaver](media/instruction-guides-hero-assembly.png "Bruke veiledninger i serviceoppgaver")</span><span class="sxs-lookup"><span data-stu-id="beb74-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="beb74-131">Instruksjoner i monteringsoperasjoner viser arbeidere verktøyene og delene de trenger, og hvordan de brukes i virkelige arbeidssituasjoner.</span><span class="sxs-lookup"><span data-stu-id="beb74-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="beb74-132">Produksjonsledere kan opprette og tilordne veiledninger, for eksempel [produksjonsruter](routes-operations.md), [operasjonsrelasjoner](routes-operations.md#operation-relations) eller [stykklister](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="beb74-133">Arbeidere finner de relevante instruksjonene om de respektive operasjonsopplevelsen i produksjonen.</span><span class="sxs-lookup"><span data-stu-id="beb74-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="beb74-134">Service</span><span class="sxs-lookup"><span data-stu-id="beb74-134">Service</span></span>

<span data-ttu-id="beb74-135">![Bruke veiledninger i serviceoppgaver](media/instruction-guides-hero-service.png "Bruke veiledninger i serviceoppgaver")</span><span class="sxs-lookup"><span data-stu-id="beb74-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="beb74-136">Utstyr teknikere med veiledende instruksjoner på jobbområdet, og eliminer behovet for å planlegge ekstra besøk.</span><span class="sxs-lookup"><span data-stu-id="beb74-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="beb74-137">Serviceledere kan tilordne veiledninger, for eksempel for bestemte [produkter](../../commerce/product.md), som går gjennom rutiner for kvalitetsvurdering.</span><span class="sxs-lookup"><span data-stu-id="beb74-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="beb74-138">Kvalitet</span><span class="sxs-lookup"><span data-stu-id="beb74-138">Quality</span></span>

<span data-ttu-id="beb74-139">![Bruk veiledninger i kvalitetssikringsoppgaver](media/instruction-guides-hero-quality.png "Bruk veiledninger i kvalitetssikringsoppgaver")</span><span class="sxs-lookup"><span data-stu-id="beb74-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="beb74-140">Distribusjon av nye prosesser og sikre økt konsekvens ved å gjøre den ansattes kunnskap om til et verktøy som kan gjentas.</span><span class="sxs-lookup"><span data-stu-id="beb74-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="beb74-141">Kvalitetssikringsledere kan tilordne veiledninger, for eksempel for [produkter](../../commerce/product.md), som går gjennom rutiner for kvalitetsvurdering.</span><span class="sxs-lookup"><span data-stu-id="beb74-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="beb74-142">Sertifiseringer</span><span class="sxs-lookup"><span data-stu-id="beb74-142">Certifications</span></span>

<span data-ttu-id="beb74-143">![Bruk veiledninger for sertifiseringsrelaterte oppgaver](media/instruction-guides-hero-certification.png "Bruk veiledninger for sertifiseringsrelaterte oppgaver")</span><span class="sxs-lookup"><span data-stu-id="beb74-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="beb74-144">Sørg for at alle ansatte oppfyller høye standarder ved raskt å identifisere hvem som trenger hjelp og hvor.</span><span class="sxs-lookup"><span data-stu-id="beb74-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="beb74-145">Sikkerhet</span><span class="sxs-lookup"><span data-stu-id="beb74-145">Safety</span></span>

<span data-ttu-id="beb74-146">![Bruk veiledninger i instruksjoner for jobbsikkerhet](media/instruction-guides-hero-safety.png "Bruk veiledninger i instruksjoner for jobbsikkerhet")</span><span class="sxs-lookup"><span data-stu-id="beb74-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="beb74-147">Angi instruksjoner som veileder virtuelt gjennom farlige prosedyrer før det prøves i det fysiske miljøet.</span><span class="sxs-lookup"><span data-stu-id="beb74-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="beb74-148">Med en metode for blandet virkelighet kan arbeidere oppleve farlige prosedyrer virtuelt.</span><span class="sxs-lookup"><span data-stu-id="beb74-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="beb74-149">Produksjonsledere kan tilby dedikerte håndteringsinstruksjoner for farlige materialhåndtering eller dedikerte håndteringsprosedyrer, ved å tilordne instruksjoner til [produktvarer](../../commerce/product.md), [ruter](routes-operations.md) og [operasjoner](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="beb74-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="beb74-150">Komme i gang med instruksjoner og veiledninger</span><span class="sxs-lookup"><span data-stu-id="beb74-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="beb74-151">Hvis du vil aktivere instruksjoner i produksjonsprosesser, inneholder Supply Chain Management en standardintegrering med Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="beb74-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="beb74-152">Det kreves en lisensiert og installert programforekomst av Guides for å bygge, vedlikeholde og tilordne instruksjoner for blandet virkelighet til produksjonsressurser og arbeid.</span><span class="sxs-lookup"><span data-stu-id="beb74-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="beb74-153">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="beb74-153">Prerequisites</span></span>

<span data-ttu-id="beb74-154">Hvis du vil bruke denne funksjonen, må systemet inneholde følgende:</span><span class="sxs-lookup"><span data-stu-id="beb74-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="beb74-155">Dynamics 365 Supply Chain Management versjon 10.0.15 eller senere</span><span class="sxs-lookup"><span data-stu-id="beb74-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="beb74-156">[Dobbel skriving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management-apper.</span><span class="sxs-lookup"><span data-stu-id="beb74-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="beb74-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versjon 400.0.1.48 eller nyere</span><span class="sxs-lookup"><span data-stu-id="beb74-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="beb74-158">Aktivere funksjonen</span><span class="sxs-lookup"><span data-stu-id="beb74-158">Turn on the feature</span></span>

<span data-ttu-id="beb74-159">Hvis du vil gjøre funksjonen tilgjengelig på systemet, må du aktivere konfigurasjonsnøklene for den.</span><span class="sxs-lookup"><span data-stu-id="beb74-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="beb74-160">Du trenger bare å gjøre dette én gang.</span><span class="sxs-lookup"><span data-stu-id="beb74-160">You only need to do this once.</span></span> <span data-ttu-id="beb74-161">Hvis du vil gjøre dette, må en administrator gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="beb74-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="beb74-162">Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="beb74-163">Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon** .</span><span class="sxs-lookup"><span data-stu-id="beb74-163">Go to **System administration \> Setup \> License configuration** .</span></span>
1. <span data-ttu-id="beb74-164">Vis delen **Blandet virkelighet** , og merk av for **Blandet virkelighet-veiledning** .</span><span class="sxs-lookup"><span data-stu-id="beb74-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="beb74-165">Vis delen **Produksjonsstyring** , og merk av for **Produksjonsinstruksjoner** .</span><span class="sxs-lookup"><span data-stu-id="beb74-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="beb74-166">Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="beb74-167">Konfigurere hvordan veiledninger vises i produksjonen</span><span class="sxs-lookup"><span data-stu-id="beb74-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="beb74-168">Hvis du vil konfigurere hvordan veiledninger skal vises i produksjonen, kan du gå til **Blandet virkelighet \> Dynamics 365 Guides \> Konfigurer integrering av veiledning** .</span><span class="sxs-lookup"><span data-stu-id="beb74-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration** .</span></span>

<span data-ttu-id="beb74-169">![Konfigurere integrering av veiledning for produksjon](media/instruction-guides-configure-integration.png "Konfigurere integrering av veiledning for produksjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="beb74-170">Angi følgende felt:</span><span class="sxs-lookup"><span data-stu-id="beb74-170">Set the following fields:</span></span>

- <span data-ttu-id="beb74-171">**Underdomene for CDS-miljø** – Dette feltet skal allerede vise en verdi.</span><span class="sxs-lookup"><span data-stu-id="beb74-171">**CDS environment subdomain** - This field should already show a value.</span></span> <span data-ttu-id="beb74-172">Dette feltet inneholder underdomenet for Common Data Service-miljøet der du oppretter veiledninger.</span><span class="sxs-lookup"><span data-stu-id="beb74-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="beb74-173">Underdomenet er den første delen av URL-adressen og blir vanligvis navngitt etter organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="beb74-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="beb74-174">Hvis for eksempel URL-adressen Common Data Service er contoso.crm4.dynamics.com, angir du *contoso* her.</span><span class="sxs-lookup"><span data-stu-id="beb74-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="beb74-175">Denne verdien brukes til å skrive adresser for veiledningene og blir kodet i QR-kodene.</span><span class="sxs-lookup"><span data-stu-id="beb74-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="beb74-176">**QR-kodestørrelse** – Angi størrelsen på den gjengitte QR-koden.</span><span class="sxs-lookup"><span data-stu-id="beb74-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="beb74-177">Vi anbefaler at du velger en størrelse som fyller meste parten av skjermen, men ikke mer.</span><span class="sxs-lookup"><span data-stu-id="beb74-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="beb74-178">Vanligvis er *15* en god verdi.</span><span class="sxs-lookup"><span data-stu-id="beb74-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="beb74-179">**Feilkorrigeringsnivå for QR-kode** – Angi detaljnivået for QR-koden.</span><span class="sxs-lookup"><span data-stu-id="beb74-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="beb74-180">Høyere detaljnivå kan bidra til å øke kodens pålitelighet, men **QR-kodestørrelse** må være stor nok til å støtte detaljnivået som kreves av det valgte korrigeringsnivået.</span><span class="sxs-lookup"><span data-stu-id="beb74-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="beb74-181">QR-kodestørrelser som er for store for skjermen, vil ta litt lengre tid å gjengi og deretter skaleres ned for å få plass til skjermen.</span><span class="sxs-lookup"><span data-stu-id="beb74-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="beb74-182">Dette har ingen fordeler.</span><span class="sxs-lookup"><span data-stu-id="beb74-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="beb74-183">QR-kodestørrelser som er for små, kan redusere muligheten for HoloLens til å lese koden på riktig måte i enkelte miljøer.</span><span class="sxs-lookup"><span data-stu-id="beb74-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="beb74-184">Vi anbefaler at du tester innstillingene for hver enhet som vil vise QR-koder for HoloLens-brukere.</span><span class="sxs-lookup"><span data-stu-id="beb74-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="beb74-185">Velg innstillinger som gir deg tilstrekkelig lesbarhet i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="beb74-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="beb74-186">Få en oversikt over alle tilordning av veiledninger</span><span class="sxs-lookup"><span data-stu-id="beb74-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="beb74-187">Bruk siden **Alle veiledninger** til å vise listen over alle tilgjengelige veiledninger i organisasjonen og alle tildelinger til produksjonsprosessene og ressurser.</span><span class="sxs-lookup"><span data-stu-id="beb74-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="beb74-188">Hvis du vil åpne den, kan du gå til **Blandet virkelighet \> Veiledninger \> Alle veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-188">To open it, go to **Mixed reality \> Guides \> All Guides** .</span></span> <span data-ttu-id="beb74-189">Listen øverst viser alle tilgjengelige veiledninger, og du kan bruke feltet her til å filtrere listen.</span><span class="sxs-lookup"><span data-stu-id="beb74-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="beb74-190">Listen nederst viser alle tilordning av veiledninger og har en verktøylinje for å behandle dem.</span><span class="sxs-lookup"><span data-stu-id="beb74-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="beb74-191">![Behandle veiledninger](media/instruction-guides-allguides.png "Behandle veiledninger")</span><span class="sxs-lookup"><span data-stu-id="beb74-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="beb74-192">Delene nedenfor beskriver objekttypene du kan tilordne veiledninger til.</span><span class="sxs-lookup"><span data-stu-id="beb74-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="beb74-193">Hver tilordnet veiledning inneholder instruksjoner som automatisk knyttes til de respektive produksjonsjobbene og vil være tilgjengelig i produksjonen.</span><span class="sxs-lookup"><span data-stu-id="beb74-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="beb74-194">Knytte en veiledning til en ressurs</span><span class="sxs-lookup"><span data-stu-id="beb74-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="beb74-195">Legg en veiledning til en [ressurs](operations-resources.md) for å tilby veiledningen i konteksten til aktuelle produksjonsjobber.</span><span class="sxs-lookup"><span data-stu-id="beb74-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="beb74-196">Vanlig scenario ved bruk av ressurser</span><span class="sxs-lookup"><span data-stu-id="beb74-196">Typical scenario using resources</span></span>

<span data-ttu-id="beb74-197">Du kan for eksempel legge til en veiledning med generell maskinsikkerhet eller håndteringsinstruksjoner i en ressurs av typen maskin.</span><span class="sxs-lookup"><span data-stu-id="beb74-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="beb74-198">Deretter vil veiledningen være tilgjengelig i alle jobber som utføres på maskinen.</span><span class="sxs-lookup"><span data-stu-id="beb74-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="beb74-199">Legg en veiledning til en ressurs</span><span class="sxs-lookup"><span data-stu-id="beb74-199">Add a Guide to a resource</span></span>

<span data-ttu-id="beb74-200">Slik legger du en veiledning til en ressurs:</span><span class="sxs-lookup"><span data-stu-id="beb74-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="beb74-201">Gå til **Produksjonskontroll \> Oppsett \> Ressurser \> Ressursfunksjoner** .</span><span class="sxs-lookup"><span data-stu-id="beb74-201">Go to **Production control \> Setup \> Resources \> Resources** .</span></span>
1. <span data-ttu-id="beb74-202">Velg ressursen du vil tilordne en veiledning til, fra listeruten.</span><span class="sxs-lookup"><span data-stu-id="beb74-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-203">Vis hurtigfanen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="beb74-204">Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="beb74-205">Det blir lagt til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="beb74-206">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="beb74-207">Hvis du har et stort antall veiledninger, kan du filtrere listen for å finne den du leter etter.</span><span class="sxs-lookup"><span data-stu-id="beb74-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="beb74-208">![Behandle veiledninger](media/instruction-guides-allguides.png "Behandle veiledninger")</span><span class="sxs-lookup"><span data-stu-id="beb74-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="beb74-209">Knytte en veiledning til en ressursgruppe</span><span class="sxs-lookup"><span data-stu-id="beb74-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="beb74-210">Du kan legge en veiledning til [ressursgrupper](tasks/define-discrete-manufacturing-resource-group.md) hvis du bruker dem til å administrere grupper av maskiner, produksjonslinjer eller arbeidsceller.</span><span class="sxs-lookup"><span data-stu-id="beb74-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="beb74-211">Vanlige scenarier ved bruk av ressursgrupper</span><span class="sxs-lookup"><span data-stu-id="beb74-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="beb74-212">**Eksempel 1:** Du har definert en ressursgruppe for flere maskiner av samme modell.</span><span class="sxs-lookup"><span data-stu-id="beb74-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="beb74-213">I stedet for å tilordne den veiledningen for håndteringsinstruksjoner for maskinmodellen til hver relevante ressurs, kan du i stedet tilordne veiledningen til ressursgruppen som gjenspeiler denne maskinmodellen.</span><span class="sxs-lookup"><span data-stu-id="beb74-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="beb74-214">**Eksempel 2:** Du har definert en ressursgruppe for en arbeidscelle som inneholder forskjellige maskiner, og du har en veiledning som inneholder generelle instruksjoner for hvordan du vedlikeholder arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="beb74-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="beb74-215">Veiledningen gjelder alle produksjonsaktiviteter i denne arbeidscellen.</span><span class="sxs-lookup"><span data-stu-id="beb74-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="beb74-216">Legge en veiledning til en ressursgruppe:</span><span class="sxs-lookup"><span data-stu-id="beb74-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="beb74-217">Slik legger du en veiledning til en ressursgruppe:</span><span class="sxs-lookup"><span data-stu-id="beb74-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="beb74-218">Gå til **Produksjonskontroll \> Oppsett \> Ressurser \> Ressursgrupper** .</span><span class="sxs-lookup"><span data-stu-id="beb74-218">Go to **Production control \> Setup \> Resources \> Resource groups** .</span></span>
1. <span data-ttu-id="beb74-219">Velg ressursgruppen du vil tilordne en veiledning til, fra listeruten.</span><span class="sxs-lookup"><span data-stu-id="beb74-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-220">Vis hurtigfanen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="beb74-221">Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="beb74-222">Det blir lagt til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="beb74-223">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="beb74-224">Hvis du har et stort antall veiledninger, kan du filtrere listen for å finne den du leter etter.</span><span class="sxs-lookup"><span data-stu-id="beb74-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="beb74-225">![Legge en veiledning til en ressursgruppe](media/instruction-guides-resourcegroup.png "Legge en veiledning til en ressursgruppe")</span><span class="sxs-lookup"><span data-stu-id="beb74-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="beb74-226">Knytte en veiledning til et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="beb74-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="beb74-227">Du kan legge en veiledning til alle [frigitte produkter](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="beb74-228">Vanlig scenario ved bruk av frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="beb74-228">Typical scenario using released products</span></span>

<span data-ttu-id="beb74-229">Veiledninger på produktnivå kan hjelpe produksjonsarbeidere med instruksjoner som er relevante for drift av systemet eller håndtering av et bestemt frigitt produkt eller vare.</span><span class="sxs-lookup"><span data-stu-id="beb74-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="beb74-230">Legg en veiledning til et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="beb74-230">Add a Guide to a released product</span></span>

<span data-ttu-id="beb74-231">Slik legger du en veiledning til et frigitt produkt:</span><span class="sxs-lookup"><span data-stu-id="beb74-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="beb74-232">Gå til **Behandling av produksjonsinformasjon \> Produkter \> Frigitte produkter** .</span><span class="sxs-lookup"><span data-stu-id="beb74-232">Go to **Production information management \> Products \> Released products** .</span></span>
1. <span data-ttu-id="beb74-233">Åpne produktet du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-234">Åpne kategorien **Utvikling** i handlingsruten, og velg **Tilknyttede veiledninger** fra **Vis** -gruppen.</span><span class="sxs-lookup"><span data-stu-id="beb74-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides** .</span></span>
1. <span data-ttu-id="beb74-235">Siden **Tilknyttede veiledninger** åpnes for det valgte produktet.</span><span class="sxs-lookup"><span data-stu-id="beb74-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="beb74-236">Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="beb74-237">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-238">![Legge en veiledning til et frigitt produkt](media/instruction-guides-ReleasedProduct-AddGuides.png "Legge en veiledning til et frigitt produkt")</span><span class="sxs-lookup"><span data-stu-id="beb74-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="beb74-239">Knytte en veiledning til en formel</span><span class="sxs-lookup"><span data-stu-id="beb74-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="beb74-240">Du kan legge en veiledning til alle [formler](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="beb74-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="beb74-241">Vanlig scenario ved bruk av formler</span><span class="sxs-lookup"><span data-stu-id="beb74-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="beb74-242">Veiledninger på formelnivå gir produksjonsarbeidere veiledning for håndteringsinstruksjoner i konteksten til en formel eller oppskrift.</span><span class="sxs-lookup"><span data-stu-id="beb74-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="beb74-243">Veiledninger kan også tilordnes til versjoner av en formel.</span><span class="sxs-lookup"><span data-stu-id="beb74-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="beb74-244">Du kan tilordne veiledning som er relevante for produksjonsprosesser, basert på en formel, til en rute, ruteversjon eller ruteoperasjonsrelasjoner.</span><span class="sxs-lookup"><span data-stu-id="beb74-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="beb74-245">Veiledninger kan for øyeblikket ikke knyttes til individuelle formellinjer.</span><span class="sxs-lookup"><span data-stu-id="beb74-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="beb74-246">Legg en veiledning til en formel</span><span class="sxs-lookup"><span data-stu-id="beb74-246">Add a Guide to a formula</span></span>

<span data-ttu-id="beb74-247">Slik legger du en veiledning til en formel:</span><span class="sxs-lookup"><span data-stu-id="beb74-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="beb74-248">Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Formler** .</span><span class="sxs-lookup"><span data-stu-id="beb74-248">Go to **Production information management \> Bills of materials and formulas \> Formulas** .</span></span>
1. <span data-ttu-id="beb74-249">Åpne formelen du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-250">Åpne kategorien **Topptekst** over den øverste hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="beb74-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="beb74-251">Vis hurtigfanen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="beb74-252">Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="beb74-253">Det blir lagt til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="beb74-254">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-255">![Legge en veiledning til en formel](media/instruction-guides-Formula.png "Legge en veiledning til en formel")</span><span class="sxs-lookup"><span data-stu-id="beb74-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="beb74-256">Knytte en veiledning til en formelversjon</span><span class="sxs-lookup"><span data-stu-id="beb74-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="beb74-257">Du kan legge en veiledning til alle [formelversjoner](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="beb74-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="beb74-258">Vanlig scenario ved bruk av formelversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="beb74-259">Veiledninger som er knyttet til en individuell versjon av en formel, gir produksjonsarbeidere instruksjoner som går gjennom produksjonen av denne versjonen av formeloppskriften.</span><span class="sxs-lookup"><span data-stu-id="beb74-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="beb74-260">Du kan tilordne veiledning som er relevante for produksjonsprosesser, basert på denne formelversjonen, til en rute, ruteversjon eller ruteoperasjonsrelasjoner.</span><span class="sxs-lookup"><span data-stu-id="beb74-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="beb74-261">Veiledninger kan for øyeblikket ikke knyttes til individuelle formellinjer.</span><span class="sxs-lookup"><span data-stu-id="beb74-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="beb74-262">Legg en veiledning til en formelversjon</span><span class="sxs-lookup"><span data-stu-id="beb74-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="beb74-263">Slik legger du en veiledning til en formelversjon:</span><span class="sxs-lookup"><span data-stu-id="beb74-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="beb74-264">Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Formler** .</span><span class="sxs-lookup"><span data-stu-id="beb74-264">Go to **Production information management \> Bills of materials and formulas \> Formulas** .</span></span>
1. <span data-ttu-id="beb74-265">Åpne formelen som inneholder en versjon du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-266">Åpne kategorien **Topptekst** over den øverste hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="beb74-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="beb74-267">I hurtigfanen **Formelversjoner** velger du versjonen du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-268">Velg **Tilknyttede veiledninger** på verktøylinjen **Formelversjoner** .</span><span class="sxs-lookup"><span data-stu-id="beb74-268">On the **Formula versions** toolbar, select **Associated Guides** .</span></span>
    <span data-ttu-id="beb74-269">![Åpne veiledningene som er knyttet til en valgt formelversjon](media/instruction-guides-FormulaVersion.png "Åpne veiledningene som er knyttet til en valgt formelversjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="beb74-270">Siden **Tilknyttede veiledninger** åpnes for formelversjonen.</span><span class="sxs-lookup"><span data-stu-id="beb74-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="beb74-271">Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="beb74-272">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-273">![Legge en veiledning til en formelversjon](media/instruction-guides-FormulaVersionAddGuide.png "Legge en veiledning til en formelversjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="beb74-274">Knytte en veiledning til en stykkliste</span><span class="sxs-lookup"><span data-stu-id="beb74-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="beb74-275">Du kan legge en veiledning til alle [stykklister](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="beb74-276">Vanlig scenario ved bruk av stykklister</span><span class="sxs-lookup"><span data-stu-id="beb74-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="beb74-277">Veiledninger som er knyttet til en stykkliste, gir produksjonsarbeidere instruksjoner som forklarer klargjøring og håndtering av materiale fra en stykkliste.</span><span class="sxs-lookup"><span data-stu-id="beb74-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="beb74-278">Veiledninger kan også tilordnes til versjoner av en stykkliste.</span><span class="sxs-lookup"><span data-stu-id="beb74-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="beb74-279">Veiledninger kan for øyeblikket ikke knyttes til individuelle stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="beb74-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="beb74-280">Legg en veiledning til en stykkliste</span><span class="sxs-lookup"><span data-stu-id="beb74-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="beb74-281">Slik legger du en veiledning til en stykkliste:</span><span class="sxs-lookup"><span data-stu-id="beb74-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="beb74-282">Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Stykklister** .</span><span class="sxs-lookup"><span data-stu-id="beb74-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials** .</span></span>
1. <span data-ttu-id="beb74-283">Åpne stykklisten du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-284">Åpne kategorien **Topptekst** over den øverste hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="beb74-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="beb74-285">Vis hurtigfanen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="beb74-286">Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="beb74-287">Det blir lagt til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="beb74-288">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-289">![Legge en veiledning til en stykkliste](media/instruction-guides-BOM.png "Legge en veiledning til en stykkliste")</span><span class="sxs-lookup"><span data-stu-id="beb74-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="beb74-290">Knytte en veiledning til en stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="beb74-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="beb74-291">Du kan legge en veiledning til alle [stykklistversjoner](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="beb74-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="beb74-292">Vanlig scenario ved bruk av stykklistversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="beb74-293">Veiledninger som er knyttet til en enkelt stykklisteversjon, gir produksjonsarbeidere instruksjoner som forklarer klargjøring og håndtering av materiale for en stykklisteversjon som er forskjellig fra den generelle stykklisten eller andre versjoner av den.</span><span class="sxs-lookup"><span data-stu-id="beb74-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="beb74-294">Veiledninger kan for øyeblikket ikke knyttes til individuelle stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="beb74-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="beb74-295">Legg en veiledning til en stykklisteversjon</span><span class="sxs-lookup"><span data-stu-id="beb74-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="beb74-296">Slik legger du en veiledning til en stykklisteversjon:</span><span class="sxs-lookup"><span data-stu-id="beb74-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="beb74-297">Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Stykklister** .</span><span class="sxs-lookup"><span data-stu-id="beb74-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials** .</span></span>
1. <span data-ttu-id="beb74-298">Åpne stykklisten som inneholder en versjon du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-299">Åpne kategorien **Topptekst** over den øverste hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="beb74-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="beb74-300">I hurtigfanen **Stykklisteversjoner** velger du versjonen du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-301">Velg **Tilknyttede veiledninger** på verktøylinjen **Stykklisteversjoner** .</span><span class="sxs-lookup"><span data-stu-id="beb74-301">On the **BOM versions** toolbar, select **Associated Guides** .</span></span>
    <span data-ttu-id="beb74-302">![Åpne veiledningene som er knyttet til en valgt stykklisteversjon](media/instruction-guides-BOMVersion.png "Åpne veiledningene som er knyttet til en valgt stykklisteversjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="beb74-303">Siden **Tilknyttede veiledninger** åpnes for stykklisteversjonen.</span><span class="sxs-lookup"><span data-stu-id="beb74-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="beb74-304">Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="beb74-305">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-306">![Legge en veiledning til en stykklisteversjon](media/instruction-guides-BOMVersionAddGuide.png "Legge en veiledning til en stykklisteversjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="beb74-307">Knytte en veiledning til en rute</span><span class="sxs-lookup"><span data-stu-id="beb74-307">Associate a Guide to a route</span></span>

<span data-ttu-id="beb74-308">Du kan legge en veiledning til alle [ruter](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="beb74-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="beb74-309">Vanlig scenario ved bruk av ruter</span><span class="sxs-lookup"><span data-stu-id="beb74-309">Typical scenario using routes</span></span>

<span data-ttu-id="beb74-310">Ruter brukes vanligvis til å angi hvordan et bestemt frigitt produkt skal produseres basert på en stykkliste eller stykklisteversjon, og med et sett med ressurser eller ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="beb74-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="beb74-311">Tilordne en veiledning til en rute for å gi trinnvise instruksjoner for den respektive produksjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="beb74-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="beb74-312">Legg en veiledning til en rute</span><span class="sxs-lookup"><span data-stu-id="beb74-312">Add a Guide to a route</span></span>

<span data-ttu-id="beb74-313">Slik legger du en veiledning til en rute:</span><span class="sxs-lookup"><span data-stu-id="beb74-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="beb74-314">Gå til **Produksjonskontroll \> Alle ruter** .</span><span class="sxs-lookup"><span data-stu-id="beb74-314">Go to **Production control \> All routes** .</span></span>
1. <span data-ttu-id="beb74-315">Åpne ruten du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-316">Vis hurtigfanen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="beb74-317">Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger** .</span><span class="sxs-lookup"><span data-stu-id="beb74-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="beb74-318">Det blir lagt til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="beb74-319">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-320">![Legge en veiledning til en rute](media/instruction-guides-Route.png "Legge en veiledning til en rute")</span><span class="sxs-lookup"><span data-stu-id="beb74-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="beb74-321">Knytte en veiledning til en ruteversjon</span><span class="sxs-lookup"><span data-stu-id="beb74-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="beb74-322">Du kan legge en veiledning til alle [ruteversjoner](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="beb74-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="beb74-323">Vanlig scenario ved bruk av ruteversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-323">Typical scenario using route versions</span></span>

<span data-ttu-id="beb74-324">Ruteversjoner brukes vanligvis til å angi varianter av produksjonsprosesser basert på en eksisterende rute.</span><span class="sxs-lookup"><span data-stu-id="beb74-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="beb74-325">Du kan tilordne ulike veiledninger til hver ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="beb74-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="beb74-326">Legg en veiledning til en ruteversjon</span><span class="sxs-lookup"><span data-stu-id="beb74-326">Add a Guide to a route version</span></span>

<span data-ttu-id="beb74-327">Slik legger du en veiledning til en ruteversjon:</span><span class="sxs-lookup"><span data-stu-id="beb74-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="beb74-328">Gå til **Produksjonskontroll \> Alle ruter** .</span><span class="sxs-lookup"><span data-stu-id="beb74-328">Go to **Production control \> All routes** .</span></span>
1. <span data-ttu-id="beb74-329">Åpne ruten du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-330">I hurtigfanen **Versjoner** velger du versjonen du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-331">Velg **Tilknyttede veiledninger** på verktøylinjen **Versjoner** .</span><span class="sxs-lookup"><span data-stu-id="beb74-331">On the **Versions** toolbar, select **Associated Guides** .</span></span>
    <span data-ttu-id="beb74-332">![Åpne veiledningene som er knyttet til en valgt ruteversjon](media/instruction-guides-RouteVersion.png "Åpne veiledningene som er knyttet til en valgt ruteversjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="beb74-333">Siden **Tilknyttede veiledninger** åpnes for stykklisteversjonen.</span><span class="sxs-lookup"><span data-stu-id="beb74-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="beb74-334">Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="beb74-335">For den nye linjen bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="beb74-336">![Legge en veiledning til en ruteversjon](media/instruction-guides-RouteVersionAddGuide.png "Legge en veiledning til en ruteversjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="beb74-337">Knytte en veiledning til en ruteoperasjonsrelasjon</span><span class="sxs-lookup"><span data-stu-id="beb74-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="beb74-338">Du kan legge en veiledning til alle [ruteoperasjonsrelasjoner](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="beb74-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="beb74-339">Vanlig scenario ved bruk av ruteoperasjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="beb74-340">Operasjonsrelasjoner er den mest spesifikke måten å legge til veiledning i en produktprosess og relaterte operasjoner.</span><span class="sxs-lookup"><span data-stu-id="beb74-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="beb74-341">Du kan angi veiledning for hver operasjon i en rute, og angi ulike veiledninger for alle typer relasjonskontekster som er angitt for en rute, for eksempel for spesifikke varer, konfigurasjoner og mye mer.</span><span class="sxs-lookup"><span data-stu-id="beb74-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="beb74-342">Du kan også angi hvilke faser i operasjonen veiledningen gjelder for (for eksempel oppsett, kø, prosess eller transport).</span><span class="sxs-lookup"><span data-stu-id="beb74-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="beb74-343">Hvis du angir veiledninger for flere operasjonsrelasjoner for en rute, vil det bare være veiledninger fra den mest spesifikke relasjonen som vises i produksjonen for den genererte jobben.</span><span class="sxs-lookup"><span data-stu-id="beb74-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="beb74-344">Legg en veiledning til en ruteoperasjonsrelasjon</span><span class="sxs-lookup"><span data-stu-id="beb74-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="beb74-345">Slik legger du en veiledning til en ruteoperasjonsrelasjon:</span><span class="sxs-lookup"><span data-stu-id="beb74-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="beb74-346">Gå til **Produksjonskontroll \> Alle ruter** .</span><span class="sxs-lookup"><span data-stu-id="beb74-346">Go to **Production control \> All routes** .</span></span>
1. <span data-ttu-id="beb74-347">Åpne ruten du vil tilordne en veiledning til.</span><span class="sxs-lookup"><span data-stu-id="beb74-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="beb74-348">Åpne kategorien **Rute** i handlingsruten, og gå til **Vedlikehold** -gruppen og velg **Rutedetaljer** .</span><span class="sxs-lookup"><span data-stu-id="beb74-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details** .</span></span>
1. <span data-ttu-id="beb74-349">Siden **Rutedetaljer** åpnes for den valgte ruten.</span><span class="sxs-lookup"><span data-stu-id="beb74-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="beb74-350">I rutenettet øverst velger du operasjonen du vil gi veiledning for.</span><span class="sxs-lookup"><span data-stu-id="beb74-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="beb74-351">I rutenettet nederst velger du en spesifikk relasjon (eller den generelle **Alle** -relasjonen).</span><span class="sxs-lookup"><span data-stu-id="beb74-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="beb74-352">![Velg en operasjon og deretter en relasjon](media/instruction-guides-RouteOperationRelation.png "Velg en operasjon og deretter en relasjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="beb74-353">Over rutenettet nederst åpner du kategorien **Tilknyttede veiledninger** . Kategorien ![Tilknyttede veiledninger](media/instruction-guides-RouteOperationRelation-AddGuide.png "Kategorien Tilknyttede veiledninger")</span><span class="sxs-lookup"><span data-stu-id="beb74-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="beb74-354">Velg **Legg til** fra verktøylinjen øverst i rutenettet nederst for å legge til en ny linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="beb74-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="beb74-355">For den nye raden bruker du rullegardinlisten i **Navn** -kolonnen til å velge veiledningen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="beb74-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="beb74-356">I resten av raden merker du av for hver kontekst der den valgte veiledningen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="beb74-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="beb74-357">Du kan legge til én eller flere veiledninger for hvert trinn i hver operasjon.</span><span class="sxs-lookup"><span data-stu-id="beb74-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="beb74-358">Velg veiledninger fra kjøringsgrensesnittet for produksjon</span><span class="sxs-lookup"><span data-stu-id="beb74-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="beb74-359">Når en arbeider åpner en jobbliste i kjøringsgrensesnittet for produksjon, finner Supply Chain Management de relevante veiledningene for jobbene som vises.</span><span class="sxs-lookup"><span data-stu-id="beb74-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="beb74-360">Bruk **Veiledninger** -knappen til å vise de relevante veiledningene.</span><span class="sxs-lookup"><span data-stu-id="beb74-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="beb74-361">![Veiledninger-knappen i kjøringsgrensesnittet for produksjon](media/instruction-guides-Shopfloor1.png "Veiledninger-knappen i kjøringsgrensesnittet for produksjon")</span><span class="sxs-lookup"><span data-stu-id="beb74-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="beb74-362">Deretter må du ta på en HoloLens og gå til den aktuelle veiledningen ved å se på QR-koden og aktivere den aktuelle veiledningen.</span><span class="sxs-lookup"><span data-stu-id="beb74-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="beb74-363">![QR-kode for å gå til veiledninger ved hjelp av en HoloLens](media/instruction-guides-Shopfloor2.png "QR-kode for å gå til veiledninger ved hjelp av en HoloLens")</span><span class="sxs-lookup"><span data-stu-id="beb74-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="beb74-364">Løse logikken for valg av veiledninger</span><span class="sxs-lookup"><span data-stu-id="beb74-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="beb74-365">Du kan legge til veiledninger for følgende produksjonsdata:</span><span class="sxs-lookup"><span data-stu-id="beb74-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="beb74-366">Ressurser</span><span class="sxs-lookup"><span data-stu-id="beb74-366">Resources</span></span>](#resources)
- [<span data-ttu-id="beb74-367">Ressursgrupper</span><span class="sxs-lookup"><span data-stu-id="beb74-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="beb74-368">Frigitte produkter</span><span class="sxs-lookup"><span data-stu-id="beb74-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="beb74-369">Formler</span><span class="sxs-lookup"><span data-stu-id="beb74-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="beb74-370">Formelversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="beb74-371">Stykklister</span><span class="sxs-lookup"><span data-stu-id="beb74-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="beb74-372">Stykklisteversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="beb74-373">Ruter</span><span class="sxs-lookup"><span data-stu-id="beb74-373">Routes</span></span>](#routes)
- [<span data-ttu-id="beb74-374">Ruteversjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="beb74-375">Ruteoperasjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="beb74-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="beb74-376">Når Supply Chain Management genererer jobbene for produksjonen, vil det samle de relevante veiledningene fra disse kildene.</span><span class="sxs-lookup"><span data-stu-id="beb74-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="beb74-377">Legg merke til de viktigste reglene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="beb74-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="beb74-378">Hvis du knytter en stykklisteversjon eller formelversjon til en rute eller produksjonsordre, vil eventuelle veiledninger som er knyttet til denne versjonen, og også veiledningene som er knyttet til den overordnede stykklisten eller formelen til denne versjonen, vises for jobben.</span><span class="sxs-lookup"><span data-stu-id="beb74-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="beb74-379">Hvis du knytter en ruteversjon eller formelversjon til en rute eller produksjonsordre, vil eventuelle veiledninger som er knyttet til denne versjonen, og også veiledningene som er knyttet til den overordnede ruten eller formelen til denne versjonen, vises for jobben.</span><span class="sxs-lookup"><span data-stu-id="beb74-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="beb74-380">Hvis du definerer flere ruteoperasjonsrelasjoner som omfatter *Alle* -relasjonen og tilordner veiledninger til disse, vil bare veiledningene fra den mest spesifikke relasjonen vises for jobben.</span><span class="sxs-lookup"><span data-stu-id="beb74-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="beb74-381">![Diagram for å løse de relevante veiledningene](media/instruction-guides-Resolve.png "Diagram for å løse de relevante veiledningene")</span><span class="sxs-lookup"><span data-stu-id="beb74-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
