---
title: Program for salgssted (POS) og språkinnstillinger for bruker
description: Dette emnet beskriver hvordan du endrer språkinnstillinger i Modern POS (MPOS) og Cloud POS.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c5087ee04030a76aef774871b88b7970391723c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804387"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="f2fc1-103">Program for salgssted (POS) og språkinnstillinger for bruker</span><span class="sxs-lookup"><span data-stu-id="f2fc1-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2fc1-104">Dette emnet beskriver hvordan du endrer språkinnstillinger i Modern POS (MPOS) og Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="f2fc1-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f2fc1-105">Overview</span></span>
<span data-ttu-id="f2fc1-106">Modern POS (MPOS) og Cloud POS støtter miljøer der innstillinger for språk og oversettelser kan variere mellom lageret og brukerinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="f2fc1-107">Butikken kan for eksempel være plassert i et område der engelsk er mest vanlig for kundene, men noen arbeidere foretrekker å bruke programmet med franske oversettelser.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="f2fc1-108">Språk for data</span><span class="sxs-lookup"><span data-stu-id="f2fc1-108">Data language</span></span>

<span data-ttu-id="f2fc1-109">Uavhengig av brukerens innstillinger, vil MPOS og Cloud POS alltid bruke butikkens språkinnstillinger for å bestemme oversettelser som brukes for data.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="f2fc1-110">Dette sikrer at alle brukere og kunder får en ensartet opplevelse.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="f2fc1-111">Eksempler på data omfatter:</span><span class="sxs-lookup"><span data-stu-id="f2fc1-111">Examples of data include:</span></span>

- <span data-ttu-id="f2fc1-112">Produkter</span><span class="sxs-lookup"><span data-stu-id="f2fc1-112">Products</span></span>
- <span data-ttu-id="f2fc1-113">Attributter og verdier</span><span class="sxs-lookup"><span data-stu-id="f2fc1-113">Attributes and values</span></span>
- <span data-ttu-id="f2fc1-114">Kategorinavn</span><span class="sxs-lookup"><span data-stu-id="f2fc1-114">Category names</span></span>
- <span data-ttu-id="f2fc1-115">Transaksjonsmottak for utskrift eller sending via e-post</span><span class="sxs-lookup"><span data-stu-id="f2fc1-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="f2fc1-116">Navn på betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="f2fc1-116">Payment method names</span></span>
- <span data-ttu-id="f2fc1-117">Linjevisningmeldinger</span><span class="sxs-lookup"><span data-stu-id="f2fc1-117">Line display messages</span></span>

<span data-ttu-id="f2fc1-118">Butikkens språk brukes også for POS-påloggingshovedskjermen fordi brukeren ikke er kjent før du logger på.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="f2fc1-119">Hvis en oversettelse ikke er tilgjengelig for butikkens språk, vil POS gå tilbake til selskapets språk.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="f2fc1-120">Konfigurere språkinnstillingene for butikken</span><span class="sxs-lookup"><span data-stu-id="f2fc1-120">Configuring the store's language setting</span></span>

<span data-ttu-id="f2fc1-121">Butikkens språkinnstillinger settes fra **Alle butikker** på siden **Butikk** under **Generelt &gt; Regionale innstillinger &gt; Språk**.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="f2fc1-122">Bruk rullegardinlisten for å velge språk for hver butikk.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="f2fc1-123">Språk for brukergrensesnittet</span><span class="sxs-lookup"><span data-stu-id="f2fc1-123">User interface language</span></span>

<span data-ttu-id="f2fc1-124">POS-brukerens språkinnstilling bestemmer oversettelser som brukes i brukergrensesnittet for programmet.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="f2fc1-125">Dette inkluderer alle etiketter, menyer og lister som ikke anses data.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="f2fc1-126">Ett unntak er teksten som vises på POS-knappegrupper.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="f2fc1-127">Knappegruppene støtter ikke oversettelser, slik at de alltid vises teksten som er definert på-knappen.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="f2fc1-128">For å støtte oversatte knapper, må du kopiere og opprettholder egen knapp rutenett og tilordne dem til brukere etter behov.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="f2fc1-129">Konfigurere språkinnstillingene for brukeren</span><span class="sxs-lookup"><span data-stu-id="f2fc1-129">Configuring the user's language setting</span></span>

<span data-ttu-id="f2fc1-130">Salgsstedsbrukerens språkinnstillinger settes fra **Alle arbeidere** på siden **Arbeider** under **Retail og Commerce &gt; Språk**.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="f2fc1-131">Den angis ikke i hovedprofilkategorien. Denne innstillingen brukes ikke av salgssted.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="f2fc1-132">Hvis brukerens språk ikke er angitt eller den er satt til et språk der oversettelsene ikke er tilgjengelige, tilbakestiller Salgsstedet til butikkens språk.</span><span class="sxs-lookup"><span data-stu-id="f2fc1-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="f2fc1-133">Språket i Brukergrensesnittet  </span><span class="sxs-lookup"><span data-stu-id="f2fc1-133">UI language</span></span>                | <span data-ttu-id="f2fc1-134">Data-språk (produkter, kvitteringsformater, linjevisning, osv.)</span><span class="sxs-lookup"><span data-stu-id="f2fc1-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f2fc1-135">**Firma**</span><span class="sxs-lookup"><span data-stu-id="f2fc1-135">**Company**</span></span> | <span data-ttu-id="f2fc1-136">Standard</span><span class="sxs-lookup"><span data-stu-id="f2fc1-136">Default</span></span>                    | <span data-ttu-id="f2fc1-137">Standard</span><span class="sxs-lookup"><span data-stu-id="f2fc1-137">Default</span></span>                                                       |
| <span data-ttu-id="f2fc1-138">**Butikk**</span><span class="sxs-lookup"><span data-stu-id="f2fc1-138">**Store**</span></span>   | <span data-ttu-id="f2fc1-139">Overstyrer firma</span><span class="sxs-lookup"><span data-stu-id="f2fc1-139">Overrides company</span></span>          | <span data-ttu-id="f2fc1-140">Overstyrer firma</span><span class="sxs-lookup"><span data-stu-id="f2fc1-140">Overrides company</span></span>                                             |
| <span data-ttu-id="f2fc1-141">**Bruker**</span><span class="sxs-lookup"><span data-stu-id="f2fc1-141">**User**</span></span>    | <span data-ttu-id="f2fc1-142">Overstyrer butikk eller firma</span><span class="sxs-lookup"><span data-stu-id="f2fc1-142">Overrides store or company</span></span> | <span data-ttu-id="f2fc1-143">Aldri</span><span class="sxs-lookup"><span data-stu-id="f2fc1-143">Never</span></span>                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]