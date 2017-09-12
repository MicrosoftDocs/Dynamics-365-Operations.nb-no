---
title: "Salgsstedsprogram og språkinnstillinger for bruker"
description: "Dette emnet beskriver hvordan du endrer språkinnstillinger i moderne salgssted for detaljhandel (MPOS) og skysalgssted."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a9b2d8dec04ed3653b2ebcfbd2492fc40d96b77b
ms.contentlocale: nb-no
ms.lasthandoff: 06/29/2017



---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="2241b-103">Salgsstedsprogram og språkinnstillinger for bruker</span><span class="sxs-lookup"><span data-stu-id="2241b-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="2241b-104">Dette emnet beskriver hvordan du endrer språkinnstillinger i moderne salgssted for detaljhandel (MPOS) og skysalgssted.</span><span class="sxs-lookup"><span data-stu-id="2241b-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="2241b-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="2241b-105">Overview</span></span>
========

<span data-ttu-id="2241b-106">Modern POS (MPOS) og Cloud POS for detaljhandelen støtter miljøer der innstillinger for språk og oversettelser kan variere mellom lageret og brukerinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="2241b-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="2241b-107">Butikken kan for eksempel være plassert i et område der engelsk er mest vanlig for kundene, men noen arbeidere foretrekker å bruke programmet med franske oversettelser.</span><span class="sxs-lookup"><span data-stu-id="2241b-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="2241b-108">Språk for data</span><span class="sxs-lookup"><span data-stu-id="2241b-108">Data language</span></span>
<span data-ttu-id="2241b-109">Uavhengig av brukerens innstillinger, vil MPOS og Cloud POS alltid bruke butikkens språkinnstillinger for å bestemme oversettelser som brukes for data.</span><span class="sxs-lookup"><span data-stu-id="2241b-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="2241b-110">Dette sikrer at alle brukere og kunder får en ensartet opplevelse.</span><span class="sxs-lookup"><span data-stu-id="2241b-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="2241b-111">Eksempler på data omfatter:</span><span class="sxs-lookup"><span data-stu-id="2241b-111">Examples of data include:</span></span>

-   <span data-ttu-id="2241b-112">Produkter</span><span class="sxs-lookup"><span data-stu-id="2241b-112">Products</span></span>
-   <span data-ttu-id="2241b-113">Attributter og verdier</span><span class="sxs-lookup"><span data-stu-id="2241b-113">Attributes and values</span></span>
-   <span data-ttu-id="2241b-114">Kategorinavn</span><span class="sxs-lookup"><span data-stu-id="2241b-114">Category names</span></span>
-   <span data-ttu-id="2241b-115">Transaksjonsmottak for utskrift eller sending via e-post</span><span class="sxs-lookup"><span data-stu-id="2241b-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="2241b-116">Navn på betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="2241b-116">Payment method names</span></span>
-   <span data-ttu-id="2241b-117">Linjevisningmeldinger</span><span class="sxs-lookup"><span data-stu-id="2241b-117">Line display messages</span></span>

