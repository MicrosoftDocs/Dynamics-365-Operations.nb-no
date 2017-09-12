---
title: Kostnadskategorier brukt i produksjonskontroll og i prosjektstyring og regnskap
description: "Enkelte typer produksjonsarbeid kan gjelde for prosjekttidsestimater og rapportering. Denne artikkelen inneholder informasjon om kostnadskategorier som må du definere for disse typene produksjonsarbeid for produksjon og prosjekter."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1fcc7914f2bb283a746b5e10993f91f949818473
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="c5c0b-104">Kostnadskategorier brukt i produksjonskontroll og i prosjektstyring og regnskap</span><span class="sxs-lookup"><span data-stu-id="c5c0b-104">Cost categories used in Production control and Project management accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c5c0b-105">Enkelte typer produksjonsarbeid kan gjelde for prosjekttidsestimater og rapportering.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="c5c0b-106">Denne artikkelen inneholder informasjon om kostnadskategorier som må du definere for disse typene produksjonsarbeid for produksjon og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="c5c0b-107">Enkelte typer produksjonsarbeid kan gjelde for prosjekttidsestimater og rapportering.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="c5c0b-108">I dette tilfellet kreves en kostnadskategori for produksjon og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="c5c0b-109">Det må defineres prosjektrelatert tilleggsinformasjon når en kostnadskategori brukes i produksjon og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="c5c0b-110">For eksempel så kan timekostnadene tilknyttet prosjektene, være forskjellige fra timekostnadene som er tilknyttet produksjonen.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="c5c0b-111">Du kan bruke siden **Kostnadskategorier** for å definere en kostnadskategori som brukes i produksjonsstyring og i prosjektstyring og regnskap.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> <span data-ttu-id="c5c0b-112">**Obs!** Kostnadsregnskap har en **Prosjektkategorier**-side, men denne siden har ingen relasjon til funksjonene som er beskrevet i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="c5c0b-113">Når du bruker en kostnadskategori i prosjekter, har **Kostnadskategorier**-siden flere kategorier som viser prosjektrelatert tilleggsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="c5c0b-114">Denne informasjonen inkluderer kategorigruppen, en linjeegenskap og finanskontoer som er tilordnet til kostnadskategorien.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="c5c0b-115">Kostnadskategorien må være tilordnet en kategorigruppe som støtter en transaksjonstype av typen **Timer**.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="c5c0b-116">Linjeegenskapen angir standardinformasjonen om hvordan rapporterte timer kan belastes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="c5c0b-117">Finanskontoene som er relatert til kostnader og salg, er vanligvis definert for kategorigruppen som er tilordnet til kostnadskategorien.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="c5c0b-118">Imidlertid kan bestemte kontoer defineres for en individuell kostnadskategori.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="c5c0b-119">Tilleggsknappene på **Kostnadskategorier**-siden gir tilgang til prosjektrelatert informasjon om en valgt kostnadskategori.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="c5c0b-120">Du kan for eksempel vise prosjektrelaterte transaksjoner, definere ansatte eller prosjekter, definere timekostnader og salgspriser og vise rapporter.</span><span class="sxs-lookup"><span data-stu-id="c5c0b-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




