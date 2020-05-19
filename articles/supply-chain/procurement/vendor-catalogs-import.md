---
title: Import leverandørkataloger
description: Dette emnet beskriver prosessen for å importere leverandørkatalogdata.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 608d2b57bb4d5ab80d75b22ed5c8a4df5263e5f3
ms.sourcegitcommit: 86052c58e3c365c443bd6f37ad1054bea395e21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2020
ms.locfileid: "3338314"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="49508-103">Import leverandørkataloger</span><span class="sxs-lookup"><span data-stu-id="49508-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="49508-104">Import av leverandørkataloger</span><span class="sxs-lookup"><span data-stu-id="49508-104">Vendor catalogs import</span></span>

<span data-ttu-id="49508-105">I Dynamics 365 Supply Chain Management kan innkjøpere opprette og vedlikeholde kataloger som firmaets ansatte kan bruke når de bestiller varer og tjenester til internt bruk.</span><span class="sxs-lookup"><span data-stu-id="49508-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="49508-106">Hvis du vil opprette en innkjøpskatalog, kan du legge til varene og tjenestene som du vil gjøre tilgjengelig for ansatte, enten ved å importere produktkatalogdata eller ved å legge til produktkatalogdata manuelt til produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="49508-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="49508-107">Du kan laste opp katalogdataene som sendes av en leverandør, fra Microsoft Dynamics 365-klienten.</span><span class="sxs-lookup"><span data-stu-id="49508-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="49508-108">Produktdataene som en leverandøre sender til deg, i form av en PriKat-fil, må være i XML-filformat.</span><span class="sxs-lookup"><span data-stu-id="49508-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="49508-109">PriKat-filen bør inneholde detaljene for produktene som leverandøren leverer til firmaet.</span><span class="sxs-lookup"><span data-stu-id="49508-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="49508-110">Import leverandørkatalogdata</span><span class="sxs-lookup"><span data-stu-id="49508-110">Import vendor catalog data</span></span>

<span data-ttu-id="49508-111">Du må utføre følgende oppgaver for å importere leverandørkatalogdata:</span><span class="sxs-lookup"><span data-stu-id="49508-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="49508-112">Definer et prosjekt i arbeidsområdet Databehandling der du har definert regler for tilordning av data.</span><span class="sxs-lookup"><span data-stu-id="49508-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="49508-113">Velg **Databehandling**, og velg deretter **Definer roller for dataprosjekter**.</span><span class="sxs-lookup"><span data-stu-id="49508-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="49508-114">Definer et innkjøpskategorihierarki, og tilordne leverandører til innkjøpskategoriene.</span><span class="sxs-lookup"><span data-stu-id="49508-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="49508-115">Hvis du bruker varekoder, kan du legge til varekodene i innkjøpskategoriene.</span><span class="sxs-lookup"><span data-stu-id="49508-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="49508-116">Hvis du vil ha informasjon om hvordan du definerer et innkjøpskategorihierarki, se [Definer et innkjøpskategorihierarki](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="49508-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="49508-117">Konfigurer leverandøren for katalogimport.</span><span class="sxs-lookup"><span data-stu-id="49508-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="49508-118">Velg en leverandør, og velg deretter **Innkjøp** > **Oppsett** > **Konfigurer leverandør for katalogimport**.</span><span class="sxs-lookup"><span data-stu-id="49508-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="49508-119">Konfigurer arbeidsflyt for katalogimport.</span><span class="sxs-lookup"><span data-stu-id="49508-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="49508-120">Opprett en mal for PriKat-filen, og del den med leverandøren.</span><span class="sxs-lookup"><span data-stu-id="49508-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="49508-121">Velg **Innkjøp og leverandører** \> **Felles** \> **Kataloger** \> **Leverandørkataloger** for å opprette en leverandørkatalog.</span><span class="sxs-lookup"><span data-stu-id="49508-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="49508-122">PriKat-filene du mottar fra leverandøren, er gruppert i denne katalogen.</span><span class="sxs-lookup"><span data-stu-id="49508-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="49508-123">Last opp PriKat-filen.</span><span class="sxs-lookup"><span data-stu-id="49508-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="49508-124">Gå gjennom, godkjenn eller avvis produktene i leverandørkatalogen.</span><span class="sxs-lookup"><span data-stu-id="49508-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="49508-125">Produktene tilordnes automatisk til innkjøpskategoriene.</span><span class="sxs-lookup"><span data-stu-id="49508-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="49508-126">Godkjente produkter legges til i produktstandarden og frigis til de valgte juridiske enhetene.</span><span class="sxs-lookup"><span data-stu-id="49508-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="49508-127">Bare godkjente produkter kan legges til i innkjøpskatalogen.</span><span class="sxs-lookup"><span data-stu-id="49508-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="49508-128">Generere en filmal for katalogimport</span><span class="sxs-lookup"><span data-stu-id="49508-128">Generate a catalog import file template</span></span>

<span data-ttu-id="49508-129">Filmalen for katalogimport er en XSD-fil som bruker til å opprette en PriKat-fil for produktene til en leverandør.</span><span class="sxs-lookup"><span data-stu-id="49508-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="49508-130">Du kan bruke PriKat-filen til å opprette en ny katalog, erstatte en eksisterende katalog eller endre en eksisterende katalog.</span><span class="sxs-lookup"><span data-stu-id="49508-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="49508-131">Velg **Innkjøp og leverandører** \> **Kataloger** \> **Leverandørkataloger**, og dobbeltklikk katalogen du vil arbeide med.</span><span class="sxs-lookup"><span data-stu-id="49508-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="49508-132">Last ned en gjeldende katalogmportmal (XSD-fil).</span><span class="sxs-lookup"><span data-stu-id="49508-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="49508-133">På siden **Oppdater katalog**, i **handlingsruten** i kategorien **Kataloger** i gruppen **Beslektet informasjon**, klikker du **Generer katalogmal**, og velger **Innkjøpskategori**.</span><span class="sxs-lookup"><span data-stu-id="49508-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="49508-134">I **innkjøpskategorien** kan du generere en katalogmal som omfatter innkjøpskategoriene der leverandøren er autorisert til å levere produkter.</span><span class="sxs-lookup"><span data-stu-id="49508-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="49508-135">Velg plasseringen der du vil lagre katalogfilmalen og filen, i dialogboksen **Lagre som**.</span><span class="sxs-lookup"><span data-stu-id="49508-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="49508-136">Hvis du vil ha mer informasjon og eksempler, kan du se dette blogginnlegget: [Leverandørkataloger i Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="49508-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