<span data-ttu-id="2241b-118">Butikkens språk brukes også for POS-påloggingshovedskjermen fordi brukeren ikke er kjent før du logger på.</span><span class="sxs-lookup"><span data-stu-id="2241b-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="2241b-119">Hvis en oversettelse ikke er tilgjengelig for butikkens språk, vil POS gå tilbake til selskapets språk.</span><span class="sxs-lookup"><span data-stu-id="2241b-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="2241b-120">Konfigurere språkinnstillingene for butikken</span><span class="sxs-lookup"><span data-stu-id="2241b-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="2241b-121">Butikkens språkinnstillinger settes fra **Alle detaljhandelsbutikker** på siden **Detaljhandel** under **Generelt &gt; Regionale innstillinger &gt; Språk.</span><span class="sxs-lookup"><span data-stu-id="2241b-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="2241b-122">**Bruk rullegardinlisten for å velge språk for hver butikk.</span><span class="sxs-lookup"><span data-stu-id="2241b-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="2241b-123">Språk for brukergrensesnittet</span><span class="sxs-lookup"><span data-stu-id="2241b-123">User interface language</span></span>
<span data-ttu-id="2241b-124">POS-brukerens språkinnstilling bestemmer oversettelser som brukes i brukergrensesnittet for programmet.</span><span class="sxs-lookup"><span data-stu-id="2241b-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="2241b-125">Dette inkluderer alle etiketter, menyer og lister som ikke anses data.</span><span class="sxs-lookup"><span data-stu-id="2241b-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="2241b-126">Ett unntak er teksten som vises på POS-knappegrupper.</span><span class="sxs-lookup"><span data-stu-id="2241b-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="2241b-127">Knappegruppene støtter ikke oversettelser, slik at de alltid vises teksten som er definert på-knappen.</span><span class="sxs-lookup"><span data-stu-id="2241b-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="2241b-128">For å støtte oversatte knapper, må du kopiere og opprettholder egen knapp rutenett og tilordne dem til brukere etter behov.</span><span class="sxs-lookup"><span data-stu-id="2241b-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="2241b-129">Konfigurere språkinnstillingene for brukeren</span><span class="sxs-lookup"><span data-stu-id="2241b-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="2241b-130">Salgsstedsbrukerens språkinnstillinger settes fra **Alle arbeidere** på siden **Arbeider** under **Detaljhandel &gt; Språk**.</span><span class="sxs-lookup"><span data-stu-id="2241b-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="2241b-131">Det angis ikke i hovedprofilkategorien.</span><span class="sxs-lookup"><span data-stu-id="2241b-131">It is not set on the main Profile tab.</span></span>  <span data-ttu-id="2241b-132">Denne innstillingen brukes ikke av POS.</span><span class="sxs-lookup"><span data-stu-id="2241b-132">This setting is not used by POS.</span></span> <span data-ttu-id="2241b-133">Hvis brukerens språk ikke er angitt eller den er satt til et språk der oversettelsene ikke er tilgjengelige, tilbakestiller Salgsstedet til butikkens språk.</span><span class="sxs-lookup"><span data-stu-id="2241b-133">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="2241b-134">** **</span><span class="sxs-lookup"><span data-stu-id="2241b-134">** **</span></span>       | <span data-ttu-id="2241b-135">**Språket i Brukergrensesnittet** ** **</span><span class="sxs-lookup"><span data-stu-id="2241b-135">**UI language** ** **</span></span>      | <span data-ttu-id="2241b-136">**Data-språk (produkter, kvitteringsformater, linjevisning, osv.)**</span><span class="sxs-lookup"><span data-stu-id="2241b-136">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="2241b-137">**Firma**</span><span class="sxs-lookup"><span data-stu-id="2241b-137">**Company**</span></span> | <span data-ttu-id="2241b-138">Standard</span><span class="sxs-lookup"><span data-stu-id="2241b-138">Default</span></span>                    | <span data-ttu-id="2241b-139">Standard</span><span class="sxs-lookup"><span data-stu-id="2241b-139">Default</span></span>                                                           |
| <span data-ttu-id="2241b-140">**Butikk**</span><span class="sxs-lookup"><span data-stu-id="2241b-140">**Store**</span></span>   | <span data-ttu-id="2241b-141">Overstyrer firma</span><span class="sxs-lookup"><span data-stu-id="2241b-141">Overrides company</span></span>          | <span data-ttu-id="2241b-142">Overstyrer firma</span><span class="sxs-lookup"><span data-stu-id="2241b-142">Overrides company</span></span>                                                 |
| <span data-ttu-id="2241b-143">**Bruker**</span><span class="sxs-lookup"><span data-stu-id="2241b-143">**User**</span></span>    | <span data-ttu-id="2241b-144">Overstyrer butikk eller firma</span><span class="sxs-lookup"><span data-stu-id="2241b-144">Overrides store or company</span></span> | <span data-ttu-id="2241b-145">Aldri</span><span class="sxs-lookup"><span data-stu-id="2241b-145">Never</span></span>                                                             |






